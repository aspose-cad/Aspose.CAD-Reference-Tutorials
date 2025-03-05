---
title: Exportera CAD-layouter till rasterbildsformat i Aspose.CAD för .NET
linktitle: Exportera CAD-layouter till rasterbildsformat
second_title: Aspose.CAD .NET - CAD- och BIM-filformat
description: Lär dig hur du exporterar CAD-layouter till rasterbilder med Aspose.CAD för .NET. Följ vår steg-för-steg-guide för sömlös konvertering.
type: docs
weight: 10
url: /sv/net/cad-export-formats/export-cad-layouts-to-raster-image-formats/
---
## Introduktion

Letar du efter att effektivt konvertera CAD-layouter till rasterbildsformat med Aspose.CAD för .NET? Den här steg-för-steg-guiden leder dig genom processen och ger detaljerade instruktioner och kodavsnitt för att göra uppgiften sömlös. Oavsett om du är en erfaren utvecklare eller en nykomling på Aspose.CAD, vänder sig denna handledning till alla nivåer av expertis.

## Förutsättningar

Innan du dyker in i handledningen, se till att du har följande:

- Aspose.CAD för .NET Library: Se till att du har Aspose.CAD-biblioteket installerat. Om inte kan du ladda ner den från[Aspose.CAD webbplats](https://releases.aspose.com/cad/net/).

- CAD-ritningsfil: Förbered en CAD-ritningsfil (t.ex. conic_pyramid.dxf) som du vill konvertera till rasterbildsformat.

## Importera namnområden

I ditt .NET-projekt, importera de nödvändiga namnrymden för att utnyttja Aspose.CAD-funktionerna. Inkludera följande namnrymder i början av koden:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Steg 1: Ladda CAD-ritning

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

// Ladda en CAD-ritning i en instans av Image
using (var image = Image.Load(sourceFilePath))
{
    // Din kod för att ladda CAD-ritningen går här
}
```

## Steg 2: Skapa CadRasterizationOptions

```csharp
// Skapa en instans av CadRasterizationOptions
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
```

## Steg 3: Ange lager

```csharp
// Lägg till lagernamnet i CadRasterizationOptions lagerlista
rasterizationOptions.Layers = new string[] { "LayerA" };
```

## Steg 4: Skapa JpegOptions

```csharp
// Skapa en instans av JpegOptions (eller andra ImageOptions för rasterformat)
var options = new JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
```

## Steg 5: Exportera till Jpeg-format

```csharp
// Exportera varje lager till Jpeg-format
MyDir = MyDir + "CADLayersToRasterImageFormats_out.jpg";
image.Save(MyDir, options);
```

## Ytterligare steg: Konvertera alla lager

Om du vill konvertera alla lager, använd följande metod:

```csharp
ConvertAllLayersToRasterImageFormats();
```

Denna metod itererar över alla lager i CAD-ritningen och exporterar varje lager till en separat Jpeg-fil.

## Slutsats

Grattis! Du har framgångsrikt lärt dig hur du exporterar CAD-layouter till rasterbildsformat med Aspose.CAD för .NET. Denna handledning ger en omfattande guide för utvecklare som söker effektiva och pålitliga lösningar för CAD-konvertering.

## FAQ's

### F1: Kan jag använda andra bildformat för export?

 A1: Ja, det kan du. Byt bara ut`JpegOptions` med önskat formats alternativ, som t.ex`PngOptions` eller`BmpOptions`.

### F2: Finns det en testversion tillgänglig?

 S2: Ja, du kan utforska funktionerna i Aspose.CAD genom att ladda ner testversionen[här](https://releases.aspose.com/).

### F3: Hur kan jag få support för Aspose.CAD?

 A3: Besök Aspose.CAD[forum](https://forum.aspose.com/c/cad/19) för samhällsstöd eller överväg att köpa en licens för dedikerad support.

### F4: Finns tillfälliga licenser tillgängliga?

 A4: Ja, du kan få en tillfällig licens[här](https://purchase.aspose.com/temporary-license/).

### F5: Var kan jag hitta dokumentationen?

 S5: Se den detaljerade dokumentationen[här](https://reference.aspose.com/cad/net/).