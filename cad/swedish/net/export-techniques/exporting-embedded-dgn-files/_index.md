---
title: Exportera inbäddade DGN-filer - Aspose.CAD Tutorial
linktitle: Exportera inbäddade DGN-filer
second_title: Aspose.CAD .NET - CAD- och BIM-filformat
description: Utforska kraften i Aspose.CAD för .NET. Lär dig att exportera inbäddade DGN-filer till PDF utan ansträngning med denna steg-för-steg handledning.
weight: 14
url: /sv/net/export-techniques/exporting-embedded-dgn-files/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportera inbäddade DGN-filer - Aspose.CAD Tutorial

## Introduktion

den dynamiska världen av mjukvaruutveckling utmärker sig Aspose.CAD för .NET som ett kraftfullt verktyg för att hantera datorstödd design (CAD)-filer. Denna handledning guidar dig genom processen att exportera inbäddade DGN-filer med Aspose.CAD för .NET. Oavsett om du är en erfaren utvecklare eller en nyfiken nybörjare, kommer den här steg-för-steg-guiden att hjälpa dig att utnyttja funktionerna i Aspose.CAD effektivt.

## Förutsättningar

Innan du dyker in i handledningen, se till att du har följande förutsättningar på plats:

1.  Aspose.CAD för .NET: Ladda ner och installera biblioteket från[Aspose.CAD för .NET](https://releases.aspose.com/cad/net/).

2. Utvecklingsmiljö: Konfigurera en .NET-utvecklingsmiljö med Visual Studio eller någon annan föredragen IDE.

3. Exempel på DXF-fil: För den här handledningen använder vi filen "conic_pyramid.dxf". Se till att du har den tillgänglig i din utsedda dokumentkatalog.

## Importera namnområden

Se till att importera de nödvändiga namnrymden i din C#-kod:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
```

## Steg 1: Ladda DXF-filen

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    //Din kod för ytterligare steg kommer här
}
```

## Steg 2: Ställ in rasteriseringsalternativ

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new[] { "Model" };
```

## Steg 3: Ställ in PDF-alternativ

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Steg 4: Spara som PDF

```csharp
cadImage.Save(MyDir + "conic_pyramid.pdf", pdfOptions);
```

## Steg 5: Visa framgångsmeddelande

```csharp
Console.WriteLine("\nThe DXF drawing exported successfully to PDF.\nFile saved at " + MyDir);
```

## Slutsats

Grattis! Du har framgångsrikt exporterat en inbäddad DGN-fil till PDF med Aspose.CAD för .NET. Denna handledning täckte de väsentliga stegen och gav dig en grund för att utforska mer avancerade funktioner som erbjuds av Aspose.CAD.

## FAQ's

### F1: Kan jag använda Aspose.CAD för .NET med andra programmeringsspråk?

S1: Aspose.CAD stöder i första hand .NET, men Aspose tillhandahåller bibliotek för olika språk, inklusive Java och Python.

### F2: Finns det en gratis testversion tillgänglig för Aspose.CAD för .NET?

 A2: Ja, du kan få en gratis provperiod från[här](https://releases.aspose.com/).

### F3: Var kan jag hitta omfattande dokumentation för Aspose.CAD för .NET?

 A3: Se dokumentationen[här](https://reference.aspose.com/cad/net/).

### F4: Hur får jag tillfällig licens för Aspose.CAD för .NET?

 A4: Skaffa en tillfällig licens[här](https://purchase.aspose.com/temporary-license/).

### F5: Behöver du hjälp eller vill engagera dig i samhället?

A5: Besök[Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) för stöd och diskussioner.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
