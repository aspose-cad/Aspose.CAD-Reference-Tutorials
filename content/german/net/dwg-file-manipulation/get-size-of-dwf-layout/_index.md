---
title: Arbeiten mit DWG-Dateien in C# – Größe des DWF-Layouts ermitteln
linktitle: Arbeiten mit DWG-Dateien in C# – Größe des DWF-Layouts ermitteln
second_title: Aspose.CAD .NET – CAD- und BIM-Dateiformat
description: Entdecken Sie die Leistungsfähigkeit von Aspose.CAD für .NET beim Umgang mit DWG-Dateien. Erfahren Sie, wie Sie mit C# mühelos DWF-Layoutgrößen extrahieren.
type: docs
weight: 10
url: /de/net/dwg-file-manipulation/get-size-of-dwf-layout/
---
## Einführung

Im Bereich des computergestützten Designs (CAD) und der .NET-Entwicklung gilt Aspose.CAD als leistungsstarkes Werkzeug für den Umgang mit DWG-Dateien. Dieses Tutorial führt Sie durch die Arbeit mit DWG-Dateien in C# und das Extrahieren der Größe eines DWF-Layouts. Bevor wir uns mit dem Code befassen, stellen wir sicher, dass Sie alles vorbereitet haben, um diese Reise anzutreten.

## Voraussetzungen

Um diesem Tutorial reibungslos folgen zu können, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

-  Aspose.CAD für .NET: Stellen Sie sicher, dass Aspose.CAD für .NET installiert ist. Sie können es hier herunterladen[Aspose.CAD für .NET-Downloadseite](https://releases.aspose.com/cad/net/).

Nachdem Sie nun über die erforderlichen Tools verfügen, können wir uns mit der Codierung befassen.

## Namespaces importieren

Bevor wir mit der Arbeit mit dem Code beginnen, importieren wir die erforderlichen Namespaces:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Dwf;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

Diese Namespaces stellen die wesentlichen Klassen und Methoden für die Verarbeitung von CAD-Dateien mit Aspose.CAD in Ihrer C#-Anwendung bereit.

## Schritt 1: Richten Sie Ihre Umgebung ein

Stellen Sie zunächst sicher, dass Sie die richtige Umgebung für Ihr Projekt eingerichtet haben. Verweisen Sie auf die Aspose.CAD-Bibliothek in Ihrem C#-Projekt.

## Schritt 2: Dateipfade definieren

Definieren Sie die Pfade für Ihre DWG-Datei und das Ausgabeverzeichnis für die generierten JPG-Dateien:

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "blocks_and_tables.dwf";
```

## Schritt 3: Laden Sie das DWF-Bild

Laden Sie das DWF-Bild mit Aspose.CAD:

```csharp
using (DwfImage image = (DwfImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    // Code für weitere Schritte finden Sie hier
}
```

## Schritt 4: Durch die Seiten iterieren

Durchlaufen Sie die Seiten des DWF-Bildes:

```csharp
foreach (var page in image.Pages)
{
    // Code für weitere Schritte finden Sie hier
}
```

## Schritt 5: Layoutinformationen abrufen

Erhalten Sie Layoutinformationen von jeder Seite:

```csharp
var layout = page.Name;
System.Console.WriteLine("Layout= " + layout);
```

## Schritt 6: JPG-Optionen einrichten

Richten Sie Optionen zum Speichern des Layouts als JPG-Datei ein:

```csharp
using (FileStream fs = new FileStream(MyDir + "layout_" + layout + ".jpg", FileMode.Create))
{
    JpegOptions jpegOptions = new JpegOptions();
    CadRasterizationOptions options = new CadRasterizationOptions();
    options.Layouts = new string[] { layout };
    // Code für weitere Schritte finden Sie hier
}
```

## Schritt 7: Bestimmen Sie die Seitengröße

Bestimmen Sie die Größe des DWF-Layouts:

```csharp
double sizeExtX = page.MaxPoint.X - page.MinPoint.X;
double sizeExtY = page.MaxPoint.Y - page.MinPoint.Y;
// Code für weitere Schritte finden Sie hier
```

## Schritt 8: Seitenabmessungen einrichten

Richten Sie die Seitenabmessungen basierend auf dem Einheitentyp ein:

```csharp
if (page.UnitType == UnitType.Inch)
{
    options.PageHeight = CommonHelper.INtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.INtoPixels(sizeExtX, CommonHelper.DPI);
}
else if (page.UnitType == UnitType.Millimeter)
{
    options.PageHeight = CommonHelper.MMtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.MMtoPixels(sizeExtX, CommonHelper.DPI);
}
else
{
    options.PageHeight = (float)sizeExtY;
    options.PageWidth = (float)sizeExtX;
}
```

## Schritt 9: Speichern Sie die JPG-Datei

Speichern Sie die JPG-Datei mit den angegebenen Optionen:

```csharp
jpegOptions.VectorRasterizationOptions = options;
image.Save(fs, jpegOptions);
}
```

Jetzt haben Sie die Größe des DWF-Layouts mit Aspose.CAD in C# erfolgreich aus der DWG-Datei extrahiert. Entdecken Sie gerne weitere Features und Funktionalitäten, die Aspose.CAD für die .NET-Entwicklung bietet.

## Abschluss

In diesem Tutorial haben wir den Prozess der Arbeit mit DWG-Dateien in C# mithilfe von Aspose.CAD durchlaufen. Wenn Sie diese Schritte befolgen, können Sie nicht nur die Größe eines DWF-Layouts erreichen, sondern auch die Funktionen von Aspose.CAD für verschiedene CAD-bezogene Aufgaben in Ihren .NET-Projekten nutzen.

## FAQs

### F1: Ist Aspose.CAD mit den neuesten DWG-Dateiformaten kompatibel?

 A1: Aspose.CAD unterstützt verschiedene DWG-Dateiformate, einschließlich der neuesten Versionen. Siehe die[Dokumentation](https://reference.aspose.com/cad/net/) für spezifische Kompatibilitätsdetails.

### F2: Kann ich Aspose.CAD sowohl für kommerzielle als auch für private Projekte verwenden?

A2: Ja, Aspose.CAD bietet flexible Lizenzoptionen sowohl für den kommerziellen als auch für den persönlichen Gebrauch. Besuche den[Kaufseite](https://purchase.aspose.com/buy) für mehr Details.

### F3: Wie kann ich eine temporäre Lizenz für Aspose.CAD erhalten?

 A3: Sie können eine temporäre Lizenz erhalten von[Hier](https://purchase.aspose.com/temporary-license/) zu Auswertungszwecken.

### F4: Wo finde ich Unterstützung für Aspose.CAD?

 A4: Bei Fragen oder Hilfe besuchen Sie bitte die[Aspose.CAD-Forum](https://forum.aspose.com/c/cad/19).

### F5: Gibt es eine kostenlose Testversion für Aspose.CAD?

 A5: Ja, Sie können auf eine kostenlose Testversion von Aspose.CAD zugreifen[Hier](https://releases.aspose.com/).