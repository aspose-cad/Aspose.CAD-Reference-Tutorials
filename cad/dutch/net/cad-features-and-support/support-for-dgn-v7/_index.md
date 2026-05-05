---
date: 2026-03-29
description: Leer hoe u DGN naar JPEG kunt converteren met Aspose.CAD voor .NET, met
  volledige ondersteuning voor DGN V7 en waarmee u CAD eenvoudig naar rasterafbeeldingen
  kunt converteren.
linktitle: Support for DGN V7
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Converteer DGN naar JPEG met Aspose.CAD voor .NET – V7-ondersteuning
url: /nl/net/cad-features-and-support/support-for-dgn-v7/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Converteer DGN naar JPEG met Aspose.CAD voor .NET – V7-ondersteuning

## Introductie

In deze tutorial leer je hoe je **DGN naar JPEG** kunt converteren met Aspose.CAD voor .NET, waarbij je profiteert van de volledige DGN V7-ondersteuning van de bibliotheek. Het converteren van DGN‑bestanden naar rasterafbeeldingen zoals JPEG is een veelvoorkomende eis wanneer je CAD‑tekeningen in webpagina's, mobiele apps of rapportagetools moet insluiten. Aspose.CAD stelt je ook in staat om **CAD naar raster** formaten efficiënt te converteren, waardoor je flexibiliteit krijgt in hoe je ontwerpinformatie presenteert.

## Snelle antwoorden
- **Waar gaat de tutorial over?** Het converteren van een DGN V7‑bestand naar een JPEG‑rasterafbeelding met Aspose.CAD voor .NET.  
- **Welke bibliotheekversie is vereist?** Elke recente Aspose.CAD voor .NET‑release die DGN V7‑ondersteuning bevat.  
- **Heb ik een licentie nodig?** Een gratis proefversie werkt voor ontwikkeling; een commerciële licentie is vereist voor productie.  
- **Kan ik de uitvoergrootte wijzigen?** Ja – rasterisatie‑opties laten je paginabreedte, -hoogte en schaalinstellingen bepalen.  
- **Is JPEG het enige uitvoerformaat?** Nee – Aspose.CAD ondersteunt vele rasterformaten (PNG, BMP, TIFF, enz.).

## Wat is DGN V7?
DGN (Design) is een bestandsformaat dat oorspronkelijk is gemaakt door Bentley Systems voor MicroStation. Versie 7 voegt rijkere geometrie en metadata toe, waardoor het een populaire keuze is voor civiele‑techniek en infrastructuurprojecten. Aspose.CAD voor .NET kan DGN V7‑bestanden direct lezen en hun inhoud blootleggen als `CadImage`‑objecten die je kunt rasteren of naar andere formaten kunt converteren.

## Waarom DGN naar JPEG converteren?
- **Web‑klaar:** JPEG‑afbeeldingen zijn lichtgewicht en worden direct in browsers weergegeven zonder speciale plug‑ins.  
- **Cross‑platform:** JPEG kan op elk apparaat worden bekeken, waardoor het ideaal is om CAD‑tekeningen te delen met niet‑technische belanghebbenden.  
- **Vereenvoudigde werkstromen:** Het converteren naar een rasterformaat verwijdert de noodzaak voor CAD‑specifieke viewers in vervolgprocessen.

## Vereisten

Voordat we in de implementatie duiken, zorg ervoor dat je het volgende hebt:

- **Aspose.CAD voor .NET** – download het van de [website](https://releases.aspose.com/cad/net/).  
- **Ontwikkelomgeving** – Visual Studio (of elke IDE die .NET ondersteunt).  

Als je deze klaar hebt, kun je de stappen zonder onderbreking volgen.

## Namespaces importeren

Begin met het importeren van de namespaces die nodig zijn voor het verwerken van CadImage en rasterisatie.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Stap 1: Laad het DGN-bestand

Laad het bron‑DGN‑bestand in een `CadImage`‑object. Vervang het tijdelijke pad door de map die je DGN‑bestand bevat.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Subsequent steps will be placed here.
}
```

## Stap 2: Rasterisatie-opties configureren

Definieer hoe de DGN‑tekening moet worden gerasterd. Je kunt de uitvoerdimensies en schaalgedrag regelen.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions
{
    PageWidth = 600,
    PageHeight = 300,
    NoScaling = true,
    AutomaticLayoutsScaling = false
};
```

## Stap 3: Vector-rasterisatie-opties instellen

Maak een `JpegOptions`‑object (of een andere rasterformaat‑optie) aan en koppel de rasterisatie‑instellingen.

```csharp
ImageOptionsBase options = new JpegOptions
{
    VectorRasterizationOptions = rasterizationOptions
};
```

## Stap 4: Sla de gerasterde afbeelding op

Exporteer tenslotte de DGN‑tekening naar een JPEG‑bestand met behulp van de `Save`‑methode.

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpeg", options);
```

Wanneer de code succesvol wordt uitgevoerd, vind je een JPEG‑representatie van de oorspronkelijke DGN V7‑tekening in de opgegeven map.

## Veelvoorkomende problemen en oplossingen

| Probleem | Oplossing |
|----------|-----------|
| **Bestand niet gevonden** | Controleer of `MyDir` eindigt op een pad‑scheidingsteken (`\\` of `/`) en of de bestandsnaam correct is. |
| **Lege uitvoerafbeelding** | Zorg ervoor dat `NoScaling` correct is ingesteld; zet het op `false` als je wilt dat de tekening de pagina vult. |
| **Niet‑ondersteunde entiteiten** | Aspose.CAD ondersteunt de meeste DGN‑entiteiten, maar zeer oude of aangepaste objecten kunnen worden genegeerd. Controleer het conversielogboek op waarschuwingen. |

## Veelgestelde vragen

### V1: Is Aspose.CAD compatibel met de nieuwste DGN V7‑specificaties?
**A:** Ja, Aspose.CAD ondersteunt DGN V7 volledig en verwerkt zowel geometrie als metadata volgens de nieuwste normen.

### V2: Kan ik de rasterisatie‑opties aanpassen voor DGN‑bestandsconversie?
**A:** Absoluut. De `CadRasterizationOptions`‑klasse stelt je in staat om paginagrootte, schaal, lijndikte, achtergrondkleur en meer aan te passen.

### V3: Zijn er andere ondersteunde uitvoerformaten naast JPEG?
**A:** Ja, Aspose.CAD kan exporteren naar PNG, BMP, TIFF en verschillende andere rasterformaten. Gebruik eenvoudigweg de bijbehorende `*Options`‑klasse (bijv. `PngOptions`).

### V4: Hoe kan ik hulp krijgen bij vragen over Aspose.CAD?
**A:** Bezoek het [Aspose.CAD‑forum](https://forum.aspose.com/c/cad/19) voor community‑ondersteuning en officiële antwoorden.

### V5: Is er een gratis proefversie beschikbaar voor Aspose.CAD voor .NET?
**A:** Ja, je kunt een proefversie downloaden via [hier](https://releases.aspose.com/).

---

**Laatst bijgewerkt:** 2026-03-29  
**Getest met:** Aspose.CAD 24.12 voor .NET  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}