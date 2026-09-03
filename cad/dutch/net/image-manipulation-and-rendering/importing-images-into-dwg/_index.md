---
date: 2026-08-17
description: Leer hoe u afbeelding kunt toevoegen aan dwg-bestanden met C# en Aspose.CAD
  voor .NET. Deze gids leidt u door het importeren van afbeeldingen, het instellen
  van invoerpunt(en) en het exporteren naar PDF.
keywords:
- add image to dwg
- convert dwg to pdf
- set insertion point dwg
- embed png in dwg
- save dwg as pdf
lastmod: 2026-08-17
linktitle: Afbeeldingen importeren in DWG-bestanden met C#
og_description: Leer hoe u afbeelding kunt toevoegen aan dwg-bestanden met C#. Deze
  tutorial behandelt het importeren van afbeeldingen, het instellen van invoerpunt(en)
  en het converteren van dwg naar pdf met Aspose.CAD.
og_image_alt: Guide showing C# code to embed an image into a DWG file using Aspose.CAD
og_title: Hoe afbeelding toe te voegen aan dwg-bestanden met C# en Aspose.CAD
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
title: Hoe afbeelding toe te voegen aan dwg-bestanden met C# en Aspose.CAD
url: /nl/net/image-manipulation-and-rendering/importing-images-into-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hoe afbeelding toevoegen aan dwg‑bestanden met C# met Aspose.CAD

## Introductie

Een afbeelding toevoegen aan een DWG‑bestand is een routinematige vereiste wanneer je CAD‑tekeningen wilt verrijken met logo's, foto’s of raster‑graphics. In deze tutorial leer je hoe je **afbeelding aan dwg toevoegt** programmatically met C# en Aspose.CAD voor .NET, en optioneel het resultaat naar PDF converteert. De stappen zijn opgesplitst zodat je elk gedeelte kunt copy‑pasten in je eigen project.

## Snelle antwoorden
- **Welke bibliotheek voert de taak uit?** Aspose.CAD for .NET.
- **Kan ik PNG‑bestanden insluiten?** Ja – PNG, JPEG, BMP en andere rasterformaten worden ondersteund.
- **Heb ik een licentie nodig voor ontwikkeling?** Een gratis proefversie werkt voor testen; een commerciële licentie is vereist voor productie.
- **Wordt PDF‑export ondersteund?** Absoluut – je kunt de bijgewerkte DWG in één regel naar PDF converteren.
- **Welke .NET‑versies zijn compatibel?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7.

## Wat is een DWG‑bestand?

Een DWG‑bestand is het native binaire formaat voor Autodesk AutoCAD‑tekeningen, waarin vectorgeometrie, lagen en metadata worden opgeslagen. Het wordt breed gebruikt in architectuur, engineering en constructie, en Aspose.CAD kan dit formaat lezen en schrijven zonder dat AutoCAD geïnstalleerd hoeft te zijn.

## Waarom afbeelding toevoegen aan dwg met Aspose.CAD?

Aspose.CAD ondersteunt **meer dan 50 invoer‑ en uitvoerformaten**, kan bestanden groter dan 500 MB verwerken zonder het volledige document in het geheugen te laden, en biedt een deterministische API die werkt in headless serveromgevingen. Dit maakt bulk‑verwerking van DWG‑tekeningen snel en betrouwbaar.

## Vereisten
- Basiskennis van C#‑programmeren.
- Aspose.CAD voor .NET geïnstalleerd. Je kunt het downloaden van de [Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/). Je kunt ook andere Aspose‑producten verkennen op de [Aspose releases page](https://releases.aspose.com/).
- Een ontwikkelomgeving zoals Visual Studio 2022 of later.

## Hoe afbeelding toevoegen aan dwg met Aspose.CAD?

Laad het doel‑DWG, maak een raster‑afbeeldingsobject dat de afbeelding beschrijft die je wilt insluiten, stel het invoegpunt en de schaalvectoren in, en voeg vervolgens de afbeelding toe aan de tekening. Sla ten slotte het gewijzigde DWG op of exporteer het direct naar PDF. De volledige workflow vereist slechts een paar API‑aanroepen en duurt minder dan een seconde voor typische 2‑pagina‑tekeningen.

### Namespaces importeren
Voeg de namespaces toe die de CAD‑klassen blootleggen die je nodig hebt.

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

### Stap 1: stel je documentmap in
Bereid de map voor die het bron‑DWG‑bestand en de afbeelding die je wilt insluiten bevat.

```csharp
string MyDir = "Your Document Directory";
```

### Stap 2: laad het dwg‑bestand
De `CadImage`‑klasse vertegenwoordigt een DWG‑tekening en biedt toegang tot de entiteiten, lagen en metadata.

```csharp
string dwgPathToFile = MyDir + "Drawing11.dwg";
CadImage cadImage1 = (CadImage)Image.Load(dwgPathToFile);
```

### Stap 3: definieer de afbeeldings‑eigenschappen
Maak een `Image`‑object dat naar het rasterbestand (bijv. PNG) wijst en specificeer het formaat.

```csharp
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.ObjectHandle = "A3B4";
```

### Stap 4: stel het invoegpunt en de vectoren in voor dwg
Geef op waar de afbeelding in de tekening moet verschijnen en hoe deze moet worden geschaald. Het invoegpunt wordt gedefinieerd door een 2‑D‑coördinaat, terwijl de vectoren de breedte en hoogte bepalen.

```csharp
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

### Stap 5: maak en configureer de rasterafbeelding
Instantieer een `RasterImage`‑object, wijs de afbeeldingsdata toe en stel eventuele extra renderopties in.

```csharp
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.ImageDefReference = "A3B4";
cadRasterImage.DisplayFlags = 7;
cadRasterImage.ClippingState = 0;
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(639.5, 561.5));
```

### Stap 6: afbeelding toevoegen aan dwg‑bestand
Voeg de geconfigureerde rasterafbeelding toe aan de entiteiten‑collectie van de DWG zodat deze onderdeel van de tekening wordt.

```csharp
CadImage cadImage = (CadImage)cadImage1;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadRasterImage);

