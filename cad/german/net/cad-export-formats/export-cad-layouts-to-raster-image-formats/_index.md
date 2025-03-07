---
title: Exportieren Sie CAD-Layouts in Rasterbildformate in Aspose.CAD für .NET
linktitle: Exportieren Sie CAD-Layouts in Rasterbildformate
second_title: Aspose.CAD .NET – CAD- und BIM-Dateiformat
description: Erfahren Sie, wie Sie CAD-Layouts mit Aspose.CAD für .NET in Rasterbilder exportieren. Befolgen Sie unsere Schritt-für-Schritt-Anleitung für eine nahtlose Konvertierung.
weight: 10
url: /de/net/cad-export-formats/export-cad-layouts-to-raster-image-formats/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportieren Sie CAD-Layouts in Rasterbildformate in Aspose.CAD für .NET

## Einführung

Möchten Sie CAD-Layouts mit Aspose.CAD für .NET effizient in Rasterbildformate konvertieren? Diese Schritt-für-Schritt-Anleitung führt Sie durch den Prozess und bietet detaillierte Anweisungen und Codeausschnitte, um die Aufgabe reibungslos zu gestalten. Egal, ob Sie ein erfahrener Entwickler oder ein Aspose.CAD-Neuling sind, dieses Tutorial ist für alle Erfahrungsstufen geeignet.

## Voraussetzungen

Bevor Sie mit dem Tutorial beginnen, stellen Sie sicher, dass Sie über Folgendes verfügen:

- Aspose.CAD für .NET-Bibliothek: Stellen Sie sicher, dass Sie die Aspose.CAD-Bibliothek installiert haben. Wenn nicht, können Sie es hier herunterladen[Aspose.CAD-Website](https://releases.aspose.com/cad/net/).

- CAD-Zeichnungsdatei: Bereiten Sie eine CAD-Zeichnungsdatei (z. B. conic_pyramid.dxf) vor, die Sie in Rasterbildformate konvertieren möchten.

## Namespaces importieren

Importieren Sie in Ihr .NET-Projekt die erforderlichen Namespaces, um die Funktionalitäten von Aspose.CAD zu nutzen. Fügen Sie am Anfang Ihres Codes die folgenden Namespaces ein:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Schritt 1: CAD-Zeichnung laden

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

// Laden Sie eine CAD-Zeichnung in eine Instanz von Image
using (var image = Image.Load(sourceFilePath))
{
    // Hier finden Sie Ihren Code zum Laden der CAD-Zeichnung
}
```

## Schritt 2: Erstellen Sie CadRasterizationOptions

```csharp
// Erstellen Sie eine Instanz von CadRasterizationOptions
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
```

## Schritt 3: Ebenen angeben

```csharp
// Fügen Sie den Ebenennamen zur Ebenenliste von CadRasterizationOptions hinzu
rasterizationOptions.Layers = new string[] { "LayerA" };
```

## Schritt 4: JpegOptions erstellen

```csharp
// Erstellen Sie eine Instanz von JpegOptions (oder einer beliebigen ImageOptions für Rasterformate).
var options = new JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
```

## Schritt 5: In das JPEG-Format exportieren

```csharp
// Exportieren Sie jede Ebene in das JPEG-Format
MyDir = MyDir + "CADLayersToRasterImageFormats_out.jpg";
image.Save(MyDir, options);
```

## Zusätzlicher Schritt: Alle Ebenen konvertieren

Wenn Sie alle Ebenen konvertieren möchten, verwenden Sie die folgende Methode:

```csharp
ConvertAllLayersToRasterImageFormats();
```

Diese Methode durchläuft alle Ebenen in der CAD-Zeichnung und exportiert jede Ebene in eine separate JPEG-Datei.

## Abschluss

Glückwunsch! Sie haben erfolgreich gelernt, wie Sie CAD-Layouts mit Aspose.CAD für .NET in Rasterbildformate exportieren. Dieses Tutorial bietet einen umfassenden Leitfaden für Entwickler, die effiziente und zuverlässige Lösungen für die CAD-Konvertierung suchen.

## FAQs

### F1: Kann ich andere Bildformate für den Export verwenden?

 A1: Ja, das können Sie. Einfach austauschen`JpegOptions` mit den Optionen des gewünschten Formats, wie z`PngOptions` oder`BmpOptions`.

### F2: Gibt es eine Testversion?

 A2: Ja, Sie können die Funktionalität von Aspose.CAD erkunden, indem Sie die Testversion herunterladen[Hier](https://releases.aspose.com/).

### F3: Wie kann ich Unterstützung für Aspose.CAD erhalten?

 A3: Besuchen Sie Aspose.CAD[Forum](https://forum.aspose.com/c/cad/19) für Community-Support oder erwägen Sie den Kauf einer Lizenz für dedizierten Support.

### F4: Sind temporäre Lizenzen verfügbar?

 A4: Ja, Sie können eine temporäre Lizenz erhalten[Hier](https://purchase.aspose.com/temporary-license/).

### F5: Wo finde ich die Dokumentation?

 A5: Weitere Informationen finden Sie in der ausführlichen Dokumentation[Hier](https://reference.aspose.com/cad/net/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
