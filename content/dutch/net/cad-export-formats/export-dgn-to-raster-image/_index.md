---
title: Exporteer DGN naar rasterafbeelding in Aspose.CAD voor .NET
linktitle: Exporteer DGN naar rasterafbeelding
second_title: Aspose.CAD .NET - CAD- en BIM-bestandsindeling
description: Converteer DGN moeiteloos naar rasterafbeeldingen met Aspose.CAD voor .NET. Ontdek de stapsgewijze handleiding en ontketen de kracht van .NET bij het manipuleren van CAD-bestanden.
type: docs
weight: 13
url: /nl/net/cad-export-formats/export-dgn-to-raster-image/
---
## Invoering

In het dynamische domein van .NET-ontwikkeling komt Aspose.CAD naar voren als een krachtig hulpmiddel voor het verwerken van Computer-Aided Design (CAD)-bestanden. Deze tutorial duikt in het proces van het exporteren van DGN-bestanden naar rasterafbeeldingen met Aspose.CAD voor .NET. Als u uw DGN-bestanden naadloos wilt omzetten in visueel aantrekkelijke rasterafbeeldingen, bent u hier aan het juiste adres.

## Vereisten

Voordat we aan deze reis beginnen, moet u ervoor zorgen dat u aan de volgende vereisten voldoet:

-  Aspose.CAD voor .NET: Zorg ervoor dat de Aspose.CAD-bibliotheek in uw .NET-project is geïnstalleerd. U kunt de bibliotheek en relevante documentatie vinden op de[website](https://reference.aspose.com/cad/net/).

- Voorbeeld DGN-bestand: Zorg ervoor dat u een DGN-bestand gereed heeft voor conversie. In ons voorbeeld gebruiken we 'Nikon_D90_Camera.dgn'.

Laten we nu eens in de stapsgewijze handleiding duiken.

## Naamruimten importeren

Begin in uw .NET-project met het importeren van de benodigde naamruimten voor Aspose.CAD. Met deze stap krijgt u toegang tot de klassen en methoden die nodig zijn voor de conversie van DGN naar rasterafbeeldingen.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Stap 1: Laad het DGN-bestand

 Begin met het laden van het DGN-bestand in een`CadImage` voorwerp. Dit vormt een basis voor volgende operaties.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Hier vindt u uw code voor verdere verwerking
}
```

## Stap 2: Definieer rasterisatieopties

 Maak een`CadRasterizationOptions` object en stel verschillende eigenschappen in om het rasterisatieproces aan te passen aan uw vereisten.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## Stap 3: Maak een JpegOptions-object

 Omdat we ernaar streven het DGN-bestand naar JPEG te converteren, maakt u een`JpegOptions` object en wijs het eerder gedefinieerde toe`CadRasterizationOptions` ernaar.

```csharp
ImageOptionsBase options = new JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
```

## Stap 4: Sla de rasterafbeelding op

 Maak gebruik van de`Save` werkwijze van de`CadImage` class om het DGN-bestand te exporteren naar een rasterafbeelding in het gewenste formaat, in dit geval een JPEG.

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpg", options);
```

## Conclusie

Gefeliciteerd! U heeft met succes de stappen doorlopen om een DGN-bestand naar een rasterafbeelding te exporteren met Aspose.CAD voor .NET. Deze tutorial heeft u voorzien van de essentiële kennis om deze functionaliteit moeiteloos in uw .NET-projecten te integreren.

## Veelgestelde vragen

### V1: Kan ik DGN-bestanden exporteren naar andere formaten dan JPEG?

A1: Ja, Aspose.CAD voor .NET ondersteunt verschillende uitvoerformaten. U kunt de opties dienovereenkomstig aanpassen in stap 3.

### Vraag 2 Hoe kan ik omgaan met uitzonderingen tijdens het conversieproces?

A2: Zorg ervoor dat u over de juiste afhandeling van uitzonderingen beschikt, zoals gedemonstreerd in de meegeleverde code, om potentiële problemen aan te pakken.

### V3: Is er een proefversie beschikbaar voor Aspose.CAD voor .NET?

 A3: Ja, u kunt het product uitproberen met een gratis proefperiode. Bezoek[hier](https://releases.aspose.com/) voor meer informatie.

### V4: Waar kan ik hulp zoeken of problemen bespreken die verband houden met Aspose.CAD voor .NET?

 A4: Ga naar de[Aspose.CAD-forum](https://forum.aspose.com/c/cad/19) voor gemeenschapsondersteuning en discussies.

### V5: Hoe verkrijg ik een tijdelijke licentie voor Aspose.CAD voor .NET?

 A5: Bezoek[deze link](https://purchase.aspose.com/temporary-license/)om een tijdelijke licentie aan te schaffen voor uw ontwikkelingsbehoeften.