---
date: 2026-06-09
description: Erfahren Sie, wie Sie DXF mit Aspose.CAD für Java in WMF konvertieren,
  inklusive einer kostenlosen Testversion, Unterstützung für Java 8+ und optionalem
  PDF-Export. Schritt‑für‑Schritt‑Anleitung mit Code‑Beispielen.
keywords:
- convert dxf to wmf
- aspose cad java
- aspose free trial
- aspose cad conversion
- export dxf pdf
linktitle: DXF in WMF-Format exportieren mit Java
schemas:
- author: Aspose
  dateModified: '2026-06-09'
  description: Learn how to convert DXF to WMF with Aspose.CAD for Java, including
    a free trial, Java 8+ support, and optional PDF export. Step‑by‑step guide with
    code examples.
  headline: Convert DXF to WMF Using Aspose.CAD in Java
  type: TechArticle
- description: Learn how to convert DXF to WMF with Aspose.CAD for Java, including
    a free trial, Java 8+ support, and optional PDF export. Step‑by‑step guide with
    code examples.
  name: Convert DXF to WMF Using Aspose.CAD in Java
  steps:
  - name: Load DXF Drawing
    text: Image.load reads the DXF file into an Aspose.CAD Image object.
  - name: Configure Rasterization Options
    text: CadRasterizationOptions specifies page size, resolution, and background
      for rasterizing the CAD drawing.
  - name: Save as WMF
    text: ImageSaveOptions with SaveFormat.WMF tells Aspose.CAD to write the output
      as a Windows Metafile.
  - name: Dispose of Resources
    text: Calling image.close() releases native resources used by the Aspose.CAD Image
      object.
  - name: Optional – Export to PDF
    text: PdfOptions configures PDF‑specific settings when saving the image as a PDF
      document. > **Pro tip:** You can reuse the same `CadRasterizationOptions` object
      for PDF export by passing it to a `PdfOptions` instance, saving you a few lines
      of setup.
  type: HowTo
- questions:
  - answer: Yes. Load the file in a try‑with‑resources block and dispose of the `Image`
      object promptly. Adjust `CadRasterizationOptions.setPageWidth/Height` to a reasonable
      size to keep memory usage low.
    question: Can I convert large DXF files (hundreds of MB) without running out of
      memory?
  - answer: WMF is a flat vector format, so layer hierarchy is flattened, but line
      styles, colors, and hatch patterns are preserved.
    question: Does the WMF output retain layer information?
  - answer: Use `rasterizationOptions.setResolution(300);` to define DPI before saving.
    question: Is it possible to set a custom DPI for the WMF?
  - answer: Absolutely. Loop through a directory, load each file, and apply the same
      rasterization and save logic.
    question: Can I batch‑convert multiple DXF files in one run?
  - answer: Aspose.CAD for Java supports Java 8 and later, including Java 11, 17,
      and newer LTS releases.
    question: What versions of Java are supported?
  type: FAQPage
second_title: Aspose.CAD Java API
title: DXF nach WMF konvertieren mit Aspose.CAD in Java
url: /de/java/additional-features/export-dxf-to-wmf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DXF in WMF mit Aspose.CAD in Java konvertieren

## Einführung

In diesem Tutorial erfahren Sie, wie Sie **DXF in WMF** mit Aspose.CAD für Java konvertieren. Egal, ob Sie CAD‑Zeichnungen in einen Windows‑basierten Bericht einbetten, leichte Vektorgrafiken für Office‑Dokumente erzeugen oder Stapelkonvertierungen automatisieren müssen, die Konvertierung von DXF nach WMF ist ein häufiges Bedürfnis in Ingenieur‑ und Reporting‑Pipelines. Wir führen Sie durch das Laden einer DXF‑Zeichnung, das Konfigurieren von Rasterisierungsoptionen, das Speichern des Ergebnisses als WMF und optional das Exportieren derselben Zeichnung nach PDF.

## Schnelle Antworten
- **Kann ich DXF mit einer kostenlosen Testversion in WMF konvertieren?** Ja – Aspose bietet eine voll funktionsfähige 30‑tägige Testversion.  
- **Welche Java‑Version wird benötigt?** Java 8 oder höher.  
- **Benötige ich eine Lizenz, um den Code auszuführen?** Eine Lizenz ist für die Produktion erforderlich; die Testversion funktioniert für Entwicklung und Tests.  
- **Ist die Konvertierung verlustfrei?** Vektordaten werden erhalten; Rasterisierungsoptionen ermöglichen die Kontrolle der Auflösung.  
- **Kann ich dieselbe Zeichnung auch nach PDF exportieren?** Absolut – siehe den Schritt „Export nach PDF“ unten.

## Was bedeutet „DXF in WMF konvertieren“?

