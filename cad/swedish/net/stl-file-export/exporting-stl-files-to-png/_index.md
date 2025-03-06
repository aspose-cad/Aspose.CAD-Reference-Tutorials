---
title: STL till PNG-konvertering på ett enkelt sätt med Aspose.CAD för .NET
linktitle: Exportera STL-filer till PNG
second_title: Aspose.CAD .NET - CAD- och BIM-filformat
description: Konvertera enkelt STL-filer till PNG med Aspose.CAD för .NET. Följ vår steg-för-steg-guide för sömlös integration. Ladda ner nu!
weight: 10
url: /sv/net/stl-file-export/exporting-stl-files-to-png/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# STL till PNG-konvertering på ett enkelt sätt med Aspose.CAD för .NET

## Introduktion
I den dynamiska världen av datorstödd design (CAD) är effektiv filkonvertering avgörande. Aspose.CAD för .NET är en kraftfull verktygslåda som förenklar processen att exportera STL-filer till PNG, vilket ger utvecklare den flexibilitet och funktionalitet de behöver. Denna handledning guidar dig genom processen steg för steg, vilket säkerställer en smidig övergång från STL till PNG med Aspose.CAD.
## Förutsättningar
Innan vi dyker in i handledningen, se till att du har följande på plats:
1.  Aspose.CAD för .NET: Ladda ner och installera Aspose.CAD-biblioteket. Du kan hitta den[här](https://releases.aspose.com/cad/net/).
2. Utvecklingsmiljö: Konfigurera din föredragna .NET-utvecklingsmiljö.
3. STL-fil: Ha en STL-fil redo för konvertering. För den här handledningen använder vi en exempelfil med namnet "galeon.stl."
## Importera namnområden
För att starta processen, importera de nödvändiga namnområdena i din .NET-applikation. Detta säkerställer att du har tillgång till de klasser och metoder som krävs för STL till PNG-konvertering.
```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```
## Steg 1: Definiera katalog och källfilssökväg
```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "galeon.stl";
```
Se till att du ersätter "Din dokumentkatalog" med den faktiska katalogsökvägen där din STL-fil finns.
## Steg 2: Ladda CAD-bilden
```csharp
using (var cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Ytterligare steg kommer att utföras inom detta block
}
```
Detta steg laddar STL-filen som en CAD-bild, så att du kan manipulera och exportera den.
## Steg 3: Ställ in rasteriseringsalternativ
```csharp
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 100;
rasterizationOptions.PageHeight = 100;
```
Justera sidans bredd och höjd enligt dina önskemål och krav. Dessa inställningar bestämmer dimensionerna för den exporterade PNG:en.
## Steg 4: Konfigurera PNG-alternativ
```csharp
PngOptions pngOptions = new PngOptions();
pngOptions.VectorRasterizationOptions = rasterizationOptions;
```
Skapa PNG-alternativ, med rastreringsinställningarna som definierats i föregående steg.
## Steg 5: Spara PNG-filen
```csharp
string outPath = sourceFilePath + ".png";
cadImage.Save(outPath, pngOptions);
```
Ange utdatasökvägen för PNG-filen och spara CAD-bilden i PNG-format med hjälp av de angivna alternativen.
Upprepa dessa steg efter behov för ditt specifika användningsfall, så kommer du att framgångsrikt exportera STL-filer till PNG med Aspose.CAD för .NET.
## Slutsats
Aspose.CAD för .NET förenklar den komplicerade uppgiften att konvertera STL-filer till PNG, vilket ger utvecklare en tillförlitlig verktygslåda. Genom att följa denna steg-för-steg-guide kan du sömlöst integrera denna funktion i dina applikationer.
## Vanliga frågor
### F: Kan jag anpassa dimensionerna för den exporterade PNG:en?
 Absolut! Justera i steg 3`PageWidth` och`PageHeight` värden för att möta dina specifika krav.
### F: Finns en tillfällig licens tillgänglig för teständamål?
 Ja, du kan få en tillfällig licens[här](https://purchase.aspose.com/temporary-license/) för testning och utvärdering.
### F: Var kan jag hitta ytterligare stöd eller diskussioner i samhället?
 Besök[Aspose.CAD-forum](https://forum.aspose.com/c/cad/19) för stöd och samarbetsdiskussioner.
### F: Finns det andra filformat som stöds för konvertering?
 Ja, Aspose.CAD stöder olika CAD-format utöver STL. Referera till[dokumentation](https://reference.aspose.com/cad/net/) för en omfattande lista.
### F: Kan jag batchbearbeta flera STL-filer?
Säkert! Implementera en loop baserad på de angivna stegen för att batchbearbeta flera STL-filer.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
