---
title: Festlegen der Leinwandgröße und des Leinwandmodus in Aspose.CAD für .NET
linktitle: Festlegen von Leinwandgröße und -modus
second_title: Aspose.CAD .NET – CAD- und BIM-Dateiformat
description: Entdecken Sie die Schritt-für-Schritt-Anleitung zum Festlegen der Leinwandgröße und des Leinwandmodus in Aspose.CAD für .NET. Optimieren Sie Ihr CAD-Rendering ganz einfach mit diesem umfassenden Tutorial.
weight: 16
url: /de/net/cad-features-and-support/setting-canvas-size-and-mode/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Festlegen der Leinwandgröße und des Leinwandmodus in Aspose.CAD für .NET

## Einführung

Sind Sie bereit, das volle Potenzial von Aspose.CAD für .NET auszuschöpfen und Ihr CAD-Rendering-Erlebnis zu revolutionieren? In diesem Schritt-für-Schritt-Tutorial befassen wir uns mit den Feinheiten der Einstellung von Leinwandgröße und -modus mithilfe der leistungsstarken Aspose.CAD-Bibliothek. Unabhängig davon, ob Sie ein erfahrener Entwickler sind oder gerade erst anfangen, führt Sie dieser Leitfaden durch den Prozess und stellt sicher, dass Sie die Funktionen von Aspose.CAD effektiv nutzen.

## Voraussetzungen

Bevor wir uns mit dem Tutorial befassen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

-  Aspose.CAD-Bibliothek: Laden Sie die Aspose.CAD-Bibliothek von herunter und installieren Sie sie[Aspose.CAD-Website](https://releases.aspose.com/cad/net/).

- Entwicklungsumgebung: Stellen Sie sicher, dass auf Ihrem Computer eine .NET-Entwicklungsumgebung eingerichtet ist.

-  Beispiel-CAD-Datei: Für dieses Tutorial verwenden wir eine Beispiel-DXF-Datei. Einen finden Sie im[Aspose.CAD-Dokumentation](https://reference.aspose.com/cad/net/).

## Namespaces importieren

Importieren Sie zunächst die erforderlichen Namespaces am Anfang Ihrer .NET-Anwendung:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Schritt 1: CAD-Datei laden

Beginnen Sie mit dem Laden der CAD-Datei mit dem folgenden Code:

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    //Ihren Code für weitere Schritte finden Sie hier
}
```

## Schritt 2: Erstellen Sie CadRasterizationOptions

 Erstellen Sie eine Instanz von`CadRasterizationOptions` und legen Sie seine Eigenschaften fest:

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
rasterizationOptions.NoScaling = false;
```

## Schritt 3: PDFOptions erstellen

 Erstellen Sie eine Instanz von`PdfOptions` und stellen Sie es ein`VectorRasterizationOptions` Eigentum:

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Schritt 4: Als PDF exportieren

Exportieren Sie die CAD-Datei mit den konfigurierten Optionen in PDF:

```csharp
image.Save(MyDir + "result_out.pdf", pdfOptions);
```

## Schritt 5: TiffOptions erstellen

 Erstellen Sie eine Instanz von`TiffOptions` und stellen Sie es ein`VectorRasterizationOptions` Eigentum:

```csharp
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Schritt 6: Als TIFF exportieren

Exportieren Sie die CAD-Datei mit den konfigurierten Optionen nach TIFF:

```csharp
image.Save(MyDir + "result_out.tiff", tiffOptions);
```

## Abschluss

Glückwunsch! Sie haben die Leinwandgröße und den Leinwandmodus in Aspose.CAD für .NET erfolgreich festgelegt. Diese leistungsstarke Funktion eröffnet eine Welt voller Möglichkeiten für das CAD-Rendering. Experimentieren Sie mit verschiedenen Optionen und entdecken Sie das volle Potenzial von Aspose.CAD in Ihren .NET-Anwendungen.

## FAQs

### F1: Kann ich Aspose.CAD mit anderen .NET-Bibliotheken verwenden?

A1: Ja, Aspose.CAD lässt sich nahtlos in andere .NET-Bibliotheken integrieren und bietet erweiterte Funktionen für die CAD-Manipulation.

### F2: Ist eine kostenlose Testversion für Aspose.CAD verfügbar?

 A2: Ja, Sie können die Funktionen von Aspose.CAD mit einer kostenlosen Testversion erkunden. Besuchen[Hier](https://releases.aspose.com/) um loszulegen.

### F3: Wie kann ich Unterstützung für Aspose.CAD erhalten?

 A3: Für Unterstützung und Diskussionen besuchen Sie die[Aspose.CAD-Forum](https://forum.aspose.com/c/cad/19).

### F4: Wo finde ich eine umfassende Dokumentation für Aspose.CAD?

 A4: Siehe[Aspose.CAD-Dokumentation](https://reference.aspose.com/cad/net/) Ausführliche Informationen und Beispiele finden Sie hier.

### F5: Wie kaufe ich Aspose.CAD für .NET?

 A5: Um Aspose.CAD zu kaufen, besuchen Sie die[Kaufseite](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
