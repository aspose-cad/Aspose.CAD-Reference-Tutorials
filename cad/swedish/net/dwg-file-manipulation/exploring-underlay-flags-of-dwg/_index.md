---
title: Utforska underläggsflaggor för DWG-filer - Aspose.CAD Tutorial
linktitle: Utforska underläggsflaggor för DWG-filer
second_title: Aspose.CAD .NET - CAD- och BIM-filformat
description: Lås upp kraften i Aspose.CAD för .NET när du utforskar DWG-filunderlagsflaggor. Följ vår steg-för-steg-guide.
type: docs
weight: 13
url: /sv/net/dwg-file-manipulation/exploring-underlay-flags-of-dwg/
---
## Introduktion

Om du fördjupar dig i den intrikata världen av CAD-filer, speciellt DWG-filer, och du vill låsa upp mysterierna med underläggsflaggor, är du på rätt plats. Denna handledning guidar dig genom processen att utforska underläggsflaggor i DWG-filer med hjälp av det kraftfulla Aspose.CAD for .NET-biblioteket.

## Förutsättningar

Innan vi dyker in i handledningen, se till att du har följande:

- En grundläggande förståelse för programmering i C# och .NET.
-  Aspose.CAD för .NET-biblioteket installerat. Om inte kan du ladda ner den[här](https://releases.aspose.com/cad/net/).
- En DWG-fil för testning. Du kan använda exempelfilen "BlockRefDgn.dwg" som finns i handledningen.

## Importera namnområden

För att komma igång måste du importera de nödvändiga namnrymden. Här är ett utdrag som hjälper dig:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;

```

## Steg 1: Ladda DWG-fil och konvertera till CadImage

Börja med att ladda den befintliga DWG-filen och konvertera den till en CadImage:

```csharp
string fileName = MyDir + "BlockRefDgn.dwg";

// Ladda DWG-fil och konvertera till CadImage
using (CadImage image = (CadImage)Image.Load(fileName))
{
    // Din kod för efterföljande steg kommer hit
}
```

## Steg 2: Iterera genom enheter

Iterera sedan igenom varje entitet i DWG-filen:

```csharp
foreach (CadBaseEntity entity in image.Entities)
{
    // Din kod för efterföljande steg kommer hit
}
```

## Steg 3: Kontrollera om CadDgnUnderlay Type

Kontrollera om enheten är av typen CadDgnUnderlay:

```csharp
if (entity is CadDgnUnderlay)
{
    // Din kod för efterföljande steg kommer hit
}
```

## Steg 4: Få tillgång till underläggsflaggor

Få tillgång till olika underlagsflaggor och extrahera relevant information:

```csharp
CadUnderlay underlay = entity as CadUnderlay;

Console.WriteLine(underlay.UnderlayPath);
Console.WriteLine(underlay.UnderlayName);
Console.WriteLine(underlay.InsertionPoint.X);
Console.WriteLine(underlay.InsertionPoint.Y);
Console.WriteLine(underlay.RotationAngle);
Console.WriteLine(underlay.ScaleX);
Console.WriteLine(underlay.ScaleY);
Console.WriteLine(underlay.ScaleZ);
Console.WriteLine((underlay.Flags & UnderlayFlags.UnderlayIsOn) == UnderlayFlags.UnderlayIsOn);
Console.WriteLine((underlay.Flags & UnderlayFlags.ClippingIsOn) == UnderlayFlags.ClippingIsOn);
Console.WriteLine((underlay.Flags & UnderlayFlags.Monochrome) != UnderlayFlags.Monochrome);
```

## Slutsats

Grattis! Du har framgångsrikt utforskat underliggande flaggor för DWG-filer med Aspose.CAD för .NET. Denna handledning försåg dig med kunskapen att navigera genom entiteter och extrahera viktig information om underlag.

## FAQ's

### F1: Kan jag använda Aspose.CAD för .NET med andra CAD-filformat?

S1: Aspose.CAD stöder olika CAD-format, inklusive DWG, DXF, DGN och mer. Se dokumentationen för hela listan.

### F2: Finns en tillfällig licens tillgänglig för Aspose.CAD för .NET?

 A2: Ja, du kan få en tillfällig licens[här](https://purchase.aspose.com/temporary-license/).

### F3: Var kan jag hitta support för Aspose.CAD för .NET?

 S3: Besök supportforumet[här](https://forum.aspose.com/c/cad/19) för assistens.

### F4: Hur köper jag Aspose.CAD för .NET?

A4: Köp biblioteket[här](https://purchase.aspose.com/buy).

### F5: Finns det en gratis provperiod?

 A5: Ja, du kan komma åt den kostnadsfria provperioden[här](https://releases.aspose.com/).
