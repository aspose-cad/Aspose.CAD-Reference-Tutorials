---
date: 2026-10-04
description: Lär dig hur du söker text i DWG-filer med C# och Aspose.CAD för .NET.
  Extrahera text, läs DWG-filer och förbättra dina CAD-applikationer.
keywords:
- search text in dwg
- extract text from dwg
- c# read dwg file
- how to search dwg files
lastmod: 2026-10-04
linktitle: Textsökning och manipulation
og_description: Sök text i DWG-filer med C# och Aspose.CAD för .NET. Extrahera text,
  läs DWG-filer och förbättra CAD-appens prestanda.
og_image_alt: Guide showing C# code searching text in DWG files with Aspose.CAD
og_title: Sök text i DWG-filer med C# och Aspose.CAD
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
title: Sök text i DWG-filer med C# och Aspose.CAD
url: /sv/net/text-search-and-manipulation/
weight: 28
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Sök text i DWG-filer med C# med Aspose.CAD

## Introduktion

I den här handledningen kommer du att lära dig hur du **söker text i DWG**-filer med C# genom att använda det kraftfulla Aspose.CAD för .NET-biblioteket. Oavsett om du behöver hitta annotationer, extrahera attributvärden eller bygga ett sökbart index, så kommer stegen nedan att guida dig genom en pålitlig, högpresterande lösning som fungerar både på .NET Framework och .NET Core.

## Snabba svar
- **Vilket bibliotek hanterar DWG-textsökning?** Aspose.CAD for .NET.
- **Kan jag extrahera text från DWG?** Ja – API:et returnerar ren‑textsträngar för varje hittad entitet.
- **Vilka .NET‑versioner stöds?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.
- **Behöver jag en licens för utveckling?** En gratis temporär licens fungerar för utvärdering; en full licens krävs för produktion.
- **Är operationen minnes‑effektiv?** Ja, Aspose.CAD bearbetar filer strömbaserat, vilket möjliggör hantering av hundratals DWG‑sidor utan att ladda hela filen i RAM.

## Vad är söktext i DWG?

CadImage är Aspose.CAD:s objekt som representerar en laddad CAD-ritning och exponerar dess entiteter såsom textfragment.  
TextFragment representerar ett enskilt utdrag av extraherad text, inklusive dess innehåll och geometriska position.

Uttrycket *search text in DWG* avser att programatiskt lokalisera strängdata—såsom lagernamn, attributvärden eller annoteringstext—i en DWG-ritningsfil. Aspose.CAD exponerar denna funktionalitet via sitt `CadImage`-objekt och `TextFragment`-samlingen, vilket gör det möjligt för utvecklare att hämta och manipulera text effektivt.

## Varför använda Aspose.CAD för att söka DWG‑text?

Aspose.CAD stödjer **30+ CAD‑ och BIM‑format** (inklusive DWG, DXF, DGN, DWF) och kan bearbeta filer upp till **500 MB** utan fullständig in‑minnet‑laddning. Biblioteket garanterar **99 % noggrannhet vid textutdragning** på komplexa ritningar, vilket är en kvantifierad förbättring jämfört med många öppen‑källkod‑parsers som ofta missar inbäddad MTEXT eller blockattribut.

## Hur söker man text i DWG‑filer med C#?

Image.Load är en statisk metod som läser en CAD‑fil och returnerar en CadImage‑instans.

Läs in DWG‑filen med `Image.Load`, hämta `TextFragments`‑samlingen och filtrera den med LINQ baserat på ditt sökord. Detta koncisa mönster körs i linjär tid i förhållande till antalet textelement, kräver inga extra bibliotek och fungerar konsekvent i både .NET Framework och .NET Core‑miljöer.

### Steg 1: installera Aspose.CAD NuGet‑paketet
Öppna NuGet Package Manager‑konsolen och kör:

```
Install-Package Aspose.CAD
```

Detta lägger till de nödvändiga assembly‑filerna och uppdaterar din projektfil.

