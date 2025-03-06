---
title: Converteer lay-outs naar rasterafbeelding in Aspose.CAD voor .NET
linktitle: Converteer lay-outs naar rasterafbeelding
second_title: Aspose.CAD .NET - CAD- en BIM-bestandsindeling
description: Converteer CAD-lay-outs moeiteloos naar rasterafbeeldingen met Aspose.CAD voor .NET. Verbeter uw ontwikkeling met krachtige CAD-manipulatiemogelijkheden.
weight: 12
url: /nl/net/cad-drawing-manipulation/convert-layouts-to-raster-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Converteer lay-outs naar rasterafbeelding in Aspose.CAD voor .NET

## Invoering

Wilt u lay-outs moeiteloos omzetten naar rasterafbeeldingen in uw .NET-applicaties? Zoek niet verder! Deze stapsgewijze handleiding leidt u door het proces met Aspose.CAD voor .NET, een krachtige bibliotheek die Computer-Aided Design (CAD)-taken vereenvoudigt.

## Vereisten

Voordat u in de zelfstudie duikt, moet u ervoor zorgen dat u aan de volgende vereisten voldoet:

- Aspose.CAD voor .NET-bibliotheek: Download en installeer de bibliotheek van de .NET-bibliotheek[Aspose.CAD voor .NET-downloadpagina](https://releases.aspose.com/cad/net/).

- Ontwikkelomgeving: Zorg ervoor dat er een werkende .NET-ontwikkelomgeving op uw computer is geïnstalleerd.

- Te converteren document: bereid een CAD-document voor dat de lay-outs bevat die u naar rasterafbeeldingen wilt converteren.

- Uw documentenmap: Vervang de tijdelijke aanduiding "Uw documentenmap" in de code door het pad naar uw documentmap.

## Naamruimten importeren

Laten we eerst de benodigde naamruimten importeren om de Aspose.CAD-functionaliteiten toegankelijk te maken in uw code.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Stap 1: Laad het CAD-document

Begin met het laden van het CAD-document met behulp van de Aspose.CAD-bibliotheek.

```csharp
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image image = Image.Load(sourceFilePath))
{
    //Hier vindt u uw code voor verdere stappen
}
```

## Stap 2: Configureer rasterisatieopties

 Maak een exemplaar van`CadRasterizationOptions` om de paginabreedte en -hoogte in te stellen en de lay-outs op te geven die u wilt converteren.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1200;
rasterizationOptions.PageHeight = 1200;
rasterizationOptions.Layouts = new string[] { "Model", "Layout1" };
```

## Stap 3: Stel TiffOptions in voor de resulterende afbeelding

 Maak een exemplaar van`TiffOptions`om het formaat van de resulterende afbeelding te definiëren.

```csharp
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.VectorRasterizationOptions = rasterizationOptions;
```

## Stap 4: Sla de resulterende afbeelding op

Geef het uitvoerpad op en sla de geconverteerde afbeelding op.

```csharp
string outputFilePath = MyDir + "conic_pyramid_layoutstorasterimage_out.tiff";
image.Save(outputFilePath, options);
```

## Conclusie

Gefeliciteerd! U hebt CAD-lay-outs met succes geconverteerd naar een rasterafbeeldingsindeling met behulp van Aspose.CAD voor .NET. De mogelijkheden zijn enorm en deze gids dient als startpunt voor uw CAD-gerelateerde inspanningen.

## Veelgestelde vragen

### Vraag 1: Is Aspose.CAD compatibel met alle CAD-formaten?

 A1: Aspose.CAD ondersteunt een breed scala aan CAD-formaten, waaronder DWG, DXF, DWF, STL en meer. Controleer de[documentatie](https://reference.aspose.com/cad/net/) voor een uitgebreide lijst.

### V2: Hoe kan ik een tijdelijke licentie voor Aspose.CAD verkrijgen?

 A2: Bezoek de[tijdelijke licentiepagina](https://purchase.aspose.com/temporary-license/) het verkrijgen van een tijdelijke licentie voor test- en evaluatiedoeleinden.

### V3: Waar kan ik ondersteuning vinden voor Aspose.CAD?

 A3: Forums zijn een geweldige plek om hulp te zoeken. Bezoek de[Aspose.CAD-forum](https://forum.aspose.com/c/cad/19) om verbinding te maken met de gemeenschap en hulp te krijgen.

### V4: Kan ik Aspose.CAD gratis uitproberen?

 A4: Absoluut! Grijp uw[gratis proefperiode](https://releases.aspose.com/) om de functies en mogelijkheden van Aspose.CAD te verkennen.

### V5: Waar kan ik een licentie voor Aspose.CAD kopen?

 A5: Navigeer naar de[aankooppagina](https://purchase.aspose.com/buy) om een licentie te kopen en het volledige potentieel van Aspose.CAD te ontsluiten.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
