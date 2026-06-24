---
date: 2026-03-07
description: Lär dig hur du exporterar CAD till SVG med Aspose.CAD för .NET, anpassar
  SVG-färg och konverterar DWG till SVG effektivt.
linktitle: Exporting CAD Drawings to SVG Format
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Exportera CAD till SVG – Exportera CAD-ritningar till SVG-format - Aspose.CAD‑guide
url: /sv/net/advanced-export-techniques/exporting-cad-drawings-to-svg/
weight: 15
---

Also include backtop button shortcode.

Make sure to keep all shortcodes exactly.

Now produce final content.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportera CAD till SVG – Exportera CAD-ritningar till SVG-format

## Introduktion

Att exportera CAD-ritningar till SVG är ett vanligt krav när du behöver upplösningsoberoende grafik för webbsidor, rapporter eller interaktiva visualiseringar. I den här handledningen kommer du att lära dig **hur man exporterar CAD till SVG** med Aspose.CAD för .NET, utforska alternativ för **anpassa SVG-färg**, och se hur man **konverterar DWG till SVG** (eller DXF till SVG) på bara några kodrader. Stegen är snabba, API:et är intuitivt, och de resulterande SVG-filerna skalas perfekt på alla enheter.

## Snabba svar
- **Vilket bibliotek hanterar konverteringen?** Aspose.CAD för .NET.  
- **Kan jag ändra färgläget?** Ja – använd `SvgColorMode` för att ställa in gråskala, svart‑vitt eller fullfärg.  
- **Vilka CAD-format stöds?** DWG, DXF och många andra (se Aspose.CAD-dokumentationen).  
- **Behöver jag en licens för utveckling?** En tillfällig licens finns tillgänglig för testning.  
- **Hur lång tid tar konverteringen?** Vanligtvis under en sekund för standardritningar.

## Vad är “exportera CAD till SVG”?
Att exportera CAD till SVG innebär att ta en inbyggd CAD-fil (såsom DWG eller DXF) och rendera den till Scalable Vector Graphics-formatet. SVG är XML‑baserat, lättviktigt och kan stylas med CSS—vilket gör det idealiskt för moderna webb‑ och mobilapplikationer.

## Varför använda Aspose.CAD för att exportera CAD till SVG?
- **Inga externa beroenden** – ren .NET API, ingen AutoCAD‑installation behövs.  
- **Finjusterad kontroll** – du kan **anpassa SVG-färg**, bestämma om text behålls som former, och välja rasteriseringsalternativ.  
- **Brett formatstöd** – samma kod fungerar för **konvertera DWG till SVG**, **konvertera DXF till SVG**, och andra format, vilket förenklar din kodbas.  
- **Hög prestanda** – optimerad för hastighet och låg minnesanvändning, lämplig för batch‑bearbetning.

## Förutsättningar

Innan du börjar, se till att du har:

- **Aspose.CAD för .NET** installerat. Du kan ladda ner biblioteket [here](https://releases.aspose.com/cad/net/).  
- En .NET‑utvecklingsmiljö (Visual Studio, Rider eller .NET CLI).  
- En CAD‑fil (DWG eller DXF) som du vill konvertera.

## Importera namnrymder

Först, importera de nödvändiga namnrymderna i ditt projekt så att klasserna är tillgängliga.

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Steg‑för‑steg‑guide

### Steg 1: Ange dokumentkatalogen  
Definiera mappen där din käll‑CAD‑fil finns och där SVG‑utdata ska sparas.

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";
```

### Steg 2: Läs in CAD‑ritningen  
Använd `Image.Load` för att läsa DWG‑ (eller DXF‑) filen. Detta fungerar för **load DWG .NET**‑scenarier.

```csharp
using (Image image = Image.Load(MyDir + "sample.dwg"))
{
```

### Steg 3: Konfigurera SVG‑exportalternativ  
Justera exportinställningarna så att de matchar dina behov. Här sätter vi färgläget till gråskala och tvingar all text att renderas som vektorformer.

```csharp
    var options = new SvgOptions();
    options.ColorType = SvgColorMode.Grayscale;   // customize SVG color mode
    options.TextAsShapes = true;                  // ensures text appears as shapes
```

### Steg 4: Spara SVG‑filen  
Slutligen, skriv SVG‑filen till disk. Detta steg **sparar CAD som SVG** och slutför konverteringen.

```csharp
    image.Save(MyDir + "sample.svg", options);
}
```

Genom att följa dessa fyra korta steg kan du **konvertera DWG till SVG** (eller **konvertera DXF till SVG**) med full kontroll över utseendet på resultatet.

## Vanliga problem och lösningar

| Issue | Cause | Fix |
|-------|-------|-----|
| **Tom SVG‑utdata** | Sökvägen till källfilen är felaktig eller filen är korrupt. | Verifiera `MyDir` och säkerställ att CAD‑filen öppnas utan fel. |
| **Färger ser felaktiga ut** | `SvgColorMode` är oavsiktligt satt till Gråskala. | Ändra `options.ColorType` till `SvgColorMode.FullColor` för att behålla originalfärgerna. |
| **Text saknas** | `TextAsShapes` är satt till `false` och visaren stödjer inte inbäddade typsnitt. | Behåll `TextAsShapes = true` eller bädda in de nödvändiga typsnitten i SVG‑filen. |

## Vanliga frågor

### Q1: Är Aspose.CAD kompatibel med alla CAD-format?
A1: Aspose.CAD stöder olika CAD-format, inklusive DWG och DXF, vilket säkerställer bred kompatibilitet.

### Q2: Kan jag anpassa färgläget vid export till SVG?
A2: Ja, Aspose.CAD låter dig välja färgläget, vilket ger flexibilitet i resultatet.

### Q3: Finns tillfälliga licenser tillgängliga för testning?
A3: Ja, du kan skaffa en tillfällig licens [here](https://purchase.aspose.com/temporary-license/) för utvärdering.

### Q4: Var kan jag hitta detaljerad dokumentation för Aspose.CAD?
A4: Dokumentationen finns tillgänglig [here](https://reference.aspose.com/cad/net/).

### Q5: Hur kan jag få support eller ställa frågor relaterade till Aspose.CAD?
A5: Besök community‑forumet [here](https://forum.aspose.com/c/cad/19) för support och diskussioner.

## Vanligt förekommande frågor

**Q: Kan jag använda den här koden med .NET Core eller .NET 6?**  
A: Absolut. Aspose.CAD för .NET är kompatibel med .NET Framework, .NET Core och .NET 5/6+.

**Q: Är det möjligt att exportera endast en specifik layout eller lager?**  
A: Ja. Använd `SvgOptions` för att sätta `PageIndex` eller filtrera lager innan du sparar.

**Q: Hur bäddar jag in anpassade CSS‑stilar i den genererade SVG‑filen?**  
A: Efter sparning kan du efterbehandla SVG‑XML för att injicera `<style>`‑element, eller använda `options.CustomCss` om det finns i nyare versioner.

**Q: Vilka storleksgränser finns för käll‑CAD‑filen?**  
A: Biblioteket hanterar stora filer, men minnesanvändningen ökar med komplexiteten. För mycket stora ritningar, överväg att bearbeta sidor individuellt.

**Q: Bevarar konverteringen linjebredder och linjetyper?**  
A: Som standard bevaras linjebredder. Du kan justera renderingsalternativ i `SvgOptions` för finare kontroll.

**Last Updated:** 2026-03-07  
**Tested With:** Aspose.CAD for .NET 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}