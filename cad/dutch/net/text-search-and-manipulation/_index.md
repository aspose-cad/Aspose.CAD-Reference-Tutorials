---
date: 2026-10-04
description: Leer hoe u tekst kunt zoeken in DWG-bestanden met C# en Aspose.CAD voor
  .NET. Extraheer tekst, lees DWG-bestanden en verbeter uw CAD-toepassingen.
keywords:
- search text in dwg
- extract text from dwg
- c# read dwg file
- how to search dwg files
lastmod: 2026-10-04
linktitle: Tekst zoeken en manipulatie
og_description: Zoek tekst in DWG-bestanden met C# en Aspose.CAD voor .NET. Extraheer
  tekst, lees DWG-bestanden en verbeter de prestaties van CAD-applicaties.
og_image_alt: Guide showing C# code searching text in DWG files with Aspose.CAD
og_title: Zoek tekst in DWG-bestanden met C# en Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-10-04'
  description: Learn how to search text in DWG files using C# and Aspose.CAD for .NET.
    Extract text, read DWG files, and boost your CAD applications.
  headline: Search text in DWG files with C# using Aspose.CAD
  type: TechArticle
- description: Learn how to search text in DWG files using C# and Aspose.CAD for .NET.
    Extract text, read DWG files, and boost your CAD applications.
  name: Search text in DWG files with C# using Aspose.CAD
  steps:
  - name: install the Aspose.CAD NuGet package
    text: 'Open the NuGet Package Manager console and run: This adds the required
      assemblies and updates your project file.'
  - name: open the DWG file
    text: Create a `CadImage` instance by calling `Image.Load`. The method automatically
      detects the file format and prepares an in‑memory representation.
  - name: enumerate text fragments
    text: '`image.TextFragments` returns a collection of `TextFragment` objects, each
      exposing `Text`, `Location`, `Height`, and `LayerName`. You can iterate or LINQ‑filter
      this collection.'
  - name: apply your search criteria
    text: Use `String.Contains`, `Regex.IsMatch`, or any custom predicate to locate
      the exact text you need. For case‑insensitive searches, call `ToLowerInvariant()`
      on both sides.
  - name: handle the results
    text: Typical actions include logging the fragment’s coordinates, exporting to
      CSV, or highlighting the entity in a viewer. Because the API gives you the exact
      `Location`, you can feed it into any downstream CAD visualization component.
  type: HowTo
- questions:
  - answer: Yes. Provide the password via `CadLoadOptions.Password` when calling `Image.Load`.
    question: Can I search for text in password‑protected DWG files?
  - answer: Absolutely. Loop through a directory, load each file, and reuse the same
      LINQ filter – the library is thread‑safe for parallel processing.
    question: Does the API support searching across multiple DWG files at once?
  - answer: Aspose.CAD reports a **99 % success rate** on industry‑standard test sets,
      handling MTEXT, attribute definitions, and even embedded Unicode characters.
    question: How accurate is the text extraction for complex annotations?
  - answer: After obtaining the `Location` of each `TextFragment`, you can draw a
      temporary overlay using any CAD viewer that accepts geometry primitives.
    question: Is there a way to highlight found text in a viewer?
  - answer: The product uses a per‑developer or per‑server license model; a free evaluation
      license is available for 30 days.
    question: What licensing model applies to Aspose.CAD?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- CAD processing
- Aspose.CAD
- .NET
- DWG text search
title: Zoek tekst in DWG-bestanden met C# en Aspose.CAD
url: /nl/net/text-search-and-manipulation/
weight: 28
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Zoek tekst in DWG-bestanden met C# met behulp van Aspose.CAD

## Inleiding

In deze tutorial leer je hoe je **tekst zoeken in DWG** bestanden met C# kunt uitvoeren door gebruik te maken van de krachtige Aspose.CAD for .NET bibliotheek. Of je nu annotaties moet lokaliseren, attribuutwaarden moet extraheren, of een doorzoekbare index moet bouwen, de onderstaande stappen begeleiden je door een betrouwbare, high‑performance oplossing die werkt op zowel .NET Framework als .NET Core.

