---
title: Legen Sie die Leinwandgröße und den Modus fest
linktitle: Legen Sie die Leinwandgröße und den Modus fest
second_title: Aspose.CAD Java API
description: Entdecken Sie die Leistungsfähigkeit von Aspose.CAD für Java mit unserer Schritt-für-Schritt-Anleitung zum Festlegen von Leinwandgröße und -modus. Konvertieren Sie CAD-Dateien mühelos in die Formate PDF und TIFF.
weight: 16
url: /de/java/advanced-cad-features/set-canvas-size-and-mode/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Legen Sie die Leinwandgröße und den Modus fest

## Einführung

Möchten Sie die Leistungsfähigkeit von Aspose.CAD für Java nutzen, um Ihren CAD-Konvertierungsprozess zu verbessern? Diese umfassende Anleitung führt Sie durch die Schritte zum Festlegen der Leinwandgröße und des Leinwandmodus mit Aspose.CAD für Java. Egal, ob Sie ein erfahrener Entwickler sind oder gerade erst anfangen, dieses Tutorial liefert Ihnen die Einblicke, die Sie brauchen.

## Voraussetzungen

Bevor Sie mit dem Tutorial beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

-  Aspose.CAD für Java: Stellen Sie sicher, dass die Aspose.CAD-Bibliothek in Ihrer Java-Umgebung installiert ist. Sie können es herunterladen[Hier](https://releases.aspose.com/cad/java/).

- Dokumentenverzeichnis: Richten Sie ein Dokumentenverzeichnis zum Speichern Ihrer CAD-Dateien ein. Auf dieses Verzeichnis wird in den Schritten des Tutorials verwiesen.

Beginnen wir nun mit der Schritt-für-Schritt-Anleitung.

## Namespaces importieren

In diesem Schritt importieren wir die erforderlichen Namespaces, um Ihr Aspose.CAD-Projekt zu starten.
```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## Schritt 1: Aspose.CAD-Klassen importieren

```java
// Der Pfad zum Ressourcenverzeichnis.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

 In diesem Snippet richten wir den Pfad zum Ressourcenverzeichnis ein und laden eine DXF-Datei mit Aspose.CAD`Image` Klasse.

## Schritt 2: Legen Sie die CadRasterizationOptions-Eigenschaften fest

```java
// Erstellen Sie eine Instanz von CadRasterizationOptions und legen Sie deren verschiedene Eigenschaften fest
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

 Hier erstellen wir eine Instanz von`CadRasterizationOptions` und konfigurieren Sie Eigenschaften wie Seitenbreite, Seitenhöhe und Skalierungsoptionen.

## Schritt 3: Erstellen Sie PdfOptions und legen Sie VectorRasterizationOptions fest

```java
// Erstellen Sie eine Instanz von PDFOptions
PdfOptions pdfOptions = new PdfOptions();

// Legen Sie die VectorRasterizationOptions-Eigenschaft fest
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

 Jetzt erstellen wir eine`PdfOptions` Instanz und legen Sie sie fest`VectorRasterizationOptions` Eigenschaft auf die zuvor konfigurierte`CadRasterizationOptions`.

## Schritt 4: Als PDF exportieren

```java
// Exportieren Sie CAD als PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

Abschließend speichern wir das CAD-Bild mit den angegebenen Optionen in einer PDF-Datei.

## Schritt 5: Erstellen Sie TiffOptions und legen Sie VectorRasterizationOptions fest

```java
// Erstellen Sie eine Instanz von TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Legen Sie die VectorRasterizationOptions-Eigenschaft fest
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

In diesem Schritt richten wir eine ein`TiffOptions` Instanz und konfigurieren Sie sie`VectorRasterizationOptions` Eigentum.

## Schritt 6: Als TIFF exportieren

```java
// Exportieren Sie CAD nach TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

Abschließend speichern wir das CAD-Bild mit den angegebenen Optionen in einer TIFF-Datei.

## Abschluss

 Glückwunsch! Sie haben die Leinwandgröße und den Leinwandmodus erfolgreich mit Aspose.CAD für Java festgelegt. Dieses Tutorial bietet eine solide Grundlage für Ihre CAD-Konvertierungsprojekte. Entdecken Sie weitere Funktionen und Möglichkeiten im[Aspose.CAD-Dokumentation](https://reference.aspose.com/cad/java/).

## FAQs

### F1: Kann ich Aspose.CAD für Java mit anderen Java-Frameworks verwenden?

A1: Ja, Aspose.CAD ist für die nahtlose Integration in verschiedene Java-Frameworks konzipiert.

### F2: Ist eine temporäre Lizenz für Aspose.CAD verfügbar?

 A2: Ja, Sie können eine temporäre Lizenz erhalten[Hier](https://purchase.aspose.com/temporary-license/).

### F3: Wo kann ich Community-Support für Aspose.CAD erhalten?

 A3: Besuchen Sie die[Aspose.CAD-Forum](https://forum.aspose.com/c/cad/19) für Community-Unterstützung und Diskussionen.

### F4: Kann ich Aspose.CAD kostenlos testen?

 A4: Auf jeden Fall! Holen Sie sich eine kostenlose Testversion[Hier](https://releases.aspose.com/).

### F5: Wie kaufe ich Aspose.CAD für Java?

 A5: Kaufen Sie das Produkt[Hier](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
