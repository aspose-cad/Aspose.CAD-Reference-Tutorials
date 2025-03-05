---
title: Få storlek på CAD-layout i Aspose.CAD för .NET
linktitle: Få storlek på CAD-layout
second_title: Aspose.CAD .NET - CAD- och BIM-filformat
description: Lär dig hur du hämtar CAD-layoutstorlek i .NET med Aspose.CAD. Följ vår steg-för-steg-guide för effektiv CAD-filmanipulation.
type: docs
weight: 14
url: /sv/net/cad-drawing-manipulation/get-size-of-cad-layout/
---
## Introduktion

Välkommen till denna omfattande guide för att få storleken på CAD-layouter med Aspose.CAD för .NET. Aspose.CAD är ett kraftfullt bibliotek som gör det möjligt för utvecklare att arbeta med CAD-filer sömlöst. I den här handledningen går vi igenom processen för att hämta storleken på CAD-layouter med hjälp av praktiska exempel och steg-för-steg-instruktioner.

## Förutsättningar

Innan vi dyker in i handledningen, se till att du har följande förutsättningar på plats:

-  Aspose.CAD för .NET: Se till att du har Aspose.CAD-biblioteket installerat. Du kan ladda ner den från[Aspose.CAD för .NET nedladdningssida](https://releases.aspose.com/cad/net/).

- Dokumentfiler: Förbered CAD-filerna du vill arbeta med. Den här handledningen använder "conic_pyramid.dxf" och "Bottom_plate.dwg" som exempel.

Nu sätter vi igång!

## Importera namnområden

I ditt .NET-projekt börjar du med att importera de nödvändiga namnrymden:

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.ImageOptions;
```

## Steg 1: Konfigurera dokumentkatalogen

 Ställ in sökvägen till din dokumentkatalog. Byta ut`"Your Document Directory"` med den faktiska vägen.

```csharp
string MyDir = "Your Document Directory";
```

## Steg 2: Ange CAD-filsökvägar

Definiera en uppsättning CAD-filsökvägar som du vill analysera. I det här exemplet använder vi "conic_pyramid.dxf" och "Bottom_plate.dwg."

```csharp
string[] sourceFilePaths = new[]
{
    MyDir + "conic_pyramid.dxf",
    MyDir + "Bottom_plate.dwg"
};
```

## Steg 3: Iterera genom CAD-filer

Iterera igenom varje CAD-fil och hämta layoutinformationen.

```csharp
foreach (var sourceFilePath in sourceFilePaths)
{
    string extension = Path.GetExtension(sourceFilePath);
    using (CadImage cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath))
    {
        // ... (fortsätt till nästa steg)
    }
}
```

## Steg 4: Skaffa icke-tomma layouter

Definiera en hjälpmetod för att få icke-tomma layouter baserat på CAD-filtypen.

```csharp
private static List<string> GetNotEmptyLayouts(Image cadImage, string extension)
{
    // ... (fortsätt till nästa steg)
}
```

## Steg 5: Hämta layouter för DWG-filer

Implementera logik för att hämta icke-tomma layouter för DWG-filer.

```csharp
private static List<string> GetNotEmptyLayoutsForDwg(CadImage cadImage)
{
    // ... (fortsätt till nästa steg)
}
```

## Steg 6: Skaffa layouter för DXF-filer

Implementera logik för att hämta icke-tomma layouter för DXF-filer.

```csharp
private static List<string> GetNotEmptyLayoutsForDxf(CadImage cadImage)
{
    // ... (fortsätt till nästa steg)
}
```

## Steg 7: Hämta layoutstorlek och spara som bild

Slutför processen med att få layoutstorlek och spara den som en bild.

```csharp
foreach (string layout in layouts)
{
    // ... (fortsätt till nästa steg)
}
```

## Slutsats

Grattis! Du har framgångsrikt lärt dig hur du får storleken på CAD-layouter med Aspose.CAD för .NET. Den här handledningen täckte viktiga steg, från att ställa in ditt projekt till att hämta layoutinformation och spara den som en bild. Nu kan du införliva denna kunskap i dina .NET-applikationer för effektiv CAD-filmanipulation.

## FAQ's

### F1: Är Aspose.CAD kompatibel med alla CAD-filformat?

S1: Ja, Aspose.CAD stöder olika CAD-filformat, inklusive DWG och DXF.

### F2: Kan jag anpassa alternativen för bildsparande?

A2: Absolut! Du kan justera bildalternativ, såsom format och upplösning, för att uppfylla dina specifika krav.

### F3: Var kan jag hitta ytterligare dokumentation?

 A3: Se[Aspose.CAD-dokumentation](https://reference.aspose.com/cad/net/) för detaljerad information och exempel.

### F4: Finns det en gratis provperiod?

 A4: Ja, du kan utforska Aspose.CAD med en[gratis provperiod](https://releases.aspose.com/).

### Q5; Hur kan jag få teknisk support?

 S5: För teknisk support, besök[Aspose.CAD-forum](https://forum.aspose.com/c/cad/19).