---
date: 2026-03-21
description: Leer hoe je DXF naar PNG en andere rasterformaten kunt converteren met
  Aspose.CAD voor .NET. Volg onze stapsgewijze handleiding voor naadloze CAD-laagexport.
linktitle: Export CAD Layouts to Raster Image Formats
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Converteer DXF naar PNG met Aspose.CAD voor .NET
url: /nl/net/cad-export-formats/export-cad-layouts-to-raster-image-formats/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD-indelingen exporteren naar rasterafbeeldingsformaten in Aspose.CAD voor .NET

## Inleiding

Zoekt u een efficiënte manier om **convert dxf to png** en andere rasterafbeeldingsformaten te gebruiken met Aspose.CAD voor .NET? Deze stap‑voor‑stap gids leidt u door het proces, met gedetailleerde instructies en code‑fragmenten om de taak naadloos te maken. Of u nu een ervaren ontwikkelaar bent of een nieuwkomer bij Aspose.CAD, deze tutorial is geschikt voor elk niveau van expertise.

### Snelle antwoorden
- **Welke bibliotheek behandelt de conversie?** Aspose.CAD for .NET  
- **Primair ondersteund formaat out of the box?** JPEG, PNG, BMP en TIFF rasterafbeeldingen  
- **Kan ik specifieke CAD‑lagen exporteren?** Ja – gebruik `CadRasterizationOptions.Layers` om individuele lagen te targeten  
- **Heb ik een licentie nodig voor productie?** Een geldige Aspose.CAD‑licentie is vereist voor niet‑trial gebruik  
- **Ondersteunde .NET‑versies?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7  

## Wat is **convert dxf to png**?

Een DXF (Drawing Exchange Format) bestand naar PNG converteren betekent het rasteren van vector‑gebaseerde CAD‑gegevens naar een pixel‑gebaseerde afbeelding. Dit is handig wanneer u CAD‑tekeningen moet insluiten in webpagina's, rapporten of elke omgeving die alleen rastergrafieken ondersteunt.

## Waarom CAD‑lagen afzonderlijk exporteren?

Het afzonderlijk exporteren van CAD‑lagen geeft u granulaire controle over de visuele output, verkleint de bestandsgrootte van elke afbeelding, en stelt u in staat om laag‑specifieke styling of nabewerking toe te passen. Dit is vooral handig voor grote technische tekeningen waarbij slechts een deel van de lagen relevant is voor een bepaald publiek.

## Voorvereisten

Voordat u aan de tutorial begint, zorg ervoor dat u het volgende heeft:

