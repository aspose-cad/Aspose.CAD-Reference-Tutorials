---
date: 2026-03-07
description: Leer hoe u CAD naar SVG kunt exporteren met Aspose.CAD voor .NET, de
  SVG‑kleur kunt aanpassen en DWG efficiënt naar SVG kunt converteren.
linktitle: Exporting CAD Drawings to SVG Format
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: CAD exporteren naar SVG – CAD‑tekeningen exporteren naar SVG‑formaat – Aspose.CAD‑gids
url: /nl/net/advanced-export-techniques/exporting-cad-drawings-to-svg/
weight: 15
---

"

"**Tested With:** Aspose.CAD for .NET 24.12" -> "**Getest met:** Aspose.CAD for .NET 24.12"

"**Author:** Aspose" -> "**Auteur:** Aspose"

Then closing shortcodes.

Then backtop button shortcode.

Make sure to keep all shortcodes exactly.

Now produce final content.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD naar SVG exporteren – CAD-tekeningen exporteren naar SVG-indeling

## Introductie

Het exporteren van CAD-tekeningen naar SVG is een veelvoorkomende eis wanneer je resolutie‑onafhankelijke graphics nodig hebt voor webpagina's, rapporten of interactieve visualisaties. In deze tutorial leer je **hoe je CAD naar SVG exporteert** met Aspose.CAD for .NET, verken je opties om **SVG-kleur aan te passen**, en zie je hoe je **DWG naar SVG kunt converteren** (of DXF naar SVG) in slechts een paar regels code. De stappen zijn snel, de API is intuïtief, en de resulterende SVG‑bestanden schalen perfect op elk apparaat.

## Snelle antwoorden
- **Welke bibliotheek verwerkt de conversie?** Aspose.CAD for .NET.
- **Kan ik de kleermodus wijzigen?** Ja – gebruik `SvgColorMode` om grijstinten, zwart‑wit of volledige kleur in te stellen.
- **Welke CAD-formaten worden ondersteund?** DWG, DXF en vele andere (zie Aspose.CAD‑documentatie).
- **Heb ik een licentie nodig voor ontwikkeling?** Een tijdelijke licentie is beschikbaar voor testen.
- **Hoe lang duurt de conversie?** Meestal minder dan een seconde voor standaardtekeningen.

## Wat is “CAD naar SVG exporteren”?
CAD naar SVG exporteren betekent dat je een native CAD‑bestand (zoals DWG of DXF) neemt en rendert naar het Scalable Vector Graphics‑formaat. SVG is XML‑gebaseerd, lichtgewicht en kan worden gestyled met CSS—wat het ideaal maakt voor moderne web‑ en mobiele toepassingen.

## Waarom Aspose.CAD gebruiken voor CAD naar SVG exporteren?
- **Geen externe afhankelijkheden** – pure .NET API, geen AutoCAD‑installaties nodig.  
- **Fijne controle** – je kunt **SVG‑kleur aanpassen**, bepalen of tekst als vormen behouden blijft, en rasterisatie‑opties kiezen.  
- **Brede formaatondersteuning** – dezelfde code werkt voor **DWG naar SVG converteren**, **DXF naar SVG converteren**, en andere formaten, waardoor je codebasis wordt vereenvoudigd.  
- **Hoge prestaties** – geoptimaliseerd voor snelheid en laag geheugenverbruik, geschikt voor batchverwerking.

## Voorvereisten

Zorg ervoor dat je het volgende hebt voordat je begint:

