---
title: Exportieren Sie eingebettete DGN in PDF mit Aspose.CAD für Java
linktitle: Eingebettete DGN exportieren
second_title: Aspose.CAD Java API
description: Entdecken Sie die Schritt-für-Schritt-Anleitung zum Exportieren eingebetteter DGN-Dateien in PDF mit Aspose.CAD für Java. Erweitern Sie Ihre Java-Anwendungen durch nahtlose Bearbeitung von CAD-Dateien.
type: docs
weight: 11
url: /de/java/dgn-export-options/export-embedded-dgn/
---
## Einführung

Willkommen zu diesem umfassenden Tutorial zum Exportieren eingebetteter DGN-Dateien mit Aspose.CAD für Java. Aspose.CAD ist eine leistungsstarke Bibliothek, die Java-Entwicklern die nahtlose Arbeit mit CAD-Dateien ermöglicht. In diesem Tutorial führen wir Sie anhand von Schritt-für-Schritt-Anleitungen durch den Prozess des Exportierens eingebetteter DGN-Dateien in PDF. Unabhängig davon, ob Sie ein erfahrener Entwickler sind oder gerade erst anfangen, hilft Ihnen dieses Tutorial dabei, die Funktionen von Aspose.CAD zu nutzen, um Ihre Java-Anwendungen zu verbessern.

## Voraussetzungen

Bevor wir uns mit dem Tutorial befassen, stellen Sie sicher, dass Sie die folgenden Voraussetzungen erfüllen:
- Java-Entwicklungsumgebung: Stellen Sie sicher, dass auf Ihrem Computer eine Java-Entwicklungsumgebung eingerichtet ist.
-  Aspose.CAD für Java: Laden Sie die Aspose.CAD für Java-Bibliothek von herunter und installieren Sie sie[Hier](https://releases.aspose.com/cad/java/).

## Pakete importieren

Um zu beginnen, müssen Sie die erforderlichen Pakete in Ihr Java-Projekt importieren. Fügen Sie Ihrem Code die folgenden Importanweisungen hinzu:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Lassen Sie uns nun den Beispielcode in mehrere Schritte unterteilen:

## Schritt 1: Eingabe- und Ausgabepfade einrichten

Definieren Sie den Verzeichnispfad, in dem sich Ihr Dokument befindet, und geben Sie den Namen der Eingabe-DWG-Datei an.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
```

## Schritt 2: DWG-Datei laden

 Laden Sie die DWG-Datei in eine`Image` Objekt mit Aspose.CAD.

```java
Image objImage = Image.load(fileName);
```

## Schritt 3: Rasterisierungsoptionen konfigurieren

Konfigurieren Sie Rasterisierungsoptionen, z. B. Layouts, die in den Export einbezogen werden sollen.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setLayouts(new String[] {"Model"});
```

## Schritt 4: PDF-Optionen konfigurieren

Richten Sie PDF-Optionen ein, einschließlich Vektor-Rasterisierungsoptionen.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Schritt 5: PDF-Datei speichern

Speichern Sie die PDF-Datei mit den konfigurierten Optionen.
```java
objImage.save(dataDir + "BlockRefDgn.pdf", pdfOptions);
```

## Abschluss

Glückwunsch! Sie haben eine eingebettete DGN-Datei mit Aspose.CAD für Java erfolgreich in PDF exportiert. In diesem Tutorial wurden die wesentlichen Schritte zur Integration von Aspose.CAD in Ihre Java-Anwendung für eine effiziente Bearbeitung von CAD-Dateien behandelt.

## FAQs

### F1: Kann ich Aspose.CAD für Java in einem kommerziellen Projekt verwenden?

 A1: Ja, Aspose.CAD für Java ist eine kommerzielle Bibliothek. Eine Lizenz erhalten Sie bei[Hier](https://purchase.aspose.com/buy).

### F2: Gibt es eine kostenlose Testversion?

 A2: Ja, Sie können auf eine kostenlose Testversion von Aspose.CAD für Java zugreifen[Hier](https://releases.aspose.com/).

### F3: Wie erhalte ich Unterstützung für Aspose.CAD für Java?

A3: Sie können Unterstützung von der Aspose.CAD-Community unter erhalten[Forum](https://forum.aspose.com/c/cad/19).

### F4: Was passiert, wenn ich eine temporäre Lizenz benötige?

 A4: Sie können eine temporäre Lizenz erhalten[Hier](https://purchase.aspose.com/temporary-license/).

### F5: Wo finde ich die Dokumentation?

 A5: Die Dokumentation ist verfügbar[Hier](https://reference.aspose.com/cad/java/).