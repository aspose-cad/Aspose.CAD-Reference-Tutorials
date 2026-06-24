---
date: 2026-03-26
description: Lär dig hur du skapar PDF från CAD och konverterar DXF till PDF med Aspose.CAD
  för .NET. Anpassa pennalternativ för fantastiska visuella resultat i PDF, PNG, BMP
  och mer.
linktitle: Pen Support in Export
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Skapa PDF från CAD med anpassade pennalternativ – Aspose.CAD för .NET
url: /sv/net/cad-features-and-support/pen-support-in-export/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Förbättra CAD-export med anpassade pennalternativ i Aspose.CAD för .NET

## Introduction

Om du behöver **create PDF from CAD**‑filer snabbt och med full visuell kontroll, ger Aspose.CAD för .NET dig exakt det. Genom att utnyttja bibliotekets pen‑support‑funktion kan du definiera start‑ och slutkappar, linjesammansättningar och andra ritattribut, vilket ger PDF‑filer som ser exakt ut som du vill ha dem. Denna handledning guidar dig genom hela processen—från att ladda en DXF‑fil till att exportera en polerad PDF—och visar också hur samma inställningar kan återanvändas när du **export CAD to PNG** eller **rasterize CAD image**‑data för andra format.

## Quick Answers
- **Vad betyder “create PDF from CAD”?** Det konverterar vektorbaserade CAD‑ritningar (t.ex. DXF) till ett PDF‑dokument samtidigt som geometri och stil bevaras.  
- **Vilka format stödjer pennalternativ?** PDF, PNG, BMP, GIF, JPEG2000, JPEG, PSD, TIFF och WMF.  
- **Behöver jag en licens för utveckling?** En gratis provversion fungerar för testning; en kommersiell licens krävs för produktion.  
- **Kan jag ändra linjekappar för andra format?** Ja—pennalternativ gäller för alla rasteriseringsmål som stöds av Aspose.CAD.  
- **Vilka .NET‑versioner stöds?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## Vad är pennstöd i CAD-export?

Pennstöd låter dig anpassa hur linjer ritas när en CAD‑ritning rasteriseras eller vektor‑rasteriseras. Du kan ange egenskaper som `StartCap`, `EndCap`, `LineJoin` och `DashStyle`. Dessa inställningar påverkar det slutgiltiga utseendet på den exporterade bilden eller PDF‑filen och ger dig fin‑granulär kontroll över den visuella kvaliteten.

## Varför använda anpassade pennalternativ när du **create PDF from CAD**?

- **Consistent branding** – matcha företagets linjestilar i alla dokument.  
- **Improved readability** – tjockare kappar och sammankopplingar gör tekniska ritningar tydligare på skärm och i utskrift.  
- **Cross‑format flexibility** – samma pennkonfiguration fungerar för PNG, BMP och andra rasterformat, vilket sparar tid.

## Förutsättningar