Die Konvertierung von DXF nach WMF bedeutet, dass eine Drawing Exchange Format (DXF)‑Datei – ein weit verbreitetes CAD‑Format – in ein Windows Metafile (WMF) umgewandelt wird. WMF ist ein Vektor‑Bildformat, das sich nahtlos in Microsoft Office, Windows‑Anwendungen und viele Reporting‑Tools integrieren lässt.

## Warum Aspose.CAD für Java verwenden?

Aspose.CAD für Java bietet eine reine Java‑Engine ohne native DLLs, die CAD‑Dateien mit **über 99 % Vektor‑Treue** konvertiert und dabei Ebenen, Farben, Linienstile und Schraffurmuster bewahrt. Es unterstützt **mehr als 50 Eingabe‑ und Ausgabeformate** – darunter DXF, DWG, DGN, PDF, PNG, SVG und WMF – und ermöglicht das Feintuning von Seitengröße, DPI und Hintergrundfarbe über integrierte Rasterisierungsoptionen. Die gleiche API verarbeitet zudem PDF-, PNG‑ und SVG‑Exporte, sodass keine zusätzlichen Bibliotheken nötig sind.

### Wesentliche Vorteile
- **Keine externen Abhängigkeiten** – reines Java, funktioniert auf jedem OS, das Java ausführt.  
- **Hoch‑fidelitäts‑Rendering** – behält Linienstärke, Farbe und Schraffurdetails bei.  
- **Eingebaute Rasterisierung** – Steuerung von Seitengröße, Auflösung und Hintergrund.  
- **All‑in‑One‑Konvertierung** – dieselben Klassen exportieren nach WMF, PDF, PNG, SVG usw.

## Voraussetzungen

