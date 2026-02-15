---
date: 2026-02-15
description: Erfahren Sie, wie Sie die PDF‑Seitengröße festlegen und CAD mit Aspose.CAD
  für Java in PDF konvertieren, einschließlich automatischer Layout‑Skalierung und
  TIFF‑Export.
linktitle: Set PDF Page Size – Convert CAD to PDF
second_title: Aspose.CAD Java API
title: PDF‑Seitengröße festlegen – CAD zu PDF konvertieren (Java)
url: /de/java/advanced-cad-features/set-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Canvas-Größe und Modus festlegen

## Einleitung

Wenn Sie die **PDF-Seitengröße** beim Konvertieren von CAD-Zeichnungen in PDF festlegen müssen, sind Sie hier genau richtig. In diesem Tutorial zeigen wir Ihnen, wie Sie Aspose.CAD für Java verwenden, um genaue Canvas‑Dimensionen zu definieren, die automatische Layout‑Skalierung zu aktivieren und das Ergebnis sowohl als PDF als auch als TIFF zu exportieren. Egal, ob Sie technische Schemata für den Druck vorbereiten oder Thumbnails für eine Webgalerie erzeugen, die Kontrolle über die Seitengröße und die Ausgaberesolution ist entscheidend.

## Schnelle Antworten
- **Was bedeutet „convert CAD to PDF“?** Umwandlung einer CAD‑Zeichnung (z. B. DXF, DWG) in ein PDF‑Dokument, das auf jeder Plattform angezeigt werden kann.  
- **Kann ich auch nach TIFF exportieren?** Ja – verwenden Sie `TiffOptions`, um hochauflösende Rasterbilder zu erstellen.  
- **Welche Option steuert die Canvas‑Größe in Java?** `CadRasterizationOptions.setPageWidth/Height`.  
- **Was ist automatische Layout‑Skalierung?** Ein Flag (`setAutomaticLayoutsScaling(true)`), das die ursprünglichen Layout‑Proportionen beibehält, wenn die Canvas‑Größe geändert wird.  
- **Benötige ich eine Lizenz für Aspose.CAD?** Für den Produktionseinsatz ist eine temporäre oder permanente Lizenz erforderlich.

## So legen Sie die PDF‑Seitengröße beim Konvertieren von CAD nach PDF (Java) fest

Das Festlegen der PDF‑Seitengröße (oder Canvas‑Größe) ermöglicht es Ihnen, die endgültigen Abmessungen des Dokuments zu bestimmen, was besonders nützlich ist, wenn Sie **PDF‑Dimensionen** an Druckstandards oder UI‑Anforderungen anpassen müssen. Im Folgenden gehen wir jeden Schritt durch und erklären das *Warum* hinter jeder Codezeile.

## Was ist **convert CAD to PDF**?

Das Konvertieren von CAD zu PDF bedeutet, vektorbasierten technischen Zeichnungen zu nehmen und sie als PDF‑Seiten zu rendern, wobei Linien, Ebenen und Geometrie erhalten bleiben und die Datei universell zugänglich wird.

## Warum die Canvas‑Größe in **Java** festlegen?

Das Festlegen der Canvas‑Größe in Java ermöglicht es Ihnen, die Ausgaberesolution und Seitenabmessungen zu definieren, sodass das resultierende PDF oder TIFF Ihren Druck‑ oder Anzeigeanforderungen entspricht. Außerdem erhalten Sie Kontrolle über das Skalierungsverhalten, was für großformatige Zeichnungen unerlässlich ist.

## Voraussetzungen

Bevor Sie in das Tutorial einsteigen, stellen Sie sicher, dass Sie die folgenden Voraussetzungen erfüllt haben:

