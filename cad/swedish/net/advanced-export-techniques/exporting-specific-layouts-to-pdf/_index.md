---
date: 2026-03-13
description: Lär dig hur du ställer in CAD‑rasteriseringsalternativ och exporterar
  specifika DWG‑layoutar till PDF med Aspose.CAD för .NET – den definitiva guiden
  för att skapa PDF från en CAD‑fil.
linktitle: Exporting Specific Layouts to PDF
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Ställ in CAD-rasteriseringsalternativ – Exportera specifika layouter till PDF
  - Aspose.CAD Guide
url: /sv/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportera specifika layouter till PDF - Aspose.CAD Guide

## Introduction

I den här handledningen kommer du att upptäcka **hur du ställer in CAD rasterization options** så att du kan exportera en enda layout – eller flera layouter – från en DWG‑fil direkt till PDF. Aspose.CAD för .NET gör *dwg to pdf conversion c#*-processen enkel och ger dig full kontroll över sidstorlek, upplösning och layoutval. I slutet av guiden kommer du att kunna **create PDF from CAD file** med bara några få kodrader.

## Quick Answers
- **What does “set cad rasterization options” do?**  
  Det talar om för Aspose.CAD hur vektordata (layouter, lager, linjebredder) ska renderas till rasteriserade PDF‑sidor.  
- **Which method exports a DWG layout to PDF?**  
  Använd `Image.Save` med ett konfigurerat `PdfOptions` som innehåller dina `CadRasterizationOptions`.  
- **Can I export more than one layout at once?**  
  Ja – ange en array med layoutnamn i egenskapen `Layouts`.  
- **Do I need a license for production use?**  
  En kommersiell licens krävs; en gratis provversion finns tillgänglig för utvärdering.  
- **What .NET versions are supported?**  
  .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6 och senare.

## What is “set cad rasterization options”?

`CadRasterizationOptions` är klassen som styr hur CAD‑entiteter rasteriseras när de konverteras till raster‑baserade format som PDF. Genom att konfigurera dess egenskaper – sidmått, layoutval, bakgrundsfärg osv. – bestämmer du det visuella resultatet av **export dwg layout to pdf**‑operationen.

## Why set CAD rasterization options?
- **Precision** – Bevara linjebredder och skalor exakt som de visas i den ursprungliga CAD‑ritningen.  
- **Performance** – Rendera bara de layouter du behöver, vilket minskar filstorlek och bearbetningstid.  
- **Flexibility** – Justera sidbredd/höjd, DPI och bakgrund för att matcha dina rapporteringsstandarder.  

## Prerequisites

Innan vi dyker in i koden, se till att du har:

- **Aspose.CAD for .NET** installerat. Du kan ladda ner det [here](https://releases.aspose.com/cad/net/).  
- En .NET‑utvecklingsmiljö (Visual Studio, VS Code eller någon annan IDE du föredrar).  
- En DWG‑fil som innehåller minst en layout (exempelfilen som används här är `visualization_-_conference_room.dwg`).

## Import Namespaces

I ditt .NET‑projekt importerar du de nödvändiga namnutrymmena för Aspose.CAD:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Step‑by‑Step Guide

### Step 1: Load the DWG file

Först pekar du Aspose.CAD på käll‑DWG‑filen du vill konvertera.

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";

using (Image image = Image.Load(sourceFilePath))
{
    // Your code for further steps goes here.
}
```

### Step 2: Set **CadRasterizationOptions**

Här konfigurerar vi rasteriseringsinställningarna som bestämmer PDF‑sidans storlek och upplösning.

```csharp
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
```

> **Pro tip:** Justera `PageWidth` och `PageHeight` så att de matchar dimensionerna på din mål‑PDF‑layout. Större värden ger mer detalj men ökar också filstorleken.

### Step 3: Specify the layout name

Berätta för Aspose.CAD vilken(a) layout(er) som ska renderas. Ersätt `"Layout1"` med det exakta namnet på layouten i din DWG‑fil.

```csharp
// Specify desired layout name
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

> **Why this matters:** Genom att begränsa `Layouts`‑arrayen undviker du att exportera oönskade blad, vilket gör **dwg to pdf conversion c#**‑operationen snabbare och den resulterande PDF‑filen renare.

### Step 4: Create `PdfOptions`

Koppla rasteriseringsinställningarna till PDF‑exportalternativen.

```csharp
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();
// Set the VectorRasterizationOptions property
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### Step 5: Export to PDF

Spara slutligen den renderade layouten som en PDF‑fil.

```csharp
MyDir = MyDir + "ExportSpecificLayoutToPDF_out.pdf";
// Export the DWG to PDF
image.Save(MyDir, pdfOptions);
```

### Step 6: Display a success message

Ett kort konsolutskrift bekräftar att operationen lyckades.

```csharp
// Display success message
Console.WriteLine("\nThe DWG file with a specific layout exported successfully to PDF.\nFile saved at " + MyDir);
```

## Common Issues & Solutions

| Issue | Cause | Fix |
|-------|-------|-----|
| **No PDF generated** | `Layouts`‑arrayen matchar inget layoutnamn i DWG‑filen. | Verifiera layoutnamn med en CAD‑visare och uppdatera `Layouts`‑egenskapen. |
| **Blank pages** | `PageWidth`/`PageHeight` är satt till 0 eller extremt små värden. | Använd realistiska dimensioner (t.ex. 1600 × 1600) eller låt Aspose beräkna automatiskt genom att utelämna dessa egenskaper. |
| **Incorrect scaling** | DPI är inte satt när högupplöst output krävs. | Sätt `rasterizationOptions.Resolution = 300;` (eller önskad DPI) innan export. |

## Frequently Asked Questions

**Q: Can I export multiple layouts simultaneously?**  
A: Ja, ändra helt enkelt `Layouts`‑arrayen i Step 3 för att inkludera alla önskade layoutnamn, t.ex. `new string[] { "Layout1", "Layout2" }`.

**Q: Is Aspose.CAD compatible with other CAD file formats?**  
A: Absolut. Det stödjer DWG, DXF, DWF, DGN och många fler format.

**Q: How can I adjust the PDF output settings beyond page size?**  
A: Utforska ytterligare egenskaper i `CadRasterizationOptions` såsom `Resolution`, `BackgroundColor` och `DrawType` för att finjustera resultatet.

**Q: Where can I find additional Aspose.CAD documentation?**  
A: Besök [documentation](https://reference.aspose.com/cad/net/) för djupgående API‑referenser och exempel.

**Q: Is there a free trial available?**  
A: Ja, du kan få åtkomst till den fria provversionen [here](https://releases.aspose.com/).

## Conclusion

Du har nu lärt dig hur du **set CAD rasterization options** och använder dem för att **export specific DWG layouts to PDF** med Aspose.CAD för .NET. Detta tillvägagångssätt ger dig exakt kontroll över konverteringsprocessen, vilket gör det möjligt att integrera CAD‑till‑PDF‑funktionalitet i vilken C#‑applikation som helst snabbt och pålitligt.

---

**Last Updated:** 2026-03-13  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}