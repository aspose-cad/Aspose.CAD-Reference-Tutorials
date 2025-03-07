---
title: Konvertieren Sie Layouts in Rasterbilder in Aspose.CAD für .NET
linktitle: Konvertieren Sie Layouts in Rasterbilder
second_title: Aspose.CAD .NET – CAD- und BIM-Dateiformat
description: Konvertieren Sie CAD-Layouts mühelos in Rasterbilder mit Aspose.CAD für .NET. Verbessern Sie Ihre Entwicklung mit leistungsstarken CAD-Manipulationsfunktionen.
weight: 12
url: /de/net/cad-drawing-manipulation/convert-layouts-to-raster-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konvertieren Sie Layouts in Rasterbilder in Aspose.CAD für .NET

## Einführung

Möchten Sie Layouts in Ihren .NET-Anwendungen mühelos in Rasterbilder konvertieren? Suchen Sie nicht weiter! Diese Schritt-für-Schritt-Anleitung führt Sie durch den Prozess mit Aspose.CAD für .NET, einer leistungsstarken Bibliothek, die Computer-Aided Design (CAD)-Aufgaben vereinfacht.

## Voraussetzungen

Bevor Sie mit dem Tutorial beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

- Aspose.CAD für .NET-Bibliothek: Laden Sie die Bibliothek von herunter und installieren Sie sie[Aspose.CAD für .NET-Downloadseite](https://releases.aspose.com/cad/net/).

- Entwicklungsumgebung: Stellen Sie sicher, dass auf Ihrem Computer eine funktionierende .NET-Entwicklungsumgebung eingerichtet ist.

- Zu konvertierendes Dokument: Bereiten Sie ein CAD-Dokument vor, das die Layouts enthält, die Sie in Rasterbilder konvertieren möchten.

- Ihr Dokumentenverzeichnis: Ersetzen Sie den Platzhalter „Ihr Dokumentenverzeichnis“ im Code durch den Pfad zu Ihrem Dokumentenverzeichnis.

## Namespaces importieren

Importieren wir zunächst die notwendigen Namespaces, um die Aspose.CAD-Funktionalitäten in Ihrem Code zugänglich zu machen.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Schritt 1: Laden Sie das CAD-Dokument

Beginnen Sie mit dem Laden des CAD-Dokuments mithilfe der Aspose.CAD-Bibliothek.

```csharp
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image image = Image.Load(sourceFilePath))
{
    //Ihren Code für weitere Schritte finden Sie hier
}
```

## Schritt 2: Rasterisierungsoptionen konfigurieren

 Erstellen Sie eine Instanz von`CadRasterizationOptions` , um die Seitenbreite und -höhe festzulegen und die Layouts anzugeben, die Sie konvertieren möchten.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1200;
rasterizationOptions.PageHeight = 1200;
rasterizationOptions.Layouts = new string[] { "Model", "Layout1" };
```

## Schritt 3: TiffOptions für das resultierende Bild einrichten

 Erstellen Sie eine Instanz von`TiffOptions`um das Format des resultierenden Bildes zu definieren.

```csharp
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.VectorRasterizationOptions = rasterizationOptions;
```

## Schritt 4: Speichern Sie das resultierende Bild

Geben Sie den Ausgabepfad an und speichern Sie das konvertierte Bild.

```csharp
string outputFilePath = MyDir + "conic_pyramid_layoutstorasterimage_out.tiff";
image.Save(outputFilePath, options);
```

## Abschluss

Glückwunsch! Sie haben CAD-Layouts mit Aspose.CAD für .NET erfolgreich in ein Rasterbildformat konvertiert. Die Möglichkeiten sind vielfältig und dieser Leitfaden dient als Ausgangspunkt für Ihre CAD-bezogenen Bemühungen.

## FAQs

### F1: Ist Aspose.CAD mit allen CAD-Formaten kompatibel?

 A1: Aspose.CAD unterstützt eine Vielzahl von CAD-Formaten, darunter DWG, DXF, DWF, STL und mehr. Überprüf den[Dokumentation](https://reference.aspose.com/cad/net/) für eine umfassende Liste.

### F2: Wie kann ich eine temporäre Lizenz für Aspose.CAD erhalten?

 A2: Besuchen Sie die[temporäre Lizenzseite](https://purchase.aspose.com/temporary-license/) eine temporäre Lizenz zu Test- und Evaluierungszwecken zu erwerben.

### F3: Wo finde ich Unterstützung für Aspose.CAD?

 A3: Foren sind ein großartiger Ort, um Hilfe zu suchen. Besuche den[Aspose.CAD-Forum](https://forum.aspose.com/c/cad/19) um mit der Community in Kontakt zu treten und Hilfe zu erhalten.

### F4: Kann ich Aspose.CAD kostenlos testen?

 A4: Auf jeden Fall! Schnapp dir dein[Kostenlose Testphase](https://releases.aspose.com/) um die Funktionen und Möglichkeiten von Aspose.CAD zu erkunden.

### F5: Wo kann ich eine Lizenz für Aspose.CAD erwerben?

 A5: Navigieren Sie zu[Kaufseite](https://purchase.aspose.com/buy) um eine Lizenz zu kaufen und das volle Potenzial von Aspose.CAD auszuschöpfen.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
