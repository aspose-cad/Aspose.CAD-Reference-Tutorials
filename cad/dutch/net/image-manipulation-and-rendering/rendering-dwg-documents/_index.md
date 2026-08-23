---
date: 2026-08-23
description: Leer hoe u een viewport dwg c# maakt met Aspose.CAD. Deze gids behandelt
  het laden van een DWG‑bestand, het configureren van rasterisatie, het definiëren
  van een viewport en het opslaan van het resultaat als PDF.
keywords:
- create viewport dwg c#
- render dwg c#
- aspose.cad .net
lastmod: 2026-08-23
linktitle: DWG-documenten renderen in C#
og_description: Leer hoe u een viewport dwg c# maakt met Aspose.CAD in .NET. Deze
  stapsgewijze gids toont het laden, rasteriseren, definiëren van viewports en opslaan
  naar PDF.
og_image_alt: Guide showing how to create viewport dwg c# with Aspose.CAD in .NET
og_title: Hoe een viewport dwg c# te maken met Aspose.CAD voor .NET
schemas:
- author: Aspose
  dateModified: '2026-08-23'
  description: Learn how to create viewport dwg c# using Aspose.CAD. This guide covers
    loading a DWG file, configuring rasterization, defining a viewport, and saving
    the result as PDF.
  headline: How to create viewport dwg c# with Aspose.CAD for .NET
  type: TechArticle
- questions:
  - answer: Load the DWG file with `CadImage.Load`.
    question: What is the first step?
  - answer: '`Viewport` inside `CadRasterizationOptions`.'
    question: Which class defines the view area?
  - answer: Yes, using `PdfOptions` after rasterization.
    question: Can I output to PDF?
  - answer: A commercial license is required; a free trial works for evaluation.
    question: Do I need a license for production?
  - answer: Absolutely – Aspose.CAD works with .NET Framework, .NET Core, and .NET 5/6.
    question: Is .NET Core supported?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- create viewport dwg c#
- Aspose.CAD
- C# CAD rendering
- DWG to PDF
- CAD viewports
title: Hoe een viewport dwg c# te maken met Aspose.CAD voor .NET
url: /nl/net/image-manipulation-and-rendering/rendering-dwg-documents/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG-documenten renderen in C# – viewport dwg c# tutorial maken

## Introductie

In deze uitgebreide tutorial leer je hoe je **viewport dwg c#** kunt maken met Aspose.CAD en een DWG‑bestand naar PDF rendert. Of je nu een specifieke lay-out wilt extraheren, een afdrukbare bladzijde wilt genereren, of een CAD‑weergave in een rapport wilt embedden, het controleren van de viewport geeft je precieze renderingscontrole. Aspose.CAD ondersteunt **20+ CAD‑formaten** en kan bestanden met duizenden entiteiten verwerken zonder het volledige document in het geheugen te laden, waardoor het ideaal is voor high‑performance .NET‑applicaties.

## Snelle antwoorden
- **Wat is de eerste stap?** Laad het DWG‑bestand met `CadImage.Load`.
- **Welke klasse definieert het weergavegebied?** `Viewport` binnen `CadRasterizationOptions`.
- **Kan ik naar PDF exporteren?** Ja, met `PdfOptions` na rasterisatie.
- **Heb ik een licentie nodig voor productie?** Een commerciële licentie is vereist; een gratis proefversie werkt voor evaluatie.
- **Wordt .NET Core ondersteund?** Absoluut – Aspose.CAD werkt met .NET Framework, .NET Core en .NET 5/6.

## Vereisten

Voor je begint, zorg dat je het volgende hebt:

