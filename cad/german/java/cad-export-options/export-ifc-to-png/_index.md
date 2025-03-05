---
title: Exportieren Sie IFC nach PNG mit Aspose.CAD für Java
linktitle: IFC nach PNG exportieren
second_title: Aspose.CAD Java API
description: Konvertieren Sie IFC mühelos in PNG mit Aspose.CAD für Java. Folgen Sie unserer Schritt-für-Schritt-Anleitung.
type: docs
weight: 18
url: /de/java/cad-export-options/export-ifc-to-png/
---
## Einführung

Willkommen zu dieser Schritt-für-Schritt-Anleitung zum Exportieren von IFC (Industry Foundation Classes) nach PNG mit Aspose.CAD für Java. Aspose.CAD ist eine leistungsstarke Java-Bibliothek, die umfassende Funktionen für die Arbeit mit CAD-Dateien, einschließlich des IFC-Formats, bietet. In diesem Tutorial führen wir Sie durch den Prozess der Konvertierung einer IFC-Datei in ein PNG-Bild mit detaillierten Erklärungen zu jedem Schritt.

## Voraussetzungen

Bevor wir beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

-  Aspose.CAD-Bibliothek: Laden Sie die Aspose.CAD-Bibliothek für Java von herunter und installieren Sie sie[Download-Link](https://releases.aspose.com/cad/java/).

- Dokumentverzeichnis: Bereiten Sie auf Ihrem System ein Verzeichnis vor, in dem sich Ihre IFC-Datei befindet.

## Namespaces importieren

Importieren Sie in Ihrem Java-Projekt die erforderlichen Namespaces wie unten gezeigt:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## Schritt 1: Laden Sie die IFC-Datei

```java
String dataDir = "Your Document Directory" + "ExportingIFC/";
String fileName = dataDir + "example.ifc";
IfcImage cadImage = (IfcImage)Image.load(fileName);
```

Dieser Schritt beinhaltet das Laden der IFC-Datei mit Aspose.CAD.

## Schritt 2: Vektoroptionen festlegen

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

Konfigurieren Sie Vektoroptionen für die Rasterung und geben Sie die Seitenbreite und -höhe an.

## Schritt 3: PNG-Optionen festlegen

```java
PngOptions pngOptions = new PngOptions();
pngOptions.setVectorRasterizationOptions(vectorOptions);
```

Legen Sie PNG-Optionen fest, einschließlich Vektor-Rasterisierungsoptionen.

## Schritt 4: Als PNG speichern

```java
String outPath = dataDir + "example.png";
cadImage.save(outPath, pngOptions);
```

Speichern Sie das verarbeitete Bild im PNG-Format.

## Abschluss

Glückwunsch! Sie haben eine IFC-Datei mit Aspose.CAD für Java erfolgreich in PNG konvertiert. Dieses Tutorial bietet eine umfassende Anleitung, die sicherstellt, dass Sie diese Funktionalität nahtlos in Ihre Projekte integrieren können.

## FAQs

### F1: Ist Aspose.CAD mit allen Versionen von IFC-Dateien kompatibel?

 A1: Aspose.CAD unterstützt verschiedene Versionen von IFC-Dateien. Siehe die[Dokumentation](https://reference.aspose.com/cad/java/) für Kompatibilitätsdetails.

### F2: Kann ich die Rasterisierungsoptionen weiter anpassen?

 A2: Auf jeden Fall! Entdecke die[Dokumentation](https://reference.aspose.com/cad/java/) für erweiterte Anpassungsoptionen.

### F3: Gibt es eine Testversion?

A3: Ja, Sie können auf die kostenlose Testversion zugreifen[Hier](https://releases.aspose.com/).

### F4: Wie kann ich eine temporäre Lizenz für Aspose.CAD erhalten?

 A4: Besorgen Sie sich eine temporäre Lizenz von[dieser Link](https://purchase.aspose.com/temporary-license/).

### F5: Wo kann ich Hilfe suchen oder Probleme besprechen?

A5: Besuchen Sie die[Aspose.CAD-Forum](https://forum.aspose.com/c/cad/19) für die Unterstützung der Gemeinschaft.
