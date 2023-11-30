---
title: Ställa in dukstorlek och läge i Aspose.CAD för .NET
linktitle: Ställa in dukstorlek och läge
second_title: Aspose.CAD .NET - CAD- och BIM-filformat
description: Utforska steg-för-steg-guiden om hur du ställer in dukens storlek och läge i Aspose.CAD för .NET. Optimera din CAD-rendering med lätthet med denna omfattande handledning.
type: docs
weight: 16
url: /sv/net/cad-features-and-support/setting-canvas-size-and-mode/
---
## Introduktion

Är du redo att låsa upp den fulla potentialen hos Aspose.CAD för .NET och revolutionera din CAD-renderingsupplevelse? I denna steg-för-steg handledning kommer vi att fördjupa oss i krångligheterna med att ställa in storlek och läge på duken med hjälp av det kraftfulla Aspose.CAD-biblioteket. Oavsett om du är en erfaren utvecklare eller precis har börjat, kommer den här guiden att leda dig genom processen, vilket säkerställer att du utnyttjar funktionerna i Aspose.CAD effektivt.

## Förutsättningar

Innan vi dyker in i handledningen, se till att du har följande förutsättningar på plats:

-  Aspose.CAD Library: Ladda ner och installera Aspose.CAD-biblioteket från[Aspose.CAD webbplats](https://releases.aspose.com/cad/net/).

- Utvecklingsmiljö: Se till att du har en .NET-utvecklingsmiljö inställd på din dator.

-  Exempel CAD-fil: För den här handledningen använder vi en DXF-exempel. Du kan hitta en i[Aspose.CAD-dokumentation](https://reference.aspose.com/cad/net/).

## Importera namnområden

För att komma igång, importera nödvändiga namnområden i början av din .NET-applikation:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Steg 1: Ladda CAD-fil

Börja med att ladda CAD-filen med följande kod:

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    // Din kod för ytterligare steg kommer här
}
```

## Steg 2: Skapa CadRasterizationOptions

 Skapa en instans av`CadRasterizationOptions` och ställ in dess egenskaper:

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
rasterizationOptions.NoScaling = false;
```

## Steg 3: Skapa Pdf-alternativ

 Skapa en instans av`PdfOptions` och ställ in dess`VectorRasterizationOptions` fast egendom:

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Steg 4: Exportera till PDF

Exportera CAD-filen till PDF med de konfigurerade alternativen:

```csharp
image.Save(MyDir + "result_out.pdf", pdfOptions);
```

## Steg 5: Skapa TiffOptions

 Skapa en instans av`TiffOptions` och ställ in dess`VectorRasterizationOptions` fast egendom:

```csharp
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Steg 6: Exportera till TIFF

Exportera CAD-filen till TIFF med de konfigurerade alternativen:

```csharp
image.Save(MyDir + "result_out.tiff", tiffOptions);
```

## Slutsats

Grattis! Du har framgångsrikt ställt in dukens storlek och läge i Aspose.CAD för .NET. Denna kraftfulla funktion öppnar upp en värld av möjligheter för CAD-rendering. Experimentera med olika alternativ och upptäck den fulla potentialen av Aspose.CAD i dina .NET-applikationer.

## FAQ's

### F1: Kan jag använda Aspose.CAD med andra .NET-bibliotek?

S1: Ja, Aspose.CAD integreras sömlöst med andra .NET-bibliotek, vilket ger förbättrade möjligheter för CAD-manipulation.

### F2: Finns en gratis provperiod tillgänglig för Aspose.CAD?

 S2: Ja, du kan utforska funktionerna i Aspose.CAD med en gratis provperiod. Besök[här](https://releases.aspose.com/) för att starta.

### F3: Hur kan jag få support för Aspose.CAD?

 S3: För support och diskussioner, besök[Aspose.CAD-forum](https://forum.aspose.com/c/cad/19).

### F4: Var kan jag hitta omfattande dokumentation för Aspose.CAD?

 A4: Se[Aspose.CAD-dokumentation](https://reference.aspose.com/cad/net/) för detaljerad information och exempel.

### F5: Hur köper jag Aspose.CAD för .NET?

 S5: För att köpa Aspose.CAD, besök[köpsidan](https://purchase.aspose.com/buy).