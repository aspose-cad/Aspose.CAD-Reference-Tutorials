---
date: 2025-12-22
description: Erfahren Sie, wie Sie DWG-Dateien laden und Unterlage‑Informationen mit
  Aspose.CAD für Java extrahieren – ein Schritt‑für‑Schritt‑Leitfaden, der Unterlage‑Flags
  abdeckt.
linktitle: Accessing Underlay Flags of DWG
second_title: Aspose.CAD Java API
title: DWG-Datei laden & Zugriff auf Unterlage‑Kennzeichen – Aspose.CAD für Java
url: /de/java/cad-file-manipulation/accessing-underlay-flags-of-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG-Datei laden & Unterlage-Flags abrufen – Aspose.CAD für Java

In modernen CAD‑Workflows ist das **Laden einer DWG‑Datei** schnell und das Herausziehen von Unterlage‑Details eine gängige Anforderung. Egal, ob Sie einen Viewer bauen, die Stapelverarbeitung automatisieren oder Metadaten für die GIS‑Integration extrahieren, Aspose.CAD für Java bietet Ihnen einen sauberen, code‑first Ansatz dafür. In diesem Tutorial führen wir Sie durch die genauen Schritte, um **DWG‑Datei zu laden**, ihre Entitäten zu iterieren und die Unterlage‑Flags zu lesen, die viele Entwickler übersehen.

## Schnelle Antworten
- **Was ist die primäre Klasse zum Öffnen einer DWG?** `com.aspose.cad.Image.load()` gibt ein `CadImage` zurück.
- **Welches Objekt enthält Unterlage-Informationen?** `CadUnderlay` (oder abgeleitete Typen wie `CadDgnUnderlay`).
- **Benötige ich eine Lizenz für die Entwicklung?** Eine kostenlose Testversion funktioniert zum Testen; für die Produktion ist eine kommerzielle Lizenz erforderlich.
- **Kann ich mehrere DWG‑Dateien in einer Schleife verarbeiten?** Ja – wiederholen Sie einfach das Laden‑und‑Iterieren‑Muster.
- **Ist dieser Ansatz kompatibel mit Java 11+?** Absolut, Aspose.CAD unterstützt Java 8 bis zu den neuesten LTS‑Versionen.

## Was bedeutet „load dwg file“ in Aspose.CAD?
`Image.load()` liest den binären DWG‑Inhalt und erstellt ein `CadImage`‑Objekt im Speicher. Von dort aus können Sie Ebenen, Blöcke und Unterlage‑Entitäten erkunden, ohne sich selbst mit dem DWG‑Dateiformat auseinandersetzen zu müssen.

## Warum Unterlage-Flags aus einer DWG extrahieren?
Unterlage-Flags geben an, wie ein externes Referenzobjekt (wie ein DGN‑ oder PDF‑Unterlage) innerhalb der Zeichnung positioniert, skaliert und rotiert ist. Das Wissen um diese Werte ermöglicht es Ihnen:
- Das exakte visuelle Layout in einem benutzerdefinierten Viewer nachzubilden.
- Unterlagen in native CAD-Entitäten für weitere Bearbeitung zu konvertieren.
- Berichte zu erstellen, die Unterlage-Metadaten für Konformität oder Dokumentation enthalten.

## Voraussetzungen
- **Aspose.CAD Library** – download from the [releases](https://releases.aspose.com/cad/java/) page.
- **Java Development Kit** – JDK 8 oder neuer.
- **Ein Ordner**, der die DWG-Dateien enthält, die Sie analysieren möchten. Ersetzen Sie `"Your Document Directory"` im Code durch Ihren tatsächlichen Pfad.

## Namespaces importieren

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadBaseEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadDgnUnderlay;
import com.aspose.cad.fileformats.cad.cadobjects.CadUnderlay;
import com.aspose.cad.fileformats.cad.cadobjects.UnderlayFlags;
```

## Schritt‑für‑Schritt‑Anleitung

### Schritt 1: Ressourcenverzeichnis festlegen
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DWGDrawings/";
```
Definieren Sie, wo Ihre DWG‑Dateien liegen. Die Verwendung eines eigenen Ordners hält das Beispiel sauber und portabel.

### Schritt 2: DWG‑Datei laden
```java
// Input file name and path
String fileName = dataDir + "BlockRefDgn.dwg";

// Load an existing DWG file and convert it into CadImage 
CadImage image = (CadImage)Image.load(fileName);
```
Hier **laden wir die DWG‑Datei** `BlockRefDgn.dwg` in eine `CadImage`‑Instanz, bereit zur Inspektion.

### Schritt 3: Durch DWG‑Entitäten iterieren
```java
// Go through each entity inside the DWG file
for(CadBaseEntity entity : image.getEntities())
```
Die Schleife durchläuft jede Entität – Linien, Kreise, Blöcke und Unterlagen – sodass wir die benötigten herausfiltern können.

### Schritt 4: CadDgnUnderlay‑Entitäten identifizieren
```java
// Check if entity is of CadDgnUnderlay type
if (entity instanceof CadDgnUnderlay)
```
Nur `CadDgnUnderlay`‑Objekte enthalten die gesuchten Unterlage-Flags, daher filtern wir danach.

### Schritt 5: Auf Unterlage‑Informationen zugreifen
```java
// Access different underlay flags 
CadUnderlay underlay = (CadUnderlay) entity;
System.out.println(underlay.getUnderlayPath());
System.out.println(underlay.getUnderlayName());
// ... (Additional underlay properties)
break;
```
Sobald wir ein `CadUnderlay` haben, können wir seinen Pfad, Namen, Einfügepunkt, Rotation, Skalierungsfaktoren und das `UnderlayFlags`‑Enum auslesen, das Sichtbarkeit, Clipping und weitere Rendering‑Optionen angibt.

## Häufige Probleme & Tipps
- **Null underlay path** – Stellen Sie sicher, dass die DWG tatsächlich eine externe Datei referenziert; andernfalls ist der Pfad leer.
- **Unsupported underlay type** – Aspose.CAD unterstützt derzeit DGN‑Unterlagen; PDF‑Unterlagen sind noch nicht über die API verfügbar.
- **License exceptions** – Das Ausführen des Codes ohne gültige Lizenz fügt jedem exportierten Bild ein Wasserzeichen hinzu.

## Häufig gestellte Fragen

**Q: Kann ich Aspose.CAD für Java mit anderen CAD‑Dateiformaten verwenden?**  
A: Aspose.CAD konzentriert sich hauptsächlich auf das DWG‑Format, unterstützt aber auch DXF, DWF und weitere CAD‑Formate.

**Q: Gibt es eine Testversion von Aspose.CAD für Java?**  
A: Ja, Sie können die Funktionen mit einer kostenlosen Testversion von [hier](https://releases.aspose.com/) ausprobieren.

**Q: Wie kann ich Support erhalten oder Hilfe zu Aspose.CAD für Java bekommen?**  
A: Besuchen Sie das [Aspose.CAD‑Forum](https://forum.aspose.com/c/cad/19) für Community‑Support und Diskussionen.

**Q: Gibt es temporäre Lizenzen für Aspose.CAD für Java?**  
A: Ja, Sie können eine temporäre Lizenz [hier](https://purchase.aspose.com/temporary-license/) erhalten.

**Q: Wo finde ich die umfassende Dokumentation für Aspose.CAD für Java?**  
A: Siehe die [Dokumentation](https://reference.aspose.com/cad/java/) für detaillierte Informationen.

---

**Zuletzt aktualisiert:** 2025-12-22  
**Getestet mit:** Aspose.CAD 24.12 für Java  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}