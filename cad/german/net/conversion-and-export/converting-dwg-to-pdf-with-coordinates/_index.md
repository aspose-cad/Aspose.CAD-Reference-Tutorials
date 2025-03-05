---
title: Konvertieren von DWG in PDF mit Koordinaten in C# – Aspose.CAD-Tutorial
linktitle: Konvertieren von DWG in PDF mit Koordinaten in C#
second_title: Aspose.CAD .NET – CAD- und BIM-Dateiformat
description: Erfahren Sie, wie Sie mit Aspose.CAD DWG mit bestimmten Koordinaten in C# in PDF konvertieren. Befolgen Sie unsere Schritt-für-Schritt-Anleitung für präzise und effiziente CAD-Dateikonvertierungen.
type: docs
weight: 11
url: /de/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/
---
## Einführung

Willkommen zu diesem umfassenden Tutorial zum Konvertieren von DWG-Dateien in PDF mit angegebenen Koordinaten mithilfe von Aspose.CAD für .NET. Aspose.CAD ist eine leistungsstarke Bibliothek, die es Entwicklern ermöglicht, nahtlos mit CAD-Dateiformaten in ihren .NET-Anwendungen zu arbeiten. In diesem Tutorial führen wir Sie durch den Prozess der Konvertierung einer DWG-Datei in eine PDF-Datei und geben dabei bestimmte Koordinaten an, um die Präzision zu erhöhen.

## Voraussetzungen

Bevor wir beginnen, stellen Sie sicher, dass Sie die folgenden Voraussetzungen erfüllen:

- Aspose.CAD-Bibliothek: Laden Sie die Aspose.CAD-Bibliothek für .NET herunter und installieren Sie sie. Sie finden die Bibliothek[Hier](https://releases.aspose.com/cad/net/).

- Entwicklungsumgebung: Stellen Sie sicher, dass Sie eine kompatible Entwicklungsumgebung eingerichtet haben, einschließlich Visual Studio oder einer anderen bevorzugten IDE.

- DWG-Datei: Halten Sie eine DWG-Datei zur Konvertierung bereit. Sie können die bereitgestellte Beispieldatei oder Ihre benutzerdefinierte DWG-Datei verwenden.

## Namespaces importieren

Importieren Sie in Ihrem C#-Projekt die erforderlichen Namespaces:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadParameters;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.ImageOptions;
```

Lassen Sie uns den Code zum besseren Verständnis in eine Schritt-für-Schritt-Anleitung unterteilen:

## Schritt 1: Definieren Sie das Dokumentenverzeichnis

```csharp
string MyDir = "Your Document Directory";
```

## Schritt 2: Legen Sie den Quell-DWG-Dateipfad fest

```csharp
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
```

## Schritt 3: DWG-Datei laden und Rasterisierungsoptionen konfigurieren

```csharp
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
    rasterizationOptions.Layouts = new string[] { "Model" };
    rasterizationOptions.NoScaling = true;
```

## Schritt 4: Koordinaten und Ansichtsfenster definieren

```csharp
    Point topLeft = new Point(500, 1000);
    double width = 3108;
    double height = 2489;

    CadVportTableObject newView = new CadVportTableObject();
    newView.Name = new CadStringParameter();
    newView.Name.Init("*Active");
    newView.CenterPoint.X = topLeft.X + width / 2f;
    newView.CenterPoint.Y = topLeft.Y - height / 2f;
    newView.ViewHeight.Value = height;
    newView.ViewAspectRatio.Value = width / height;
```

## Schritt 5: Ansichtsfenstereinstellungen anwenden

```csharp
    for (int i = 0; i < cadImage.ViewPorts.Count; i++)
    {
        CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
        if (cadImage.ViewPorts.Count == 1 || string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
        {
            cadImage.ViewPorts[i] = newView;
            break;
        }
    }
```

## Schritt 6: PDF-Optionen und Export konfigurieren

```csharp
    Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
    pdfOptions.VectorRasterizationOptions = rasterizationOptions;

    MyDir = MyDir + "ConvertDWGToPDFBySupplyingCoordinates_out.pdf";
    cadImage.Save(MyDir, pdfOptions);
}
```

## Schritt 7: Erfolgsmeldung anzeigen

```csharp
Console.WriteLine("\nThe DWG file exported successfully to PDF.\nFile saved at " + MyDir);
```

## Abschluss

Glückwunsch! Sie haben mit Aspose.CAD für .NET erfolgreich eine DWG-Datei mit den angegebenen Koordinaten in eine PDF-Datei konvertiert. Dieses Tutorial behandelte wesentliche Schritte und bot Entwicklern eine klare Anleitung.

## FAQs

### F1: Kann ich Aspose.CAD mit anderen CAD-Dateiformaten verwenden?

A1: Ja, Aspose.CAD unterstützt verschiedene CAD-Formate, einschließlich DWG, DXF, DWF und mehr.

### F2: Wie kann ich mit Fehlern während des Konvertierungsprozesses umgehen?

A2: Implementieren Sie Fehlerbehandlungsmechanismen mithilfe von Try-Catch-Blöcken, um Ausnahmen zu erfassen und zu verwalten.

### F3: Ist Aspose.CAD sowohl für Windows- als auch für Linux-Umgebungen geeignet?

A3: Ja, Aspose.CAD ist sowohl mit Windows- als auch mit Linux-Plattformen kompatibel.

### F4: Kann ich die PDF-Ausgabe weiter anpassen?

A4: Auf jeden Fall! Entdecken Sie die umfangreichen Möglichkeiten von Aspose.CAD, um die PDF-Ausgabe an Ihre spezifischen Anforderungen anzupassen.

### F5: Wo finde ich zusätzlichen Support oder Community-Diskussionen?

A5: Besuchen Sie die[Aspose.CAD-Forum](https://forum.aspose.com/c/cad/19) für Community-Unterstützung und Diskussionen.