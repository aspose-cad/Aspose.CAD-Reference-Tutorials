---
date: 2026-08-12
description: Text aus DWG extrahieren und ein bestimmtes DWG in ein Bild konvertieren
  in C# mit Aspose.CAD für .NET. Lernen Sie Schritt für Schritt mit Code‑Beispielen.
keywords:
- extract text from dwg
- convert specific dwg to image
- Aspose.CAD .NET
lastmod: 2026-08-12
linktitle: Konvertierung eines bestimmten DWG in ein Bild in C#
og_description: Text aus DWG extrahieren und ein bestimmtes DWG in ein Bild konvertieren
  in C# mit Aspose.CAD. Folgen Sie diesem kurzen Leitfaden für eine schnelle Implementierung.
og_image_alt: Guide showing DWG to image conversion and text extraction using Aspose.CAD
  in C#
og_title: Text aus DWG extrahieren und ein bestimmtes DWG in ein Bild konvertieren
  in C#
schemas:
- author: Aspose
  dateModified: '2026-08-12'
  description: Extract text from DWG and convert specific DWG to image in C# using
    Aspose.CAD for .NET. Learn step‑by‑step with code snippets.
  headline: Extract text from DWG and convert specific DWG to image in C#
  type: TechArticle
- questions:
  - answer: Aspose.CAD supports DWG releases from AutoCAD 2000 up to the latest 2024
      version, covering over 90 % of files created in the field.
    question: Is Aspose.CAD compatible with all versions of DWG files?
  - answer: Yes – you can change resolution, image format, anti‑aliasing, and background
      color to suit PNG, JPEG, or PDF targets.
    question: Can I customize the rasterization options for different outputs?
  - answer: Explore the comprehensive [Aspose.CAD documentation](https://reference.aspose.com/cad/net/)
      for more code samples and API details.
    question: Where can I find additional examples and documentation?
  - answer: Absolutely – you can download a trial version on the **[Aspose trial download
      page](https://releases.aspose.com/)** and evaluate all features without restrictions
      for 30 days.
    question: Is there a free trial available for Aspose.CAD?
  - answer: Join the active [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)
      where developers share solutions and the Aspose team answers questions.
    question: How can I get support or connect with the community?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- extract text from dwg
- Aspose.CAD
- C# CAD processing
title: Text aus DWG extrahieren und ein bestimmtes DWG in ein Bild konvertieren in
  C#
url: /de/net/image-manipulation-and-rendering/converting-particular-dwg-to-image/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konvertieren bestimmter DWG in ein Bild in C# – Aspose.CAD‑Leitfaden

## Einführung

In modernen Ingenieur‑Anwendungen müssen Sie häufig **Text aus DWG**‑Dateien extrahieren und **bestimmte DWG in Bild**‑Formate konvertieren für Berichte oder Visualisierungen. Aspose.CAD für .NET bietet Ihnen eine voll ausgestattete API, die beide Aufgaben erledigt, ohne dass externe CAD‑Software erforderlich ist. In diesem Tutorial lernen Sie, wie Sie ein DWG laden, nach Textelementen filtern, die Zeichnung rasterisieren und schließlich das Ergebnis als PDF‑Bild speichern – alles in sauberem C#‑Code.

## Schnelle Antworten
- **Was ist der erste Schritt?** Laden Sie die DWG‑Datei mit `new CadImage("file.dwg")`.  
- **Welche Klasse filtert Text?** Verwenden Sie `CadEntityFilter`, um `Text`‑Entitäten auszuwählen.  
- **Wie definieren Sie die Bildgröße?** Setzen Sie `Width` und `Height` in `CadRasterizationOptions`.  
- **Welches Ausgabeformat wird verwendet?** Das Beispiel speichert als PDF, das das Rasterbild einbettet.  
- **Benötige ich eine Lizenz für die Produktion?** Ja – eine kommerzielle Aspose.CAD‑Lizenz entfernt die Evaluationsbeschränkungen.

## Wie extrahiere ich Text aus DWG?

Laden Sie das DWG, wenden Sie einen Filter an, der nur Textelemente auswählt, und lesen Sie anschließend die `TextString`‑Eigenschaft jedes Elements. Dieser Ansatz gibt jedes Anmerkungs‑, Beschriftungs‑ oder Maßtextstück zurück, das in der Zeichnung vorhanden ist, sodass Sie es für Suche, Indexierung oder Berichterstellung wiederverwenden können.

## Warum ein bestimmtes DWG in ein Bild konvertieren?

Das Konvertieren eines DWG in ein Rasterbild ermöglicht es Ihnen, die Zeichnung in Dokumente, Webseiten oder mobile Apps einzubetten, die native CAD‑Formate nicht rendern können. Aspose.CAD verarbeitet **über 50 CAD‑Formate** und kann mehrhundertseitige Zeichnungen rasterisieren, wobei weniger als 200  MB Speicher verbraucht werden, was es für hochdurchsatz‑Server‑Szenarien geeignet macht.

## Voraussetzungen

- Visual Studio (beliebige aktuelle Edition) zum Kompilieren und Ausführen von C#‑Projekten.  
- Aspose.CAD für .NET – stellen Sie sicher, dass die Bibliothek installiert ist. Den Download‑Link finden Sie auf der **[Aspose.CAD für .NET Download‑Seite](https://releases.aspose.com/cad/net/)**.  
- Eine DWG‑Datei, mit der Sie arbeiten möchten; die Beispieldatei *visualization_-_conference_room.dwg* wird in den Code‑Snippets verwendet.

## Namespaces importieren

The following namespaces give you access to the core CAD classes, rasterization options, and PDF output helpers:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Schritt 1: DWG‑Datei laden

Create a `CadImage` instance by passing the path of your DWG file. The `CadImage` object represents the entire drawing in memory and provides access to its layers, entities, and metadata.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
var cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath);
```

## Schritt 2: Entitäten filtern

`CadEntityFilter` lets you pick only the entities you need. In this guide we configure it to keep **text** objects, discarding lines, circles, and other geometry that you don’t want in the final image.

```csharp
CadBaseEntity[] entities = cadImage.Entities;
List<CadBaseEntity> filteredEntities = new List<CadBaseEntity>();

foreach (CadBaseEntity baseEntity in entities)
{
    // Selection or filtration of entities
    if (baseEntity.TypeName == CadEntityTypeName.TEXT)
    {
        filteredEntities.Add(baseEntity);
    }
}

cadImage.Entities = filteredEntities.ToArray();
```

## Schritt 3: Rasterisierungsoptionen festlegen

`CadRasterizationOptions` controls how the drawing is turned into a bitmap. You can define the output size, background color, and resolution (DPI). The following definition anchor introduces the class:

The `CadRasterizationOptions` class specifies image dimensions, resolution, and rendering settings for converting CAD drawings to raster formats.  

Set the desired width, height, and background color before passing the options to the PDF exporter.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions =
    new Aspose.CAD.ImageOptions.CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
```

## Schritt 4: PDF‑Optionen festlegen

`PdfOptions` bundles the rasterization settings with PDF‑specific features such as compression. The definition anchor for this class appears first:

`PdfOptions` encapsulates PDF‑generation parameters, including the rasterization options that dictate how CAD data is rendered inside the PDF document.  

Assign the previously created `CadRasterizationOptions` instance to the `VectorRasterizationOptions` property.

```csharp
Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Schritt 5: Als PDF speichern

Finally, call the `Save` method on the `CadImage` object, passing the target file name and the configured `PdfOptions`. The PDF will contain a high‑quality image of the filtered drawing.

```csharp
string outFile = MyDir + "result_out_generated.pdf";
cadImage.Save(outFile, pdfOptions);
```

## Häufige Probleme und Fehlersuche

- **Fehlender Text nach dem Filtern** – Stellen Sie sicher, dass das DWG tatsächlich `Text`‑Entitäten enthält; einige Zeichnungen speichern Anmerkungen als `MText`. Passen Sie den Filter an, um `MText` einzuschließen, falls nötig.  
- **Leeres Ausgabebild** – Überprüfen Sie, ob die Rasterisierungs‑DPI hoch genug ist (300 DPI ist ein sicherer Standard) und dass die Hintergrundfarbe beim Betrachten des PDFs nicht auf transparent gesetzt ist.  
- **Out‑of‑Memory‑Fehler bei großen Dateien** – Verwenden Sie die Überladung von `LoadOptions`, die Streaming ermöglicht, wodurch verhindert wird, dass die gesamte Datei gleichzeitig in den Speicher geladen wird.

## Häufig gestellte Fragen

**F: Ist Aspose.CAD mit allen Versionen von DWG‑Dateien kompatibel?**  
A: Aspose.CAD unterstützt DWG‑Versionen von AutoCAD 2000 bis zur neuesten Version 2024 und deckt über 90 % der im Feld erstellten Dateien ab.

**F: Kann ich die Rasterisierungsoptionen für verschiedene Ausgaben anpassen?**  
A: Ja – Sie können Auflösung, Bildformat, Anti‑Aliasing und Hintergrundfarbe ändern, um PNG-, JPEG‑ oder PDF‑Ziele zu unterstützen.

**F: Wo finde ich weitere Beispiele und Dokumentation?**  
A: Durchsuchen Sie die umfassende [Aspose.CAD‑Dokumentation](https://reference.aspose.com/cad/net/) für weitere Code‑Beispiele und API‑Details.

**F: Gibt es eine kostenlose Testversion von Aspose.CAD?**  
A: Auf jeden Fall – Sie können eine Testversion auf der **[Aspose‑Test‑Download‑Seite](https://releases.aspose.com/)** herunterladen und alle Funktionen 30 Tage lang uneingeschränkt testen.

**F: Wie kann ich Support erhalten oder mit der Community in Kontakt treten?**  
A: Treten Sie dem aktiven [Aspose.CAD‑Forum](https://forum.aspose.com/c/cad/19) bei, wo Entwickler Lösungen teilen und das Aspose‑Team Fragen beantwortet.

---

**Zuletzt aktualisiert:** 2026-08-12  
**Getestet mit:** Aspose.CAD 24.11 für .NET  
**Autor:** Aspose

## Verwandte Tutorials

- [Suche nach Text in DWG‑Dateien mit C# – Aspose.CAD‑Tutorial](/cad/net/text-search-and-manipulation/searching-text-in-dwg-files/)
- [CAD‑Zeichnung in Rasterbild konvertieren in Aspose.CAD für .NET](/cad/net/cad-drawing-manipulation/convert-cad-drawing-to-raster-image/)
- [DWG‑Dokumente in C# rendern – Aspose.CAD‑Leitfaden](/cad/net/image-manipulation-and-rendering/rendering-dwg-documents/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}