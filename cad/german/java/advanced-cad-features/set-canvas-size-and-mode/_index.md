---
date: 2025-12-10
description: Erfahren Sie, wie Sie CAD mit Aspose.CAD für Java in PDF konvertieren,
  dabei die Canvas‑Größe festlegen, die automatische Layout‑Skalierung verwenden und
  in TIFF exportieren.
linktitle: Convert CAD to PDF – Set Canvas Size & Mode
second_title: Aspose.CAD Java API
title: CAD in PDF konvertieren – Canvas‑Größe und Modus festlegen (Java)
url: /de/java/advanced-cad-features/set-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Canvasgröße und Modus festlegen

## Einleitung

Suchen Sie nach einer Möglichkeit, **CAD in PDF zu konvertieren**, während Sie die volle Kontrolle über die Canvasgröße und den Rendering‑Modus behalten? Dieser umfassende Leitfaden führt Sie Schritt für Schritt durch das Festlegen der Canvasgröße in Java, das Aktivieren der automatischen Layout‑Skalierung und das anschließende Exportieren des Ergebnisses sowohl in PDF‑ als auch in TIFF‑Formate mit Aspose.CAD. Egal, ob Sie eine Produktionspipeline verfeinern oder mit einem Prototyp experimentieren, hier finden Sie klare, umsetzbare Anweisungen.

## Schnelle Antworten
- **Was bedeutet “convert CAD to PDF”?** Umwandlung einer CAD‑Zeichnung (z. B. DXF, DWG) in ein PDF‑Dokument, das auf jeder Plattform angezeigt werden kann.  
- **Kann ich auch nach TIFF exportieren?** Ja – verwenden Sie `TiffOptions`, um hochauflösende Rasterbilder zu erstellen.  
- **Welche Option steuert die Canvasgröße in Java?** `CadRasterizationOptions.setPageWidth/Height`.  
- **Was ist automatische Layout‑Skalierung?** Ein Flag (`setAutomaticLayoutsScaling(true)`), das die ursprünglichen Layout‑Proportionen beibehält, wenn die Canvasgröße geändert wird.  
- **Benötige ich eine Lizenz für Aspose.CAD?** Für den Produktionseinsatz ist eine temporäre oder permanente Lizenz erforderlich.

## Was ist **convert CAD to PDF**?

Das Konvertieren von CAD zu PDF bedeutet, vektorbasierten Konstruktionszeichnungen zu nehmen und sie als PDF‑Seiten zu rendern, wobei Linienarbeit, Ebenen und Geometrie erhalten bleiben und die Datei universell zugänglich wird.

## Warum die Canvasgröße in **java** festlegen?

Das Festlegen der Canvasgröße in Java ermöglicht es Ihnen, die Ausgabeauflösung und die Seitengröße zu definieren, sodass das resultierende PDF oder TIFF Ihren Druck‑ oder Anzeigeanforderungen entspricht. Es gibt Ihnen zudem die Kontrolle über das Skalierungsverhalten, was für großformatige Zeichnungen unerlässlich ist.

## Voraussetzungen

Bevor Sie in das Tutorial eintauchen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

