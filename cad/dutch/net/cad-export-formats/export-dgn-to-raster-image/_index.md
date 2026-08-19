---
date: 2026-03-24
description: Leer hoe u dgn naar png kunt converteren en cad als jpeg kunt opslaan
  met Aspose.CAD voor .NET – een snelle gids voor CAD-naar-afbeeldingsconversie.
linktitle: Export DGN to Raster Image
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Hoe DGN naar PNG converteren in Aspose.CAD voor .NET
url: /nl/net/cad-export-formats/export-dgn-to-raster-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DGN naar PNG converteren in Aspose.CAD voor .NET

In moderne .NET‑ontwikkeling is **convert dgn to png** een veelvoorkomende eis wanneer u CAD‑tekeningen op het web wilt weergeven of in rapporten wilt insluiten. Aspose.CAD voor .NET maakt deze conversie eenvoudig, zodat u met slechts een paar regels code een DGN‑bestand kunt omzetten naar een rasterafbeelding van hoge kwaliteit. In deze gids lopen we het volledige proces door, van het opzetten van het project tot het opslaan van het uiteindelijke PNG‑ (of JPEG‑) bestand.

## Snelle antwoorden
- **Kan ik DGN naar PNG converteren met Aspose.CAD?** Ja – configureer gewoon de rasterisatie‑opties en kies PNG of JPEG als output.  
- **Heb ik een licentie nodig voor productiegebruik?** Een geldige Aspose.CAD‑licentie is vereist voor niet‑trial‑implementaties.  
- **Welke .NET‑versies worden ondersteund?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7.  
- **Welke afbeeldingsformaten zijn beschikbaar?** PNG, JPEG, BMP, GIF, TIFF en meer.  
- **Is foutafhandeling noodzakelijk?** Absoluut – wikkel de conversie in een try/catch‑blok om bestands‑toegangsproblemen af te handelen.

## Wat is “convert dgn to png”?
Een DGN (MicroStation)‑bestand naar PNG converteren betekent het rasteren van vector‑CAD‑gegevens naar een pixel‑gebaseerde afbeelding. Dit is handig voor het genereren van voorbeeldweergaven, het insluiten van tekeningen in HTML‑e‑mails, of het maken van miniaturen voor documentbeheersystemen.

## Waarom Aspose.CAD gebruiken voor CAD‑naar‑afbeelding conversie?
- **Geen externe afhankelijkheden** – werkt volledig in beheerde code.  
- **Hoge nauwkeurigheid** – behoudt lijndiktes, lagen en kleuren.  
- **Flexibele output** – schakel tussen PNG, JPEG, BMP, enz., door één optie te wijzigen.  
- **Prestaties geoptimaliseerd** – rasteren is snel, zelfs voor grote tekeningen.

## Vereisten

Voordat we beginnen, zorg ervoor dat u het volgende heeft:

- **Aspose.CAD voor .NET** geïnstalleerd in uw project. U kunt het downloaden van de [website](https://reference.aspose.com/cad/net/).  
- Een voorbeeld DGN‑bestand (bijv. `Nikon_D90_Camera.dgn`) geplaatst in een bekende map.

## Namespaces importeren

Begin met het toevoegen van de vereiste `using`‑statements zodat u toegang heeft tot de Aspose.CAD‑klassen.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Stap 1: Laad het DGN‑bestand

Laad de bron‑DGN in een `CadImage`‑object. Dit object vertegenwoordigt de CAD‑tekening in het geheugen en dient als bron voor rasterisatie.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for further processing goes here
}
```

## Stap 2: Definieer rasterisatie‑opties

Stel in hoe de CAD‑tekening moet worden gerasterd. Hier kunt u de afbeeldingsgrootte, schaal en achtergrondkleur regelen.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## Stap 3: Kies het uitvoerformaat (PNG of JPEG)

Hoewel de tutorial zich richt op PNG, wilt u misschien ook **cad opslaan als jpeg**. Maak het juiste image‑options‑object aan en koppel de rasterisatie‑instellingen.

```csharp
ImageOptionsBase options = new JpegOptions();   // Change to PngOptions() for PNG output
options.VectorRasterizationOptions = rasterizationOptions;
```

> **Pro tip:** Om een PNG‑bestand te genereren, vervang `new JpegOptions()` door `new PngOptions()`.

## Stap 4: Sla de gerasterde afbeelding op

Roep tenslotte `Save` aan op de `CadImage`‑instantie, met de gewenste bestandsnaam en het geconfigureerde options‑object.

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpg", options);
```

Als u bent overgeschakeld naar `PngOptions`, wordt het bestand opgeslagen als `ExportDGNToRasterImage_out.png`.

## Veelvoorkomende problemen en oplossingen

| Probleem | Oorzaak | Oplossing |
|----------|---------|-----------|
| **Lege uitvoerafbeelding** | `NoScaling` onjuist ingesteld of layout niet geselecteerd | Stel `AutomaticLayoutsScaling = true` in of specificeer de gewenste layout. |
| **Out‑of‑memory voor grote bestanden** | Het laden van een enorme DGN zonder streaming | Gebruik `Image.Load(sourceFilePath, new LoadOptions { LoadOnDemand = true })`. |
| **Niet‑ondersteunde DGN‑versie** | Oudere MicroStation‑versies | Zorg ervoor dat u de nieuwste Aspose.CAD‑versie hebt die legacy‑formaten ondersteunt. |

## Veelgestelde vragen

**V: Kan ik DGN‑bestanden exporteren naar andere formaten dan JPEG?**  
A: Ja, Aspose.CAD voor .NET ondersteunt PNG, BMP, GIF, TIFF en meer – vervang gewoon de options‑klasse (bijv. `new PngOptions()`).

**V: Hoe moet ik uitzonderingen afhandelen tijdens de conversie?**  
A: Plaats de conversiecode in een `try/catch`‑blok en log `Aspose.CAD.CadException` voor gedetailleerde foutinformatie.

**V: Is er een proefversie beschikbaar voor Aspose.CAD voor .NET?**  
A: Ja, u kunt het product uitproberen met een gratis trial. Bezoek [hier](https://releases.aspose.com/) voor meer informatie.

**V: Waar kan ik hulp zoeken of discussies voeren over Aspose.CAD voor .NET?**  
A: Ga naar het [Aspose.CAD‑forum](https://forum.aspose.com/c/cad/19) voor community‑ondersteuning en discussies.

**V: Hoe verkrijg ik een tijdelijke licentie voor Aspose.CAD voor .NET?**  
A: Bezoek [deze link](https://purchase.aspose.com/temporary-license/) om een tijdelijke licentie aan te schaffen voor uw ontwikkelbehoeften.

## Conclusie

U heeft nu geleerd hoe u **dgn naar png** (of JPEG) kunt converteren met Aspose.CAD voor .NET. Door de rasterisatie‑opties aan te passen en de image‑options‑klasse te wisselen, kunt u de output afstemmen op elke projectvereiste. Voel u vrij om te experimenteren met verschillende paginagroottes, DPI‑instellingen en bestandsformaten om de perfecte rasterafbeelding voor uw applicatie te krijgen.

---

**Laatst bijgewerkt:** 2026-03-24  
**Getest met:** Aspose.CAD 24.11 voor .NET  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}