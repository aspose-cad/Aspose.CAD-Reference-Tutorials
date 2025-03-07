---
title: Exportera IFC-filer till PNG - Aspose.CAD Tutorial
linktitle: Exportera IFC-filer till PNG
second_title: Aspose.CAD .NET - CAD- och BIM-filformat
description: Utforska Aspose.CAD för .NET, en robust lösning för sömlös IFC till PNG-konvertering. Ladda ner nu för effektiv CAD-filbehandling.
weight: 10
url: /sv/net/exporting-to-image-formats/exporting-ifc-files-to-png/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportera IFC-filer till PNG - Aspose.CAD Tutorial

## Introduktion

den dynamiska världen av datorstödd design (CAD) är effektiv filkonvertering avgörande. Aspose.CAD för .NET framstår som ett kraftfullt verktyg som erbjuder sömlösa möjligheter för export av IFC-filer (Industry Foundation Classes) till PNG-format. Denna steg-för-steg handledning guidar dig genom processen, vilket säkerställer en smidig upplevelse med Aspose.CAD.

## Förutsättningar

Innan du dyker in i handledningen, se till att du har följande förutsättningar på plats:

### 1. Aspose.CAD-installation

 Se till att du har Aspose.CAD för .NET installerat. Du kan ladda ner den från releasesidan[här](https://releases.aspose.com/cad/net/).

### 2. Dokumentkatalog

 Skapa en avsedd katalog för dina dokument. I det angivna exemplet, variabeln`MyDir` representerar dokumentkatalogen.

## Importera namnområden

Nu när du har ställt in förutsättningarna, låt oss importera de nödvändiga namnområdena i din .NET-applikation för att använda Aspose.CAD-funktioner.

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using Aspose.CAD.FileFormats.Ifc;
```

## Steg 1: Ladda IFC-fil

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "example.ifc";
using (IfcImage cadImage = (IfcImage)Image.Load(sourceFilePath))
{
```

 I det här steget initierar vi Aspose.CAD`IfcImage` objekt och ladda in IFC-filen i den.

## Steg 2: Ställ in rasteriseringsalternativ

```csharp
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
   
    rasterizationOptions.PageWidth = 100;
    rasterizationOptions.PageHeight = 100;
```

Definiera rastreringsalternativ för att konfigurera sidbredden och höjden för PNG-utdata.

## Steg 3: Ställ in PNG-alternativ

```csharp
    PngOptions pngOptions = new PngOptions();
    pngOptions.VectorRasterizationOptions = rasterizationOptions;
```

Skapa PNG-alternativ och associera de tidigare definierade rastreringsalternativen.

## Steg 4: Ange utdatasökväg

```csharp
    // Ställ också in utmatningsväg
    string outPath = sourceFilePath + ".png";
    cadImage.Save(outPath, pngOptions);
}
```

Definiera utdatasökvägen för PNG-filen och se till att den har samma namn som källfilen med tillägget ".png". Slutligen, spara den konverterade bilden.

## Slutsats

Med dessa enkla steg har du framgångsrikt exporterat en IFC-fil till PNG med Aspose.CAD för .NET. Detta mångsidiga verktyg förenklar CAD-konverteringsprocessen och gör den tillgänglig för utvecklare och ingenjörer.

## FAQ's

### F1: Kan jag använda Aspose.CAD för .NET på macOS eller Linux?

S1: Nej, Aspose.CAD för .NET är speciellt designat för Windows-miljöer.

### F2: Är en tillfällig licens tillgänglig för teständamål?

 A2: Ja, du kan få en tillfällig licens från[här](https://purchase.aspose.com/temporary-license/) för utvärdering.

### F3: Hur kan jag få support för Aspose.CAD?

 A3: Besök[Aspose.CAD-forum](https://forum.aspose.com/c/cad/19) för samhällsstöd och diskussioner.

### F4: Var kan jag hitta omfattande dokumentation?

 A4: Se[Aspose.CAD-dokumentation](https://reference.aspose.com/cad/net/) för detaljerad information och exempel.

### F5: Vad händer om jag stöter på problem under installationen?

 S5: Kontrollera dokumentationen eller sök hjälp om[Aspose.CAD-forum](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
