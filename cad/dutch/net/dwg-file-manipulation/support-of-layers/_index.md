---
date: 2026-04-09
description: Leer hoe u DWG‑lagen exporteert, DWG‑afbeeldingen converteert en DWG‑JPEG
  opslaat met C# en Aspose.CAD voor .NET. Stapsgewijze handleiding voor efficiënte
  CAD‑bestandsmanipulatie.
keywords:
- export dwg layers
- convert dwg image
- dwg layer visibility
- save dwg jpeg
linktitle: Lagen verwerken in DWG‑bestanden met C#
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: DWG-lagen exporteren met C# – Aspose.CAD-tutorial
url: /nl/net/dwg-file-manipulation/support-of-layers/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export DWG-lagen met C# – Aspose.CAD Tutorial

## Inleiding

In deze uitgebreide gids leer je **how to export DWG layers** met C# en de Aspose.CAD‑bibliotheek. Of je nu **convert DWG image**‑formaten moet omzetten, **DWG layer visibility** moet beheren, of simpelweg **save DWG JPEG**‑bestanden wilt opslaan, de onderstaande stappen laten je precies zien hoe je dit efficiënt kunt doen. Aan het einde van de tutorial heb je een kant‑klaar fragment dat een specifieke laag isoleert en rendert als een JPEG van hoge kwaliteit.

## Snelle antwoorden
- **What does “export dwg layers” mean?** Het betekent het rasteren van geselecteerde lagen van een DWG‑bestand naar een afbeeldingsformaat zoals JPEG of PNG.  
- **Which library is best for this task?** Aspose.CAD for .NET biedt volledige functionaliteit zonder dat AutoCAD nodig is.  
- **Can I export multiple layers at once?** Ja – geef een array van laagnamen door aan de rasterisatie‑opties.  
- **Do I need a license for production use?** Een commerciële licentie is vereist; een gratis proefversie is beschikbaar voor evaluatie.  
- **What output formats are supported?** JPEG, PNG, BMP, TIFF en diverse andere via de ImageOptions‑klassen.

## Wat is export dwg layers?
Exporteren van DWG‑lagen betekent dat je de vectordata die behoort tot één of meer lagen binnen een DWG‑tekening neemt en deze rastert naar een bitmap‑afbeelding. Dit is handig wanneer je een weergave van een specifiek deel van een tekening wilt delen zonder het volledige CAD‑bestand bloot te stellen.

## Waarom de zichtbaarheid van DWG-lagen regelen?
Het regelen van de laagzichtbaarheid stelt je in staat om:

- Schone visuele assets te creëren voor presentaties of documentatie.  
- De bestandsgrootte te verkleinen door alleen de benodigde geometrie te exporteren.  
- Proprietaire ontwerpdetails te beschermen door vertrouwelijke lagen te verbergen.  

## Vereisten

Voordat we beginnen, controleer je of je het volgende hebt:

