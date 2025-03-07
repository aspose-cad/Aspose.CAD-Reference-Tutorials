---
title: Lägga till vattenstämplar till CAD-ritningar - Aspose.CAD Guide
linktitle: Lägga till vattenstämplar till CAD-ritningar
second_title: Aspose.CAD .NET - CAD- och BIM-filformat
description: Förbättra dina CAD-ritningar med professionella vattenstämplar med Aspose.CAD för .NET. Följ vår steg-för-steg-guide för personliga och engagerande design.
weight: 11
url: /sv/net/plt-and-watermarking/adding-watermarks-to-cad-drawings/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Lägga till vattenstämplar till CAD-ritningar - Aspose.CAD Guide

## Introduktion

Vill du förbättra dina CAD-ritningar genom att lägga till professionella vattenstämplar? Aspose.CAD för .NET ger en robust lösning för att sömlöst integrera vattenstämplar i dina CAD-filer. I den här steg-för-steg-guiden går vi igenom processen att lägga till vattenstämplar med Aspose.CAD, vilket säkerställer att dina ritningar inte bara förmedlar viktig information utan också bär ditt unika märke.

## Förutsättningar

Innan du dyker in i handledningen, se till att du har följande:
-  Aspose.CAD för .NET: Se till att du har Aspose.CAD-biblioteket installerat. Du kan ladda ner den[här](https://releases.aspose.com/cad/net/).
- Din dokumentkatalog: Skapa en katalog för att lagra dina CAD-ritningar.
Låt oss nu börja med att lägga till vattenstämplar i dina CAD-ritningar!

## Importera namnområden

Börja med att importera de nödvändiga namnrymden till ditt .NET-projekt:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Steg 1: Ladda CAD-ritningen

```csharp
// Sökvägen till dokumentkatalogen.
string MyDir = "Your Document Directory";
using (CadImage cadImage = (CadImage)Image.Load(MyDir + "Drawing11.dwg")) {
```

## Steg 2: Lägg till vattenstämpel som MTEXT

```csharp
// Lägg till ny MTEXT
CadMText watermark = new CadMText();
watermark.Text = "Watermark message";
watermark.InitialTextHeight = 40;
watermark.InsertionPoint = new Cad3DPoint(300, 40);
watermark.LayerName = "0";
cadImage.BlockEntities["*Model_Space"].AddEntity(watermark);
```

## Steg 3: Eller lägg till vattenstämpel som text

```csharp
// Alternativt kan du lägga till en enklare enhet som Text
CadText text = new CadText();
text.DefaultValue = "Watermark text";
text.TextHeight = 40;
text.FirstAlignment = new Cad3DPoint(300, 40);
text.LayerName = "0";
cadImage.BlockEntities["*Model_Space"].AddEntity(text);
```

## Steg 4: Exportera till PDF

```csharp
// Exportera CAD-ritningen med vattenstämpel till PDF
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.Layouts = new[] { "Model" };
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
cadImage.Save(MyDir + "AddWatermark_out.pdf", pdfOptions);
```

Upprepa dessa steg för olika ritningar, så får du professionellt utseende vattenmärkta CAD-filer på nolltid!

## Slutsats

Grattis! Du har framgångsrikt lärt dig hur du lägger till vattenstämplar i dina CAD-ritningar med Aspose.CAD för .NET. Denna enkla men kraftfulla process låter dig anpassa dina mönster samtidigt som integriteten hos dina tekniska ritningar bibehålls.

## FAQ's

### F1: Kan jag anpassa utseendet på vattenstämpeln?

S1: Ja, du kan anpassa texten, teckensnittet, storleken och placeringen av vattenstämpeln enligt dina önskemål.

### F2: Är Aspose.CAD kompatibel med olika CAD-filformat?

S2: Aspose.CAD stöder olika CAD-filformat, inklusive DWG och DXF, vilket säkerställer bred kompatibilitet.

### F3: Kan jag lägga till flera vattenstämplar i en enda CAD-ritning?

A3: Absolut! Du kan lägga till så många vattenstämplar som behövs, vilket ger flexibilitet för olika användningsfall.

### F4: Erbjuder Aspose.CAD en gratis provperiod?

S4: Ja, du kan utforska Aspose.CAD:s funktioner med en gratis provperiod. Förstår[här](https://releases.aspose.com/).

### F5: Var kan jag hitta support för Aspose.CAD?

 S5: För eventuella frågor eller hjälp, besök[Aspose.CAD-forum](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
