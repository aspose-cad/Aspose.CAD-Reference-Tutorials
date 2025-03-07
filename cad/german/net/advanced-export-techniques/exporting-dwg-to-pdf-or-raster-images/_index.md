---
title: Exportieren von DWG in PDF- oder Rasterbilder – Aspose.CAD-Handbuch
linktitle: Exportieren von DWG in PDF- oder Rasterbilder
second_title: Aspose.CAD .NET – CAD- und BIM-Dateiformat
description: Entdecken Sie eine umfassende Anleitung zum Exportieren von DWG in PDF oder Rasterbilder mit Aspose.CAD für .NET. Lernen Sie die Schritte und Voraussetzungen kennen und nutzen Sie diese leistungsstarke Bibliothek praktisch.
weight: 11
url: /de/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportieren von DWG in PDF- oder Rasterbilder – Aspose.CAD-Handbuch

## Einführung

Möchten Sie DWG-Dateien in Ihrer .NET-Anwendung nahtlos in PDF- oder Rasterbilder konvertieren? Suchen Sie nicht weiter! Diese Schritt-für-Schritt-Anleitung führt Sie durch den Prozess mit der leistungsstarken Aspose.CAD für .NET-Bibliothek. Egal, ob Sie ein erfahrener Entwickler sind oder gerade erst anfangen, dieses Tutorial ist für alle Kenntnisstufen geeignet.

## Voraussetzungen

Bevor wir uns mit dem Tutorial befassen, stellen Sie sicher, dass Sie Folgendes eingerichtet haben:

- Ein grundlegendes Verständnis der .NET-Programmierung.
-  Aspose.CAD für .NET-Bibliothek installiert. Wenn nicht, laden Sie es herunter[Hier](https://releases.aspose.com/cad/net/).
- Ihre bevorzugte integrierte Entwicklungsumgebung (IDE), eingerichtet für die .NET-Entwicklung.

## Namespaces importieren

Beginnen wir mit dem Importieren der erforderlichen Namespaces in Ihr .NET-Projekt. Dadurch wird sichergestellt, dass Sie Zugriff auf die Aspose.CAD-Funktionalität in Ihrem Code haben.

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

## Schritt 1: DWG-Datei laden

Laden Sie zunächst die DWG-Datei, die Sie konvertieren möchten. Ersetzen Sie „Ihr Dokumentverzeichnis“ durch den Pfad zu Ihrer DWG-Datei.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Ihr Code zum Laden von DWG finden Sie hier
}
```

## Schritt 2: PDF-Export einrichten

Jetzt konfigurieren wir die PDF-Exporteinstellungen. Dieses Beispiel zeigt, wie das Layout festgelegt und Einheitenumrechnungen durchgeführt werden.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };

// Überprüfen und definieren Sie das Einheitensystem
bool currentUnitIsMetric = false;
double currentUnitCoefficient = 1.0;
DefineUnitSystem(cadImage.UnitType, out currentUnitIsMetric, out currentUnitCoefficient);

// Ihr Code zum Einrichten des PDF-Exports finden Sie hier
```

## Schritt 3: Als PDF exportieren

Führen Sie den Export nach PDF mit den konfigurierten Einstellungen durch.

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath, pdfOptions);
```

## Schritt 4: In Rasterbilder exportieren

Erweitern Sie die Funktionalität zum Exportieren in Rasterbilder wie PNG.

```csharp
// A4-Größe bei 300 DPI – 2480 x 3508
rasterizationOptions.PageHeight = 3508;
rasterizationOptions.PageWidth = 2480;

PngOptions pngOptions = new PngOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath.Replace("pdf", "png"), pngOptions);
```

## Abschluss

Glückwunsch! Sie haben erfolgreich gelernt, wie Sie mit Aspose.CAD für .NET DWG-Dateien sowohl in PDF- als auch in Rasterbilder exportieren. Diese leistungsstarke Bibliothek rationalisiert den Prozess und macht ihn effizient und entwicklerfreundlich.

## FAQs

### F1: Kann ich Aspose.CAD für .NET in meinen kommerziellen Projekten verwenden?

 A1: Ja, das können Sie. Besuchen[Purchase.aspose.com/buy](https://purchase.aspose.com/buy) für Lizenzdetails.

### F2: Gibt es eine kostenlose Testversion?

 A2: Auf jeden Fall! Sichern Sie sich Ihre kostenlose Testversion[Hier](https://releases.aspose.com/).

### F3: Wie erhalte ich Unterstützung für Aspose.CAD für .NET?

 A3: Gehen Sie rüber zum[Aspose.CAD-Forum](https://forum.aspose.com/c/cad/19) für die Unterstützung der Gemeinschaft.

### F4: Kann ich zu Testzwecken eine temporäre Lizenz erhalten?

 A4: Ja, Sie können eine temporäre Lizenz erhalten[Hier](https://purchase.aspose.com/temporary-license/).

### F5: Wo finde ich die ausführliche Dokumentation?

 A5: Die Dokumentation ist verfügbar unter[Aspose.CAD](https://reference.aspose.com/cad/net/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
