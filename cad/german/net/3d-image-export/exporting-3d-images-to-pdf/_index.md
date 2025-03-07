---
title: Exportieren von 3D-Bildern in PDF – Aspose.CAD-Tutorial
linktitle: Exportieren von 3D-Bildern in PDF
second_title: Aspose.CAD .NET – CAD- und BIM-Dateiformat
description: Konvertieren Sie mühelos 3D-CAD-Bilder in PDF mit Aspose.CAD für .NET. Folgen Sie unserer Schritt-für-Schritt-Anleitung für den nahtlosen PDF-Export.
weight: 10
url: /de/net/3d-image-export/exporting-3d-images-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportieren von 3D-Bildern in PDF – Aspose.CAD-Tutorial

## Einführung

Möchten Sie 3D-Bilder mit Aspose.CAD für .NET nahtlos in PDF exportieren? Dieses Schritt-für-Schritt-Tutorial führt Sie durch den Prozess und stellt sicher, dass Sie die Leistungsfähigkeit von Aspose.CAD nutzen, um Ihre 3D-Bilder mühelos in das PDF-Format zu konvertieren.

## Voraussetzungen

Bevor Sie mit dem Tutorial beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

-  Aspose.CAD für .NET: Stellen Sie sicher, dass Sie die Aspose.CAD-Bibliothek für .NET installiert haben. Wenn nicht, können Sie es hier herunterladen[Aspose.CAD für .NET-Downloadseite](https://releases.aspose.com/cad/net/).

- Dokumentenverzeichnis: Richten Sie ein Verzeichnis ein, in dem Ihre CAD-Dateien gespeichert werden, und notieren Sie sich den Pfad.

## Namespaces importieren

Importieren Sie in Ihr .NET-Projekt die erforderlichen Namespaces für die Arbeit mit Aspose.CAD. Fügen Sie am Anfang Ihrer Codedatei die folgenden Zeilen hinzu:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

## Schritt 1: Laden Sie das CAD-Bild

 Laden Sie zunächst das CAD-Bild, das Sie als PDF exportieren möchten. Benutzen Sie die`Load` Methode aus der Aspose.CAD-Bibliothek. Ersetzen`"conic_pyramid.dxf"` mit dem Pfad zu Ihrer CAD-Datei.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image cadImage = Image.Load(sourceFilePath))
{
    // Hier finden Sie Ihren Code zum Laden des CAD-Bildes
}
```

## Schritt 2: Rasterisierungsoptionen konfigurieren

 Konfigurieren Sie die Rasterungsoptionen für das CAD-Bild. Legen Sie Parameter wie Seitenbreite, Seitenhöhe und Layouts fest. Kommentieren Sie die entsprechende Zeile aus`TypeOfEntities` wenn Ihre Entitäten 3D sind.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
// rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;

rasterizationOptions.Layouts = new string[] { "Model" };
```

## Schritt 3: PDF-Optionen festlegen

Erstellen Sie PDF-Optionen und verknüpfen Sie sie mit den Rasterisierungsoptionen.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Schritt 4: Als PDF speichern

Speichern Sie das CAD-Bild mit den konfigurierten Optionen als PDF-Datei. Geben Sie den Ausgabepfad für die PDF-Datei an.

```csharp
MyDir = MyDir + "Export3DImagestoPDF_out.pdf";
cadImage.Save(MyDir, pdfOptions);
```

## Abschluss

Glückwunsch! Sie haben 3D-Bilder mit Aspose.CAD für .NET erfolgreich in PDF exportiert. Dieses unkomplizierte Tutorial stellt sicher, dass Sie Ihre CAD-Dateien mühelos in ein besser zugängliches Format konvertieren.

## FAQs

### F1: Ist Aspose.CAD mit allen CAD-Dateiformaten kompatibel?

A1: Ja, Aspose.CAD unterstützt eine Vielzahl von CAD-Formaten und gewährleistet so Flexibilität bei der Handhabung verschiedener Dateitypen.

### F2: Kann ich die Seitenabmessungen beim Exportieren in PDF anpassen?

A2: Absolut. Das Tutorial zeigt, wie Sie die Seitenbreite und -höhe entsprechend Ihren Anforderungen konfigurieren.

### F3: Sind temporäre Lizenzen für Aspose.CAD verfügbar?

 A3: Ja, Sie können temporäre Lizenzen für Aspose.CAD erhalten, indem Sie hier besuchen[Temporäre Lizenz](https://purchase.aspose.com/temporary-license/).

### F4: Wo finde ich zusätzlichen Support oder Community-Diskussionen?

 A4: Gehen Sie zu[Aspose.CAD-Forum](https://forum.aspose.com/c/cad/19) für die Unterstützung und das Engagement in der Gemeinschaft.

### F5: Gibt es eine kostenlose Testversion von Aspose.CAD?

 A5: Ja, Sie können die Funktionen von Aspose.CAD erkunden, indem Sie auf zugreifen[Kostenlose Testphase](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
