---
title: Canvasgrootte en -modus instellen in Aspose.CAD voor .NET
linktitle: Canvasgrootte en -modus instellen
second_title: Aspose.CAD .NET - CAD- en BIM-bestandsindeling
description: Verken de stapsgewijze handleiding voor het instellen van de canvasgrootte en -modus in Aspose.CAD voor .NET. Optimaliseer uw CAD-weergave eenvoudig met behulp van deze uitgebreide tutorial.
type: docs
weight: 16
url: /nl/net/cad-features-and-support/setting-canvas-size-and-mode/
---
## Invoering

Bent u klaar om het volledige potentieel van Aspose.CAD voor .NET te ontsluiten en een revolutie teweeg te brengen in uw CAD-renderingervaring? In deze stapsgewijze zelfstudie verdiepen we ons in de fijne kneepjes van het instellen van de canvasgrootte en -modus met behulp van de krachtige Aspose.CAD-bibliotheek. Of u nu een doorgewinterde ontwikkelaar bent of net begint, deze gids leidt u door het proces en zorgt ervoor dat u de mogelijkheden van Aspose.CAD effectief kunt benutten.

## Vereisten

Voordat we ingaan op de tutorial, zorg ervoor dat je aan de volgende vereisten voldoet:

-  Aspose.CAD-bibliotheek: Download en installeer de Aspose.CAD-bibliotheek van de[Aspose.CAD-website](https://releases.aspose.com/cad/net/).

- Ontwikkelomgeving: Zorg ervoor dat er een .NET-ontwikkelomgeving op uw computer is geïnstalleerd.

-  Voorbeeld van een CAD-bestand: voor deze zelfstudie gebruiken we een voorbeeld van een DXF-bestand. Je vindt er een in de[Aspose.CAD-documentatie](https://reference.aspose.com/cad/net/).

## Naamruimten importeren

Importeer om te beginnen de benodigde naamruimten aan het begin van uw .NET-applicatie:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Stap 1: CAD-bestand laden

Begin met het laden van het CAD-bestand met behulp van de volgende code:

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    //Hier vindt u uw code voor verdere stappen
}
```

## Stap 2: Maak CadRasterizationOptions

 Maak een exemplaar van`CadRasterizationOptions` en stel de eigenschappen in:

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
rasterizationOptions.NoScaling = false;
```

## Stap 3: Maak PdfOptions

 Maak een exemplaar van`PdfOptions` en stel zijn`VectorRasterizationOptions` eigendom:

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Stap 4: Exporteren naar PDF

Exporteer het CAD-bestand naar PDF met behulp van de geconfigureerde opties:

```csharp
image.Save(MyDir + "result_out.pdf", pdfOptions);
```

## Stap 5: Maak TiffOptions

 Maak een exemplaar van`TiffOptions` en stel zijn`VectorRasterizationOptions` eigendom:

```csharp
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Stap 6: Exporteren naar TIFF

Exporteer het CAD-bestand naar TIFF met behulp van de geconfigureerde opties:

```csharp
image.Save(MyDir + "result_out.tiff", tiffOptions);
```

## Conclusie

Gefeliciteerd! U hebt de canvasgrootte en -modus met succes ingesteld in Aspose.CAD voor .NET. Deze krachtige functie opent een wereld aan mogelijkheden voor CAD-weergave. Experimenteer met verschillende opties en ontdek het volledige potentieel van Aspose.CAD in uw .NET-toepassingen.

## Veelgestelde vragen

### V1: Kan ik Aspose.CAD gebruiken met andere .NET-bibliotheken?

A1: Ja, Aspose.CAD kan naadloos worden geïntegreerd met andere .NET-bibliotheken, waardoor verbeterde mogelijkheden voor CAD-manipulatie worden geboden.

### V2: Is er een gratis proefversie beschikbaar voor Aspose.CAD?

 A2: Ja, u kunt de functies van Aspose.CAD verkennen met een gratis proefperiode. Bezoek[hier](https://releases.aspose.com/) starten.

### V3: Hoe kan ik ondersteuning krijgen voor Aspose.CAD?

 A3: Bezoek voor ondersteuning en discussies de[Aspose.CAD-forum](https://forum.aspose.com/c/cad/19).

### V4: Waar kan ik uitgebreide documentatie voor Aspose.CAD vinden?

 A4: Raadpleeg de[Aspose.CAD-documentatie](https://reference.aspose.com/cad/net/) voor gedetailleerde informatie en voorbeelden.

### V5: Hoe koop ik Aspose.CAD voor .NET?

 A5: Om Aspose.CAD te kopen, gaat u naar de[aankooppagina](https://purchase.aspose.com/buy).