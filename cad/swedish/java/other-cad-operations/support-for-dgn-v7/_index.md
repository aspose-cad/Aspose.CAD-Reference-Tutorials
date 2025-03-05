---
title: DGN till PDF-konverteringsguide - Aspose.CAD för Java
linktitle: Stöd för DGN V7
second_title: Aspose.CAD Java API
description: Konvertera enkelt DGN-filer till PDF med Aspose.CAD för Java. Följ vår steg-för-steg-guide för sömlös integration och effektivt arbetsflöde.
type: docs
weight: 11
url: /sv/java/other-cad-operations/support-for-dgn-v7/
---
## Introduktion

I den dynamiska världen av CAD (Computer Aided Design) är effektiv konvertering av DGN (Design)-filer till PDF (Portable Document Format) ett avgörande krav. Aspose.CAD för Java framstår som en kraftfull lösning som erbjuder sömlös integration och robusta möjligheter. Denna steg-för-steg-guide syftar till att leda dig genom processen att exportera DGN-filer till PDF med Aspose.CAD för Java, vilket säkerställer ett smidigt och effektivt arbetsflöde.

## Förutsättningar

Innan du dyker in i handledningen, se till att du har följande förutsättningar på plats:
-  Aspose.CAD för Java Library: Ladda ner och installera biblioteket från[Aspose.CAD för Java Nedladdningssida](https://releases.aspose.com/cad/java/).
- Java-utvecklingsmiljö: Se till att du har en Java-utvecklingsmiljö inställd på din maskin.

## Importera paket

Börja med att importera de nödvändiga paketen till ditt Java-projekt:

## Steg 1: Importera nödvändiga paket

Importera de nödvändiga paketen för Aspose.CAD för Java i ditt Java-projekt.
```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.cadobjects.DgnImage;
import com.aspose.cad.imageoptions.PdfOptions;
import java.awt.Color;
```

## Steg 2: Ställ in filsökvägar

Definiera sökvägarna för din indata-DGN-fil och utdata-PDF-filen.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

## Steg 3: Ladda DGN-bild

Ladda DGN-bilden med Aspose.CAD-biblioteket.

```java
DgnImage objImage = (DgnImage)Image.load(fileName);
```

## Steg 4: Konfigurera PDF-exportalternativ

Ställ in alternativ för export till PDF, inklusive siddimensioner, automatisk layoutskalning, bakgrundsfärg och specifika layouter att exportera.

```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setBackgroundColor(Color.getBlack());
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); //exportera endast 4 (1,2,3 och 9) visningar
options.setVectorRasterizationOptions(vectorOptions);
```

## Steg 5: Spara PDF-fil

Spara DGN-bilden som en PDF-fil med de angivna alternativen.

```java
objImage.save(outFile, options);
```

Upprepa dessa steg för olika DGN-filer, justera filsökvägar och alternativ efter behov.

## Slutsats

Med Aspose.CAD för Java blir det en enkel process att konvertera DGN-filer till PDF. Den här guiden utrustar dig med kunskapen för att sömlöst integrera biblioteket i dina Java-projekt, vilket underlättar effektiva CAD-filkonverteringar.

## FAQ's

### F1: Kan jag använda Aspose.CAD för Java med andra CAD-filformat?

S1: Ja, Aspose.CAD stöder olika CAD-format, vilket ger mångsidig funktionalitet utöver DGN till PDF-konvertering.

### F2: Finns en tillfällig licens tillgänglig för Aspose.CAD för Java?

 A2: Ja, du kan få en tillfällig licens[här](https://purchase.aspose.com/temporary-license/) för teständamål.

### F3: Hur kan jag söka support eller ställa frågor om Aspose.CAD för Java?

 A3: Besök[Aspose.CAD-forum](https://forum.aspose.com/c/cad/19)att få kontakt med samhället och söka hjälp.

### F4: Vilka layouter kan jag exportera när jag konverterar DGN till PDF?

 S4: Du kan ange layouterna som ska exporteras genom att anpassa`setLayouts` array i koden.

### F5: Var kan jag hitta omfattande dokumentation för Aspose.CAD för Java?

 A5: Se[Aspose.CAD för Java-dokumentation](https://reference.aspose.com/cad/java/) för detaljerad information.