---
title: Konvertera DWG till PDF med koordinater i C# - Aspose.CAD Tutorial
linktitle: Konvertera DWG till PDF med koordinater i C#
second_title: Aspose.CAD .NET - CAD- och BIM-filformat
description: Lär dig hur du konverterar DWG till PDF med specifika koordinater i C# med Aspose.CAD. Följ vår steg-för-steg-guide för exakta och effektiva CAD-filkonverteringar.
weight: 11
url: /sv/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konvertera DWG till PDF med koordinater i C# - Aspose.CAD Tutorial

## Introduktion

Välkommen till denna omfattande handledning om att konvertera DWG-filer till PDF med specificerade koordinater med Aspose.CAD för .NET. Aspose.CAD är ett kraftfullt bibliotek som låter utvecklare arbeta med CAD-filformat i sina .NET-applikationer sömlöst. I den här handledningen går vi igenom processen att konvertera en DWG-fil till PDF samtidigt som vi tillhandahåller specifika koordinater för att förbättra precisionen.

## Förutsättningar

Innan vi börjar, se till att du har följande förutsättningar:

- Aspose.CAD Library: Ladda ner och installera Aspose.CAD-biblioteket för .NET. Du hittar biblioteket[här](https://releases.aspose.com/cad/net/).

- Utvecklingsmiljö: Se till att du har en kompatibel utvecklingsmiljö inställd, inklusive Visual Studio eller någon annan föredragen IDE.

- DWG-fil: Ha en DWG-fil redo för konvertering. Du kan använda den medföljande exempelfilen eller din anpassade DWG-fil.

## Importera namnområden

Importera de nödvändiga namnrymden i ditt C#-projekt:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadParameters;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.ImageOptions;
```

Låt oss dela upp koden i en steg-för-steg-guide för en bättre förståelse:

## Steg 1: Definiera dokumentkatalogen

```csharp
string MyDir = "Your Document Directory";
```

## Steg 2: Ställ in sökvägen för käll-DWG-filen

```csharp
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
```

## Steg 3: Ladda DWG-fil och konfigurera rasteriseringsalternativ

```csharp
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
    rasterizationOptions.Layouts = new string[] { "Model" };
    rasterizationOptions.NoScaling = true;
```

## Steg 4: Definiera koordinater och vyport

```csharp
    Point topLeft = new Point(500, 1000);
    double width = 3108;
    double height = 2489;

    CadVportTableObject newView = new CadVportTableObject();
    newView.Name = new CadStringParameter();
    newView.Name.Init("*Active");
    newView.CenterPoint.X = topLeft.X + width / 2f;
    newView.CenterPoint.Y = topLeft.Y - height / 2f;
    newView.ViewHeight.Value = height;
    newView.ViewAspectRatio.Value = width / height;
```

## Steg 5: Använd Viewport Settings

```csharp
    for (int i = 0; i < cadImage.ViewPorts.Count; i++)
    {
        CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
        if (cadImage.ViewPorts.Count == 1 || string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
        {
            cadImage.ViewPorts[i] = newView;
            break;
        }
    }
```

## Steg 6: Konfigurera PDF-alternativ och exportera

```csharp
    Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
    pdfOptions.VectorRasterizationOptions = rasterizationOptions;

    MyDir = MyDir + "ConvertDWGToPDFBySupplyingCoordinates_out.pdf";
    cadImage.Save(MyDir, pdfOptions);
}
```

## Steg 7: Visa framgångsmeddelande

```csharp
Console.WriteLine("\nThe DWG file exported successfully to PDF.\nFile saved at " + MyDir);
```

## Slutsats

Grattis! Du har framgångsrikt konverterat en DWG-fil till PDF med specificerade koordinater med Aspose.CAD för .NET. Denna handledning täckte viktiga steg och gav en tydlig guide för utvecklare.

## FAQ's

### F1: Kan jag använda Aspose.CAD med andra CAD-filformat?

S1: Ja, Aspose.CAD stöder olika CAD-format, inklusive DWG, DXF, DWF och mer.

### F2: Hur kan jag hantera fel under konverteringsprocessen?

S2: Implementera felhanteringsmekanismer med hjälp av försöksfångstblock för att fånga och hantera undantag.

### F3: Är Aspose.CAD lämplig för både Windows- och Linux-miljöer?

S3: Ja, Aspose.CAD är kompatibel med både Windows- och Linux-plattformar.

### F4: Kan jag anpassa PDF-utdata ytterligare?

A4: Visst! Utforska de omfattande alternativen som tillhandahålls av Aspose.CAD för att skräddarsy PDF-utdata efter dina specifika krav.

### F5: Var kan jag hitta ytterligare stöd eller diskussioner i samhället?

A5: Besök[Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) för samhällsstöd och diskussioner.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
