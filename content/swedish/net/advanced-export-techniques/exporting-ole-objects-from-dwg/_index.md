---
title: Exportera OLE-objekt från DWG-filer - Aspose.CAD Tutorial
linktitle: Exportera OLE-objekt från DWG-filer
second_title: Aspose.CAD .NET - CAD- och BIM-filformat
description: Utforska steg-för-steg-guiden för att exportera OLE-objekt från DWG-filer med Aspose.CAD för .NET. Förbättra dina färdigheter i CAD-filhantering utan ansträngning.
type: docs
weight: 12
url: /sv/net/advanced-export-techniques/exporting-ole-objects-from-dwg/
---
## Introduktion

Vill du enkelt extrahera OLE-objekt från DWG-filer? Aspose.CAD för .NET är här för att effektivisera processen åt dig. I den här självstudien guidar vi dig genom att exportera OLE-objekt steg för steg, så att du får ut det mesta av detta kraftfulla .NET-bibliotek. 

## Förutsättningar

Innan vi dyker in i handledningen, se till att du har följande förutsättningar på plats:

-  Aspose.CAD för .NET Library: Se till att du har biblioteket installerat. Du kan ladda ner den från[Aspose.CAD för .NET nedladdningssida](https://releases.aspose.com/cad/net/).

-  Dokumentkatalog: Skapa en katalog där dina DWG-filer lagras. Byta ut`"Your Document Directory"` det medföljande kodavsnittet med den faktiska sökvägen.

## Importera namnområden

I ditt .NET-projekt måste du importera de nödvändiga namnområdena för att utnyttja Aspose.CAD-funktionerna. Använd följande kodavsnitt:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Steg 1: Ställ in dokumentkatalogen

```csharp
string MyDir = "Your Document Directory";
```

 Byta ut`"Your Document Directory"` med sökvägen där dina DWG-filer finns.

## Steg 2: Ange DWG-filer

```csharp
string[] files = new string[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

Lista de DWG-filer du vill bearbeta i arrayen.

## Steg 3: Konfigurera exportalternativ

```csharp
PngOptions pngOptions = new PngOptions { };
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.VectorRasterizationOptions = rasterizationOptions;
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

Anpassa exportalternativen baserat på dina krav. I det här exemplet konfigurerar vi PNG-export med en specificerad layout.

## Steg 4: Iterera genom filer och exportera

```csharp
foreach (string file in files)
{
    using (CadImage cadImage = (CadImage)Image.Load(MyDir + file))
    {
        cadImage.Save(MyDir + file + "_out.png", pngOptions);
    }
}
```

Iterera genom de angivna DWG-filerna, ladda var och en och spara den exporterade PNG-filen med de definierade alternativen.

## Slutsats

Grattis! Du har framgångsrikt exporterat OLE-objekt från DWG-filer med Aspose.CAD för .NET. Detta kraftfulla bibliotek förenklar komplexa uppgifter och ger effektivitet och flexibilitet vid CAD-filmanipulation.

## FAQ's

### F1: Är Aspose.CAD för .NET lämplig för både junior och senior CAD-filer?

S1: Ja, Aspose.CAD för .NET är mångsidig och kan hantera ett brett utbud av CAD-filer, inklusive både junior- och seniorvarianter.

### F2: Kan jag anpassa exportalternativ för olika layouter?

A2: Absolut! Som visas i handledningen kan du skräddarsy exportalternativ, inklusive layouter, för att passa dina specifika behov.

### F3: Var kan jag hitta detaljerad dokumentation för Aspose.CAD för .NET?

 A3: Utforska[Aspose.CAD för .NET-dokumentation](https://reference.aspose.com/cad/net/) för fördjupad information och exempel.

### F4: Finns det en gratis provperiod?

 S4: Ja, du kan uppleva funktionerna i Aspose.CAD för .NET med en gratis provperiod. Besök[den här länken](https://releases.aspose.com/) för att starta.

### F5: Hur kan jag få stöd eller få kontakt med samhället?

 S5: För support och samhällsengagemang, besök[Aspose.CAD-forum](https://forum.aspose.com/c/cad/19).