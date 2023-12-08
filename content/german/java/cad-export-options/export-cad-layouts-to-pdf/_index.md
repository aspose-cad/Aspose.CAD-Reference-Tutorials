---
title: Exportieren Sie CAD-Layouts mit Aspose.CAD für Java in PDF
linktitle: Exportieren Sie CAD-Layouts als PDF
second_title: Aspose.CAD Java API
description: Entdecken Sie Aspose.CAD für Java, um CAD-Layouts mühelos in PDF zu exportieren. Effizient, zuverlässig und entwicklerfreundlich.
type: docs
weight: 11
url: /de/java/cad-export-options/export-cad-layouts-to-pdf/
---
## Einführung

Im sich ständig weiterentwickelnden Bereich des computergestützten Designs (CAD) zeichnet sich Aspose.CAD für Java als leistungsstarkes Tool zum Bearbeiten und Konvertieren von CAD-Dateien aus. In diesem Tutorial führen wir Sie durch den Prozess des Exportierens von CAD-Layouts in PDF mit Aspose.CAD für Java. Egal, ob Sie ein erfahrener Entwickler sind oder gerade erst in die Welt des CAD eintauchen, diese Schritt-für-Schritt-Anleitung hilft Ihnen dabei, das volle Potenzial dieser vielseitigen Java-Bibliothek auszuschöpfen.

## Voraussetzungen

Bevor wir uns mit dem Tutorial befassen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

-  Aspose.CAD für Java: Stellen Sie sicher, dass Sie die Bibliothek installiert haben. Sie können es von der Aspose-Website herunterladen[Hier](https://releases.aspose.com/cad/java/).

- Java-Entwicklungsumgebung: Stellen Sie sicher, dass auf Ihrem Computer eine Java-Entwicklungsumgebung eingerichtet ist.

Nachdem Sie nun alles eingerichtet haben, beginnen wir mit dem Tutorial.

## Namespaces importieren

Beginnen Sie in Ihrem Java-Code mit dem Importieren der erforderlichen Namespaces. Diese Importe bieten Zugriff auf die Klassen und Methoden, die für die Arbeit mit Aspose.CAD für Java erforderlich sind.

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterpolationMode;
import com.aspose.cad.SmoothingMode;
import com.aspose.cad.TextRenderingHint;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

## Schritt 1: Laden Sie die CAD-Datei

 Laden Sie zunächst die CAD-Datei mit in Ihre Java-Anwendung`Image.load` Methode. Ersetzen`"conic_pyramid.dxf"` mit dem Pfad zu Ihrer CAD-Datei.

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

## Schritt 2: Rasterisierungsoptionen festlegen

 Erstellen Sie eine Instanz von`CadRasterizationOptions` um zu definieren, wie die CAD-Elemente gerastert werden sollen. Passen Sie Parameter wie Seitenbreite, Seitenhöhe und Layoutskalierung entsprechend Ihren Anforderungen an.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(false);
rasterizationOptions.setContentAsBitmap(true);
rasterizationOptions.setLayouts(new String[]{"Model"});
```

## Schritt 3: PDF-Optionen festlegen

 Erstellen Sie eine Instanz von`PdfOptions` und verknüpfen Sie es mit den Rasterisierungsoptionen. Legen Sie außerdem Grafikoptionen für den PDF-Export fest, z. B. den Glättungsmodus, den Textwiedergabehinweis und den Interpolationsmodus.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.getGraphicsOptions().setSmoothingMode(SmoothingMode.HighQuality);
rasterizationOptions.getGraphicsOptions().setTextRenderingHint(TextRenderingHint.AntiAliasGridFit);
rasterizationOptions.getGraphicsOptions().setInterpolationMode(InterpolationMode.HighQualityBicubic);
```

## Schritt 4: Als PDF exportieren

 Exportieren Sie abschließend die CAD-Layouts mit in eine PDF-Datei`save` Methode der`cadImage` Objekt.

```java
cadImage.save(dataDir + "CADLayoutsToPDF_out_.pdf", pdfOptions);
```

Glückwunsch! Sie haben CAD-Layouts mit Aspose.CAD für Java erfolgreich in PDF exportiert. Erkunden Sie gerne die zusätzlichen Features und Funktionen von Aspose.CAD, um Ihr Erlebnis bei der Bearbeitung von CAD-Dateien zu verbessern.

## Abschluss

In diesem Tutorial haben wir den Prozess des Exportierens von CAD-Layouts in PDF mit Aspose.CAD für Java durchlaufen. Mit seinen robusten Funktionen und der benutzerfreundlichen API ermöglicht Aspose.CAD Entwicklern die effiziente Arbeit mit CAD-Dateien in ihren Java-Anwendungen.

## FAQs

### F1: Kann ich Aspose.CAD für Java mit anderen CAD-Dateiformaten verwenden?

 A1: Ja, Aspose.CAD unterstützt verschiedene CAD-Formate, einschließlich DWG, DXF, DWF und mehr. Überprüfen Sie die Dokumentation[Hier](https://reference.aspose.com/cad/java/) für eine vollständige Liste.

### F2: Gibt es eine kostenlose Testversion für Aspose.CAD für Java?

 A2: Ja, Sie können die Funktionen von Aspose.CAD mit einer kostenlosen Testversion erkunden[Hier](https://releases.aspose.com/).

### F3: Wie erhalte ich Unterstützung für Aspose.CAD für Java?

 A3: Besuchen Sie das Aspose.CAD-Forum[Hier](https://forum.aspose.com/c/cad/19) für die Unterstützung der Gemeinschaft. Für Premium-Support sollten Sie den Kauf einer Lizenz in Betracht ziehen[Hier](https://purchase.aspose.com/buy).

### F4: Was ist der Unterschied zwischen automatischer und manueller Layout-Skalierung?

A4: Die automatische Layoutskalierung passt die Layoutgröße basierend auf den angegebenen Seitenabmessungen an, während Sie bei der manuellen Skalierung benutzerdefinierte Skalierungswerte festlegen können.

### F5: Kann ich das Erscheinungsbild exportierter PDF-Dateien anpassen?

A5: Ja, Sie können die Grafikoptionen im Code anpassen, um die Qualität und das Erscheinungsbild der exportierten PDF-Datei zu steuern.