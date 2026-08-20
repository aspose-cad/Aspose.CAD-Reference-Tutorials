---
date: 2026-04-06
description: Leer hoe je DWF naar JPG converteert in C# met Aspose.CAD en ontdek hoe
  je de DWF‑layoutgrootte uit DWG‑bestanden kunt extraheren.
keywords:
- convert dwf to jpg
- how to extract dwf
- convert dwg to jpg
linktitle: Werken met DWG‑bestanden in C# – Grootte van DWF‑layout ophalen
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: DWF naar JPG converteren in C# – DWF‑layoutgrootte ophalen uit DWG
url: /nl/net/dwg-file-manipulation/get-size-of-dwf-layout/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convert DWF naar JPG in C# – Verkrijg DWF‑indelingsgrootte van DWG

## Inleiding

Als u **convert DWF to JPG** moet uitvoeren en tegelijkertijd de exacte indelingsafmetingen wilt achterhalen, bent u op de juiste plek. In deze tutorial lopen we een volledig end‑to‑end voorbeeld door dat Aspose.CAD for .NET gebruikt om een van DWG afgeleide DWF‑file te openen, de grootte van elke indeling te lezen en de indeling op te slaan als een JPG‑afbeelding van hoge kwaliteit. Aan het einde weet u niet alleen hoe u DWF‑indelingsinformatie kunt extraheren, maar heeft u ook een herbruikbare code‑snippet die u in elk C#‑project kunt gebruiken.

## Snelle antwoorden

- **Wat betekent “convert DWF to JPG”?** Het betekent het rasteren van een vector‑DWF‑indeling naar een bitmap‑JPEG‑afbeelding.  
- **Waarom eerst de indelingsgrootte lezen?** Het kennen van de exacte afmetingen stelt u in staat de juiste paginadimensies in te stellen, waardoor uitgerekte of bijgesneden output wordt voorkomen.  
- **Welke bibliotheek behandelt dit?** Aspose.CAD for .NET biedt volledige ondersteuning voor DWG, DWF en raster‑afbeeldingsconversie.  
- **Heb ik een licentie nodig?** Een tijdelijke licentie werkt voor evaluatie; een volledige licentie is vereist voor productie.  
- **Welke .NET‑versies worden ondersteund?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## Wat is “convert DWF to JPG” en waarom is het belangrijk?

Het converteren van een DWF (Design Web Format)‑bestand naar JPG creëert een draagbare afbeelding die in browsers kan worden weergegeven, in rapporten kan worden ingebed, of kan worden gedeeld met belanghebbenden die geen CAD‑software hebben. De conversie geeft u ook de flexibiliteit om de afbeelding te bewerken (formaat wijzigen, comprimeren, watermerk) met standaard beeldverwerkingstools.

## Waarom DWF‑indelingsgrootte extraheren?

Een DWF‑bestand kan meerdere indelingen bevatten, elk met een eigen coördinatensysteem en eenheden (inches, millimeters, enz.). Het extraheren van de indelingsgrootte stelt u in staat:

1. De oorspronkelijke beeldverhouding te behouden bij het rasteren.  
2. De juiste DPI te kiezen voor output met hoge resolutie.  
3. Batchverwerking van vele indelingen te automatiseren zonder handmatig bijstellen.

## Voorvereisten

- Aspose.CAD for .NET: Zorg ervoor dat u Aspose.CAD for .NET geïnstalleerd heeft. U kunt het downloaden van de [Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/).

De bibliotheek klaar hebben betekent dat u zich kunt concentreren op de code in plaats van afhankelijkheden op te zoeken.

## Namespaces importeren

Voordat we beginnen met coderen, importeren we de benodigde namespaces. Deze leveren de klassen die we nodig hebben om met CAD‑bestanden, rasterisatie‑opties en bestands‑I/O te werken.

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Dwf;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

## Stap 1: Stel uw omgeving in

Maak een nieuw C#‑console‑ of class‑library‑project, voeg een referentie toe aan de **Aspose.CAD.dll**, en zorg ervoor dat het project een compatibele .NET‑versie target.

## Stap 2: Definieer bestands‑paden (hoe DWF te extraheren)

