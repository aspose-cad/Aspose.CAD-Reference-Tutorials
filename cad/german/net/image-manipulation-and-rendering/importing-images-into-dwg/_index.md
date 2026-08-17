---
date: 2026-08-17
description: Erfahren Sie, wie Sie mit C# und Aspose.CAD für .NET ein Bild zu DWG-Dateien
  hinzufügen. Dieser Leitfaden führt Sie durch das Importieren von Bildern, das Festlegen
  von Einfügepunkten und das Exportieren in PDF.
keywords:
- add image to dwg
- convert dwg to pdf
- set insertion point dwg
- embed png in dwg
- save dwg as pdf
lastmod: 2026-08-17
linktitle: Importieren von Bildern in DWG-Dateien mit C#
og_description: Erfahren Sie, wie Sie mit C# ein Bild zu DWG-Dateien hinzufügen. Dieses
  Tutorial behandelt das Importieren von Bildern, das Festlegen von Einfügepunkten
  und das Konvertieren von DWG zu PDF mit Aspose.CAD.
og_image_alt: Guide showing C# code to embed an image into a DWG file using Aspose.CAD
og_title: Wie man ein Bild zu DWG-Dateien mit C# und Aspose.CAD hinzufügt
schemas:
- author: Aspose
  dateModified: '2026-08-17'
  description: Learn how to add image to dwg files using C# and Aspose.CAD for .NET.
    This guide walks you through importing images, setting insertion points, and exporting
    to PDF.
  headline: How to add image to dwg files with C# using Aspose.CAD
  type: TechArticle
- description: Learn how to add image to dwg files using C# and Aspose.CAD for .NET.
    This guide walks you through importing images, setting insertion points, and exporting
    to PDF.
  name: How to add image to dwg files with C# using Aspose.CAD
  steps:
  - name: set up your document directory
    text: Prepare the folder that contains the source DWG and the image you want to
      embed.
  - name: load the dwg file
    text: The `CadImage` class represents a DWG drawing and provides access to its
      entities, layers, and metadata.
  - name: define the image properties
    text: Create an `Image` object that points to the raster file (e.g., PNG) and
      specify its format.
  - name: set insertion point dwg and vectors
    text: Specify where the image should appear inside the drawing and how it should
      be scaled. The insertion point is defined by a 2‑D coordinate, while the vectors
      control width and height.
  - name: create and configure the raster image
    text: Instantiate a `RasterImage` object, assign the image data, and set any additional
      rendering options.
  - name: add image to dwg file
    text: Insert the configured raster image into the DWG’s entities collection so
      it becomes part of the drawing.
  - name: save as pdf (export dwg to pdf)
    text: After embedding the image you can **convert dwg to pdf** or **save dwg as
      pdf** with a single call. This is useful for sharing the drawing with stakeholders
      who don’t have CAD software.
  type: HowTo
