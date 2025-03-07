---
title: DGN-element som stöds i Aspose.CAD för .NET
linktitle: DGN-element som stöds
second_title: Aspose.CAD .NET - CAD- och BIM-filformat
description: Utforska Aspose.CAD för .NETs kraftfulla funktioner för att hantera DGN-filer. Följ vår steg-för-steg-guide för att arbeta sömlöst med 2D- och 3D-element.
weight: 18
url: /sv/net/cad-features-and-support/supported-dgn-elements/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DGN-element som stöds i Aspose.CAD för .NET

## Introduktion

Är du en .NET-utvecklare som vill arbeta med DGN-filer sömlöst? Aspose.CAD för .NET tillhandahåller en robust lösning för att hantera DGN-filer effektivt. I den här handledningen kommer vi att fördjupa oss i de DGN-element som stöds, och guida dig genom processen att arbeta med Aspose.CAD för .NET.

## Förutsättningar

Innan vi börjar, se till att du har följande:

- Grundläggande kunskaper i .NET-programmering.
- Visual Studio installerat på din dator.
-  Aspose.CAD för .NET-bibliotek, som du kan ladda ner[här](https://releases.aspose.com/cad/net/).

## Importera namnområden

För att kickstarta ditt projekt, importera de nödvändiga namnrymden till din .NET-applikation. Detta steg säkerställer att du har tillgång till funktionerna som tillhandahålls av Aspose.CAD för .NET.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.FileFormats.Dgn.DgnElements;
```

## Steg 1: Ladda DGN-filen

Börja med att ladda en befintlig DGN-fil som en CadImage i din .NET-applikation.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Din kod här
}
```

## Steg 2: Iterera genom DGN-element

Iterera genom DGN-elementen med en foreach loop. Aspose.CAD för .NET tillhandahåller en mängd olika DGN-elementtyper som du kan arbeta med.

```csharp
foreach (DgnDrawingElementBase element in dgnImage.Elements)
{
    // Din kod här
}
```

## Steg 3: Hantera tidigare stödda enheter

Hantera de tidigare stödda 2D-entiteterna, som nu även stöds för 3D.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.Line:
    case DgnElementType.Ellipse:
    case DgnElementType.Curve:
    // Ytterligare fall
        {
            // Din kod här
            break;
        }
}
```

## Steg 4: Hantera 3D-entiteter som stöds

Hantera de 3D-entiteter som stöds som tillhandahålls av Aspose.CAD för .NET.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.SolidHeader3D:
    case DgnElementType.Cone:
    case DgnElementType.CellHeader:
        {
            // Din kod här
            break;
        }
}
```

## Steg 5: Exportera och spara

Exportera slutligen den modifierade DGN-filen till en rasterbild och spara den i den angivna katalogen.

```csharp
Console.WriteLine("\nThe DGN file exported successfully to raster image.\nFile saved at " + MyDir);
```

## Slutsats

den här handledningen utforskade vi funktionerna hos Aspose.CAD för .NET för att hantera och manipulera DGN-filer. Genom att följa steg-för-steg-guiden kan du effektivt arbeta med DGN-element som stöds, oavsett om de är 2D- eller 3D-enheter. Aspose.CAD för .NET ger dig möjlighet att sömlöst integrera DGN-filbehandling i dina .NET-applikationer.

## FAQ's

### F1: Var kan jag hitta dokumentationen för Aspose.CAD för .NET?

 A1: Du kan hitta dokumentationen[här](https://reference.aspose.com/cad/net/).

### F2: Hur laddar jag ner Aspose.CAD för .NET?

 A2: Du kan ladda ner biblioteket[här](https://releases.aspose.com/cad/net/).

### F3: Finns det en gratis testversion tillgänglig för Aspose.CAD för .NET?

 A3: Ja, du kan komma åt den kostnadsfria provperioden[här](https://releases.aspose.com/).

### F4: Var kan jag få tillfälliga licenser för Aspose.CAD för .NET?

 A4: Tillfälliga licenser finns tillgängliga[här](https://purchase.aspose.com/temporary-license/).

### F5: Behöver du hjälp eller har frågor?

 S5: Besök Aspose.CAD för .NET-gemenskapen[supportforum](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
