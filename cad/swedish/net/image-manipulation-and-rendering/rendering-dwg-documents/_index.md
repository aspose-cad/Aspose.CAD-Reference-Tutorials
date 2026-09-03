---
date: 2026-08-23
description: Lär dig hur du skapar viewport dwg c# med Aspose.CAD. Denna guide täcker
  loading av en DWG-fil, configuring rasterization, defining en viewport och saving
  resultatet som PDF.
keywords:
- create viewport dwg c#
- render dwg c#
- aspose.cad .net
lastmod: 2026-08-23
linktitle: Rendering av DWG-dokument i C#
og_description: Lär dig hur du skapar viewport dwg c# med Aspose.CAD. Denna guide
  täcker loading av en DWG-fil, configuring rasterization, defining en viewport och
  saving resultatet som PDF.
og_image_alt: Guide showing how to create viewport dwg c# with Aspose.CAD in .NET
og_title: Hur man skapar viewport dwg c# med Aspose.CAD för .NET
schemas:
- author: Aspose
  dateModified: '2026-08-23'
  description: Learn how to create viewport dwg c# using Aspose.CAD. This guide covers
    loading a DWG file, configuring rasterization, defining a viewport, and saving
    the result as PDF.
  headline: How to create viewport dwg c# with Aspose.CAD for .NET
  type: TechArticle
- questions:
  - answer: Load the DWG file with `CadImage.Load`.
    question: What is the first step?
  - answer: '`Viewport` inside `CadRasterizationOptions`.'
    question: Which class defines the view area?
  - answer: Yes, using `PdfOptions` after rasterization.
    question: Can I output to PDF?
  - answer: A commercial license is required; a free trial works for evaluation.
    question: Do I need a license for production?
  - answer: Absolutely – Aspose.CAD works with .NET Framework, .NET Core, and .NET 5/6.
    question: Is .NET Core supported?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- create viewport dwg c#
- Aspose.CAD
- C# CAD rendering
- DWG to PDF
- CAD viewports
title: Hur man skapar viewport dwg c# med Aspose.CAD för .NET
url: /sv/net/image-manipulation-and-rendering/rendering-dwg-documents/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Rendera DWG-dokument i C# – skapa viewport dwg c# handledning

## Introduktion

I den här omfattande handledningen kommer du att lära dig hur du **create viewport dwg c#** med Aspose.CAD och renderar en DWG-fil till PDF. Oavsett om du behöver extrahera en specifik layout, generera ett utskrivbart blad eller bädda in en CAD-vy i en rapport, ger kontroll av viewporten dig exakt renderingskontroll. Aspose.CAD stöder **20+ CAD formats** och kan bearbeta filer med tusentals entiteter utan att ladda hela dokumentet i minnet, vilket gör det idealiskt för högpresterande .NET-applikationer.

## Snabba svar
- **Vad är det första steget?** Läs in DWG-filen med `CadImage.Load`.
- **Vilken klass definierar visningsområdet?** `Viewport` i `CadRasterizationOptions`.
- **Kan jag exportera till PDF?** Ja, med `PdfOptions` efter rasterisering.
- **Behöver jag en licens för produktion?** En kommersiell licens krävs; en gratis provversion fungerar för utvärdering.
- **Stöds .NET Core?** Absolut – Aspose.CAD fungerar med .NET Framework, .NET Core och .NET 5/6.

## Förutsättningar

Innan du dyker ner i koden, se till att du har:

