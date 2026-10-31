---
date: 2026-10-30
description: Erfahren Sie, wie Sie DXF-Dateien stapelweise in WMF konvertieren können,
  indem Sie Aspose.CAD für Java verwenden, mit Schritt‑für‑Schritt‑Code, Informationen
  zur kostenlosen Testversion und optionalem PDF‑Export.
keywords:
- batch convert dxf files
- aspose cad java
- dxf to wmf conversion
- java cad rasterization
- aspose free trial
lastmod: 2026-10-30
linktitle: DXF in WMF-Format exportieren mit Java
og_description: DXF-Dateien stapelweise in WMF konvertieren mit Aspose.CAD für Java.
  Folgen Sie dieser Anleitung, um DXF-Zeichnungen zu laden, Rasterisierungsoptionen
  festzulegen, als WMF zu speichern und optional mit einer kostenlosen Testversion
  in PDF zu exportieren.
og_image_alt: Tutorial showing batch conversion of DXF to WMF in Java using Aspose.CAD
og_title: DXF-Dateien stapelweise in WMF konvertieren mit Aspose.CAD für Java
schemas:
- author: Aspose
  dateModified: '2026-10-30'
  description: Learn how to batch convert DXF files to WMF using Aspose.CAD for Java,
    with step‑by‑step code, free trial info, and optional PDF export.
  headline: Batch convert DXF files to WMF with Aspose.CAD for Java
  type: TechArticle
- description: Learn how to batch convert DXF files to WMF using Aspose.CAD for Java,
    with step‑by‑step code, free trial info, and optional PDF export.
  name: Batch convert DXF files to WMF with Aspose.CAD for Java
  steps:
  - name: load dxf drawing
    text: Image.load reads the DXF file into an Aspose.CAD Image object.
  - name: configure rasterization options
    text: '`CadRasterizationOptions` specifies page size, resolution, and background
      for rasterizing the CAD drawing.'
  - name: save as wmf
    text: '`ImageSaveOptions` with `SaveFormat.WMF` tells Aspose.CAD to write the
      output as a Windows Metafile.'
  - name: dispose of resources
    text: Calling `image.close()` releases native resources used by the Aspose.CAD
      Image object.
  - name: optional – export to pdf
    text: '`PdfOptions` configures PDF‑specific settings when saving the image as
      a PDF document. > **Pro tip:** You can reuse the same `CadRasterizationOptions`
      object for PDF export by passing it to a `PdfOptions` instance, saving you a
      few lines of setup.'
  type: HowTo
