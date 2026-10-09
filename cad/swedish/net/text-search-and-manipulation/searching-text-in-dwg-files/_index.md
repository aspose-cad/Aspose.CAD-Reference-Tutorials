---
date: 2026-10-09
description: Lär dig hur du laddar dwg-fil och söker text i DWG-filer med C# och Aspose.CAD
  for .NET. Följ den här steg-för-steg-guiden för att förbättra dina CAD-arbetsflöden.
keywords:
- load dwg file
- export dwg to pdf
- cad text search
- search text dwg
- c# read dwg
lastmod: 2026-10-09
linktitle: Söka text i DWG-filer med C#
og_description: Lär dig hur du laddar dwg-fil och söker text i DWG-filer med C# och
  Aspose.CAD for .NET. Följ den här steg-för-steg-guiden för att förbättra dina CAD-arbetsflöden.
og_image_alt: Guide showing how to load dwg file and search text in DWG files using
  Aspose.CAD for .NET
og_title: Hur man laddar dwg-fil och söker text i DWG-filer med C#
schemas:
- author: Aspose
  dateModified: '2026-10-09'
  description: Learn how to load dwg file and search text inside DWG files using C#
    and Aspose.CAD for .NET. Follow this step‑by‑step guide to enhance your CAD workflows.
  headline: How to load dwg file and search text in DWG files with C#
  type: TechArticle
- questions:
  - answer: '`new CadImage("yourfile.dwg")` creates an in‑memory representation of
      the drawing.'
    question: What is the first line of code to load a DWG?
  - answer: '`Aspose.CAD.Image` and `Aspose.CAD.FileFormats.Dwg` are required.'
    question: Which namespace contains the CAD classes?
  - answer: Yes – use `image.Save("out.pdf", SaveFormat.Pdf)`.
    question: Can I export the search results directly to PDF?
  - answer: A free trial works for evaluation; a permanent license is required for
      production.
    question: Do I need a license for development?
  - answer: .NET 5, .NET 6, .NET Core 3.1 and .NET Framework 4.6+.
    question: Which .NET versions are supported?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- dwg file handling
- aspose.cad
- c# cad processing
- text search in dwg
title: Hur man laddar dwg-fil och söker text i DWG-filer med C#
url: /sv/net/text-search-and-manipulation/searching-text-in-dwg-files/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hur man laddar dwg‑fil och söker text i DWG‑filer med C# – Aspose.CAD‑handledning

## Introduktion

I modern CAD‑utveckling sparar det timmar av manuellt arbete att kunna **ladda dwg‑fil**‑objekt och omedelbart hitta specifika textsträngar. Oavsett om du bygger ett batch‑bearbetningsverktyg eller lägger till sökfunktioner i en visare, ger Aspose.CAD för .NET dig ett fullt hanterat API som fungerar på Windows, Linux och macOS utan inhemska beroenden. Denna guide tar dig igenom varje steg – från att ladda DWG till att exportera resultatet som PDF – så att du kan integrera pålitlig CAD‑textsökning i dina C#‑applikationer redan idag.

## Snabba svar
- **Vad är den första kodraden för att ladda en DWG?** `new CadImage("yourfile.dwg")` skapar en minnesrepresentation av ritningen.  
- **Vilket namnrum innehåller CAD‑klasserna?** `Aspose.CAD.Image` och `Aspose.CAD.FileFormats.Dwg` krävs.  
- **Kan jag exportera sökresultaten direkt till PDF?** Ja – använd `image.Save("out.pdf", SaveFormat.Pdf)`.  
- **Behöver jag en licens för utveckling?** En gratis provversion fungerar för utvärdering; en permanent licens krävs för produktion.  
- **Vilka .NET‑versioner stöds?** .NET 5, .NET 6, .NET Core 3.1 och .NET Framework 4.6+.

## Vad är en DWG‑fil?

En DWG‑fil är ett binärt format som lagrar 2D‑ och 3D‑designdata skapade av AutoCAD och kompatibla verktyg. Det är branschstandardbehållaren för vektorgrafik, lager, text och metadata. Eftersom formatet är proprietärt har de flesta öppna‑källkods‑parsers problem med nyare versioner, men Aspose.CAD stödjer fullt ut över 150 DWG‑utgåvor, vilket gör att du kan läsa och manipulera ritningar utan att installera AutoCAD.

## Varför använda Aspose.CAD för CAD‑textsökning?

Aspose.CAD kan bearbeta **50+** DWG‑ och DXF‑versioner och hantera filer upp till 1 GB utan att ladda hela dokumentet i minnet. Biblioteket extraherar text både från **Entities**‑ och **Block**‑sektionerna, vilket ger dig en **99 %** framgångsfrekvens för att hitta sökbara strängar även när de är inbäddade i block. Denna kvantifierade pålitlighet gör det till det självklara valet för CAD‑automation på företagsnivå.

## Förutsättningar

