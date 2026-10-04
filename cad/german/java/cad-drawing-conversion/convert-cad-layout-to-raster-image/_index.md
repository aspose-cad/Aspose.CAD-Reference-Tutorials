---
date: 2026-10-04
description: Erfahren Sie, wie Sie DWG schnell in PNG konvertieren und CAD mit Aspose.CAD
  for Java als PNG oder andere Rasterformate exportieren können. Erhalten Sie hochwertige
  Ergebnisse schnell.
keywords:
- convert dwg to png
- dwg to raster image
- convert cad to pdf
- export cad as png
- convert dwg to jpeg
lastmod: 2026-10-04
linktitle: CAD-Layout in Rasterbildformat konvertieren
og_description: Konvertieren Sie DWG schnell in PNG mit Aspose.CAD for Java. Erfahren
  Sie Schritt für Schritt, wie Sie CAD als PNG, JPEG, TIFF und mehr exportieren.
og_image_alt: 'Developer guide: Convert DWG to PNG and other raster formats using
  Aspose.CAD for Java'
og_title: DWG in PNG und andere Rasterformate mit Aspose.CAD for Java konvertieren
schemas:
- author: Aspose
  dateModified: '2026-10-04'
  description: Learn how to quickly convert dwg to png and export cad as png or other
    raster formats using Aspose.CAD for Java. Get high‑quality results fast.
  headline: Convert DWG to PNG and other raster formats using Aspose.CAD for Java
  type: TechArticle
- description: Learn how to quickly convert dwg to png and export cad as png or other
    raster formats using Aspose.CAD for Java. Get high‑quality results fast.
  name: Convert DWG to PNG and other raster formats using Aspose.CAD for Java
  steps:
  - name: set up the resource directory
    text: Replace `"Your Document Directory"` with the absolute path where your CAD
      files reside. This directory will be used for both input and output files.
  - name: load the CAD file
    text: '`Image.load` parses the source file and creates an in‑memory representation
      that you can rasterize. You can load any supported format (DWG, DXF, DGN, etc.)
      – this is the **how to convert cad** part.'
  - name: configure rasterization options
    text: '`CadRasterizationOptions` defines how the vector data is turned into pixels.
      `setPageWidth` and `setPageHeight` control output resolution (larger values
      = higher DPI). `setLayouts` lets you **convert CAD to raster** for specific
      layouts; omit it to rasterize the whole drawing.'
  - name: set image options
    text: '`TiffOptions` (or `PngOptions` for PNG) tells Aspose which raster format
      to generate and lets you fine‑tune compression, color depth, and other format‑specific
      settings. Choose the options class that matches your desired output.'
  - name: save the resultant image
    text: Call `save` on the `Image` instance, passing the output file name and the
      options object. Change the file extension to `.png` (and use `PngOptions`) to
      **save CAD as PNG**. The same pattern works for JPEG, BMP, or PDF. > **Common
      pitfall:** Forgetting to match the file extension with the options cla
  type: HowTo
- questions:
  - answer: Yes, it supports over 30 CAD and raster formats, including DWG, DXF, DGN,
      and SVG.
    question: Is Aspose.CAD compatible with different CAD file formats?
  - answer: Absolutely. Adjust `setPageWidth`, `setPageHeight`, or `setResolution`
      in `CadRasterizationOptions` to achieve the desired DPI.
    question: Can I customize the resolution of the output raster image?
  - answer: Provide an array with all layout names to `setLayouts`, e.g., `new String[]{"Model","Layout1","Layout2"}`.
    question: How can I convert multiple CAD layouts in a single run?
  - answer: Yes—PNG, JPEG, BMP, PDF, and more are available via their respective `*Options`
      classes.
    question: Are there output formats besides TIFF supported?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community
      support and official assistance.
    question: Where can I get help or share my experience with Aspose.CAD?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- convert dwg
- Aspose.CAD
- Java raster conversion
- CAD image processing
title: DWG in PNG und andere Rasterformate mit Aspose.CAD for Java konvertieren
url: /de/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG in PNG und andere Rasterformate mit Aspose.CAD für Java konvertieren

## Einführung

`Aspose.CAD for Java` ist eine Bibliothek, die die programmgesteuerte Konvertierung von CAD‑Dateien in Rasterbilder wie PNG, JPEG und TIFF ermöglicht. Die Konvertierung von DWG zu PNG (oder anderen Rasterbildformaten) ist ein häufiges Bedürfnis, wenn Sie CAD‑Zeichnungen mit Teamkollegen teilen müssen, die keinen CAD‑Viewer besitzen, Designs in Dokumentationen einbetten oder Thumbnails für Web‑Galerien erzeugen wollen. In diesem Leitfaden lernen Sie, wie Sie DWG schnell und zuverlässig in PNG umwandeln, egal ob Sie mit einer kompletten Zeichnungsdatei oder nur einem bestimmten Layout arbeiten. Möglicherweise müssen Sie auch **CAD in Raster konvertieren** für Web‑Vorschauen, Reporting‑Tools oder mobile Apps.

