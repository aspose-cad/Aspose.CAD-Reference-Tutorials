---
title: Exportera till PDF med Aspose.CAD för Java
linktitle: Exportera till PDF
second_title: Aspose.CAD Java API
description: Lär dig hur du exporterar CAD-filer till PDF utan ansträngning med Aspose.CAD för Java. Följ vår steg-för-steg-guide för sömlös integration.
type: docs
weight: 13
url: /sv/java/cad-export-options/export-to-pdf/
---
## Introduktion

Välkommen till denna omfattande handledning om att exportera CAD-filer till PDF med Aspose.CAD för Java. Om du letar efter att sömlöst konvertera dina CAD-ritningar till det allmänt stödda PDF-formatet, är du på rätt plats. I den här steg-för-steg-guiden kommer vi att bryta ner processen och se till att du förstår varje steg för att uppnå framgångsrik PDF-export.

## Förutsättningar

Innan du dyker in i handledningen, se till att du har följande förutsättningar på plats:

-  Aspose.CAD för Java: Se till att du har Aspose.CAD-biblioteket installerat i din Java-miljö. Du kan ladda ner den[här](https://releases.aspose.com/cad/java/).

- Resurskatalog: Skapa en katalog där dina CAD-filer lagras. Ersätt "Din dokumentkatalog" i det medföljande kodavsnittet med den faktiska sökvägen.

Låt oss nu gå vidare till huvudstegen.

## Importera namnområden

I ditt Java-projekt börjar du med att importera de nödvändiga namnområdena för att möjliggöra användningen av Aspose.CAD-funktioner.

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterpolationMode;
import com.aspose.cad.SmoothingMode;
import com.aspose.cad.TextRenderingHint;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//importera com.aspose.cad.imageoptions.TypeOfEntities;
```

## Steg 1: Ladda CAD-fil

Ladda din CAD-fil i Aspose.CAD Image-objektet. Ersätt "site.dwf" med ditt faktiska CAD-filnamn.

```java
String fileName = (dataDir + "site.dwf");
Image image = Image.load(fileName);
```

## Steg 2: Konfigurera PDF-alternativ

Ställ in alternativen för PDF-export, inklusive vektorrastreringsalternativ som sidhöjd, bredd och layouter.

```java
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);

rasterizationOptions.setPageHeight(500);
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setLayouts(new String[] { "Model" });
```

## Steg 3: Exportera till PDF

Ange utdatasökvägen för den genererade PDF-filen och spara bilden med de konfigurerade PDF-alternativen.

```java
String outPath = dataDir + "site.pdf";
image.save(outPath, pdfOptions);
```

Grattis! Du har framgångsrikt exporterat din CAD-fil till en PDF med Aspose.CAD för Java.

## Slutsats

I den här handledningen utforskade vi steg-för-steg-processen för att exportera CAD-filer till PDF med Aspose.CAD för Java. Genom att följa dessa enkla men effektiva steg kan du sömlöst integrera denna funktion i dina Java-applikationer.

## FAQ's

### F1: Är Aspose.CAD kompatibel med alla CAD-filformat?

S1: Ja, Aspose.CAD stöder ett brett utbud av CAD-format, vilket säkerställer kompatibilitet med olika designprogram.

### F2: Kan jag anpassa inställningarna för PDF-utdata?

A2: Absolut. Handledningen ger en glimt av anpassningsalternativen, men du kan utforska vidare för att skräddarsy resultatet efter dina behov.

### F3: Var kan jag hitta ytterligare stöd för Aspose.CAD?

 S3: För eventuella frågor eller problem, besök[Aspose.CAD-forum](https://forum.aspose.com/c/cad/19) att söka hjälp från samhället.

### F4: Finns det en gratis provperiod?

 S4: Ja, du kan få tillgång till en gratis provversion av Aspose.CAD[här](https://releases.aspose.com/).

### F5: Hur kan jag få en tillfällig licens för Aspose.CAD?

 A5: För tillfällig licensiering, besök[den här länken](https://purchase.aspose.com/temporary-license/).