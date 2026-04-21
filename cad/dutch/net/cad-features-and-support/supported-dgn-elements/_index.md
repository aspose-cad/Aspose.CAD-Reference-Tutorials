---
date: 2026-03-29
description: Leer hoe u DGN naar PNG kunt converteren met Aspose.CAD voor .NET. Deze
  gids behandelt ook de ondersteuning van CAD‑bestandsformaten en de volledige set
  ondersteunde DGN‑elementen.
linktitle: Supported DGN Elements
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Converteer DGN naar PNG met Aspose.CAD voor .NET
url: /nl/net/cad-features-and-support/supported-dgn-elements/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DGN naar PNG converteren met Aspose.CAD voor .NET

## Introductie

Bent u een .NET‑ontwikkelaar die **DGN naar PNG** naadloos wil **converteren**? Aspose.CAD voor .NET biedt een robuuste oplossing om DGN‑bestanden efficiënt te verwerken. In deze tutorial gaan we dieper in op de ondersteunde DGN‑elementen, begeleiden we u bij het werken met Aspose.CAD voor .NET en laten we precies zien hoe u die elementen naar PNG‑afbeeldingen exporteert.

## Snelle antwoorden
- **Wat doet Aspose.CAD?** Het leest, wijzigt en converteert CAD/BIM‑bestanden (inclusief DGN) naar rasterformaten zoals PNG.  
- **Kan ik 2D‑ en 3D‑DGN‑elementen converteren?** Ja – zowel 2‑D‑ als 3‑D‑entiteiten worden ondersteund.  
- **Welke .NET‑versies zijn vereist?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Heb ik een licentie nodig voor testen?** Er is een gratis proefversie beschikbaar; een licentie is vereist voor productie.  
- **Waar kan ik de bibliotheek verkrijgen?** Download deze van de officiële Aspose‑site (link hieronder).

## Wat betekent “DGN naar PNG converteren”?
DGN naar PNG converteren betekent het renderen van de vector‑gebaseerde DGN‑tekening (2‑D of 3‑D) naar een rasterafbeeldingsformaat (PNG). Dit is handig wanneer u CAD‑tekeningen op het web wilt weergeven, in rapporten wilt insluiten of miniaturen wilt genereren zonder een CAD‑viewer.

## Waarom Aspose.CAD voor .NET gebruiken voor CAD‑bestandsformaatondersteuning?
- **Volledige CAD‑bestandsformaatondersteuning** – DGN, DWG, DXF, DWF en meer.  
- **Geen externe afhankelijkheden** – pure .NET‑bibliotheek, geen native CAD‑installaties.  
- **High‑fidelity rendering** – behoudt lijndiktes, kleuren en 3‑D‑geometrie.  
- **Batchverwerking** – gemakkelijk door veel bestanden itereren in een server‑side applicatie.

## Vereisten

Voordat we beginnen, zorg ervoor dat u het volgende heeft:

- Basiskennis van .NET‑programmeren.  
- Visual Studio geïnstalleerd op uw machine.  
- Aspose.CAD voor .NET‑bibliotheek, die u kunt downloaden [hier](https://releases.aspose.com/cad/net/).

## Namespaces importeren

Om uw project op te starten, importeert u de benodigde namespaces in uw .NET‑applicatie. Deze stap zorgt ervoor dat u toegang heeft tot de functionaliteiten die door Aspose.CAD voor .NET worden geleverd.

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

## Hoe DGN naar PNG converteren

Hieronder vindt u een stapsgewijze handleiding die u meeneemt door het laden van een DGN‑bestand, het itereren van de elementen, het verwerken van zowel 2‑D‑ als 3‑D‑entiteiten, en uiteindelijk het exporteren van het resultaat naar een PNG‑rasterafbeelding.

### Stap 1: Laad het DGN‑bestand

Begin met het laden van een bestaand DGN‑bestand als een `DgnImage` in uw .NET‑applicatie.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Your code here
}
```

### Stap 2: Doorloop DGN‑elementen

Doorloop de DGN‑elementen met een `foreach`‑lus. Aspose.CAD voor .NET biedt verschillende DGN‑elementtypen waarmee u kunt werken.

```csharp
foreach (DgnDrawingElementBase element in dgnImage.Elements)
{
    // Your code here
}
```

### Stap 3: Verwerk eerder ondersteunde 2‑D‑entiteiten

Deze entiteiten worden nu ook ondersteund voor 3‑D‑rendering. De switch‑statement laat u de logica vertakken op basis van het elementtype.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.Line:
    case DgnElementType.Ellipse:
    case DgnElementType.Curve:
    // Additional cases
        {
            // Your code here
            break;
        }
}
```

### Stap 4: Verwerk ondersteunde 3‑D‑entiteiten

Aspose.CAD voegt volledige ondersteuning toe voor verschillende 3‑D‑DGN‑elementen. Breid de switch uit om ze naar behoefte te verwerken.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.SolidHeader3D:
    case DgnElementType.Cone:
    case DgnElementType.CellHeader:
        {
            // Your code here
            break;
        }
}
```

### Stap 5: Exporteren en opslaan als PNG

Na eventuele benodigde manipulatie, exporteer de DGN‑tekening naar een PNG‑rasterafbeelding en sla deze op in de opgegeven map.

```csharp
Console.WriteLine("\nThe DGN file exported successfully to raster image.\nFile saved at " + MyDir);
```

> **Pro tip:** Gebruik `Image.Save` met `new PngOptions()` om de resolutie, achtergrondkleur en andere PNG‑specifieke instellingen te regelen.

## Overzicht van CAD‑bestandsformaatondersteuning

Aspose.CAD voor .NET is niet beperkt tot DGN. Het ondersteunt ook DWG, DXF, DWF en vele andere CAD‑formaten, waardoor u één API heeft om een breed scala aan technische tekeningen te verwerken. Dit maakt het ideaal voor projecten die **CAD‑bestandsformaatondersteuning** over meerdere standaarden vereisen.

## Veelvoorkomende problemen & oplossingen

| Probleem | Reden | Oplossing |
|----------|-------|-----------|
| **Afbeelding is leeg** | Geëxporteerd met nul DPI | Specificeer `ResolutionX` en `ResolutionY` in `PngOptions`. |
| **Ontbrekende 3‑D‑geometrie** | Elementtype niet verwerkt in switch | Voeg de ontbrekende `DgnElementType`‑case toe en render dienovereenkomstig. |
| **Geheugentekort bij grote bestanden** | Het volledige bestand in één keer laden | Verwerk elementen in batches of gebruik streaming waar mogelijk. |

## Veelgestelde vragen

### Q1: Waar kan ik de documentatie voor Aspose.CAD voor .NET vinden?
U kunt de documentatie vinden [hier](https://reference.aspose.com/cad/net/).

### Q2: Hoe download ik Aspose.CAD voor .NET?
U kunt de bibliotheek downloaden [hier](https://releases.aspose.com/cad/net/).

### Q3: Is er een gratis proefversie beschikbaar voor Aspose.CAD voor .NET?
Ja, u kunt de gratis proefversie krijgen [hier](https://releases.aspose.com/).

### Q4: Waar kan ik tijdelijke licenties voor Aspose.CAD voor .NET krijgen?
Tijdelijke licenties zijn beschikbaar [hier](https://purchase.aspose.com/temporary-license/).

### Q5: Hulp nodig of vragen?
Bezoek het Aspose.CAD voor .NET community [support forum](https://forum.aspose.com/c/cad/19).

---

**Laatst bijgewerkt:** 2026-03-29  
**Getest met:** Aspose.CAD voor .NET 24.11  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}