## Schnelle Antworten
- **Welche Bibliothek verarbeitet DWG zu PNG?** Aspose.CAD for Java stellt die Konvertierungs‑Engine bereit.  
- **Welche Rasterformate kann ich exportieren?** PNG, JPEG, TIFF, PDF, BMP und mehr als 30 weitere Formate.  
- **Benötige ich eine Lizenz für Tests?** Eine kostenlose Testversion funktioniert für die Entwicklung; für die Produktion ist eine kommerzielle Lizenz erforderlich.  
- **Kann ich ein bestimmtes Layout auswählen?** Ja – verwenden Sie `setLayouts`, um „Model“, „Layout1“ usw. anzusprechen.  
- **Ist eine hochauflösende Ausgabe möglich?** Absolut – passen Sie `setPageWidth` und `setPageHeight` (oder `setResolution`) an, um die DPI zu steuern.

## Was bedeutet „DWG in PNG konvertieren“?

DWG in PNG zu konvertieren bedeutet, eine DWG‑Vektorkonstruktion in ein pixelbasiertes PNG‑Bild zu verwandeln, das von jedem gängigen Bildbetrachter angezeigt werden kann. Dieser Vorgang rasterisiert Vektorelemente, bewahrt Linienstärken, Farben und Ebenen und überträgt sie in ein festauflösendes Bitmap. Das Ergebnis ist ideal für die Einbettung in PDFs, Word‑Dokumente oder Webseiten, wo Vektorunterstützung begrenzt ist.

## Warum CAD als PNG (oder andere Rasterformate) exportieren?

Der Export von CAD als PNG bietet universelle Kompatibilität, schnelles Laden und einfache Einbettung auf allen gängigen Plattformen. Rasterbilder laden sofort im Vergleich zum Öffnen einer schweren DWG‑Datei, und die verlustfreie Kompression von PNG gewährleistet visuelle Treue. Durch die Steuerung von Auflösung, Hintergrundfarbe und Layout stellen Sie sicher, dass jeder Stakeholder das gleiche Erscheinungsbild sieht, egal ob die Datei auf einem Desktop, Mobilgerät oder im Browser betrachtet wird.

## Häufige Anwendungsfälle

| Szenario | Warum Rasterausgabe hilft |
|----------|----------------------------|
| **Projektdokumentation** | Das Einbetten von PNGs in PDFs oder Word‑Dokumente vermeidet, dass Reviewer CAD‑Software benötigen. |
| **Webportale** | Vorschaubilder, die aus DWG‑Dateien erzeugt werden, laden sofort und verbessern die Benutzererfahrung. |
| **Mobile Apps** | Rasterbilder werden korrekt auf Geräten angezeigt, die keinen CAD‑Viewer besitzen. |
| **Automatisiertes Reporting** | Mehrere Layouts stapelweise in PNG/JPEG konvertieren, um sie in Diagrammen oder Dashboards einzufügen. |

## Voraussetzungen

Bevor Sie beginnen, stellen Sie sicher, dass Sie Folgendes haben:

