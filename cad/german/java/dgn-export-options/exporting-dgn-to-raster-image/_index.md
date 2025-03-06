---
title: Java DGN in JPEG-Konvertierung mit Aspose.CAD-Tutorial
linktitle: Exportieren von DGN im AutoCAD-Format in das Rasterbildformat
second_title: Aspose.CAD Java API
description: Erfahren Sie, wie Sie DGN-Dateien mit Aspose.CAD in Java in JPEG-Bilder exportieren. Dieses Schritt-für-Schritt-Tutorial führt Sie mühelos durch den Prozess.
weight: 13
url: /de/java/dgn-export-options/exporting-dgn-to-raster-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java DGN in JPEG-Konvertierung mit Aspose.CAD-Tutorial

## Einführung

Willkommen zu diesem umfassenden Tutorial zum Exportieren von DGN-Dateien (Design) in das Rasterbildformat mit Aspose.CAD für Java. Aspose.CAD ist eine leistungsstarke Bibliothek, die Java-Entwicklern die nahtlose Arbeit mit CAD-Dateien ermöglicht. In diesem Tutorial führen wir Sie durch den Prozess der Konvertierung von DGN-Dateien in JPEG-Bilder und stellen Ihnen Schritt-für-Schritt-Anleitungen und Codebeispiele zur Verfügung.

## Voraussetzungen

Bevor Sie mit dem Tutorial beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:
1.  Aspose.CAD-Bibliothek: Stellen Sie sicher, dass Sie die Aspose.CAD für Java-Bibliothek installiert haben. Sie können es herunterladen[Hier](https://releases.aspose.com/cad/java/).
2. Java Development Kit (JDK): Stellen Sie sicher, dass Java auf Ihrem Computer installiert ist.
3. Integrierte Entwicklungsumgebung (IDE): Verwenden Sie eine Java-kompatible IDE wie IntelliJ oder Eclipse.

## Pakete importieren

Importieren Sie in Ihrem Java-Projekt die erforderlichen Pakete für Aspose.CAD. Fügen Sie Ihrem Code die folgenden Zeilen hinzu:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
```

## Schritt 1: DGN-Datei laden

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
DgnImage dgnImage = (DgnImage) Image.load(dataDir + "Nikon_D90_Camera.dgn");
```

## Schritt 2: JpegOptions-Objekt erstellen

```java
ImageOptionsBase options = new JpegOptions();
```

## Schritt 3: Rasterisierungsoptionen zuweisen

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(600);
vectorOptions.setPageHeight(400);
vectorOptions.setNoScaling(true);
vectorOptions.setAutomaticLayoutsScaling(false);
options.setVectorRasterizationOptions(vectorOptions);
```

## Schritt 4: Speichern Sie das konvertierte Bild

```java
OutputStream outStream = new FileOutputStream(dataDir + "ExportDGNToRasterImage_Out.jpg");
dgnImage.save(outStream, options);
```

Wiederholen Sie diese Schritte für Ihre spezifischen DGN-Dateien und passen Sie die Dateipfade entsprechend an.

## Abschluss

Glückwunsch! Sie haben erfolgreich gelernt, wie Sie DGN-Dateien mit Aspose.CAD für Java in das Rasterbildformat exportieren. Dieses Tutorial hat Ihnen das Wissen vermittelt, diese Funktionalität in Ihre Java-Anwendungen zu integrieren.

## FAQs

### F1: Kann ich Aspose.CAD für Java mit anderen CAD-Dateiformaten verwenden?

A1: Ja, Aspose.CAD unterstützt verschiedene CAD-Formate und bietet eine vielseitige Lösung für Java-Entwickler.

### F2: Gibt es eine kostenlose Testversion für Aspose.CAD für Java?

 A2: Ja, Sie können auf eine kostenlose Testversion zugreifen[Hier](https://releases.aspose.com/).

### F3: Wo finde ich Dokumentation für Aspose.CAD für Java?

 A3: Sehen Sie sich die Dokumentation an[Hier](https://reference.aspose.com/cad/java/).

### F4: Wie erhalte ich Unterstützung für Aspose.CAD für Java?

 A4: Besuchen Sie das Support-Forum[Hier](https://forum.aspose.com/c/cad/19).

### F5: Wo kann ich eine Lizenz für Aspose.CAD für Java erwerben?

 A5: Sie können eine Lizenz kaufen[Hier](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