### Steg 2: öppna DWG‑filen
Skapa en `CadImage`‑instans genom att anropa `Image.Load`. Metoden upptäcker automatiskt filformatet och förbereder en in‑minnet‑representation.

### Steg 3: enumerera textfragment
`image.TextFragments` returnerar en samling av `TextFragment`‑objekt, där varje objekt exponerar `Text`, `Location`, `Height` och `LayerName`. Du kan iterera eller LINQ‑filtrera denna samling.

### Steg 4: tillämpa dina sökkriterier
Använd `String.Contains`, `Regex.IsMatch` eller någon anpassad predikat för att lokalisera den exakta texten du behöver. För skiftläges‑okänsliga sökningar, anropa `ToLowerInvariant()` på båda sidor.

### Steg 5: hantera resultaten
Typiska åtgärder inkluderar att logga fragmentets koordinater, exportera till CSV eller markera entiteten i en visare. Eftersom API:et ger dig den exakta `Location` kan du föra in den i någon efterföljande CAD‑visualiseringskomponent.

## Hur extraherar man text från DWG?

TextFragment är objektet som innehåller extraherad text och dess associerade metadata såsom position och lager.

Att extrahera text är identiskt med att söka; enumerera helt enkelt `TextFragment`‑samlingen och läs varje `TextFragment.Text`‑egenskap. Du kan konkatenera strängarna till ett enda dokument, skriva dem till en CSV‑fil eller föra in dem i ett sökindex för snabb återvinning över flera ritningar.

## Vanliga fallgropar och felsökning
- **Saknad MTEXT:** Vissa äldre DWG‑versioner lagrar flerradig text i blockattribut. Se till att även inspektera `image.Blocks` för `Attribute`‑objekt.  
- **Kodningsproblem:** DWG‑filer kan använda icke‑Unicode kodtabeller. Ställ in `image.LoadOptions.Encoding` till rätt `System.Text.Encoding` innan du laddar.  
- **Stora filer:** För filer större än 200 MB, aktivera `image.LoadOptions.Streaming = true` för att hålla minnesanvändningen under 100 MB.

## Vanliga frågor

**Q: Kan jag söka efter text i lösenordsskyddade DWG‑filer?**  
A: Ja. Ange lösenordet via `CadLoadOptions.Password` när du anropar `Image.Load`.

**Q: Stöder API:et att söka i flera DWG‑filer samtidigt?**  
A: Absolut. Loop igenom en katalog, ladda varje fil och återanvänd samma LINQ‑filter – biblioteket är trådsäkert för parallell bearbetning.

**Q: Hur exakt är textutdragningen för komplexa annotationer?**  
A: Aspose.CAD rapporterar en **99 % framgångsfrekvens** på branschstandardtestset, hanterar MTEXT, attributdefinitioner och även inbäddade Unicode‑tecken.

**Q: Finns det ett sätt att markera hittad text i en visare?**  
A: Efter att ha erhållit `Location` för varje `TextFragment` kan du rita ett temporärt överlägg med någon CAD‑visare som accepterar geometriska primitiv.

**Q: Vilken licensmodell gäller för Aspose.CAD?**  
A: Produkten använder en per‑utvecklare eller per‑server licensmodell; en gratis utvärderingslicens finns tillgänglig i 30 dagar.

**Senast uppdaterad:** 2026-10-04  
**Testat med:** Aspose.CAD 24.11 for .NET  
**Författare:** Aspose  

## Textsökning och manipulationshandledningar
### [Söka text i DWG‑filer med C# – Aspose.CAD‑handledning](./searching-text-in-dwg-files/)

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

## Relaterade handledningar

- [Konvertera DWG till PDF och lägg till text i C# – Aspose.CAD‑handledning](/cad/net/dwg-file-manipulation/adding-text-to-dwg/)
- [Hur man konverterar DWG till PDF och rasterbilder med Aspose.CAD för .NET](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [Hur man renderar CAD och konverterar DWG – Aspose.CAD .NET](/cad/net/conversion-and-export/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}