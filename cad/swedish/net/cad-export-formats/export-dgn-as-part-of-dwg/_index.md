---
date: 2026-03-21
description: Lär dig hur du skapar PDF från DWG och exporterar DGN som en del av DWG
  med Aspose.CAD för .NET. Denna guide visar också hur du konverterar DWG till PDF
  och ställer in PDF‑alternativ.
linktitle: Export DGN as Part of DWG
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Skapa PDF från DWG och exportera DGN som del av DWG – Aspose.CAD för .NET
url: /sv/net/cad-export-formats/export-dgn-as-part-of-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Skapa PDF från DWG och exportera DGN som del av DWG – Aspose.CAD för .NET

## Introduction

Om du behöver **skapa PDF från DWG**‑filer samtidigt som du bäddar in en DGN‑design som en del av DWG‑filen, gör Aspose.CAD för .NET det enkelt. I den här handledningen går vi igenom hela arbetsflödet: läsa in en DWG, hitta den inbäddade DGN‑underlayen, konfigurera rasteriseringsalternativ och slutligen exportera resultatet till ett PDF‑dokument. Oavsett om du bygger ett batch‑konverteringsverktyg, en rapportmotor eller en CAD‑BIM‑integrationsservice, ger stegen nedan dig en solid, produktionsklar grund.

## Quick Answers
- **Vilket bibliotek hanterar DWG → PDF‑konvertering?** Aspose.CAD för .NET  
- **Kan jag exportera en DGN‑underlay medan jag skapar PDF‑filen?** Ja – underlayen nås via `CadDgnUnderlay`.  
- **Vilken metod ställer in PDF‑alternativ?** `PdfOptions` tillsammans med `CadRasterizationOptions`.  
- **Behöver jag en licens för kommersiell användning?** Ja, en giltig Aspose.CAD‑licens krävs.  
- **Stödda .NET‑versioner?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## What is “create PDF from DWG”?

Att skapa en PDF från en DWG‑fil innebär att rendera den vektorbaserade ritningen till ett raster‑ eller vektorbaserat PDF‑dokument. Detta är användbart för att dela ritningar med intressenter som inte har CAD‑programvara, för arkivering eller för att generera utskrivbara rapporter. Aspose.CAD förenklar uppgiften genom att hantera den tunga parsningen av DWG‑entiteter och erbjuder fin‑granulär kontroll över utdata via `PdfOptions`.

## Why export DGN as part of a DWG?

En DGN‑underlay representerar ofta referensgeometri från MicroStation‑projekt. Genom att exportera DGN tillsammans med DWG bevaras den ursprungliga designkontexten, vilket säkerställer att mottagare ser hela ritningssättet. Detta är särskilt värdefullt i tvärvetenskapliga projekt där både DWG‑ och DGN‑filer samexisterar.

## Prerequisites

