---
title: CAD-tekeninggrootte aanpassen in Aspose.CAD voor .NET
linktitle: De grootte van de CAD-tekening aanpassen
second_title: Aspose.CAD .NET - CAD- en BIM-bestandsindeling
description: Leer hoe u moeiteloos CAD-tekeningformaten in .NET kunt aanpassen met Aspose.CAD. Volg onze stapsgewijze handleiding voor het naadloos aanpassen van het formaat.
type: docs
weight: 10
url: /nl/net/cad-drawing-manipulation/adjust-cad-drawing-size/
---
## Invoering

Wilt u de grootte van CAD-tekeningen naadloos aanpassen in uw .NET-applicaties? Aspose.CAD voor .NET biedt een robuuste oplossing waarmee u moeiteloos het formaat van CAD-tekeningen kunt wijzigen. In deze zelfstudie begeleiden we u door het proces, waarbij we elke stap opsplitsen, zodat u de fijne kneepjes van het formaat van CAD-tekeningen met Aspose.CAD begrijpt.

## Vereisten

Voordat we ingaan op de tutorial, zorg ervoor dat je aan de volgende vereisten voldoet:

- Aspose.CAD voor .NET-bibliotheek: Download en installeer de bibliotheek van de .NET-bibliotheek[Aspose.CAD voor .NET-downloadpagina](https://releases.aspose.com/cad/net/).
- Voorbeeld-CAD-tekening: Zorg ervoor dat u een voorbeeld-CAD-tekeningbestand (bijvoorbeeld "sample.dwg") in uw documentmap hebt.

## Naamruimten importeren

Begin met het importeren van de benodigde naamruimten in uw .NET-applicatie. Deze stap is cruciaal om toegang te krijgen tot de functionaliteiten van Aspose.CAD voor .NET.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Stap 1: CAD-tekening laden

Begin met het laden van de CAD-tekening in een exemplaar van de klasse Aspose.CAD.Image. Zorg ervoor dat u het juiste bestandspad voor uw voorbeeldtekening heeft.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "sample.dwg";

// Laad een CAD-tekening in een exemplaar van Image
using (var image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // Jouw code hier...
}
```

## Stap 2: Maak BmpOptions

Maak een exemplaar van de klasse BmpOptions, die verantwoordelijk is voor het opgeven van opties bij het opslaan van de CAD-tekening als een BMP-bestand.

```csharp
Aspose.CAD.ImageOptions.BmpOptions bmpOptions = new Aspose.CAD.ImageOptions.BmpOptions();
```

## Stap 3: Stel CadRasterizationOptions in

Instantieer de klasse CadRasterizationOptions en configureer de eigenschappen ervan voor vectorrasterisatie.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions cadRasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
bmpOptions.VectorRasterizationOptions = cadRasterizationOptions;
```

## Stap 4: Stel de UnitType-eigenschap in

Stel de eigenschap UnitType van CadRasterizationOptions in om het eenheidstype op te geven waarvan de grootte moet worden gewijzigd. In dit voorbeeld is deze ingesteld op Centimeter.

```csharp
cadRasterizationOptions.UnitType = Aspose.CAD.ImageOptions.UnitType.Centimeter;
```

## Stap 5: Stel de lay-outeigenschap in

Geef de lay-outs op die u in de tekening met gewijzigd formaat wilt opnemen door de eigenschap Layouts in te stellen.

```csharp
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## Stap 6: Exporteren naar BMP

Sla ten slotte de gewijzigde lay-out op als een BMP-bestand met behulp van de Save-methode.

```csharp
string outPath = sourceFilePath + ".bmp";
image.Save(outPath, bmpOptions);
```

Nu hebt u met succes de grootte van uw CAD-tekening aangepast met Aspose.CAD voor .NET!

## Conclusie

In deze zelfstudie hebben we het proces doorlopen van het wijzigen van de grootte van CAD-tekeningen in .NET met behulp van Aspose.CAD. Door deze stappen te volgen, kunt u deze functionaliteit naadloos in uw applicaties integreren, waardoor een soepele gebruikerservaring ontstaat.

## Veelgestelde vragen

### V1: Is Aspose.CAD voor .NET compatibel met alle CAD-formaten?

 A1: Aspose.CAD voor .NET ondersteunt een breed scala aan CAD-formaten, waaronder DWG, DXF, DWF en meer. Controleer de[documentatie](https://reference.aspose.com/cad/net/) voor de volledige lijst.

### Vraag 2: Kan ik het formaat van meerdere lay-outs tegelijk wijzigen?

A2: Ja, u kunt het formaat van meerdere lay-outs wijzigen door de lay-outmatrix in CadRasterizationOptions aan te passen.

### V3: Waar kan ik ondersteuning krijgen voor Aspose.CAD voor .NET?

 A3: Bezoek de[Aspose.CAD-forum](https://forum.aspose.com/c/cad/19) voor steun en hulp van de gemeenschap.

### Vraag 4: Is er een gratis proefversie beschikbaar?

 A4: Ja, u kunt een[gratis proefperiode](https://releases.aspose.com/) om de functies van Aspose.CAD voor .NET te evalueren.

### V5: Hoe kan ik een tijdelijke licentie verkrijgen voor Aspose.CAD voor .NET?

 A5: Verkrijg een tijdelijke licentie voor testdoeleinden[hier](https://purchase.aspose.com/temporary-license/).