---
date: 2026-07-18
description: Så exporterar du CAD till PNG med Aspose.CAD för .NET. Konvertera IFC-filer
  till högkvalitativa PNG-bilder snabbt och pålitligt.
keywords:
- how to export cad to png
- Aspose.CAD IFC conversion
- CAD to PNG .NET
lastmod: 2026-07-18
linktitle: Exportera IFC-filer till PNG
og_description: Så exporterar du CAD till PNG med Aspose.CAD för .NET. Lär dig steg-för-steg-konvertering
  av IFC-filer till PNG-bilder utan kod.
og_image_alt: Guide showing IFC to PNG conversion with Aspose.CAD for .NET
og_title: Så exporterar du CAD till PNG – Aspose.CAD .NET-guide
schemas:
- author: Aspose
  dateModified: '2026-07-18'
  description: How to export CAD to PNG using Aspose.CAD for .NET. Convert IFC files
    to high‑quality PNG images quickly and reliably.
  headline: How to Export CAD to PNG – Exporting IFC Files with Aspose.CAD
  type: TechArticle
- questions:
  - answer: No, Aspose.CAD for .NET is specifically designed for Windows environments.
    question: Can I use Aspose.CAD for .NET on macOS or Linux?
  - answer: Yes, you can obtain a temporary license from [here](https://purchase.aspose.com/temporary-license/)
      for evaluation.
    question: Is a temporary license available for testing purposes?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community
      support and discussions.
    question: How can I get support for Aspose.CAD?
  - answer: Refer to the [Aspose.CAD documentation](https://reference.aspose.com/cad/net/)
      for detailed information and examples.
    question: Where can I find comprehensive documentation?
  - answer: Check the documentation or seek assistance on the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19).
    question: What if I encounter issues during installation?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- export cad
- Aspose.CAD
- IFC to PNG
- .NET image conversion
title: Så exporterar du CAD till PNG – Exporterar IFC-filer med Aspose.CAD
url: /sv/net/exporting-to-image-formats/exporting-ifc-files-to-png/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hur man exporterar CAD till PNG – Exporterar IFC-filer med Aspose.CAD

## Introduktion

Om du behöver **how to export cad to png**, erbjuder Aspose.CAD för .NET ett pålitligt, kod‑fritt sätt att omvandla IFC (Industry Foundation Classes)-modeller till skarpa PNG‑rasterbilder. I den här handledningen går vi igenom hela arbetsflödet—från installation av biblioteket till sparande av den slutgiltiga PNG‑filen—så att du kan integrera konverteringen i vilken .NET‑applikation som helst med förtroende.

## Snabba svar
- **Vilket bibliotek hanterar konverteringen?** Aspose.CAD for .NET.
- **Stödd källformat?** IFC (Industry Foundation Classes)-filer.
- **Målbildformat?** PNG, med full kontroll över storlek och upplösning.
- **Minsta .NET-version?** .NET Framework 4.5+ eller .NET Core 3.1+.
- **Licenskrav?** En giltig Aspose.CAD-licens för produktionsanvändning.

## Vad är “how to export cad to png”?

Frasen avser processen att konvertera CAD‑baserade filformat, såsom IFC, till Portable Network Graphics (PNG)-rasterbilder. Denna konvertering möjliggör enkel visning, delning och inbäddning av CAD‑visualiseringar i webbsidor, dokumentation eller rapporter, och erbjuder ett lättviktigt, brett stödjande format som bevarar visuell kvalitet utan att kräva specialiserade CAD‑visare.

## Varför använda Aspose.CAD för denna konvertering?

Aspose.CAD stöder **50+ CAD- och BIM-format** och kan bearbeta flertalet hundra‑sidiga IFC-modeller utan att läsa in hela filen i minnet. Det levererar snabba, minnes‑effektiva konverteringar på standard serverhårdvara, hanterar automatiskt lager, linjebredder och färgkartläggning samtidigt som det erbjuder omfattande konfigurationsalternativ för utdata­kvalitet och storlek.

## Förutsättningar

### 1. Aspose.CAD-installation
Se till att du har Aspose.CAD för .NET installerat. Du kan ladda ner det från releasesidan [here](https://releases.aspose.com/cad/net/).

### 2. Dokumentkatalog
Skapa en avsedd katalog för dina dokument. I det medföljande exemplet representerar variabeln `MyDir` dokumentkatalogen.

## Importera namnrymder
Nu när förutsättningarna är klara, importera de namnrymder som krävs för att arbeta med Aspose.CAD i ditt .NET‑projekt.

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using Aspose.CAD.FileFormats.Ifc;
```

## Hur man exporterar CAD till PNG?

`IfcImage` representerar en IFC CAD‑bild som kan rasteriseras till rasterformat som PNG. Ladda din IFC‑fil med `new IfcImage("source.ifc")`, konfigurera rasterisering via `RasterizationOptions`, ställ in PNG‑specifika inställningar med `PngOptions` och anropa slutligen `Save(outputPath, pngOptions)`. Detta end‑to‑end‑flöde konverterar CAD‑modellen till en högupplöst PNG på bara några kodrader, och hanterar automatiskt lager, färger och linjebredder.

## Steg 1: Ladda IFC-fil
`IfcImage`‑klassen laddar en IFC‑modell och förbereder den för rasterisering.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "example.ifc";
using (IfcImage cadImage = (IfcImage)Image.Load(sourceFilePath))
{
```

I detta steg initierar vi Aspose.CAD `IfcImage`‑objektet och laddar IFC‑filen i det.

## Steg 2: Ställ in rasteriseringsalternativ
`RasterizationOptions`‑klassen definierar hur vektordata konverteras till rasterbilder, inklusive sidbredd, höjd och bakgrundsfärg.

```csharp
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
   
    rasterizationOptions.PageWidth = 100;
    rasterizationOptions.PageHeight = 100;
```

Definiera rasteriseringsalternativ för att konfigurera sidbredd och -höjd för PNG‑utdata.

## Steg 3: Ställ in PNG-alternativ
`PngOptions`‑klassen innehåller inställningar specifika för PNG‑utdata, såsom komprimeringsnivå och färgdjup.

```csharp
    PngOptions pngOptions = new PngOptions();
    pngOptions.VectorRasterizationOptions = rasterizationOptions;
```

Skapa PNG‑alternativ och associera de tidigare definierade rasteriseringsalternativen.

## Steg 4: Ange utdataväg
Utdatavägen bestämmer var den genererade PNG‑filen sparas.

```csharp
    // Set output path as well
    string outPath = sourceFilePath + ".png";
    cadImage.Save(outPath, pngOptions);
}
```

Definiera utdatavägen för PNG‑filen, så att den har samma namn som källfilen med ".png"-ändelsen. Slutligen sparas den konverterade bilden.

## Vanliga problem och lösningar
- **Saknade typsnitt eller linjestilar:** Se till att käll‑IFC refererar till alla nödvändiga resurser; Aspose.CAD bäddar in saknade resurser när det är möjligt.
- **Stora filer orsakar minnesökningar:** Använd egenskapen `MemoryLimit` på `RasterizationOptions` för att begränsa minnesanvändningen.
- **Felaktiga färger:** Verifiera att käll‑IFC‑färgdefinitionerna följer IFC‑schemat; Aspose.CAD respekterar den standardiserade färgkartläggningen.

## Vanliga frågor

**Q: Kan jag använda Aspose.CAD för .NET på macOS eller Linux?**  
A: Nej, Aspose.CAD för .NET är specifikt designat för Windows‑miljöer.

**Q: Finns en temporär licens tillgänglig för teständamål?**  
A: Ja, du kan få en temporär licens från [here](https://purchase.aspose.com/temporary-license/) för utvärdering.

**Q: Hur kan jag få support för Aspose.CAD?**  
A: Besök [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) för community‑support och diskussioner.

**Q: Var kan jag hitta omfattande dokumentation?**  
A: Se [Aspose.CAD documentation](https://reference.aspose.com/cad/net/) för detaljerad information och exempel.

**Q: Vad gör jag om jag stöter på problem under installationen?**  
A: Kontrollera dokumentationen eller sök hjälp på [Aspose.CAD forum](https://forum.aspose.com/c/cad/19).

---

**Last Updated:** 2026-07-18  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose

## Relaterade handledningar

- [Konvertera CAD-ritning till rasterbild i Aspose.CAD för .NET](/cad/net/cad-drawing-manipulation/convert-cad-drawing-to-raster-image/)
- [STL till PNG-konvertering gjort enkelt med Aspose.CAD för .NET](/cad/net/stl-file-export/exporting-stl-files-to-png/)
- [Exportera CAD‑layouter till rasterbildformat i Aspose.CAD för .NET](/cad/net/cad-export-formats/export-cad-layouts-to-raster-image-formats/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}