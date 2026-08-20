---
date: 2026-03-29
description: Leer hoe u een PDF maakt vanuit CAD, de canvasgrootte instelt en CAD
  exporteert naar PDF of TIFF met Aspose.CAD voor .NET in deze stap‑voor‑stap‑gids.
linktitle: Setting Canvas Size and Mode
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 'Hoe PDF te maken vanuit CAD: Canvasgrootte en modus instellen in Aspose.CAD
  voor .NET'
url: /nl/net/cad-features-and-support/setting-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Instellen van Canvasgrootte en Modus in Aspose.CAD voor .NET

## Introductie

Klaar om **PDF uit CAD** bestanden te maken terwijl u de uitvoerafmetingen controleert? In deze tutorial lopen we door het instellen van de canvasgrootte en modus, het laden van een CAD‑bestand, en het exporteren naar PDF of TIFF met Aspose.CAD voor .NET. Of u nu **DXF naar PDF wilt converteren**, hoge‑resolutie tekeningen wilt genereren, of simpelweg het rasterisatiegebied wilt aanpassen, de onderstaande stappen bieden een solide, productie‑klare oplossing.

## Snelle Antwoorden
- **Wat betekent “create PDF from CAD”?** Een CAD‑tekening (bijv. DXF, DWG) omzetten naar een PDF‑document dat vector‑ en rasterdetails behoudt.  
- **Welke optie bepaalt de uitvoergrootte?** `CadRasterizationOptions.PageWidth` en `PageHeight` (canvasgrootte).  
- **Kan ik ook naar TIFF exporteren?** Ja – gebruik `TiffOptions` met dezelfde rasterisatie‑instellingen.  
- **Heb ik een licentie nodig voor productie?** Een commerciële licentie is vereist; een gratis proefversie is beschikbaar.  
- **Ondersteunde .NET‑versies?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## Wat is “create PDF from CAD”?
Het maken van een PDF uit CAD betekent dat de CAD‑tekening wordt gerenderd naar een paginageoriënteerd formaat (PDF) dat kan worden bekeken, afgedrukt of gedeeld zonder dat CAD‑software nodig is. Aspose.CAD doet het zware werk, zodat u canvasgrootte, schaal en uitvoerformaat kunt definiëren.

## Waarom canvasgrootte instellen bij het maken van PDF uit CAD?
Het instellen van de canvasgrootte geeft u precieze controle over de resolutie en afmetingen van de resulterende PDF of TIFF. Dit is vooral nuttig wanneer:
- Het voorbereiden van tekeningen voor afdrukken op specifieke papierformaten.  
- Miniaturen of hoge‑resolutie afbeeldingen genereren voor web‑preview.  
- Zorgen voor een consistente lay-out over meerdere documenten.

## Vereisten

