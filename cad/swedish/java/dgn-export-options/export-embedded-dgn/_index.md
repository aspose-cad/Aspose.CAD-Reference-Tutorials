---
title: Exportera inbäddad DGN till PDF med Aspose.CAD för Java
linktitle: Exportera inbäddad DGN
second_title: Aspose.CAD Java API
description: Utforska steg-för-steg-guiden för att exportera inbäddade DGN-filer till PDF med Aspose.CAD för Java. Förbättra dina Java-applikationer med sömlös CAD-filmanipulation.
weight: 11
url: /sv/java/dgn-export-options/export-embedded-dgn/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportera inbäddad DGN till PDF med Aspose.CAD för Java

## Introduktion

Välkommen till denna omfattande handledning om att exportera inbäddade DGN-filer med Aspose.CAD för Java. Aspose.CAD är ett kraftfullt bibliotek som gör det möjligt för Java-utvecklare att arbeta med CAD-filer sömlöst. I den här handledningen guidar vi dig genom processen att exportera inbäddade DGN-filer till PDF med steg-för-steg-instruktioner. Oavsett om du är en erfaren utvecklare eller precis har börjat, hjälper den här handledningen dig att utnyttja funktionerna i Aspose.CAD för att förbättra dina Java-applikationer.

## Förutsättningar

Innan vi dyker in i handledningen, se till att du har följande förutsättningar:
- Java-utvecklingsmiljö: Se till att du har en Java-utvecklingsmiljö inställd på din maskin.
-  Aspose.CAD for Java: Ladda ner och installera Aspose.CAD for Java-biblioteket från[här](https://releases.aspose.com/cad/java/).

## Importera paket

För att komma igång måste du importera nödvändiga paket i ditt Java-projekt. Lägg till följande importsatser till din kod:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Låt oss nu dela upp exempelkoden i flera steg:

## Steg 1: Ställ in in- och utmatningsvägar

Definiera katalogsökvägen där ditt dokument finns och ange DWG-filnamnet.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
```

## Steg 2: Ladda DWG-fil

 Ladda DWG-filen i en`Image` objekt med Aspose.CAD.

```java
Image objImage = Image.load(fileName);
```

## Steg 3: Konfigurera rasteriseringsalternativ

Konfigurera rastreringsalternativ, till exempel layouter som ska inkluderas i exporten.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setLayouts(new String[] {"Model"});
```

## Steg 4: Konfigurera PDF-alternativ

Ställ in PDF-alternativ, inklusive vektorrasteriseringsalternativ.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Steg 5: Spara PDF-fil

Spara PDF-filen med de konfigurerade alternativen.
```java
objImage.save(dataDir + "BlockRefDgn.pdf", pdfOptions);
```

## Slutsats

Grattis! Du har framgångsrikt exporterat en inbäddad DGN-fil till PDF med Aspose.CAD för Java. Denna handledning täckte de väsentliga stegen för att integrera Aspose.CAD i din Java-applikation för effektiv CAD-filmanipulation.

## FAQ's

### F1: Kan jag använda Aspose.CAD för Java i ett kommersiellt projekt?

 S1: Ja, Aspose.CAD för Java är ett kommersiellt bibliotek. Du kan få en licens från[här](https://purchase.aspose.com/buy).

### F2: Finns det en gratis provperiod?

 S2: Ja, du kan få tillgång till en gratis testversion av Aspose.CAD för Java[här](https://releases.aspose.com/).

### F3: Hur kan jag få support för Aspose.CAD för Java?

S3: Du kan söka stöd från Aspose.CAD-communityt på[forum](https://forum.aspose.com/c/cad/19).

### F4: Vad händer om jag behöver en tillfällig licens?

 S4: Du kan få en tillfällig licens[här](https://purchase.aspose.com/temporary-license/).

### F5: Var kan jag hitta dokumentationen?

 S5: Dokumentationen finns tillgänglig[här](https://reference.aspose.com/cad/java/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
