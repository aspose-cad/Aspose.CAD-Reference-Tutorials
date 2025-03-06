---
title: Skapa en enda PDF med olika layouter - Aspose.CAD Guide
linktitle: Skapa en enda PDF med olika layouter
second_title: Aspose.CAD .NET - CAD- och BIM-filformat
description: Skapa en enda PDF med olika layouter med Aspose.CAD för .NET. Följ vår steg-för-steg-guide för sömlös integration och effektiv PDF-generering.
weight: 13
url: /sv/net/advanced-cad-techniques/creating-single-pdf-with-different-layouts/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Skapa en enda PDF med olika layouter - Aspose.CAD Guide

## Introduktion

Vill du skapa ett enda PDF-dokument från en CAD-ritning med olika layouter med Aspose.CAD för .NET? Den här steg-för-steg-guiden leder dig genom processen och hjälper dig att uppnå sömlös integrering och effektivt skapande av PDF. Aspose.CAD för .NET tillhandahåller kraftfulla funktioner för att manipulera CAD-ritningar programmatiskt, och i denna handledning kommer vi att fokusera på att skapa en enda PDF-fil med olika layouter.

## Förutsättningar

Innan du dyker in i handledningen, se till att du har följande förutsättningar:

-  Aspose.CAD för .NET: Se till att du har Aspose.CAD för .NET installerat. Du kan ladda ner den från[här](https://releases.aspose.com/cad/net/).

- Utvecklingsmiljö: Sätt upp en .NET-utvecklingsmiljö och ha en grundläggande förståelse för C#-programmering.

## Importera namnområden

ditt C#-projekt, inkludera de nödvändiga namnrymden för att utnyttja funktionerna i Aspose.CAD för .NET:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Steg 1: Ladda CAD-bilden

```csharp
// Sökvägen till dokumentkatalogen.
string MyDir = "Your Document Directory";

using (CadImage cadImage = (CadImage)Image.Load(MyDir + "City skyway map.dwg"))
{
    // Din kod för steg 1 kommer här
}
```

## Steg 2: Anpassa rasteriseringsalternativ

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1000;
rasterizationOptions.PageHeight = 1000;

// Anpassade storlekar för flera layouter
rasterizationOptions.LayoutPageSizes.Add("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.LayoutPageSizes.Add("8.5 x 11 Plot", new SizeF(1000, 100));
```

## Steg 3: Definiera PDF-alternativ

```csharp
PdfOptions pdfOptions = new PdfOptions() { VectorRasterizationOptions = rasterizationOptions };
```

## Steg 4: Spara som PDF

```csharp
cadImage.Save(MyDir + "singlePDF_out.pdf", pdfOptions);
```

Nu har du framgångsrikt skapat ett enda PDF-dokument med olika layouter med Aspose.CAD för .NET. Utforska gärna fler funktioner och anpassa koden efter dina specifika krav.

## Slutsats

I den här handledningen täckte vi processen att skapa en enda PDF från en CAD-ritning med olika layouter med Aspose.CAD för .NET. Detta kraftfulla bibliotek förenklar CAD-manipulationsuppgifter och erbjuder flexibilitet för olika scenarier.

## FAQ's

### F1: Kan jag använda Aspose.CAD för .NET med andra CAD-format?

S1: Ja, Aspose.CAD för .NET stöder olika CAD-format som DWG, DXF, DGN och mer.

### F2: Finns det en gratis provperiod?

 A2: Ja, du kan utforska en gratis provperiod[här](https://releases.aspose.com/).

### F3: Hur kan jag få support för Aspose.CAD för .NET?

 A3: Besök[Aspose.CAD-forum](https://forum.aspose.com/c/cad/19) för samhällsstöd.

### F4: Var kan jag hitta detaljerad dokumentation?

 S4: Se dokumentationen[här](https://reference.aspose.com/cad/net/).

### F5: Kan jag köpa en licens för Aspose.CAD för .NET?

 A5: Ja, du kan köpa en licens[här](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
