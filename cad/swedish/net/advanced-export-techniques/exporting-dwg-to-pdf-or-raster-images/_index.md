---
title: Exportera DWG till PDF eller rasterbilder - Aspose.CAD Guide
linktitle: Exportera DWG till PDF eller rasterbilder
second_title: Aspose.CAD .NET - CAD- och BIM-filformat
description: Utforska en omfattande guide för att exportera DWG till PDF eller rasterbilder med Aspose.CAD för .NET. Lär dig stegen, förutsättningarna och kom igång med detta kraftfulla bibliotek.
weight: 11
url: /sv/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportera DWG till PDF eller rasterbilder - Aspose.CAD Guide

## Introduktion

Vill du sömlöst konvertera DWG-filer till PDF- eller rasterbilder i ditt .NET-program? Kolla inte vidare! Denna steg-för-steg-guide kommer att leda dig genom processen med det kraftfulla Aspose.CAD för .NET-biblioteket. Oavsett om du är en erfaren utvecklare eller precis har börjat, vänder sig den här handledningen till alla färdighetsnivåer.

## Förutsättningar

Innan vi dyker in i handledningen, se till att du har följande på plats:

- En grundläggande förståelse för .NET-programmering.
-  Aspose.CAD för .NET-biblioteket installerat. Om inte, ladda ner den[här](https://releases.aspose.com/cad/net/).
- Din favorit integrerade utvecklingsmiljö (IDE) inställd för .NET-utveckling.

## Importera namnområden

Låt oss kicka igång genom att importera de nödvändiga namnrymden i ditt .NET-projekt. Detta säkerställer att du har tillgång till Aspose.CAD-funktionen i din kod.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
```

## Steg 1: Ladda DWG-fil

Börja med att ladda DWG-filen du vill konvertera. Ersätt "Din dokumentkatalog" med sökvägen till din DWG-fil.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Din kod för att ladda DWG går här
}
```

## Steg 2: Ställ in PDF-export

Låt oss nu konfigurera PDF-exportinställningarna. Det här exemplet visar hur man ställer in layouten och hanterar enhetsomvandlingar.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };

// Kontrollera och definiera enhetssystemet
bool currentUnitIsMetric = false;
double currentUnitCoefficient = 1.0;
DefineUnitSystem(cadImage.UnitType, out currentUnitIsMetric, out currentUnitCoefficient);

// Din kod för att ställa in PDF-export går här
```

## Steg 3: Exportera till PDF

Utför exporten till PDF med de konfigurerade inställningarna.

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath, pdfOptions);
```

## Steg 4: Exportera till rasterbilder

Utöka funktionaliteten för att exportera till rasterbilder, till exempel PNG.

```csharp
// A4-storlek vid 300 DPI - 2480 x 3508
rasterizationOptions.PageHeight = 3508;
rasterizationOptions.PageWidth = 2480;

PngOptions pngOptions = new PngOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath.Replace("pdf", "png"), pngOptions);
```

## Slutsats

Grattis! Du har framgångsrikt lärt dig hur du använder Aspose.CAD för .NET för att exportera DWG-filer till både PDF- och rasterbilder. Detta kraftfulla bibliotek effektiviserar processen, vilket gör den effektiv och utvecklarvänlig.

## FAQ's

### F1: Kan jag använda Aspose.CAD för .NET i mina kommersiella projekt?

 A1: Ja, det kan du. Besök[buy.aspose.com/buy](https://purchase.aspose.com/buy) för licensinformation.

### F2: Finns det en gratis provperiod?

 A2: Visst! Ta din gratis provperiod[här](https://releases.aspose.com/).

### F3: Hur kan jag få support för Aspose.CAD för .NET?

 A3: Gå över till[Aspose.CAD-forum](https://forum.aspose.com/c/cad/19) för samhällsstöd.

### F4: Kan jag få en tillfällig licens för teständamål?

 A4: Ja, du kan få en tillfällig licens[här](https://purchase.aspose.com/temporary-license/).

### F5: Var kan jag hitta den detaljerade dokumentationen?

 S5: Dokumentationen finns tillgänglig på[Aspose.CAD](https://reference.aspose.com/cad/net/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
