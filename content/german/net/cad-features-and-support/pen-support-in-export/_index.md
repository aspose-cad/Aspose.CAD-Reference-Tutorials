---
title: Optimieren Sie den CAD-Export mit benutzerdefinierten Stiftoptionen in Aspose.CAD für .NET
linktitle: Stiftunterstützung beim Export
second_title: Aspose.CAD .NET – CAD- und BIM-Dateiformat
description: Erfahren Sie, wie Sie Ihre CAD-Bildexporte mit Aspose.CAD für .NET verbessern. Passen Sie die Stiftoptionen an, um atemberaubende Grafiken in PDF, PNG, BMP und mehr zu erhalten.
type: docs
weight: 12
url: /de/net/cad-features-and-support/pen-support-in-export/
---
## Einführung

Aspose.CAD für .NET bietet leistungsstarke Tools für die Arbeit mit CAD-Dateien (Computer-Aided Design), mit denen Entwickler CAD-Bilder nahtlos bearbeiten und exportieren können. Eine bemerkenswerte Funktion ist die Stiftunterstützung während des Exports, die es Benutzern ermöglicht, die Anfangs- und Endkappeneinstellungen für Stifte anzupassen, wenn sie CAD-Bilder in verschiedene Formate wie PDF, PNG, BMP, GIF, JPEG2000, JPEG, PSD, TIFF und WMF exportieren.

In diesem Tutorial befassen wir uns mit den Besonderheiten der Stiftunterstützung beim Export mit Aspose.CAD für .NET. Wir werden jeden Schritt aufschlüsseln und Ihnen klare Erklärungen und Beispiele geben, die Sie durch den Prozess führen.

## Voraussetzungen

Bevor wir uns mit dem Tutorial befassen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

-  Aspose.CAD für .NET ist in Ihrer Entwicklungsumgebung installiert. Sie können es hier herunterladen[Release-Seite](https://releases.aspose.com/cad/net/).

- Ein grundlegendes Verständnis der CAD-Dateiformate, insbesondere DXF (Drawing Exchange Format).

- Grundkenntnisse der Programmiersprache C#.

## Namespaces importieren

Stellen Sie zunächst sicher, dass Sie die erforderlichen Namespaces in Ihr C#-Projekt importieren:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Drawing;
using System.Drawing.Drawing2D;
```

## Schritt 1: Richten Sie Ihr Dokumentenverzeichnis ein

Definieren Sie das Verzeichnis, in dem sich Ihr CAD-Dokument befindet:

```csharp
string MyDir = "Your Document Directory";
```

## Schritt 2: Laden Sie das CAD-Bild

Laden Sie das CAD-Bild mit Aspose.CAD:

```csharp
string sourceFilePath = MyDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage)Image.Load(sourceFilePath);
```

## Schritt 3: Rasterisierungsoptionen konfigurieren

Erstellen Sie Rasterisierungs- und PDF-Optionen, um den Exportvorgang anzupassen:

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
PdfOptions pdfOptions = new PdfOptions();
```

## Schritt 4: Passen Sie die Stiftoptionen an

Legen Sie die Start- und Endkappenoptionen für Stifte fest:

```csharp
rasterizationOptions.PenOptions = new PenOptions
{
   StartCap = LineCap.Flat,
   EndCap = LineCap.Flat
};
```

## Schritt 5: Vektor-Rasterisierungsoptionen anwenden

Wenden Sie die Rasterungsoptionen auf die PDF-Optionen an:

```csharp
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Schritt 6: Speichern Sie das exportierte PDF

Speichern Sie das CAD-Bild mit benutzerdefinierten Stiftoptionen als PDF-Datei:

```csharp
cadImage.Save(MyDir + "9LHATT-A56_generated.pdf", pdfOptions);
```

## Abschluss

In diesem Tutorial haben wir die Stiftunterstützung in der Exportfunktion von Aspose.CAD für .NET untersucht. Indem Sie der Schritt-für-Schritt-Anleitung folgen, können Sie die Anfangs- und Endkappeneinstellungen für Stifte ganz einfach anpassen und so die Flexibilität Ihrer CAD-Bildexporte erhöhen.

Experimentieren Sie ruhig mit verschiedenen Stiftoptionen, um die gewünschten visuellen Effekte in Ihren exportierten Bildern zu erzielen.

## FAQs

### F1: Kann ich diese Stiftoptionen für andere Bildformate außer PDF verwenden?

A1: Ja, die Stiftoptionen können auf verschiedene Bildformate wie PNG, BMP, GIF, JPEG und mehr angewendet werden.

### F2: Wo finde ich zusätzliche Dokumentation für Aspose.CAD für .NET?

 A2: Siehe[Dokumentation](https://reference.aspose.com/cad/net/) Ausführliche Informationen und Beispiele finden Sie hier.

### F3: Gibt es eine kostenlose Testversion für Aspose.CAD für .NET?

 A3: Ja, Sie können auf eine kostenlose Testversion zugreifen[Hier](https://releases.aspose.com/).

### F4: Wie kann ich temporäre Lizenzen für Aspose.CAD für .NET erhalten?

 A4: Besuchen Sie die[temporäre Lizenzseite](https://purchase.aspose.com/temporary-license/) für temporäre Lizenzoptionen.

### F5: Wo kann ich Community-Unterstützung für Aspose.CAD für .NET suchen?

 A5: Interagieren Sie mit der Community auf der[Aspose.CAD-Forum](https://forum.aspose.com/c/cad/19).