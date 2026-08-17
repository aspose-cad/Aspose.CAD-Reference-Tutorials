---
date: 2026-08-17
description: Lär dig hur du lägger till image i dwg-filer med C# och Aspose.CAD för
  .NET. Denna guide går igenom import av images, inställning av infogningspunkter
  och export till PDF.
keywords:
- add image to dwg
- convert dwg to pdf
- set insertion point dwg
- embed png in dwg
- save dwg as pdf
lastmod: 2026-08-17
linktitle: Import av Images i DWG-filer med C#
og_description: Lär dig hur du lägger till image i dwg-filer med C#. Denna handledning
  täcker import av images, inställning av infogningspunkter och konvertering av dwg
  till pdf med Aspose.CAD.
og_image_alt: Guide showing C# code to embed an image into a DWG file using Aspose.CAD
og_title: Hur man lägger till image i dwg-filer med C# och Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-08-17'
  description: Learn how to add image to dwg files using C# and Aspose.CAD for .NET.
    This guide walks you through importing images, setting insertion points, and exporting
    to PDF.
  headline: How to add image to dwg files with C# using Aspose.CAD
  type: TechArticle
- description: Learn how to add image to dwg files using C# and Aspose.CAD for .NET.
    This guide walks you through importing images, setting insertion points, and exporting
    to PDF.
  name: How to add image to dwg files with C# using Aspose.CAD
  steps:
  - name: set up your document directory
    text: Prepare the folder that contains the source DWG and the image you want to
      embed.
  - name: load the dwg file
    text: The `CadImage` class represents a DWG drawing and provides access to its
      entities, layers, and metadata.
  - name: define the image properties
    text: Create an `Image` object that points to the raster file (e.g., PNG) and
      specify its format.
  - name: set insertion point dwg and vectors
    text: Specify where the image should appear inside the drawing and how it should
      be scaled. The insertion point is defined by a 2‑D coordinate, while the vectors
      control width and height.
  - name: create and configure the raster image
    text: Instantiate a `RasterImage` object, assign the image data, and set any additional
      rendering options.
  - name: add image to dwg file
    text: Insert the configured raster image into the DWG’s entities collection so
      it becomes part of the drawing.
  - name: save as pdf (export dwg to pdf)
    text: After embedding the image you can **convert dwg to pdf** or **save dwg as
      pdf** with a single call. This is useful for sharing the drawing with stakeholders
      who don’t have CAD software.
  type: HowTo
