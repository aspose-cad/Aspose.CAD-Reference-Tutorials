---
date: 2026-03-21
description: Leer hoe u de CAD‑layoutgrootte in .NET kunt ophalen met Aspose.CAD.
  Volg onze stapsgewijze gids voor efficiënte CAD‑bestandsbewerking.
linktitle: Get Size of CAD Layout
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: CAD-lay-outgrootte ophalen in Aspose.CAD voor .NET
url: /nl/net/cad-drawing-manipulation/get-size-of-cad-layout/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Verkrijg CAD‑layoutgrootte in Aspose.CAD voor .NET

## Introductie

In deze uitgebreide tutorial ontdek je **hoe je de CAD‑layoutgrootte kunt ophalen** met behulp van de Aspose.CAD‑bibliotheek voor .NET. Of je nu een CAD‑viewer bouwt, miniaturen genereert, of precieze layout‑afmetingen nodig hebt voor verdere verwerking, het kennen van de exacte grootte van elke layout is essentieel. We lopen het volledige werkproces door — van het laden van een tekening tot het extraheren van layout‑afmetingen en optioneel opslaan als afbeeldingen — zodat je deze functionaliteit met vertrouwen in je eigen applicaties kunt integreren.

## Snelle antwoorden
- **Wat betekent “CAD‑layoutgrootte ophalen”?** Het betekent het ophalen van de breedte en hoogte (in tekeneenheden) van elke niet‑lege layout in een CAD‑bestand.  
- **Welke bibliotheek ondersteunt dit?** Aspose.CAD voor .NET biedt een eenvoudige API om layout‑informatie te benaderen.  
- **Heb ik een licentie nodig?** Een gratis proefversie werkt voor evaluatie; een commerciële licentie is vereist voor productiegebruik.  
- **Ondersteunde formaten?** DWG, DXF en vele andere CAD/BIM‑formaten worden volledig ondersteund.  
- **Typische implementatietijd?** Ongeveer 10‑15 minuten voor een basisroutine om de grootte op te halen.

## Wat is “CAD‑layoutgrootte ophalen”?
Het ophalen van de CAD‑layoutgrootte betekent het extraheren van de geometrische extents van elke layout (paper space) die in een CAD‑tekening is gedefinieerd. Deze extents worden uitgedrukt in de native eenheden van de tekening (meestal millimeters of inches) en zijn nuttig voor taken zoals schalen, afdrukken of het genereren van voorbeeldafbeeldingen.

## Waarom CAD‑layoutgrootte ophalen met Aspose.CAD?
- **Geen CAD‑software vereist** – Werkt volledig server‑side.  
- **Cross‑platform** – Werkt met .NET Framework, .NET Core en .NET 5/6+.  
- **Nauwkeurige metingen** – Retourneert exacte extents zoals opgeslagen in het bestand, waardoor handmatig parsen wordt vermeden.  
- **Eenvoudige integratie** – Simpele API‑aanroepen passen naadloos in bestaande C#‑projecten.

## Vereisten

Voordat we in de code duiken, zorg dat je het volgende hebt:

- Aspose.CAD voor .NET geïnstalleerd. Je kunt het downloaden vanaf de [Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/).
- Een of meer CAD‑bestanden (DWG, DXF, enz.) die je wilt analyseren. Deze gids gebruikt `conic_pyramid.dxf` en `Bottom_plate.dwg` als voorbeeldbestanden.

## Namespaces importeren

In je .NET‑project begin je met het importeren van de benodigde namespaces:

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.ImageOptions;
```

## Stap 1: Stel de documentmap in

Definieer de map die je CAD‑bestanden bevat. Vervang de placeholder door het daadwerkelijke pad op jouw machine.

```csharp
string MyDir = "Your Document Directory";
```

## Stap 2: Specificeer CAD‑bestandspaden

Maak een array die verwijst naar elk CAD‑bestand dat je wilt verwerken.

```csharp
string[] sourceFilePaths = new[]
{
    MyDir + "conic_pyramid.dxf",
    MyDir + "Bottom_plate.dwg"
};
```

## Stap 3: Doorloop CAD‑bestanden

Laad elk bestand, detecteer het formaat en bereid je voor om layout‑informatie te extraheren.

```csharp
foreach (var sourceFilePath in sourceFilePaths)
{
    string extension = Path.GetExtension(sourceFilePath);
    using (CadImage cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath))
    {
        // ... (continue to the next step)
    }
}
```

## Stap 4: Haal niet‑lege layouts op

We hebben een hulpmethode nodig die alleen de layouts retourneert die daadwerkelijk teken‑entiteiten bevatten. Lege layouts worden genegeerd omdat ze geen grootte hebben om te rapporteren.

```csharp
private static List<string> GetNotEmptyLayouts(Image cadImage, string extension)
{
    // ... (continue to the next step)
}
```

## Stap 5: Haal layouts op voor DWG‑bestanden

DWG‑bestanden slaan layout‑informatie op in de `HeaderVariables`‑tabel. De volgende methode extraheert de namen van alle niet‑lege layouts voor een DWG‑tekening.

```csharp
private static List<string> GetNotEmptyLayoutsForDwg(CadImage cadImage)
{
    // ... (continue to the next step)
}
```

## Stap 6: Haal layouts op voor DXF‑bestanden

DXF‑bestanden gebruiken een andere structuur. Deze methode doorloopt de `Tables`‑collectie om paper‑space‑layouts te vinden die entiteiten bevatten.

```csharp
private static List<string> GetNotEmptyLayoutsForDxf(CadImage cadImage)
{
    // ... (continue to the next step)
}
```

## Stap 7: Haal layoutgrootte op en sla op als afbeelding

Loop tenslotte door elke gevonden layout, lees de extents, en render de layout optioneel naar een afbeeldingsbestand voor visuele verificatie.

```csharp
foreach (string layout in layouts)
{
    // ... (continue to the next step)
}
```

## Veelvoorkomende problemen & tips

- **Ontbrekende layout‑namen:** Zorg ervoor dat het CAD‑bestand daadwerkelijk paper‑space‑layouts bevat; sommige bestanden hebben alleen model‑space.  
- **Onjuiste eenheden:** De grootte wordt geretourneerd in de native eenheden van de tekening. Converteer naar millimeters of inches indien nodig.  
- **Prestaties:** Het laden van zeer grote DWG/DXF‑bestanden kan veel geheugen vergen; overweeg om bestanden asynchroon of in batches te verwerken.

## Veelgestelde vragen

**V: Is Aspose.CAD compatibel met alle CAD‑bestandsformaten?**  
A: Ja, Aspose.CAD ondersteunt een breed scala aan formaten, waaronder DWG, DXF, DGN en vele BIM‑bestandstypen.

**V: Kan ik de opties voor het opslaan van afbeeldingen aanpassen?**  
A: Absoluut! Je kunt de `CadRasterizationOptions` (formaat, resolutie, achtergrondkleur, enz.) aanpassen om aan je specifieke behoeften te voldoen.

**V: Waar kan ik extra documentatie vinden?**  
A: Raadpleeg de [Aspose.CAD documentation](https://reference.aspose.com/cad/net/) voor gedetailleerde API‑referenties en meer voorbeelden.

**V: Is er een gratis proefversie beschikbaar?**  
A: Ja, je kunt Aspose.CAD verkennen met een [free trial](https://releases.aspose.com/).

**V: Hoe kan ik technische ondersteuning krijgen?**  
A: Voor technische ondersteuning, bezoek het [Aspose.CAD forum](https://forum.aspose.com/c/cad/19).

---

**Last Updated:** 2026-03-21  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}