List<CadBaseObject> list = new List<CadBaseObject>(cadImage.Objects);
list.Add(cadRasterImageDef);
cadImage.Objects = list.ToArray();
```

### Stap 7: opslaan als pdf (exporteer dwg naar pdf)
Na het insluiten van de afbeelding kun je **dwg naar pdf converteren** of **dwg als pdf opslaan** met één enkele aanroep. Dit is handig om de tekening te delen met belanghebbenden die geen CAD‑software hebben.

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

## Hoe dwg naar pdf converteren na het insluiten van een afbeelding?

Roep de `Save`‑methode aan op de `CadImage`‑instantie, waarbij je `SaveFormat.Pdf` doorgeeft en optioneel een `PdfOptions`‑object om paginagrootte, rasterisatie en metadata te regelen. Aspose.CAD behoudt de ingesloten rasterafbeelding, lagen en lijndiktes, en produceert een getrouwe PDF‑representatie die in elke viewer kan worden geopend. Deze conversie wordt uitgevoerd in één regel code.

## Veelvoorkomende problemen en oplossingen
- **Afbeelding verschijnt op de verkeerde locatie** – controleer de coördinaten van het invoegpunt en de richtingsvectoren; ze zijn relatief ten opzichte van de oorsprong van de tekening.
- **Grote afbeeldingen veroorzaken geheugenpieken** – gebruik de `Resize`‑optie op de rasterafbeelding vóór het invoegen, of werk met een lagere resolutie‑kopie.
- **PDF‑export verliest vectorkwaliteit** – zorg ervoor dat je opslaat met `PdfOptions` die vectorgegevens behouden; rasterafbeeldingen worden altijd ingesloten zoals ze zijn.

## Veelgestelde vragen

**Q: Kan ik Aspose.CAD voor .NET gebruiken met andere programmeertalen?**  
A: De kernbibliotheek is .NET‑specifiek, maar Aspose biedt equivalente API’s voor Java, Python en andere platformen.

**Q: Is een gratis proefversie beschikbaar voor Aspose.CAD?**  
A: Ja, je kunt een gratis proefversie verkennen op de [Aspose free trial page](https://releases.aspose.com/).

**Q: Waar kan ik gedetailleerde documentatie vinden voor Aspose.CAD?**  
A: De documentatie is beschikbaar in de [Aspose.CAD .NET API reference](https://reference.aspose.com/cad/net/).

**Q: Hoe verkrijg ik een tijdelijke licentie voor Aspose.CAD?**  
A: Bezoek de [temporary license page](https://purchase.aspose.com/temporary-license/) om een tijdelijke licentie te krijgen.

**Q: Zijn er community‑forums voor Aspose.CAD‑ondersteuning?**  
A: Ja, je kunt ondersteuning zoeken en deelnemen aan de community in het [Aspose.CAD community forum](https://forum.aspose.com/c/cad/19).

---

**Last Updated:** 2026-08-17  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose

## Gerelateerde tutorials

- [DWG exporteren naar PDF of rasterafbeeldingen - Aspose.CAD-gids](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [DWG exporteren naar DXF-formaat in C# - Aspose.CAD-tutorial](/cad/net/advanced-export-techniques/exporting-dwg-to-dxf/)
- [Specifieke lay-outs exporteren naar PDF - Aspose.CAD-gids](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}