---
date: 2026-03-16
description: Leer hoe u DWG naar PDF of rasterafbeeldingen kunt converteren met Aspose.CAD
  voor .NET. Deze stap‑voor‑stap CAD‑naar‑PDF‑tutorial behandelt het exporteren van
  DWG naar afbeeldingsformaten zoals PNG en laat zien hoe u DWG efficiënt naar afbeeldingsbestanden
  kunt exporteren.
linktitle: Exporting DWG to PDF or Raster Images
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Hoe DWG naar PDF en rasterafbeeldingen converteren met Aspose.CAD voor .NET
url: /nl/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/
weight: 11
---

### Q7: What is the best way to **how to convert dwg** when the source file contains multiple layouts?
"Wat is de beste manier om **dwg te converteren** wanneer het bronbestand meerdere lay‑outs bevat?"
Answer: "Vul `rasterizationOptions.Layouts` met alle lay‑outnamen die je wilt exporteren, loop vervolgens door elke lay‑out en roep `Save` aan voor elk uitvoerformaat."

Then the footer:

**Last Updated:** 2026-03-16 => "**Laatst bijgewerkt:** 2026-03-16"

**Tested With:** Aspose.CAD 24.11 for .NET => "**Getest met:** Aspose.CAD 24.11 voor .NET"

**Author:** Aspose => "**Auteur:** Aspose"

Now ensure shortcodes at end.

Now produce final content.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG exporteren naar PDF of rasterafbeeldingen - Aspose.CAD-gids

## Introductie

Als je **DWG naar PDF wilt converteren** (of naar rasterformaten zoals PNG) rechtstreeks vanuit een .NET‑applicatie, ben je hier aan het juiste adres. In deze tutorial lopen we stap voor stap door de exacte stappen die nodig zijn om Aspose.CAD for .NET te gebruiken voor de conversie, leggen we uit waarom de bibliotheek een solide keuze is, en laten we zien hoe je zowel PDF‑ als afbeeldingoutput kunt afhandelen met slechts een paar regels code.

## Snelle antwoorden
- **Welke bibliotheek behandelt DWG-conversie?** Aspose.CAD for .NET  
- **Kan ik DWG exporteren naar PNG evenals PDF?** Ja – dezelfde rasterisatie‑opties werken voor beide formaten.  
- **Heb ik een licentie nodig voor ontwikkeling?** Een gratis proefversie werkt voor testen; een commerciële licentie is vereist voor productie.  
- **Welke .NET‑versies worden ondersteund?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Wordt eenheidconversie automatisch afgehandeld?** Je kunt het eenhedensysteem handmatig definiëren (metrisch of imperiaal) zoals in de code getoond.

## Wat is “convert DWG to PDF”?
DWG naar PDF converteren betekent dat je een CAD‑tekening (DWG) neemt en deze rendert naar een draagbaar, alleen‑leesbaar document (PDF). Dit is handig voor het delen van ontwerpen met belanghebbenden die geen CAD‑software hebben, voor het maken van afdrukbare documentatie, of voor het archiveren van tekeningen in een universeel leesbaar formaat.

## Waarom Aspose.CAD gebruiken voor deze conversie?
- **Geen externe afhankelijkheden** – de bibliotheek werkt volledig in beheerde code.  
- **Hoge getrouwheid** – behoudt lagen, lijndiktes en lay‑outinformatie.  
- **Ingebouwde rasteropties** – stelt je in staat om te exporteren naar PNG, JPEG, BMP, enz., met één configuratie‑object.  
- **Cross‑platform** – werkt op Windows, Linux en macOS met .NET Core.

## Voorvereisten

Voordat we in de tutorial duiken, zorg dat je het volgende hebt:

- Een basisbegrip van .NET‑programmering.  
- Aspose.CAD for .NET bibliotheek geïnstalleerd. Zo niet, download deze [hier](https://releases.aspose.com/cad/net/).  
- Je favoriete geïntegreerde ontwikkelomgeving (IDE) ingesteld voor .NET‑ontwikkeling.

## Namespaces importeren

Laten we beginnen met het importeren van de benodigde namespaces in je .NET‑project. Dit zorgt ervoor dat je toegang hebt tot de Aspose.CAD‑functionaliteit in je code.

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

## Stap 1: DWG‑bestand laden

Begin met het laden van het DWG‑bestand dat je wilt converteren. Vervang `"Your Document Directory"` door het pad naar je DWG‑bestand.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for loading DWG goes here
}
```

## Stap 2: PDF‑export instellen (Hoe DWG naar PDF exporteren)

Stel nu de PDF‑exportinstellingen in. Dit voorbeeld laat zien hoe je de lay‑out instelt en eenheidconversies afhandelt.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };

// Check and define the unit system
bool currentUnitIsMetric = false;
double currentUnitCoefficient = 1.0;
DefineUnitSystem(cadImage.UnitType, out currentUnitIsMetric, out currentUnitCoefficient);

// Your code for setting up PDF export goes here
```

## Stap 3: Exporteren naar PDF

Voer de export naar PDF uit met de geconfigureerde instellingen.

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath, pdfOptions);
```

## Stap 4: Exporteren naar rasterafbeeldingen (dwg naar afbeelding exporteren)

Breid de functionaliteit uit om te exporteren naar rasterafbeeldingen, zoals PNG.

```csharp
// A4 size at 300 DPI - 2480 x 3508
rasterizationOptions.PageHeight = 3508;
rasterizationOptions.PageWidth = 2480;

PngOptions pngOptions = new PngOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath.Replace("pdf", "png"), pngOptions);
```

## Veelvoorkomende problemen en oplossingen

| Probleem | Waarom het gebeurt | Hoe op te lossen |
|----------|--------------------|------------------|
| **Lege pagina's in PDF** | Lay‑out niet correct gespecificeerd | Zorg ervoor dat `rasterizationOptions.Layouts` de juiste lay‑outnaam bevat (bijv. `"Model"`). |
| **Onjuiste afmetingen** | DPI of paginagrootte komt niet overeen | Pas `PageHeight`, `PageWidth` en DPI‑waarden aan in `CadRasterizationOptions`. |
| **Eenheden lijken onjuist** | Eenheidconversie niet gedefinieerd | Gebruik `DefineUnitSystem` om `currentUnitIsMetric` en `currentUnitCoefficient` in te stellen op basis van `cadImage.UnitType`. |
| **Licentie‑exception** | Beperkingen van de proefversie | Pas een tijdelijke of permanente licentie toe vóór het aanroepen van `Image.Load`. |

## Veelgestelde vragen

### Q1: Kan ik Aspose.CAD voor .NET gebruiken in mijn commerciële projecten?
A1: Ja, dat kan. Bezoek [purchase.aspose.com/buy](https://purchase.aspose.com/buy) voor licentie‑details.

### Q2: Is er een gratis proefversie beschikbaar?
A2: Zeker! Download je gratis proefversie [hier](https://releases.aspose.com/).

### Q3: Hoe kan ik ondersteuning krijgen voor Aspose.CAD voor .NET?
A3: Ga naar het [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) voor community‑ondersteuning.

### Q4: Kan ik een tijdelijke licentie verkrijgen voor testdoeleinden?
A4: Ja, je kunt een tijdelijke licentie krijgen [hier](https://purchase.aspose.com/temporary-license/).

### Q5: Waar kan ik de gedetailleerde documentatie vinden?
A5: De documentatie is beschikbaar op [Aspose.CAD](https://reference.aspose.com/cad/net/).

### Q6: Hoe sla ik **CAD op als PNG** met hoge kwaliteit?
A6: Stel `PageHeight` en `PageWidth` in op de gewenste pixelafmetingen en kies een DPI van 300 of hoger in `CadRasterizationOptions`.

### Q7: Wat is de beste manier om **dwg te converteren** wanneer het bronbestand meerdere lay‑outs bevat?
A7: Vul `rasterizationOptions.Layouts` met alle lay‑outnamen die je wilt exporteren, loop vervolgens door elke lay‑out en roep `Save` aan voor elk uitvoerformaat.

---

**Laatst bijgewerkt:** 2026-03-16  
**Getest met:** Aspose.CAD 24.11 voor .NET  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}