---
title: Ondersteunde DGN-elementen in Aspose.CAD voor .NET
linktitle: Ondersteunde DGN-elementen
second_title: Aspose.CAD .NET - CAD- en BIM-bestandsindeling
description: Ontdek de krachtige functies van Aspose.CAD voor .NET voor het verwerken van DGN-bestanden. Volg onze stapsgewijze handleiding om naadloos te werken met 2D- en 3D-elementen.
type: docs
weight: 18
url: /nl/net/cad-features-and-support/supported-dgn-elements/
---
## Invoering

Bent u een .NET-ontwikkelaar en wilt u naadloos met DGN-bestanden werken? Aspose.CAD voor .NET biedt een robuuste oplossing om DGN-bestanden efficiënt te verwerken. In deze tutorial gaan we dieper in op de ondersteunde DGN-elementen en begeleiden we u door het proces van het werken met Aspose.CAD voor .NET.

## Vereisten

Voordat we beginnen, zorg ervoor dat u over het volgende beschikt:

- Basiskennis van .NET-programmering.
- Visual Studio is op uw computer geïnstalleerd.
-  Aspose.CAD voor .NET-bibliotheek, die u kunt downloaden[hier](https://releases.aspose.com/cad/net/).

## Naamruimten importeren

Om uw project een vliegende start te geven, importeert u de benodigde naamruimten in uw .NET-applicatie. Deze stap zorgt ervoor dat u toegang heeft tot de functionaliteiten van Aspose.CAD voor .NET.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.FileFormats.Dgn.DgnElements;
```

## Stap 1: Laad het DGN-bestand

Begin met het laden van een bestaand DGN-bestand als CadImage in uw .NET-applicatie.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Jouw code hier
}
```

## Stap 2: Herhaal de DGN-elementen

Doorloop de DGN-elementen met behulp van een foreach-lus. Aspose.CAD voor .NET biedt een verscheidenheid aan DGN-elementtypen waarmee u kunt werken.

```csharp
foreach (DgnDrawingElementBase element in dgnImage.Elements)
{
    // Jouw code hier
}
```

## Stap 3: Eerder ondersteunde entiteiten verwerken

Behandel de voorheen ondersteunde 2D-entiteiten, die nu ook voor 3D worden ondersteund.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.Line:
    case DgnElementType.Ellipse:
    case DgnElementType.Curve:
    // Extra gevallen
        {
            // Jouw code hier
            break;
        }
}
```

## Stap 4: Ondersteunde 3D-entiteiten verwerken

Verwerk de ondersteunde 3D-entiteiten van Aspose.CAD voor .NET.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.SolidHeader3D:
    case DgnElementType.Cone:
    case DgnElementType.CellHeader:
        {
            // Jouw code hier
            break;
        }
}
```

## Stap 5: Exporteren en opslaan

Exporteer ten slotte het gewijzigde DGN-bestand naar een rasterafbeelding en sla het op in de opgegeven map.

```csharp
Console.WriteLine("\nThe DGN file exported successfully to raster image.\nFile saved at " + MyDir);
```

## Conclusie

In deze zelfstudie hebben we de mogelijkheden van Aspose.CAD voor .NET onderzocht bij het verwerken en manipuleren van DGN-bestanden. Door de stapsgewijze handleiding te volgen, kunt u efficiënt werken met ondersteunde DGN-elementen, of het nu 2D- of 3D-entiteiten zijn. Met Aspose.CAD voor .NET kunt u de verwerking van DGN-bestanden naadloos integreren in uw .NET-toepassingen.

## Veelgestelde vragen

### V1: Waar kan ik de documentatie voor Aspose.CAD voor .NET vinden?

 A1: U kunt de documentatie vinden[hier](https://reference.aspose.com/cad/net/).

### V2: Hoe download ik Aspose.CAD voor .NET?

 A2: U kunt de bibliotheek downloaden[hier](https://releases.aspose.com/cad/net/).

### V3: Is er een gratis proefversie beschikbaar voor Aspose.CAD voor .NET?

 A3: Ja, u heeft toegang tot de gratis proefperiode[hier](https://releases.aspose.com/).

### V4: Waar kan ik tijdelijke licenties krijgen voor Aspose.CAD voor .NET?

 A4: Er zijn tijdelijke licenties beschikbaar[hier](https://purchase.aspose.com/temporary-license/).

### Q5: Hulp nodig of vragen?

 A5: Bezoek de Aspose.CAD voor .NET-community[Helpforum](https://forum.aspose.com/c/cad/19).