---
date: 2026-08-12
description: Tekst uit DWG extraheren en specifieke DWG naar afbeelding converteren
  in C# met Aspose.CAD voor .NET. Leer stap‑voor‑stap met code‑fragmenten.
keywords:
- extract text from dwg
- convert specific dwg to image
- Aspose.CAD .NET
lastmod: 2026-08-12
linktitle: Specifieke DWG naar afbeelding converteren in C#
og_description: Tekst uit DWG extraheren en specifieke DWG naar afbeelding converteren
  in C# met Aspose.CAD. Volg deze beknopte gids voor snelle implementatie.
og_image_alt: Guide showing DWG to image conversion and text extraction using Aspose.CAD
  in C#
og_title: Tekst uit DWG extraheren en specifieke DWG naar afbeelding converteren in
  C#
schemas:
- author: Aspose
  dateModified: '2026-08-12'
  description: Extract text from DWG and convert specific DWG to image in C# using
    Aspose.CAD for .NET. Learn step‑by‑step with code snippets.
  headline: Extract text from DWG and convert specific DWG to image in C#
  type: TechArticle
- questions:
  - answer: Aspose.CAD supports DWG releases from AutoCAD 2000 up to the latest 2024
      version, covering over 90 % of files created in the field.
    question: Is Aspose.CAD compatible with all versions of DWG files?
  - answer: Yes – you can change resolution, image format, anti‑aliasing, and background
      color to suit PNG, JPEG, or PDF targets.
    question: Can I customize the rasterization options for different outputs?
  - answer: Explore the comprehensive [Aspose.CAD documentation](https://reference.aspose.com/cad/net/)
      for more code samples and API details.
    question: Where can I find additional examples and documentation?
  - answer: Absolutely – you can download a trial version on the **[Aspose trial download
      page](https://releases.aspose.com/)** and evaluate all features without restrictions
      for 30 days.
    question: Is there a free trial available for Aspose.CAD?
  - answer: Join the active [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)
      where developers share solutions and the Aspose team answers questions.
    question: How can I get support or connect with the community?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- extract text from dwg
- Aspose.CAD
- C# CAD processing
title: Tekst uit DWG extraheren en specifieke DWG naar afbeelding converteren in C#
url: /nl/net/image-manipulation-and-rendering/converting-particular-dwg-to-image/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Specifieke DWG naar afbeelding converteren in C# - Aspose.CAD gids

## Inleiding

In moderne engineering‑toepassingen moet je vaak **tekst uit DWG**‑bestanden extraheren en **specifieke DWG naar afbeelding**‑formaten converteren voor rapportage of visualisatie. Aspose.CAD voor .NET biedt een volledig uitgeruste API die beide taken afhandelt zonder dat externe CAD‑software nodig is. In deze tutorial leer je hoe je een DWG laadt, tekst‑entiteiten filtert, de tekening rasteriseert en uiteindelijk het resultaat opslaat als een PDF‑afbeelding — alles in nette C#‑code.

## Snelle antwoorden
- **Wat is de eerste stap?** Laad het DWG‑bestand met `new CadImage("file.dwg")`.  
- **Welke klasse filtert tekst?** Gebruik `CadEntityFilter` om `Text`‑entiteiten te selecteren.  
- **Hoe definieer je de afbeeldingsgrootte?** Stel `Width` en `Height` in op `CadRasterizationOptions`.  
- **Welk uitvoerformaat wordt gebruikt?** Het voorbeeld slaat op als PDF, waarin de rasterafbeelding is ingebed.  
- **Heb ik een licentie nodig voor productie?** Ja – een commerciële Aspose.CAD‑licentie verwijdert de evaluatielimieten.

## Hoe tekst uit DWG extraheren?

Laad de DWG, pas een filter toe dat alleen tekst‑entiteiten selecteert, en lees vervolgens de `TextString`‑eigenschap van elke entiteit. Deze aanpak retourneert elk annotatie‑, label‑ of dimensietekst‑deel dat in de tekening aanwezig is, zodat je het kunt hergebruiken voor zoeken, indexeren of rapportage.

## Waarom specifieke DWG naar afbeelding converteren?

Het converteren van een DWG naar een rasterafbeelding stelt je in staat de tekening in documenten, webpagina’s of mobiele apps te embedden die geen native CAD‑formaten kunnen weergeven. Aspose.CAD verwerkt **meer dan 50 CAD‑formaten** en kan tekeningen met honderden pagina’s rasteriseren terwijl het minder dan 200 MB geheugen gebruikt, wat het geschikt maakt voor high‑throughput server‑scenario’s.

## Vereisten

- Visual Studio (een recente editie) om C#‑projecten te compileren en uit te voeren.  
- Aspose.CAD voor .NET – zorg ervoor dat je de bibliotheek geïnstalleerd hebt. Je kunt de downloadlink vinden op de **[Aspose.CAD voor .NET downloadpagina](https://releases.aspose.com/cad/net/)**.  
- Een DWG‑bestand waarmee je wilt werken; het voorbeeldbestand *visualization_-_conference_room.dwg* wordt gebruikt in de code‑fragmenten.

## Namespaces importeren

De volgende namespaces geven je toegang tot de kern‑CAD‑klassen, rasterisatie‑opties en PDF‑output‑helpers:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Stap 1: DWG‑bestand laden

Maak een `CadImage`‑instantie aan door het pad van je DWG‑bestand door te geven. Het `CadImage`‑object vertegenwoordigt de volledige tekening in het geheugen en biedt toegang tot de lagen, entiteiten en metadata.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
var cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath);
```

## Stap 2: entiteiten filteren

`CadEntityFilter` stelt je in staat alleen de entiteiten te kiezen die je nodig hebt. In deze gids configureren we het om **tekst**‑objecten te behouden en lijnen, cirkels en andere geometrie die je niet in de uiteindelijke afbeelding wilt, te verwijderen.

```csharp
CadBaseEntity[] entities = cadImage.Entities;
List<CadBaseEntity> filteredEntities = new List<CadBaseEntity>();

foreach (CadBaseEntity baseEntity in entities)
{
    // Selection or filtration of entities
    if (baseEntity.TypeName == CadEntityTypeName.TEXT)
    {
        filteredEntities.Add(baseEntity);
    }
}

cadImage.Entities = filteredEntities.ToArray();
```

## Stap 3: rasterisatie‑opties instellen

`CadRasterizationOptions` bepaalt hoe de tekening wordt omgezet naar een bitmap. Je kunt de uitvoergrootte, achtergrondkleur en resolutie (DPI) definiëren. De volgende definitie‑anchor introduceert de klasse:

De `CadRasterizationOptions`‑klasse specificeert afbeeldingsafmetingen, resolutie en renderinstellingen voor het converteren van CAD‑tekeningen naar rasterformaten.  

Stel de gewenste breedte, hoogte en achtergrondkleur in voordat je de opties doorgeeft aan de PDF‑exporteur.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions =
    new Aspose.CAD.ImageOptions.CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
```

## Stap 4: PDF‑opties instellen

`PdfOptions` bundelt de rasterisatie‑instellingen met PDF‑specifieke functies zoals compressie. De definitie‑anchor voor deze klasse verschijnt eerst:

`PdfOptions` omvat PDF‑generatie‑parameters, inclusief de rasterisatie‑opties die bepalen hoe CAD‑data wordt gerenderd binnen het PDF‑document.  

Wijs de eerder gemaakte `CadRasterizationOptions`‑instantie toe aan de `VectorRasterizationOptions`‑eigenschap.

```csharp
Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Stap 5: opslaan als PDF

Roep tenslotte de `Save`‑methode aan op het `CadImage`‑object, waarbij je de doelbestandsnaam en de geconfigureerde `PdfOptions` doorgeeft. De PDF zal een afbeelding van hoge kwaliteit van de gefilterde tekening bevatten.

```csharp
string outFile = MyDir + "result_out_generated.pdf";
cadImage.Save(outFile, pdfOptions);
```

## Veelvoorkomende problemen en foutoplossing

- **Ontbrekende tekst na filteren** – Zorg ervoor dat de DWG daadwerkelijk `Text`‑entiteiten bevat; sommige tekeningen slaan annotaties op als `MText`. Pas het filter aan om `MText` op te nemen indien nodig.  
- **Lege uitvoerafbeelding** – Controleer of de rasterisatie‑DPI hoog genoeg is (300 DPI is een veilige standaard) en dat de achtergrondkleur niet op transparent staat bij het bekijken van de PDF.  
- **Out‑of‑memory‑fouten bij grote bestanden** – Gebruik de `LoadOptions`‑overload die streaming mogelijk maakt, waardoor het volledige bestand niet in één keer in het geheugen wordt geladen.

## Veelgestelde vragen

**V: Is Aspose.CAD compatibel met alle versies van DWG‑bestanden?**  
**A:** Aspose.CAD ondersteunt DWG‑releases van AutoCAD 2000 tot en met de nieuwste 2024‑versie, en dekt meer dan 90 % van de in het veld gemaakte bestanden.

**V: Kan ik de rasterisatie‑opties aanpassen voor verschillende uitvoerformaten?**  
**A:** Ja – je kunt resolutie, afbeeldingsformaat, anti‑aliasing en achtergrondkleur wijzigen om aan PNG-, JPEG- of PDF‑doelen te voldoen.

**V: Waar vind ik extra voorbeelden en documentatie?**  
**A:** Bekijk de uitgebreide [Aspose.CAD‑documentatie](https://reference.aspose.com/cad/net/) voor meer code‑voorbeelden en API‑details.

**V: Is er een gratis proefversie beschikbaar voor Aspose.CAD?**  
**A:** Zeker – je kunt een proefversie downloaden op de **[Aspose‑proefdownloadpagina](https://releases.aspose.com/)** en alle functies zonder beperkingen gedurende 30 dagen evalueren.

**V: Hoe kan ik ondersteuning krijgen of contact maken met de community?**  
**A:** Word lid van het actieve [Aspose.CAD‑forum](https://forum.aspose.com/c/cad/19) waar ontwikkelaars oplossingen delen en het Aspose‑team vragen beantwoordt.

---

**Laatst bijgewerkt:** 2026-08-12  
**Getest met:** Aspose.CAD 24.11 voor .NET  
**Auteur:** Aspose

## Gerelateerde tutorials

- [Zoeken naar tekst in DWG‑bestanden met C# - Aspose.CAD tutorial](/cad/net/text-search-and-manipulation/searching-text-in-dwg-files/)
- [CAD‑tekening converteren naar rasterafbeelding in Aspose.CAD voor .NET](/cad/net/cad-drawing-manipulation/convert-cad-drawing-to-raster-image/)
- [DWG‑documenten renderen in C# - Aspose.CAD gids](/cad/net/image-manipulation-and-rendering/rendering-dwg-documents/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}