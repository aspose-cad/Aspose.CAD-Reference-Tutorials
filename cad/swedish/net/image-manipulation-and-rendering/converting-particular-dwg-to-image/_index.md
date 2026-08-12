---
date: 2026-08-12
description: Extrahera text från DWG och konvertera specifik DWG till bild i C# med
  Aspose.CAD för .NET. Lär dig steg‑för‑steg med kodexempel.
keywords:
- extract text from dwg
- convert specific dwg to image
- Aspose.CAD .NET
lastmod: 2026-08-12
linktitle: Konvertera specifik DWG till bild i C#
og_description: Extrahera text från DWG och konvertera specifik DWG till bild i C#
  med Aspose.CAD. Följ denna koncisa guide för snabb implementering.
og_image_alt: Guide showing DWG to image conversion and text extraction using Aspose.CAD
  in C#
og_title: Extrahera text från DWG och konvertera specifik DWG till bild i C#
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
title: Extrahera text från DWG och konvertera specifik DWG till bild i C#
url: /sv/net/image-manipulation-and-rendering/converting-particular-dwg-to-image/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konvertera specifik DWG till bild i C# - Aspose.CAD guide

## Introduktion

I moderna ingenjörsapplikationer behöver du ofta **extrahera text från DWG**‑filer och **konvertera specifik DWG till bild**‑format för rapportering eller visualisering. Aspose.CAD för .NET ger dig ett fullständigt API som hanterar båda uppgifterna utan att kräva någon extern CAD‑programvara. I den här handledningen kommer du att lära dig hur du laddar en DWG, filtrerar efter textelement, rasteriserar ritningen och slutligen sparar resultatet som en PDF‑bild – allt i ren C#‑kod.

## Snabba svar
- **Vad är första steget?** Ladda DWG-filen med `new CadImage("file.dwg")`.  
- **Vilken klass filtrerar text?** Använd `CadEntityFilter` för att välja `Text`‑entiteter.  
- **Hur definierar du bildstorlek?** Sätt `Width` och `Height` på `CadRasterizationOptions`.  
- **Vilket utdataformat används?** Exemplet sparar till PDF, som bäddar in rasterbilden.  
- **Behöver jag en licens för produktion?** Ja – en kommersiell Aspose.CAD‑licens tar bort utvärderingsbegränsningarna.

## Hur extraherar man text från dwg?

Läs in DWG‑filen, tillämpa ett filter som endast väljer textelement och läs sedan egenskapen `TextString` för varje entitet. Detta tillvägagångssätt returnerar varje annotering, etikett eller dimensions­text som finns i ritningen, så att du kan återanvända den för sökning, indexering eller rapportering.

## Varför konvertera specifik dwg till bild?

Att konvertera en DWG till en rasterbild gör att du kan bädda in ritningen i dokument, webbsidor eller mobila appar som inte kan rendera inbyggda CAD‑format. Aspose.CAD bearbetar **över 50+ CAD‑format** och kan rasterisera ritningar med hundratals sidor samtidigt som den använder mindre än 200 MB minne, vilket gör den lämplig för hög‑genomströmning på servermiljöer.

## Förutsättningar

- Visual Studio (valfri nyare version) för att kompilera och köra C#‑projekt.  
- Aspose.CAD for .NET – se till att du har biblioteket installerat. Du kan hitta nedladdningslänken på den **[Aspose.CAD för .NET nedladdningssidan](https://releases.aspose.com/cad/net/)**.  
- En DWG‑fil du vill arbeta med; exempelfilen *visualization_-_conference_room.dwg* används i kodsnuttarna.

## Importera namnrymder

Följande namnrymder ger dig åtkomst till de centrala CAD‑klasserna, rasteriseringsalternativen och PDF‑utdatahjälpmedlen:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Steg 1: ladda dwg-filen

Skapa en `CadImage`‑instans genom att ange sökvägen till din DWG‑fil. `CadImage`‑objektet representerar hela ritningen i minnet och ger åtkomst till dess lager, entiteter och metadata.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
var cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath);
```

## Steg 2: filtrera entiteter

`CadEntityFilter` låter dig plocka ut endast de entiteter du behöver. I den här guiden konfigurerar vi den för att behålla **text**‑objekt och filtrera bort linjer, cirklar och annan geometri som du inte vill ha i den slutliga bilden.

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

## Steg 3: ange rasteriseringsalternativ

`CadRasterizationOptions` styr hur ritningen omvandlas till en bitmap. Du kan definiera utdata­storlek, bakgrundsfärg och upplösning (DPI). Följande definition introducerar klassen:

`CadRasterizationOptions`‑klassen specificerar bilddimensioner, upplösning och renderingsinställningar för konvertering av CAD‑ritningar till rasterformat.  

Ställ in önskad bredd, höjd och bakgrundsfärg innan du vidarebefordrar alternativen till PDF‑exportören.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions =
    new Aspose.CAD.ImageOptions.CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
```

