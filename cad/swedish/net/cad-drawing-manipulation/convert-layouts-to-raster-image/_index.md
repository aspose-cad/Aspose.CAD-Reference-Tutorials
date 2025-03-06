---
title: Konvertera layouter till rasterbild i Aspose.CAD för .NET
linktitle: Konvertera layouter till rasterbild
second_title: Aspose.CAD .NET - CAD- och BIM-filformat
description: Konvertera enkelt CAD-layouter till rasterbilder med Aspose.CAD för .NET. Förbättra din utveckling med kraftfulla CAD-manipuleringsmöjligheter.
weight: 12
url: /sv/net/cad-drawing-manipulation/convert-layouts-to-raster-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konvertera layouter till rasterbild i Aspose.CAD för .NET

## Introduktion

Vill du enkelt konvertera layouter till rasterbilder i dina .NET-applikationer? Kolla inte vidare! Denna steg-för-steg guide kommer att leda dig genom processen med Aspose.CAD för .NET, ett kraftfullt bibliotek som förenklar datorstödd design (CAD) uppgifter.

## Förutsättningar

Innan du dyker in i handledningen, se till att du har följande förutsättningar på plats:

- Aspose.CAD för .NET Library: Ladda ner och installera biblioteket från[Aspose.CAD för .NET nedladdningssida](https://releases.aspose.com/cad/net/).

- Utvecklingsmiljö: Se till att du har en fungerande .NET-utvecklingsmiljö inställd på din maskin.

- Dokument att konvertera: Förbered ett CAD-dokument som innehåller de layouter du vill konvertera till rasterbilder.

- Din dokumentkatalog: Ersätt platshållaren "Din dokumentkatalog" i koden med sökvägen till din dokumentkatalog.

## Importera namnområden

Låt oss först importera de nödvändiga namnrymden för att göra Aspose.CAD-funktionerna tillgängliga i din kod.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Steg 1: Ladda CAD-dokumentet

Börja med att ladda CAD-dokumentet med Aspose.CAD-biblioteket.

```csharp
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image image = Image.Load(sourceFilePath))
{
    //Din kod för ytterligare steg kommer här
}
```

## Steg 2: Konfigurera rasteriseringsalternativ

 Skapa en instans av`CadRasterizationOptions` för att ställa in sidbredd, höjd och ange de layouter du vill konvertera.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1200;
rasterizationOptions.PageHeight = 1200;
rasterizationOptions.Layouts = new string[] { "Model", "Layout1" };
```

## Steg 3: Ställ in TiffOptions för den resulterande bilden

 Skapa en instans av`TiffOptions`för att definiera formatet för den resulterande bilden.

```csharp
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.VectorRasterizationOptions = rasterizationOptions;
```

## Steg 4: Spara den resulterande bilden

Ange utdatasökvägen och spara den konverterade bilden.

```csharp
string outputFilePath = MyDir + "conic_pyramid_layoutstorasterimage_out.tiff";
image.Save(outputFilePath, options);
```

## Slutsats

Grattis! Du har framgångsrikt konverterat CAD-layouter till ett rasterbildsformat med Aspose.CAD för .NET. Möjligheterna är stora, och den här guiden fungerar som en startpunkt för dina CAD-relaterade ansträngningar.

## FAQ's

### F1: Är Aspose.CAD kompatibel med alla CAD-format?

 S1: Aspose.CAD stöder ett brett utbud av CAD-format, inklusive DWG, DXF, DWF, STL och mer. Kolla[dokumentation](https://reference.aspose.com/cad/net/) för en omfattande lista.

### F2: Hur kan jag få en tillfällig licens för Aspose.CAD?

 A2: Besök[sida för tillfällig licens](https://purchase.aspose.com/temporary-license/) att förvärva en tillfällig licens för test- och utvärderingsändamål.

### F3: Var kan jag hitta support för Aspose.CAD?

 S3: Forum är ett bra ställe att söka hjälp. Besök[Aspose.CAD-forum](https://forum.aspose.com/c/cad/19) att få kontakt med samhället och få hjälp.

### F4: Kan jag prova Aspose.CAD gratis?

 A4: Absolut! Ta din[gratis provperiod](https://releases.aspose.com/) för att utforska funktionerna och funktionerna i Aspose.CAD.

### F5: Var kan jag köpa en licens för Aspose.CAD?

 A5: Navigera till[köpsidan](https://purchase.aspose.com/buy) att köpa en licens och låsa upp den fulla potentialen hos Aspose.CAD.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
