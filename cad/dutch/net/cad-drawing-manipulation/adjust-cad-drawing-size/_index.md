---
date: 2026-03-19
description: Leer hoe u CAD‑tekeningen in .NET kunt schalen met Aspose.CAD, inclusief
  hoe u CAD‑tekeningeenheden schaalt en de lay‑outgrootte aanpast. Volg onze stap‑voor‑stap‑gids.
linktitle: Adjusting CAD Drawing Size
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Hoe CAD-tekeningen te schalen met Aspose.CAD voor .NET
url: /nl/net/cad-drawing-manipulation/adjust-cad-drawing-size/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hoe CAD‑tekeningen te schalen met Aspose.CAD voor .NET

## Introductie

Als u **CAD‑bestanden wilt schalen** direct vanuit uw .NET‑applicatie, bent u hier aan het juiste adres. In deze tutorial laten we u zien hoe u CAD‑eenheidsinstellingen wijzigt, de afmetingen van een CAD‑tekening schaalt en de CAD‑grootte programmatically aanpast met Aspose.CAD voor .NET. Aan het einde van de gids heeft u een solide, productie‑klare oplossing voor het schalen van elk ondersteund CAD‑formaat.

## Snelle antwoorden
- **Welke bibliotheek is vereist?** Aspose.CAD for .NET  
- **Kan ik het eenheidstype wijzigen?** Ja – stel `UnitType` in `CadRasterizationOptions`  
- **Is een licentie nodig voor productie?** Een geldige Aspose.CAD‑licentie is vereist voor niet‑trial gebruik  
- **Naar welk beeldformaat exporteert het voorbeeld?** BMP (maar elk ondersteund rasterformaat werkt)  
- **Hoeveel regels code?** Minder dan 30 regels voor een volledige schaalbewerking  

## Wat betekent “CAD schalen” in de praktijk?
Het schalen van een CAD‑tekening betekent het converteren van de vectordata naar een rasterafbeelding op een specifieke schaal of eenheid (bijv. centimeters, inches). Dit is handig wanneer u tekeningen in rapporten wilt insluiten, miniaturen wilt genereren of CAD‑visualisaties in webpagina's wilt integreren.

## Waarom CAD‑grootte aanpassen met Aspose.CAD?
- **Geen externe CAD‑software** – alles draait binnen uw .NET‑code.  
- **Fijne controle** over eenheden, lay-outs en rasterisatie‑opties.  
- **Cross‑formaatondersteuning** – dezelfde code werkt voor DWG, DXF, DWF en meer.  

## Vereisten

Voordat we beginnen, zorg ervoor dat u het volgende heeft:

