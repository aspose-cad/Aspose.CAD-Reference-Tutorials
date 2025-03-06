---
title: Ondersteuning van 3D voor DGN V7 in Aspose.CAD voor .NET
linktitle: Ondersteuning van 3D voor DGN V7
second_title: Aspose.CAD .NET - CAD- en BIM-bestandsindeling
description: Ontgrendel de kracht van 3D-ondersteuning voor DGN V7 in Aspose.CAD voor .NET. Volg onze stap-voor-stap handleiding.
weight: 20
url: /nl/net/cad-features-and-support/support-of-3d-for-dgn-v7/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ondersteuning van 3D voor DGN V7 in Aspose.CAD voor .NET

## Invoering

Welkom bij onze uitgebreide tutorial over het benutten van de ondersteuning van 3D voor DGN V7 in Aspose.CAD voor .NET! Aspose.CAD is een krachtige bibliotheek waarmee ontwikkelaars naadloos kunnen werken met CAD-bestanden in hun .NET-applicaties. In deze zelfstudie verkennen we de stappen om 3D-ondersteuning voor DGN V7 te gebruiken, waardoor u de kennis krijgt om uw CAD-gerelateerde projecten te verbeteren.

## Vereisten

Voordat u in de zelfstudie duikt, moet u ervoor zorgen dat u aan de volgende vereisten voldoet:

-  Aspose.CAD voor .NET: Zorg ervoor dat Aspose.CAD voor .NET is geïnstalleerd. Als dit niet het geval is, kunt u deze downloaden van[hier](https://releases.aspose.com/cad/net/).

- Ontwikkelomgeving: Zet een geschikte ontwikkelomgeving op, zoals Visual Studio, voor de ontwikkeling van .NET-applicaties.

- Voorbeeld-DGN-bestand: Zorg ervoor dat u een voorbeeld-DGN-bestand gereed heeft om te testen. U kunt het meegeleverde voorbeeldbestand "Nikon_D90_Camera.dgn" gebruiken.

Laten we nu eens kijken naar de stappen om 3D-ondersteuning voor DGN V7 te bereiken met behulp van Aspose.CAD voor .NET!

## Naamruimten importeren

Begin in uw .NET-applicatie met het importeren van de benodigde naamruimten:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.ImageOptions;
```

## Stap 1: Stel uw documentenmap in

 Zorg ervoor dat er een documentmap is ingesteld in uw project. Vervangen`"Your Document Directory"` met het daadwerkelijke pad naar uw documentmap.

```csharp
string MyDir = "Your Document Directory";
```

## Stap 2: Laad het DGN-bestand

Laad het bestaande DGN-bestand als CadImage met behulp van de volgende code:

```csharp
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";
string outFile = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Hier vindt u uw code voor verdere verwerking
}
```

## Stap 3: Configureer PDF-exportopties

Stel opties in voor het exporteren naar PDF en geef opties voor vectorrastering op, zoals pagina-afmetingen, automatische schaling van lay-outs, achtergrondkleur en te exporteren lay-outs.

```csharp
var options = new PdfOptions
{
    VectorRasterizationOptions = new CadRasterizationOptions
    {
        PageWidth = 1500,
        PageHeight = 1500,
        AutomaticLayoutsScaling = true,
        BackgroundColor = Color.Black,
        Layouts = new string[] { "1", "2", "3", "9" } // Exporteer alleen gespecificeerde weergaven
    }
};
```

## Stap 4: Sla de rasterafbeelding op

Sla het DGN-bestand op als rasterafbeelding met de geconfigureerde opties.

```csharp
dgnImage.Save(outFile, options);
```

## Conclusie

Gefeliciteerd! U hebt Aspose.CAD voor .NET met succes gebruikt om een DGN-bestand met 3D-ondersteuning naar een rasterafbeelding te exporteren. Deze tutorial heeft u voorzien van de essentiële stappen om deze functionaliteit in uw CAD-projecten te integreren.

## Veelgestelde vragen

### V1: Kan ik Aspose.CAD voor .NET gebruiken met andere CAD-bestandsindelingen?

A1: Ja, Aspose.CAD ondersteunt verschillende CAD-bestandsformaten, waaronder DWG en DXF.

### Vraag 2: Hoe kan ik omgaan met uitzonderingen bij het werken met Aspose.CAD?

A2: Verpak uw code in een try-catch-blok, zoals gedemonstreerd in het gegeven voorbeeld, om uitzonderingen netjes af te handelen.

### Vraag 3: Is Aspose.CAD geschikt voor commerciële projecten?

 A3: Absoluut! U kunt Aspose.CAD voor .NET aanschaffen[hier](https://purchase.aspose.com/buy).

### V4: Kan ik Aspose.CAD voor .NET uitproberen voordat ik een aankoop doe?

A4: Zeker! Ontdek de gratis proefperiode[hier](https://releases.aspose.com/).

### V5: Waar kan ik community-ondersteuning vinden voor Aspose.CAD voor .NET?

 A5: Bezoek het communityforum[hier](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
