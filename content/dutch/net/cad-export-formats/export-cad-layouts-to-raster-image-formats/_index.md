---
title: Exporteer CAD-lay-outs naar rasterafbeeldingsformaten in Aspose.CAD voor .NET
linktitle: Exporteer CAD-lay-outs naar rasterafbeeldingsformaten
second_title: Aspose.CAD .NET - CAD- en BIM-bestandsindeling
description: Leer hoe u CAD-lay-outs naar rasterafbeeldingen kunt exporteren met Aspose.CAD voor .NET. Volg onze stapsgewijze handleiding voor een naadloze conversie.
type: docs
weight: 10
url: /nl/net/cad-export-formats/export-cad-layouts-to-raster-image-formats/
---
## Invoering

Wilt u CAD-lay-outs efficiënt converteren naar rasterafbeeldingsformaten met behulp van Aspose.CAD voor .NET? Deze stapsgewijze handleiding leidt u door het proces en biedt gedetailleerde instructies en codefragmenten om de taak naadloos te laten verlopen. Of je nu een doorgewinterde ontwikkelaar bent of een nieuwkomer bij Aspose.CAD, deze tutorial is geschikt voor alle niveaus van expertise.

## Vereisten

Voordat u in de zelfstudie duikt, moet u ervoor zorgen dat u over het volgende beschikt:

- Aspose.CAD voor .NET-bibliotheek: Zorg ervoor dat de Aspose.CAD-bibliotheek is geïnstalleerd. Als dit niet het geval is, kunt u deze downloaden van de[Aspose.CAD-website](https://releases.aspose.com/cad/net/).

- CAD-tekeningbestand: bereid een CAD-tekeningbestand voor (bijvoorbeeld conic_pyramid.dxf) dat u wilt converteren naar rasterafbeeldingsformaten.

## Naamruimten importeren

Importeer in uw .NET-project de benodigde naamruimten om de Aspose.CAD-functionaliteiten te benutten. Voeg de volgende naamruimten toe aan het begin van uw code:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Stap 1: CAD-tekening laden

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

// Laad een CAD-tekening in een exemplaar van Image
using (var image = Image.Load(sourceFilePath))
{
    // Hier vindt u uw code voor het laden van de CAD-tekening
}
```

## Stap 2: Maak CadRasterizationOptions

```csharp
// Maak een exemplaar van CadRasterizationOptions
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
```

## Stap 3: Geef lagen op

```csharp
// Voeg de laagnaam toe aan de lagenlijst van CadRasterizationOptions
rasterizationOptions.Layers = new string[] { "LayerA" };
```

## Stap 4: Maak JpegOptions

```csharp
// Maak een exemplaar van JpegOptions (of een ImageOptions voor rasterformaten)
var options = new JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
```

## Stap 5: Exporteren naar JPEG-formaat

```csharp
// Exporteer elke laag naar Jpeg-formaat
MyDir = MyDir + "CADLayersToRasterImageFormats_out.jpg";
image.Save(MyDir, options);
```

## Extra stap: converteer alle lagen

Als u alle lagen wilt converteren, gebruikt u de volgende methode:

```csharp
ConvertAllLayersToRasterImageFormats();
```

Deze methode herhaalt zich over alle lagen in de CAD-tekening, waarbij elke laag naar een afzonderlijk Jpeg-bestand wordt geëxporteerd.

## Conclusie

Gefeliciteerd! U hebt met succes geleerd hoe u CAD-lay-outs kunt exporteren naar rasterafbeeldingsformaten met behulp van Aspose.CAD voor .NET. Deze tutorial biedt een uitgebreide handleiding voor ontwikkelaars die op zoek zijn naar efficiënte en betrouwbare oplossingen voor CAD-conversie.

## Veelgestelde vragen

### Vraag 1: Kan ik andere afbeeldingsformaten gebruiken voor export?

 A1: Ja, dat kan. Gewoon vervangen`JpegOptions` met de opties van het gewenste formaat, zoals`PngOptions` of`BmpOptions`.

### Vraag 2: Is er een proefversie beschikbaar?

 A2: Ja, u kunt de functionaliteit van Aspose.CAD verkennen door de proefversie te downloaden[hier](https://releases.aspose.com/).

### V3: Hoe kan ik ondersteuning krijgen voor Aspose.CAD?

 A3: Bezoek Aspose.CAD[forum](https://forum.aspose.com/c/cad/19) voor gemeenschapsondersteuning of overweeg een licentie aan te schaffen voor specifieke ondersteuning.

### Vraag 4: Zijn er tijdelijke licenties beschikbaar?

 A4: Ja, u kunt een tijdelijke licentie verkrijgen[hier](https://purchase.aspose.com/temporary-license/).

### Vraag 5: Waar kan ik de documentatie vinden?

 A5: Raadpleeg de gedetailleerde documentatie[hier](https://reference.aspose.com/cad/net/).