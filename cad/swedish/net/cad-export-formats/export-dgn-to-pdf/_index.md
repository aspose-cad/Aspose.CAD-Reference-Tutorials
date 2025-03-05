---
title: Exportera DGN till PDF i Aspose.CAD för .NET
linktitle: Exportera DGN till PDF
second_title: Aspose.CAD .NET - CAD- och BIM-filformat
description: Lär dig hur du exporterar DGN-filer till PDF utan ansträngning med Aspose.CAD för .NET. En steg-för-steg-guide för sömlös CAD-filmanipulation.
type: docs
weight: 12
url: /sv/net/cad-export-formats/export-dgn-to-pdf/
---
## Introduktion

I en värld av .NET-utveckling är Aspose.CAD ett kraftfullt bibliotek som underlättar manipulering och konvertering av CAD-filer. En vanlig uppgift som utvecklare ofta stöter på är att exportera DGN-filer till PDF-format. I den här handledningen går vi igenom processen steg för steg, med hjälp av Aspose.CAD för .NET.

## Förutsättningar

Innan du dyker in i handledningen, se till att du har följande på plats:

- En praktisk kunskap om C# och .NET-ramverket.
-  Aspose.CAD för .NET-biblioteket installerat. Du kan ladda ner den[här](https://releases.aspose.com/cad/net/).
- Ett exempel på DGN-fil, till exempel "Nikon_D90_Camera.dgn" för denna handledning.

## Importera namnområden

I ditt C#-projekt börjar du med att importera de nödvändiga namnrymden:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Steg 1: Ladda DGN-fil

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage cadImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Din kod här...
}
```

## Steg 2: Konfigurera rasteriseringsalternativ

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## Steg 3: Skapa PDF-alternativ

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Steg 4: Spara som PDF

```csharp
cadImage.Save(MyDir + "ExportDGNToPdf_out.pdf", pdfOptions);
```

## Slutsats

Grattis! Du har framgångsrikt exporterat en DGN-fil till PDF med Aspose.CAD för .NET. Denna handledning täckte de väsentliga stegen, från att ladda DGN-filen till att konfigurera rastreringsalternativ och spara utdata som en PDF.

## FAQ's

### F1: Kan jag använda Aspose.CAD för .NET utan förkunskaper om CAD?

A1: Absolut! Aspose.CAD förenklar komplexa CAD-uppgifter, vilket gör det tillgängligt för utvecklare med olika bakgrunder.

### F2: Var kan jag hitta fler exempel och dokumentation för Aspose.CAD?

 A2: Utforska[dokumentation](https://reference.aspose.com/cad/net/) för omfattande guider och exempel.

### F3: Finns det en gratis testversion tillgänglig för Aspose.CAD?

A3: Ja, du kan få en gratis provperiod[här](https://releases.aspose.com/).

### F4: Hur kan jag få tillfälliga licenser för Aspose.CAD?

 A4: Skaffa tillfälliga licenser[här](https://purchase.aspose.com/temporary-license/).

### F5: Behöver du hjälp eller har frågor?

A5: Besök[Aspose.CAD-forum](https://forum.aspose.com/c/cad/19) för samhällsstöd.