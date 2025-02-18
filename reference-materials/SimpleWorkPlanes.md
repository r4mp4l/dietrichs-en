# Simple Guide to D-CAM Workplanes

## What Are Workplanes?

Workplanes are like invisible sheets that help you draw and build in 3D space. Think of them as virtual drawing boards that you can place anywhere in your project. They are essential in D-CAM because you cannot add materials or components to your project without them - they provide the necessary reference for positioning and orienting building elements.

### Key Properties of Workplanes

1. **Thickness**
   - Workplanes have no physical thickness
   - They are purely reference surfaces for construction
   - Components can be placed on either side of the workplane

2. **Size and Boundaries**
   - Workplanes are technically infinite in size
   - The visible grid area can be adjusted as needed
   - You can work beyond the visible grid area
   ![](media-workplanes/media/image55.png)

3. **Resizing Options**
   - Use the Clipbox to control the visible area
   - Adjust grid size and spacing for different tasks
   - Save different size settings as favorites for quick access
   ![](media-workplanes/media/image64.jpeg)

![](media-workplanes/media/image3.jpeg)  
![](media-workplanes/media/image4.png) 
![](media-workplanes/media/image6.png) 

## Basic Concepts

### Types of Workplanes

1. **Horizontal Workplanes**
   - Like a flat table surface
   - Great for floor plans and top-down views
   ![](media-workplanes/media/image32.png)

2. **Vertical Workplanes**
   - Like a wall surface
   - Perfect for working on walls and elevations
   ![](media-workplanes/media/image36.png)

3. **Arbitrary Workplanes**
   - Can be placed at any angle
   - Useful for roof slopes and complex angles
   ![](media-workplanes/media/image38.png)

### Working with the Grid

- You can turn the grid on/off using the "R" key
- Adjust grid size for different tasks:
  - Small grid for detailed work
  - Large grid for rough layouts
![](media-workplanes/media/image58.jpeg)

### Important Tips

1. Components stay in place even if you delete the workplane
2. You can move workplanes without moving components
3. Drawing elements (like lines) move with the workplane
4. You can work in 2D or 3D at any time

## Practical Applications

### Using Workplanes for Buildings

1. Start with a horizontal workplane for the foundation
2. Add vertical workplanes for walls
3. Use angled workplanes for roofs
![](media-workplanes/media/image104.jpeg)

### Common Tasks

1. **Adding Beams**
   - Use "beam along X" for horizontal beams
   - Use "beam along Y" for vertical posts
   ![](media-workplanes/media/image107.png)

2. **Creating Joints**
   - Position workplanes at connection points
   - Use appropriate joint types for each connection
   ![](media-workplanes/media/image115.jpeg)

## Beginner Tutorials

## Detailed Tutorials

### Tutorial 1: Creating a Simple Frame
1. **Set Up Base Workplane**
   - Create a new horizontal workplane at ground level
   - Set grid size to 0.100 for precision
   - Make workplane area 6.000 x 6.000 meters
   ![](media-workplanes/media/image105.png)

2. **Add Corner Posts**
   - Create vertical workplane at front edge
   - Use "beam along Y" to add 0.160 x 0.160 posts
   - Set positioning point to "Choice" for easy corner placement
   - Create posts at both ends of front edge
   ![](media-workplanes/media/image107.png)

3. **Add Top Plate**
   - Stay in vertical workplane
   - Use "beam along X" for horizontal plate
   - Set beam size to 0.160 x 0.240
   - Rotate cross-section 90° if needed
   ![](media-workplanes/media/image109.jpeg)

4. **Add Diagonal Bracing**
   - Use "Beam 2 Points" for diagonal brace
   - Set step joint depth to 0.020
   - Position lower end 0.200 from post bottom
   - Set upper opening to 1.000 from post inside
   ![](media-workplanes/media/image110.png)

### Tutorial 2: Building a Basic Roof
1. **Create Top Level Workplane**
   - Make horizontal workplane at wall plate height
   - Set grid to match building dimensions
   - Ensure proper orientation for roof layout
   ![](media-workplanes/media/image116.png)

2. **Set Up Roof Angle**
   - Create vertical workplane at gable end
   - Draw circle (r=0.215) at plate corner for rafter positioning
   - Draw lines for roof slope from ridge point
   - Define eaves point for rafter ends
   ![](media-workplanes/media/image117.png)

3. **Add First Rafters**
   - Use "beam 2 points" for gable rafter
   - Set correct cross-section rotation
   - Create birds mouth joint where rafter meets plate
   - Copy rafter to opposite end
   ![](media-workplanes/media/image119.png)

4. **Complete Rafter Layout**
   - Create arbitrary workplane on roof slope
   - Distribute intermediate rafters
   - Set spacing using "Clear distance" option
   - Add birds mouth cuts to all rafters
   ![](media-workplanes/media/image121.png)

