---
title: Zeitüberschreitung beim Speichern für CAD mit Aspose.CAD
linktitle: Setzen Sie beim Speichern eine Zeitüberschreitung
second_title: Aspose.CAD Java API
description: Erfahren Sie, wie Sie mit Aspose.CAD die Leistung Ihrer Java-Anwendung steigern. Legen Sie beim Speichern von CAD-Zeichnungen eine Zeitüberschreitung fest. Folgen Sie unserer Schritt-für-Schritt-Anleitung.
weight: 15
url: /de/java/other-cad-operations/put-timeout-on-save/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Zeitüberschreitung beim Speichern für CAD mit Aspose.CAD

## Einführung

Willkommen beim Tutorial zum Festlegen einer Zeitüberschreitung beim Speichern mit Aspose.CAD für Java. In diesem Leitfaden führen wir Sie durch den Prozess des Festlegens eines Zeitlimits für das Speichern von CAD-Zeichnungen, um die Leistung Ihrer Anwendung zu verbessern. Aspose.CAD für Java ist eine leistungsstarke Bibliothek, die Ihnen die nahtlose Arbeit mit CAD-Dateien in Ihren Java-Anwendungen ermöglicht.

## Voraussetzungen

Bevor Sie mit dem Tutorial beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:
-  Aspose.CAD für Java-Bibliothek: Stellen Sie sicher, dass die Aspose.CAD für Java-Bibliothek in Ihr Projekt integriert ist. Sie können die Bibliothek unter herunterladen[Webseite](https://releases.aspose.com/cad/java/).
- Entwicklungsumgebung: Richten Sie Ihre Java-Entwicklungsumgebung mit allen erforderlichen Tools und Abhängigkeiten ein.

## Pakete importieren

Importieren Sie zunächst die erforderlichen Pakete in Ihr Java-Projekt. Fügen Sie am Anfang Ihrer Java-Datei die folgenden Zeilen hinzu:

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterruptionTokenSource;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.concurrent.TimeUnit;
```

Lassen Sie uns nun den Beispielcode in Schritt-für-Schritt-Anleitungen unterteilen:

## Schritt 1: Quell- und Ausgabeverzeichnisse festlegen

```java
final String SourceDir = Utils.getDataDir_DWGDrawings();
final String OutputDir = Utils.getDataDir_Output();
```

Stellen Sie sicher, dass Sie über die richtigen Quell- und Ausgabeverzeichnisse für Ihre CAD-Zeichnungen verfügen.

## Schritt 2: Unterbrechungstokenquelle erstellen

```java
final InterruptionTokenSource source = new com.aspose.cad.InterruptionTokenSource();
```

Initialisieren Sie eine Unterbrechungstokenquelle, um Unterbrechungen während des Speichervorgangs zu verwalten.

## Schritt 3: CAD-Zeichnung laden

```java
final CadImage cadImageBig = (CadImage)Image.load(SourceDir + "Drawing11.dwg");
```

 Laden Sie die CAD-Zeichnung in ein`CadImage` Objekt.

## Schritt 4: Rasterisierungsoptionen konfigurieren

```java
CadRasterizationOptions rasterizationOptionsBig = new CadRasterizationOptions();
rasterizationOptionsBig.setPageWidth(cadImageBig.getSize().getWidth() / 2);
rasterizationOptionsBig.setPageHeight(cadImageBig.getSize().getHeight() / 2);
```

Konfigurieren Sie Rasterisierungsoptionen für die CAD-Zeichnung.

## Schritt 5: PDF-Optionen konfigurieren

```java
final PdfOptions CADfBig = new PdfOptions();
CADfBig.setVectorRasterizationOptions(rasterizationOptionsBig);
CADfBig.setInterruptionToken(source.getToken());
```

Richten Sie PDF-Optionen mit Vektor-Rasterisierungsoptionen und dem Unterbrechungstoken ein.

## Schritt 6: Zeichnung mit Timeout speichern

```java
cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
```

Speichern Sie die CAD-Zeichnung mit dem angegebenen Zeitlimit in einer PDF-Datei.

## Schritt 7: Behandeln Sie die Unterbrechung

```java
java.lang.Thread thread = new java.lang.Thread(new Runnable() {
    @Override
    public void run() {
        try {
            cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
        } catch (Throwable th) {
            System.out.println("interrupted !!!");
        }
    }
});
thread.start();
TimeUnit.SECONDS.sleep(3);
source.interrupt();
thread.join();
```

Erstellen Sie einen Thread, der den Speichervorgang abwickelt, und unterbrechen Sie ihn nach einem angegebenen Timeout.

## Abschluss

Glückwunsch! Sie haben erfolgreich gelernt, wie Sie mit Aspose.CAD für Java eine Zeitüberschreitung beim Speichern festlegen. Diese Funktion kann die Effizienz Ihrer CAD-bezogenen Anwendungen erheblich steigern.

## FAQs

### F1: Wie kann ich Aspose.CAD für Java herunterladen?

 A1: Sie können es von herunterladen[Veröffentlichungsseite](https://releases.aspose.com/cad/java/).

### F2: Wo finde ich die Dokumentation für Aspose.CAD für Java?

 A2: Siehe[Dokumentation](https://reference.aspose.com/cad/java/) für umfassende Informationen.

### F3: Gibt es eine kostenlose Testversion?

A3: Ja, Sie können eine kostenlose Testversion von erhalten[dieser Link](https://releases.aspose.com/).

### F4: Wie erhalte ich eine temporäre Lizenz?

 A4: Besuchen[Hier](https://purchase.aspose.com/temporary-license/) für Details zur temporären Lizenz.

### F5: Benötigen Sie Hilfe oder haben Sie Fragen?

 A5: Gehen Sie rüber zum[Aspose.CAD-Forum](https://forum.aspose.com/c/cad/19) für die Unterstützung der Gemeinschaft.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
