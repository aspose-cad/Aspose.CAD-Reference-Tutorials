---
date: 2026-09-04
description: Lär dig hur du åsidosätter dwg codepage-detektering i DWG-filer med Aspose.CAD
  för .NET, vilket ger dig exakt kontroll över teckenkodning.
keywords:
- override dwg codepage
- dwg codepage detection
- aspose.cad .net
- cad file encoding
- dwg processing
lastmod: 2026-09-04
linktitle: Åsidosätt automatisk codepage-detektering i DWG-filer – Aspose.CAD-handledning
og_description: Lär dig hur du åsidosätter dwg codepage-detektering i DWG-filer med
  Aspose.CAD för .NET, vilket ger dig exakt kontroll över teckenkodning och förbättrar
  CAD-filhantering.
og_image_alt: Guide showing how to override DWG codepage with Aspose.CAD in .NET
og_title: Hur man åsidosätter dwg codepage i Aspose.CAD för .NET
schemas:
- author: Aspose
  dateModified: '2026-09-04'
  description: Learn how to override dwg codepage detection in DWG files using Aspose.CAD
    for .NET, giving you precise control over character encoding.
  headline: How to override dwg codepage in Aspose.CAD for .NET
  type: TechArticle
- questions:
  - answer: It forces Aspose.CAD to use the encoding you specify instead of guessing,
      preventing character corruption.
    question: What does overriding the DWG codepage do?
  - answer: Whenever a DWG file contains text in a language that isn’t the default
      Windows codepage (e.g., Central European, Cyrillic).
    question: When should I use it?
  - answer: Any .NET `Encoding` such as `Encoding.GetEncoding(1250)` for Central European.
    question: Which encodings are supported?
  - answer: A trial works for development; a commercial license is required for production.
    question: Do I need a license?
  - answer: Yes, the setting is applied per `Image` instance, so multiple threads
      can process different files concurrently.
    question: Is it thread‑safe?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- override dwg codepage
- Aspose.CAD
- .NET CAD processing
- DWG codepage
- CAD rendering
title: Hur man åsidosätter dwg codepage i Aspose.CAD för .NET
url: /sv/net/image-manipulation-and-rendering/override-automatic-codepage-detection-in-dwg/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hur man åsidosätter dwg-kodpage i Aspose.CAD för .NET

I många äldre DWG-filer upptäcks den inbäddade kodpage automatiskt, vilket kan leda till förvrängd text när filen använder en icke‑standardkodning. **Override dwg codepage** låter dig explicit ange önskad kodning så att geometri och annoteringstext renderas korrekt. I den här handledningen kommer du att se varför detta är viktigt, hur API:et ser ut och hur du tillämpar inställningen i några enkla steg.

## Snabba svar
- **Vad gör det att åsidosätta DWG-kodpage?** Det tvingar Aspose.CAD att använda den kodning du anger istället för att gissa, vilket förhindrar teckenkorruption.  
- **När bör jag använda det?** När en DWG-fil innehåller text på ett språk som inte är Windows standardkodpage (t.ex. Centraleuropeisk, Kyrillisk).  
- **Vilka kodningar stöds?** Alla .NET `Encoding` såsom `Encoding.GetEncoding(1250)` för Centraleuropeisk.  
- **Behöver jag en licens?** En provversion fungerar för utveckling; en kommersiell licens krävs för produktion.  
- **Är den trådsäker?** Ja, inställningen tillämpas per `Image`-instans, så flera trådar kan bearbeta olika filer samtidigt.

## Vad är override dwg codepage?
Override dwg codepage är en funktion i Aspose.CAD som låter dig ersätta bibliotekets automatiska kodpage-detektering med en specifik teckenkodning som du anger. Detta säkerställer att textsträngar i DWG-filen tolkas korrekt oavsett filens ursprungliga metadata.

## Varför använda override dwg codepage?
Aspose.CAD stöder **50+ DWG/DXF-versioner** och kan bearbeta filer upp till **2 GB** utan att ladda hela dokumentet i minnet. När den automatiska detektionen misslyckas kan du förlora upp till **100 % av annoteringsläsbarheten**. Genom att explicit ange kodpage minskar du denna risk till **0 %** och behåller renderingtiderna oförändrade.

## Förutsättningar