- Aspose.CAD for .NET bibliotheek: download en installeer de bibliotheek vanaf de [Aspose.CAD for .NET downloadpagina](https://releases.aspose.com/cad/net/).  
- Voorbeeld CAD‑tekening: een bestand zoals `sample.dwg` geplaatst in de documentmap van uw project.  

## Namespaces importeren

Importeer eerst de namespaces die u toegang geven tot de klassen van Aspose.CAD.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Stap 1: Laad de CAD‑tekening

Laad het bronbestand in een `Image`‑object. Dit object vertegenwoordigt de CAD‑tekening in het geheugen en vormt de basis voor alle verdere bewerkingen.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "sample.dwg";

// Load a CAD drawing in an instance of Image
using (var image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // Your code here...
}
```

## Stap 2: Maak BmpOptions (of een ander rasterformaat)

`BmpOptions` vertelt Aspose.CAD hoe de vectordata moet worden gerenderd wanneer u deze opslaat als bitmap. U kunt dit vervangen door `PngOptions`, `JpegOptions`, enz., afhankelijk van uw doelformaat.

```csharp
Aspose.CAD.ImageOptions.BmpOptions bmpOptions = new Aspose.CAD.ImageOptions.BmpOptions();
```

## Stap 3: Stel CadRasterizationOptions in

`CadRasterizationOptions` bevat de kerninstellingen voor schalen, eenheidsconversie en lay-outselectie. Door het te koppelen aan de `VectorRasterizationOptions`‑eigenschap van `BmpOptions` zorgt u ervoor dat de rasterizer uw aangepaste instellingen gebruikt.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions cadRasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
bmpOptions.VectorRasterizationOptions = cadRasterizationOptions;
```

## Stap 4: Stel UnitType in (CAD‑eenheid wijzigen)

Hier wijzigen we de CAD‑eenheid van de standaardwaarde naar centimeters. Dit is waar het trefwoord **change cad unit** zich bevindt, en het beïnvloedt direct de uiteindelijke afbeeldingsgrootte.

```csharp
cadRasterizationOptions.UnitType = Aspose.CAD.ImageOptions.UnitType.Centimeter;
```

## Stap 5: Kies lay-outs (CAD‑lay-outs instellen)

Als uw tekening meerdere lay-outs bevat (bijv. Model, Sheet1), geef dan aan welke u wilt rasteren. Het selecteren van de juiste lay-out is essentieel wanneer u **set cad layouts** gebruikt voor een geschaalde output.

```csharp
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## Stap 6: Exporteren naar BMP (CAD‑tekening schalen)

Sla tenslotte de gerasterde afbeelding op. Het uitvoerbestand weerspiegelt de nieuwe grootte, eenheid en lay-out die u hebt geconfigureerd – waardoor de **resize CAD drawing** bewerking effectief wordt voltooid.

```csharp
string outPath = sourceFilePath + ".bmp";
image.Save(outPath, bmpOptions);
```

U heeft nu een BMP‑bestand dat de geschaalde CAD‑tekening weergeeft, klaar voor verdere verwerking of weergave.

## Veelvoorkomende problemen en oplossingen

| Probleem | Waarom het gebeurt | Oplossing |
|----------|--------------------|-----------|
| Output is blurry | Low DPI (dots per inch) default | Set `cadRasterizationOptions.Resolution = 300;` before saving |
| Wrong layout appears | Layout name typo | Verify the exact layout name using a CAD viewer or the `Layouts` collection |
| Unit conversion looks off | Mixing metric and imperial units | Ensure `UnitType` matches the desired measurement system |

## Veelgestelde vragen

### Q1: Is Aspose.CAD for .NET compatibel met alle CAD‑formaten?

A1: Aspose.CAD for .NET ondersteunt een breed scala aan CAD‑formaten, waaronder DWG, DXF, DWF en meer. Bekijk de [documentatie](https://reference.aspose.com/cad/net/) voor de volledige lijst.

### Q2: Kan ik meerdere lay-outs tegelijk schalen?

A2: Ja, u kunt meerdere lay-outs schalen door de `Layouts`‑array in de `CadRasterizationOptions` aan te passen.

### Q3: Waar kan ik ondersteuning krijgen voor Aspose.CAD for .NET?

A3: Bezoek het [Aspose.CAD‑forum](https://forum.aspose.com/c/cad/19) voor community‑ondersteuning en hulp.

### Q4: Is er een gratis proefversie beschikbaar?

A4: Ja, u kunt een [gratis proefversie](https://releases.aspose.com/) verkennen om de functies van Aspose.CAD for .NET te evalueren.

### Q5: Hoe kan ik een tijdelijke licentie voor Aspose.CAD for .NET verkrijgen?

A5: Verkrijg een tijdelijke licentie voor testdoeleinden [hier](https://purchase.aspose.com/temporary-license/).

## Veelgestelde vragen

**Q: Hoe schaal ik een CAD‑tekening zonder de eenheid te wijzigen?**  
A: Pas de `Zoom`‑eigenschap van `CadRasterizationOptions` aan (bijv. `cadRasterizationOptions.Zoom = 2.0;`) om de grootte te verdubbelen terwijl u de oorspronkelijke eenheid behoudt.

**Q: Kan ik exporteren naar andere formaten dan BMP?**  
A: Zeker. Vervang `BmpOptions` door `PngOptions`, `JpegOptions` of een andere ondersteunde rasterformaat‑klasse.

**Q: Is het mogelijk om een map met tekeningen batch‑matig te verwerken?**  
A: Ja. Loop door de bestanden in een map, pas dezelfde rasterisatie‑logica toe en sla elke uitvoer op met een unieke naam.

---

**Laatst bijgewerkt:** 2026-03-19  
**Getest met:** Aspose.CAD for .NET 24.11 (latest at time of writing)  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}