- Grundläggande kunskap i C#-programmering.
- Visual Studio (någon nyare version) installerad.
- Aspose.CAD-biblioteket tillagt i ditt projekt. Du kan ladda ner det från [Aspose.CAD download page](https://releases.aspose.com/cad/net/).
- En exempel‑DWG‑fil, t.ex. **Bottom_plate.dwg**, att följa med.

## Importera namnrymder

Lägg till de nödvändiga `using`-direktiven högst upp i din C#-fil så att kompilatorn kan hitta Aspose.CAD-typerna.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.FileFormats.Cad;
```

Nu när miljön är klar, låt oss gå igenom implementeringen steg för steg.

## Hur skapar man viewport dwg c#?

För att skapa en anpassad viewport, läs först in DWG-filen i ett `CadImage`-objekt, konfigurera sedan `CadRasterizationOptions` med önskad layout och skalning. Definiera regionen du vill visa, skapa en `CadVportTableObject` med beräknat centrum, höjd och bildförhållande, ersätt den aktiva viewporten, ange eventuella PDF-alternativ och spara slutligen resultatet.

## Step 1: läs in dwg-filen

`CadImage.Load` läser in en DWG-fil i ett `CadImage`-objekt, som representerar CAD-ritningen i minnet.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for loading the DWG file goes here.
}
```

## Step 2: konfigurera rasteriseringsalternativ

`CadRasterizationOptions` anger hur CAD-ritningen rasteriseras, inklusive layoutval, skalning och utskriftsstorlek.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };
rasterizationOptions.NoScaling = true;
// Additional rasterization configurations can be added here.
```

## Step 3: definiera region att rita

`Point` definierar X- och Y-koordinaterna för det övre vänstra hörnet av regionen som ska renderas.

```csharp
Point topLeft = new Point(6156, 7053);
double width = 3108;
double height = 2489;
```

## Step 4: skapa en ny viewport

`CadVportTableObject` representerar ett viewport-objekt som styr det synliga området och bildförhållandet för den renderade ritningen.

```csharp
CadVportTableObject newView = new CadVportTableObject();
newView.Name.Value = "*Active";
newView.CenterPoint.X = topLeft.X + width / 2f;
newView.CenterPoint.Y = topLeft.Y - height / 2f;
newView.ViewHeight.Value = height;
newView.ViewAspectRatio.Value = width / height;
```

## Step 5: ersätt aktiv viewport

Loopen ersätter den aktiva viewporten med den nyss skapade för att tillämpa de anpassade vyinställningarna.

```csharp
for (int i = 0; i < cadImage.ViewPorts.Count; i++)
{
    CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
    if ((currentView.Name.Value == null && cadImage.ViewPorts.Count == 1) ||
    string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
    {
        cadImage.ViewPorts[i] = newView;
        break;
    }
}
```

## Step 6: konfigurera PDF-alternativ

`PdfOptions` konfigurerar PDF-utdata parametrar såsom komprimering och metadata.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Step 7: spara den renderade dwg som PDF

`image.Save` skriver den renderade bilden till en fil med de angivna formatalternativen.

```csharp
cadImage.Save(MyDir, pdfOptions);
```

## Varför använda en anpassad viewport vid rendering av DWG?

En anpassad viewport låter dig isolera en specifik layout eller region, vilket minskar filstorleken och förbättrar renderingshastigheten. Aspose.CAD kan rendera en 300‑sidig DWG på under 2 sekunder när en fokuserad viewport används, jämfört med rendering av hela ritningen som kan ta flera sekunder längre.

## Vanliga problem och lösningar

- **Blank output** – Se till att viewportkoordinaterna ligger inom ritningens gränser; använd `CadImage.Size` för att verifiera gränserna.
- **Missing layers** – Ställ in `CadRasterizationOptions.Layouts` till rätt layoutnamn; annars kan standardlayouten vara tom.
- **Performance slowdown** – Inaktivera anti‑aliasing i `CadRasterizationOptions` om du bara behöver en snabb förhandsgranskning.

## Vanliga frågor

### Q1: Kan jag använda Aspose.CAD med andra CAD-filformat?

A1: Ja, Aspose.CAD stöder olika format, inklusive DWG, DXF, DWF och mer än 20 ytterligare CAD-typer.

### Q2: Är Aspose.CAD kompatibel med .NET Core?

A2: Ja, Aspose.CAD fungerar med .NET Framework, .NET Core och de senaste .NET-utgåvorna.

### Q3: Hur kan jag hantera olika layouter i en DWG-fil?

A3: Ange önskad layout med `Layouts`-egenskapen i `CadRasterizationOptions` innan rendering.

### Q4: Finns det licensieringsaspekter för att använda Aspose.CAD?

A4: För licensinformation, besök [Aspose.CAD licensing page](https://purchase.aspose.com/buy).

### Q5: Var kan jag hitta ytterligare support?

A5: Besök [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) för gemenskapsstöd och diskussioner.

### Q6: Kan jag rendera direkt till PNG istället för PDF?

A6: Ja, ändra `PdfOptions` till `PngOptions` och anropa `image.Save("output.png", pngOptions)`.

### Q7: Hur bäddar jag in den renderade bilden i en Windows Forms-applikation?

A7: Läs in den sparade bilden i en `PictureBox`-kontroll med `Image.FromFile("output.png")`.

## Slutsats

Du vet nu hur du **create viewport dwg c#** och renderar en DWG-fil till PDF (eller andra rasterformat) med Aspose.CAD. Genom att behärska viewport-manipulering får du fin‑granulär kontroll över den visuella utskriften, vilket är avgörande för att skapa exakta ingenjörsritningar, rapporter eller miniatyrbilder. Utforska ytterligare rasteriseringsinställningar, experimentera med olika utskriftsformat och integrera koden i större .NET‑tjänster eller skrivbordsverktyg.

---

**Senast uppdaterad:** 2026-08-23  
**Testad med:** Aspose.CAD 24.11 for .NET  
**Författare:** Aspose

## Relaterade handledningar

- [Hur man ställer in viewport vid konvertering av DWG till PDF med koordinater i C# - Aspose.CAD Tutorial](/cad/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/)
- [Lär dig att ställa in CAD rasteriseringsalternativ – Exportera specifika layouter till PDF med Aspose.CAD](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)
- [Hur man konverterar DWG till PDF och rasterbilder med Aspose.CAD för .NET](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}