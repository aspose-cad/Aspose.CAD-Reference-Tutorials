---
date: 2026-03-05
description: Leer hoe u het xref‑pad wijzigt, de blokreferentie bijwerkt en CAD‑hyperlinks
  beheert met Aspose.CAD voor .NET in een paar eenvoudige stappen.
linktitle: Editing Hyperlinks in CAD Files
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Hoe het xref-pad te wijzigen en hyperlinks in CAD‑bestanden te bewerken – Aspose.CAD‑tutorial
url: /nl/net/advanced-cad-techniques/editing-hyperlinks-in-cad-files/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hyperlinks bewerken in CAD‑bestanden - Aspose.CAD‑handleiding

## Introductie

Welkom bij onze stapsgewijze gids over hoe u **xref‑pad wijzigt** en hyperlinks in CAD‑bestanden bewerkt met Aspose.CAD voor .NET. Of u nu **blokreferentie**‑informatie moet **bijwerken** of eenvoudigweg **CAD‑hyperlinks** moet **beheren**, deze tutorial leidt u door het volledige proces, van het laden van een DWG‑bestand tot het opslaan van de wijzigingen. Aan het einde heeft u een duidelijk, herbruikbaar patroon om uw CAD‑documenten correct gelinkt te houden.

## Snelle antwoorden
- **Wat betekent “change xref path”?** Het werkt het pad van de externe referentie (XRef) bij dat in een CAD‑blok is opgeslagen.  
- **Welke bibliotheek behandelt dit?** Aspose.CAD voor .NET biedt een eenvoudige API voor het bewerken van XRef‑paden en hyperlinks.  
- **Heb ik een licentie nodig?** Een gratis proefversie werkt voor ontwikkeling; een commerciële licentie is vereist voor productie.  
- **Kan ik dit gebruiken met .NET Core?** Ja, de bibliotheek ondersteunt .NET Framework en .NET Core/.NET 5+.  
- **Hoe lang duurt de implementatie?** Meestal minder dan 10 minuten voor een eenvoudig bestand.

## Wat betekent het wijzigen van het XRef‑pad?

In CAD‑terminologie verwijst een **XRef** (externe referentie) naar een ander tekeningsbestand dat als een blok wordt ingevoegd. Het wijzigen van het XRef‑pad betekent dat het blok naar een nieuwe bestandslocatie wordt geleid, wat essentieel is bij het reorganiseren van projectmappen of het bijwerken van gekoppelde bronnen.

## Waarom blokreferentie bijwerken en CAD‑hyperlinks beheren?

- **Consistentie behouden** wanneer bestanden tussen omgevingen worden verplaatst.  
- **Gebroken links voorkomen** die fouten kunnen veroorzaken tijdens het renderen of verdere verwerking.  
- **BIM‑werkstromen stroomlijnen** door programmatisch te zorgen dat alle referenties actueel zijn.  

## Voorwaarden

