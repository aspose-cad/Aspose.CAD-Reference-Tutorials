---
title: Rendering av DWG-dokument i C# - Aspose.CAD Guide
linktitle: Rendera DWG-dokument i C#
second_title: Aspose.CAD .NET - CAD- och BIM-filformat
description: Lär dig hur du renderar DWG-dokument i C# med Aspose.CAD. Den här steg-för-steg-guiden täcker import, konfigurering och sparande med kodexempel.
type: docs
weight: 17
url: /sv/net/image-manipulation-and-rendering/rendering-dwg-documents/
---
## Introduktion

Välkommen till den omfattande guiden för att rendera DWG-dokument i C# med Aspose.CAD. Oavsett om du är en erfaren utvecklare eller precis har börjat med .NET, kommer den här handledningen att leda dig genom processen att utnyttja Aspose.CAD för att rendera DWG-filer effektivt. Aspose.CAD är ett kraftfullt API som ger robusta funktioner för att arbeta med CAD-filformat, vilket gör det till ett bra val för utvecklare som hanterar DWG-filer.

## Förutsättningar

Innan du dyker in i handledningen, se till att du har följande förutsättningar:

- Grundläggande kunskaper i programmeringsspråket C#.
- Visual Studio installerat på din dator.
-  Aspose.CAD-bibliotek integrerat i ditt projekt. Du kan ladda ner den från[här](https://releases.aspose.com/cad/net/).
- Ett exempel på DWG-fil, till exempel "Bottom_plate.dwg", som följer med exemplen.

## Importera namnområden

För att komma igång, se till att importera de nödvändiga namnrymden i början av din C#-kod:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.FileFormats.Cad;
```

Låt oss nu dela upp exemplet i flera steg:

## Steg 1: Ladda DWG-filen

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    //Din kod för att ladda DWG-filen finns här.
}
```

## Steg 2: Konfigurera rasteriseringsalternativ

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };
rasterizationOptions.NoScaling = true;
// Ytterligare rastreringskonfigurationer kan läggas till här.
```

## Steg 3: Definiera region att rita

```csharp
Point topLeft = new Point(6156, 7053);
double width = 3108;
double height = 2489;
```

## Steg 4: Skapa en ny visningsport

```csharp
CadVportTableObject newView = new CadVportTableObject();
newView.Name.Value = "*Active";
newView.CenterPoint.X = topLeft.X + width / 2f;
newView.CenterPoint.Y = topLeft.Y - height / 2f;
newView.ViewHeight.Value = height;
newView.ViewAspectRatio.Value = width / height;
```

## Steg 5: Byt ut Active Viewport

```csharp
for (int i = 0; i < cadImage.ViewPorts.Count; i++)
{
    CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
    if ((currentView.Name.Value == null && cadImage.ViewPorts.Count == 1) ||
    string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
    {
        cadImage.ViewPorts[i] = newView;
        break;
    }
}
```

## Steg 6: Konfigurera PDF-alternativ

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Steg 7: Spara den renderade DWG-filen som PDF

```csharp
cadImage.Save(MyDir, pdfOptions);
```

## Slutsats

Grattis! Du har framgångsrikt renderat ett DWG-dokument till PDF med Aspose.CAD i C#. Utforska gärna fler funktioner och anpassa koden utifrån dina specifika krav.

## FAQ's

### F1: Kan jag använda Aspose.CAD med andra CAD-filformat?

S1: Ja, Aspose.CAD stöder olika CAD-format, inklusive DWG, DXF, DWF och mer.

### F2: Är Aspose.CAD kompatibel med .NET Core?

S2: Ja, Aspose.CAD är kompatibel med både .NET Framework och .NET Core.

### F3: Hur kan jag hantera olika layouter i en DWG-fil?

 S3: Du kan ange önskad layout i`Layouts` egendom av`CadRasterizationOptions`.

### F4: Finns det några licensöverväganden för att använda Aspose.CAD?

 A4: För licensinformation, besök[här](https://purchase.aspose.com/buy).

### F5: Var kan jag hitta ytterligare support?

 A5: Besök[Aspose.CAD-forum](https://forum.aspose.com/c/cad/19) för samhällsstöd och diskussioner.