- Basiskennis van de programmeertaal C#.  
- Visual Studio geïnstalleerd op je machine.  
- Aspose.CAD for .NET‑bibliotheek, die je kunt downloaden van de [Aspose.CAD website](https://releases.aspose.com/cad/net/).

## Namespaces importeren

Om te beginnen importeer je de namespaces die je toegang geven tot rasterisatie‑ en afbeeldingsexportfuncties.

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

## Stap 1: Laad het DWG‑bestand

Laad het bron‑DWG (of DWF)‑bestand in een `Image`‑object. Dit object vertegenwoordigt de volledige tekening in het geheugen.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "for_layers_test.dwf";

using (Aspose.CAD.Image image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // Your code for subsequent steps goes here
}
```

*Waarom dit belangrijk is:* Het bestand één keer laden stelt je in staat om dezelfde `image`‑instantie te hergebruiken voor een willekeurig aantal laag‑specifieke exports, wat de prestaties verbetert.

## Stap 2: Rasterisatie‑opties configureren

Maak een `CadRasterizationOptions`‑instantie aan om Aspose.CAD te vertellen hoe de tekening moet worden gerenderd. Hier stellen we een hoge resolutie (1600 × 1600) in om ervoor te zorgen dat de geëxporteerde JPEG scherp is.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
```

Je kunt ook de achtergrondkleur, lijndikte‑schaal of anti‑aliasing‑instellingen aanpassen indien nodig.

## Stap 3: Lagen specificeren (DWG-laagzichtbaarheid)

Voeg de lagen toe die je wilt **export dwg layers**. In dit voorbeeld exporteren we alleen “LayerA”. Om meerdere lagen te exporteren, lijst je ze simpelweg op in de array.

```csharp
rasterizationOptions.Layers = new string[] { "LayerA" };
```

*Pro tip:* Gebruik de exacte laagnaam zoals deze in de tekening verschijnt; laagnamen zijn hoofdlettergevoelig.

## Stap 4: Afbeeldings‑exportopties configureren

Kies het afbeeldingsformaat dat je wilt maken. We gebruiken `JpegOptions` omdat JPEG een goede balans biedt tussen kwaliteit en bestandsgrootte, wat ideaal is wanneer je **save dwg jpeg**‑bestanden voor web‑preview nodig hebt.

```csharp
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.VectorRasterizationOptions = rasterizationOptions;
```

Als je **convert dwg image** naar PNG of TIFF wilt, vervang je `JpegOptions` door de overeenkomstige options‑klasse.

## Stap 5: Sla de geëxporteerde afbeelding op

Definieer het uitvoer‑bestandspad en roep `Save` aan. De rasterisatie‑engine respecteert de door jou opgegeven laaglijst, zodat alleen “LayerA” in de uiteindelijke JPEG verschijnt.

```csharp
MyDir = MyDir + "for_layers_test.jpg";
image.Save(MyDir, jpegOptions);
```

Na het uitvoeren van deze regel vind je `for_layers_test.jpg` in je documentmap, met alleen de geselecteerde laag.

## Veelvoorkomende problemen en oplossingen

| Probleem | Oplossing |
|----------|-----------|
| **Layer name not found** | Controleer de exacte spelling en hoofdlettergebruik van de laag in de originele DWG. Gebruik een CAD‑viewer om laagnamen weer te geven. |
| **Blank output image** | Zorg ervoor dat de rasterisatie‑opties een niet‑transparante achtergrond hebben en dat de geselecteerde lagen daadwerkelijk geometrie bevatten. |
| **Low‑resolution output** | Verhoog `PageWidth` en `PageHeight` of stel `Resolution` in bij `CadRasterizationOptions`. |
| **Unsupported DWG version** | Werk bij naar de nieuwste Aspose.CAD‑versie; deze voegt ondersteuning toe voor nieuwere AutoCAD‑releases. |

## Veelgestelde vragen

### Q1: Kan ik meerdere lagen tegelijk verwerken?
A1: Ja, dat kan. Voeg simpelweg de laagnamen toe aan de `rasterizationOptions.Layers`‑array.

### Q2: Is een proefversie van Aspose.CAD beschikbaar?
A2: Ja, je kunt een gratis proefversie krijgen via [hier](https://releases.aspose.com/).

### Q3: Waar kan ik de documentatie vinden?
A3: De documentatie is beschikbaar [hier](https://reference.aspose.com/cad/net/).

### Q4: Hoe krijg ik ondersteuning voor Aspose.CAD?
A4: Je kunt ondersteuning zoeken op het [Aspose.CAD forum](https://forum.aspose.com/c/cad/19).

### Q5: Wat zijn de licentieopties voor Aspose.CAD?
A5: Je kunt de licentieopties en aankoopdetails verkennen [hier](https://purchase.aspose.com/buy).

**Aanvullende Q&A**

**Q: Kan ik de tekening exporteren naar PNG in plaats van JPEG?**  
A: Absoluut. Vervang `JpegOptions` door `PngOptions` en pas de bestandsextensie dienovereenkomstig aan.

**Q: Behoudt de bibliotheek lijntypen en kleuren?**  
A: Ja. Alle vector‑eigenschappen worden getrouw gerenderd tijdens het rasteren.

---

**Laatst bijgewerkt:** 2026-04-09  
**Getest met:** Aspose.CAD for .NET (latest release)  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}