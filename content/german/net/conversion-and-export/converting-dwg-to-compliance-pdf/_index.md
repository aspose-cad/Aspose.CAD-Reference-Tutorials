---
title: Konvertieren von DWG in Compliance-PDF – Aspose.CAD-Tutorial
linktitle: Konvertieren von DWG in Compliance-PDF
second_title: Aspose.CAD .NET – CAD- und BIM-Dateiformat
description: Konvertieren Sie DWG in Compliance-PDF mit Aspose.CAD für .NET. Folgen Sie unserem Tutorial für eine Schritt-für-Schritt-Anleitung.
type: docs
weight: 13
url: /de/net/conversion-and-export/converting-dwg-to-compliance-pdf/
---
## Einführung

Willkommen zu unserem Schritt-für-Schritt-Tutorial zum Konvertieren von DWG-Dateien in Compliance-PDF mit Aspose.CAD für .NET. Aspose.CAD ist eine leistungsstarke .NET-API, die es Entwicklern ermöglicht, mühelos mit CAD-Dateiformaten zu arbeiten. In diesem Tutorial führen wir Sie mit detaillierten Beispielen und Erklärungen durch den Prozess der Konvertierung einer DWG-Datei in ein Compliance-PDF.

## Voraussetzungen

Bevor wir beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

-  Aspose.CAD für .NET: Stellen Sie sicher, dass die Aspose.CAD-Bibliothek in Ihr .NET-Projekt integriert ist. Sie können es herunterladen[Hier](https://releases.aspose.com/cad/net/).

- Entwicklungsumgebung: Installieren Sie eine funktionierende .NET-Entwicklungsumgebung und stellen Sie sicher, dass sie richtig konfiguriert ist.

- Beispiel-DWG-Datei: Laden Sie eine Beispiel-DWG-Datei herunter, die Sie in Compliance-PDF konvertieren möchten.

## Namespaces importieren

Importieren Sie in Ihr .NET-Projekt die erforderlichen Namespaces, um die Aspose.CAD-Funktionen zu nutzen.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

Lassen Sie uns nun den Prozess der Konvertierung einer DWG-Datei in ein Compliance-PDF in mehrere Schritte unterteilen.

## Schritt 1: Laden Sie die DWG-Datei

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

Aspose.CAD.Image cadImage = Aspose.CAD.Image.Load(sourceFilePath);
```

## Schritt 2: Rasterisierungsoptionen festlegen

 Erstellen Sie eine Instanz von`CadRasterizationOptions` und konfigurieren Sie seine Eigenschaften, wie z. B. Hintergrundfarbe, Seitenbreite und Seitenhöhe.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions
{
    BackgroundColor = Aspose.CAD.Color.White,
    PageWidth = 1600,
    PageHeight = 1600
};
```

## Schritt 3: PDF-Optionen erstellen

 Erstellen Sie eine Instanz von`PdfOptions` und legen Sie die Optionen für die Vektorrasterung fest.

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions,
    CorePdfOptions = new PdfDocumentOptions { Compliance = PdfCompliance.PdfA1a }
};
```

## Schritt 4: Als PDF speichern (A1a-Konformität)

Speichern Sie das CAD-Bild als Compliance-PDF mit A1a-Konformität.

```csharp
cadImage.Save(MyDir + "PDFA1_A.pdf", pdfOptions);
```

## Schritt 5: Als PDF speichern (A1b-Konformität)

Ändern Sie den Compliance-Typ in A1b und speichern Sie das CAD-Bild als Compliance-PDF.

```csharp
pdfOptions.CorePdfOptions.Compliance = PdfCompliance.PdfA1b;
cadImage.Save(MyDir + "PDFA1_B.pdf", pdfOptions);
```

## Abschluss

Glückwunsch! Sie haben eine DWG-Datei mit Aspose.CAD für .NET erfolgreich in Compliance PDF konvertiert. Dieses Tutorial bietet eine umfassende Anleitung für Entwickler, die CAD-Konvertierungsfunktionen in ihre Anwendungen integrieren möchten.

## FAQs

### F1: Kann ich mit Aspose.CAD andere CAD-Formate in Compliance PDF konvertieren?

A1: Ja, Aspose.CAD unterstützt verschiedene CAD-Formate und ermöglicht die Konvertierung in Compliance PDF.

### F2: Ist Aspose.CAD mit .NET Core kompatibel?

A2: Ja, Aspose.CAD ist sowohl mit .NET Framework als auch .NET Core kompatibel.

### F3: Gibt es Lizenzoptionen für Aspose.CAD?

 A3: Ja, Sie können Lizenzierungsoptionen erkunden[Hier](https://purchase.aspose.com/buy).

### F4: Gibt es eine kostenlose Testversion?

 A4: Ja, Sie können eine kostenlose Testversion erhalten[Hier](https://releases.aspose.com/).

### F5: Wo erhalte ich Unterstützung für Aspose.CAD?

 A5: Besuchen Sie die[Aspose.CAD-Forum](https://forum.aspose.com/c/cad/19) für alle Supportanfragen.