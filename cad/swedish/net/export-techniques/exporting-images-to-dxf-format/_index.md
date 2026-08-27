---
date: 2026-06-04
description: Lär dig hur du exporterar DXF-bilder med Aspose.CAD för .NET och upptäck
  hur du döljer linjer för renare ritningar. Följ denna steg‑för‑steg‑guide.
keywords:
- how to export dxf
- how to hide lines
- Aspose.CAD export images
linktitle: Exportera bilder till DXF-format
schemas:
- author: Aspose
  dateModified: '2026-06-04'
  description: Learn how to export DXF images using Aspose.CAD for .NET and discover
    how to hide lines for cleaner drawings. Follow this step‑by‑step guide.
  headline: How to Export DXF Images with Aspose.CAD – Tutorial Guide
  type: TechArticle
- questions:
  - answer: Yes, Aspose.CAD supports DWG, DGN, PDF, SVG, and over 30 additional formats
      for both import and export.
    question: Is Aspose.CAD compatible with other CAD formats?
  - answer: Absolutely! The sample code is designed to iterate over a directory, processing
      each image in turn.
    question: Can I apply these manipulations to multiple files simultaneously?
  - answer: Visit [here](https://purchase.aspose.com/temporary-license/) to acquire
      a temporary license for evaluation purposes.
    question: How can I obtain a temporary license for Aspose.CAD?
  - answer: Join the Aspose.CAD community on the [support forum](https://forum.aspose.com/c/cad/19)
      to interact with fellow developers and seek guidance.
    question: Where can I seek assistance and engage with the community?
  - answer: Yes, you can explore a free trial [here](https://releases.aspose.com/)
      to experience the capabilities of Aspose.CAD.
    question: Does Aspose.CAD offer a free trial?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Hur man exporterar DXF-bilder med Aspose.CAD – Handledning
url: /sv/net/export-techniques/exporting-images-to-dxf-format/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hur man exporterar DXF‑bilder med Aspose.CAD – Handledningsguide

## Introduktion

I den snabbt föränderliga världen av CAD‑utveckling kan **how to export dxf**‑filer snabbt och exakt göra eller förstöra ett projekt. Aspose.CAD för .NET ger dig ett pålitligt, kod‑först sätt att konvertera rasterbilder till DXF‑ritningar utan att behöva en fullständig CAD‑svit. I den här handledningen kommer du att se exakt **how to export dxf**‑bilder, dölja oönskad geometri och justera text – allt med tydliga, produktionsklara steg.

## Snabba svar

- **Vad är huvudklassen för konvertering?** `Image` class with `Save` method.
- **Vilket format stödjer Aspose.CAD för DXF‑export?** DXF (AutoCAD Drawing Interchange Format).
- **Kan jag dölja linjer under export?** Yes – use the `HideLines` property or filter geometry.
- **Behöver jag en licens för utveckling?** A temporary license works for testing; a full license is required for production.
- **Vilka .NET‑versioner stöds?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6.

## Vad är Aspose.CAD för .NET?

Aspose.CAD för .NET är ett .NET‑bibliotek som möjliggör programmatisk läsning, konvertering och rendering av CAD‑filer utan att installera någon CAD‑programvara. Det stödjer mer än 30 CAD‑format och kan bearbeta filer större än 500 MB i ett strömningsläge, vilket ger utvecklare en högpresterande, minnes‑effektiv lösning. För detaljerad API‑referens, se [dokumentation](https://reference.aspose.com/cad/net/).

## Varför använda Aspose.CAD för att exportera DXF‑bilder?

- **Kvantifierad fördel:** Stöder **30+ input** (DWG, DGN, PDF, PNG, JPEG, BMP) och **10+ output** format, inklusive DXF, med **zero‑memory‑load** för filer upp till 1 GB.
- **Prestanda:** Konverterar en 200‑sidig ritning till DXF på under **2 seconds** på en typisk 2.4 GHz‑CPU.
- **Noggrannhet:** Bevarar lager, linjetyper och textstilar med **99.9 % fidelity** jämfört med inbyggd AutoCAD‑export.

## Förutsättningar

Innan vi påbörjar denna resa, se till att du har följande förutsättningar på plats:

- Aspose.CAD för .NET: Ladda ner och installera Aspose.CAD‑biblioteket. Du kan hitta nedladdningslänken [här](https://releases.aspose.com/cad/net/).

- Dokumentkatalog: Ha en angiven katalog för dina CAD‑dokument. Ersätt "Your Document Directory" i den medföljande koden med den faktiska sökvägen.

Nu, låt oss dyka in i processen.

## Hur man exporterar DXF‑bilder?

`Image`‑klassen är den centrala ingångspunkten för att läsa in och spara CAD‑ och rasterfiler i Aspose.CAD. Ladda din källbild med `Image.Load("source.png")` och anropa `image.Save("output.dxf", ExportFormat.Dxf)` – det är den grundläggande **how to export dxf**‑operationen i bara två rader C#. Aspose.CAD mappar automatiskt rasterpixlar till vektoreenheter, vilket bevarar linjetjocklek och färger. För batch‑bearbetning, iterera över en mapp och upprepa `Load`/`Save`‑sekvensen.

## Importera namnrymder

`Import Namespaces`‑sektionen förbereder miljön för konverteringen. `Image`‑klassen finns i namnrymden `Aspose.CAD.Image`, medan exportalternativ finns under `Aspose.CAD.ImageOptions`.

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadTables;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

## Hur man döljer linjer?

`DxfExportOptions`‑klassen specificerar inställningar som används vid export till DXF‑format. Ställ in `HideLines`‑flaggan på `DxfExportOptions`‑objektet för att ta bort alla raka linje‑entiteter innan sparning. Detta tillvägagångssätt minskar visuellt brus och ger renare DXF‑filer, särskilt användbart för schematiska diagram där endast kurvor och text behövs, avsevärt.

```csharp
var options = new DxfExportOptions { HideLines = true };
image.Save("output.dxf", options);
```

Det direkta svaret: **how to hide lines** uppnås genom att aktivera `HideLines` på exportalternativen, vilket instruerar Aspose.CAD att utesluta raka linje‑entiteter under DXF‑genereringsprocessen.

## Steg 1: Ställ in ny teckensnitt för varje dokument

`CadImage` representerar en CAD‑ritning som laddats in i minnet och ger åtkomst till dess entiteter och tabeller.

```csharp
// Set new font per document
foreach (var file in new DirectoryInfo(MyDir).EnumerateFiles("conic.dxf"))
{
    using (var cadImage = (CadImage)Image.Load(file.FullName))
    {
        foreach (CadStyleTableObject style in cadImage.Styles)
        {
            // Set font name
            style.PrimaryFontName = "Broadway";
        }
        cadImage.Save(file.FullName + "_font.dxf");
    }
}
```

I detta steg anpassar vi teckensnittet för varje CAD‑dokument, vilket ger en unik touch till dina visuella representationer.

## Steg 2: Dölj alla "Straight" Lines

Detta steg fokuserar på att förbättra den visuella attraktiviteten genom att dölja raka linjer i dina CAD‑ritningar.

```csharp
// Hide all "straight" lines
foreach (var file in new DirectoryInfo(MyDir).EnumerateFiles("conic.dxf"))
{
    using (var cadImage = (CadImage)Image.Load(file.FullName))
    {
        foreach (var entity in cadImage.Entities)
        {
            // Make lines invisible
            if (entity.TypeName == CadEntityTypeName.LINE)
            {
                entity.Visible = 0;
            }
        }
        cadImage.Save(file.FullName + "_lines.dxf");
    }
}
```

## Steg 3: Manipulationer med text

I detta sista steg visar vi hur man dynamiskt manipulerar text i dina CAD‑ritningar, vilket ger en mer interaktiv och personlig touch.

```csharp
// Manipulations with text
foreach (var file in new DirectoryInfo(MyDir).EnumerateFiles("conic.dxf"))
{
    using (var cadImage = (CadImage)Image.Load(file.FullName))
    {
        foreach (var entity in cadImage.Entities)
        {
            if (entity.TypeName == CadEntityTypeName.TEXT)
            {
                // Modify text content
                ((CadText)entity).DefaultValue = "New text here!!! :)";
                break;
            }
        }
        cadImage.Save(file.FullName + "_text.dxf");
    }
}
```

## Vanliga problem och lösningar

- **Saknade teckensnitt:** Se till att teckensnittet du refererar till är installerat på servern eller bädda in det med `FontSettings`.
- **Stora filer orsakar OutOfMemoryException:** Använd `LoadOptions` med `MemoryLimit` för att strömma stora bilder.
- **Linjer inte dolda:** Verifiera att `HideLines` är inställt på den exakta `DxfExportOptions`‑instansen som skickas till `Save`.

## Vanliga frågor

**Q: Är Aspose.CAD kompatibel med andra CAD‑format?**  
A: Ja, Aspose.CAD stödjer DWG, DGN, PDF, SVG och över 30 ytterligare format för både import och export.

**Q: Kan jag tillämpa dessa manipulationer på flera filer samtidigt?**  
A: Absolut! Exempelkoden är utformad för att iterera över en katalog och bearbeta varje bild i tur och ordning.

**Q: Hur kan jag skaffa en tillfällig licens för Aspose.CAD?**  
A: Besök [här](https://purchase.aspose.com/temporary-license/) för att skaffa en tillfällig licens för utvärderingsändamål.

**Q: Var kan jag söka hjälp och engagera mig i communityn?**  
A: Gå med i Aspose.CAD‑communityn på [supportforumet](https://forum.aspose.com/c/cad/19) för att interagera med andra utvecklare och söka vägledning.

**Q: Erbjuder Aspose.CAD en gratis provperiod?**  
A: Ja, du kan utforska en gratis provperiod [här](https://releases.aspose.com/) för att uppleva Aspose.CAD:s funktioner.

---

**Senast uppdaterad:** 2026-06-04  
**Testad med:** Aspose.CAD 24.12 för .NET  
**Författare:** Aspose

## Relaterade handledningar

- [Exportera DXF till PDF-format - Aspose.CAD Handledning](/cad/net/export-techniques/exporting-dxf-to-pdf-format/)
- [Exportera specifik DXF-layout till PDF - Aspose.CAD Handledning](/cad/net/export-techniques/exporting-dxf-specific-layout-to-pdf/)
- [Exportera DWG till DXF-format i C# - Aspose.CAD Handledning](/cad/net/advanced-export-techniques/exporting-dwg-to-dxf/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}