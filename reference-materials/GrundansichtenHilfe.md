-   [[1]{.toc-section-number} 5.4.X Grundansichten](#x-grundansichten){#toc-x-grundansichten}
    -   [[1.1]{.toc-section-number} 5.4.X.1 Einleitung](#x.1-einleitung){#toc-x.1-einleitung}
    -   [[1.2]{.toc-section-number} 5.4.X.2 Grundlegende Informationen](#x.2-grundlegende-informationen){#toc-x.2-grundlegende-informationen}
    -   [[1.3]{.toc-section-number} 5.4.X.3 Erweiterung der Darstellungsschaltung](#x.3-erweiterung-der-darstellungsschaltung){#toc-x.3-erweiterung-der-darstellungsschaltung}
    -   [[1.4]{.toc-section-number} 5.4.X.4 Speichern einer Grundansicht](#x.4-speichern-einer-grundansicht){#toc-x.4-speichern-einer-grundansicht}
-   [[2]{.toc-section-number} X.X.X.X Grundansichtsplan](#x.x.x.x-grundansichtsplan){#toc-x.x.x.x-grundansichtsplan}

# 5.4.X Grundansichten

## 5.4.X.1 Einleitung

Arbeitsvorbereiter benötigen, je nach aktueller Tätigkeit, unterschiedlichste Kombinationen aus Darstellungsschaltung, Layerschaltung und automatischer Bemaßung und Beschriftung.

Planer und Bauzeichner müssen ebenfalls, je nach geforderter Aufgabenstellung (Lageplan, Möbel- und Küchenplan, Eingabeplan etc.), unterschiedlichste Ablagen für Pläne erzeugen

(s. **X.X.X.X Grundansichtsplan**).

Dazu werden Grundansichten verwendet, da diese die oben genannten Einstellungen individuell und getrennt speichern.

## 5.4.X.2 Grundlegende Informationen

Grundansichten werden in der Gebäudenavigation aufgelistet. Jedes Stockwerk besitzt dabei standardmäßig einen eigenen Unterzweig \"**Grundansichten**\".

Um eine neue Grundansicht zu erzeugen, klickt man mit \'**MausRechts**\' auf den Zweig \"**Grundansichten**\" in der \"**Gebäudenavigation**\" und anschließend im Kontextmenü auf \"**Neue Grundansicht**\".

Grundansichten können folgende Einstellungen unabhängig von \"**Grundriss**\" und weiteren \"**Grundansichten**\" getrennt speichern:

-   Bildausschnitt

-   Auswahl der Layerschaltung (inkl. Layergruppen)

-   Darstellungsschaltung (inkl. Einstellungen zur automatischen Bemaßung und Beschriftung)

Sind die Checkboxen gesetzt, werden die verwendeten Einstellungen in der aktuellen Grundansicht gespeichert.

Des Weiteren besitzt jede Grundansicht einen eigenen Maßstab, welcher die Größe der darzustellenden Zeichnungselemente steuert. Das Verhalten ist identisch mit dem Maßstab eines Ansichtsfenster im Planprogramm. Der Modellbereich \"**Grundriss**\" verwendet weiterhin die Maßstabseinstellungen der Layerschaltung.

Grundansichten können über ihr Kontextmenü bearbeitet werden. Dazu klickt man in der \"**Gebäudenavigation**\" mit \'**MausRechts**\' auf die jeweilige Grundansicht. Es stehen nun folgende Optionen zur Verfügung:

-   \"**Neue Grundansicht**\": Anlegen neuer bzw. weiterer Grundansichten

-   \"**Bearbeiten**\": Aufruf des Bearbeitungsdialogs der aktuellen Grundansicht

-   \"**Mit aktueller Darstellung und Einstellungen überschreiben**\": Die aktuelle Grundansicht wird mit den aktuellen Einstellungen \[\"**1-7-1 Darstellungsschaltung**\" und \"**04-1 Layerschaltung**\"\] aus dem Modellbereich überschrieben.

-   \"**Bemaßung und Beschriftung neuberechnen**\": Manuelles Auslösen der Neuberechnung von automatisch erzeugten Bemaßungen und Beschriftungen aus der Darstellungsschaltung.

-   \"**Löschen**\": Löschen der aktuellen Grundansicht inkl. aller zu dieser Grundansicht gehörenden Zeichnungselemente.

## 5.4.X.3 Erweiterung der Darstellungsschaltung

Um in einer Grundansicht Zeichnungselemente aus anderen Grundansichten bzw. aus dem Grundriss gezielt ein- und ausblenden zu können, gibt es in der Darstellungsschaltung zwei Einträge dazu.

Über die Checkbox und den Edit \"**Grunda.**\" (unterhalb der Darstellungsschaltung für \"**Räume**\") können Grundansichten bzw. die Zeichnungselemente des Grundriss in der aktuellen Grundansicht angezeigt werden. Gleiches gilt für die Darstellung von Grundansichten im Modellbereich \"**Grundriss**\".

Zuerst wird die Checkbox gesetzt. Anschließend kann man über den Button \"**Einstellungen ändern**\", den Dialog \"**Grundansichten zur Anzeige der Planelemente**\" öffnen. In diesem werden nun die Grundansichten aktiv gesetzt, die dargestellt werden sollen. Die aktivierten Grundansichten werden zur Information auch als kommagetrennte Liste in dem vorangestellten Textfeld angezeigt.

Die gleiche Methodik findet Anwendung für die Darstellungsschaltung der Grundansichten aus anderen Stockwerken. Dazu wurde die Liste der Stockwerke (\"**übrige Stockwerke, Grundansichten**\"), mit der oben beschriebenen Systematik, erweitert.

Es ist zu beachten, dass zur Anzeige von Zeichnungselemente aus anderen Grundansichten auch die Checkboxen für \"**Linien, Kreise, Schraffuren, ..**\" und ggf. \"**Bemaßung, Texte, ..**\" aktiviert sein müssen. Ebenso müssen die entsprechenden Layer, in der Layerschaltung, als sichtbar gesetzt sein.

## 5.4.X.4 Speichern einer Grundansicht

Um inkonsistente Situationen der Darstellungsschaltung zu vermeiden, wird bei einem Wechsel der Grundansicht explizit abgefragt, ob die Änderungen gespeichert werden sollen.

Änderungen können über zwei Wege geschehen.

Zum einen können Änderungen der aktuellen Grundansicht im Grafikbereich gemacht werden. Dies geschieht über Änderungen in der Darstellungsschaltung und/oder den Einstellungen des Layerdialogs. Sollen diese Änderungen in die aktuelle Grundansicht gespeichert werden, bestätigt man die Abfrage mit \"**Ja**\". Das Programm speichert nun die aktuellen Einstellungen vom Bildschirm in die Grundansicht.

Der zweite Weg Änderungen in der aktuellen Grundansicht zu machen, erfolgt über das Kontextmenü der Gebäudenavigation. Dazu klickt man mit \'**MausRechts**\' auf die aktuelle Grundansicht und anschließend auf \"**Bearbeiten**\". Werden jetzt im Dialog \"**Grundansicht**\" Einstellungen (Darstellungsschaltung und/oder Layerdialog) geändert und der Dialog mit \"**Ok**\" verlassen, wählt man in der anschließenden Abfrage \"**Nein**\". Damit wird die veraltete Situation im Grafikbereich mit den neuen, eben angepassten Einstellungen der Grundansicht überschrieben.

# X.X.X.X Grundansichtsplan

Zur Erzeugung von Plänen bzw. Ablagen für Pläne gibt es für Grundansichten eine eigene Funktion.

Diese ist im Menü unter \"**1-01-5 Grundansichtsplan**\" zu finden. Aktiv ist diese nur, wenn man sich in einer Grundansicht befindet.

Grundlegende Philosophie der Grundansichten ist es, die finale Situation - welche im Plan dargestellt werden soll - bereits im Bauwerk vollständig auszuarbeiten. Daher können im Dialog \"**Ablage Grundansichtsplan**\" keine weiteren, spezifischen Einstellungen zur Ablage mehr getroffen werden.

**Ablagenummer:** ...

**Ablage für:** ...

**Planvorlage:** ...

**Kategorie:** ...

**Maßstab runden auf:** ...

**Wert:** ...

**Festwert:** ...

**Texthöhe für DXF:** ...