- **Aspose.CAD for .NET Library** – download deze van de [Aspose.CAD website](https://releases.aspose.com/cad/net/).  
- **CAD‑tekenbestand** – een DXF‑bestand (bijv. `conic_pyramid.dxf`) dat u wilt converteren naar rasterformaten.  

## Namespaces importeren

Importeer in uw .NET‑project de benodigde namespaces om de functionaliteit van Aspose.CAD te benutten. Voeg de volgende namespaces toe aan het begin van uw code:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Hoe **convert dxf to png** – Stapsgewijze gids

### Stap 1: CAD‑tekening laden

Laad eerst het DXF‑bestand in een `Image`‑object. Dit object vertegenwoordigt de volledige CAD‑tekening in het geheugen.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

// Load a CAD drawing in an instance of Image
using (var image = Image.Load(sourceFilePath))
{
    // Your code for loading the CAD drawing goes here
}
```

### Stap 2: Maak `CadRasterizationOptions` aan

Configureer rasterisatie‑instellingen zoals uitvoerafmetingen en resolutie. Deze opties bepalen hoe de vectorgegevens worden gerasterd.

```csharp
// Create an instance of CadRasterizationOptions
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
```

### Stap 3: Specificeer lagen (CAD‑lagen exporteren)

Als u slechts een specifieke laag nodig heeft, vermeld dan hier de naam. Dit toont **export cad layers** afzonderlijk.

```csharp
// Add the layer name to the CadRasterizationOptions's layer list
rasterizationOptions.Layers = new string[] { "LayerA" };
```

### Stap 4: Kies een afbeeldingsformaat – Sla CAD op als PNG (of JPEG)

Maak een opties‑object aan dat specifiek is voor het afbeeldingsformaat. Vervang `JpegOptions` door `PngOptions` wanneer u **save cad as png** wilt.

```csharp
// Create an instance of JpegOptions (or any ImageOptions for raster formats)
var options = new JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
```

> **Pro tip:** Om PNG‑bestanden te genereren, maakt u eenvoudig `new PngOptions()` aan in plaats van `JpegOptions`.

### Stap 5: Exporteren naar JPEG (of PNG) formaat

Sla tenslotte de gerasterde afbeelding op schijf op. De bestandsextensie bepaalt het uitvoerformaat.

```csharp
// Export each layer to Jpeg format
MyDir = MyDir + "CADLayersToRasterImageFormats_out.jpg";
image.Save(MyDir, options);
```

Wanneer u `JpegOptions` vervangt door `PngOptions`, zal dezelfde code **convert dxf to png** en een `.png`‑bestand genereren.

### Aanvullende stap: Alle lagen converteren

Als u **convert cad to raster** voor elke laag in de tekening moet uitvoeren, roep dan de onderstaande hulpfunctie aan. Deze doorloopt alle lagen en slaat elke laag op als een afzonderlijke afbeelding.

```csharp
ConvertAllLayersToRasterImageFormats();
```

> *Opmerking:* De implementatie van `ConvertAllLayersToRasterImageFormats` maakt deel uit van de volledige Aspose.CAD‑samplesuite en toont batchverwerking van lagen.

## Veelvoorkomende problemen & probleemoplossing

| Symptoom | Waarschijnlijke oorzaak | Oplossing |
|----------|--------------------------|-----------|
| Lege of witte afbeelding | Rasterisatie‑opties niet ingesteld (bijv. `PageWidth`/`PageHeight` = 0) | Zorg ervoor dat `PageWidth` en `PageHeight` positieve waarden hebben |
| Ontbrekende lagen | Onjuiste laagnaam in `Layers`‑array | Controleer de exacte laagnaam in het CAD‑bestand (hoofdlettergevoelig) |
| Lage kwaliteit PNG | Standaard DPI is laag | Stel `rasterizationOptions.Resolution = 300;` in voor hogere kwaliteit |

## Veelgestelde vragen (Origineel)

### V1: Kan ik andere afbeeldingsformaten gebruiken voor export?

A1: Ja, dat kan. Vervang simpelweg `JpegOptions` door de opties van het gewenste formaat, zoals `PngOptions` of `BmpOptions`.

### V2: Is er een proefversie beschikbaar?

A2: Ja, u kunt de functionaliteit van Aspose.CAD verkennen door de proefversie te downloaden [hier](https://releases.aspose.com/).

### V3: Hoe kan ik ondersteuning krijgen voor Aspose.CAD?

A3: Bezoek het Aspose.CAD‑[forum](https://forum.aspose.com/c/cad/19) voor community‑ondersteuning of overweeg een licentie aan te schaffen voor toegewijde ondersteuning.

### V4: Zijn tijdelijke licenties beschikbaar?

A4: Ja, u kunt een tijdelijke licentie verkrijgen [hier](https://purchase.aspose.com/temporary-license/).

### V5: Waar kan ik de documentatie vinden?

A5: Raadpleeg de gedetailleerde documentatie [hier](https://reference.aspose.com/cad/net/).

## Aanvullende FAQ

**V: Kan ik alle lagen in één commando exporteren?**  
A: Ja, gebruik de `ConvertAllLayersToRasterImageFormats`‑methode die hierboven is getoond.

**V: Ondersteunt Aspose.CAD vectorformaten zoals SVG?**  
A: Het richt zich voornamelijk op rasterformaten, maar u kunt exporteren naar PDF dat vectorgegevens behoudt.

**V: Hoe kan ik de achtergrondkleur van de geëxporteerde PNG regelen?**  
A: Stel `rasterizationOptions.BackgroundColor` in op de gewenste `Color` vóór het opslaan.

**V: Is het mogelijk om een enkele lay-out te exporteren in plaats van de volledige tekening?**  
A: Ja, configureer `rasterizationOptions.Layouts` om de lay-outnaam (‑en) op te geven die u wilt rasteren.

## Conclusie

U heeft nu geleerd hoe u **convert dxf to png**, **export cad layers**, en **save cad as png** of JPEG kunt gebruiken met Aspose.CAD voor .NET. Door `CadRasterizationOptions` aan te passen en afbeeldingsformaat‑opties te wisselen, kunt u de conversie afstemmen op vrijwel elke rasteroutput die u nodig heeft. Verken de andere formaatopties in de Aspose.CAD‑API om uw CAD‑naar‑raster‑workflow uit te breiden.

---

**Last Updated:** 2026-03-21  
**Tested With:** Aspose.CAD for .NET 24.11 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}