- Basiskennis van C#‑programmeren.
- Visual Studio (een recente editie) geïnstalleerd.
- Aspose.CAD‑bibliotheek toegevoegd aan je project. Je kunt deze downloaden van [Aspose.CAD download page](https://releases.aspose.com/cad/net/).
- Een voorbeeld‑DWG‑bestand, zoals **Bottom_plate.dwg**, om te volgen.

## Namespaces importeren

Voeg de vereiste `using`‑directieven toe aan de bovenkant van je C#‑bestand zodat de compiler de Aspose.CAD‑typen kan vinden.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.FileFormats.Cad;
```

Nu de omgeving klaar is, laten we de implementatie stap voor stap doorlopen.

## Hoe maak je viewport dwg c#?

Om een aangepaste viewport te maken, laad je eerst het DWG‑bestand in een `CadImage`‑object, configureer je vervolgens `CadRasterizationOptions` met de gewenste lay-out en schaal. Definieer de regio die je wilt weergeven, instantieer een `CadVportTableObject` met het berekende midden, de hoogte en de beeldverhouding, vervang de actieve viewport, stel eventuele PDF‑opties in, en sla tenslotte het resultaat op.

## Stap 1: laad het dwg‑bestand

`CadImage.Load` laadt een DWG‑bestand in een `CadImage`‑object, dat de CAD‑tekening in het geheugen vertegenwoordigt.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for loading the DWG file goes here.
}
```

## Stap 2: rasterisatie‑opties configureren

`CadRasterizationOptions` specificeert hoe de CAD‑tekening wordt gerasterd, inclusief lay-outselectie, schaal en uitvoergrootte.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };
rasterizationOptions.NoScaling = true;
// Additional rasterization configurations can be added here.
```

## Stap 3: regio definiëren om te tekenen

`Point` definieert de X‑ en Y‑coördinaten van de linkerbovenhoek van de te renderen regio.

```csharp
Point topLeft = new Point(6156, 7053);
double width = 3108;
double height = 2489;
```

## Stap 4: een nieuwe viewport maken

`CadVportTableObject` vertegenwoordigt een viewport‑object dat het zichtbare gebied en de beeldverhouding van de gerenderde tekening regelt.

```csharp
CadVportTableObject newView = new CadVportTableObject();
newView.Name.Value = "*Active";
newView.CenterPoint.X = topLeft.X + width / 2f;
newView.CenterPoint.Y = topLeft.Y - height / 2f;
newView.ViewHeight.Value = height;
newView.ViewAspectRatio.Value = width / height;
```

## Stap 5: actieve viewport vervangen

De lus vervangt de actieve viewport door de nieuw aangemaakte om de aangepaste weergave‑instellingen toe te passen.

```csharp
for (int i = 0; i < cadImage.ViewPorts.Count; i++)
{
    CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
    if ((currentView.Name.Value == null && cadImage.ViewPorts.Count == 1) ||
    string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
    {
        cadImage.ViewPorts[i] = newView;
        break;
    }
}
```

## Stap 6: PDF‑opties configureren

`PdfOptions` configureert PDF‑uitvoerparameters zoals compressie en metadata.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Stap 7: sla de gerenderde dwg op als PDF

`image.Save` schrijft de gerenderde afbeelding naar een bestand met de opgegeven formaatopties.

```csharp
cadImage.Save(MyDir, pdfOptions);
```

## Waarom een aangepaste viewport gebruiken bij het renderen van DWG?

Een aangepaste viewport stelt je in staat een specifieke lay-out of regio te isoleren, waardoor de bestandsgrootte wordt verkleind en de rendersnelheid verbetert. Aspose.CAD kan een 300‑pagina‑DWG in minder dan 2 seconden renderen wanneer een gerichte viewport wordt gebruikt, vergeleken met het renderen van de volledige tekening dat enkele seconden langer kan duren.

## Veelvoorkomende problemen en oplossingen

- **Lege uitvoer** – Zorg ervoor dat de viewport‑coördinaten binnen de tekeningsafmetingen liggen; gebruik `CadImage.Size` om de grenzen te verifiëren.
- **Ontbrekende lagen** – Stel `CadRasterizationOptions.Layouts` in op de juiste lay-outnaam; anders kan de standaardlay-out leeg zijn.
- **Prestatie‑vertraging** – Schakel anti‑aliasing uit in `CadRasterizationOptions` als je alleen een snelle preview nodig hebt.

## Veelgestelde vragen

### Q1: Kan ik Aspose.CAD gebruiken met andere CAD‑bestandsformaten?

A1: Ja, Aspose.CAD ondersteunt verschillende formaten, waaronder DWG, DXF, DWF en meer dan 20 extra CAD‑typen.

### Q2: Is Aspose.CAD compatibel met .NET Core?

A2: Ja, Aspose.CAD werkt met .NET Framework, .NET Core en de nieuwste .NET‑releases.

### Q3: Hoe kan ik verschillende lay-outs in een DWG‑bestand behandelen?

A3: Geef de gewenste lay-out op met de `Layouts`‑eigenschap van `CadRasterizationOptions` vóór het renderen.

### Q4: Zijn er licentie‑overwegingen voor het gebruik van Aspose.CAD?

A4: Voor licentie‑details, bezoek de [Aspose.CAD licensing page](https://purchase.aspose.com/buy).

### Q5: Waar kan ik extra ondersteuning vinden?

A5: Bezoek het [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) voor community‑hulp en discussies.

### Q6: Kan ik direct naar PNG renderen in plaats van PDF?

A6: Ja, wijzig de `PdfOptions` naar `PngOptions` en roep `image.Save("output.png", pngOptions)` aan.

### Q7: Hoe embed ik de gerenderde afbeelding in een Windows Forms‑applicatie?

A7: Laad de opgeslagen afbeelding in een `PictureBox`‑control met `Image.FromFile("output.png")`.

## Conclusie

Je weet nu hoe je **viewport dwg c#** kunt **maken** en een DWG‑bestand naar PDF (of andere rasterformaten) kunt renderen met Aspose.CAD. Door viewport‑manipulatie onder de knie te krijgen, krijg je fijnmazige controle over de visuele output, wat essentieel is voor het genereren van nauwkeurige technische tekeningen, rapporten of miniaturen. Verken extra rasterisatie‑instellingen, experimenteer met verschillende uitvoerformaten en integreer de code in grotere .NET‑services of desktop‑hulpmiddelen.

---

**Laatst bijgewerkt:** 2026-08-23  
**Getest met:** Aspose.CAD 24.11 for .NET  
**Auteur:** Aspose

## Gerelateerde tutorials

- [Hoe viewport instellen tijdens het converteren van DWG naar PDF met coördinaten in C# - Aspose.CAD tutorial](/cad/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/)
- [Leer CAD-rasterisatie‑opties instellen – Specifieke lay-outs exporteren naar PDF met Aspose.CAD](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)
- [Hoe DWG naar PDF en rasterafbeeldingen converteren met Aspose.CAD voor .NET](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}