- **Aspose.CAD für Java** in Ihr Projekt integriert. Laden Sie es von der offiziellen Seite herunter: [Aspose.CAD Java download](https://releases.aspose.com/cad/java/).  
- **Dokumentenverzeichnis**, in dem Ihre DXF‑Dateien gespeichert sind (z. B. `Your Document Directory/DXFDrawings/`).  

## Namespaces importieren

Die folgenden Importe bringen die für das Laden, Rasterisieren und Speichern von CAD‑Dateien benötigten Aspose.CAD‑Klassen ein.  
```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageSaveOptions;
import com.aspose.cad.fileformats.cad.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.CadImageInfo;
import com.aspose.cad.fileformats.cad.CadImageInfo;
import java.awt.Color;
```

## Schritt‑für‑Schritt‑Anleitung

### Wie konvertiere ich DXF in WMF in Java?

Laden Sie Ihre DXF‑Datei mit `Image.load("yourFile.dxf")`, konfigurieren Sie `CadRasterizationOptions` für die gewünschte Seitengröße und DPI und rufen Sie anschließend `image.save("output.wmf", new ImageSaveOptions(SaveFormat.WMF))` auf. Dieses Drei‑Schritt‑Muster führt die vollständige Konvertierung durch, bewahrt die Vektor‑Qualität und erfordert nur wenige Code‑Zeilen.

#### Schritt 1: DXF‑Zeichnung laden

Image.load liest die DXF‑Datei in ein Aspose.CAD Image‑Objekt ein.  
```java
import com.aspose.cad.Color;
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.WmfOptions;
```

#### Schritt 2: Rasterisierungsoptionen konfigurieren

CadRasterizationOptions gibt Seitengröße, Auflösung und Hintergrund für die Rasterisierung der CAD‑Zeichnung an.  
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DXFDrawings/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

#### Schritt 3: Als WMF speichern

ImageSaveOptions mit SaveFormat.WMF weist Aspose.CAD an, die Ausgabe als Windows Metafile zu schreiben.  
```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(100);
rasterizationOptions.setPageHeight(100);
WmfOptions wmfOptions = new WmfOptions();
```

#### Schritt 4: Ressourcen freigeben

Der Aufruf von image.close() gibt die von dem Aspose.CAD Image‑Objekt genutzten nativen Ressourcen frei.  
```java
cadImage.save(dataDir+" example.ifc.wmf", wmfOptions);
```

#### Schritt 5: Optional – Export nach PDF

PdfOptions konfiguriert PDF‑spezifische Einstellungen beim Speichern des Bildes als PDF‑Dokument.  
```java
finally
{
  cadImage.dispose();
}
```

> **Pro‑Tipp:** Sie können dasselbe `CadRasterizationOptions`‑Objekt für den PDF‑Export wiederverwenden, indem Sie es an eine `PdfOptions`‑Instanz übergeben – das spart ein paar Zeilen Setup.

## Wie exportiere ich DXF nach PDF mit Aspose CAD Java?

Der Export nach PDF folgt denselben Lade‑ und Rasterisierungsschritten; ersetzen Sie einfach das WMF‑Speicherformat durch PDF. Verwenden Sie `new ImageSaveOptions(SaveFormat.Pdf)` und setzen Sie optional PDF‑spezifische Optionen wie Kompressionsgrad oder Autor‑Metadaten. Dieser Einzeiler erzeugt ein durchsuchbares, seitengetreues PDF, das das ursprüngliche CAD‑Layout exakt widerspiegelt.

## Häufige Probleme und Lösungen

| Problem | Ursache | Lösung |
|---------|---------|--------|
| **`NullPointerException` on `cadImage.save`** | Variable `cadImage` nicht definiert (sollte `image` sein). | Ersetzen Sie `cadImage` durch `image` oder benennen Sie die Variable konsistent um. |
| **Output WMF is blank** | Rasterisierungs‑Seitengröße zu klein oder Hintergrundfarbe auf transparent gesetzt. | Erhöhen Sie `PageWidth`/`PageHeight` oder setzen Sie eine Hintergrundfarbe via `rasterizationOptions.setBackgroundColor(Color.WHITE);`. |
| **License exception** | Ausführung ohne gültige Aspose‑Lizenz in der Produktion. | Laden Sie die Lizenzdatei beim Anwendungsstart: `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`. |

## Fazit

Sie verfügen nun über einen vollständigen, produktions‑bereiten Workflow, um **DXF in WMF** mit Aspose.CAD für Java zu konvertieren, mit einem optionalen Schritt zum **Export derselben Zeichnung nach PDF**. Dieser Ansatz liefert hochwertige Vektor‑Ausgaben, die sich nahtlos in Windows‑basierte Reporting‑ und Dokumentations‑Tools integrieren, und hält Ihren Code‑Bestand einfach und ohne zusätzliche Abhängigkeiten.

## FAQ

### Q1: Wo finde ich die Aspose.CAD‑Dokumentation?

Sie können die Dokumentation [hier](https://reference.aspose.com/cad/java/) aufrufen.

### Q2: Wie lade ich Aspose.CAD für Java herunter?

Laden Sie die Bibliothek [hier](https://releases.aspose.com/cad/java/) herunter.

### Q3: Gibt es eine kostenlose Testversion?

Ja, Sie können eine kostenlose Testversion [hier](https://releases.aspose.com/) erhalten.

### Q4: Benötige ich temporäre Lizenzoptionen?

Erkunden Sie temporäre Lizenzen [hier](https://purchase.aspose.com/temporary-license/).

### Q5: Wo bekomme ich Support?

Besuchen Sie das Aspose.CAD‑Support‑Forum [hier](https://forum.aspose.com/c/cad/19).

## Häufig gestellte Fragen

**Q: Kann ich große DXF‑Dateien (hunderte MB) konvertieren, ohne dass der Speicher ausgeht?**  
A: Ja. Laden Sie die Datei in einem try‑with‑resources‑Block und geben Sie das `Image`‑Objekt sofort wieder frei. Passen Sie `CadRasterizationOptions.setPageWidth/Height` auf eine vernünftige Größe an, um den Speicherverbrauch gering zu halten.

**Q: Behält die WMF‑Ausgabe Ebeneninformationen bei?**  
A: WMF ist ein flaches Vektorformat, sodass die Ebenenhierarchie abgeflacht wird, aber Linienstile, Farben und Schraffurmuster bleiben erhalten.

**Q: Ist es möglich, eine benutzerdefinierte DPI für das WMF festzulegen?**  
A: Verwenden Sie `rasterizationOptions.setResolution(300);`, um die DPI vor dem Speichern zu definieren.

**Q: Kann ich mehrere DXF‑Dateien in einem Durchlauf stapelweise konvertieren?**  
A: Absolut. Durchlaufen Sie ein Verzeichnis, laden Sie jede Datei und wenden Sie dieselbe Rasterisierungs‑ und Speicherlogik an.

**Q: Welche Java‑Versionen werden unterstützt?**  
A: Aspose.CAD für Java unterstützt Java 8 und höher, einschließlich Java 11, 17 und neueren LTS‑Versionen.

**Last Updated:** 2026-06-09  
**Tested With:** Aspose.CAD for Java 24.11  
**Author:** Aspose

```java
image.save(dataDir + "conic_pyramid_out_.pdf"); 
```

## Verwandte Tutorials

- [Create PDF from CAD – Export DXF to PDF with Aspose.CAD for Java](/cad/java/additional-features/export-dxf-to-pdf/)
- [Create PDF from DXF: Export Layer with Aspose.CAD for Java](/cad/java/additional-features/export-specific-layer-to-pdf/)
- [How to Convert DXF Layout to JPEG Image with Aspose.CAD in Java](/cad/java/additional-features/export-specific-layout-to-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}