- Aspose.CAD für Java: Stellen Sie sicher, dass die Aspose.CAD‑Bibliothek in Ihrer Java‑Umgebung installiert ist. Sie können sie [hier](https://releases.aspose.com/cad/java/) herunterladen.
- Dokumentverzeichnis: Richten Sie ein Verzeichnis ein, um Ihre CAD‑Dateien zu speichern. Dieses Verzeichnis wird in den Schritten des Tutorials referenziert.

Jetzt beginnen wir mit der Schritt‑für‑Schritt‑Anleitung.

## Namespaces importieren

In diesem Schritt importieren wir die erforderlichen Namespaces, um Ihr Aspose.CAD‑Projekt zu starten.

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

Hier erstellen wir eine Instanz von `CadRasterizationOptions` und konfigurieren Eigenschaften wie Seitenbreite, Seitenhöhe und **automatic layout scaling**. Dies ist der Kern von **configure canvas mode** für Ihre Konvertierung.

```java
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

## Schritt 3: PdfOptions erstellen und VectorRasterizationOptions festlegen

Jetzt erstellen wir eine `PdfOptions`‑Instanz und setzen deren `VectorRasterizationOptions`‑Eigenschaft auf die zuvor konfigurierte `CadRasterizationOptions`.

```java
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Set the VectorRasterizationOptions property
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Schritt 4: Export nach PDF (convert cad to pdf)

Abschließend speichern wir das CAD‑Bild mit den angegebenen Optionen in einer PDF‑Datei und schließen damit den **convert CAD to PDF**‑Prozess ab.

```java
// Export CAD to PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

## Schritt 5: TiffOptions erstellen und VectorRasterizationOptions festlegen (export cad to tiff)

In diesem Schritt richten wir eine `TiffOptions`‑Instanz ein und konfigurieren deren `VectorRasterizationOptions`‑Eigenschaft.

```java
// Create an instance of TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Set the VectorRasterizationOptions property
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Schritt 6: Export nach TIFF

Abschließend speichern wir das CAD‑Bild mit den angegebenen Optionen in einer TIFF‑Datei und zeigen, wie man **export CAD to TIFF** nach dem Konfigurieren der Canvasgröße durchführt.

```java
// Export CAD to TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

## Häufige Probleme und Lösungen

| Problem | Ursache | Lösung |
|-------|-------|-----|
| Ausgabe-PDF ist leer | `setNoScaling(true)` deaktiviert das Rendering für einige Zeichnungen | Entfernen Sie `setNoScaling(true)` oder setzen Sie es auf `false`. |
| TIFF-Auflösung wirkt niedrig | Seitenbreite/-höhe zu klein | Erhöhen Sie die Werte von `setPageWidth` / `setPageHeight`. |
| Layout sieht verzerrt aus | Automatische Layout‑Skalierung deaktiviert | Stellen Sie sicher, dass `setAutomaticLayoutsScaling(true)` aktiviert ist. |

## Fazit

Herzlichen Glückwunsch! Sie haben erfolgreich **convert CAD to PDF** und **export CAD to TIFF** durchgeführt, während Sie **set canvas size java** verwendet haben, **automatic layout scaling** aktiviert haben und gelernt haben, wie man **configure canvas mode** für hochwertige Ausgaben einstellt. Dieses Tutorial bietet eine solide Grundlage für Ihre CAD‑Konvertierungsprojekte. Erkunden Sie weitere Funktionen und Möglichkeiten in der [Aspose.CAD‑Dokumentation](https://reference.aspose.com/cad/java/).

## FAQ

### Q1: Kann ich Aspose.CAD für Java mit anderen Java‑Frameworks verwenden?

A1: Ja, Aspose.CAD ist so konzipiert, dass es sich nahtlos in verschiedene Java‑Frameworks integrieren lässt.

### Q2: Ist eine temporäre Lizenz für Aspose.CAD verfügbar?

A2: Ja, Sie können eine temporäre Lizenz [hier](https://purchase.aspose.com/temporary-license/) erhalten.

### Q3: Wo kann ich Community‑Support für Aspose.CAD erhalten?

A3: Besuchen Sie das [Aspose.CAD‑Forum](https://forum.aspose.com/c/cad/19) für Community‑Support und Diskussionen.

### Q4: Kann ich Aspose.CAD kostenlos testen?

A4: Auf jeden Fall! Holen Sie sich eine kostenlose Testversion [hier](https://releases.aspose.com/).

### Q5: Wie kaufe ich Aspose.CAD für Java?

A5: Kaufen Sie das Produkt [hier](https://purchase.aspose.com/buy).

**Zusätzliche Q&A**

**Q: Beeinflusst die Canvasgröße die Vektorqualität im PDF?**  
A: Nein. Die Canvasgröße steuert die Seitengröße; Vektordaten bleiben auflösungsunabhängig, wodurch eine klare Darstellung bei jedem Zoom‑Level gewährleistet ist.

**Q: Kann ich für die TIFF‑Ausgabe eine andere DPI einstellen?**  
A: Ja. Passen Sie `rasterizationOptions.setResolution(dpiValue)` an, bevor Sie `TiffOptions` erstellen.

---

**Zuletzt aktualisiert:** 2025-12-10  
**Getestet mit:** Aspose.CAD for Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}