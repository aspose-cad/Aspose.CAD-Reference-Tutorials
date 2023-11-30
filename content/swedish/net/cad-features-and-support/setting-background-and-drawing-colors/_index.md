---
title: Ställa in bakgrunds- och ritfärger i Aspose.CAD för .NET
linktitle: Ställa in bakgrunds- och ritfärger
second_title: Aspose.CAD .NET - CAD- och BIM-filformat
description: Master Aspose.CAD för .NET. Ange bakgrund och rita färger utan ansträngning. Följ vår steg-för-steg-guide.
type: docs
weight: 15
url: /sv/net/cad-features-and-support/setting-background-and-drawing-colors/
---
## Introduktion

den dynamiska världen av .NET-utveckling framstår Aspose.CAD som ett kraftfullt verktyg för att hantera datorstödd design (CAD)-filer. Om du är ivrig att förbättra dina färdigheter i att manipulera CAD-ritningar, är den här handledningen din inkörsport. Vi kommer att fördjupa oss i krångligheterna med att ställa in bakgrund och rita färger med Aspose.CAD för .NET, vilket ger dig en steg-för-steg-guide som säkerställer tydlighet och effektivitet.

## Förutsättningar

Innan vi ger oss ut på denna resa, se till att du har följande förutsättningar på plats:

- Grundläggande förståelse för .NET-utveckling.
-  Installation av Aspose.CAD för .NET. Om du inte har gjort det ännu kan du ladda ner det[här](https://releases.aspose.com/cad/net/).
- Ett exempel på CAD-fil för experiment. Du kan hitta en i din dokumentkatalog.

## Importera namnområden

I ditt .NET-projekt börjar du med att importera de nödvändiga namnrymden:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Steg 1: Ladda CAD-filen

Börja med att ladda CAD-filen du vill arbeta med med hjälp av följande kodavsnitt:

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    // Din kod för vidare bearbetning kommer här
}
```

## Steg 2: Konfigurera rasteriseringsalternativ

 Skapa en instans av`CadRasterizationOptions` och ställ in dess egenskaper för bakgrunds- och ritfärgsinställning:

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.BackgroundColor = Color.Beige;
rasterizationOptions.DrawType = CadDrawTypeMode.UseDrawColor;
rasterizationOptions.DrawColor = Color.Blue;
```

## Steg 3: Exportera till PDF

 Skapa en instans av`PdfOptions` och ställ in`VectorRasterizationOptions` fast egendom:

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;

// Exportera CAD till PDF
image.Save(MyDir + "result_out.pdf", pdfOptions);
```

## Steg 4: Exportera till TIFF

 Skapa en instans av`TiffOptions` och ställ in`VectorRasterizationOptions` fast egendom:

```csharp
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.VectorRasterizationOptions = rasterizationOptions;

// Exportera CAD till TIFF
image.Save(MyDir + "result_out.tiff", tiffOptions);
```

## Slutsats

Grattis! Du har framgångsrikt lärt dig hur du ställer in bakgrunds- och ritfärger i Aspose.CAD för .NET. Denna handledning utrustar dig med färdigheter att manipulera CAD-filer utan ansträngning.

## FAQ's

### F1: Kan jag använda Aspose.CAD för .NET med någon typ av CAD-fil?

S1: Ja, Aspose.CAD stöder olika CAD-format, inklusive DWG, DXF och DGN.

### F2: Finns en gratis testversion tillgänglig för Aspose.CAD för .NET?

 A2: Ja, du kan utforska en gratis provperiod[här](https://releases.aspose.com/).

### F3: Var kan jag hitta detaljerad dokumentation för Aspose.CAD för .NET?

 A3: Se dokumentationen[här](https://reference.aspose.com/cad/net/).

### F4: Hur kan jag få tillfällig licens för Aspose.CAD?

 A4: Tillfälliga licenser kan erhållas[här](https://purchase.aspose.com/temporary-license/).

### F5: Behöver du hjälp eller vill få kontakt med samhället?

 S5: Besök supportforumet[här](https://forum.aspose.com/c/cad/19).
