---
date: 2026-01-12
description: Erfahren Sie, wie Sie mit Aspose.CAD für Java Bilder zu DWG-Dateien hinzufügen
  und DWG in PDF konvertieren. Folgen Sie unserer Schritt‑für‑Schritt‑Anleitung für
  eine effiziente Entwicklung.
linktitle: Import Image to DWG File Using Java
second_title: Aspose.CAD Java API
title: Bilder mühelos zu DWG-Dateien hinzufügen mit Aspose.CAD Java
url: /de/java/dwg-file-operations/import-image-to-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Bild zu DWG-Dateien mühelos hinzufügen mit Aspose.CAD Java

In modernen Java‑Anwendungen ist **das Hinzufügen eines Bildes zu DWG**‑Dateien ein häufiges Anliegen – egal, ob Sie einen CAD‑Viewer bauen, Zeichenupdates automatisieren oder Dokumentationen erzeugen. Aspose.CAD für Java bietet Ihnen einen einfachen, hochperformanten Weg, Rasterbilder direkt in DWG‑Zeichnungen einzubetten, ohne dass ein vollständiger CAD‑Motor nötig ist. In diesem Tutorial führen wir Sie durch den gesamten Prozess, vom Laden einer DWG‑Datei bis zum Export des Ergebnisses als PDF.

## Schnellantworten
- **Welche Bibliothek benötige ich?** Aspose.CAD für Java  
- **Kann ich auch nach PDF exportieren?** Ja – verwenden Sie `PdfOptions` zusammen mit `CadRasterizationOptions`  
- **Benötige ich eine Lizenz für die Entwicklung?** Eine kostenlose Testversion reicht für Tests; für die Produktion ist eine kommerzielle Lizenz erforderlich  
- **Welche Java‑Version wird unterstützt?** Java 8 und höher  
- **Wie lange dauert die Implementierung?** Etwa 10‑15 Minuten für einen einfachen Bildimport

## Was bedeutet „Bild zu DWG hinzufügen“?
Ein Bild zu einer DWG‑Datei hinzuzufügen bedeutet, ein Rasterbild (PNG, JPEG usw.) als `CadRasterImage`‑Objekt im Modell‑Raum der Zeichnung zu platzieren. Das Bild wird Teil des CAD‑Entitätsbaums und kann wie jedes andere CAD‑Objekt positioniert, skaliert und beschnitten werden.

## Warum Aspose.CAD für Java zum Bild‑zu‑DWG‑Hinzufügen verwenden?
- **Keine CAD‑Software nötig** – die API übernimmt das DWG‑Parsing intern.  
- **Fein abgestimmte Kontrolle** über Einfügepunkt, Skalierungsvektoren und Beschnitt.  
- **Integrierte PDF‑Konvertierung**, sodass Sie im selben Workflow ein druckfähiges PDF erzeugen können.  
- **Plattformübergreifend** – funktioniert unter Windows, Linux und macOS.

