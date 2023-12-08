---
title: Müheloser DGN-zu-AutoCAD-PDF-Export mit Aspose.CAD für Java
linktitle: Exportieren von DGN im AutoCAD-Format in PDF
second_title: Aspose.CAD Java API
description: Entdecken Sie die Schritt-für-Schritt-Anleitung zum Exportieren von DGN-Dateien in das AutoCAD-Format im PDF-Format mit Aspose.CAD für Java. Erweitern Sie mühelos die CAD-Verarbeitungsmöglichkeiten Ihrer Java-Anwendung.
type: docs
weight: 12
url: /de/java/dgn-export-options/exporting-dgn-to-pdf/
---
## Einführung

Willkommen zu diesem umfassenden Tutorial zur Verwendung von Aspose.CAD für Java zum Exportieren von DGN-Dateien im AutoCAD-Format in PDF. Wenn Sie die Fähigkeit Ihrer Java-Anwendung zur Verarbeitung von CAD-Dateien verbessern möchten, ist Aspose.CAD eine ausgezeichnete Wahl. In diesem Tutorial führen wir Sie Schritt für Schritt durch den Prozess des Exportierens von DGN-Dateien.


## Voraussetzungen
Bevor wir uns mit dem Tutorial befassen, stellen Sie sicher, dass Sie die folgenden Voraussetzungen erfüllen:
-  Aspose.CAD-Bibliothek: Stellen Sie sicher, dass Sie die Aspose.CAD-Bibliothek für Java installiert haben. Sie können es herunterladen[Hier](https://releases.aspose.com/cad/java/).
- Dokumentenverzeichnis: Richten Sie ein Dokumentenverzeichnis ein, in dem Ihre Eingabe- und Ausgabedateien gespeichert werden.

## Pakete importieren

Importieren Sie in Ihrem Java-Projekt die erforderlichen Pakete, um auf die Aspose.CAD-Funktionen zuzugreifen:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Lassen Sie uns nun den Beispielcode in mehrere Schritte unterteilen:

## Schritt 1: Dateipfade definieren

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

Stellen Sie sicher, dass Sie „Ihr Dokumentenverzeichnis“ durch den tatsächlichen Pfad ersetzen, in dem sich Ihre Dateien befinden.

## Schritt 2: DGN-Bild laden

```java
DgnImage objImage = (DgnImage) Image.load(fileName);
```

Laden Sie die DGN-Datei mit Aspose.CAD.

## Schritt 3: PDF-Exportoptionen festlegen

```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); // Exportieren Sie bestimmte Ansichten
options.setVectorRasterizationOptions(vectorOptions);
```

Definieren Sie die PDF-Exportoptionen, einschließlich Seitenabmessungen und Layouteinstellungen.

## Schritt 4: PDF-Datei speichern

```java
objImage.save(outFile, options);
```

Speichern Sie die exportierte PDF-Datei.

Wiederholen Sie diese Schritte für alle weiteren DGN-Dateien, die Sie konvertieren möchten. Glückwunsch! Sie haben DGN-Dateien mit Aspose.CAD für Java erfolgreich in das AutoCAD-Format im PDF-Format exportiert.

## Abschluss

In diesem Tutorial haben wir untersucht, wie Sie Aspose.CAD für Java nutzen können, um die CAD-Dateiverarbeitungsfunktionen Ihrer Anwendung zu verbessern. Mit leicht verständlichen Schritten und Codebeispielen können Sie DGN-Dateien jetzt nahtlos in das AutoCAD-Format im PDF-Format exportieren.

## FAQs

### F1: Ist Aspose.CAD mit allen CAD-Dateiformaten kompatibel?

A1: Ja, Aspose.CAD unterstützt eine Vielzahl von CAD-Formaten und gewährleistet so Vielseitigkeit bei der Verarbeitung verschiedener Dateitypen.

### F2: Kann ich die PDF-Exporteinstellungen anpassen?

A2: Absolut. Wie im Tutorial gezeigt, können Sie Optionen wie Seitenabmessungen und Layouts an Ihre Anforderungen anpassen.

### F3: Wo finde ich zusätzliche Unterstützung oder Unterstützung?

 A3: Besuchen Sie die[Aspose.CAD-Forum](https://forum.aspose.com/c/cad/19) für Community-Unterstützung und Diskussionen.

### F4: Gibt es eine kostenlose Testversion?

 A4: Ja, Sie können auf die kostenlose Testversion zugreifen[Hier](https://releases.aspose.com/).

### F5: Wie kann ich eine temporäre Lizenz erhalten?

 A5: Besorgen Sie sich eine temporäre Lizenz[Hier](https://purchase.aspose.com/temporary-license/).