### Tutorial 3: Creating Wall Connections
1. **Prepare Wall Workplanes**
   - Create vertical workplanes for each wall
   - Set grid size appropriate for stud spacing
   - Ensure proper workplane orientation
   ![](media-workplanes/media/image122.png)

2. **Add Wall Components**
   - Position bottom plate using "beam along X"
   - Add top plate at wall height
   - Use "distribute" function for regular stud spacing
   - Add door/window openings as needed

3. **Create Corner Connections**
   - Use end lap joints for plate corners
   - Add corner studs with proper overlap
   - Create proper nailing surfaces
   ![](media-workplanes/media/image114.jpeg)

4. **Add Wall Bracing**
   - Create diagonal braces at 45 degrees
   - Use step joints at brace ends
   - Ensure proper depth positioning
   - Mirror bracing for opposite direction
   ![](media-workplanes/media/image123.png)

Tips for All Tutorials:
- Always check active workplane before adding components
- Use "R" key to toggle grid visibility
- Save work frequently
- Double-check component orientations
- Verify joints and connections

## Tips for Success

1. Always check your workplane orientation before adding components
2. Use the grid for precise placement
3. Save common grid settings as favorites
4. Remember you can switch between 2D and 3D views
5. Practice with simple projects first

## Working Without Workplanes

### Why Workplanes Are Essential
1. Cannot add materials directly to 3D space
2. Need reference planes for accurate positioning
3. Required for proper component orientation
4. Necessary for precise measurements
5. Essential for joint creation

### What Happens Without Workplanes
1. Cannot place components accurately
2. No reference for alignments
3. Difficult to maintain proper angles
4. Impossible to create certain joints
5. Risk of misaligned structures

## Common Mistakes to Avoid

1. Forgetting which workplane is active
2. Not checking component orientation
3. Using wrong grid size for the task
4. Ignoring depth position settings
5. Not saving work regularly
6. Trying to work without appropriate workplanes
7. Not adjusting workplane visibility for complex areas
8. Forgetting to check workplane orientation before adding components

## Advanced Workplane Features

### Clipbox Control
- Defines the 3D viewing boundaries
- Helps focus on specific areas
- Can be turned on/off as needed
![](media-workplanes/media/image67.jpeg)

### Managing Workplanes

#### Renaming Workplanes
You can rename workplanes in two ways:

1. **Through Building Navigation**
   - Right-click workplane name in building navigation panel
   - Select option to change attributes/name
   - Enter new name
   ![](media-workplanes/media/image47.png)

2. **Through View Menu**
   - Navigate to View → Section → Work planes
   - Locate desired workplane
   - Change properties to update name
   ![](media-workplanes/media/image48.jpeg)

**Tips for Naming Workplanes:**
- Use clear, descriptive names
- Consider naming by:
  - Location (e.g., "Front Wall", "Rear Gable")
  - Level (e.g., "Ground Floor", "Roof Level")
  - Purpose (e.g., "Layout Grid", "Detail View")
- Rename at any time without affecting components
- Consistent naming helps with complex projects

### Material Positioning

### Depth Position Options
When placing materials or components on a workplane, you have several positioning options:

1. **Basic Positions**
   - Flush Front: Material sits on front of workplane
   - Flush Back: Material sits on back of workplane
   - Center: Material is centered on workplane
   ![](media-workplanes/media/image68.jpeg)

2. **Custom Offset**
   - Enter specific distance from workplane
   - Positive values move forward from plane
   - Negative values move backward from plane
   - Use for precise positioning needs

3. **Important Notes**
   - Default is usually flush front
   - Check positioning before confirming placement
   - Offset values are perpendicular to workplane
   - Position affects joints and connections

### Common Applications
1. **Wall Construction**
   - Sheathing: Often flush front or back
   - Studs: Usually centered
   - Trim: Specific offset for detail work

2. **Roof Elements**
   - Rafters: Position affects bird's mouth cuts
   - Sheathing: Usually flush to outer face
   - Fascia: Specific offset from rafter ends

### Tips for Positioning
- Always verify depth position before mass operations
- Use consistent positioning for similar elements
- Consider final assembly when choosing position
- Remember position affects joint creation

## Grid Customization
1. **Size Adjustment**
   - Change visible area for different tasks
   - Adjust grid spacing for precision
   - Save custom settings as favorites

2. **Display Options**
   - Control grid line visibility
   - Adjust reference point display
   - Customize workplane appearance
   ![](media-workplanes/media/image62.png)

3. **Working Beyond the Grid**
   - Grid boundaries don't limit work area
   - Can select points outside visible area
   - Infinite workplane extends beyond display

Remember: Workplanes are tools to help you work more efficiently. They don't affect your final model - they just make it easier to create it!