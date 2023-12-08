---
title: Exportieren eingebetteter DGN-Dateien – Aspose.CAD-Tutorial
linktitle: Exportieren eingebetteter DGN-Dateien
second_title: Aspose.CAD .NET – CAD- und BIM-Dateiformat
description: Entdecken Sie die Leistungsfähigkeit von Aspose.CAD für .NET. Erfahren Sie in dieser Schritt-für-Schritt-Anleitung, wie Sie eingebettete DGN-Dateien mühelos in PDF exportieren.
type: docs
weight: 14
url: /de/net/export-techniques/exporting-embedded-dgn-files/
---
## Einführung

In der dynamischen Welt der Softwareentwicklung sticht Aspose.CAD für .NET als leistungsstarkes Werkzeug für den Umgang mit CAD-Dateien (Computer-Aided Design) hervor. Dieses Tutorial führt Sie durch den Prozess des Exports eingebetteter DGN-Dateien mit Aspose.CAD für .NET. Egal, ob Sie ein erfahrener Entwickler oder ein neugieriger Anfänger sind, diese Schritt-für-Schritt-Anleitung hilft Ihnen dabei, die Funktionen von Aspose.CAD effektiv zu nutzen.

## Voraussetzungen

Bevor Sie mit dem Tutorial beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

1.  Aspose.CAD für .NET: Laden Sie die Bibliothek herunter und installieren Sie sie[Aspose.CAD für .NET](https://releases.aspose.com/cad/net/).

2. Entwicklungsumgebung: Richten Sie eine .NET-Entwicklungsumgebung mit Visual Studio oder einer anderen bevorzugten IDE ein.

3. Beispiel-DXF-Datei: Für dieses Tutorial verwenden wir die Datei „conic_pyramid.dxf“. Stellen Sie sicher, dass es in Ihrem angegebenen Dokumentenverzeichnis verfügbar ist.

## Namespaces importieren

Stellen Sie sicher, dass Sie in Ihrem C#-Code die erforderlichen Namespaces importieren:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
```

## Schritt 1: Laden Sie die DXF-Datei

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    //Ihren Code für weitere Schritte finden Sie hier
}
```

## Schritt 2: Rasterisierungsoptionen festlegen

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new[] { "Model" };
```

## Schritt 3: PDF-Optionen festlegen

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Schritt 4: Als PDF speichern

```csharp
cadImage.Save(MyDir + "conic_pyramid.pdf", pdfOptions);
```

## Schritt 5: Erfolgsmeldung anzeigen

```csharp
Console.WriteLine("\nThe DXF drawing exported successfully to PDF.\nFile saved at " + MyDir);
```

## Abschluss

Glückwunsch! Sie haben eine eingebettete DGN-Datei mit Aspose.CAD für .NET erfolgreich in PDF exportiert. Dieses Tutorial behandelt die wesentlichen Schritte und bietet Ihnen eine Grundlage für die Erkundung der erweiterten Funktionen von Aspose.CAD.

## FAQs

### F1: Kann ich Aspose.CAD für .NET mit anderen Programmiersprachen verwenden?

A1: Aspose.CAD unterstützt hauptsächlich .NET, Aspose bietet jedoch Bibliotheken für verschiedene Sprachen, einschließlich Java und Python.

### F2: Gibt es eine kostenlose Testversion für Aspose.CAD für .NET?

 A2: Ja, Sie können eine kostenlose Testversion von erhalten[Hier](https://releases.aspose.com/).

### F3: Wo finde ich eine umfassende Dokumentation für Aspose.CAD für .NET?

 A3: Sehen Sie sich die Dokumentation an[Hier](https://reference.aspose.com/cad/net/).

### F4: Wie erhalte ich eine temporäre Lizenz für Aspose.CAD für .NET?

 A4: Besorgen Sie sich eine temporäre Lizenz[Hier](https://purchase.aspose.com/temporary-license/).

### F5: Benötigen Sie Hilfe oder möchten Sie mit der Community in Kontakt treten?

A5: Besuchen Sie die[Aspose.CAD-Forum](https://forum.aspose.com/c/cad/19) für Unterstützung und Diskussionen.