- questions:
  - answer: The core library is .NET‑specific, but Aspose offers equivalent APIs for
      Java, Python and other platforms.
    question: Can I use Aspose.CAD for .NET with other programming languages?
  - answer: Yes, you can explore a free trial on the [Aspose free trial page](https://releases.aspose.com/).
    question: Is a free trial available for Aspose.CAD?
  - answer: The documentation is available in the [Aspose.CAD .NET API reference](https://reference.aspose.com/cad/net/).
    question: Where can I find detailed documentation for Aspose.CAD?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to get a temporary license.
    question: How do I obtain a temporary license for Aspose.CAD?
  - answer: Yes, you can seek support and engage with the community in the [Aspose.CAD
      community forum](https://forum.aspose.com/c/cad/19).
    question: Are there community forums for Aspose.CAD support?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- CAD
- Aspose.CAD
- C# image processing
- DWG manipulation
title: Wie man ein Bild zu DWG-Dateien mit C# und Aspose.CAD hinzufügt
url: /de/net/image-manipulation-and-rendering/importing-images-into-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Wie man ein Bild zu DWG-Dateien mit C# und Aspose.CAD hinzufügt

## Einführung

Ein Bild zu einer DWG-Datei hinzuzufügen ist eine gängige Anforderung, wenn Sie CAD-Zeichnungen mit Logos, Fotos oder Rastergrafiken anreichern müssen. In diesem Tutorial lernen Sie, wie Sie **add image to dwg** programmgesteuert mit C# und Aspose.CAD für .NET hinzufügen und optional das Ergebnis in PDF konvertieren. Die Schritte sind aufgeteilt, sodass Sie jeden Abschnitt in Ihr eigenes Projekt kopieren‑und‑einfügen können.

## Schnelle Antworten
- **Welche Bibliothek erledigt die Aufgabe?** Aspose.CAD for .NET.
- **Kann ich PNG-Dateien einbetten?** Ja – PNG, JPEG, BMP und andere Rasterformate werden unterstützt.
- **Benötige ich eine Lizenz für die Entwicklung?** Eine kostenlose Testversion funktioniert für Tests; für die Produktion ist eine kommerzielle Lizenz erforderlich.
- **Wird der PDF-Export unterstützt?** Absolut – Sie können das aktualisierte DWG mit einer Zeile in PDF konvertieren.
- **Welche .NET-Versionen sind kompatibel?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7.

## Was ist eine DWG-Datei?

Eine DWG-Datei ist das native Binärformat für Autodesk AutoCAD‑Zeichnungen und speichert Vektorgeometrie, Ebenen und Metadaten. Sie wird in Architektur, Ingenieurwesen und Bauwesen weit verbreitet eingesetzt, und Aspose.CAD kann dieses Format lesen und schreiben, ohne dass AutoCAD installiert sein muss.

## Warum ein Bild zu DWG mit Aspose.CAD hinzufügen?

Aspose.CAD unterstützt **über 50 Eingabe‑ und Ausgabeformate**, kann Dateien größer als 500 MB verarbeiten, ohne das gesamte Dokument in den Speicher zu laden, und bietet eine deterministische API, die in headless Server‑Umgebungen funktioniert. Das macht die Massenverarbeitung von DWG‑Zeichnungen schnell und zuverlässig.

## Voraussetzungen
- Grundkenntnisse in C#‑Programmierung.
- Aspose.CAD für .NET installiert. Sie können es von der [Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/) herunterladen. Weitere Aspose‑Produkte finden Sie auf der [Aspose releases page](https://releases.aspose.com/).
- Eine Entwicklungsumgebung wie Visual Studio 2022 oder neuer.

## Wie man ein Bild zu DWG mit Aspose.CAD hinzufügt?

Laden Sie das Ziel‑DWG, erstellen Sie ein Rasterbild‑Objekt, das das einzubettende Bild beschreibt, setzen Sie den Einfügepunkt und die Skalierungsvektoren und fügen Sie das Bild dann der Zeichnung hinzu. Abschließend speichern Sie das modifizierte DWG oder exportieren es direkt nach PDF. Der gesamte Workflow erfordert nur wenige API‑Aufrufe und läuft bei typischen 2‑Seiten‑Zeichnungen in weniger als einer Sekunde.

### Namespaces importieren
Binden Sie die Namespaces ein, die die CAD‑Klassen bereitstellen, die Sie benötigen.

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

### Schritt 1: Dokumentverzeichnis einrichten
Bereiten Sie den Ordner vor, der das Quell‑DWG und das Bild, das Sie einbetten möchten, enthält.

```csharp
string MyDir = "Your Document Directory";
```

### Schritt 2: DWG-Datei laden
Die Klasse `CadImage` repräsentiert eine DWG‑Zeichnung und bietet Zugriff auf ihre Entitäten, Ebenen und Metadaten.

```csharp
string dwgPathToFile = MyDir + "Drawing11.dwg";
CadImage cadImage1 = (CadImage)Image.Load(dwgPathToFile);
```

### Schritt 3: Bildeigenschaften definieren
Erstellen Sie ein `Image`‑Objekt, das auf die Rasterdatei (z. B. PNG) verweist, und geben Sie dessen Format an.

```csharp
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.ObjectHandle = "A3B4";
```

### Schritt 4: Einfügepunkt und Vektoren festlegen
Geben Sie an, wo das Bild in der Zeichnung erscheinen soll und wie es skaliert werden soll. Der Einfügepunkt wird durch eine 2‑D‑Koordinate definiert, während die Vektoren Breite und Höhe steuern.

```csharp
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

### Schritt 5: Rasterbild erstellen und konfigurieren
Instanziieren Sie ein `RasterImage`‑Objekt, weisen Sie die Bilddaten zu und setzen Sie zusätzliche Rendering‑Optionen.

```csharp
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.ImageDefReference = "A3B4";
cadRasterImage.DisplayFlags = 7;
cadRasterImage.ClippingState = 0;
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(639.5, 561.5));
```

### Schritt 6: Bild zur DWG-Datei hinzufügen
Fügen Sie das konfigurierte Rasterbild in die Entitäten‑Sammlung des DWG ein, sodass es Teil der Zeichnung wird.

```csharp
CadImage cadImage = (CadImage)cadImage1;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadRasterImage);

List<CadBaseObject> list = new List<CadBaseObject>(cadImage.Objects);
list.Add(cadRasterImageDef);
cadImage.Objects = list.ToArray();
```

### Schritt 7: Als PDF speichern (DWG nach PDF exportieren)
Nach dem Einbetten des Bildes können Sie **convert dwg to pdf** oder **save dwg as pdf** mit einem einzigen Aufruf durchführen. Das ist nützlich, um die Zeichnung mit Interessengruppen zu teilen, die keine CAD‑Software besitzen.

```csharp
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;

cadRasterizationOptions.PageHeight = 1600;
cadRasterizationOptions.PageWidth = 1600;
cadRasterizationOptions.Layouts = new string[] { "Model" };
cadImage1.Save(MyDir + "export2.pdf", pdfOptions);
```

## Wie man DWG nach dem Einbetten eines Bildes in PDF konvertiert?

Rufen Sie die `Save`‑Methode der `CadImage`‑Instanz auf, übergeben Sie `SaveFormat.Pdf` und optional ein `PdfOptions`‑Objekt, um Seitengröße, Rasterung und Metadaten zu steuern. Aspose.CAD bewahrt das eingebettete Rasterbild, Ebenen und Linienstärken und erzeugt eine getreue PDF‑Darstellung, die in jedem Viewer geöffnet werden kann. Diese Konvertierung erfolgt in einer einzigen Codezeile.

## Häufige Probleme und Lösungen
- **Bild erscheint an falscher Stelle** – überprüfen Sie die Koordinaten des Einfügepunkts und die Richtungsvektoren; sie sind relativ zum Ursprung der Zeichnung.
- **Große Bilder verursachen Speicherspitzen** – verwenden Sie die `Resize`‑Option beim Rasterbild vor dem Einfügen oder arbeiten Sie mit einer Kopie niedrigerer Auflösung.
- **PDF‑Export verliert Vektorqualität** – stellen Sie sicher, dass Sie mit `PdfOptions` speichern, die Vektordaten erhalten; Rasterbilder werden immer unverändert eingebettet.

## Häufig gestellte Fragen

**Q: Kann ich Aspose.CAD für .NET mit anderen Programmiersprachen verwenden?**  
A: Die Kernbibliothek ist .NET‑spezifisch, aber Aspose bietet gleichwertige APIs für Java, Python und andere Plattformen.

**Q: Gibt es eine kostenlose Testversion für Aspose.CAD?**  
A: Ja, Sie können eine kostenlose Testversion auf der [Aspose free trial page](https://releases.aspose.com/) erkunden.

**Q: Wo finde ich die detaillierte Dokumentation für Aspose.CAD?**  
A: Die Dokumentation ist verfügbar in der [Aspose.CAD .NET API reference](https://reference.aspose.com/cad/net/).

**Q: Wie erhalte ich eine temporäre Lizenz für Aspose.CAD?**  
A: Besuchen Sie die [temporary license page](https://purchase.aspose.com/temporary-license/), um eine temporäre Lizenz zu erhalten.

**Q: Gibt es Community-Foren für den Aspose.CAD‑Support?**  
A: Ja, Sie können Unterstützung suchen und sich mit der Community im [Aspose.CAD community forum](https://forum.aspose.com/c/cad/19) austauschen.

---

**Zuletzt aktualisiert:** 2026-08-17  
**Getestet mit:** Aspose.CAD 24.11 für .NET  
**Autor:** Aspose

## Verwandte Tutorials

- [Exportieren von DWG zu PDF oder Rasterbildern – Aspose.CAD‑Leitfaden](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [Exportieren von DWG in das DXF-Format in C# – Aspose.CAD‑Tutorial](/cad/net/advanced-export-techniques/exporting-dwg-to-dxf/)
- [Exportieren spezifischer Layouts nach PDF – Aspose.CAD‑Leitfaden](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}