- **Aspose.CAD for .NET** geïnstalleerd. Je kunt de bibliotheek downloaden [hier](https://releases.aspose.com/cad/net/).  
- Een .NET‑ontwikkelomgeving (Visual Studio, Rider of de .NET CLI).  
- Een CAD‑bestand (DWG of DXF) dat je wilt converteren.

## Namespaces importeren

Breng eerst de benodigde namespaces in je project zodat de klassen beschikbaar zijn.

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Stapsgewijze handleiding

### Stap 1: Stel de documentdirectory in  
Definieer de map waarin je bron‑CAD‑bestand zich bevindt en waar de SVG‑output wordt opgeslagen.

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";
```

### Stap 2: Laad de CAD‑tekening  
Gebruik `Image.Load` om het DWG‑ (of DXF‑) bestand te lezen. Dit werkt voor **load DWG .NET** scenario's.

```csharp
using (Image image = Image.Load(MyDir + "sample.dwg"))
{
```

### Stap 3: Configureer SVG‑exportopties  
Pas de exportinstellingen aan volgens je behoeften. Hier stellen we de kleermodus in op grijstinten en dwingen we alle tekst af te beelden als vectorvormen.

```csharp
    var options = new SvgOptions();
    options.ColorType = SvgColorMode.Grayscale;   // customize SVG color mode
    options.TextAsShapes = true;                  // ensures text appears as shapes
```

### Stap 4: Sla het SVG‑bestand op  
Schrijf tenslotte het SVG‑bestand naar de schijf. Deze stap **slaat CAD op als SVG** en voltooit de conversie.

```csharp
    image.Save(MyDir + "sample.svg", options);
}
```

Door deze vier beknopte stappen te volgen, kun je **DWG naar SVG converteren** (of **DXF naar SVG converteren**) met volledige controle over het uiterlijk van de output.

## Veelvoorkomende problemen en oplossingen

| Issue | Cause | Fix |
|-------|-------|-----|
| **Lege SVG-uitvoer** | Het pad naar het bronbestand is onjuist of het bestand is beschadigd. | Controleer `MyDir` en zorg ervoor dat het CAD‑bestand zonder fouten opent. |
| **Kleuren zien er verkeerd uit** | `SvgColorMode` onbedoeld ingesteld op Grayscale. | Wijzig `options.ColorType` naar `SvgColorMode.FullColor` om de oorspronkelijke kleuren te behouden. |
| **Tekst ontbreekt** | `TextAsShapes` ingesteld op `false` en de viewer ondersteunt geen ingesloten lettertypen. | Behoud `TextAsShapes = true` of embed de vereiste lettertypen in de SVG. |

## Veelgestelde vragen

### Q1: Is Aspose.CAD compatibel met alle CAD-formaten?
A1: Aspose.CAD ondersteunt verschillende CAD-formaten, waaronder DWG en DXF, wat zorgt voor brede compatibiliteit.

### Q2: Kun ik de kleermodus aanpassen bij het exporteren naar SVG?
A2: Ja, Aspose.CAD stelt je in staat de kleermodus te kiezen, wat flexibiliteit biedt in de output.

### Q3: Zijn tijdelijke licenties beschikbaar voor testdoeleinden?
A3: Ja, je kunt een tijdelijke licentie verkrijgen [hier](https://purchase.aspose.com/temporary-license/) voor evaluatie.

### Q4: Waar kan ik gedetailleerde documentatie voor Aspose.CAD vinden?
A4: De documentatie is beschikbaar [hier](https://reference.aspose.com/cad/net/).

### Q5: Hoe kan ik ondersteuning krijgen of vragen stellen over Aspose.CAD?
A5: Bezoek het community‑forum [hier](https://forum.aspose.com/c/cad/19) voor ondersteuning en discussies.

## Veelgestelde vragen

**Q: Kan ik deze code gebruiken met .NET Core of .NET 6?**  
A: Absoluut. Aspose.CAD for .NET is compatibel met .NET Framework, .NET Core en .NET 5/6+.

**Q: Is het mogelijk om alleen een specifieke lay-out of laag te exporteren?**  
A: Ja. Gebruik `SvgOptions` om `PageIndex` in te stellen of lagen te filteren vóór het opslaan.

**Q: Hoe kan ik aangepaste CSS‑stijlen in de gegenereerde SVG embedden?**  
A: Na het opslaan kun je de SVG‑XML post‑processen om `<style>`‑elementen toe te voegen, of `options.CustomCss` gebruiken indien beschikbaar in nieuwere versies.

**Q: Welke grootte‑limieten gelden er voor het bron‑CAD‑bestand?**  
A: De bibliotheek kan grote bestanden aan, maar het geheugenverbruik neemt toe met de complexiteit. Voor zeer grote tekeningen kun je overwegen om pagina's afzonderlijk te verwerken.

**Q: Behoudt de conversie lijndiktes en lijntypen?**  
A: Standaard worden lijndiktes behouden. Je kunt de renderopties in `SvgOptions` aanpassen voor fijnere controle.

---

**Laatst bijgewerkt:** 2026-03-07  
**Getest met:** Aspose.CAD for .NET 24.12  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}