Geef aan waar uw bron‑DWF‑bestand zich bevindt en waar de gegenereerde JPG‑bestanden moeten worden weggeschreven.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "blocks_and_tables.dwf";
```

> **Pro tip:** Gebruik `Path.Combine(MyDir, "blocks_and_tables.dwf")` voor veiliger padbeheer op verschillende besturingssystemen.

## Stap 3: Laad de DWF‑afbeelding

Laad het DWF‑bestand in een `Aspose.CAD.Image`‑object. We casten het naar `DwfImage` omdat we toegang nodig hebben tot paginagerichte eigenschappen.

```csharp
using (DwfImage image = (DwfImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    // Code for further steps will go here
}
```

## Stap 4: Doorloop pagina’s

Een DWF kan meerdere pagina’s (indelingen) bevatten. Loop door elke pagina zodat we ze afzonderlijk kunnen verwerken.

```csharp
foreach (var page in image.Pages)
{
    // Code for further steps will go here
}
```

## Stap 5: Verkrijg indelingsinformatie

Binnen de lus haalt u de indelingsnaam op. Deze naam wordt zowel voor logging als voor het benoemen van het output‑JPG‑bestand gebruikt.

```csharp
var layout = page.Name;
System.Console.WriteLine("Layout= " + layout);
```

## Stap 6: Stel JPG‑opties in

Maak een `JpegOptions`‑instance aan en configureer rasterisatie‑opties. De eigenschap `Layouts` vertelt Aspose.CAD welke indeling moet worden gerenderd.

```csharp
using (FileStream fs = new FileStream(MyDir + "layout_" + layout + ".jpg", FileMode.Create))
{
    JpegOptions jpegOptions = new JpegOptions();
    CadRasterizationOptions options = new CadRasterizationOptions();
    options.Layouts = new string[] { layout };
    // Code for further steps will go here
}
```

## Stap 7: Bepaal paginagrootte (dwg naar jpg converteren)

Bereken de breedte en hoogte van de indeling in de oorspronkelijke eenheden. Deze informatie is essentieel om de raster‑paginagrootte correct in te stellen.

```csharp
double sizeExtX = page.MaxPoint.X - page.MinPoint.X;
double sizeExtY = page.MaxPoint.Y - page.MinPoint.Y;
// Code for further steps will go here
```

## Stap 8: Stel paginadimensies in

Converteer de oorspronkelijke eenheden (inch of millimeter) naar pixels met behulp van de hulpmethoden die door Aspose.CAD worden geleverd. Als het eenheidstype geen van beide is, vallen we terug op het gebruik van de ruwe waarden.

```csharp
if (page.UnitType == UnitType.Inch)
{
    options.PageHeight = CommonHelper.INtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.INtoPixels(sizeExtX, CommonHelper.DPI);
}
else if (page.UnitType == UnitType.Millimeter)
{
    options.PageHeight = CommonHelper.MMtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.MMtoPixels(sizeExtX, CommonHelper.DPI);
}
else
{
    options.PageHeight = (float)sizeExtY;
    options.PageWidth = (float)sizeExtX;
}
```

## Stap 9: Sla het JPG‑bestand op

Bind tenslotte de rasterisatie‑opties aan de JPEG‑opties en sla de afbeelding op schijf op.

```csharp
jpegOptions.VectorRasterizationOptions = options;
image.Save(fs, jpegOptions);
}
```

Wanneer de lus is voltooid, heeft u een JPG‑bestand voor elke indeling, elk exact passend bij de oorspronkelijke DWF‑afmetingen.

## Veelvoorkomende problemen en oplossingen

| Symptoom | Waarschijnlijke oorzaak | Oplossing |
|----------|--------------------------|-----------|
| Lege JPG‑output | `options.Layouts` niet correct ingesteld | Controleer of de indelingsnaam overeenkomt met `page.Name`. |
| Vervormde afbeelding | Verkeerde DPI‑conversie | Gebruik `CommonHelper.DPI = 300` (of uw doel‑DPI) vóór conversie. |
| Bestand niet gevonden | Onjuist `MyDir`‑pad | Gebruik absolute paden of `Path.Combine`. |
| Licentie‑exception | Geen licentie toegepast | Laad een tijdelijke of permanente licentie vóór het aanroepen van `Image.Load`. |

## Veelgestelde vragen

### Q1: Is Aspose.CAD compatibel met de nieuwste DWG‑bestandformaten?

A1: Aspose.CAD ondersteunt verschillende DWG‑bestandformaten, inclusief de nieuwste versies. Raadpleeg de [documentation](https://reference.aspose.com/cad/net/) voor specifieke compatibiliteitsdetails.

### Q2: Kan ik Aspose.CAD gebruiken voor zowel commerciële als persoonlijke projecten?

A2: Ja, Aspose.CAD biedt flexibele licentie‑opties voor zowel commercieel als persoonlijk gebruik. Bezoek de [purchase page](https://purchase.aspose.com/buy) voor meer details.

### Q3: Hoe kan ik een tijdelijke licentie voor Aspose.CAD verkrijgen?

A3: U kunt een tijdelijke licentie verkrijgen via [here](https://purchase.aspose.com/temporary-license/) voor evaluatiedoeleinden.

### Q4: Waar kan ik ondersteuning voor Aspose.CAD vinden?

A4: Voor vragen of hulp, bezoek het [Aspose.CAD forum](https://forum.aspose.com/c/cad/19).

### Q5: Is er een gratis proefversie beschikbaar voor Aspose.CAD?

A5: Ja, u kunt een gratis proefversie van Aspose.CAD [here](https://releases.aspose.com/) verkrijgen.

### Q6: Hoe converteer ik een DWG‑bestand direct naar JPG zonder eerst DWF te extraheren?

A6: U kunt het DWG‑bestand laden met `Aspose.CAD.Image.Load` en dezelfde rasterisatie‑workflow gebruiken; stel gewoon `options.Layouts` in op de gewenste indelingsnaam(men) uit de DWG.

### Q7: Behoudt de conversie de vectorkwaliteit?

A7: Zodra gerasterd naar JPG, is de afbeelding bitmap‑gebaseerd, waardoor vector‑schaalbaarheid verloren gaat. Voor verliesloze schaalvergroting, overweeg export naar PNG of SVG.

**Laatst bijgewerkt:** 2026-04-06  
**Getest met:** Aspose.CAD 24.11 for .NET  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}