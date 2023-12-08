---
title: Erstellen dynamischer PDFs mit Aspose.CAD für Java
linktitle: Einzelnes PDF mit verschiedenen Layouts
second_title: Aspose.CAD Java API
description: Erstellen Sie mit Aspose.CAD für Java beeindruckende PDFs mit verschiedenen Layouts aus CAD-Zeichnungen. Einfache Integration und leistungsstarke Funktionen für Java-Entwickler.
type: docs
weight: 16
url: /de/java/other-cad-operations/single-pdf-different-layouts/
---
## Einführung

Willkommen in der Welt von Aspose.CAD für Java, einer leistungsstarken Bibliothek, die Entwicklern die mühelose Bearbeitung von CAD-Zeichnungen ermöglicht. In diesem Tutorial befassen wir uns mit der Erstellung einzelner PDFs mit unterschiedlichen Layouts mit Aspose.CAD für Java. Egal, ob Sie ein erfahrener Entwickler sind oder gerade erst anfangen, diese Schritt-für-Schritt-Anleitung führt Sie durch den Prozess.

## Voraussetzungen

Bevor wir uns auf diese Reise begeben, stellen Sie sicher, dass Sie über die folgenden Voraussetzungen verfügen:
- Java-Umgebung: Stellen Sie sicher, dass Java auf Ihrem Computer installiert ist.
-  Aspose.CAD-Bibliothek: Laden Sie die Aspose.CAD-Bibliothek für Java von herunter und installieren Sie sie[Download-Link](https://releases.aspose.com/cad/java/).
- Dokumentverzeichnis: Richten Sie ein Verzeichnis für Ihre DWG-Zeichnungen ein.

## Pakete importieren

Importieren Sie in Ihrem Java-Projekt die erforderlichen Pakete:

```java
import com.aspose.cad.Image;
import com.aspose.cad.SizeF;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.VectorRasterizationOptions;
```

## Schritt 1: CAD-Zeichnung laden

 Laden Sie zunächst Ihre CAD-Zeichnung in ein`CadImage` Objekt:

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
CadImage cadImage = (CadImage)Image.load(dataDir + "City skyway map.dwg");
```

## Schritt 2: Rasterisierungsoptionen konfigurieren

Richten Sie die Rasterungsoptionen für das CAD-Bild ein:

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1000);
rasterizationOptions.setPageHeight(1000);
```

## Schritt 3: Passen Sie die Seitengrößen des Layouts an

Definieren Sie benutzerdefinierte Größen für mehrere Layouts innerhalb der CAD-Zeichnung:

```java
rasterizationOptions.getLayoutPageSizes().addItem("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.getLayoutPageSizes().addItem("8.5 x 11 Plot", new SizeF(1000, 100));
```

## Schritt 4: PDF-Optionen festlegen

Konfigurieren Sie PDF-Optionen unter Einbeziehung der Rasterungseinstellungen:

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Schritt 5: Als PDF speichern

Speichern Sie das bearbeitete CAD-Bild als PDF:

```java
cadImage.save(dataDir + "singlePDF_out.pdf", pdfOptions);
```

Glückwunsch! Sie haben mit Aspose.CAD für Java erfolgreich ein einzelnes PDF mit verschiedenen Layouts erstellt.

## Abschluss

In diesem Tutorial haben wir die nahtlose Integration von Aspose.CAD für Java untersucht, um PDFs mit verschiedenen Layouts aus CAD-Zeichnungen zu generieren. Die Flexibilität und die robusten Funktionen der Bibliothek machen sie zur ersten Wahl für CAD-Manipulationsaufgaben.

## FAQs

### F1: Kann ich Aspose.CAD für Java mit anderen Java-Bibliotheken verwenden?

A1: Ja, Aspose.CAD für Java ist für die nahtlose Integration mit anderen Java-Bibliotheken konzipiert und bietet umfassende Funktionalität.

### F2: Gibt es eine Testversion?

 A2: Auf jeden Fall! Sie können auf eine kostenlose Testversion zugreifen[Hier](https://releases.aspose.com/).

### F3: Wo finde ich zusätzliche Unterstützung?

 A3: Besuchen Sie die[Aspose.CAD-Forum](https://forum.aspose.com/c/cad/19) für Community-Unterstützung und Diskussionen.

### F4: Wie erhalte ich eine temporäre Lizenz?

 A4: Sie können eine temporäre Lizenz erhalten[Hier](https://purchase.aspose.com/temporary-license/).

### F5: Wo kann ich die Vollversion kaufen?

A5: Kaufen Sie die Vollversion von Aspose.CAD für Java[Hier](https://purchase.aspose.com/buy).