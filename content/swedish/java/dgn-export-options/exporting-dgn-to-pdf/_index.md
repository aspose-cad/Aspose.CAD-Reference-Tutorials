---
title: Enkel DGN till AutoCAD PDF-export med Aspose.CAD för Java
linktitle: Exportera DGN i AutoCAD-format till PDF
second_title: Aspose.CAD Java API
description: Utforska steg-för-steg-guiden för att exportera DGN-filer till AutoCAD-format i PDF med Aspose.CAD för Java. Förhöj din Java-applikations CAD-hanteringsmöjligheter utan ansträngning.
type: docs
weight: 12
url: /sv/java/dgn-export-options/exporting-dgn-to-pdf/
---
## Introduktion

Välkommen till denna omfattande handledning om hur du använder Aspose.CAD för Java för att exportera DGN-filer i AutoCAD-format till PDF. Om du vill förbättra din Java-applikations förmåga att hantera CAD-filer, är Aspose.CAD ett utmärkt val. I den här handledningen guidar vi dig genom processen att exportera DGN-filer steg för steg.


## Förutsättningar
Innan vi dyker in i handledningen, se till att du har följande förutsättningar:
-  Aspose.CAD Library: Se till att du har Aspose.CAD-biblioteket för Java installerat. Du kan ladda ner den[här](https://releases.aspose.com/cad/java/).
- Dokumentkatalog: Skapa en dokumentkatalog där dina in- och utdatafiler kommer att lagras.

## Importera paket

I ditt Java-projekt, importera de nödvändiga paketen för att komma åt Aspose.CAD-funktioner:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Låt oss nu dela upp exempelkoden i flera steg:

## Steg 1: Definiera filsökvägar

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

Se till att ersätta "Din dokumentkatalog" med den faktiska sökvägen där dina filer finns.

## Steg 2: Ladda DGN-bild

```java
DgnImage objImage = (DgnImage) Image.load(fileName);
```

Ladda DGN-filen med Aspose.CAD.

## Steg 3: Ställ in PDF-exportalternativ

```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); // Exportera specifika vyer
options.setVectorRasterizationOptions(vectorOptions);
```

Definiera PDF-exportalternativen, inklusive siddimensioner och layoutinställningar.

## Steg 4: Spara PDF-fil

```java
objImage.save(outFile, options);
```

Spara den exporterade PDF-filen.

Upprepa dessa steg för eventuella ytterligare DGN-filer som du vill konvertera. Grattis! Du har framgångsrikt exporterat DGN-filer till AutoCAD-format i PDF med Aspose.CAD för Java.

## Slutsats

den här handledningen undersökte vi hur man kan utnyttja Aspose.CAD för Java för att förbättra din applikations CAD-filhanteringsmöjligheter. Med lätta att följa steg och kodexempel kan du nu sömlöst exportera DGN-filer till AutoCAD-format i PDF.

## FAQ's

### F1: Är Aspose.CAD kompatibel med alla CAD-filformat?

S1: Ja, Aspose.CAD stöder ett brett utbud av CAD-format, vilket säkerställer mångsidighet vid hantering av olika filtyper.

### F2: Kan jag anpassa PDF-exportinställningarna?

A2: Absolut. Som visas i handledningen kan du justera alternativ som siddimensioner och layouter för att passa dina krav.

### F3: Var kan jag hitta ytterligare stöd eller hjälp?

 A3: Besök[Aspose.CAD-forum](https://forum.aspose.com/c/cad/19) för samhällsstöd och diskussioner.

### F4: Finns det en gratis provperiod?

 A4: Ja, du kan komma åt den kostnadsfria provperioden[här](https://releases.aspose.com/).

### F5: Hur kan jag få en tillfällig licens?

 A5: Skaffa en tillfällig licens[här](https://purchase.aspose.com/temporary-license/).