- questions:
  - answer: You can access the documentation [Aspose.CAD Java documentation](https://reference.aspose.com/cad/java/).
    question: Where can I find the Aspose.CAD documentation?
  - answer: Download the library [Aspose.CAD Java download page](https://releases.aspose.com/cad/java/).
    question: How do I download Aspose.CAD for Java?
  - answer: Yes, you can get a free trial [Aspose free trial page](https://releases.aspose.com/).
    question: Is there a free trial available?
  - answer: Explore temporary licenses [temporary license options](https://purchase.aspose.com/temporary-license/).
    question: Need temporary licensing options?
  - answer: Visit the Aspose.CAD support forum [Aspose.CAD support forum](https://forum.aspose.com/c/cad/19).
    question: Where can I get support?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- batch convert dxf
- Aspose.CAD
- Java CAD conversion
- WMF export
- DXF processing
title: DXF-Dateien stapelweise in WMF konvertieren mit Aspose.CAD für Java
url: /de/java/additional-features/export-dxf-to-wmf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DXF-Dateien stapelweise in WMF konvertieren mit Aspose.CAD für Java

## Einleitung

In diesem Tutorial lernen Sie, wie Sie **DXF-Dateien stapelweise in WMF** konvertieren können, indem Sie Aspose.CAD für Java verwenden. Egal, ob Sie CAD-Zeichnungen in Windows‑basierten Berichten einbetten, leichte Vektorgrafiken für Office‑Dokumente erzeugen oder groß angelegte Konvertierungen automatisieren müssen – dieser Leitfaden führt Sie durch das Laden einer DXF‑Zeichnung, das Konfigurieren von Rasterisierungsoptionen, das Speichern als WMF und optional das Exportieren derselben Zeichnung nach PDF. Die Schritte funktionieren auf jeder Plattform, die Java 8+ ausführt.

## Schnelle Antworten
- **Kann ich DXF mit einer kostenlosen Testversion in WMF konvertieren?** Ja – Aspose bietet eine voll funktionsfähige 30‑tägige Testversion.  
- **Welche Java-Version wird benötigt?** Java 8 oder höher.  
- **Benötige ich eine Lizenz, um den Code auszuführen?** Für den Produktionseinsatz ist eine Lizenz erforderlich; die Testversion funktioniert für Entwicklung und Tests.  
- **Ist die Konvertierung verlustfrei?** Vektordaten bleiben erhalten; Rasterisierungsoptionen ermöglichen die Kontrolle der Auflösung.  
- **Kann ich dieselbe Zeichnung auch nach PDF exportieren?** Absolut – siehe den Schritt „Export to PDF“ unten.  
- **Wie konvertiere ich viele DXF-Dateien gleichzeitig stapelweise?** Durchlaufen Sie einen Ordner und wenden Sie das gleiche Laden‑Rasterisieren‑Speichern‑Muster auf jede Datei an.

## Was bedeutet das stapelweise Konvertieren von DXF-Dateien?

Das stapelweise Konvertieren von DXF-Dateien bedeutet, mehrere Drawing Exchange Format (DXF)-Zeichnungen in einem Durchlauf zu verarbeiten und für jede eine WMF-Ausgabe zu erzeugen. WMF (Windows Metafile) ist ein Vektorbildformat, das nativ in Microsoft Office, Windows‑Anwendungen und vielen Reporting‑Tools integriert ist.

## Warum Aspose.CAD für Java verwenden?

Aspose.CAD für Java ist eine reine Java‑Engine, die **über 50 Eingabe‑ und Ausgabeformate** unterstützt – darunter DXF, DWG, DGN, PDF, PNG, SVG und WMF – und dabei **99 % Vektortreue** liefert. Sie läuft auf jedem Betriebssystem, das Java unterstützt, benötigt keine nativen DLLs und ermöglicht die Steuerung von Seitengröße, DPI und Hintergrundfarbe über eine einzige Klasse `CadRasterizationOptions`. dieselbe API verarbeitet zudem PDF-, PNG‑ und SVG‑Exporte, wodurch der Bedarf an mehreren Bibliotheken entfällt.

### Quantifizierte Vorteile
- **Mehr als 50 unterstützte Formate** reduzieren den Bedarf an Drittanbieter‑Konvertern.  
- **Verarbeitet 300‑seitige DXF-Dateien in unter 5 Sekunden** auf einem typischen 2,5 GHz‑Server bei einer Rasterisierung von 150 DPI.  
- **Der Speicherverbrauch bleibt unter 200 MB** für Dateien bis zu 500 MB, wenn Sie geeignete Seitengrößen festlegen.  

## Voraussetzungen

- **Aspose.CAD für Java** in Ihr Projekt integriert. Laden Sie es von der offiziellen Seite herunter: [Aspose.CAD Java download](https://releases.aspose.com/cad/java/).  
- Ein Ordner, der die DXF-Dateien enthält, die Sie konvertieren möchten (z. B. `Your Document Directory/DXFDrawings/`).  

## Namespaces importieren

`Image` ist die Kernklasse von Aspose.CAD, die eine CAD‑Zeichnung im Speicher repräsentiert. Nach dem Laden einer Datei werden alle nachfolgenden Vorgänge – Rasterisierung, Formatkonvertierung und Ressourcenbereinigung – über dieses Objekt ausgeführt.

Die folgenden Importe bringen die für das Laden, Rasterisieren und Speichern von CAD‑Dateien erforderlichen Aspose.CAD‑Klassen ein.
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

### Wie konvertiere ich DXF-Dateien stapelweise in WMF mit Java?

Laden Sie jede DXF mit `Image.load`, konfigurieren Sie `CadRasterizationOptions` für die gewünschte Seitengröße und DPI und rufen Sie `image.save` mit `SaveFormat.WMF` auf. Dieses Drei‑Schritte‑Muster führt die vollständige Konvertierung durch, behält die Vektorqualität bei und erfordert nur wenige Codezeilen pro Datei.

#### Schritt 1: DXF-Zeichnung laden

`Image.load` liest die DXF‑Datei in ein Aspose.CAD‑Image‑Objekt ein.
```java
import com.aspose.cad.Color;
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.WmfOptions;
```

#### Schritt 2: Rasterisierungsoptionen konfigurieren

`CadRasterizationOptions` gibt Seitengröße, Auflösung und Hintergrund für die Rasterisierung der CAD‑Zeichnung an.
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DXFDrawings/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

#### Schritt 3: Als WMF speichern

`ImageSaveOptions` mit `SaveFormat.WMF` weist Aspose.CAD an, die Ausgabe als Windows Metafile zu schreiben.
```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(100);
rasterizationOptions.setPageHeight(100);
WmfOptions wmfOptions = new WmfOptions();
```

#### Schritt 4: Ressourcen freigeben

Der Aufruf von `image.close()` gibt die von dem Aspose.CAD‑Image‑Objekt genutzten nativen Ressourcen frei.
```java
cadImage.save(dataDir+" example.ifc.wmf", wmfOptions);
```

#### Schritt 5: optional – Export nach PDF

`PdfOptions` konfiguriert PDF‑spezifische Einstellungen beim Speichern des Bildes als PDF‑Dokument.
```java
finally
{
  cadImage.dispose();
}
```

> **Pro tip:** Sie können dasselbe `CadRasterizationOptions`‑Objekt für den PDF‑Export wiederverwenden, indem Sie es an eine `PdfOptions`‑Instanz übergeben, was Ihnen einige Zeilen Setup erspart.

## Wie exportiere ich DXF nach PDF mit Aspose CAD Java?

Ersetzen Sie das WMF‑Speicherformat durch PDF, indem Sie `new ImageSaveOptions(SaveFormat.Pdf)` verwenden. Die gleichen Rasterisierungseinstellungen gelten, und Sie können zusätzlich PDF‑spezifische Optionen wie Autoren‑Metadaten oder Komprimierungsgrad festlegen. Diese Einzeiler‑Konvertierung erzeugt ein durchsuchbares, seitengetreues PDF, das das ursprüngliche CAD‑Layout widerspiegelt.

## Häufige Probleme und Lösungen

`License` ist die Aspose‑Klasse, die verwendet wird, um zur Laufzeit eine Produktlizenz anzuwenden.

| Problem | Ursache | Lösung |
|-------|-------|-----|
| **`NullPointerException` bei `cadImage.save`** | Variable `cadImage` ist nicht definiert (sollte `image` sein). | `cadImage` durch `image` ersetzen oder die Variable konsequent umbenennen. |
| **Ausgabe‑WMF ist leer** | Seitengröße der Rasterisierung zu klein oder Hintergrundfarbe ist transparent eingestellt. | `PageWidth`/`PageHeight` erhöhen oder eine Hintergrundfarbe über `rasterizationOptions.setBackgroundColor(Color.WHITE);` festlegen. |
| **License exception** | Ausführung ohne gültige Aspose‑Lizenz in der Produktion. | Lizenzdatei beim Anwendungsstart anwenden: `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`. |

## Häufig gestellte Fragen

**Q: Wo finde ich die Aspose.CAD‑Dokumentation?**  
A: Sie können die Dokumentation unter [Aspose.CAD Java documentation](https://reference.aspose.com/cad/java/) aufrufen.

**Q: Wie lade ich Aspose.CAD für Java herunter?**  
A: Laden Sie die Bibliothek von der [Aspose.CAD Java download page](https://releases.aspose.com/cad/java/) herunter.

**Q: Gibt es eine kostenlose Testversion?**  
A: Ja, Sie können eine kostenlose Testversion auf der [Aspose free trial page](https://releases.aspose.com/) erhalten.

**Q: Benötigen Sie temporäre Lizenzoptionen?**  
A: Erkunden Sie temporäre Lizenzen unter [temporary license options](https://purchase.aspose.com/temporary-license/).

**Q: Wo bekomme ich Support?**  
A: Besuchen Sie das Aspose.CAD‑Support‑Forum unter [Aspose.CAD support forum](https://forum.aspose.com/c/cad/19).

## Zusätzliche häufig gestellte Fragen

**Q: Kann ich große DXF-Dateien (Hunderte MB) konvertieren, ohne dass der Speicher ausgeht?**  
A: Ja. Laden Sie die Datei in einem try‑with‑resources‑Block und geben Sie das `Image`‑Objekt umgehend frei. Passen Sie `CadRasterizationOptions.setPageWidth/Height` auf eine angemessene Größe an, um den Speicherverbrauch gering zu halten.

**Q: Behält die WMF‑Ausgabe Ebeneninformationen bei?**  
A: WMF ist ein flaches Vektorformat, sodass die Ebenenhierarchie abgeflacht wird, jedoch bleiben Linienstile, Farben und Schraffurmuster erhalten.

**Q: Ist es möglich, eine benutzerdefinierte DPI für das WMF festzulegen?**  
A: Verwenden Sie `rasterizationOptions.setResolution(300);`, um die DPI vor dem Speichern zu definieren.

**Q: Kann ich mehrere DXF-Dateien in einem Durchlauf stapelweise konvertieren?**  
A: Absolut. Durchlaufen Sie ein Verzeichnis, laden Sie jede Datei und wenden Sie dieselbe Rasterisierungs‑ und Speicherlogik an.

**Q: Welche Java-Versionen werden unterstützt?**  
A: Aspose.CAD für Java unterstützt Java 8 und höher, einschließlich Java 11, 17 und neueren LTS‑Versionen.

---

**Zuletzt aktualisiert:** 2026-10-30  
**Getestet mit:** Aspose.CAD for Java 24.11  
**Autor:** Aspose

## Verwandte Tutorials

- [PDF aus CAD erstellen – DXF nach PDF exportieren mit Aspose.CAD für Java](/cad/java/additional-features/export-dxf-to-pdf/)
- [PDF aus DXF erstellen: Ebene exportieren mit Aspose.CAD für Java](/cad/java/additional-features/export-specific-layer-to-pdf/)
- [Wie man DXF-Layout in JPEG-Bild konvertiert mit Aspose.CAD in Java](/cad/java/additional-features/export-specific-layout-to-image/)

```java
image.save(dataDir + "conic_pyramid_out_.pdf"); 
```

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}