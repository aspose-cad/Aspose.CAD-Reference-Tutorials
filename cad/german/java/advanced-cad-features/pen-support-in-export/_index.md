---
title: Stiftunterstützung beim Export
linktitle: Stiftunterstützung beim Export
second_title: Aspose.CAD Java API
description: Master-Stiftanpassung im CAD-Export mit Aspose.CAD für Java. Befolgen Sie unsere Schritt-für-Schritt-Anleitung für eine nahtlose Integration.
weight: 13
url: /de/java/advanced-cad-features/pen-support-in-export/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Stiftunterstützung beim Export

## Einführung

In der sich ständig weiterentwickelnden Landschaft der CAD-Konvertierungen (Computer-Aided Design) erweist sich Aspose.CAD für Java als leistungsstarkes Tool, das umfangreiche Funktionen zur Bearbeitung von CAD-Dateien bietet. Unter den vielseitigen Funktionen sticht die Unterstützung der Stiftanpassung während des Exports hervor, sodass Benutzer das Erscheinungsbild exportierter Bilder individuell anpassen können. Dieses Tutorial führt Sie durch den Prozess der Nutzung der Stiftunterstützung in der Exportfunktionalität und konzentriert sich dabei auf die praktische Implementierung mit Java.

## Voraussetzungen

Bevor Sie sich mit dem Tutorial befassen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

- Java-Entwicklungsumgebung: Stellen Sie sicher, dass auf Ihrem Computer eine funktionsfähige Java-Entwicklungsumgebung eingerichtet ist.

-  Aspose.CAD-Bibliothek: Laden Sie die Aspose.CAD-Bibliothek herunter und integrieren Sie sie in Ihr Java-Projekt. Sie finden die Bibliothek[Hier](https://releases.aspose.com/cad/java/).

Lassen Sie uns nun mit dem Tutorial beginnen und die Schritte zur Nutzung der Stiftunterstützung während des CAD-Exports erkunden.

## Namespaces importieren

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.PenOptions;
import com.aspose.cad.internal.imaging.LineCap;
```

## Schritt 1: Definieren Sie Ihr Dokumentenverzeichnis

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

Stellen Sie sicher, dass Sie „Ihr Dokumentverzeichnis“ durch den tatsächlichen Pfad zu Ihren CAD-Dokumenten ersetzen.

## Schritt 2: Laden Sie die CAD-Datei

```java
String srcFile = dataDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage) Image.load(srcFile);
```

Dieser Schritt umfasst das Laden der CAD-Datei, in diesem Fall „conic_pyramid.dxf“, mithilfe der Aspose.CAD-Bibliothek.

## Schritt 3: Rasterisierungsoptionen konfigurieren

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(cadImage.getWidth() * 100);
rasterizationOptions.setPageHeight(cadImage.getHeight() * 100);
```

Passen Sie die Seitenbreite und -höhe entsprechend Ihren spezifischen Anforderungen an. Diese Werte bestimmen die Abmessungen des exportierten Bildes.

## Schritt 4: Passen Sie die Stiftoptionen an

```java
PenOptions penOts = new PenOptions();
penOts.setStartCap(LineCap.Flat);
penOts.setEndCap(LineCap.Flat);
```

Passen Sie die Anfangs- und Endkappen der Stifte nach Bedarf an. Diese Anpassung gilt beim Exportieren des CadImage-Objekts in verschiedene Bildformate.

## Schritt 5: PDF-Exportoptionen konfigurieren

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Geben Sie die Vektor-Rasterisierungsoptionen an, einschließlich der zuvor konfigurierten Rasterisierungsoptionen.

## Schritt 6: Speichern Sie das exportierte PDF

```java
cadImage.save((dataDir + "9LHATT-A56_generated.pdf"), pdfOptions);
```

Speichern Sie die exportierte PDF-Datei mit dem angegebenen Dateinamen (in diesem Beispiel „9LHATT-A56_generated.pdf“) und den konfigurierten Optionen.

## Abschluss

Zusammenfassend lässt sich sagen, dass Benutzer durch die Nutzung der Stiftunterstützung während des CAD-Exports mit Aspose.CAD für Java das Erscheinungsbild exportierter Bilder individuell anpassen können. Durch Befolgen dieser Schritt-für-Schritt-Anleitung haben Sie gelernt, wie Sie die Stiftanpassung nahtlos in Ihren CAD-Konvertierungsworkflow integrieren können.

## FAQs

### F1: Kann ich die Stiftoptionen für andere Formate als PDF anpassen?

A1: Ja, die in diesem Tutorial gezeigte Stiftanpassung ist auf verschiedene Bildformate anwendbar, darunter PDF, PNG, BMP, GIF, JPEG2000, JPEG, PSD, TIFF und WMF.

### F2: Wie kann ich mit unterschiedlichen Anfangs- und Endkappen für Stifte umgehen?

 A2: Nutzen Sie die`PenOptions` -Klasse zum Festlegen der gewünschten Start- und Endkappen und bietet so Flexibilität bei der Definition des Erscheinungsbilds von Linien.

### F3: Was passiert, wenn ich keine Stiftoptionen spezifiziere?

A3: Wenn Stiftoptionen nicht explizit festgelegt sind, verwendet das System seine Standardstifte, die je nach Kontext variieren können.

### F4: Gibt es spezielle Überlegungen zu Rasterisierungsoptionen?

A4: Passen Sie die Seitenbreite und -höhe in den Rasterungsoptionen an, um die Abmessungen des exportierten Bildes zu steuern.

### F5: Wo finde ich zusätzlichen Support oder Community-Diskussionen?

 A5: Entdecken Sie das Aspose.CAD-Community-Forum unter[Hier](https://forum.aspose.com/c/cad/19) für Unterstützung und Diskussionen.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
