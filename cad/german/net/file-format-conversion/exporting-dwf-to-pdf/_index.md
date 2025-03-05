---
title: Exportieren von DWF in PDF – Aspose.CAD-Handbuch
linktitle: Exportieren von DWF in PDF
second_title: Aspose.CAD .NET – CAD- und BIM-Dateiformat
description: Entdecken Sie eine nahtlose Anleitung zum Exportieren von DWF in PDF mit Aspose.CAD für .NET. Erweitern Sie mühelos Ihre Möglichkeiten zur Bearbeitung von CAD-Dateien.
type: docs
weight: 10
url: /de/net/file-format-conversion/exporting-dwf-to-pdf/
---
## Einführung

In der Welt der .NET-Entwicklung sticht Aspose.CAD als leistungsstarke Bibliothek für den Umgang mit CAD-Dateien (Computer-Aided Design) hervor. In diesem Tutorial konzentrieren wir uns auf eine bestimmte Aufgabe: den Export von DWF-Dateien (Design Web Format) in PDF mit Aspose.CAD für .NET. Egal, ob Sie ein erfahrener Entwickler sind oder gerade erst anfangen, folgen Sie uns, um diese Funktionalität nahtlos in Ihre Anwendungen zu integrieren.

## Voraussetzungen

Bevor Sie mit dem Tutorial beginnen, stellen Sie sicher, dass Sie die folgenden Voraussetzungen erfüllen:

-  Aspose.CAD für .NET: Stellen Sie sicher, dass Aspose.CAD für .NET installiert ist. Sie können es herunterladen unter[Hier](https://releases.aspose.com/cad/net/).

- Entwicklungsumgebung: Richten Sie eine funktionierende .NET-Entwicklungsumgebung ein, einschließlich Visual Studio oder einer anderen bevorzugten IDE.

## Namespaces importieren

Beginnen Sie mit dem Importieren der erforderlichen Namespaces in Ihr Projekt. Dieser Schritt ist entscheidend für den Zugriff auf die von Aspose.CAD bereitgestellten Funktionen.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

## Schritt 1: Laden Sie die DWF-Datei

Laden Sie zunächst die DWF-Datei, die Sie als PDF exportieren möchten. Passen Sie den Dateipfad entsprechend an.

```csharp
string MyDir = "Your Document Directory";
string fileName = MyDir + "18-12-11 9644 - site.dwf";

using (Image image = Image.Load(fileName))
{
    // Ihr Code hier...
}
```

## Schritt 2: Rasterisierungsoptionen konfigurieren

Richten Sie die Rasterungsoptionen für DWF ein, um die gewünschte Ausgabe sicherzustellen. In diesem Beispiel definieren wir die Seitenhöhe und -breite.

```csharp
CadRasterizationOptions dwfRasterizationOptions = new CadRasterizationOptions();
dwfRasterizationOptions.PageHeight = 500;
dwfRasterizationOptions.PageWidth = 500;
```

## Schritt 3: Definieren Sie PDF-Optionen

Erstellen Sie PDF-Optionen und verknüpfen Sie sie mit den zuvor konfigurierten Rasterisierungsoptionen.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = dwfRasterizationOptions;
```

## Schritt 4: Als PDF exportieren

Führen Sie den Exportvorgang aus und geben Sie dabei den Ausgabepfad für die resultierende PDF-Datei an.

```csharp
string outPath = MyDir + "18-12-11 9644 - site.pdf";
image.Save(outPath, pdfOptions);
```

## Schritt 5: Überprüfen Sie den Export

Stellen Sie den erfolgreichen Export von 3D-Bildern in PDF sicher. Zeigt eine Bestätigungsmeldung mit dem gespeicherten Dateipfad an.

```csharp
Console.WriteLine("\n3D images exported successfully to PDF.\nFile saved at " + MyDir);
```

Jetzt haben Sie die DWF-zu-PDF-Exportfunktionalität mit Aspose.CAD erfolgreich in Ihrer .NET-Anwendung implementiert.

## Abschluss

In diesem Tutorial haben wir den Prozess des Exportierens von DWF-Dateien in PDF mit Aspose.CAD für .NET untersucht. Wenn Sie diese Schritte befolgen, können Sie diese Funktionalität nahtlos in Ihre Projekte integrieren und so Ihre Möglichkeiten zur Bearbeitung von CAD-Dateien verbessern.

## FAQs

### F1: Kann ich Aspose.CAD für .NET mit anderen CAD-Dateiformaten verwenden?

A1: Ja, Aspose.CAD unterstützt verschiedene CAD-Dateiformate, einschließlich DWG, DXF, DWF und mehr. Eine umfassende Liste finden Sie in der Dokumentation.

### F2: Wo finde ich zusätzliche Unterstützung für Aspose.CAD?

 A2: Weitere Unterstützung finden Sie unter[Aspose.CAD-Forum](https://forum.aspose.com/c/cad/19) Hier können Sie Fragen stellen und mit der Community interagieren.

### F3: Gibt es eine kostenlose Testversion für Aspose.CAD?

 A3: Ja, Sie können eine kostenlose Testversion von Aspose.CAD unter erkunden[Hier](https://releases.aspose.com/).

### F4: Wie erhalte ich eine temporäre Lizenz für Aspose.CAD?

 A4: Sie können eine temporäre Lizenz erhalten von[dieser Link](https://purchase.aspose.com/temporary-license/).

### F5: Wo kann ich die Vollversion von Aspose.CAD für .NET kaufen?

 A5: Sie können die Vollversion von Aspose.CAD für .NET bei erwerben[Hier](https://purchase.aspose.com/buy).