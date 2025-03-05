---
title: Wasserzeichen zu CAD-Zeichnungen hinzufügen – Aspose.CAD für Java-Tutorial
linktitle: Wasserzeichen hinzufügen
second_title: Aspose.CAD Java API
description: Verbessern Sie Ihre CAD-Zeichnungen mit personalisierten Wasserzeichen mit Aspose.CAD für Java. Befolgen Sie unsere Schritt-für-Schritt-Anleitung für eine nahtlose Integration.
type: docs
weight: 12
url: /de/java/other-cad-operations/add-watermark/
---
## Einführung

Willkommen zu dieser umfassenden Anleitung zum Hinzufügen von Wasserzeichen zu CAD-Zeichnungen mit Aspose.CAD für Java. In diesem Tutorial erfahren Sie, wie Sie Wasserzeichen effizient integrieren und Ihre CAD-Dokumente mit personalisierten Nachrichten oder Branding aufwerten. Aspose.CAD für Java bietet eine Reihe leistungsstarker Funktionen, die das Hinzufügen von Wasserzeichen unkompliziert machen.

## Voraussetzungen

Bevor wir uns mit dem Tutorial befassen, stellen Sie sicher, dass Sie die folgenden Voraussetzungen erfüllen:

-  Aspose.CAD für Java: Stellen Sie sicher, dass die Aspose.CAD-Bibliothek in Ihrer Java-Umgebung installiert ist. Sie können es herunterladen[Hier](https://releases.aspose.com/cad/java/).
- Java Development Kit (JDK): Stellen Sie sicher, dass auf Ihrem System die neueste Version des JDK installiert ist.

## Pakete importieren

Importieren Sie in Ihr Java-Projekt die erforderlichen Aspose.CAD-Pakete, um zu beginnen:

```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.Cad3DPoint;
import com.aspose.cad.fileformats.cad.cadobjects.CadMText;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Schritt 1: Neuen MTEXT hinzufügen

```java
//neuen MTEXT hinzufügen
CadMText watermark = new CadMText();
watermark.setText("Watermark message");
watermark.setInitialTextHeight(40);
watermark.setInsertionPoint(new Cad3DPoint(300, 40));
watermark.setLayerName("0");
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(watermark);
```

## Schritt 2: Fügen Sie eine einfache Entität wie Text hinzu

Sie können auch eine einfachere Entität wie Text hinzufügen:

```java
// oder fügen Sie eine einfachere Entität wie Text hinzu
CadText text = new CadText();
text.setDefaultValue("Watermark text");
text.setTextHeight(40);
text.setFirstAlignment(new Cad3DPoint(300, 40));
text.setLayerName("0") ;
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(text);
```

## Schritt 3: Als PDF exportieren

Exportieren Sie die CAD-Zeichnung mit dem hinzugefügten Wasserzeichen in eine PDF-Datei:

```java
// als PDF exportieren
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setLayouts(new String[]{"Model"});
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
cadImage.save(dataDir + "AddWatermark_out.pdf", pdfOptions);

```

## Abschluss

Glückwunsch! Sie haben mit Aspose.CAD für Java erfolgreich Wasserzeichen zu Ihren CAD-Zeichnungen hinzugefügt. Mit diesem einfachen, aber leistungsstarken Verfahren können Sie Ihre Designs personalisieren oder durch Branding schützen.

## FAQs

### F1: Ist Aspose.CAD mit allen CAD-Dateiformaten kompatibel?

A1: Aspose.CAD unterstützt verschiedene CAD-Formate, einschließlich DWG, DXF, DWT und DWF.

### F2: Kann ich das Erscheinungsbild des Wasserzeichentextes anpassen?

A2: Ja, Sie haben die volle Kontrolle über das Erscheinungsbild des Wasserzeichens, einschließlich Textgröße, Farbe und Position.

### F3: Gibt es eine Testversion für Aspose.CAD für Java?

 A3: Ja, Sie können die Testversion herunterladen[Hier](https://releases.aspose.com/).

### F4: Wie kann ich Unterstützung für Aspose.CAD erhalten?

 A4: Besuchen Sie die[Aspose.CAD-Forum](https://forum.aspose.com/c/cad/19) für die Unterstützung der Gemeinschaft.

### F5: Wo finde ich die vollständige Dokumentation für Aspose.CAD für Java?

 A5: Siehe[Dokumentation](https://reference.aspose.com/cad/java/) für detaillierte Informationen.