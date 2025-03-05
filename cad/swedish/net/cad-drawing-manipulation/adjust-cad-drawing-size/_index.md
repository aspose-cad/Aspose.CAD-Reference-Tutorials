---
title: Justera CAD-ritningsstorlek i Aspose.CAD för .NET
linktitle: Justera CAD-ritningsstorlek
second_title: Aspose.CAD .NET - CAD- och BIM-filformat
description: Lär dig hur du enkelt justerar CAD-ritningsstorlekar i .NET med Aspose.CAD. Följ vår steg-för-steg-guide för sömlös storleksändring.
type: docs
weight: 10
url: /sv/net/cad-drawing-manipulation/adjust-cad-drawing-size/
---
## Introduktion

Vill du sömlöst justera storleken på CAD-ritningar i dina .NET-applikationer? Aspose.CAD för .NET ger en robust lösning som gör att du enkelt kan hantera storleksändring av CAD-ritningar. I den här handledningen guidar vi dig genom processen och delar upp varje steg för att säkerställa att du förstår krångligheterna med att ändra storlek på CAD-ritningar med Aspose.CAD.

## Förutsättningar

Innan vi dyker in i handledningen, se till att du har följande förutsättningar på plats:

- Aspose.CAD för .NET Library: Ladda ner och installera biblioteket från[Aspose.CAD för .NET nedladdningssida](https://releases.aspose.com/cad/net/).
- Exempel CAD-ritning: Se till att du har ett exempel på CAD-ritningsfil (t.ex. "sample.dwg") i din dokumentkatalog.

## Importera namnområden

Börja med att importera de nödvändiga namnområdena till ditt .NET-program. Detta steg är avgörande för att få tillgång till funktionerna som tillhandahålls av Aspose.CAD för .NET.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Steg 1: Ladda CAD-ritning

Börja med att ladda CAD-ritningen i en instans av klassen Aspose.CAD.Image. Se till att du har rätt sökväg för din provritning.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "sample.dwg";

// Ladda en CAD-ritning i en instans av Image
using (var image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // Din kod här...
}
```

## Steg 2: Skapa BmpOptions

Skapa en instans av klassen BmpOptions, som är ansvarig för att ange alternativ när du sparar CAD-ritningen som en BMP-fil.

```csharp
Aspose.CAD.ImageOptions.BmpOptions bmpOptions = new Aspose.CAD.ImageOptions.BmpOptions();
```

## Steg 3: Ställ in CadRasterizationOptions

Instantiera klassen CadRasterizationOptions och konfigurera dess egenskaper för vektorrasterisering.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions cadRasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
bmpOptions.VectorRasterizationOptions = cadRasterizationOptions;
```

## Steg 4: Ställ in UnitType Property

Ställ in egenskapen UnitType för CadRasterizationOptions för att ange enhetstypen för storleksändring. I det här exemplet är den inställd på Centimeter.

```csharp
cadRasterizationOptions.UnitType = Aspose.CAD.ImageOptions.UnitType.Centimeter;
```

## Steg 5: Ställ in layoutegenskaper

Ange de layouter du vill inkludera i den ändrade storleksritningen genom att ställa in egenskapen Layouts.

```csharp
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## Steg 6: Exportera till BMP

Slutligen, spara den ändrade storlekslayouten som en BMP-fil med hjälp av Spara-metoden.

```csharp
string outPath = sourceFilePath + ".bmp";
image.Save(outPath, bmpOptions);
```

Nu har du justerat storleken på din CAD-ritning med Aspose.CAD för .NET!

## Slutsats

I den här handledningen gick vi igenom processen att ändra storlek på CAD-ritningar i .NET med Aspose.CAD. Genom att följa dessa steg kan du sömlöst integrera den här funktionen i dina applikationer, vilket ger en smidig användarupplevelse.

## Vanliga frågor

### F1: Är Aspose.CAD för .NET kompatibelt med alla CAD-format?

 S1: Aspose.CAD för .NET stöder ett brett utbud av CAD-format, inklusive DWG, DXF, DWF och mer. Kolla[dokumentation](https://reference.aspose.com/cad/net/) för hela listan.

### F2: Kan jag ändra storlek på flera layouter samtidigt?

S2: Ja, du kan ändra storlek på flera layouter genom att justera layoutarrayen i CadRasterizationOptions.

### F3: Var kan jag få support för Aspose.CAD för .NET?

 A3: Besök[Aspose.CAD-forum](https://forum.aspose.com/c/cad/19) för samhällsstöd och hjälp.

### F4: Finns det en gratis provperiod?

 A4: Ja, du kan utforska en[gratis provperiod](https://releases.aspose.com/) för att utvärdera funktionerna i Aspose.CAD för .NET.

### F5: Hur kan jag få en tillfällig licens för Aspose.CAD för .NET?

 S5: Skaffa en tillfällig licens för teständamål[här](https://purchase.aspose.com/temporary-license/).