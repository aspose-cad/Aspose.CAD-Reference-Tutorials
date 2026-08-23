---
date: 2026-05-20
description: Erfahren Sie, wie Sie mit Aspose.CAD für Java ein Bild zu DWG-Dateien
  hinzufügen und DWG in PDF konvertieren. Folgen Sie unserer Schritt‑für‑Schritt‑Anleitung
  für eine effiziente Entwicklung.
keywords:
- add image to dwg
- convert dwg to pdf
- import image into dwg
- embed raster image dwg
- dwg file operations
linktitle: Bild in DWG-Datei importieren mit Java
schemas:
- author: Aspose
  dateModified: '2026-05-20'
  description: Learn how to add image to DWG files using Aspose.CAD for Java and also
    convert DWG to PDF. Follow our step-by-step guide for efficient development.
  headline: Add Image to DWG Files Effortlessly Using Aspose.CAD Java
  type: TechArticle
- description: Learn how to add image to DWG files using Aspose.CAD for Java and also
    convert DWG to PDF. Follow our step-by-step guide for efficient development.
  name: Add Image to DWG Files Effortlessly Using Aspose.CAD Java
  steps:
  - name: Load the DWG File
    text: First, point to the folder that contains your DWG drawing and load it with
      `Image.load`.
  - name: Define the Raster Image Definition
    text: The `CadRasterImageDef` class defines the external raster image resource
      to be embedded in the drawing.
  - name: Set Insertion Point and Scaling Vectors
    text: The insertion point determines where the lower‑left corner of the image
      will appear. The **U** and **V** vectors control horizontal and vertical scaling.
  - name: Create the CadRasterImage Object
    text: The `CadRasterImage` entity represents a raster picture placed in the DWG
      model space.
  - name: Add the Image to Model Space
    text: Insert the raster image into the `*Model_Space` block, then update the drawing’s
      object collection so the definition is saved.
  - name: Configure PDF Export Options (Optional)
    text: '`PdfOptions` specifies settings for saving a CAD drawing as a PDF file.
      `CadRasterizationOptions` defines how the CAD content is rasterized during PDF
      conversion.'
  - name: Save the Resulting PDF
    text: 'Finally, export the modified drawing as a PDF file. The same `image` instance
      is used, so the PDF reflects the newly added raster image. By following these
      steps, you can **add image to dwg** files quickly and also **save dwg as pdf**
      when needed, covering the most common **dwg file operations** in '
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD for Java works with any IDE that supports JDK 8+, including
      IntelliJ IDEA, Eclipse, and VS Code.
    question: Is Aspose.CAD for Java compatible with all Java development environments?
  - answer: Yes, you can use Aspose.CAD for Java for commercial projects. Visit **[here](https://purchase.aspose.com/buy)**
      for licensing details.
    question: Can I use Aspose.CAD for Java for commercial projects?
  - answer: Yes, you can access the free trial **[here](https://releases.aspose.com/)**.
    question: Is there a free trial available for Aspose.CAD for Java?
  - answer: You can seek support on the **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)**.
    question: How can I get support for Aspose.CAD for Java?
  - answer: Yes, you can get a temporary license **[here](https://purchase.aspose.com/temporary-license/)**.
    question: Can I obtain a temporary license for Aspose.CAD for Java?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Bild in DWG-Dateien mühelos hinzufügen mit Aspose.CAD Java
url: /de/java/dwg-file-operations/import-image-to-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Bild zu DWG-Dateien mühelos hinzufügen mit Aspose.CAD Java

In modernen Java-Anwendungen ist das **Hinzufügen eines Bildes zu DWG**-Dateien eine gängige Anforderung – egal, ob Sie einen CAD‑Viewer erstellen, Zeichenaktualisierungen automatisieren oder Dokumentationen erzeugen. Aspose.CAD für Java bietet Ihnen eine unkomplizierte, leistungsstarke Möglichkeit, Rasterbilder direkt in DWG‑Zeichnungen einzubetten, ohne dass ein vollständiger CAD‑Motor erforderlich ist. In diesem Tutorial führen wir Sie durch den gesamten Prozess, vom Laden einer DWG bis zum Export des Ergebnisses als PDF, und wir behandeln außerdem, wie man **import image into dwg** und **convert dwg to pdf** in einem einzigen Workflow.

## Schnelle Antworten
- **Welche Bibliothek benötige ich?** Aspose.CAD for Java  
- **Kann ich auch nach PDF exportieren?** Ja – verwenden Sie `PdfOptions` mit `CadRasterizationOptions`  
- **Benötige ich eine Lizenz für die Entwicklung?** Eine kostenlose Testversion funktioniert für Tests; eine kommerzielle Lizenz ist für die Produktion erforderlich  
- **Welche Java-Version wird unterstützt?** Java 8 und höher  
- **Wie lange dauert die Implementierung?** Etwa 10‑15 Minuten für einen einfachen Bildimport  

## Was ist „add image to dwg“?

Das Hinzufügen eines Bildes zu einer DWG-Datei bedeutet, ein Rasterbild (PNG, JPEG usw.) als **CadRasterImage**‑Entität im Modellraum der Zeichnung einzubetten, wo es wie jedes andere CAD‑Objekt positioniert, skaliert und optional beschnitten werden kann. Es wird in der Objekttabelle der Zeichnung gespeichert und von Standard‑CAD‑Betrachtern angezeigt.

## Warum Aspose.CAD für Java zum Hinzufügen von Bildern zu dwg verwenden?

Sie können Rastergrafiken in DWG-Dateien einbetten, ohne Drittanbieter‑CAD‑Software zu installieren, und die API bietet Ihnen pixelgenaue Kontrolle über Einfügepunkt, Skalierungsvektoren und Beschnitte‑Grenzen. Aspose.CAD verarbeitet Dateien bis zu einer Größe von 2 GB, unterstützt **mehr als 50 Eingabe‑ und Ausgabeformate** und läuft unter Windows, Linux und macOS, sodass Sie die CAD‑Manipulation in jedes Java‑basierte Backend integrieren können.

## Voraussetzungen
- **Aspose.CAD for Java** – laden Sie das neueste JAR von der offiziellen Seite **[hier](https://releases.aspose.com/cad/java/)** herunter.  
- **Java Development Kit** – JDK 8 oder neuer, mit Ihrer bevorzugten IDE (IntelliJ IDEA, Eclipse, VS Code usw.).  
- Eine gültige **Aspose.CAD‑Lizenz** für den Produktionseinsatz (die Testversion funktioniert für Experimente).  

## Pakete importieren

Die folgenden Importe bringen die wesentlichen Aspose.CAD‑Klassen für Bildmanipulation und PDF‑Konvertierung ein.  
```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.*;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Schritt‑für‑Schritt‑Anleitung

### Schritt 1: DWG-Datei laden
Zuerst geben Sie den Ordner an, der Ihre DWG‑Zeichnung enthält, und laden sie mit `Image.load`.  
```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Drawing11.dwg";
Image image = Image.load(srcFile);
```

### Schritt 2: Raster‑Bilddefinition festlegen
Die Klasse `CadRasterImageDef` definiert die externe Raster‑Bildressource, die in die Zeichnung eingebettet werden soll.  
```java
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.setObjectHandle("A3B4");
```

### Schritt 3: Einfügepunkt und Skalierungsvektoren festlegen
Der Einfügepunkt bestimmt, wo die linke untere Ecke des Bildes erscheint. Die **U**‑ und **V**‑Vektoren steuern die horizontale bzw. vertikale Skalierung.  
```java
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

### Schritt 4: CadRasterImage‑Objekt erstellen
Die Entität `CadRasterImage` stellt ein Rasterbild dar, das im Modellraum der DWG platziert wird.  
```java
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.setImageDefReference("A3B4");
cadRasterImage.setDisplayFlags((short)7);
cadRasterImage.setClippingState((short)0);
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(639.5, 561.5));
```

### Schritt 5: Bild zum Modellraum hinzufügen
Fügen Sie das Rasterbild in den Block `*Model_Space` ein und aktualisieren Sie anschließend die Objekt‑Collection der Zeichnung, damit die Definition gespeichert wird.  
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
`PdfOptions` legt die Einstellungen für das Speichern einer CAD‑Zeichnung als PDF‑Datei fest. `CadRasterizationOptions` definiert, wie der CAD‑Inhalt während der PDF‑Konvertierung rasterisiert wird.  
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
Abschließend exportieren Sie die modifizierte Zeichnung als PDF‑Datei. Die gleiche `image`‑Instanz wird verwendet, sodass das PDF das neu hinzugefügte Rasterbild enthält.  
```java
image.save((srcFile + "_generated.pdf"), pdfOptions);
```

Durch Befolgen dieser Schritte können Sie **add image to dwg**-Dateien schnell hinzufügen und bei Bedarf auch **save dwg as pdf** durchführen, wodurch die gängigsten **dwg file operations** in einer einzigen kompakten Routine abgedeckt werden.

## Häufige Probleme und Lösungen
- **Bild wird nicht angezeigt** – Überprüfen Sie, ob der Bilddateipfad (`road-sign-custom.png`) korrekt ist und ob die Bildabmessungen den an `CadRasterImageDef` übergebenen Werten entsprechen.  
- **Falsche Skalierung** – Passen Sie die U‑ und V‑Vektoren an; sie geben die Zeichen‑Einheiten pro Pixel an.  
- **PDF ist leer** – Stellen Sie sicher, dass `CadRasterizationOptions.setDrawType` auf `UseObjectColor` oder einen anderen geeigneten Modus gesetzt ist.  

## Häufig gestellte Fragen

**Q: Ist Aspose.CAD für Java mit allen Java‑Entwicklungsumgebungen kompatibel?**  
A: Ja, Aspose.CAD für Java funktioniert mit jeder IDE, die JDK 8+ unterstützt, einschließlich IntelliJ IDEA, Eclipse und VS Code.

**Q: Kann ich Aspose.CAD für Java für kommerzielle Projekte verwenden?**  
A: Ja, Sie können Aspose.CAD für Java für kommerzielle Projekte nutzen. Besuchen Sie **[hier](https://purchase.aspose.com/buy)** für Lizenzdetails.

**Q: Gibt es eine kostenlose Testversion für Aspose.CAD für Java?**  
A: Ja, Sie können die kostenlose Testversion **[hier](https://releases.aspose.com/)** nutzen.

**Q: Wie kann ich Support für Aspose.CAD für Java erhalten?**  
A: Sie können Support im **[Aspose.CAD‑Forum](https://forum.aspose.com/c/cad/19)** erhalten.

**Q: Kann ich eine temporäre Lizenz für Aspose.CAD für Java erhalten?**  
A: Ja, Sie können eine temporäre Lizenz **[hier](https://purchase.aspose.com/temporary-license/)** erhalten.

---

**Zuletzt aktualisiert:** 2026-05-20  
**Getestet mit:** Aspose.CAD for Java 24.11  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Verwandte Tutorials

- [DWG mit Aspose.CAD für Java nach PDF oder Raster exportieren](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Benutzerdefinierte Eigenschaften zu DWG-Dateien mit Aspose.CAD für Java hinzufügen](/cad/java/additional-features/add-custom-properties/)
- [CAD als PNG speichern – CAD-Zeichnung in Rasterbildformat konvertieren mit Aspose.CAD für Java](/cad/java/cad-drawing-conversion/convert-cad-drawing-to-raster-image/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}