- Aspose.CAD für Java: Stellen Sie sicher, dass die Aspose.CAD‑Bibliothek in Ihrer Java‑Umgebung installiert ist. Sie können sie [hier](https://releases.aspose.com/cad/java/) herunterladen.
- Dokumentverzeichnis: Richten Sie ein Verzeichnis ein, um Ihre CAD‑Dateien zu speichern. Dieses Verzeichnis wird in den Tutorial‑Schritten referenziert.

Jetzt beginnen wir mit der Schritt‑für‑Schritt‑Anleitung.

## Namespaces importieren

In diesem Schritt importieren wir die notwendigen Namespaces, um Ihr Aspose.CAD‑Projekt zu starten.

```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## Schritt 1: Aspose.CAD‑Klassen importieren

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

In diesem Snippet richten wir den Pfad zum Ressourcenverzeichnis ein und laden eine DXF‑Datei mit der `Image`‑Klasse von Aspose.CAD.

## Schritt 2: **CadRasterizationOptions**‑Eigenschaften festlegen (set canvas size java)

```java
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

Hier erstellen wir eine Instanz von `CadRasterizationOptions` und konfigurieren Eigenschaften wie Seitenbreite, Seitenhöhe und **automatische Layout‑Skalierung**. Dies ist der Kern von **configure canvas mode** für Ihre Konvertierung.

## Schritt 3: PdfOptions erstellen und VectorRasterizationOptions festlegen

```java
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Set the VectorRasterizationOptions property
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Jetzt erstellen wir eine Instanz von `PdfOptions` und setzen deren Eigenschaft `VectorRasterizationOptions` auf die zuvor konfigurierte `CadRasterizationOptions`.

## Schritt 4: Export nach PDF (convert cad to pdf)

```java
// Export CAD to PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

Abschließend speichern wir das CAD‑Bild mit den angegebenen Optionen in einer PDF‑Datei und schließen damit den **convert CAD to PDF**‑Prozess ab.

## Schritt 5: TiffOptions erstellen und VectorRasterizationOptions festlegen (export cad to tiff)

```java
// Create an instance of TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Set the VectorRasterizationOptions property
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

In diesem Schritt richten wir eine Instanz von `TiffOptions` ein und konfigurieren deren Eigenschaft `VectorRasterizationOptions`.

## Schritt 6: Export nach TIFF

```java
// Export CAD to TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

Abschließend speichern wir das CAD‑Bild mit den angegebenen Optionen in einer TIFF‑Datei und demonstrieren, wie man **CAD nach TIFF exportiert** nach der Konfiguration der Canvas‑Größe.

## Häufige Probleme und Lösungen

| Problem | Ursache | Lösung |
|---------|---------|--------|
| Ausgabe-PDF ist leer | `setNoScaling(true)` deaktiviert das Rendern bei einigen Zeichnungen | Entfernen Sie `setNoScaling(true)` oder setzen Sie es auf `false`. |
| TIFF-Auflösung ist niedrig | Seitenbreite/-höhe zu klein | Erhöhen Sie die Werte von `setPageWidth` / `setPageHeight`. |
| Layout sieht verzerrt aus | Automatische Layout‑Skalierung deaktiviert | Stellen Sie sicher, dass `setAutomaticLayoutsScaling(true)` aktiviert ist. |

## Warum Canvas‑Größe und DPI anpassen?

Das Ändern der Canvas‑Größe beeinflusst direkt die Rasterisierungsauflösung der Ausgabe. Wenn Sie die **TIFF‑Auflösung erhöhen** müssen, erhöhen Sie einfach die Werte von `setPageWidth` / `setPageHeight` oder rufen Sie `rasterizationOptions.setResolution(300)` auf, bevor Sie die `TiffOptions` erstellen. Dadurch erhalten Sie hochqualitative Rasterbilder, die für den Druck oder die detaillierte Inspektion geeignet sind.

## Häufig gestellte Fragen

### Q1: Kann ich Aspose.CAD für Java mit anderen Java‑Frameworks verwenden?

A1: Ja, Aspose.CAD ist so konzipiert, dass es nahtlos mit verschiedenen Java‑Frameworks integriert werden kann.

### Q2: Ist eine temporäre Lizenz für Aspose.CAD verfügbar?

A2: Ja, Sie können eine temporäre Lizenz [hier](https://purchase.aspose.com/temporary-license/) erhalten.

### Q3: Wo kann ich Community‑Support für Aspose.CAD erhalten?

A3: Besuchen Sie das [Aspose.CAD‑Forum](https://forum.aspose.com/c/cad/19) für Community‑Support und Diskussionen.

### Q4: Kann ich Aspose.CAD kostenlos testen?

A4: Natürlich! Holen Sie sich eine kostenlose Testversion [hier](https://releases.aspose.com/).

### Q5: Wie kaufe ich Aspose.CAD für Java?

A5: Kaufen Sie das Produkt [hier](https://purchase.aspose.com/buy).

**Zusätzliche Fragen & Antworten**

**Q: Beeinflusst die Canvas‑Größe die Vektorqualität im PDF?**  
A: Nein. Die Canvas‑Größe steuert die Seitenabmessungen; Vektordaten bleiben auflösungsunabhängig, wodurch eine scharfe Darstellung bei jeder Zoomstufe gewährleistet ist.

**Q: Kann ich für die TIFF‑Ausgabe eine andere DPI einstellen?**  
A: Ja. Passen Sie `rasterizationOptions.setResolution(dpiValue)` an, bevor Sie `TiffOptions` erstellen.

**Q: Wie kann ich **PDF-Dimensionen** für ein bestehendes PDF ändern, ohne das CAD neu zu rendern?**  
A: Verwenden Sie Aspose.PDF, um das erzeugte PDF zu laden, und rufen Sie `pdf.getPages().setPageSize(PageSize.A4)` oder eine benutzerdefinierte Größe auf.

**Q: Was ist der beste Weg, **dxf nach pdf** zu konvertieren und dabei Ebenen zu erhalten?**  
A: Behalten Sie `setAutomaticLayoutsScaling(true)` bei und vermeiden Sie `setNoScaling(true)`; dadurch bleiben die Ebenen sichtbar und das Layout erhalten.

## Fazit

Herzlichen Glückwunsch! Sie haben erfolgreich **CAD zu PDF konvertiert** und **CAD nach TIFF exportiert**, während Sie **set canvas size java** verwendet haben, die **automatische Layout‑Skalierung** aktiviert haben und gelernt haben, wie man **canvas mode konfiguriert** für hochwertige Ausgaben. Dieses Tutorial bietet eine solide Grundlage für Ihre CAD‑Konvertierungsprojekte. Erkunden Sie weitere Funktionen und Möglichkeiten in der [Aspose.CAD‑Dokumentation](https://reference.aspose.com/cad/java/).

---

**Zuletzt aktualisiert:** 2026-02-15  
**Getestet mit:** Aspose.CAD für Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}