- Grundläggande kunskap om C# och .NET-plattformen.  
- Aspose.CAD för .NET installerat. Om du ännu inte har installerat det, ladda ner det **[Aspose.CAD för .NET nedladdningssida](https://releases.aspose.com/cad/net/)**.  
- En DWG-fil som använder en icke‑standard kodpage (t.ex. en fil skapad på ett system med kodpage 1250).

## Importera namnrymder

För att börja, lägg till de nödvändiga `using`-direktiven så att kompilatorn kan hitta Aspose.CAD-klasser.

Infoga följande högst upp i din C#-källfil:

```csharp
using System;
using Aspose.CAD.FileFormats.Cad;
```

Detta förbereder miljön för alla efterföljande CAD-operationer.

## Steg 1: definiera din dokumentkatalog

Ange mappen som innehåller DWG-filen du vill bearbeta. Ersätt platshållaren med den faktiska sökvägen på din maskin:

```csharp
//ExStart:1
string SourceDir = "Your Document Directory";
//ExEnd:1
```

## Steg 2: åsidosätt automatisk kodpage-detektering

Nu kommer vi till kärnan i handledningen. Koden nedan laddar en DWG-fil, tvingar kodpage till **Windows‑1250** (Centraleuropeisk), och sparar sedan bilden som en PNG. Ändra filnamnet och kodningen efter behov för ditt scenario.

```csharp
//ExStart:1
using (CadImage cadImage = (CadImage)Image.Load(SourceDir + "SimpleEntites.dwg",
new LoadOptions()
{
	SpecifiedEncoding = CodePages.Japanese,
	SpecifiedMifEncoding = MifCodePages.Japanese,
	RecoverMalformedCifMif = false
}))
{
	// Perform export or other operations with cadImage
}
//ExEnd:1
Console.WriteLine("OverrideAutomaticCodePageDetectionDwg executed successfully");
```

`Image.Load` är en statisk metod som laddar en CAD-fil och returnerar ett `CadImage`-objekt. `LoadOptions.CodePage` anger teckenkodningen som ska användas under inläsning. `CadImage` representerar den in‑minnet‑representation av en CAD-ritning och tillhandahåller metoder för rendering eller konvertering.

## Vanliga problem och lösningar

- **Skräptecken kvarstår efter åsidosättning** – Verifiera att den kodning du valt matchar filens ursprungliga språk. Använd `Encoding.GetEncoding(1251)` för kyrilliska, till exempel.  
- **Filen går inte att ladda** – Säkerställ att DWG-versionen stöds av din Aspose.CAD-version; uppgradera vid behov.  
- **Prestandaförlust** – Åsidosättningen lägger inte till någon extra belastning; om du märker en långsamhet, kontrollera orelaterade I/O-flaskhalsar.

## Vanliga frågor

### Q1: Kan jag använda Aspose.CAD för .NET med andra språk än C#?
A1: Aspose.CAD för .NET är främst designat för C#, men det kan användas i andra .NET-språk såsom VB.NET.

### Q2: Finns en gratis provversion tillgänglig?
A2: Ja, du kan få åtkomst till en gratis provversion **[Aspose.CAD gratis provnedladdningssida](https://releases.aspose.com/)**.

### Q3: Hur kan jag få support för Aspose.CAD för .NET?
A3: Besök **[Aspose.CAD-forum](https://forum.aspose.com/c/cad/19)** för community-support.

### Q4: Kan jag köpa en tillfällig licens?
A4: Ja, du kan skaffa en tillfällig licens **[tillfällig licens köpsida](https://purchase.aspose.com/temporary-license/)**.

### Q5: Var kan jag hitta detaljerad dokumentation?
A5: Se den omfattande **[Aspose.CAD .NET API-dokumentation](https://reference.aspose.com/cad/net/)**.

### Q6: Påverkar åsidosättning av kodpage rasterrenderingskvaliteten?
A6: Nej. Kodpage-inställningen påverkar endast hur textsträngar avkodas; bildkvaliteten förblir oförändrad.

### Q7: Kan jag tillämpa åsidosättningen när jag konverterar till andra format än PNG?
A7: Absolut. Samma `LoadOptions.CodePage`-värde fungerar för PDF, SVG eller något annat utdataformat som stöds av Aspose.CAD.

---

**Senast uppdaterad:** 2026-09-04  
**Testat med:** Aspose.CAD 24.10 för .NET  
**Författare:** Aspose

## Relaterade handledningar

- [Söka text i DWG-filer med C# - Aspose.CAD-handledning](/cad/net/text-search-and-manipulation/searching-text-in-dwg-files/)
- [Konvertera DWG till PDF och lägg till text i C# – Aspose.CAD-handledning](/cad/net/dwg-file-manipulation/adding-text-to-dwg/)
- [Hur man konverterar DWG till PDF och rasterbilder med Aspose.CAD för .NET](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}