- questions:
  - answer: The core library is .NET‑specific, but Aspose offers equivalent APIs for
      Java, Python and other platforms.
    question: Can I use Aspose.CAD for .NET with other programming languages?
  - answer: Yes, you can explore a free trial on the [Aspose free trial page](https://releases.aspose.com/).
    question: Is a free trial available for Aspose.CAD?
  - answer: The documentation is available in the [Aspose.CAD .NET API reference](https://reference.aspose.com/cad/net/).
    question: Where can I find detailed documentation for Aspose.CAD?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to get a temporary license.
    question: How do I obtain a temporary license for Aspose.CAD?
  - answer: Yes, you can seek support and engage with the community in the [Aspose.CAD
      community forum](https://forum.aspose.com/c/cad/19).
    question: Are there community forums for Aspose.CAD support?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- CAD
- Aspose.CAD
- C# image processing
- DWG manipulation
title: Hur man lägger till image i dwg-filer med C# och Aspose.CAD
url: /sv/net/image-manipulation-and-rendering/importing-images-into-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hur man lägger till bild i dwg-filer med C# och Aspose.CAD

## Introduktion

Att lägga till en bild i en DWG-fil är ett vanligt krav när du behöver berika CAD-ritningar med logotyper, foton eller rastergrafik. I den här handledningen kommer du att lära dig hur du **lägger till bild i dwg** programatiskt med C# och Aspose.CAD för .NET, och sedan eventuellt konvertera resultatet till PDF. Stegen är uppdelade så att du kan kopiera‑klistra varje avsnitt i ditt eget projekt.

## Snabba svar
- **Vilket bibliotek hanterar uppgiften?** Aspose.CAD för .NET.
- **Kan jag bädda in PNG-filer?** Ja – PNG, JPEG, BMP och andra rasterformat stöds.
- **Behöver jag en licens för utveckling?** En gratis provversion fungerar för testning; en kommersiell licens krävs för produktion.
- **Stöds PDF-export?** Absolut – du kan konvertera den uppdaterade DWG till PDF med en rad.
- **Vilka .NET-versioner är kompatibla?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7.

## Vad är en DWG-fil?

En DWG-fil är det inhemska binära formatet för Autodesk AutoCAD-ritningar, som lagrar vektorgrafik, lager och metadata. Den används i stor utsträckning inom arkitektur, ingenjörsvetenskap och byggnation, och Aspose.CAD kan läsa och skriva detta format utan att AutoCAD behöver vara installerat.

## Varför lägga till bild i dwg med Aspose.CAD?

Aspose.CAD stöder **50+ in- och utdataformat**, kan bearbeta filer större än 500 MB utan att ladda hela dokumentet i minnet, och erbjuder ett deterministiskt API som fungerar i huvudlösa servermiljöer. Detta gör massbearbetning av DWG-ritningar snabb och pålitlig.

## Förutsättningar
- Grundläggande kunskap i C#-programmering.
- Aspose.CAD för .NET installerat. Du kan ladda ner det från [Aspose.CAD för .NET nedladdningssida](https://releases.aspose.com/cad/net/). Du kan också utforska andra Aspose-produkter på [Aspose releases-sidan](https://releases.aspose.com/).
- En utvecklingsmiljö som Visual Studio 2022 eller senare.

## Hur man lägger till bild i dwg med Aspose.CAD?

Läs in mål‑DWG, skapa ett rasterbildobjekt som beskriver bilden du vill bädda in, ange infogningspunkten och skalningsvektorerna, och fäst sedan bilden i ritningen. Slutligen sparar du den modifierade DWG:n eller exporterar den direkt till PDF. Hela arbetsflödet kräver bara några API‑anrop och körs på under en sekund för typiska tvåsidiga ritningar.

### Importera namnrymder
Inkludera namnrymderna som exponerar de CAD-klasser du kommer att behöva.

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

### Steg 1: konfigurera din dokumentkatalog
Förbered mappen som innehåller käll‑DWG:n och bilden du vill bädda in.

```csharp
string MyDir = "Your Document Directory";
```

### Steg 2: läs in dwg-filen
`CadImage`-klassen representerar en DWG-ritning och ger åtkomst till dess entiteter, lager och metadata.

```csharp
string dwgPathToFile = MyDir + "Drawing11.dwg";
CadImage cadImage1 = (CadImage)Image.Load(dwgPathToFile);
```

### Steg 3: definiera bildens egenskaper
Skapa ett `Image`-objekt som pekar på rasterfilen (t.ex. PNG) och ange dess format.

```csharp
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.ObjectHandle = "A3B4";
```

### Steg 4: ange infogningspunkt för dwg och vektorer
Ange var bilden ska visas i ritningen och hur den ska skalas. Infogningspunkten definieras av en 2‑D-koordinat, medan vektorerna styr bredd och höjd.

```csharp
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

### Steg 5: skapa och konfigurera rasterbilden
Instansiera ett `RasterImage`-objekt, tilldela bilddata och ange eventuella ytterligare renderingsalternativ.

```csharp
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.ImageDefReference = "A3B4";
cadRasterImage.DisplayFlags = 7;
cadRasterImage.ClippingState = 0;
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(639.5, 561.5));
```

### Steg 6: lägg till bild i dwg-fil
Infoga den konfigurerade rasterbilden i DWG:s entitetskollektion så att den blir en del av ritningen.

```csharp
CadImage cadImage = (CadImage)cadImage1;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadRasterImage);

List<CadBaseObject> list = new List<CadBaseObject>(cadImage.Objects);
list.Add(cadRasterImageDef);
cadImage.Objects = list.ToArray();
```

### Steg 7: spara som pdf (exportera dwg till pdf)
Efter att ha bäddat in bilden kan du **konvertera dwg till pdf** eller **spara dwg som pdf** med ett enda anrop. Detta är användbart för att dela ritningen med intressenter som inte har CAD‑programvara.

```csharp
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;

cadRasterizationOptions.PageHeight = 1600;
cadRasterizationOptions.PageWidth = 1600;
cadRasterizationOptions.Layouts = new string[] { "Model" };
cadImage1.Save(MyDir + "export2.pdf", pdfOptions);
```

## Hur man konverterar dwg till pdf efter att ha bäddat in en bild?

Anropa `Save`‑metoden på `CadImage`‑instansen, skicka `SaveFormat.Pdf` och eventuellt ett `PdfOptions`‑objekt för att styra sidstorlek, rasterisering och metadata. Aspose.CAD bevarar den inbäddade rasterbilden, lager och linjebredder, och skapar en trogen PDF‑representation som kan öppnas i vilken visare som helst. Denna konvertering utförs med en enda kodrad.

## Vanliga problem och lösningar
- **Bilden visas på fel plats** – dubbelkolla infogningspunktens koordinater och riktningsvektorerna; de är relativa till ritningens ursprung.
- **Stora bilder orsakar minnesspikar** – använd `Resize`‑alternativet på rasterbilden före infogning, eller arbeta med en lägre upplösningskopia.
- **PDF‑export förlorar vektor­kvalitet** – se till att du sparar med `PdfOptions` som behåller vektordata; rasterbilder är alltid inbäddade som de är.

## Vanliga frågor

**Q: Kan jag använda Aspose.CAD för .NET med andra programmeringsspråk?**  
A: Kärnbiblioteket är .NET‑specifikt, men Aspose erbjuder motsvarande API:er för Java, Python och andra plattformar.

**Q: Finns en gratis provversion för Aspose.CAD?**  
A: Ja, du kan utforska en gratis provversion på [Aspose provversionssida](https://releases.aspose.com/).

**Q: Var kan jag hitta detaljerad dokumentation för Aspose.CAD?**  
A: Dokumentationen finns i [Aspose.CAD .NET API-referens](https://reference.aspose.com/cad/net/).

**Q: Hur får jag en tillfällig licens för Aspose.CAD?**  
A: Besök [tillfällig licenssida](https://purchase.aspose.com/temporary-license/) för att få en tillfällig licens.

**Q: Finns det community-forum för Aspose.CAD‑support?**  
A: Ja, du kan söka support och engagera dig med communityn i [Aspose.CAD community-forum](https://forum.aspose.com/c/cad/19).

---

**Last Updated:** 2026-08-17  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose

## Relaterade handledningar

- [Exportera DWG till PDF eller rasterbilder - Aspose.CAD Guide](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [Exportera DWG till DXF-format i C# - Aspose.CAD Tutorial](/cad/net/advanced-export-techniques/exporting-dwg-to-dxf/)
- [Exportera specifika layouter till PDF - Aspose.CAD Guide](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}