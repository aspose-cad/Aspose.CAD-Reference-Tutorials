---
date: 2026-04-09
description: Leer hoe je DWG naar afbeelding kunt converteren en hoe je onderlegger‑vlaggen
  kunt lezen met Aspose.CAD voor .NET in deze stapsgewijze handleiding.
keywords:
- convert dwg to image
- how to read underlay
- Aspose.CAD DWG underlay flags
linktitle: Verkennen van onderleggervlaggen van DWG‑bestanden
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: DWG naar afbeelding converteren – Onderleggervlaggen van DWG‑bestanden verkennen
  – Aspose.CAD‑tutorial
url: /nl/net/dwg-file-manipulation/exploring-underlay-flags-of-dwg/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Verkennen van Underlay‑vlaggen van DWG‑bestanden - Aspose.CAD‑tutorial

## Inleiding

Als je je verdiept in de complexe wereld van CAD‑bestanden, specifiek DWG‑bestanden, en je wilt **DWG naar afbeelding converteren** terwijl je ook **onderlaag‑vlaggen** wilt lezen, ben je hier aan het juiste adres. Deze tutorial leidt je stap voor stap door het gebruik van de krachtige Aspose.CAD for .NET‑bibliotheek, zodat je onderlaag‑informatie kunt extraheren en de tekening met vertrouwen als afbeelding kunt renderen.

## Snelle antwoorden
- **Wat betekent “convert DWG to image”?**  
  Het betekent het renderen van een DWG‑tekening naar een rasterformaat (PNG, JPEG, enz.) met behulp van Aspose.CAD.
- **Welke methode onthult underlay‑vlaggen?**  
  Toegang tot de `Flags`‑eigenschap van het `CadUnderlay`‑object na het laden van de DWG.
- **Heb ik een licentie nodig voor Aspose.CAD?**  
  Een tijdelijke licentie is beschikbaar voor evaluatie; een volledige licentie is vereist voor productie.
- **Welke .NET‑versies worden ondersteund?**  
  .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6 en later.
- **Kan ik onderlaag‑geometrie extraheren?**  
  Ja – het onderlaagpad, het invoerpunt, de schaal, rotatie en vlag‑toestanden zijn allemaal toegankelijk.

## Wat is “convert DWG to image” en waarom is het belangrijk?

Een DWG‑bestand naar een afbeelding converteren stelt je in staat CAD‑tekeningen weer te geven in browsers, in rapporten in te sluiten of te delen met belanghebbenden die geen CAD‑viewer hebben. Tijdens het renderen moet je vaak **underlay**‑objecten (bijv. DGN‑referenties) inspecteren om te zorgen dat ze correct verschijnen. Het begrijpen van de onderlaag‑vlaggen helpt je bij het oplossen van problemen met bijsnijden, monochroom renderen en zichtbaarheid voordat je de uiteindelijke afbeelding genereert.

## Voorvereisten

