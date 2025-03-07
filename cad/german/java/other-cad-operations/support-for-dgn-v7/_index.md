---
title: DGN-zu-PDF-Konvertierungshandbuch – Aspose.CAD für Java
linktitle: Unterstützung für DGN V7
second_title: Aspose.CAD Java API
description: Konvertieren Sie DGN-Dateien mühelos in PDF mit Aspose.CAD für Java. Befolgen Sie unsere Schritt-für-Schritt-Anleitung für eine nahtlose Integration und einen effizienten Workflow.
weight: 11
url: /de/java/other-cad-operations/support-for-dgn-v7/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DGN-zu-PDF-Konvertierungshandbuch – Aspose.CAD für Java

## Einführung

In der dynamischen Welt des CAD (Computer-Aided Design) ist die effiziente Konvertierung von DGN-Dateien (Design) in PDF (Portable Document Format) eine entscheidende Voraussetzung. Aspose.CAD für Java erweist sich als leistungsstarke Lösung, die nahtlose Integration und robuste Funktionen bietet. Diese Schritt-für-Schritt-Anleitung soll Sie durch den Prozess des Exports von DGN-Dateien in PDF mit Aspose.CAD für Java führen und so einen reibungslosen und effizienten Arbeitsablauf gewährleisten.

## Voraussetzungen

Bevor Sie mit dem Tutorial beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:
-  Aspose.CAD für Java-Bibliothek: Laden Sie die Bibliothek von herunter und installieren Sie sie[Aspose.CAD für Java-Downloadseite](https://releases.aspose.com/cad/java/).
- Java-Entwicklungsumgebung: Stellen Sie sicher, dass auf Ihrem Computer eine Java-Entwicklungsumgebung eingerichtet ist.

## Pakete importieren

Importieren Sie zunächst die erforderlichen Pakete in Ihr Java-Projekt:

## Schritt 1: Notwendige Pakete importieren

Importieren Sie in Ihrem Java-Projekt die erforderlichen Pakete für Aspose.CAD für Java.
```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.cadobjects.DgnImage;
import com.aspose.cad.imageoptions.PdfOptions;
import java.awt.Color;
```

## Schritt 2: Dateipfade festlegen

Definieren Sie die Pfade für Ihre Eingabe-DGN-Datei und die Ausgabe-PDF-Datei.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

## Schritt 3: DGN-Bild laden

Laden Sie das DGN-Bild mit der Aspose.CAD-Bibliothek.

```java
DgnImage objImage = (DgnImage)Image.load(fileName);
```

## Schritt 4: PDF-Exportoptionen konfigurieren

Richten Sie Optionen für den Export in PDF ein, einschließlich Seitenabmessungen, automatische Layoutskalierung, Hintergrundfarbe und bestimmte zu exportierende Layouts.

```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setBackgroundColor(Color.getBlack());
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); //Exportieren Sie nur 4 (1,2,3 und 9) Ansichten
options.setVectorRasterizationOptions(vectorOptions);
```

## Schritt 5: PDF-Datei speichern

Speichern Sie das DGN-Bild als PDF-Datei mit den angegebenen Optionen.

```java
objImage.save(outFile, options);
```

Wiederholen Sie diese Schritte für verschiedene DGN-Dateien und passen Sie Dateipfade und Optionen nach Bedarf an.

## Abschluss

Mit Aspose.CAD für Java wird die Konvertierung von DGN-Dateien in PDF zu einem unkomplizierten Vorgang. Dieser Leitfaden vermittelt Ihnen das Wissen, die Bibliothek nahtlos in Ihre Java-Projekte zu integrieren und so eine effiziente CAD-Dateikonvertierung zu ermöglichen.

## FAQs

### F1: Kann ich Aspose.CAD für Java mit anderen CAD-Dateiformaten verwenden?

A1: Ja, Aspose.CAD unterstützt verschiedene CAD-Formate und bietet vielseitige Funktionen, die über die Konvertierung von DGN in PDF hinausgehen.

### F2: Ist eine temporäre Lizenz für Aspose.CAD für Java verfügbar?

 A2: Ja, Sie können eine temporäre Lizenz erhalten[Hier](https://purchase.aspose.com/temporary-license/) zu Testzwecken.

### F3: Wie kann ich Unterstützung suchen oder Fragen zu Aspose.CAD für Java stellen?

 A3: Besuchen Sie die[Aspose.CAD-Forum](https://forum.aspose.com/c/cad/19)um mit der Community in Kontakt zu treten und Hilfe zu suchen.

### F4: Welche Layouts kann ich beim Konvertieren von DGN in PDF exportieren?

 A4: Sie können die zu exportierenden Layouts angeben, indem Sie die anpassen`setLayouts` Array im Code.

### F5: Wo finde ich eine umfassende Dokumentation für Aspose.CAD für Java?

 A5: Siehe[Aspose.CAD für Java-Dokumentation](https://reference.aspose.com/cad/java/) für detaillierte Informationen.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