1. **Java-Entwicklungsumgebung** – JDK 8 oder neuer installiert und konfiguriert.  
2. **Aspose.CAD für Java** – Laden Sie die neueste JAR von der [Aspose.CAD für Java Dokumentation](https://reference.aspose.com/cad/java/) herunter.  

## Namensräume importieren

`com.aspose.cad.Image` ist die Kernklasse, die jede CAD‑Datei im Speicher repräsentiert. `com.aspose.cad.imageoptions.*` stellt Options‑Objekte für jedes Rasterformat bereit. Importieren Sie die Klassen, die Sie benötigen, um eine Zeichnung zu laden, die Rasterisierung zu konfigurieren und das Ergebnis zu speichern.

> **Profi‑Tipp:** Wenn Sie **CAD als PNG exportieren** statt TIFF möchten, ersetzen Sie `TiffOptions` durch `PngOptions` (zu finden in `com.aspose.cad.imageoptions.PngOptions`).

## Schritt‑für‑Schritt-Anleitung

### Schritt 1: Ressourcenverzeichnis einrichten

Ersetzen Sie `"Your Document Directory"` durch den absoluten Pfad, in dem Ihre CAD‑Dateien liegen. Dieses Verzeichnis wird sowohl für Eingabe‑ als auch Ausgabedateien verwendet.

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

### Schritt 2: CAD-Datei laden

`Image.load` analysiert die Quelldatei und erstellt eine In‑Memory‑Repräsentation, die Sie rasterisieren können. Sie können jedes unterstützte Format (DWG, DXF, DGN usw.) laden – das ist der **Wie‑man‑CAD‑konvertiert**‑Teil.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";
```

### Schritt 3: Rasterisierungsoptionen konfigurieren

`CadRasterizationOptions` definiert, wie die Vektordaten in Pixel umgewandelt werden. `setPageWidth` und `setPageHeight` steuern die Ausgaberesolution (größere Werte = höhere DPI). `setLayouts` ermöglicht es Ihnen, **CAD in Raster** für bestimmte Layouts zu konvertieren; lassen Sie es weg, um die gesamte Zeichnung zu rasterisieren.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### Schritt 4: Bildoptionen festlegen

`TiffOptions` (oder `PngOptions` für PNG) teilt Aspose mit, welches Rasterformat erzeugt werden soll, und lässt Sie Kompression, Farbtiefe und andere format‑spezifische Einstellungen feinjustieren. Wählen Sie die Options‑Klasse, die Ihrem gewünschten Ausgabeformat entspricht.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
rasterizationOptions.setLayouts(new String[] {"Model", "Layout1"});
```

### Schritt 5: Ergebnisbild speichern

Rufen Sie `save` auf der `Image`‑Instanz auf und übergeben Sie den Ausgabedateinamen sowie das Options‑Objekt. Ändern Sie die Dateierweiterung zu `.png` (und verwenden Sie `PngOptions`), um **CAD als PNG zu speichern**. Das gleiche Muster funktioniert für JPEG, BMP oder PDF.

```java
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.setVectorRasterizationOptions(rasterizationOptions);
```

> **Häufiges Problem:** Wenn die Dateierweiterung nicht zur Options‑Klasse passt, entsteht eine `UnsupportedFormatException`. Halten Sie sie immer synchron.

## Häufige Probleme und Lösungen

| Problem | Lösung |
|---------|--------|
| **Leeres Ausgabebild** | Stellen Sie sicher, dass die Layoutnamen in `setLayouts` exakt mit denen in der Quell‑CAD‑Datei übereinstimmen. |
| **Niedrigauflösendes PNG** | Erhöhen Sie `setPageWidth` / `setPageHeight` oder setzen Sie `setResolution` in den Rasterisierungsoptionen. |
| **Nicht unterstützte DWG-Version** | Stellen Sie sicher, dass Sie die neueste Aspose.CAD‑Version verwenden; ältere Versionen unterstützen möglicherweise neuere DWG‑Versionen nicht. |
| **Speicherfehler bei großen Dateien** | Verarbeiten Sie Seiten einzeln oder erhöhen Sie den JVM‑Heap (`-Xmx2g`). |

## Häufig gestellte Fragen

**Q:** Ist Aspose.CAD mit verschiedenen CAD-Dateiformaten kompatibel?  
**A:** Ja, es unterstützt über 30 CAD‑ und Rasterformate, darunter DWG, DXF, DGN und SVG.

**Q:** Kann ich die Auflösung des Ausgabebildes anpassen?  
**A:** Absolut. Passen Sie `setPageWidth`, `setPageHeight` oder `setResolution` in `CadRasterizationOptions` an, um die gewünschte DPI zu erreichen.

**Q:** Wie kann ich mehrere CAD‑Layouts in einem Durchlauf konvertieren?  
**A:** Übergeben Sie ein Array mit allen Layoutnamen an `setLayouts`, z. B. `new String[]{"Model","Layout1","Layout2"}`.

**Q:** Gibt es neben TIFF weitere unterstützte Ausgabeformate?  
**A:** Ja – PNG, JPEG, BMP, PDF und weitere sind über die jeweiligen `*Options`‑Klassen verfügbar.

**Q:** Wo kann ich Hilfe erhalten oder meine Erfahrungen mit Aspose.CAD teilen?  
**A:** Besuchen Sie das [Aspose.CAD‑Forum](https://forum.aspose.com/c/cad/19) für Community‑Support und offizielle Unterstützung.

## Fazit

Indem Sie diese Schritte befolgen, können Sie **DWG in PNG konvertieren**, **CAD als PNG exportieren**, **CAD als JPEG speichern** oder jedes andere benötigte Rasterformat erzeugen. Aspose.CAD für Java übernimmt die schwere Arbeit, sodass Sie sich darauf konzentrieren können, hochwertige Bilder in Ihre Anwendungen, Dokumentationen oder Web‑Portale zu integrieren. Die Unterstützung von über 30 Formaten und die Fähigkeit, mehrhundertseitige Zeichnungen zu rendern, ohne die gesamte Datei in den Speicher zu laden, machen die Bibliothek zu einer robusten Wahl für unternehmensweite CAD‑Rasterisierung.

---

**Zuletzt aktualisiert:** 2026-10-04  
**Getestet mit:** Aspose.CAD für Java 24.12  
**Autor:** Aspose  







```java
image.save(dataDir + "conic_pyramid_layoutstorasterimage_out_.tiff", options);
```

```bash
java -jar aspose-cad.jar -i input.dwg -o output.png -w 1200 -h 1200
```

## Verwandte Tutorials

- [DWG schnell nach PDF oder Raster exportieren mit Java CAD-Bibliothek Aspose.CAD für Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [DWG nach BMP konvertieren mit Aspose.CAD für Java](/cad/java/cad-export-options/export-to-bmp/)
- [DWG nach PDF exportieren: Bestimmtes Layout mit Aspose.CAD für Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}