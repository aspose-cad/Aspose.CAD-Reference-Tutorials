---
title: Ondersteuning voor DGN V7 in Aspose.CAD voor .NET
linktitle: Ondersteuning voor DGN V7
second_title: Aspose.CAD .NET - CAD- en BIM-bestandsindeling
description: Ontdek de naadloze ondersteuning van Aspose.CAD voor .NET voor DGN V7. Converteer DGN-bestanden moeiteloos naar rasterafbeeldingen met stapsgewijze begeleiding.
type: docs
weight: 19
url: /nl/net/cad-features-and-support/support-for-dgn-v7/
---
## Invoering

Op het gebied van .NET-ontwikkeling onderscheidt Aspose.CAD zich als een krachtige bibliotheek voor het verwerken van Computer-Aided Design (CAD)-bestanden. Deze tutorial gaat dieper in op een specifieke functie van Aspose.CAD voor .NET: ondersteuning voor DGN V7-bestanden. DGN, afkorting van Design, is een veelgebruikt bestandsformaat in het CAD-domein. Aspose.CAD vereenvoudigt het werken met DGN V7-bestanden en biedt ontwikkelaars een naadloze ervaring.

## Vereisten

Voordat we ingaan op de implementatie, moet u ervoor zorgen dat u aan de volgende vereisten voldoet:

-  Aspose.CAD voor .NET: Zorg ervoor dat de Aspose.CAD-bibliotheek is geïnstalleerd. Je kunt het downloaden van de[website](https://releases.aspose.com/cad/net/).

- Ontwikkelomgeving: Zet een werkende .NET-ontwikkelomgeving op, inclusief Visual Studio of een andere gewenste IDE.

Nu we de vereisten op orde hebben, gaan we kijken hoe we de ondersteuning voor DGN V7 in Aspose.CAD voor .NET kunnen benutten.

## Naamruimten importeren

Begin met het importeren van de benodigde naamruimten om toegang te krijgen tot de functionaliteit van Aspose.CAD:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Stap 1: Laad het DGN-bestand

 Begin met het laden van een bestaand DGN-bestand als`CadImage` Vervangen`"Your Document Directory"` En`"Nikon_D90_Camera.dgn"` met het juiste mappad en de juiste bestandsnaam.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Code voor verdere stappen vindt u hier...
}
```

## Stap 2: Configureer rasterisatieopties

 Maak een`CadRasterizationOptions` object om verschillende eigenschappen met betrekking tot rastering te definiëren en in te stellen.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions
{
    PageWidth = 600,
    PageHeight = 300,
    NoScaling = true,
    AutomaticLayoutsScaling = false
};
```

## Stap 3: Stel opties voor vectorrasterisatie in

 Maak een`JpegOptions` object omdat we van plan zijn het DGN-bestand naar JPEG te converteren. Wijs het eerder gemaakte toe`CadRasterizationOptions` er bezwaar tegen maken.

```csharp
ImageOptionsBase options = new JpegOptions
{
    VectorRasterizationOptions = rasterizationOptions
};
```

## Stap 4: Sla de gerasterde afbeelding op

 Bel de`Save` werkwijze van de`CadImage` class-object om het DGN-bestand naar een rasterafbeelding te exporteren, in dit geval een JPEG.

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpeg", options);
```

Nadat deze stappen zijn voltooid, wordt het DGN-bestand met succes geëxporteerd naar een rasterafbeelding.

## Conclusie

In deze tutorial hebben we de naadloze ondersteuning voor DGN V7 in Aspose.CAD voor .NET onderzocht. Door de stapsgewijze handleiding te volgen, kunnen ontwikkelaars DGN-bestanden moeiteloos naar rasterafbeeldingen converteren, waardoor de mogelijkheden van hun .NET-applicaties worden uitgebreid.

## Veelgestelde vragen

### V1: Is Aspose.CAD compatibel met de nieuwste DGN V7-specificaties?

A1: Ja, Aspose.CAD is ontworpen om DGN V7-bestanden naadloos te verwerken, waardoor compatibiliteit met de nieuwste specificaties wordt gegarandeerd.

### V2: Kan ik de rasteropties voor DGN-bestandsconversie aanpassen?

 A2: Absoluut. In de zelfstudie wordt gedemonstreerd hoe u`CadRasterizationOptions` om het conversieproces op maat te maken.

### Vraag 3: Zijn er naast JPEG nog andere ondersteunde uitvoerformaten?

A3: Ja, Aspose.CAD ondersteunt verschillende uitvoerformaten. U kunt de documentatie raadplegen voor een uitgebreide lijst.

### V4: Hoe kan ik ondersteuning krijgen voor Aspose.CAD-gerelateerde vragen?

 A4: Bezoek de[Aspose.CAD-forum](https://forum.aspose.com/c/cad/19) voor gemeenschapsondersteuning en discussies.

### V5: Is er een gratis proefversie beschikbaar voor Aspose.CAD voor .NET?

 A5: Ja, u heeft toegang tot een gratis proefperiode[hier](https://releases.aspose.com/).