## Steg 4: ange PDF‑alternativ

`PdfOptions` samlar rasteriseringsinställningarna med PDF‑specifika funktioner såsom komprimering. Definitionen av denna klass visas först:

`PdfOptions` kapslar in parametrar för PDF‑generering, inklusive rasteriseringsalternativen som bestämmer hur CAD‑data renderas i PDF‑dokumentet.  

Tilldela den tidigare skapade `CadRasterizationOptions`‑instansen till egenskapen `VectorRasterizationOptions`.

```csharp
Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Steg 5: spara som PDF

Slutligen anropar du `Save`‑metoden på `CadImage`‑objektet, anger målfilens namn och de konfigurerade `PdfOptions`. PDF‑filen kommer att innehålla en högkvalitativ bild av den filtrerade ritningen.

```csharp
string outFile = MyDir + "result_out_generated.pdf";
cadImage.Save(outFile, pdfOptions);
```

## Vanliga problem och felsökning

- **Saknad text efter filtrering** – Säkerställ att DWG‑filen faktiskt innehåller `Text`‑entiteter; vissa ritningar lagrar annotationer som `MText`. Justera filtret för att inkludera `MText` om det behövs.  
- **Tom utdata bild** – Verifiera att rasteriserings‑DPI är tillräckligt hög (300 DPI är ett säkert standardvärde) och att bakgrundsfärgen inte är inställd på transparent när PDF‑filen visas.  
- **Minnesbristfel på stora filer** – Använd `LoadOptions`‑överladdningen som möjliggör strömning, vilket förhindrar att hela filen laddas in i minnet på en gång.

## Vanliga frågor

**Q: Är Aspose.CAD kompatibel med alla versioner av DWG‑filer?**  
A: Aspose.CAD stödjer DWG‑utgåvor från AutoCAD 2000 upp till den senaste 2024‑versionen, vilket täcker över 90 % av filerna som skapas i fältet.

**Q: Kan jag anpassa rasteriseringsalternativen för olika utdata?**  
A: Ja – du kan ändra upplösning, bildformat, anti‑aliasing och bakgrundsfärg för att passa PNG, JPEG eller PDF‑mål.

**Q: Var kan jag hitta ytterligare exempel och dokumentation?**  
A: Utforska den omfattande [Aspose.CAD‑dokumentationen](https://reference.aspose.com/cad/net/) för fler kodexempel och API‑detaljer.

**Q: Finns det en gratis provversion av Aspose.CAD?**  
A: Absolut – du kan ladda ner en provversion på **[Aspose provnedladdningssida](https://releases.aspose.com/)** och utvärdera alla funktioner utan begränsningar i 30 dagar.

**Q: Hur får jag support eller kontakt med communityn?**  
A: Gå med i det aktiva [Aspose.CAD‑forumet](https://forum.aspose.com/c/cad/19) där utvecklare delar lösningar och Aspose‑teamet svarar på frågor.

---

**Senast uppdaterad:** 2026-08-12  
**Testad med:** Aspose.CAD 24.11 for .NET  
**Författare:** Aspose

## Relaterade handledningar

- [Söka text i DWG-filer med C# - Aspose.CAD-handledning](/cad/net/text-search-and-manipulation/searching-text-in-dwg-files/)
- [Konvertera CAD-ritning till rasterbild i Aspose.CAD för .NET](/cad/net/cad-drawing-manipulation/convert-cad-drawing-to-raster-image/)
- [Rendera DWG-dokument i C# - Aspose.CAD-guide](/cad/net/image-manipulation-and-rendering/rendering-dwg-documents/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}