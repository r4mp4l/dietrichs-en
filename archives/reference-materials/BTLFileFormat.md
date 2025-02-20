# Introduction to BTL: Rawparts, Nesting, and Process Ordering

## Core Concepts

BTL (Building Transfer Language) is a format designed specifically for timber manufacturing. Unlike general CAD formats, it combines three key aspects:
1. Raw material definition
2. Component nesting
3. Manufacturing process ordering

### 1. Rawparts: The Starting Material

A rawpart in BTL represents your blank piece of timber material, such as:
- CLT panels
- Glulam beams
- Solid timber sections

Each rawpart has:
- Dimensions (length, width, height)
- Material properties
- Coordinate system
- Grain direction (optional)

Example:
```
[RAWPART]
LENGTH: 4000    # 4 meter length
WIDTH: 200      # 200mm width
HEIGHT: 100     # 100mm height
MATERIAL: "GL24h"
```

### 2. Nesting: Parts on Rawparts

BTL allows multiple finished parts to be nested onto a single rawpart:
- Each part has a unique ID (UID)
- Parts are positioned using transformation matrices
- Multiple parts can share one rawpart
- Nesting optimizes material usage

Example structure:
```
Rawpart (4m Glulam beam)
├── Part A: Rafter (1.2m)
│   └── Position: (0,0,0)
├── Part B: Rafter (1.2m)
│   └── Position: (1500,0,0)
└── Part C: Beam End (0.8m)
    └── Position: (3000,0,0)
```

### 3. Process Ordering: Manufacturing Optimization

BTL uses a sophisticated process ordering system that prioritizes manufacturing efficiency over component completion:

#### Priority Mechanisms:
1. Explicit Priority Values
```
PRIORITY: Integer   # Higher number = higher priority
```

2. Process Groups
- Groups 1,2: Separating processes (cuts)
- Groups 3,4: In-between processes (drilling, routing)
- Group 0: Universal processes

3. Tool-based Optimization
- Processes using the same tool are grouped
- Minimizes tool changes
- Optimizes machine movements

Example Process Flow:
```
Rawpart with 3 parts needing:
Part A: Cut, Drill(8mm), Slot
Part B: Cut, Drill(8mm)
Part C: Cut, Slot

Optimized Process Order:
1. All Cuts (same saw)
2. All 8mm Drilling (same drill bit)
3. All Slots (same router bit)
```

## Real-World Example

Consider manufacturing roof rafters:

```
[RAWPART]
TYPE: GLULAM
LENGTH: 6000

  [PART] "Rafter 1"
  - Cut to 2000mm
  - Bird's mouth joint
  - 8mm holes for fixings

  [PART] "Rafter 2"
  - Cut to 2000mm
  - Bird's mouth joint
  - 8mm holes for fixings

Process Order:
1. Cut both rafters to length (same saw)
2. Cut both bird's mouth joints (same tooling)
3. Drill all 8mm holes (same drill bit)
```

This ordering:
- Minimizes tool changes
- Optimizes machine movements
- Reduces manufacturing time
- Improves efficiency

## Key Differences from Traditional CAM

1. Component-Centric vs Process-Centric
- Traditional CAM: Complete one component before starting next
- BTL: Optimize across all components for efficiency

2. Material Usage
- Traditional CAM: Often one part per raw material
- BTL: Multiple parts nested on one rawpart

3. Process Organization
- Traditional CAM: Sequential by component
- BTL: Organized by tool and process type

## Comparison with STEP and IFC

### STEP (Standard for Exchange of Product Data)
1. Purpose & Scope
- General-purpose CAD/CAM exchange format
- Focuses on precise geometry and tolerances
- Handles assembly relationships
- Used across many industries (not timber-specific)

2. Key Differences from BTL
- More complex and verbose
- No timber-specific features
- Lacks optimization for wood manufacturing
- More detailed tolerance specifications
- No built-in nesting capabilities
- Process ordering is not inherent

3. When to Use STEP
- Exchanging general CAD data
- Need for detailed tolerancing
- Working with non-timber materials
- Complex geometric definitions

### IFC (Industry Foundation Classes)
1. Purpose & Scope
- Building Information Modeling (BIM) format
- Focuses on building elements and relationships
- Contains project and construction information
- Used for full building documentation

2. Key Differences from BTL
- Building-level focus vs manufacturing focus
- No manufacturing process information
- Different type of nesting (spatial vs manufacturing)
- Contains non-geometric information (cost, scheduling)
- No machine processing instructions
- No material optimization features

3. When to Use IFC
- Building-level coordination
- Design documentation
- Project management
- Multi-discipline coordination

### Format Selection Guide
Use BTL when:
- Manufacturing timber components
- Need CNC machine instructions
- Optimizing material usage
- Timber-specific processing