- Aspose.CAD för .NET installerat (ladda ner från den [release page](https://releases.aspose.com/cad/net/)).  
- Grundläggande kunskap om DXF (Drawing Exchange Format).  
- Bekantskap med C#‑programmering.

## Importera namnrymder

För att komma igång, se till att du importerar de nödvändiga namnrymderna i ditt C#‑projekt:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Drawing;
using System.Drawing.Drawing2D;
```

## Steg 1: Ställ in din dokumentkatalog

Definiera mappen som innehåller käll‑CAD‑filen:

```csharp
string MyDir = "Your Document Directory";
```

## Steg 2: Ladda CAD‑bilden

Ladda CAD‑ritningen (t.ex. en DXF‑fil) i ett `Aspose.CAD.Image`‑objekt:

```csharp
string sourceFilePath = MyDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage)Image.Load(sourceFilePath);
```

## Steg 3: Konfigurera rasteriseringsalternativ

Skapa rasteriserings‑ och PDF‑alternativobjekt. Dessa objekt låter dig styra hur CAD‑data omvandlas till en rasterbild eller PDF‑sida:

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
PdfOptions pdfOptions = new PdfOptions();
```

## Steg 4: Anpassa pennalternativ

Här är där du **customize the pen** som ritar linjerna. Du kan sätta start‑ och slutkappar till `Flat`, `Round`, `Square` osv. Detta är kärnan i “how to export CAD” med den visuella stil du behöver:

```csharp
rasterizationOptions.PenOptions = new PenOptions
{
   StartCap = LineCap.Flat,
   EndCap = LineCap.Flat
};
```

*Pro tip:* Experimentera med `LineCap.Round` för mjukare linjeändar när du **export CAD to PNG**.

## Steg 5: Använd vektor‑rasteriseringsalternativ

Fäst rasteriseringsinställningarna på PDF‑alternativen så exportprocessen vet vilken pennkonfiguration som ska användas:

```csharp
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Steg 6: Spara den exporterade PDF‑filen

Slutligen, generera PDF‑filen. Detta steg **creates PDF from CAD** med de anpassade penninställningarna tillämpade:

```csharp
cadImage.Save(MyDir + "9LHATT-A56_generated.pdf", pdfOptions);
```

Du kan ersätta `PdfOptions` med `PngOptions`, `BmpOptions` osv., för att **export CAD to PNG** eller andra rasterformat samtidigt som du behåller samma pennkonfiguration.

## Vanliga användningsfall

- **Technical documentation** – infoga precisa linjestilar i ingenjörs‑PDF‑filer.  
- **Automated report generation** – batch‑processa många DXF‑filer till PDF‑filer med en enda pennprofil.  
- **Web services** – exponera ett API som konverterar uppladdade DXF‑filer till PDF‑filer i realtid, vilket säkerställer konsekvent stil.

## Felsökning & vanliga fallgropar

| Problem | Orsak | Lösning |
|---------|-------|----------|
| Exporterade linjer ser tjockare ut än förväntat | DPI är högre än avsett | Ställ in `rasterizationOptions.PageWidth` / `PageHeight` eller justera `Resolution`. |
| Pennalternativ ignoreras för PNG‑utdata | Använder `ImageOptions` istället för `VectorRasterizationOptions` | Se till att du tilldelar `rasterizationOptions.PenOptions` innan du sparar. |
| PDF‑filen är tom | Käll‑DXF‑sökvägen är felaktig eller filen är korrupt | Verifiera `sourceFilePath` och bekräfta att DXF‑filen laddas utan undantag. |

## Vanliga frågor

### Q1: Kan jag använda dessa pennalternativ för andra bildformat än PDF?

A1: Ja, pennalternativen kan tillämpas på olika bildformat såsom PNG, BMP, GIF, JPEG och fler.

### Q2: Var kan jag hitta ytterligare dokumentation för Aspose.CAD för .NET?

A2: Se [documentation](https://reference.aspose.com/cad/net/) för omfattande information och exempel.

### Q3: Finns det en gratis provversion tillgänglig för Aspose.CAD för .NET?

A3: Ja, du kan få en gratis provversion [here](https://releases.aspose.com/).

### Q4: Hur kan jag få tillfälliga licenser för Aspose.CAD för .NET?

A4: Besök [temporary license page](https://purchase.aspose.com/temporary-license/) för tillfälliga licensalternativ.

### Q5: Var kan jag söka gemenskapsstöd för Aspose.CAD för .NET?

A5: Engagera dig med gemenskapen på [Aspose.CAD forum](https://forum.aspose.com/c/cad/19).

## Ytterligare vanliga frågor

**Q: Hur konverterar jag **convert DXF to PDF** programatiskt?**  
A: Ladda DXF‑filen med `Image.Load`, konfigurera `CadRasterizationOptions` och `PdfOptions`, och anropa sedan `Save` som visas i stegen ovan.

**Q: Kan jag rasterisera en CAD‑bild utan att skapa en PDF?**  
A: Ja—använd `PngOptions`, `BmpOptions` eller någon annan rasterformatklass och tilldela samma `rasterizationOptions` för att uppnå högkvalitativ rasterisering.

**Q: Är det möjligt att ändra linjebredden när man skapar en PDF från CAD?**  
A: Justera `rasterizationOptions.CustomLineWidth` eller ändra `PenOptions.Width`‑egenskapen innan du sparar.

**Q: Stöder biblioteket 3D DXF‑filer?**  
A: Aspose.CAD fokuserar på 2D‑vektordata; 3D‑entiteter ignoreras under rasterisering.

**Q: Vilken version av Aspose.CAD krävs för dessa funktioner?**  
A: Pennstöd har funnits sedan version 20.9; vilken nyare version som helst fungerar.

---

**Senast uppdaterad:** 2026-03-26  
**Testat med:** Aspose.CAD för .NET 24.12  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}