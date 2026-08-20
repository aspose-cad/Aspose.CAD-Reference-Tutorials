---
date: 2026-03-29
description: Leer hoe je snel lettertypen vervangt in Aspose.CAD voor .NET. Deze stapsgewijze
  handleiding laat je zien hoe je de primaire lettertype‑naam instelt en CAD‑tekeningen
  efficiënt aanpast.
linktitle: Substituting Fonts
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Hoe lettertypen te vervangen in Aspose.CAD voor .NET
url: /nl/net/cad-features-and-support/substituting-fonts/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hoe lettertypen te vervangen in Aspose.CAD voor .NET

## Inleiding

In het domein van CAD-ontwikkeling met .NET is het leren **hoe lettertypen te vervangen** een cruciale vaardigheid die de visuele kwaliteit van je tekeningen drastisch kan verbeteren. Aspose.CAD voor .NET biedt een eenvoudige API waarmee je **de primaire lettertype‑naam kunt instellen** voor elke stijl, waardoor globale of selectieve lettertype‑vervanging een fluitje van een cent wordt. In deze tutorial lopen we het volledige proces door — van het laden van een tekening tot het verwisselen van lettertypen, zowel globaal als per specifieke stijlnaam.

## Snelle antwoorden

- **Wat is de hoofdklasse voor CAD-manipulatie?** `Aspose.CAD.Image` (of de afgeleide `CadImage`).
- **Welke eigenschap wijzigt het lettertype?** `PrimaryFontName` op `CadStyleTableObject`.
- **Kan ik alle lettertypen in één keer vervangen?** Ja, itereren door `cadImage.Styles` en de eigenschap instellen.
- **Heb ik een licentie nodig voor productie?** Een geldige Aspose.CAD‑licentie is vereist voor niet‑trial gebruik.
- **Ondersteunde .NET‑versies?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## Wat is lettertype‑substitutie in CAD?

Lettertype‑substitutie betekent het vervangen van het oorspronkelijke lettertype dat in een CAD-tekening wordt gebruikt door een ander lettertype dat beschikbaar is op het doelsysteem. Dit is vooral nuttig wanneer het originele lettertype ontbreekt, wanneer je een consistente bedrijfsstijl nodig hebt, of bij het voorbereiden van tekeningen voor afdrukken op apparaten die slechts een beperkte set lettertypen ondersteunen.

## Waarom lettertypen vervangen met Aspose.CAD?

- **Geen externe afhankelijkheden** – de bibliotheek behandelt lettertype‑mapping intern.
- **Werkt met veel formaten** – DXF, DWG, DGN en meer.
- **Programmeerbare controle** – automatiseer het proces voor batch‑conversies of CI‑pijplijnen.
- **Behoudt teken‑geometrie** – alleen de visuele weergave van tekst verandert.

## Voorvereisten

- Basiskennis van .NET‑programmeren.
- Aspose.CAD voor .NET geïnstalleerd. Als je het nog niet hebt geïnstalleerd, download het [hier](https://releases.aspose.com/cad/net/).
- Een CAD-tekeningsbestand (DXF, DWG, enz.) om mee te experimenteren.

## Namespaces importeren

Voordat je begint, importeer je de benodigde namespaces om toegang te krijgen tot de Aspose.CAD‑functionaliteiten in je .NET‑applicatie.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad.CadTables;
```

## Stap 1: CAD-tekening laden

Begin met het laden van de CAD-tekening in een instantie van `CadImage`. Zorg ervoor dat je het juiste pad naar je documentmap opgeeft.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (CadImage cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    // Your code for further actions goes here
}
```

## Stap 2: Over stijlen itereren

Vervolgens itereren over de stijlen in de CAD-tekening met een `foreach`‑lus. Hiermee kun je individuele lettertype‑stijlen benaderen en manipuleren.

```csharp
foreach (CadStyleTableObject style in cadImage.Styles)
{
    // Your code for style manipulation goes here
}
```

## Hoe de primaire lettertype‑naam in te stellen voor lettertype‑substitutie

De eigenschap `PrimaryFontName` op elk `CadStyleTableObject` bepaalt welk lettertype wordt gebruikt wanneer de tekening wordt gerenderd. Door deze eigenschap in te stellen vervang je effectief het originele lettertype.

### Stap 3: Lettertypen globaal vervangen

Om lettertypen voor **alle** stijlen te vervangen, stel je de eigenschap `PrimaryFontName` voor elke stijl in op de gewenste lettertype‑naam, bijvoorbeeld `"Arial"`.

```csharp
foreach (CadStyleTableObject style in cadImage.Styles)
{
    style.PrimaryFontName = "Arial";
}
```

### Stap 4: Lettertype vervangen op stijlnaam

Als je alleen het lettertype voor een specifieke stijl moet vervangen (bijv. de stijl met de naam `"Roman"`), voeg dan een voorwaardelijke controle toe binnen de lus.

```csharp
foreach (CadStyleTableObject style in cadImage.Styles)
{
    if (style.StyleName == "Roman")
    {
        style.PrimaryFontName = "Arial";
    }
}
```

## Veelvoorkomende problemen & probleemoplossing

| Probleem | Oorzaak | Oplossing |
|----------|---------|-----------|
| Lettertype verandert niet na het uitvoeren van de code | De tekening is in cache of geopend in alleen‑lezen modus | Zorg ervoor dat je de afbeelding opslaat na wijziging (`cadImage.Save(...)`) of laad het bestand opnieuw om te verifiëren. |
| Gewenst lettertype niet gevonden op het systeem | Lettertype niet geïnstalleerd op de machine die de code uitvoert | Installeer het benodigde TrueType/OpenType‑lettertype of embed het in de applicatie‑resources. |
| Tekst verschijnt onsamenhangend | Onjuiste codering of ontbrekende Unicode‑ondersteuning | Gebruik een lettertype dat de vereiste tekenset ondersteunt (bijv. Arial Unicode MS). |

## Veelgestelde vragen

**Q: Kan ik lettertype‑wijzigingen terugdraaien in Aspose.CAD voor .NET?**  
A: Ja, je kunt terugdraaien door de originele CAD-tekening opnieuw te laden of door een back‑upkopie te bewaren voordat je wijzigingen aanbrengt.

**Q: Zijn er andere lettertype‑eigenschappen die ik kan aanpassen?**  
A: Zeker. Naast `PrimaryFontName` kun je werken met `SecondaryFontName`, `FontFamily` en andere stijlgerelateerde attributen voor geavanceerde aanpassingen.

**Q: Is Aspose.CAD compatibel met verschillende CAD‑formaten?**  
A: Ja, Aspose.CAD ondersteunt een breed scala aan formaten zoals DXF, DWG, DGN, DWF en meer, waardoor je flexibiliteit krijgt over projecten.

**Q: Kan ik lettertype‑substitutie automatiseren in batchverwerking?**  
A: Zeker. Plaats de laad‑ en substitutielogica in een lus die over een map met CAD‑bestanden itereren, of integreer het in een CI/CD‑pijplijn.

**Q: Waar kan ik extra ondersteuning vinden voor Aspose.CAD voor .NET?**  
A: Voor extra ondersteuning en community‑discussies, bezoek het [Aspose.CAD‑forum](https://forum.aspose.com/c/cad/19).

---

**Laatst bijgewerkt:** 2026-03-29  
**Getest met:** Aspose.CAD for .NET (latest release)  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}