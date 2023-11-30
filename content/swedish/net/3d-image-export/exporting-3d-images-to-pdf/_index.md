---
title: Exportera 3D-bilder till PDF - Aspose.CAD Tutorial
linktitle: Exportera 3D-bilder till PDF
second_title: Aspose.CAD .NET - CAD- och BIM-filformat
description: Konvertera enkelt 3D CAD-bilder till PDF med Aspose.CAD för .NET. Följ vår steg-för-steg handledning för sömlös PDF-export.
type: docs
weight: 10
url: /sv/net/3d-image-export/exporting-3d-images-to-pdf/
---
## Introduktion

Vill du sömlöst exportera 3D-bilder till PDF med Aspose.CAD för .NET? Denna steg-för-steg handledning guidar dig genom processen och säkerställer att du utnyttjar kraften i Aspose.CAD för att enkelt konvertera dina 3D-bilder till PDF-format.

## Förutsättningar

Innan du dyker in i handledningen, se till att du har följande förutsättningar på plats:

-  Aspose.CAD för .NET: Se till att du har Aspose.CAD-biblioteket för .NET installerat. Om inte kan du ladda ner den från[Aspose.CAD för .NET nedladdningssida](https://releases.aspose.com/cad/net/).

- Dokumentkatalog: Skapa en katalog där dina CAD-filer lagras och anteckna sökvägen.

## Importera namnområden

I ditt .NET-projekt, importera de nödvändiga namnrymden för att arbeta med Aspose.CAD. Lägg till följande rader överst i din kodfil:

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

 Börja med att ladda CAD-bilden du vill exportera till PDF. Använd`Load` metod från Aspose.CAD-biblioteket. Byta ut`"conic_pyramid.dxf"` med sökvägen till din CAD-fil.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image cadImage = Image.Load(sourceFilePath))
{
    // Din kod för att ladda CAD-bilden kommer här
}
```

## Steg 2: Konfigurera rasteriseringsalternativ

 Konfigurera rastreringsalternativen för CAD-bilden. Ställ in parametrar som sidbredd, sidhöjd och layouter. Avkommentera raden som rör`TypeOfEntities` om dina enheter är 3D.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
//rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;

rasterizationOptions.Layouts = new string[] { "Model" };
```

## Steg 3: Ställ in PDF-alternativ

Skapa PDF-alternativ och associera dem med rastreringsalternativen.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Steg 4: Spara som PDF

Spara CAD-bilden som en PDF-fil med de konfigurerade alternativen. Ange utdatasökvägen för PDF-filen.

```csharp
MyDir = MyDir + "Export3DImagestoPDF_out.pdf";
cadImage.Save(MyDir, pdfOptions);
```

## Slutsats

Grattis! Du har framgångsrikt exporterat 3D-bilder till PDF med Aspose.CAD för .NET. Denna enkla handledning säkerställer att du enkelt konverterar dina CAD-filer till ett mer tillgängligt format.

## FAQ's

### F1: Är Aspose.CAD kompatibel med alla CAD-filformat?

S1: Ja, Aspose.CAD stöder ett brett utbud av CAD-format, vilket säkerställer flexibilitet vid hantering av olika filtyper.

### F2: Kan jag anpassa siddimensionerna när jag exporterar till PDF?

A2: Absolut. Handledningen visar hur du konfigurerar sidbredd och höjd enligt dina krav.

### F3: Finns tillfälliga licenser tillgängliga för Aspose.CAD?

S3: Ja, du kan få tillfälliga licenser för Aspose.CAD genom att besöka[Tillfällig licens](https://purchase.aspose.com/temporary-license/).

### F4: Var kan jag hitta ytterligare stöd eller diskussioner i samhället?

 A4: Gå till[Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) för stöd och engagemang i samhället.

### F5: Finns det en gratis testversion av Aspose.CAD tillgänglig?

 S5: Ja, du kan utforska funktionerna i Aspose.CAD genom att komma åt[gratis provperiod](https://releases.aspose.com/).