---
title: Konvertera DWG till Compliance PDF - Aspose.CAD Tutorial
linktitle: Konvertera DWG till Compliance PDF
second_title: Aspose.CAD .NET - CAD- och BIM-filformat
description: Konvertera DWG till Compliance PDF med Aspose.CAD för .NET. Följ vår handledning för steg-för-steg-vägledning.
type: docs
weight: 13
url: /sv/net/conversion-and-export/converting-dwg-to-compliance-pdf/
---
## Introduktion

Välkommen till vår steg-för-steg handledning om att konvertera DWG-filer till Compliance PDF med Aspose.CAD för .NET. Aspose.CAD är ett kraftfullt .NET API som gör det möjligt för utvecklare att arbeta med CAD-filformat utan ansträngning. I den här handledningen guidar vi dig genom processen att konvertera en DWG-fil till Compliance PDF med detaljerade exempel och förklaringar.

## Förutsättningar

Innan vi börjar, se till att du har följande förutsättningar på plats:

-  Aspose.CAD för .NET: Se till att du har Aspose.CAD-biblioteket integrerat i ditt .NET-projekt. Du kan ladda ner den[här](https://releases.aspose.com/cad/net/).

- Utvecklingsmiljö: Ha en fungerande .NET-utvecklingsmiljö installerad och se till att den är korrekt konfigurerad.

- DWG-exempelfil: Ladda ner en DWG-exempelfil som du vill konvertera till Compliance PDF.

## Importera namnområden

I ditt .NET-projekt, importera de nödvändiga namnrymden för att använda Aspose.CAD-funktioner.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

Låt oss nu dela upp processen att konvertera en DWG-fil till Compliance PDF i flera steg.

## Steg 1: Ladda DWG-filen

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

Aspose.CAD.Image cadImage = Aspose.CAD.Image.Load(sourceFilePath);
```

## Steg 2: Ställ in rasteriseringsalternativ

 Skapa en instans av`CadRasterizationOptions` och konfigurera dess egenskaper, såsom bakgrundsfärg, sidbredd och sidhöjd.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions
{
    BackgroundColor = Aspose.CAD.Color.White,
    PageWidth = 1600,
    PageHeight = 1600
};
```

## Steg 3: Skapa PDF-alternativ

 Skapa en instans av`PdfOptions` och ställ in vektorrasteriseringsalternativen.

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions,
    CorePdfOptions = new PdfDocumentOptions { Compliance = PdfCompliance.PdfA1a }
};
```

## Steg 4: Spara som PDF (A1a-överensstämmelse)

Spara CAD-bilden som Compliance PDF med A1a-kompatibilitet.

```csharp
cadImage.Save(MyDir + "PDFA1_A.pdf", pdfOptions);
```

## Steg 5: Spara som PDF (A1b-överensstämmelse)

Ändra överensstämmelsetypen till A1b och spara CAD-bilden som överensstämmelse-PDF.

```csharp
pdfOptions.CorePdfOptions.Compliance = PdfCompliance.PdfA1b;
cadImage.Save(MyDir + "PDFA1_B.pdf", pdfOptions);
```

## Slutsats

Grattis! Du har framgångsrikt konverterat en DWG-fil till Compliance PDF med Aspose.CAD för .NET. Denna handledning ger en omfattande guide för utvecklare som vill integrera CAD-konverteringsfunktioner i sina applikationer.

## FAQ's

### F1: Kan jag konvertera andra CAD-format till Compliance PDF med Aspose.CAD?

S1: Ja, Aspose.CAD stöder olika CAD-format, vilket möjliggör konvertering till Compliance PDF.

### F2: Är Aspose.CAD kompatibel med .NET Core?

S2: Ja, Aspose.CAD är kompatibel med både .NET Framework och .NET Core.

### F3: Finns det några licensalternativ för Aspose.CAD?

 S3: Ja, du kan utforska licensalternativ[här](https://purchase.aspose.com/buy).

### F4: Finns det en gratis provperiod?

 A4: Ja, du kan få en gratis provperiod[här](https://releases.aspose.com/).

### F5: Var kan jag få support för Aspose.CAD?

 A5: Besök[Aspose.CAD-forum](https://forum.aspose.com/c/cad/19) för alla supportrelaterade frågor.