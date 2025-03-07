---
title: Underlay-vlaggen van DWG-bestanden verkennen - Aspose.CAD-zelfstudie
linktitle: Underlay-vlaggen van DWG-bestanden verkennen
second_title: Aspose.CAD .NET - CAD- en BIM-bestandsindeling
description: Ontgrendel de kracht van Aspose.CAD voor .NET bij het verkennen van underlay-vlaggen voor DWG-bestanden. Volg onze stapsgewijze handleiding.
weight: 13
url: /nl/net/dwg-file-manipulation/exploring-underlay-flags-of-dwg/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Underlay-vlaggen van DWG-bestanden verkennen - Aspose.CAD-zelfstudie

## Invoering

Als u zich verdiept in de ingewikkelde wereld van CAD-bestanden, met name DWG-bestanden, en u de mysteries van onderlegvlaggen wilt ontrafelen, bent u hier op de juiste plek. Deze tutorial begeleidt u bij het verkennen van underlay-vlaggen in DWG-bestanden met behulp van de krachtige Aspose.CAD voor .NET-bibliotheek.

## Vereisten

Voordat we ingaan op de tutorial, zorg ervoor dat je over het volgende beschikt:

- Een basiskennis van programmeren in C# en .NET.
-  Aspose.CAD voor .NET-bibliotheek geïnstalleerd. Zo niet, dan kunt u deze downloaden[hier](https://releases.aspose.com/cad/net/).
- Een DWG-bestand om te testen. U kunt het voorbeeldbestand "BlockRefDgn.dwg" uit de zelfstudie gebruiken.

## Naamruimten importeren

Om aan de slag te gaan, moet u de benodigde naamruimten importeren. Hier is een fragment om u te helpen:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;

```

## Stap 1: Laad het DWG-bestand en converteer naar CadImage

Begin met het laden van het bestaande DWG-bestand en het converteren ervan naar een CadImage:

```csharp
string fileName = MyDir + "BlockRefDgn.dwg";

// Laad het DWG-bestand en converteer naar CadImage
using (CadImage image = (CadImage)Image.Load(fileName))
{
    // Uw code voor de volgende stappen komt hier terecht
}
```

## Stap 2: Herhaal de entiteiten

Herhaal vervolgens elke entiteit in het DWG-bestand:

```csharp
foreach (CadBaseEntity entity in image.Entities)
{
    // Uw code voor de volgende stappen komt hier terecht
}
```

## Stap 3: Controleer op CadDgnUnderlay-type

Controleer of de entiteit van het type CadDgnUnderlay is:

```csharp
if (entity is CadDgnUnderlay)
{
    // Uw code voor de volgende stappen komt hier terecht
}
```

## Stap 4: Toegang tot ondervloervlaggen

Krijg toegang tot verschillende ondervloervlaggen en extraheer relevante informatie:

```csharp
CadUnderlay underlay = entity as CadUnderlay;

Console.WriteLine(underlay.UnderlayPath);
Console.WriteLine(underlay.UnderlayName);
Console.WriteLine(underlay.InsertionPoint.X);
Console.WriteLine(underlay.InsertionPoint.Y);
Console.WriteLine(underlay.RotationAngle);
Console.WriteLine(underlay.ScaleX);
Console.WriteLine(underlay.ScaleY);
Console.WriteLine(underlay.ScaleZ);
Console.WriteLine((underlay.Flags & UnderlayFlags.UnderlayIsOn) == UnderlayFlags.UnderlayIsOn);
Console.WriteLine((underlay.Flags & UnderlayFlags.ClippingIsOn) == UnderlayFlags.ClippingIsOn);
Console.WriteLine((underlay.Flags & UnderlayFlags.Monochrome) != UnderlayFlags.Monochrome);
```

## Conclusie

Gefeliciteerd! U hebt met succes de underlay-vlaggen van DWG-bestanden verkend met Aspose.CAD voor .NET. Deze tutorial heeft u de kennis gegeven om door entiteiten te navigeren en cruciale informatie over underlays te extraheren.

## Veelgestelde vragen

### V1: Kan ik Aspose.CAD voor .NET gebruiken met andere CAD-bestandsindelingen?

A1: Aspose.CAD ondersteunt verschillende CAD-formaten, waaronder DWG, DXF, DGN en meer. Raadpleeg de documentatie voor de volledige lijst.

### V2: Is er een tijdelijke licentie beschikbaar voor Aspose.CAD voor .NET?

 A2: Ja, u kunt een tijdelijke licentie verkrijgen[hier](https://purchase.aspose.com/temporary-license/).

### V3: Waar kan ik ondersteuning vinden voor Aspose.CAD voor .NET?

 A3: Bezoek het ondersteuningsforum[hier](https://forum.aspose.com/c/cad/19) Voor assistentie.

### V4: Hoe koop ik Aspose.CAD voor .NET?

A4: Koop de bibliotheek[hier](https://purchase.aspose.com/buy).

### Vraag 5: Is er een gratis proefversie beschikbaar?

 A5: Ja, u heeft toegang tot de gratis proefperiode[hier](https://releases.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
