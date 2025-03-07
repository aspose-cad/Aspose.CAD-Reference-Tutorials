---
title: Exportera till BMP-format - Aspose.CAD Tutorial
linktitle: Exporterar till BMP-format
second_title: Aspose.CAD .NET - CAD- och BIM-filformat
description: Utforska den sömlösa världen av 3D-bildexport till BMP med Aspose.CAD för .NET. Följ vår handledning för en problemfri upplevelse.
weight: 11
url: /sv/net/file-format-conversion/exporting-to-bmp-format/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportera till BMP-format - Aspose.CAD Tutorial

## Introduktion

den dynamiska världen av mjukvaruutveckling utmärker sig Aspose.CAD för .NET som ett kraftfullt verktyg för att hantera datorstödd design (CAD)-filer. Om du funderar på att exportera CAD-bilder till det allmänt använda BMP-formatet, är den här handledningen din bästa guide. I denna steg-för-steg-genomgång kommer vi att utforska processen att exportera 3D-bilder till BMP med Aspose.CAD för .NET. Låt oss dyka in!

## Förutsättningar

Innan vi börjar med den här handledningen, se till att du har följande förutsättningar på plats:

-  Aspose.CAD för .NET: Ladda ner och installera Aspose.CAD-biblioteket från[här](https://releases.aspose.com/cad/net/).
- Utvecklingsmiljö: Skapa en .NET-utvecklingsmiljö.
- CAD-fil: Ha en CAD-fil redo för export. I det här exemplet använder vi "18-12-11 9644 - site.dwf."

## Importera namnområden

Se till att importera de nödvändiga namnrymden i ditt .NET-projekt:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

## Steg 1: Ladda CAD-bilden

Börja med att ladda CAD-bilden i ditt projekt. Ersätt "Din dokumentkatalog" med den faktiska katalogsökvägen.

```csharp
string MyDir = "Your Document Directory";
string inputFile = MyDir + "18-12-11 9644 - site.dwf";

using (Image image = Image.Load(inputFile))
{
    // Din kod för att ladda bilden går här
}
```

## Steg 2: Konfigurera BMP-exportalternativ

Ställ in BMP-exportalternativ, inklusive vektorrasteriseringsalternativ för CAD-filer.

```csharp
BmpOptions bmpOptions = new BmpOptions();
var dwfRasterizationOptions = new CadRasterizationOptions();
bmpOptions.VectorRasterizationOptions = dwfRasterizationOptions;

dwfRasterizationOptions.PageHeight = 500;
dwfRasterizationOptions.PageWidth = 500;
```

## Steg 3: Exportera till BMP

Kör exportprocessen och ange utdatasökvägen för BMP-filen.

```csharp
string outPath = MyDir + "18-12-11 9644 - site.bmp";
image.Save(outPath, bmpOptions);
```

## Slutsats

Grattis! Du har framgångsrikt exporterat en 3D-bild till BMP med Aspose.CAD för .NET. Denna handledning ger en inblick i mångsidigheten i Aspose.CAD, vilket gör att komplexa uppgifter känns som en bris.

## FAQ's

### F1: Kan jag använda Aspose.CAD för .NET med vilket CAD-filformat som helst?

S1: Ja, Aspose.CAD stöder olika CAD-filformat, vilket ger flexibilitet i dina projekt.

### F2: Är en tillfällig licens tillgänglig för teständamål?

 A2: Visst! Du kan få en tillfällig licens[här](https://purchase.aspose.com/temporary-license/) för utvärdering.

### F3: Var kan jag hitta omfattande dokumentation för Aspose.CAD?

 A3: Se dokumentationen[här](https://reference.aspose.com/cad/net/) för detaljerad information och exempel.

### F4: Hur söker jag stöd eller får kontakt med samhället?

 S4: Besök Aspose.CAD-forumet[här](https://forum.aspose.com/c/cad/19) att ställa frågor och engagera sig i samhället.

### F5: Kan jag köpa Aspose.CAD för .NET?

 S5: Ja, du kan köpa Aspose.CAD[här](https://purchase.aspose.com/buy) för att frigöra dess fulla potential för dina projekt.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