Use STEP when:
- Exchanging general CAD geometry
- Need precise tolerancing
- Working with multiple CAD systems
- Non-timber manufacturing

Use IFC when:
- Building-level coordination
- Full project documentation
- Multi-discipline collaboration
- Need building context

## Benefits

1. Manufacturing Efficiency
- Reduced tool changes
- Optimized machine movements
- Better material utilization

2. Flexibility
- Can handle complex prefabrication
- Supports various machine types
- Adaptable to different manufacturing setups

3. Quality Control
- Process priority control
- Quality parameters per operation
- Manual intervention points when needed

# BTL Processes Reference Table

## Process Key Format
- First digit: Group (0,1,2,3,4)
  - 0: General/Universal
  - 1,2: Separating processes
  - 3,4: Processes lying between

## Cutting and Basic Processes

| Process Name | Process Key | Description | Key Parameters |
|--------------|-------------|-------------|----------------|
| Cut | 1/2-010-X | Basic cut operation | P01: Distance from start, P06: Inclination, P07: Angle to reference |
| Longitudinal Cut | 0/3/4-010-X | Cut along length | P01: Distance, P02: Depth, P07: Inclination |
| Double Cut | 1/2-011-X | Two cuts meeting at point | P01: Distance, P06/P07: Cut angles |
| Ridge/Valley Cut | 0-012-X | Roof ridge cuts | P07/P09: Face inclinations, P11: Depth |
| Saw Cut | 0/3/4-013-X | Basic saw operation | P01: Distance, P06: Inclination, P11: Depth |

## Joints and Connections

| Process Name | Process Key | Description | Key Parameters |
|--------------|-------------|-------------|----------------|
| Slot | 3/4-016-X | Creates slot/groove | P11: Length, P12: Thickness, P13/P14: Displacement |
| Front Slot | 3/4-017-X | Front-facing slot | P11: Width, P12: Length, P13: Depth |
| Birds Mouth | 3/4-020-X | Roof framing joint | P07/P08: Angles, P11: Depth |
| Lap Joint | 3/4-030-X | Overlapping joint | P11: Length, P12: Depth, P13: Angle |
| Block House Half Lap | 4-037-X | Log construction joint | P11-P15: Lap dimensions |
| Dovetail | 1/2/3/4-138-X | Traditional woodworking joint | P11: Length, P12: Depth |
| Tyrolean Dovetail | 1/2/3/4-136-X | Regional dovetail variant | P11: Length, P14/P15: Dimensions |

## Drilling and Mortising

| Process Name | Process Key | Description | Key Parameters |
|--------------|-------------|-------------|----------------|
| Drilling | 3/4-040-X | Creates holes | P11: Diameter, P12: Depth |
| Mortise | 3/4-050-X | Mortise for tenon | P11: Width, P13: Depth |
| Mortise Front | 3/4-051-X | Front-facing mortise | P11: Width, P12: Depth |
| House Mortise | 3/4-053-X | Special housing joint | Based on mortise parameters |

## Surface Operations

| Process Name | Process Key | Description | Key Parameters |
|--------------|-------------|-------------|----------------|
| Planing | 3/4-090-X | Surface smoothing | P11: Depth, P12: Length |
| Profile Front | 3/4-100-X | Front profiling | P11/P12: Profile dimensions |
| Profile Head | 3/4-106-X | End profiling | Multiple profile parameters |
| Chamfer | 3/4-036-X | Edge beveling | P11: Depth, P12: Length |

## Specialized Operations

| Process Name | Process Key | Description | Key Parameters |
|--------------|-------------|-------------|----------------|
| Marking/Labeling | 3/4-060-X | Text/marks on timber | P15: Text string |
| Text | 4-061-X | Text application | P13: Height, P15: Text string |
| Free Contour | 0/3/4-250-X | Custom shape cutting | Multiple contour points |
| Sphere | 3/4-107-X | Spherical cut | P11: Radius, P12/P13: Offsets |
| Variant | 0/1/2/3/4-900-X | Custom processing | User-defined parameters |

## Special Joint Types

| Process Name | Process Key | Description | Key Parameters |
|--------------|-------------|-------------|----------------|
| Step Joint | 1/2-080-X | Stepped connection | P11: Depth, P14/P15: Dimensions |
| Simple Scarf | 1/2-070-X | Basic scarf joint | P11/P12: Depths, P13: Length |
| Scarf Joint | 1/2-071-X | Complex scarf joint | P11: Depth, P13: Length |

## Notes:
- All dimensions are in millimeters (mm)
- All angles are in degrees (°)
- X in process keys represents sequential numbering
- Most processes support transformation parameters for positioning
- Many processes include optional parameters for fine-tuning