- Basiskennis van C# en .NET‑ontwikkeling.  
- Aspose.CAD voor .NET geïnstalleerd – download het [hier](https://releases.aspose.com/cad/net/).  
- Een voorbeeld‑CAD‑bestand (bijv. *AutoCad_Sample.dwg*) om mee te experimenteren.

## Namespaces importeren

Voeg in uw C#‑project de benodigde namespaces toe:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

Laten we nu stap voor stap door de implementatie lopen.

## Stap 1: Het CAD‑bestand laden

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";
string dwgPathToFile = MyDir + "AutoCad_Sample.dwg";

using (CadImage cadImage = (CadImage)Image.Load(dwgPathToFile))
{
    // Your code for editing hyperlinks will go here.
}
```

## Stap 2: Door entiteiten itereren

```csharp
foreach (CadBaseEntity entity in cadImage.Entities)
{
    // Your code for handling each entity will go here.
}
```

## Stap 3: Insert‑objecten bewerken – XRef‑pad wijzigen

```csharp
if (entity is CadInsertObject)
{
    CadBlockEntity block = cadImage.BlockEntities[((CadInsertObject)entity).Name];
    if (!string.IsNullOrEmpty(block.XRefPathName.Value))
    {
        // **Primary keyword usage:** change xref path
        block.XRefPathName.Value = "new file reference.dwg";
    }
}
```

*Hier **werken we de blokreferentie bij** door een nieuwe XRef‑bestandsnaam toe te wijzen. Dit is de kern van het wijzigen van het XRef‑pad.*

## Stap 4: Hyperlinks aanpassen – CAD‑hyperlinks beheren

```csharp
if (entity.Hyperlink == "https://products.aspose.com")
{
    // **Secondary keyword usage:** manage cad hyperlinks
    entity.Hyperlink = "https://www.aspose.com";
}
```

*Dit fragment laat zien hoe u **CAD‑links** (hyperlinks) kunt **bijwerken** zodat ze naar het juiste webadres wijzen.*

## Veelvoorkomende problemen en oplossingen

| Probleem | Oorzaak | Oplossing |
|----------|---------|-----------|
| XRef‑pad wordt niet bijgewerkt | Blok is geen `CadInsertObject` | Controleer het entiteitstype vóór het casten. |
| Hyperlink niet gewijzigd | Hyperlink‑eigenschap is null of heeft een andere hoofdlettergevoeligheid | Gebruik `StringComparison.OrdinalIgnoreCase` bij het vergelijken. |
| Bestand kan niet worden geladen | Ontbrekende Aspose.CAD‑licentie in productie | Pas een geldige licentie toe vóór het laden van de afbeelding. |

## Conclusie

U heeft nu geleerd hoe u **xref‑pad wijzigt**, **blokreferentie bijwerkt** en **CAD‑hyperlinks beheert** met Aspose.CAD voor .NET. Deze mogelijkheden stellen u in staat grote CAD‑projecten georganiseerd en vrij van gebroken referenties te houden, waardoor de betrouwbaarheid in geautomatiseerde pipelines toeneemt.

## Veelgestelde vragen

### V1: Is Aspose.CAD compatibel met andere CAD‑bestandsformaten?

A1: Ja, Aspose.CAD ondersteunt verschillende CAD‑formaten, waaronder DWG, DXF, DGN en meer.

### V2: Kan ik Aspose.CAD uitproberen voordat ik het koop?

A2: Zeker! U kunt een gratis proefversie krijgen [hier](https://releases.aspose.com/).

### V3: Waar kan ik gedetailleerde documentatie voor Aspose.CAD vinden?

A3: Raadpleeg de documentatie [hier](https://reference.aspose.com/cad/net/).

### V4: Hoe krijg ik een tijdelijke licentie voor Aspose.CAD?

A4: Verkrijg een tijdelijke licentie [hier](https://purchase.aspose.com/temporary-license/).

### V5: Hulp nodig of vragen?

A5: Bezoek ons ondersteuningsforum [hier](https://forum.aspose.com/c/cad/19).

## Aanvullende veelgestelde vragen

**V: Kan ik programmatisch meerdere XRef‑paden in één keer wijzigen?**  
A: Ja, itereren door alle `CadInsertObject`‑entiteiten en `XRefPathName.Value` instellen indien nodig.

**V: Heeft het wijzigen van het XRef‑pad invloed op het visuele uiterlijk van de tekening?**  
A: De referentie wordt bijgewerkt, maar de tekening toont het nieuwe externe bestand wanneer geopend in een CAD‑viewer.

**V: Is er een manier om alle huidige hyperlinks in een CAD‑bestand te tonen?**  
A: Loop door `cadImage.Entities` en verzamel `entity.Hyperlink`‑waarden die niet null of leeg zijn.

**V: Werkt deze aanpak met grote DWG‑bestanden (honderden MB)?**  
A: Aspose.CAD is geoptimaliseerd voor prestaties, maar zorg voor voldoende geheugen en overweeg verwerking in delen indien nodig.

---

**Laatst bijgewerkt:** 2026-03-05  
**Getest met:** Aspose.CAD 24.12 for .NET  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}