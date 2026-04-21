---
date: 2026-03-29
description: Leer hoe u CAD‑rasterisatieopties configureert en DGN naar PDF exporteert
  met 3D‑ondersteuning met behulp van Aspose.CAD voor .NET.
linktitle: Support of 3D for DGN V7
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Configureer CAD-rasterisatie‑opties voor DGN V7 3D
url: /nl/net/cad-features-and-support/support-of-3d-for-dgn-v7/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Configureer CAD-rasterisatie-opties voor DGN V7 3D

## Inleiding

In deze uitgebreide tutorial leer je **hoe je CAD-rasterisatie-opties configureert** om een 3‑D DGN V7-bestand naar PDF te exporteren met Aspose.CAD voor .NET. Of je nu een CAD-viewer, een rapportagetool of een geautomatiseerde conversiepijplijn bouwt, het beheersen van deze instellingen geeft je nauwkeurige controle over paginagrootte, lay-outschaling, achtergrondkleuren en de specifieke weergaven die je wilt renderen. Laten we stap voor stap door het proces lopen.

## Snelle antwoorden
- **Wat betekent “configure CAD rasterization options”?**  
  Het verwijst naar het instellen van eigenschappen zoals paginadimensies, schaal, achtergrondkleur en lay-outselectie voordat een CAD-bestand naar een rasterformaat (bijv. PDF) wordt geconverteerd.
- **Hoe exporteer je DGN naar PDF met 3‑D-ondersteuning?**  
  Laad de DGN met `DgnImage`, definieer `PdfOptions` + `CadRasterizationOptions`, en roep vervolgens `Save` aan.
- **Heb ik een licentie nodig voor productiegebruik?**  
  Ja – een commerciële licentie is vereist voor implementatie; een gratis proefversie is beschikbaar.
- **Welke .NET-versies worden ondersteund?**  
  .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.
- **Kan ik specifieke weergaven kiezen om te exporteren?**  
  Absoluut – stel de `Layouts`-array in de rasterisatie‑opties in.

## Wat is “configure CAD rasterization options”?

Het configureren van CAD-rasterisatie‑opties betekent het aanpassen van hoe een CAD-tekening wordt gerasterd (omgezet van vector naar bitmap of PDF). Door deze instellingen aan te passen beheer je de visuele output, prestaties en bestandsgrootte van het resulterende document.

## Waarom Aspose.CAD gebruiken voor 3‑D DGN V7-export?

- **Volledige .NET-integratie** – geen COM of native DLL's vereist.  
- **Ondersteunt 3‑D-geometry** – behoudt diepte-informatie bij het renderen naar PDF.  
- **Fijne controle** – kies exacte lay-outs, schaal en achtergrondkleuren.  
- **Cross‑platform** – werkt op Windows, Linux en macOS met .NET Core.

## Vereisten

Voordat je begint, zorg ervoor dat je het volgende hebt:

- **Aspose.CAD for .NET** – download het van [hier](https://releases.aspose.com/cad/net/).  
- **Visual Studio** of een andere compatibele .NET IDE.  
- **Een voorbeeld DGN‑bestand** – voor deze gids gebruiken we `Nikon_D90_Camera.dgn` (bijgevoegd in het Aspose‑voorbeeldpakket).  

Nu alles klaar is, duiken we in de code.

## Namespaces importeren

In je .NET‑project, importeer de vereiste namespaces:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.ImageOptions;
```

## Stap 1: Stel uw documentmap in

Maak een variabele die verwijst naar de map waar je bron‑DGN en de uitvoerbestanden zich bevinden.

```csharp
string MyDir = "Your Document Directory";
```

## Stap 2: Laad het DGN‑bestand

Laad het DGN‑bestand als een `DgnImage`. Dit object geeft je toegang tot de CAD‑gegevens en de rasterisatie‑pipeline.

```csharp
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";
string outFile = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Your code for further processing goes here
}
```

## Stap 3: Configureer PDF‑exportopties (Configure CAD Rasterization Options)

Hier **configureren we CAD-rasterisatie‑opties** die bepalen hoe het 3‑D‑model wordt gerenderd naar PDF. Je kunt paginagrootte aanpassen, automatische lay‑outschaling inschakelen, een achtergrondkleur instellen en de exacte lay-outs (weergaven) kiezen die je wilt exporteren.

```csharp
var options = new PdfOptions
{
    VectorRasterizationOptions = new CadRasterizationOptions
    {
        PageWidth = 1500,
        PageHeight = 1500,
        AutomaticLayoutsScaling = true,
        BackgroundColor = Color.Black,
        Layouts = new string[] { "1", "2", "3", "9" } // Only export specified views
    }
};
```

## Stap 4: Sla het raster‑beeld op

Exporteer tenslotte de DGN naar een PDF‑bestand met de opties die je zojuist hebt geconfigureerd.

```csharp
dgnImage.Save(outFile, options);
```

## Veelvoorkomende problemen en oplossingen

| Probleem | Oplossing |
|----------|-----------|
| **Lege PDF-uitvoer** | Controleer of de `Layouts`-array de juiste weergave‑identifiers bevat die in het DGN‑bestand aanwezig zijn. |
| **Onjuiste kleuren** | Zorg ervoor dat `BackgroundColor` is ingesteld op de gewenste waarde; gebruik `Color.White` voor een lichte achtergrond. |
| **Prestatie‑knelpunt bij grote bestanden** | Schakel `AutomaticLayoutsScaling` in en overweeg `PageWidth/PageHeight` te verkleinen voor een lagere rasterresolutie. |
| **Licentie‑exception** | Installeer een geldige Aspose.CAD‑licentie voordat je de afbeelding laadt om proef‑watermerken te vermijden. |

## Veelgestelde vragen

**Q: Kun ik Aspose.CAD voor .NET gebruiken met andere CAD‑bestandsformaten?**  
A: Ja, Aspose.CAD ondersteunt DWG, DXF, DWF, DGN en nog veel meer formaten.

**Q: Hoe kan ik uitzonderingen afhandelen bij het werken met Aspose.CAD?**  
A: Plaats je code in een `try‑catch`‑blok en inspecteer `Aspose.CAD.CADException` voor gedetailleerde foutinformatie.

**Q: Is Aspose.CAD geschikt voor commerciële projecten?**  
A: Absoluut. Je kunt een licentie aanschaffen [hier](https://purchase.aspose.com/buy).

**Q: Kan ik Aspose.CAD voor .NET uitproberen voordat ik koop?**  
A: Ja, een gratis proefversie is beschikbaar [hier](https://releases.aspose.com/).

**Q: Waar kan ik community‑ondersteuning vinden voor Aspose.CAD?**  
A: Word lid van het discussieforum [hier](https://forum.aspose.com/c/cad/19).

---

**Laatst bijgewerkt:** 2026-03-29  
**Getest met:** Aspose.CAD 24.11 for .NET  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}