## Snelle antwoorden
- **Welke bibliotheek behandelt DWG-tekst zoeken?** Aspose.CAD for .NET.
- **Kan ik tekst uit DWG extraheren?** Ja – de API retourneert platte‑tekst strings voor elke gevonden entiteit.
- **Welke .NET-versies worden ondersteund?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.
- **Heb ik een licentie nodig voor ontwikkeling?** Een gratis tijdelijke licentie werkt voor evaluatie; een volledige licentie is vereist voor productie.
- **Is de bewerking geheugen‑efficiënt?** Ja, Aspose.CAD verwerkt bestanden stream‑wise, waardoor multi‑honderd‑pagina DWG‑verwerking mogelijk is zonder het volledige bestand in het RAM te laden.

## Wat is zoeken naar tekst in DWG?

CadImage is het object van Aspose.CAD dat een geladen CAD-tekening vertegenwoordigt en zijn entiteiten, zoals tekstfragmenten, blootlegt.  
TextFragment vertegenwoordigt een individueel stuk geëxtraheerde tekst, inclusief de inhoud en de geometrische locatie.

De uitdrukking *search text in DWG* verwijst naar het programmatically lokaliseren van tekenreeksgegevens — zoals laagnaam, attribuutwaarden of annotatietekst — binnen een DWG-tekeningsbestand. Aspose.CAD maakt deze mogelijkheid beschikbaar via zijn `CadImage` object en de `TextFragment` collectie, waardoor ontwikkelaars tekst efficiënt kunnen ophalen en manipuleren.

## Waarom Aspose.CAD gebruiken voor het zoeken naar DWG-tekst?

Aspose.CAD ondersteunt **30+ CAD- en BIM-formaten** (inclusief DWG, DXF, DGN, DWF) en kan bestanden verwerken tot **500 MB** zonder volledige in‑geheugen lading. De bibliotheek garandeert **99 % nauwkeurigheid bij tekst‑extractie** op complexe tekeningen, wat een kwantitatieve verbetering is ten opzichte van veel open‑source parsers die vaak ingebedde MTEXT of blok‑attributen missen.

## Hoe tekst zoeken in DWG-bestanden met C#?

Image.Load is een statische methode die een CAD‑bestand leest en een CadImage‑instantie retourneert.  

Laad de DWG met `Image.Load`, haal de `TextFragments` collectie op, en filter deze met LINQ op basis van je zoekterm. Dit beknopte patroon draait in lineaire tijd ten opzichte van het aantal textelementen, vereist geen extra bibliotheken, en werkt consistent in .NET Framework‑ en .NET Core‑omgevingen.

### Stap 1: installeer het Aspose.CAD NuGet‑pakket
Open de NuGet Package Manager console en voer uit:

```
Install-Package Aspose.CAD
```

### Stap 2: open het DWG‑bestand
Maak een `CadImage`‑instantie aan door `Image.Load` aan te roepen. De methode detecteert automatisch het bestandsformaat en bereidt een in‑memory representatie voor.

### Stap 3: doorloop tekstfragmenten
`image.TextFragments` retourneert een collectie van `TextFragment` objecten, elk met `Text`, `Location`, `Height` en `LayerName`. Je kunt deze collectie itereren of met LINQ filteren.

### Stap 4: pas je zoekcriteria toe
Gebruik `String.Contains`, `Regex.IsMatch`, of een aangepaste predicate om de exacte tekst te vinden die je nodig hebt. Voor hoofdletter‑ongevoelige zoekopdrachten, roep `ToLowerInvariant()` aan beide zijden aan.

