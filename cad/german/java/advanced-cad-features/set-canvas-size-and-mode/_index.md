---
date: 2026-08-29
description: Erfahren Sie, wie Sie die PDF‑Seitengröße festlegen und CAD mit Aspose.CAD
  für Java in PDF konvertieren, mit automatischer Layoutskalierung und TIFF‑Export.
keywords:
- set pdf page size
- convert cad to pdf
- canvas size java
- high resolution tiff
- change pdf dimensions
lastmod: 2026-08-29
linktitle: PDF‑Seitengröße festlegen – CAD zu PDF konvertieren
og_description: Erfahren Sie, wie Sie die PDF‑Seitengröße beim Konvertieren von CAD‑Zeichnungen
  zu PDF in Java mit Aspose.CAD festlegen. Dieser Leitfaden behandelt Canvas‑Abmessungen,
  automatische Layoutskalierung und den Export in hochauflösendes TIFF.
og_image_alt: Tutorial showing how to set pdf page size and convert CAD to PDF in
  Java
og_title: PDF‑Seitengröße festlegen – CAD zu PDF mit Aspose in Java
schemas:
- author: Aspose
  dateModified: '2026-08-29'
  description: Learn how to set pdf page size and convert CAD to PDF using Aspose.CAD
    for Java, with automatic layout scaling and TIFF export.
  headline: Set pdf page size – convert cad to pdf (Java)
  type: TechArticle
- questions:
  - answer: No. Canvas size controls page dimensions; vector data remains resolution‑independent,
      ensuring crisp rendering at any zoom level.
    question: does the canvas size affect vector quality in the PDF?
  - answer: Yes. Adjust `rasterizationOptions.setResolution(dpiValue)` before creating
      `TiffOptions`.
    question: can I set a different DPI for the TIFF output?
  - answer: Use Aspose.PDF to load the generated PDF and call `pdf.getPages().setPageSize(PageSize.A4)`
      or a custom size.
    question: how can I change PDF dimensions for an existing PDF without re‑rendering
      the CAD?
  - answer: Keep `setAutomaticLayoutsScaling(true)` and avoid `setNoScaling(true)`;
      this retains layer visibility and layout fidelity.
    question: what is the best way to convert dxf to pdf while preserving layers?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- set pdf page size
- convert cad
- Aspose.CAD
- Java
- high resolution tiff
title: PDF‑Seitengröße festlegen – CAD zu PDF konvertieren (Java)
url: /de/java/advanced-cad-features/set-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PDF-Seitengröße festlegen – CAD in PDF konvertieren (Java)

## Einleitung

Wenn Sie **set pdf page size** festlegen müssen, während Sie CAD-Zeichnungen in PDF konvertieren, sind Sie hier genau richtig. In diesem Tutorial zeigen wir Ihnen, wie Sie Aspose.CAD für Java verwenden, um genaue Canvas‑Abmessungen zu definieren, die automatische Layout‑Skalierung zu aktivieren und das Ergebnis sowohl als PDF als auch als TIFF zu exportieren. Egal, ob Sie technische Schemata für den Druck vorbereiten oder Miniaturansichten für eine Web‑Galerie erzeugen, die Kontrolle über die Seitengröße und die output resolution ist entscheidend.

## Schnelle Antworten
- **Was bedeutet “convert CAD to PDF”?** Transforming a CAD drawing (e.g., DXF, DWG) into a PDF document that can be viewed on any platform.  
- **Kann ich auch nach TIFF exportieren?** Yes—use `TiffOptions` to create high‑resolution raster images.  
- **Welche Option steuert die Canvas‑Größe in Java?** `CadRasterizationOptions.setPageWidth/Height`.  
- **Was ist automatische Layout‑Skalierung?** A flag (`setAutomaticLayoutsScaling(true)`) that preserves the original layout proportions when the canvas size changes.  
- **Benötige ich eine Lizenz für Aspose.CAD?** A temporary or permanent license is required for production use.

## Wie man die pdf page size beim Konvertieren von CAD zu PDF in Java festlegt

Laden Sie Ihre CAD‑Datei, konfigurieren Sie `CadRasterizationOptions` mit der gewünschten Breite und Höhe, aktivieren Sie die automatische Layout‑Skalierung und speichern Sie das Ergebnis anschließend als PDF. Dieser zweistufige Ansatz ermöglicht es Ihnen, die genauen Abmessungen der Ausgabeseite zu steuern, ohne die Vektorqualität zu beeinträchtigen.