## Voraussetzungen
- Aspose.CAD für Java: Stellen Sie sicher, dass die Aspose.CAD‑Bibliothek installiert ist. Sie können sie [hier](https://releases.aspose.com/cad/java/) herunterladen.  
- Java‑Entwicklungsumgebung: JDK 8+ mit Ihrer bevorzugten IDE (IntelliJ, Eclipse, VS Code usw.).

## Pakete importieren
```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.*;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Schritt‑für‑Schritt‑Anleitung

### Schritt 1: DWG‑Datei laden
Zuerst geben Sie den Ordner an, der Ihre DWG‑Zeichnung enthält, und laden sie mit `Image.load`.
```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Drawing11.dwg";
Image image = Image.load(srcFile);
```

### Schritt 2: Raster‑Bilddefinition festlegen
Erzeugen Sie ein `CadRasterImageDef`, das auf das externe PNG verweist, das Sie einbetten möchten. Der Konstruktor nimmt den Bilddateinamen und seine Pixelabmessungen entgegen.
```java
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.setObjectHandle("A3B4");
```

### Schritt 3: Einfügepunkt und Skalierungsvektoren setzen
Der Einfügepunkt bestimmt, wo die linke untere Ecke des Bildes erscheinen soll. Die **U**‑ und **V**‑Vektoren steuern die horizontale bzw. vertikale Skalierung.
```java
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

### Schritt 4: CadRasterImage‑Objekt erstellen
Kombinieren Sie Definition, Einfügepunkt und Vektoren zu einem `CadRasterImage`. Sie können zudem Beschnitte‑Grenzen festlegen, falls nur ein Teil des Bildes sichtbar sein soll.
```java
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.setImageDefReference("A3B4");
cadRasterImage.setDisplayFlags((short)7);
cadRasterImage.setClippingState((short)0);
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(639.5, 561.5));
```

### Schritt 5: Bild zum Modell‑Raum hinzufügen
Fügen Sie das Rasterbild in den Block `*Model_Space` ein und aktualisieren anschließend die Objekt‑Sammlung der Zeichnung, damit die Definition gespeichert wird.
```java
CadImage cadImage = ((CadImage)(image));
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(cadRasterImage);
CadBaseObject[] objs = cadImage.getObjects();
CadBaseObject[] arr = new CadBaseObject[objs.length + 1];
int ind = 0;
for (CadBaseObject obj : objs)
{
    arr[ind] = obj;
    ind++;
}
arr[ind] = cadRasterImageDef;
cadImage.setObjects(arr);
```

### Schritt 6: PDF‑Exportoptionen konfigurieren (optional)
Falls Sie zusätzlich eine PDF‑Version der Zeichnung benötigen, konfigurieren Sie `PdfOptions` zusammen mit `CadRasterizationOptions`. Dieser Schritt zeigt, wie Sie **DWG zu PDF konvertieren** im selben Ablauf.
```java
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

### Schritt 7: Ergebnis‑PDF speichern
Exportieren Sie abschließend die modifizierte Zeichnung als PDF‑Datei. Die gleiche `image`‑Instanz wird verwendet, sodass das PDF das neu hinzugefügte Rasterbild enthält.
```java
image.save((srcFile + "_generated.pdf"), pdfOptions);
```

Durch Befolgen dieser Schritte können Sie **Bild zu DWG**‑Dateien schnell hinzufügen und bei Bedarf **DWG als PDF speichern**.

## Häufige Probleme und Lösungen
- **Bild wird nicht angezeigt** – Prüfen Sie, ob der Bilddateipfad (`road-sign-custom.png`) korrekt ist und ob die Bildabmessungen den an `CadRasterImageDef` übergebenen Werten entsprechen.  
- **Falsche Skalierung** – Passen Sie die U‑ und V‑Vektoren an; sie geben die Zeichen‑Einheiten pro Pixel an.  
- **PDF ist leer** – Stellen Sie sicher, dass `CadRasterizationOptions.setDrawType` auf `UseObjectColor` oder einen anderen geeigneten Modus gesetzt ist.

## Häufig gestellte Fragen

**F: Ist Aspose.CAD für Java mit allen Java‑Entwicklungsumgebungen kompatibel?**  
A: Ja, Aspose.CAD für Java ist mit den meisten Java‑Entwicklungsumgebungen kompatibel.

**F: Kann ich Aspose.CAD für Java in kommerziellen Projekten einsetzen?**  
A: Ja, Sie können Aspose.CAD für Java in kommerziellen Projekten verwenden. Weitere Lizenzdetails finden Sie [hier](https://purchase.aspose.com/buy).

**F: Gibt es eine kostenlose Testversion von Aspose.CAD für Java?**  
A: Ja, die kostenlose Testversion erhalten Sie [hier](https://releases.aspose.com/).

**F: Wie erhalte ich Support für Aspose.CAD für Java?**  
A: Support erhalten Sie im [Aspose.CAD‑Forum](https://forum.aspose.com/c/cad/19).

**F: Kann ich eine temporäre Lizenz für Aspose.CAD für Java erhalten?**  
A: Ja, eine temporäre Lizenz erhalten Sie [hier](https://purchase.aspose.com/temporary-license/).

---

**Zuletzt aktualisiert:** 2026-01-12  
**Getestet mit:** Aspose.CAD für Java 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}