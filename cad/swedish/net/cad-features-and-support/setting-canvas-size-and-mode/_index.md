---
date: 2026-03-29
description: Lär dig hur du skapar PDF från CAD, ställer in canvasstorlek och exporterar
  CAD till PDF eller TIFF med Aspose.CAD för .NET i den här steg‑för‑steg‑guiden.
linktitle: Setting Canvas Size and Mode
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 'Hur man skapar PDF från CAD: Ställ in canvasstorlek och läge i Aspose.CAD
  för .NET'
url: /sv/net/cad-features-and-support/setting-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ställa in dukstorlek och läge i Aspose.CAD för .NET

## Introduktion

Redo att **create PDF from CAD**‑filer samtidigt som du kontrollerar utmatningsdimensionerna? I den här handledningen går vi igenom hur du ställer in dukstorlek och läge, laddar en CAD‑fil och exporterar den till PDF eller TIFF med Aspose.CAD för .NET. Oavsett om du behöver **convert DXF to PDF**, skapa högupplösta ritningar eller helt enkelt justera rasteriseringsområdet, så ger stegen nedan dig en solid, produktionsklar lösning.

## Snabba svar
- **Vad betyder “create PDF from CAD”?** Konvertering av en CAD‑ritning (t.ex. DXF, DWG) till ett PDF‑dokument som bevarar vektor‑ och rasterdetaljer.  
- **Vilket alternativ styr utmatningsstorleken?** `CadRasterizationOptions.PageWidth` och `PageHeight` (dukstorlek).  
- **Kan jag också exportera till TIFF?** Ja – använd `TiffOptions` med samma rasteriseringsinställningar.  
- **Behöver jag en licens för produktion?** En kommersiell licens krävs; en gratis provversion finns tillgänglig.  
- **Stödda .NET‑versioner?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## Vad betyder “create PDF from CAD”?
Att skapa en PDF från CAD innebär att rendera CAD‑ritningen till ett sidorienterat format (PDF) som kan visas, skrivas ut eller delas utan att behöva CAD‑programvara. Aspose.CAD sköter det tunga arbetet och låter dig definiera dukstorlek, skalning och utdataformat.

## Varför ange dukstorlek när du skapar PDF från CAD?
Att ange dukstorlek ger dig exakt kontroll över upplösning och dimensioner på den resulterande PDF‑ eller TIFF‑filen. Detta är särskilt användbart när:
- Du förbereder ritningar för utskrift på specifika pappersstorlekar.  
- Du genererar miniatyrbilder eller högupplösta bilder för webb‑förhandsgranskning.  
- Du säkerställer en konsekvent layout över flera dokument.

## Förutsättningar

- Aspose.CAD Library: Ladda ner och installera Aspose.CAD‑biblioteket från [Aspose.CAD website](https://releases.aspose.com/cad/net/).
- Development Environment: Se till att du har en .NET‑utvecklingsmiljö installerad på din maskin.
- Sample CAD File: För den här handledningen använder vi en exempel‑DXF‑fil. Du kan hitta en i [Aspose.CAD documentation](https://reference.aspose.com/cad/net/).

## Importera namnrymder

Först importerar du de namnrymder som krävs för CAD‑bearbetning:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Så skapar du PDF från CAD med anpassad dukstorlek

### Steg 1: Ladda CAD‑fil

Vi börjar med att **ladda CAD‑filen** (t.ex. en DXF) i ett `Image`‑objekt. Detta är punkten där du **laddar CAD‑filen** i minnet.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    // Your code for further steps will go here
}
```

### Steg 2: Skapa CadRasterizationOptions

Skapa en `CadRasterizationOptions`‑instans och definiera dukstorleken. `PageWidth`‑ och `PageHeight`‑egenskaperna låter dig **ange dukstorlek** till de exakta dimensioner du behöver.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
rasterizationOptions.NoScaling = false;
```

### Steg 3: Skapa PdfOptions (Exportera CAD till PDF)

Koppla rasteriseringsinställningarna till ett `PdfOptions`‑objekt. Denna konfiguration gör att du kan **exportera CAD till PDF** med den anpassade duk du definierat.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### Steg 4: Exportera till PDF (Konvertera DXF till PDF)

Spara nu bilden som en PDF. Detta steg **skapar PDF från CAD** med de alternativ vi har angett.

```csharp
image.Save(MyDir + "result_out.pdf", pdfOptions);
```

### Steg 5: Skapa TiffOptions (Exportera CAD till TIFF)

Om du också behöver en rasterbild, konfigurera `TiffOptions`. Samma rasteriseringsalternativ återanvänds, så **exportera CAD till TIFF** respekterar dukstorleken.

```csharp
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.VectorRasterizationOptions = rasterizationOptions;
```

### Steg 6: Exportera till TIFF

Spara slutligen ritningen som en TIFF‑fil.

```csharp
image.Save(MyDir + "result_out.tiff", tiffOptions);
```

## Vanliga problem och lösningar

- **Canvas appears cropped** – Verifiera att `AutomaticLayoutsScaling` är satt till `true` och `NoScaling` är `false` så att ritningen skalas för att passa duken.  
- **Low‑resolution PDF** – Öka `PageWidth`/`PageHeight` eller sätt `Resolution` på `CadRasterizationOptions`.  
- **File not found error** – Säkerställ att `MyDir` pekar på en giltig katalog och att DXF‑filnamnet matchar exakt.

## Vanliga frågor

### Q1: Kan jag använda Aspose.CAD med andra .NET‑bibliotek?
A1: Ja, Aspose.CAD integreras sömlöst med andra .NET‑bibliotek och ger förbättrade möjligheter för CAD‑manipulation.

### Q2: Finns en gratis provversion av Aspose.CAD?
A2: Ja, du kan utforska funktionerna i Aspose.CAD med en gratis provversion. Besök [here](https://releases.aspose.com/) för att komma igång.

### Q3: Hur kan jag få support för Aspose.CAD?
A3: För support och diskussioner, besök [Aspose.CAD forum](https://forum.aspose.com/c/cad/19).

### Q4: Var kan jag hitta omfattande dokumentation för Aspose.CAD?
A4: Se [Aspose.CAD documentation](https://reference.aspose.com/cad/net/) för detaljerad information och exempel.

### Q5: Hur köper jag Aspose.CAD för .NET?
A5: För att köpa Aspose.CAD, besök [purchase page](https://purchase.aspose.com/buy).

**Q: Kan jag exportera en flersidig CAD‑ritning till en enda PDF?**  
A: Ja. Ställ in `PageCount` i `CadRasterizationOptions` så kommer biblioteket att sammanfoga sidorna till en PDF.

**Q: Påverkar dukstorleken kvaliteten på vektordata?**  
A: Vektordata förblir upplösningsoberoende; dukstorleken påverkar endast rasteriserade element och bildens upplösning.

**Senast uppdaterad:** 2026-03-29  
**Testad med:** Aspose.CAD 24.11 för .NET  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}