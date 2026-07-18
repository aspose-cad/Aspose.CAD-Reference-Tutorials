---
date: 2026-07-18
description: Hoe CAD naar PNG te exporteren met Aspose.CAD voor .NET. Converteer IFC-bestanden
  naar PNG-afbeeldingen van hoge kwaliteit, snel en betrouwbaar.
keywords:
- how to export cad to png
- Aspose.CAD IFC conversion
- CAD to PNG .NET
lastmod: 2026-07-18
linktitle: IFC-bestanden exporteren naar PNG
og_description: Hoe CAD naar PNG te exporteren met Aspose.CAD voor .NET. Leer stap‑voor‑stap
  de conversie van IFC-bestanden naar PNG-afbeeldingen met een code‑vrije installatie.
og_image_alt: Guide showing IFC to PNG conversion with Aspose.CAD for .NET
og_title: Hoe CAD naar PNG exporteren – Aspose.CAD .NET-gids
schemas:
- author: Aspose
  dateModified: '2026-07-18'
  description: How to export CAD to PNG using Aspose.CAD for .NET. Convert IFC files
    to high‑quality PNG images quickly and reliably.
  headline: How to Export CAD to PNG – Exporting IFC Files with Aspose.CAD
  type: TechArticle
- questions:
  - answer: No, Aspose.CAD for .NET is specifically designed for Windows environments.
    question: Can I use Aspose.CAD for .NET on macOS or Linux?
  - answer: Yes, you can obtain a temporary license from [here](https://purchase.aspose.com/temporary-license/)
      for evaluation.
    question: Is a temporary license available for testing purposes?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community
      support and discussions.
    question: How can I get support for Aspose.CAD?
  - answer: Refer to the [Aspose.CAD documentation](https://reference.aspose.com/cad/net/)
      for detailed information and examples.
    question: Where can I find comprehensive documentation?
  - answer: Check the documentation or seek assistance on the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19).
    question: What if I encounter issues during installation?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- export cad
- Aspose.CAD
- IFC to PNG
- .NET image conversion
title: Hoe CAD naar PNG exporteren – IFC-bestanden exporteren met Aspose.CAD
url: /nl/net/exporting-to-image-formats/exporting-ifc-files-to-png/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hoe CAD naar PNG exporteren – IFC-bestanden exporteren met Aspose.CAD

## Introductie

Als u **how to export cad to png** nodig heeft, biedt Aspose.CAD voor .NET een betrouwbare, code‑vrije manier om IFC (Industry Foundation Classes) modellen om te zetten in scherpe PNG rasterafbeeldingen. In deze tutorial lopen we het volledige werkproces door — van het installeren van de bibliotheek tot het opslaan van de uiteindelijke PNG — zodat u de conversie met vertrouwen kunt integreren in elke .NET‑applicatie.

## Snelle antwoorden
- **Welke bibliotheek verwerkt de conversie?** Aspose.CAD for .NET.
- **Ondersteund bronformaat?** IFC (Industry Foundation Classes) bestanden.
- **Doelformaat afbeelding?** PNG, met volledige controle over grootte en resolutie.
- **Minimale .NET‑versie?** .NET Framework 4.5+ of .NET Core 3.1+.
- **Licentie‑vereiste?** Een geldige Aspose.CAD‑licentie voor productiegebruik.

## Wat is “how to export cad to png”?

De uitdrukking verwijst naar het proces van het converteren van CAD‑gebaseerde bestandsformaten, zoals IFC, naar Portable Network Graphics (PNG) rasterafbeeldingen. Deze conversie maakt eenvoudig bekijken, delen en insluiten van CAD‑visualisaties in webpagina’s, documentatie of rapporten mogelijk, en biedt een lichtgewicht, breed ondersteund formaat dat de visuele nauwkeurigheid behoudt zonder dat er gespecialiseerde CAD‑viewers nodig zijn.

## Waarom Aspose.CAD voor deze conversie gebruiken?

Aspose.CAD ondersteunt **50+ CAD‑ en BIM‑formaten** en kan multi‑honderd‑pagina‑IFC‑modellen verwerken zonder het volledige bestand in het geheugen te laden. Het levert snelle, geheugen‑efficiënte conversies op standaard serverhardware, waarbij automatisch lagen, lijndiktes en kleuraanpassing worden afgehandeld, terwijl uitgebreide configuratie‑opties voor outputkwaliteit en -grootte worden geboden.

## Voorvereisten

### 1. Aspose.CAD‑installatie
Zorg ervoor dat u Aspose.CAD voor .NET geïnstalleerd heeft. U kunt het downloaden vanaf de release‑pagina [hier](https://releases.aspose.com/cad/net/).

### 2. Documentmap
Maak een aangewezen map voor uw documenten. In het gegeven voorbeeld vertegenwoordigt de variabele `MyDir` de documentmap.

## Importeer namespaces
Nu de voorvereisten klaar zijn, importeert u de namespaces die nodig zijn om met Aspose.CAD te werken in uw .NET‑project.

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using Aspose.CAD.FileFormats.Ifc;
```

## Hoe CAD naar PNG exporteren?

`IfcImage` vertegenwoordigt een IFC‑CAD‑afbeelding die kan worden gerasterd naar rasterformaten zoals PNG. Laad uw IFC‑bestand met `new IfcImage("source.ifc")`, configureer rasterisatie via `RasterizationOptions`, stel PNG‑specifieke instellingen in met `PngOptions` en roep ten slotte `Save(outputPath, pngOptions)` aan. Deze end‑to‑end‑stroom converteert het CAD‑model naar een hoge‑resolutie PNG in slechts een paar regels code, waarbij automatisch lagen, kleuren en lijndiktes worden afgehandeld.

## Stap 1: IFC‑bestand laden
De `IfcImage`‑klasse laadt een IFC‑model en bereidt het voor op rasterisatie.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "example.ifc";
using (IfcImage cadImage = (IfcImage)Image.Load(sourceFilePath))
{
```

In deze stap initialiseren we het Aspose.CAD `IfcImage`‑object en laden we het IFC‑bestand erin.

## Stap 2: Rasterisatie‑opties instellen
De `RasterizationOptions`‑klasse bepaalt hoe vectorgegevens worden omgezet in rasterafbeeldingen, inclusief paginabreedte, -hoogte en achtergrondkleur.

```csharp
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
   
    rasterizationOptions.PageWidth = 100;
    rasterizationOptions.PageHeight = 100;
```

Definieer rasterisatie‑opties om de paginabreedte en -hoogte voor de PNG‑output in te stellen.

## Stap 3: PNG‑opties instellen
De `PngOptions`‑klasse bevat instellingen die specifiek zijn voor PNG‑output, zoals compressieniveau en kleurdiepte.

```csharp
    PngOptions pngOptions = new PngOptions();
    pngOptions.VectorRasterizationOptions = rasterizationOptions;
```

Maak PNG‑opties aan en koppel de eerder gedefinieerde rasterisatie‑opties.

## Stap 4: Uitvoerpad opgeven
Het uitvoerpad bepaalt waar het gegenereerde PNG‑bestand wordt opgeslagen.

```csharp
    // Set output path as well
    string outPath = sourceFilePath + ".png";
    cadImage.Save(outPath, pngOptions);
}
```

Definieer het uitvoerpad voor het PNG‑bestand, zorg ervoor dat het dezelfde naam heeft als het bronbestand met de extensie ".png". Sla ten slotte de geconverteerde afbeelding op.

## Veelvoorkomende problemen en oplossingen
- **Ontbrekende lettertypen of lijntypen:** Zorg ervoor dat de bron‑IFC alle vereiste bronnen verwijst; Aspose.CAD voegt ontbrekende assets in wanneer mogelijk.
- **Grote bestanden veroorzaken geheugenpieken:** Gebruik de `MemoryLimit`‑eigenschap op `RasterizationOptions` om het geheugengebruik te beperken.
- **Onjuiste kleuren:** Controleer of de kleurdefinities van de bron‑IFC voldoen aan het IFC‑schema; Aspose.CAD respecteert de standaard kleurtoewijzing.

## Veelgestelde vragen

**Q: Kan ik Aspose.CAD voor .NET gebruiken op macOS of Linux?**  
A: Nee, Aspose.CAD voor .NET is specifiek ontworpen voor Windows‑omgevingen.

**Q: Is er een tijdelijke licentie beschikbaar voor testdoeleinden?**  
A: Ja, u kunt een tijdelijke licentie verkrijgen via [hier](https://purchase.aspose.com/temporary-license/) voor evaluatie.

**Q: Hoe kan ik ondersteuning krijgen voor Aspose.CAD?**  
A: Bezoek het [Aspose.CAD‑forum](https://forum.aspose.com/c/cad/19) voor community‑ondersteuning en discussies.

**Q: Waar kan ik uitgebreide documentatie vinden?**  
A: Raadpleeg de [Aspose.CAD‑documentatie](https://reference.aspose.com/cad/net/) voor gedetailleerde informatie en voorbeelden.

**Q: Wat als ik problemen ondervind tijdens de installatie?**  
A: Controleer de documentatie of vraag hulp op het [Aspose.CAD‑forum](https://forum.aspose.com/c/cad/19).

---

**Laatst bijgewerkt:** 2026-07-18  
**Getest met:** Aspose.CAD 24.11 for .NET  
**Auteur:** Aspose

## Gerelateerde tutorials

- [CAD-tekening naar rasterafbeelding converteren in Aspose.CAD voor .NET](/cad/net/cad-drawing-manipulation/convert-cad-drawing-to-raster-image/)
- [STL naar PNG-conversie eenvoudig gemaakt met Aspose.CAD voor .NET](/cad/net/stl-file-export/exporting-stl-files-to-png/)
- [CAD‑lay-outs exporteren naar rasterafbeeldingsformaten in Aspose.CAD voor .NET](/cad/net/cad-export-formats/export-cad-layouts-to-raster-image-formats/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}