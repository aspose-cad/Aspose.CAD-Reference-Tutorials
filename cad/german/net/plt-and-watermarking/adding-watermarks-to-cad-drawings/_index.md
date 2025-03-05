---
title: Wasserzeichen zu CAD-Zeichnungen hinzufügen – Aspose.CAD-Handbuch
linktitle: Hinzufügen von Wasserzeichen zu CAD-Zeichnungen
second_title: Aspose.CAD .NET – CAD- und BIM-Dateiformat
description: Verbessern Sie Ihre CAD-Zeichnungen mit professionellen Wasserzeichen mit Aspose.CAD für .NET. Befolgen Sie unsere Schritt-für-Schritt-Anleitung für personalisierte und ansprechende Designs.
type: docs
weight: 11
url: /de/net/plt-and-watermarking/adding-watermarks-to-cad-drawings/
---
## Einführung

Möchten Sie Ihre CAD-Zeichnungen durch das Hinzufügen professioneller Wasserzeichen verbessern? Aspose.CAD für .NET bietet eine robuste Lösung zur nahtlosen Integration von Wasserzeichen in Ihre CAD-Dateien. In dieser Schritt-für-Schritt-Anleitung führen wir Sie durch den Prozess des Hinzufügens von Wasserzeichen mit Aspose.CAD und stellen so sicher, dass Ihre Zeichnungen nicht nur wichtige Informationen vermitteln, sondern auch Ihr einzigartiges Zeichen tragen.

## Voraussetzungen

Bevor Sie mit dem Tutorial beginnen, stellen Sie sicher, dass Sie über Folgendes verfügen:
-  Aspose.CAD für .NET: Stellen Sie sicher, dass die Aspose.CAD-Bibliothek installiert ist. Sie können es herunterladen[Hier](https://releases.aspose.com/cad/net/).
- Ihr Dokumentenverzeichnis: Richten Sie ein Verzeichnis zum Speichern Ihrer CAD-Zeichnungen ein.
Beginnen wir nun mit dem Hinzufügen von Wasserzeichen zu Ihren CAD-Zeichnungen!

## Namespaces importieren

Beginnen Sie mit dem Importieren der erforderlichen Namespaces in Ihr .NET-Projekt:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Schritt 1: Laden Sie die CAD-Zeichnung

```csharp
// Der Pfad zum Dokumentenverzeichnis.
string MyDir = "Your Document Directory";
using (CadImage cadImage = (CadImage)Image.Load(MyDir + "Drawing11.dwg")) {
```

## Schritt 2: Wasserzeichen als MTEXT hinzufügen

```csharp
// Neuen MTEXT hinzufügen
CadMText watermark = new CadMText();
watermark.Text = "Watermark message";
watermark.InitialTextHeight = 40;
watermark.InsertionPoint = new Cad3DPoint(300, 40);
watermark.LayerName = "0";
cadImage.BlockEntities["*Model_Space"].AddEntity(watermark);
```

## Schritt 3: Oder fügen Sie Wasserzeichen als Text hinzu

```csharp
// Alternativ können Sie eine einfachere Entität wie Text hinzufügen
CadText text = new CadText();
text.DefaultValue = "Watermark text";
text.TextHeight = 40;
text.FirstAlignment = new Cad3DPoint(300, 40);
text.LayerName = "0";
cadImage.BlockEntities["*Model_Space"].AddEntity(text);
```

## Schritt 4: Als PDF exportieren

```csharp
// Exportieren Sie die CAD-Zeichnung mit Wasserzeichen als PDF
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.Layouts = new[] { "Model" };
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
cadImage.Save(MyDir + "AddWatermark_out.pdf", pdfOptions);
```

Wiederholen Sie diese Schritte für verschiedene Zeichnungen, und Sie erhalten im Handumdrehen professionell aussehende CAD-Dateien mit Wasserzeichen!

## Abschluss

Glückwunsch! Sie haben erfolgreich gelernt, wie Sie mit Aspose.CAD für .NET Wasserzeichen zu Ihren CAD-Zeichnungen hinzufügen. Mit diesem einfachen, aber leistungsstarken Verfahren können Sie Ihre Designs personalisieren und gleichzeitig die Integrität Ihrer technischen Zeichnungen bewahren.

## FAQs

### F1: Kann ich das Erscheinungsbild des Wasserzeichens anpassen?

A1: Ja, Sie können den Text, die Schriftart, die Größe und die Position des Wasserzeichens nach Ihren Wünschen anpassen.

### F2: Ist Aspose.CAD mit verschiedenen CAD-Dateiformaten kompatibel?

A2: Aspose.CAD unterstützt verschiedene CAD-Dateiformate, einschließlich DWG und DXF, und gewährleistet so eine umfassende Kompatibilität.

### F3: Kann ich einer einzelnen CAD-Zeichnung mehrere Wasserzeichen hinzufügen?

A3: Auf jeden Fall! Sie können beliebig viele Wasserzeichen hinzufügen und bieten so Flexibilität für verschiedene Anwendungsfälle.

### F4: Bietet Aspose.CAD eine kostenlose Testversion an?

A4: Ja, Sie können die Funktionen von Aspose.CAD mit einer kostenlosen Testversion erkunden. Bekomme es[Hier](https://releases.aspose.com/).

### F5: Wo finde ich Unterstützung für Aspose.CAD?

 A5: Bei Fragen oder Hilfe besuchen Sie die[Aspose.CAD-Forum](https://forum.aspose.com/c/cad/19).