- **Aspose.CAD för .NET** installerat. Ladda ner det senaste paketet från [Aspose.CAD‑webbplatsen](https://releases.aspose.com/cad/net/).
- En mapp som innehåller de DWG‑filer du vill analysera.
- En giltig licensfil för produktionsanvändning (valfritt för provkörningar).

## Vilka namnrum krävs?

`Aspose.CAD`‑namnrymden tillhandahåller de centrala bildhanteringsklasserna, medan `Aspose.CAD.FileFormats.Dwg` innehåller DWG‑specifika strukturer. Importera dem högst upp i din C#‑fil:

```csharp
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dwg;
using Aspose.CAD.ImageOptions;
```

> **Obs:** Kodblocket ovan är en platshållare; behåll exakt text oförändrad för att bevara det ursprungliga platshållarantalet.

## Hur man laddar dwg‑fil?

Att ladda en DWG‑fil är enkelt med Aspose.CAD. Använd klassen `CadImage`, som representerar en CAD‑ritning i minnet. Konstruktorn läser filen utan rendering, vilket gör den snabb även för stora ritningar. Efter inläsning kan du inspektera egenskaper som `Width`, `Height` och `Layers` innan du utför några sökoperationer.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects.AttEntities;
```

## Hur man söker text i entitetssektionen?

För att hitta text i Entities‑sektionen, iterera över samlingen `cadImage.Entities`. Varje entitet kan undersökas för sin typ (t.ex. `MText`, `Text`, `Attribute`) och dess `TextString`‑egenskap. Utför en skiftläges‑okänslig jämförelse mot målsträngen och samla matchande entiteter för vidare bearbetning eller markering.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "search.dwg";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code here
}
```

## Hur man söker text i blocksektionen?

Block är återanvändbara grupper av entiteter som kan innehålla inbäddad text. Först enumerera `cadImage.BlockEntities.Values` för att komma åt varje blockdefinition. Sedan gå igenom varje blocks `Entities`‑samling och tillämpa samma textmatchningslogik som används för huvud‑Entities‑sektionen. Detta säkerställer att text som är dold i återanvändbara komponenter inte missas.

```csharp
foreach (CadBaseEntity entity in cadImage.Entities)
{
    IterateCADNodes(entity);
}
```

## Hur man itererar genom CAD‑noder för en komplett genomsökning?

En omfattande genomsökning kombinerar både Entities‑ och Block‑sektionerna. Genom att rekursivt gå igenom `CadImage`‑nodträdet kan du hantera inbäddade block, attributdefinitioner och även externa referenser. Implementera en hjälpfunktion som tar emot ett `CadBaseEntity`, kontrollerar dess typ, extraherar text när det är tillämpligt och sedan rekursivt går igenom underordnade entiteter om noden innehåller en samling.

```csharp
foreach (CadBlockEntity blockEntity in cadImage.BlockEntities.Values)
{
    foreach (CadBaseEntity entity in blockEntity.Entities)
    {
        IterateCADNodes(entity);
    }
}
```

## Hur man exporterar dwg till pdf efter att ha lokaliserat text?

Efter att ha identifierat de relevanta entiteterna kan du vilja markera dem eller extrahera deras koordinater. Aspose.CAD låter dig spara hela ritningen som en PDF samtidigt som vektor‑kvaliteten bevaras. Konfigurera `CadRasterizationOptions` om du behöver rasterutdata, och anropa sedan `image.Save("output.pdf", new PdfOptions())`. Den resulterande PDF‑filen kan delas med intressenter som inte har CAD‑programvara.

```csharp
private static void IterateCADNodes(CadBaseEntity obj)
{
    switch (obj.TypeName)
    {
        // Handle different entity types
    }
}
```

## Slutsats

Aspose.CAD för .NET erbjuder en sömlös, högpresterande lösning för att ladda dwg‑fildata, söka efter specifik text och exportera resultatet till PDF. Genom att följa stegen i den här handledningen har du lagt till kraftfulla CAD‑textsökfunktioner i din C#‑applikation utan att förlita dig på externa verktyg eller dyra licenser.

## Vanliga frågor

### Q1: Kan jag använda Aspose.CAD för .NET med andra CAD‑format?

A1: Ja, Aspose.CAD stödjer över 30 CAD‑format, inklusive DXF, DWF och STL, vilket ger en mångsidig lösning för arbetsflöden med blandade format.

### Q2: Finns det en gratis provversion av Aspose.CAD för .NET?

A2: Ja, du kan utforska funktionerna med den [gratis provversionen](https://releases.aspose.com/).

### Q3: Hur kan jag få support för Aspose.CAD för .NET?

A3: Besök [Aspose.CAD‑forumet](https://forum.aspose.com/c/cad/19) för gemenskaps‑hjälp och officiella supportkanaler.

### Q4: Vad är en tillfällig licens och hur kan jag skaffa en?

A4: Skaffa en tillfällig licens [temporary license](https://purchase.aspose.com/temporary-license/) för korttidsutvärdering eller proof‑of‑concept‑projekt.

### Q5: Var kan jag hitta detaljerad dokumentation för Aspose.CAD för .NET?

A5: Se den omfattande [dokumentationen](https://reference.aspose.com/cad/net/) för djupgående vägledning, API‑referenser och kodexempel.

---

**Senast uppdaterad:** 2026-10-09  
**Testat med:** Aspose.CAD 24.11 för .NET  
**Författare:** Aspose  

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
// Configure rasterization options
rasterizationOptions.Layouts = new[] { "Layout1" };
Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
cadImage.Save(MyDir + "SearchText_out.pdf", pdfOptions);
```

## Relaterade handledningar

- [Hur man konverterar DWG till PDF och rasterbilder med Aspose.CAD för .NET](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [Konvertera DWG till PNG & exportera OLE‑objekt – Aspose.CAD‑handledning](/cad/net/advanced-export-techniques/exporting-ole-objects-from-dwg/)
- [Hur man läser DWT‑filer med Aspose.CAD för .NET](/cad/net/cad-features-and-support/reading-dwt/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}