### Stap 5: verwerk de resultaten
Typische acties omvatten het loggen van de coördinaten van het fragment, exporteren naar CSV, of het markeren van de entiteit in een viewer. Omdat de API je de exacte `Location` geeft, kun je deze doorgeven aan elke downstream CAD‑visualisatiecomponent.

## Hoe tekst extraheren uit DWG?

TextFragment is het object dat geëxtraheerde tekst en de bijbehorende metadata zoals positie en laag bevat.  

Tekst extraheren is identiek aan zoeken; doorloop simpelweg de `TextFragment` collectie en lees elke `TextFragment.Text` eigenschap. Je kunt de strings samenvoegen tot één document, ze naar een CSV‑bestand schrijven, of ze in een zoekindex voeren voor snelle terugwinning over meerdere tekeningen.

## Veelvoorkomende valkuilen en probleemoplossing
- **Ontbrekende MTEXT:** Sommige oudere DWG‑versies slaan meer‑regelige tekst op in blok‑attributen. Zorg ervoor dat je ook `image.Blocks` inspecteert op `Attribute` objecten.  
- **Codering problemen:** DWG‑bestanden kunnen niet‑Unicode codepagina's gebruiken. Stel `image.LoadOptions.Encoding` in op de juiste `System.Text.Encoding` vóór het laden.  
- **Grote bestanden:** Voor bestanden groter dan 200 MB, schakel `image.LoadOptions.Streaming = true` in om het geheugenverbruik onder 100 MB te houden.

## Veelgestelde vragen

**Q: Kan ik zoeken naar tekst in met wachtwoord‑beveiligde DWG‑bestanden?**  
A: Ja. Geef het wachtwoord op via `CadLoadOptions.Password` bij het aanroepen van `Image.Load`.

**Q: Ondersteunt de API zoeken over meerdere DWG‑bestanden tegelijk?**  
A: Absoluut. Loop door een map, laad elk bestand, en hergebruik hetzelfde LINQ‑filter – de bibliotheek is thread‑safe voor parallelle verwerking.

**Q: Hoe nauwkeurig is de tekst‑extractie voor complexe annotaties?**  
A: Aspose.CAD meldt een **99 % succespercentage** op industriestandaard testsets, waarbij MTEXT, attribuutdefinities en zelfs ingebedde Unicode‑tekens worden verwerkt.

**Q: Is er een manier om gevonden tekst te markeren in een viewer?**  
A: Na het verkrijgen van de `Location` van elk `TextFragment`, kun je een tijdelijke overlay tekenen met elke CAD‑viewer die geometrische primitieve accepteert.

**Q: Welk licentiemodel geldt voor Aspose.CAD?**  
A: Het product gebruikt een per‑ontwikkelaar of per‑server licentiemodel; een gratis evaluatielicentie is beschikbaar voor 30 dagen.

**Laatst bijgewerkt:** 2026-10-04  
**Getest met:** Aspose.CAD 24.11 for .NET  
**Auteur:** Aspose  

## Tutorials voor tekst zoeken en manipulatie

### [Tekst zoeken in DWG-bestanden met C# - Aspose.CAD Tutorial](./searching-text-in-dwg-files/)

```csharp
using Aspose.CAD;
using Aspose.CAD.ImageOptions;

// Load the DWG file
using var image = (CadImage)Image.Load("sample.dwg");

// Retrieve all text fragments
var fragments = image.TextFragments;

// Filter fragments that contain the target string
var matches = fragments.Where(t => t.Text.Contains("TargetString"));
```

## Gerelateerde tutorials

- [DWG converteren naar PDF en tekst toevoegen in C# – Aspose.CAD Tutorial](/cad/net/dwg-file-manipulation/adding-text-to-dwg/)
- [Hoe DWG converteren naar PDF en rasterafbeeldingen met Aspose.CAD voor .NET](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [Hoe CAD renderen en DWG converteren – Aspose.CAD .NET](/cad/net/conversion-and-export/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}