---
title: Erstellen einer einzelnen PDF-Datei mit verschiedenen Layouts – Aspose.CAD-Handbuch
linktitle: Erstellen einer einzelnen PDF-Datei mit verschiedenen Layouts
second_title: Aspose.CAD .NET – CAD- und BIM-Dateiformat
description: Erstellen Sie mit Aspose.CAD für .NET ein einzelnes PDF mit verschiedenen Layouts. Befolgen Sie unsere Schritt-für-Schritt-Anleitung für eine nahtlose Integration und effiziente PDF-Generierung.
weight: 13
url: /de/net/advanced-cad-techniques/creating-single-pdf-with-different-layouts/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Erstellen einer einzelnen PDF-Datei mit verschiedenen Layouts – Aspose.CAD-Handbuch

## Einführung

Möchten Sie mit Aspose.CAD für .NET ein einzelnes PDF-Dokument aus einer CAD-Zeichnung mit unterschiedlichen Layouts generieren? Diese Schritt-für-Schritt-Anleitung führt Sie durch den Prozess und hilft Ihnen dabei, eine nahtlose Integration und effiziente PDF-Erstellung zu erreichen. Aspose.CAD für .NET bietet leistungsstarke Funktionen zur programmgesteuerten Bearbeitung von CAD-Zeichnungen. In diesem Tutorial konzentrieren wir uns auf die Erstellung einer einzelnen PDF-Datei mit verschiedenen Layouts.

## Voraussetzungen

Bevor Sie mit dem Tutorial beginnen, stellen Sie sicher, dass Sie die folgenden Voraussetzungen erfüllen:

-  Aspose.CAD für .NET: Stellen Sie sicher, dass Aspose.CAD für .NET installiert ist. Sie können es herunterladen unter[Hier](https://releases.aspose.com/cad/net/).

- Entwicklungsumgebung: Richten Sie eine .NET-Entwicklungsumgebung ein und verfügen Sie über grundlegende Kenntnisse der C#-Programmierung.

## Namespaces importieren

Fügen Sie in Ihr C#-Projekt die erforderlichen Namespaces ein, um die Funktionen von Aspose.CAD für .NET zu nutzen:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Schritt 1: Laden Sie das CAD-Bild

```csharp
// Der Pfad zum Dokumentenverzeichnis.
string MyDir = "Your Document Directory";

using (CadImage cadImage = (CadImage)Image.Load(MyDir + "City skyway map.dwg"))
{
    // Ihr Code für Schritt 1 finden Sie hier
}
```

## Schritt 2: Rasterisierungsoptionen anpassen

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1000;
rasterizationOptions.PageHeight = 1000;

// Benutzerdefinierte Größen für mehrere Layouts
rasterizationOptions.LayoutPageSizes.Add("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.LayoutPageSizes.Add("8.5 x 11 Plot", new SizeF(1000, 100));
```

## Schritt 3: Definieren Sie PDF-Optionen

```csharp
PdfOptions pdfOptions = new PdfOptions() { VectorRasterizationOptions = rasterizationOptions };
```

## Schritt 4: Als PDF speichern

```csharp
cadImage.Save(MyDir + "singlePDF_out.pdf", pdfOptions);
```

Jetzt haben Sie mit Aspose.CAD für .NET erfolgreich ein einzelnes PDF-Dokument mit verschiedenen Layouts erstellt. Entdecken Sie gerne weitere Funktionen und passen Sie den Code an Ihre spezifischen Anforderungen an.

## Abschluss

In diesem Tutorial haben wir den Prozess der Erstellung einer einzelnen PDF-Datei aus einer CAD-Zeichnung mit unterschiedlichen Layouts mit Aspose.CAD für .NET behandelt. Diese leistungsstarke Bibliothek vereinfacht CAD-Manipulationsaufgaben und bietet Flexibilität für verschiedene Szenarien.

## FAQs

### F1: Kann ich Aspose.CAD für .NET mit anderen CAD-Formaten verwenden?

A1: Ja, Aspose.CAD für .NET unterstützt verschiedene CAD-Formate wie DWG, DXF, DGN und mehr.

### F2: Gibt es eine kostenlose Testversion?

 A2: Ja, Sie können eine kostenlose Testversion ausprobieren[Hier](https://releases.aspose.com/).

### F3: Wie erhalte ich Unterstützung für Aspose.CAD für .NET?

 A3: Besuchen Sie die[Aspose.CAD-Forum](https://forum.aspose.com/c/cad/19) für die Unterstützung der Gemeinschaft.

### F4: Wo finde ich eine ausführliche Dokumentation?

 A4: Sehen Sie sich die Dokumentation an[Hier](https://reference.aspose.com/cad/net/).

### F5: Kann ich eine Lizenz für Aspose.CAD für .NET erwerben?

 A5: Ja, Sie können eine Lizenz kaufen[Hier](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
