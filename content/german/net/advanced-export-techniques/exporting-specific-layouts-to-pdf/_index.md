---
title: Exportieren bestimmter Layouts in PDF – Aspose.CAD-Handbuch
linktitle: Exportieren bestimmter Layouts in PDF
second_title: Aspose.CAD .NET – CAD- und BIM-Dateiformat
description: Erfahren Sie, wie Sie mit Aspose.CAD für .NET bestimmte Layouts in PDF exportieren. Schritt-für-Schritt-Anleitung für eine nahtlose Integration.
type: docs
weight: 13
url: /de/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/
---
## Einführung

Willkommen zu unserer Schritt-für-Schritt-Anleitung zum Exportieren bestimmter Layouts in PDF mit Aspose.CAD für .NET. Aspose.CAD ist eine leistungsstarke Bibliothek, die Entwicklern die nahtlose Arbeit mit CAD-Dateiformaten ermöglicht. In diesem Tutorial konzentrieren wir uns auf den Export bestimmter Layouts aus einer DWG-Datei in eine PDF-Datei mithilfe von Aspose.CAD in einer .NET-Umgebung.

## Voraussetzungen

Bevor wir uns mit dem Tutorial befassen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

-  Aspose.CAD für .NET-Bibliothek: Stellen Sie sicher, dass Sie die Aspose.CAD-Bibliothek installiert haben. Sie können es herunterladen[Hier](https://releases.aspose.com/cad/net/).

- Entwicklungsumgebung: Richten Sie eine .NET-Entwicklungsumgebung ein, z. B. Visual Studio.

## Namespaces importieren

Importieren Sie in Ihrem .NET-Projekt die erforderlichen Namespaces für Aspose.CAD:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Schritt 1: DWG-Datei laden

```csharp
// Der Pfad zum Dokumentenverzeichnis.
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";

using (Image image = Image.Load(sourceFilePath))
{
    // Ihr Code für weitere Schritte finden Sie hier.
}
```

## Schritt 2: CadRasterizationOptions festlegen

```csharp
// Erstellen Sie eine Instanz von CadRasterizationOptions und legen Sie deren verschiedene Eigenschaften fest
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
```

## Schritt 3: Geben Sie den Layoutnamen an

```csharp
// Geben Sie den gewünschten Layoutnamen an
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

## Schritt 4: PDFOptions erstellen

```csharp
// Erstellen Sie eine Instanz von PDFOptions
PdfOptions pdfOptions = new PdfOptions();
// Legen Sie die VectorRasterizationOptions-Eigenschaft fest
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Schritt 5: Als PDF exportieren

```csharp
MyDir = MyDir + "ExportSpecificLayoutToPDF_out.pdf";
// Exportieren Sie die DWG-Datei als PDF
image.Save(MyDir, pdfOptions);
```

## Schritt 6: Erfolgsmeldung anzeigen

```csharp
// Erfolgsmeldung anzeigen
Console.WriteLine("\nThe DWG file with a specific layout exported successfully to PDF.\nFile saved at " + MyDir);
```

## Abschluss

Glückwunsch! Sie haben erfolgreich gelernt, wie Sie mit Aspose.CAD für .NET bestimmte Layouts in PDF exportieren. Dieser Leitfaden bietet eine detaillierte Anleitung und stellt sicher, dass Sie diese Funktionalität mühelos in Ihre Projekte integrieren können.

## FAQs

### F1: Kann ich mehrere Layouts gleichzeitig exportieren?

 A1: Ja, ändern Sie einfach das`Layouts` Array in Schritt 3, um die Namen aller gewünschten Layouts einzuschließen.

### F2: Ist Aspose.CAD mit anderen CAD-Dateiformaten kompatibel?

A2: Ja, Aspose.CAD unterstützt verschiedene CAD-Formate, darunter DWG, DXF, DWF und mehr.

### F3: Wie kann ich die PDF-Ausgabeeinstellungen anpassen?

 A3: Entdecken Sie die Eigenschaften von`CadRasterizationOptions` in Schritt 2 für Anpassungsoptionen.

### F4: Wo finde ich zusätzliche Aspose.CAD-Dokumentation?

 A4: Besuchen Sie die[Dokumentation](https://reference.aspose.com/cad/net/) für ausführliche Informationen.

### F5: Gibt es eine kostenlose Testversion?

 A5: Ja, Sie können auf die kostenlose Testversion zugreifen[Hier](https://releases.aspose.com/).