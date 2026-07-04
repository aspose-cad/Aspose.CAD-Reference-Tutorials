---
date: 2026-07-04
description: Erfahren Sie, wie Sie die PDF‑Seitengröße festlegen und PDFs aus 3D‑CAD‑Bildern
  mit Aspose.CAD für .NET exportieren – eine Schritt‑für‑Schritt‑Anleitung zum Konvertieren
  von DWG in PDF und zum Speichern von CAD als PDF.
keywords:
- set pdf page size
- export pdf from cad
- convert dwg to pdf
- save cad as pdf
- cad to pdf tutorial
linktitle: Exportieren von 3D‑Bildern in PDF
schemas:
- author: Aspose
  dateModified: '2026-07-04'
  description: Learn how to set PDF page size and export PDF from 3D CAD images using
    Aspose.CAD for .NET – a step‑by‑step guide to convert DWG to PDF and save CAD
    as PDF.
  headline: Set PDF page size – Export 3D Images to PDF with Aspose.CAD
  type: TechArticle
- description: Learn how to set PDF page size and export PDF from 3D CAD images using
    Aspose.CAD for .NET – a step‑by‑step guide to convert DWG to PDF and save CAD
    as PDF.
  name: Set PDF page size – Export 3D Images to PDF with Aspose.CAD
  steps:
  - name: Load the CAD Image
    text: '`Image` class represents a CAD drawing loaded into memory, ready for rasterization.'
  - name: Configure Rasterization Options (Save CAD as PDF)
    text: '`RasterizationOptions` class defines how the CAD data is rasterized, including
      page size, DPI, and whether 3‑D entities are rendered.'
  - name: Set PDF Options (Create PDF from CAD)
    text: '`PdfOptions` class holds the output format settings and links the rasterization
      options to PDF generation.'
  - name: Save as PDF (Generate PDF from 3D Model)
    text: '`Save` method on the `Image` object writes the rasterized content to the
      specified PDF file, producing a ready‑to‑share document.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD supports more than 50 input and output formats, including
      DWG, DXF, DGN, STL, and IFC, ensuring flexibility for any project.
    question: Is Aspose.CAD compatible with all CAD file formats?
  - answer: Absolutely. Set `PageWidth` and `PageHeight` in `RasterizationOptions`
      to any size in points, inches, or millimetres before calling `Save`.
    question: Can I customize the page dimensions when exporting to PDF?
  - answer: Yes, you can obtain temporary licenses for Aspose.CAD by visiting [Temporary
      License](https://purchase.aspose.com/temporary-license/).
    question: Are temporary licenses available for Aspose.CAD?
  - answer: Head to the [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) for
      expert help and peer‑to‑peer advice.
    question: Where can I find additional support or community discussions?
  - answer: Yes, you can explore the features of Aspose.CAD by accessing the [free
      trial](https://releases.aspose.com/).
    question: Is there a free trial version of Aspose.CAD?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: PDF‑Seitengröße festlegen – 3D‑Bilder in PDF exportieren mit Aspose.CAD
url: /de/net/3d-image-export/exporting-3d-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportieren von 3D-Bildern nach PDF – Aspose.CAD Tutorial

## Einleitung

Wenn Sie die **PDF-Seitengröße festlegen** müssen, während Sie eine 3‑D-CAD-Zeichnung in PDF konvertieren, sind Sie hier genau richtig. Dieses Tutorial zeigt Ihnen Schritt für Schritt, wie Sie eine CAD-Datei laden, Rasterisierungsoptionen konfigurieren – einschließlich benutzerdefinierter Seitengrößen – und ein hochqualitatives PDF mit Aspose.CAD für .NET erzeugen. Am Ende können Sie **PDF aus CAD exportieren**, **CAD als PDF speichern** und jedes Layout-Detail steuern, ohne AutoCAD zu installieren.

## Schnelle Antworten
- **Was bedeutet „PDF aus CAD exportieren“?** Es konvertiert eine CAD-Zeichnung (DWG, DXF, DGN usw.) in ein PDF, das auf jedem Gerät geöffnet werden kann.  
- **Welche Bibliothek führt die Konvertierung durch?** Aspose.CAD for .NET bietet Rasterisierung und PDF-Export ohne externe Abhängigkeiten.  
- **Benötige ich eine Lizenz?** Für die Produktion ist eine temporäre oder vollständige Lizenz erforderlich; eine kostenlose Testversion ist verfügbar.  
- **Kann ich benutzerdefinierte Seitengrößen festlegen?** Ja – verwenden Sie `PageWidth` und `PageHeight` in `RasterizationOptions`.  
- **Wird die 3‑D-Geometrie beibehalten?** Die 3‑D-Entitäten werden gerastert; aktivieren Sie `TypeOfEntities.Entities3D` für vollständige 3‑D-Unterstützung.

## Was bedeutet „PDF exportieren“ im Kontext von CAD?

Das Exportieren von PDF aus CAD bedeutet, eine CAD-Zeichnung (DWG, DXF, DGN usw.) zu nehmen und sie in eine PDF-Datei zu konvertieren, die Vektorgrafiken, gerasterte 3‑D-Ansichten und präzise Seitenlayout-Informationen enthalten kann, sodass sie leicht mit Personen geteilt werden kann, die keine CAD-Software besitzen.

## Warum Aspose.CAD zum PDF-Export verwenden?

Aspose.CAD lässt Sie **PDF-Seitengröße festlegen** und PDFs vollständig in verwaltetem .NET-Code exportieren. Es unterstützt über 50 CAD-Formate, verarbeitet Dateien bis zu 2 GB, ohne das gesamte Dokument in den Speicher zu laden, und bewahrt Linienstärken, Farben sowie optionale 3‑D-Entitätsdarstellung mit einer Rasterisierungs‑DPI von bis zu 1200. Die Bibliothek läuft unter Windows, Linux und macOS, sodass die erzeugten PDFs auf jeder Plattform funktionieren.

## Voraussetzungen

- **Aspose.CAD for .NET** installiert. Laden Sie es von der [Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/) herunter.  
- Ein Ordner, der die CAD-Dateien enthält, die Sie konvertieren möchten (z. B. `C:\CAD\`).  
- .NET 6.0 oder höher (oder .NET Framework 4.7.2).  

## Namespaces importieren

`using`‑Anweisungen importieren die für die Arbeit mit Rasterisierungs‑ und PDF-Optionen benötigten Aspose.CAD-Namespaces.  

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

## Schritt‑für‑Schritt‑Anleitung

### Wie legt man die PDF-Seitengröße fest, wenn man CAD nach PDF exportiert?

Laden Sie Ihre CAD-Datei, konfigurieren Sie die Seitengrößen in `RasterizationOptions`, binden Sie diese Optionen an eine `PdfOptions`‑Instanz und rufen Sie `Save` auf. Dieser vierstufige Ablauf gibt Ihnen volle Kontrolle über Größe und Qualität der Ausgabe, während der Code kompakt bleibt.

### Schritt 1: CAD-Bild laden

`Image`‑Klasse repräsentiert eine CAD-Zeichnung, die in den Speicher geladen wurde und bereit für die Rasterisierung ist.  

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image cadImage = Image.Load(sourceFilePath))
{
    // Your code for loading the CAD image goes here
}
```

### Schritt 2: Rasterisierungsoptionen konfigurieren (CAD als PDF speichern)

`RasterizationOptions`‑Klasse definiert, wie die CAD-Daten gerastert werden, einschließlich Seitengröße, DPI und ob 3‑D‑Entitäten gerendert werden.  

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
// rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;

rasterizationOptions.Layouts = new string[] { "Model" };
```

### Schritt 3: PDF-Optionen festlegen (PDF aus CAD erstellen)

`PdfOptions`‑Klasse enthält die Einstellungen für das Ausgabeformat und verknüpft die Rasterisierungsoptionen mit der PDF-Erzeugung.  

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### Schritt 4: Als PDF speichern (PDF aus 3D-Modell erzeugen)

`Save`‑Methode des `Image`‑Objekts schreibt den gerasterten Inhalt in die angegebene PDF‑Datei und erzeugt ein sofort teilbares Dokument.  

```csharp
MyDir = MyDir + "Export3DImagestoPDF_out.pdf";
cadImage.Save(MyDir, pdfOptions);
```

## Häufige Probleme und Lösungen

| Problem | Grund | Lösung |
|-------|--------|-----|
| **Ausgabe-PDF ist leer** | Falscher Layout-Name oder fehlendes `Model`-Layout. | Stellen Sie sicher, dass `rasterizationOptions.Layouts` einem im CAD‑File vorhandenen Layout entspricht. |
| **Niedrige Auflösung** | Standard‑Rasterisierungs‑DPI ist niedrig. | Setzen Sie `rasterizationOptions.Resolution = 300;` vor dem Speichern. |
| **3‑D-Entitäten werden nicht angezeigt** | `TypeOfEntities` ist auskommentiert. | Entkommentieren Sie `rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;`. |
| **Lizenzausnahme** | Verwendung einer Testversion ohne Lizenz. | Wenden Sie eine temporäre oder permanente Lizenz an via `License license = new License(); license.SetLicense("Aspose.CAD.lic");`. |

## Häufig gestellte Fragen

**Q: Ist Aspose.CAD mit allen CAD-Dateiformaten kompatibel?**  
A: Ja, Aspose.CAD unterstützt mehr als 50 Eingabe‑ und Ausgabeformate, einschließlich DWG, DXF, DGN, STL und IFC, und bietet damit Flexibilität für jedes Projekt.

**Q: Kann ich die Seitengrößen beim Export nach PDF anpassen?**  
A: Absolut. Setzen Sie `PageWidth` und `PageHeight` in `RasterizationOptions` auf jede gewünschte Größe in Punkten, Zoll oder Millimetern, bevor Sie `Save` aufrufen.

**Q: Sind temporäre Lizenzen für Aspose.CAD verfügbar?**  
A: Ja, Sie können temporäre Lizenzen für Aspose.CAD erhalten, indem Sie die Seite [Temporary License](https://purchase.aspose.com/temporary-license/) besuchen.

**Q: Wo finde ich zusätzlichen Support oder Community‑Diskussionen?**  
A: Gehen Sie zum [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) für Expertenhilfe und Peer‑to‑Peer‑Ratschläge.

**Q: Gibt es eine kostenlose Testversion von Aspose.CAD?**  
A: Ja, Sie können die Funktionen von Aspose.CAD erkunden, indem Sie die [free trial](https://releases.aspose.com/) nutzen.

## Fazit

Sie haben nun eine vollständige, produktionsreife Methode, um **PDF-Seitengröße festzulegen** und **PDF aus 3D-CAD-Bildern zu exportieren** mit Aspose.CAD für .NET. Durch Anpassen der Rasterisierungsoptionen können Sie Auflösung, Seitenlayout und 3‑D‑Entitätsdarstellung feinjustieren, um jede Dokumentationsanforderung zu erfüllen. Experimentieren Sie mit verschiedenen DPI‑Einstellungen und Seitengrößen, um das optimale Gleichgewicht zwischen Dateigröße und visueller Treue zu erreichen.

{{< blocks/products/products-backtop-button >}}

## Verwandte Tutorials

- [Exportieren spezifischer Layouts nach PDF – Aspose.CAD Leitfaden](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)
- [Exportieren von DWG nach PDF oder Rasterbildern – Aspose.CAD Leitfaden](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [Export von DGN nach PDF in Aspose.CAD für .NET](/cad/net/cad-export-formats/export-dgn-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

--- 

**Zuletzt aktualisiert:** 2026-07-04  
**Getestet mit:** Aspose.CAD 24.11 for .NET  
**Autor:** Aspose