- Aspose.CAD Bibliotheek: Download en installeer de Aspose.CAD bibliotheek van de [Aspose.CAD website](https://releases.aspose.com/cad/net/).
- Ontwikkelomgeving: Zorg ervoor dat u een .NET ontwikkelomgeving op uw machine hebt ingesteld.
- Voorbeeld CAD‑bestand: Voor deze tutorial gebruiken we een voorbeeld‑DXF‑bestand. U kunt er een vinden in de [Aspose.CAD documentatie](https://reference.aspose.com/cad/net/).

## Namespaces Importeren

Importeer eerst de namespaces die nodig zijn voor CAD‑verwerking:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Hoe PDF uit CAD maken met aangepaste canvasgrootte

### Stap 1: CAD‑bestand laden

We beginnen met het **laden van het CAD‑bestand** (bijv. een DXF) in een `Image`‑object. Dit is het moment waarop u het CAD‑bestand in het geheugen **laadt**.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    // Your code for further steps will go here
}
```

### Stap 2: CadRasterizationOptions maken

Maak een `CadRasterizationOptions`‑instance en definieer de canvasgrootte. De eigenschappen `PageWidth` en `PageHeight` laten u **canvasgrootte instellen** op de exacte afmetingen die u nodig heeft.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
rasterizationOptions.NoScaling = false;
```

### Stap 3: PdfOptions maken (CAD exporteren naar PDF)

Koppel de rasterisatie‑instellingen aan een `PdfOptions`‑object. Deze configuratie stelt u in staat om **CAD naar PDF te exporteren** met het aangepaste canvas dat u hebt gedefinieerd.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### Stap 4: Exporteren naar PDF (DXF naar PDF converteren)

Sla nu het beeld op als een PDF. Deze stap **maakt PDF uit CAD** met behulp van de ingestelde opties.

```csharp
image.Save(MyDir + "result_out.pdf", pdfOptions);
```

### Stap 5: TiffOptions maken (CAD exporteren naar TIFF)

Als u ook een rasterafbeelding nodig heeft, configureer dan `TiffOptions`. Dezelfde rasterisatie‑opties worden hergebruikt, zodat de **export CAD naar TIFF** de canvasgrootte respecteert.

```csharp
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.VectorRasterizationOptions = rasterizationOptions;
```

### Stap 6: Exporteren naar TIFF

Sla ten slotte de tekening op als een TIFF‑bestand.

```csharp
image.Save(MyDir + "result_out.tiff", tiffOptions);
```

## Veelvoorkomende Problemen en Oplossingen

- **Canvas wordt bijgesneden** – Controleer of `AutomaticLayoutsScaling` is ingesteld op `true` en `NoScaling` op `false` zodat de tekening schaalt om op het canvas te passen.  
- **Lage resolutie PDF** – Verhoog `PageWidth`/`PageHeight` of stel `Resolution` in op `CadRasterizationOptions`.  
- **Bestand niet gevonden fout** – Zorg ervoor dat `MyDir` naar een geldige map wijst en dat de DXF‑bestandsnaam exact overeenkomt.

## Veelgestelde Vragen

### Q1: Kan ik Aspose.CAD gebruiken met andere .NET‑bibliotheken?
A1: Ja, Aspose.CAD integreert naadloos met andere .NET‑bibliotheken en biedt uitgebreide mogelijkheden voor CAD‑manipulatie.

### Q2: Is er een gratis proefversie beschikbaar voor Aspose.CAD?
A2: Ja, u kunt de functies van Aspose.CAD verkennen met een gratis proefversie. Bezoek [hier](https://releases.aspose.com/) om te beginnen.

### Q3: Hoe kan ik ondersteuning krijgen voor Aspose.CAD?
A3: Voor ondersteuning en discussies, bezoek het [Aspose.CAD forum](https://forum.aspose.com/c/cad/19).

### Q4: Waar kan ik uitgebreide documentatie vinden voor Aspose.CAD?
A4: Raadpleeg de [Aspose.CAD documentatie](https://reference.aspose.com/cad/net/) voor gedetailleerde informatie en voorbeelden.

### Q5: Hoe koop ik Aspose.CAD voor .NET?
A5: Om Aspose.CAD aan te schaffen, ga naar de [aankooppagina](https://purchase.aspose.com/buy).

**Aanvullende Vragen & Antwoorden**

**V: Kan ik een meer‑pagina CAD‑tekening exporteren naar één PDF?**  
**A: Ja. Stel `PageCount` in `CadRasterizationOptions` in en de bibliotheek zal de pagina's samenvoegen tot één PDF.**

**V: Heeft de canvasgrootte invloed op de kwaliteit van vectorgegevens?**  
**A: Vectorgegevens blijven resolutie‑onafhankelijk; de canvasgrootte beïnvloedt alleen gerasterde elementen en de beeldresolutie.**

---

**Laatst bijgewerkt:** 2026-03-29  
**Getest met:** Aspose.CAD 24.11 voor .NET  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}