- **Aspose.CAD för .NET** – ladda ner den [here](https://releases.aspose.com/cad/net/).  
- **Utvecklingsmiljö** – Visual Studio (valfri nyare version) eller din föredragna .NET‑IDE.  
- **Grundläggande C#‑kunskaper** – du bör vara bekväm med C#‑syntax och .NET‑projektstruktur.

## Import Namespaces

Lägg till de nödvändiga `using`‑direktiven högst upp i din C#‑källfil:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Step‑by‑Step Guide

### Step 1: Define File Paths

Ange indata‑DWG‑filen och namn på utdata‑PDF‑filen.

```csharp
// Input and Output file paths
string fileName = "BlockRefDgn.dwg";
string outPath = fileName + ".pdf";
```

### Step 2: Create `PdfOptions` Instance (set pdf options)

`PdfOptions` låter dig styra hur PDF‑filen genereras, t.ex. sidstorlek, komprimering och metadata.

```csharp
// Create an instance of PdfOptions class for exporting DWG to PDF
PdfOptions exportOptions = new PdfOptions();
```

### Step 3: Load the DWG File

Läs in DWG‑filen som ett `CadImage` så att du kan inspektera dess entiteter.

```csharp
// Load the existing DWG file as an image and convert it to CadImage type
using (CadImage cadImage = (CadImage)Image.Load(fileName))
```

### Step 4: Iterate Through Entities

Gå igenom varje entitet i ritningen för att hitta DGN‑underlayen.

```csharp
// Iterate through each entity inside the DWG file
foreach (CadBaseEntity baseEntity in cadImage.Entities)
```

### Step 5: Check Entity Type (how to export dgn)

Identifiera om den aktuella entiteten är en DGN‑underlay.

```csharp
// Check if the entity is an image definition
if (baseEntity.TypeName == CadEntityTypeName.DGNUNDERLAY)
```

### Step 6: Get Underlay Path

Hämta den externa referensvägen till DGN‑filen.

```csharp
// If it's an image definition, get the external reference to the object
CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
Console.WriteLine(dgnFile.UnderlayPath);
```

### Step 7: Define Rasterization Options (convert dwg to pdf)

Konfigurera hur DWG‑filen rasteriseras innan den placeras i PDF‑filen.

```csharp
// Define settings for CadRasterizationOptions object
exportOptions.VectorRasterizationOptions = new CadRasterizationOptions()
{
    PageWidth = 1600,
    PageHeight = 1600,
    Layouts = new string[] { "Model" },
    AutomaticLayoutsScaling = false,
    NoScaling = true,
    BackgroundColor = Color.Black,
    DrawType = CadDrawTypeMode.UseObjectColor
};
```

### Step 8: Export DWG to PDF

Spara slutligen den renderade bilden som en PDF‑fil.

```csharp
// Export the DWG to PDF by calling Save method
cadImage.Save(outPath, exportOptions);
```

## Common Issues and Solutions

| Issue | Reason | Fix |
|-------|--------|-----|
| **`Image.Load` throws “File not found”** | Felaktig sökväg eller saknad fil. | Använd en absolut sökväg eller säkerställ att DWG‑filen kopieras till output‑mappen. |
| **Underlay path is empty** | DGN‑underlay ej inbäddad eller referens bruten. | Verifiera att DWG‑filen faktiskt innehåller en DGN‑underlay och att den externa DGN‑filen är åtkomlig. |
| **PDF output is blank** | Rasteriseringsalternativ satta till nollstorlek. | Justera `PageWidth`/`PageHeight` eller sätt `NoScaling = false`. |
| **License exception** | Kör utan en giltig Aspose.CAD‑licens. | Applicera licensen innan bilden laddas: `License lic = new License(); lic.SetLicense("Aspose.CAD.lic");` |

## Frequently Asked Questions

### Q1: Can I use Aspose.CAD for .NET in my commercial projects?
A1: Yes, you can. Visit [here](https://purchase.aspose.com/buy) to explore licensing options.

### Q2: Are there any limitations on the size of DWG files I can process?
A2: Aspose.CAD supports handling large DWG files, but hardware limitations may apply.

### Q3: Is there a trial version available?
A3: Yes, you can get a free trial [here](https://releases.aspose.com/).

### Q4: How can I get temporary licenses?
A4: Temporary licenses can be obtained [here](https://purchase.aspose.com/temporary-license/).

### Q5: Where can I seek assistance if I encounter issues?
A5: You can visit the Aspose.CAD forum [here](https://forum.aspose.com/c/cad/19) for support.

**Q: How do I set additional PDF metadata (author, title, etc.)?**  
A: Use `exportOptions.Metadata` properties before calling `Save`.

**Q: Can I export multiple layouts into separate PDF pages?**  
A: Yes – set `Layouts = new string[] { "Layout1", "Layout2" }` in `CadRasterizationOptions`.

**Q: Does Aspose.CAD support converting DWG to other image formats?**  
A: Absolutely. You can export to PNG, JPEG, SVG, and more by using the corresponding `Image.Save` overloads.

---

**Last Updated:** 2026-03-21  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}