- Een basisbegrip van C#‑ en .NET‑programmering.  
- **Aspose.CAD for .NET**‑bibliotheek geïnstalleerd. Als je die nog niet hebt, download deze **[hier](https://releases.aspose.com/cad/net/)**.  
- Een DWG‑bestand voor testen – het voorbeeldbestand **“BlockRefDgn.dwg”** wordt door de hele gids gebruikt.

## Namespaces importeren

Om te beginnen, importeer de benodigde namespaces:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Stap 1: DWG‑bestand laden en converteren naar `CadImage`

Eerst laad je het DWG‑bestand en cast je het naar een `CadImage`. Dit object geeft je toegang tot alle teken‑entiteiten, inclusief onderlagen.

```csharp
string fileName = MyDir + "BlockRefDgn.dwg";

// Load DWG file and convert to CadImage
using (CadImage image = (CadImage)Image.Load(fileName))
{
    // Your code for subsequent steps will go here
}
```

## Stap 2: Door entiteiten itereren

Vervolgens loop je door elke entiteit in de tekening. Hier vind je de onderlaag‑objecten.

```csharp
foreach (CadBaseEntity entity in image.Entities)
{
    // Your code for subsequent steps will go here
}
```

## Stap 3: Controleren op type `CadDgnUnderlay`

Identificeer onderlaag‑entiteiten door hun runtime‑type te controleren. De `CadDgnUnderlay`‑klasse vertegenwoordigt DGN‑onderlagen die in een DWG zijn ingebed.

```csharp
if (entity is CadDgnUnderlay)
{
    // Your code for subsequent steps will go here
}
```

## Stap 4: Toegang tot underlay‑vlaggen

Zodra je een `CadDgnUnderlay` hebt, cast je deze naar `CadUnderlay` om zijn eigenschappen en vlag‑toestanden te lezen. De vlaggen geven aan of de onderlaag zichtbaar, bijgesneden of in monochroom wordt gerenderd.

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

### Wat de output aangeeft

- **UnderlayPath / UnderlayName** – waar het externe DGN‑bestand zich bevindt.  
- **InsertionPoint (X, Y)** – coördinaten waar de onderlaag in de DWG‑ruimte wordt geplaatst.  
- **RotationAngle** – rotatie toegepast op de onderlaag.  
- **ScaleX / ScaleY / ScaleZ** – schaalfactoren voor elke as.  
- **Flags** – booleaanse waarden die zichtbaarheid (`UnderlayIsOn`), bijsnijden (`ClippingIsOn`) en monochroom renderen (`Monochrome`) aangeven.

## Veelvoorkomende problemen & oplossingen

| Issue | Reason | Fix |
|-------|--------|-----|
| Geen output voor vlagcontroles | Underlay‑vlaggen worden standaard op 0 gezet wanneer de onderlaag is uitgeschakeld. | Zorg ervoor dat de DWG daadwerkelijk een actieve onderlaag bevat of schakel de zichtbaarheid in het bron‑CAD‑bestand in. |
| `Invalid cast`‑exception | Het object is geen `CadDgnUnderlay`. | Controleer de `if (entity is CadDgnUnderlay)`‑voorwaarde vóór het casten. |
| Afbeeldingsrendering mislukt na vlagextractie | De onderlaag kan bijgesneden of uitgeschakeld zijn, wat leidt tot een leeg gebied. | Pas de vlaggen aan (`UnderlayIsOn = true`, `ClippingIsOn = false`) vóór het renderen van de uiteindelijke afbeelding. |

## Veelgestelde vragen

### V1: Kan ik Aspose.CAD for .NET gebruiken met andere CAD‑bestandsformaten?

A1: Aspose.CAD ondersteunt verschillende CAD‑formaten, waaronder DWG, DXF, DGN en meer. Raadpleeg de documentatie voor de volledige lijst.

### V2: Is er een tijdelijke licentie beschikbaar voor Aspose.CAD for .NET?

A2: Ja, je kunt een tijdelijke licentie verkrijgen **[hier](https://purchase.aspose.com/temporary-license/)**.

### V3: Waar kan ik ondersteuning vinden voor Aspose.CAD for .NET?

A3: Bezoek het ondersteuningsforum **[hier](https://forum.aspose.com/c/cad/19)** voor hulp.

### V4: Hoe koop ik Aspose.CAD for .NET?

A4: Koop de bibliotheek **[hier](https://purchase.aspose.com/buy)**.

### V5: Is er een gratis proefversie beschikbaar?

A5: Ja, je kunt de gratis proefversie **[hier](https://releases.aspose.com/)**.

## Conclusie

Gefeliciteerd! Je hebt met succes geleerd **hoe je DWG naar afbeelding kunt converteren** terwijl je ook **onderlaag‑vlaggen** kunt lezen met Aspose.CAD for .NET. Met deze kennis kun je:

- DWG‑tekeningen renderen als rasterafbeeldingen voor web‑ of rapportagescenario's.  
- Onderlaag‑eigenschappen inspecteren en manipuleren om correcte weergave te garanderen.  
- Problemen met zichtbaarheid, bijsnijden en monochroom debuggen vóór de definitieve afbeeldinggeneratie.

Voel je vrij om andere Aspose.CAD‑functies te verkennen, zoals laagbeheer, tekste­xtractie en batch‑conversie, om je CAD‑automatiseringsworkflows verder uit te breiden.

---

**Last Updated:** 2026-04-09  
**Tested With:** Aspose.CAD for .NET 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}