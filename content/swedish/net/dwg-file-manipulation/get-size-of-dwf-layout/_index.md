---
title: Arbeta med DWG-filer i C# - Få storlek på DWF-layout
linktitle: Arbeta med DWG-filer i C# - Få storlek på DWF-layout
second_title: Aspose.CAD .NET - CAD- och BIM-filformat
description: Utforska kraften i Aspose.CAD för .NET för att hantera DWG-filer. Lär dig att extrahera DWF-layoutstorlekar utan ansträngning med C#.
type: docs
weight: 10
url: /sv/net/dwg-file-manipulation/get-size-of-dwf-layout/
---
## Introduktion

Inom området datorstödd design (CAD) och .NET-utveckling står Aspose.CAD som ett kraftfullt verktyg för att hantera DWG-filer. Denna handledning guidar dig genom processen att arbeta med DWG-filer i C# och extrahera storleken på en DWF-layout. Innan vi dyker in i koden, låt oss se till att du har allt förberett för att ge dig ut på denna resa.

## Förutsättningar

För att följa denna handledning sömlöst, se till att du har följande förutsättningar på plats:

-  Aspose.CAD för .NET: Se till att du har Aspose.CAD för .NET installerat. Du kan ladda ner den från[Aspose.CAD för .NET nedladdningssida](https://releases.aspose.com/cad/net/).

Nu när du har de nödvändiga verktygen, låt oss hoppa in på kodningsarenan.

## Importera namnområden

Innan vi börjar arbeta med koden, låt oss importera de nödvändiga namnrymden:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Dwf;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

Dessa namnområden kommer att tillhandahålla de väsentliga klasserna och metoderna för att hantera CAD-filer med Aspose.CAD i din C#-applikation.

## Steg 1: Ställ in din miljö

Börja med att se till att du har rätt miljö inställd för ditt projekt. Referera till Aspose.CAD-biblioteket i ditt C#-projekt.

## Steg 2: Definiera filsökvägar

Definiera sökvägarna för din DWG-fil och utdatakatalogen för de genererade JPG-filerna:

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "blocks_and_tables.dwf";
```

## Steg 3: Ladda DWF-bilden

Ladda DWF-bilden med Aspose.CAD:

```csharp
using (DwfImage image = (DwfImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    // Koden för ytterligare steg kommer här
}
```

## Steg 4: Iterera genom sidor

Iterera genom sidorna i DWF-bilden:

```csharp
foreach (var page in image.Pages)
{
    // Koden för ytterligare steg kommer här
}
```

## Steg 5: Få layoutinformation

Få layoutinformation från varje sida:

```csharp
var layout = page.Name;
System.Console.WriteLine("Layout= " + layout);
```

## Steg 6: Ställ in JPG-alternativ

Ställ in alternativ för att spara layouten som en JPG-fil:

```csharp
using (FileStream fs = new FileStream(MyDir + "layout_" + layout + ".jpg", FileMode.Create))
{
    JpegOptions jpegOptions = new JpegOptions();
    CadRasterizationOptions options = new CadRasterizationOptions();
    options.Layouts = new string[] { layout };
    // Koden för ytterligare steg kommer här
}
```

## Steg 7: Bestäm sidstorlek

Bestäm storleken på DWF-layouten:

```csharp
double sizeExtX = page.MaxPoint.X - page.MinPoint.X;
double sizeExtY = page.MaxPoint.Y - page.MinPoint.Y;
// Koden för ytterligare steg kommer här
```

## Steg 8: Ställ in sidmått

Ställ in sidmåtten baserat på enhetstypen:

```csharp
if (page.UnitType == UnitType.Inch)
{
    options.PageHeight = CommonHelper.INtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.INtoPixels(sizeExtX, CommonHelper.DPI);
}
else if (page.UnitType == UnitType.Millimeter)
{
    options.PageHeight = CommonHelper.MMtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.MMtoPixels(sizeExtX, CommonHelper.DPI);
}
else
{
    options.PageHeight = (float)sizeExtY;
    options.PageWidth = (float)sizeExtX;
}
```

## Steg 9: Spara JPG-filen

Spara JPG-filen med de angivna alternativen:

```csharp
jpegOptions.VectorRasterizationOptions = options;
image.Save(fs, jpegOptions);
}
```

Nu har du framgångsrikt extraherat storleken på DWF-layouten från DWG-filen med Aspose.CAD i C#. Utforska gärna fler funktioner och funktioner som Aspose.CAD erbjuder för .NET-utveckling.

## Slutsats

I den här handledningen har vi gått igenom processen att arbeta med DWG-filer i C# med Aspose.CAD. Genom att följa dessa steg kan du inte bara få storleken på en DWF-layout utan också utnyttja funktionerna i Aspose.CAD för olika CAD-relaterade uppgifter i dina .NET-projekt.

## FAQ's

### F1: Är Aspose.CAD kompatibel med de senaste DWG-filformaten?

 S1: Aspose.CAD stöder olika DWG-filformat, inklusive de senaste versionerna. Referera till[dokumentation](https://reference.aspose.com/cad/net/) för specifika kompatibilitetsdetaljer.

### F2: Kan jag använda Aspose.CAD för både kommersiella och personliga projekt?

S2: Ja, Aspose.CAD erbjuder flexibla licensalternativ för både kommersiellt och personligt bruk. Besök[köpsidan](https://purchase.aspose.com/buy) för mer detaljer.

### F3: Hur kan jag få en tillfällig licens för Aspose.CAD?

 A3: Du kan få en tillfällig licens från[här](https://purchase.aspose.com/temporary-license/) i utvärderingssyfte.

### F4: Var kan jag hitta support för Aspose.CAD?

 S4: För eventuella frågor eller hjälp, besök[Aspose.CAD-forum](https://forum.aspose.com/c/cad/19).

### F5: Finns det en gratis testversion tillgänglig för Aspose.CAD?

 S5: Ja, du kan få tillgång till en gratis testversion av Aspose.CAD[här](https://releases.aspose.com/).