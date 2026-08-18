---
date: 2026-03-02
description: Lär dig hur du skapar en enda PDF med olika layouter med Aspise.CAD för
  .NET – konvertera CAD till PDF, exportera DWG till PDF och spara CAD som PDF på
  ett effektivt sätt.
linktitle: Creating Single PDF with Different Layouts
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Hur man skapar en enda PDF med olika layouter – Aspose.CAD-guide
url: /sv/net/advanced-cad-techniques/creating-single-pdf-with-different-layouts/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hur man skapar en enda pdf med olika layouter - Aspose.CAD Guide

## Introduktion

Om du behöver **create single pdf** filer som innehåller flera CAD‑layouter, är du på rätt plats. I den här handledningen går vi igenom de exakta stegen som krävs för att konvertera CAD‑ritningar till ett PDF‑dokument, med hantering av flera layouter på vägen. Du kommer att se hur Aspose.CAD för .NET gör det enkelt att **convert CAD to PDF**, **export DWG to PDF**, och **save CAD as PDF** med bara några rader C#‑kod.

## Snabba svar
- **What does this tutorial cover?** Generera en PDF som innehåller flera CAD‑layouter.  
- **Which library is used?** Aspose.CAD for .NET.  
- **Do I need a license?** En gratis provversion fungerar för utvärdering; en licens krävs för produktion.  
- **Supported CAD formats?** DWG, DXF, DGN och många andra.  
- **Typical implementation time?** Omkring 10‑15 minuter för en grundläggande konvertering.

## Vad betyder “create single pdf” i ett CAD‑sammanhang?

Att skapa en enda PDF innebär att ta en CAD‑källfil som kan innehålla flera layoutdefinitioner (paperspaces) och slå ihop varje layout till separata sidor i ett PDF‑dokument. Detta är särskilt användbart för arkitektoniska ritningar, ingenjörsscheman eller någon situation där en kund förväntar sig ett samlat PDF‑paket.

## Varför använda Aspose.CAD för denna uppgift?

- **No external dependencies** – ren .NET, ingen AutoCAD‑installation krävs.  
- **Full control over rasterization** – du kan ange sidstorlek, DPI och anpassade layoutdimensioner.  
- **High‑fidelity rendering** – vektordata bevaras där det är möjligt, vilket säkerställer skarp output.  
- **Batch‑ready** – samma kod kan placeras i en loop för att automatiskt bearbeta många ritningar.

## Förutsättningar

- Aspose.CAD for .NET: Se till att du har Aspose.CAD for .NET installerat. Du kan ladda ner det från [here](https://releases.aspose.com/cad/net/).  
- Development Environment: Ställ in en .NET‑utvecklingsmiljö och ha en grundläggande förståelse för C#‑programmering.

## Importera namnrymder

I ditt C#‑projekt, inkludera de nödvändiga namnrymderna för att utnyttja funktionerna i Aspose.CAD för .NET:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Steg‑för‑steg‑guide

### Steg 1: Ladda CAD‑bilden

Först, ladda käll‑CAD‑filen (t.ex. en DWG‑ritning). Klassen `CadImage` ger dig åtkomst till alla layouter i filen.

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";

using (CadImage cadImage = (CadImage)Image.Load(MyDir + "City skyway map.dwg"))
{
    // Your code for Step 1 goes here
}
```

### Steg 2: Anpassa rasteriseringsalternativ

Definiera hur varje layout ska rasteriseras. Du kan ange en standard sidstorlek och sedan åsidosätta den för specifika layouter med `LayoutPageSizes`.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1000;
rasterizationOptions.PageHeight = 1000;

// Custom sizes for several layouts
rasterizationOptions.LayoutPageSizes.Add("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.LayoutPageSizes.Add("8.5 x 11 Plot", new SizeF(1000, 100));
```

> **Pro tip:** Justera DPI (`rasterizationOptions.Resolution`) om du behöver högre upplösning för detaljerade ritningar.

### Steg 3: Definiera PDF‑alternativ

Packa rasteriseringsinställningarna i ett `PdfOptions`‑objekt. Detta instruerar Aspose.CAD att rendera CAD‑data direkt till en PDF‑ström.

```csharp
PdfOptions pdfOptions = new PdfOptions() { VectorRasterizationOptions = rasterizationOptions };
```

### Steg 4: Spara som PDF

Slutligen, anropa `Save` på `CadImage`‑instansen, ange målets PDF‑filnamn och de förberedda alternativen. Biblioteket kommer att generera en enda PDF som innehåller en sida för varje layout du konfigurerat.

```csharp
cadImage.Save(MyDir + "singlePDF_out.pdf", pdfOptions);
```

Efter detta anrop har du en PDF som kombinerar layouterna “ANSI C Plot” och “8.5 x 11 Plot” till ett sammanhängande dokument.

## Vanliga fallgropar & felsökning

| Problem | Orsak | Lösning |
|---------|-------|---------|
| Layouter saknas i PDF | `LayoutPageSizes` är inte definierad för ett layoutnamn | Verifiera de exakta layoutnamnen i CAD‑filen (skiftlägeskänsligt). |
| Lågkvalitativ output | Standard‑DPI är 96 | Ställ in `rasterizationOptions.Resolution = 300` (eller högre) innan du sparar. |
| Filen hittades inte | Fel `MyDir`‑sökväg | Använd `Path.Combine` för att bygga plattformsoberoende sökvägar. |

## Vanliga frågor

### Q1: Kan jag använda Aspose.CAD för .NET med andra CAD‑format?

A1: Ja, Aspose.CAD för .NET stödjer olika CAD‑format såsom DWG, DXF, DGN och fler.

### Q2: Finns en gratis provversion tillgänglig?

A2: Ja, du kan utforska en gratis provversion [here](https://releases.aspose.com/).

### Q3: Hur kan jag få support för Aspose.CAD för .NET?

A3: Besök [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) för gemenskapsstöd.

### Q4: Var kan jag hitta detaljerad dokumentation?

A4: Se dokumentationen [here](https://reference.aspose.com/cad/net/).

### Q5: Kan jag köpa en licens för Aspose.CAD för .NET?

A5: Ja, du kan köpa en licens [here](https://purchase.aspose.com/buy).

**Additional Q&A**

**Q:** Hur exporterar jag **export DWG to PDF** med anpassade sidstorlekar?  
**A:** Använd `CadRasterizationOptions.LayoutPageSizes` för att mappa varje DWG‑layout till önskade PDF‑sidimensioner, som visas i Steg 2.

**Q:** Är det möjligt att **save CAD as PDF** utan att rasterisera vektordata?  
**A:** Aspose.CAD rasteriserar alltid när PDF skapas, men du kan öka DPI för att behålla visuell noggrannhet.

## Slutsats

I den här guiden demonstrerade vi hur man **create single pdf** filer från CAD‑ritningar som innehåller flera layouter, med Aspose.CAD för .NET. Du har nu byggstenarna för att **convert CAD to PDF**, **export DWG to PDF**, och **save CAD as PDF** i ett enda, automatiserat arbetsflöde. Experimentera med olika rasteriseringsinställningar för att matcha ditt projekts kvalitetskrav, och integrera denna kod i större batch‑bearbetningspipelines vid behov.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Senast uppdaterad:** 2026-03-02  
**Testad med:** Aspose.CAD for .NET 24.11  
**Författare:** Aspose