## Was bedeutet convert CAD to PDF?

Das Konvertieren von CAD zu PDF bedeutet, vektorbasierte technische Zeichnungen zu nehmen und sie als PDF‑Seiten zu rendern, wobei Linien, Ebenen und Geometrie erhalten bleiben und die Datei universell zugänglich wird. Der Vorgang rastert die Zeichnung gemäß den angegebenen Optionen, erzeugt ein PDF, das auf jedem Gerät geöffnet werden kann, ohne dass CAD‑Software erforderlich ist, und bewahrt die visuelle Treue des Originaldesigns.

## Warum Canvas‑Größe in Java festlegen?

Das Festlegen der Canvas‑Größe in Java ermöglicht es Ihnen, die Ausgaberesolution und die Seitengröße zu definieren, sodass das resultierende PDF oder TIFF Ihren Druck‑ oder Anzeigeanforderungen entspricht. Es gibt Ihnen zudem die Kontrolle über das Skalierungsverhalten, was für großformatige Zeichnungen unerlässlich ist.

## Voraussetzungen

Bevor Sie in das Tutorial einsteigen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

- Aspose.CAD for Java: Stellen Sie sicher, dass die Aspose.CAD‑Bibliothek in Ihrer Java‑Umgebung installiert ist. Sie können die Aspose.CAD‑Bibliothek für Java [hier](https://releases.aspose.com/cad/java/) herunterladen.
- Dokumentverzeichnis: Richten Sie ein Dokumentverzeichnis ein, um Ihre CAD‑Dateien zu speichern. Dieses Verzeichnis wird in den Schritten des Tutorials referenziert.

Jetzt beginnen wir mit der Schritt‑für‑Schritt‑Anleitung.

## Namespaces importieren

In diesem Schritt importieren wir die erforderlichen Namespaces, um Ihr Aspose.CAD‑Projekt zu starten.

`Image` ist die Hauptklasse zum Laden von CAD‑Dateien.

```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## Schritt 1: Aspose.CAD‑Klassen importieren

Die Klasse `Image` bietet Methoden zum Laden und Speichern von CAD‑Zeichnungen.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

In diesem Snippet richten wir den Pfad zum Ressourcenverzeichnis ein und laden eine DXF‑Datei mit der `Image`‑Klasse von Aspose.CAD.

## Schritt 2: CadRasterizationOptions‑Eigenschaften festlegen (set canvas size java)

`CadRasterizationOptions` gibt Rasterisierungseinstellungen wie Seitengröße und Skalierung für die CAD‑zu‑Raster‑Konvertierung an.

```java
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

Hier erstellen wir eine Instanz von `CadRasterizationOptions` und konfigurieren Eigenschaften wie Seitenbreite, Seitenhöhe und **automatic layout scaling**. Dies ist das Kernstück von **configure canvas mode** für Ihre Konvertierung.

## Schritt 3: PdfOptions erstellen und vectorRasterizationOptions festlegen

`PdfOptions` definiert die PDF‑Ausgabeeinstellungen für die Konvertierung.

```java
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Set the VectorRasterizationOptions property
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Jetzt erstellen wir eine `PdfOptions`‑Instanz und setzen deren Eigenschaft `VectorRasterizationOptions` auf die zuvor konfigurierte `CadRasterizationOptions`.

## Schritt 4: Export nach PDF (convert CAD to PDF)

```java
// Export CAD to PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

Abschließend speichern wir das CAD‑Bild mit den angegebenen Optionen in einer PDF‑Datei und schließen damit den **convert CAD to PDF**‑Prozess ab.

## Schritt 5: TiffOptions erstellen und vectorRasterizationOptions festlegen (export CAD to TIFF)

`TiffOptions` konfiguriert TIFF‑Ausgabeparameter wie Kompression und Auflösung.

```java
// Create an instance of TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Set the VectorRasterizationOptions property
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Schritt 6: Export nach TIFF

```java
// Export CAD to TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

Abschließend speichern wir das CAD‑Bild mit den angegebenen Optionen in einer TIFF‑Datei und zeigen, wie man **export CAD to TIFF** nach der Konfiguration der Canvas‑Größe durchführt.

## Häufige Probleme und Lösungen

| Problem | Ursache | Lösung |
|-------|-------|-----|
| Ausgabe-PDF ist leer | `setNoScaling(true)` deaktiviert das Rendern für einige Zeichnungen | Entfernen Sie `setNoScaling(true)` oder setzen Sie es auf `false`. |
| TIFF-Auflösung wirkt niedrig | Seitenbreite/-höhe zu klein | Erhöhen Sie die Werte von `setPageWidth` / `setPageHeight`. |
| Layout wirkt verzerrt | Automatische Layout‑Skalierung deaktiviert | Stellen Sie sicher, dass `setAutomaticLayoutsScaling(true)` aktiviert ist. |

## Warum Canvas‑Größe und DPI anpassen?

Das Ändern der Canvas‑Größe beeinflusst direkt die Rasterisierungsauflösung der Ausgabe. Wenn Sie die **increase TIFF resolution** erhöhen müssen, erhöhen Sie einfach die Werte von `setPageWidth` / `setPageHeight` oder rufen Sie `rasterizationOptions.setResolution(300)` auf, bevor Sie die `TiffOptions` erstellen. Dadurch erhalten Sie hochwertige Rasterbilder, die für den Druck oder eine detaillierte Inspektion geeignet sind.

## Häufig gestellte Fragen

**Q1: Kann ich Aspose.CAD für Java mit anderen Java‑Frameworks verwenden?**  
A: Ja, Aspose.CAD ist so konzipiert, dass es nahtlos mit verschiedenen Java‑Frameworks integriert werden kann.

**Q2: Ist eine temporäre Lizenz für Aspose.CAD verfügbar?**  
A: Ja, Sie können eine temporäre Lizenzseite [hier](https://purchase.aspose.com/temporary-license/) erhalten.

**Q3: Wo kann ich Community‑Support für Aspose.CAD erhalten?**  
A: Besuchen Sie das Aspose.CAD‑Forum [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) für Community‑Support und Diskussionen.

**Q4: Kann ich Aspose.CAD kostenlos testen?**  
A: Absolut! Laden Sie die kostenlose Testversion [hier](https://releases.aspose.com/) herunter.

**Q5: Wie kaufe ich Aspose.CAD für Java?**  
A: Kaufen Sie Aspose.CAD für Java [hier](https://purchase.aspose.com/buy).

**Q: Beeinflusst die Canvas‑Größe die Vektorqualität im PDF?**  
A: Nein. Die Canvas‑Größe steuert die Seitengröße; Vektordaten bleiben auflösungsunabhängig und gewährleisten eine scharfe Darstellung bei jedem Zoom‑Level.

**Q: Kann ich für die TIFF‑Ausgabe ein anderes DPI festlegen?**  
A: Ja. Passen Sie `rasterizationOptions.setResolution(dpiValue)` an, bevor Sie `TiffOptions` erstellen.

**Q: Wie kann ich die PDF‑Abmessungen einer bestehenden PDF ändern, ohne das CAD neu zu rendern?**  
A: Verwenden Sie Aspose.PDF, um das erzeugte PDF zu laden und rufen Sie `pdf.getPages().setPageSize(PageSize.A4)` oder eine benutzerdefinierte Größe auf.

**Q: Was ist der beste Weg, DXF zu PDF zu konvertieren und dabei Ebenen zu erhalten?**  
A: Behalten Sie `setAutomaticLayoutsScaling(true)` bei und vermeiden Sie `setNoScaling(true)`; dies bewahrt die Ebenen‑Sichtbarkeit und die Layout‑Treue.

## Fazit

Herzlichen Glückwunsch! Sie haben erfolgreich **convert CAD to PDF** und **export CAD to TIFF** durchgeführt, während Sie **set canvas size java** verwendet haben, die **automatic layout scaling** aktiviert haben und gelernt haben, wie man **configure canvas mode** für hochwertige Ausgaben konfiguriert. Dieses Tutorial bietet eine solide Grundlage für Ihre CAD‑Konvertierungsprojekte. Erkunden Sie weitere Funktionen und Möglichkeiten in der [Aspose.CAD‑Dokumentation](https://reference.aspose.com/cad/java/).

---

**Zuletzt aktualisiert:** 2026-08-29  
**Getestet mit:** Aspose.CAD for Java 24.12  
**Autor:** Aspose

## Verwandte Tutorials

- [Canvas-Größe festlegen – Erweiterte CAD‑Funktionen mit Aspose.CAD für Java](/cad/java/advanced-cad-features/)
- [DWG nach PDF in Java exportieren – PDF‑Seitengröße festlegen mit Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)
- [Benutzerdefinierte Seitengröße festlegen – PDF aus CAD mit automatischer Layout‑Skalierung](/cad/java/advanced-cad-features/setting-auto-layout-scaling/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}