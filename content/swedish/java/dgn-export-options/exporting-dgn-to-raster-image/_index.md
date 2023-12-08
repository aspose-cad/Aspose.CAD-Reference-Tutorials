---
title: Java DGN till JPEG-konvertering med Aspose.CAD Tutorial
linktitle: Exportera DGN i AutoCAD-format till rasterbildsformat
second_title: Aspose.CAD Java API
description: Lär dig hur du exporterar DGN-filer till JPEG-bilder i Java med Aspose.CAD. Denna steg-för-steg handledning guidar dig genom processen utan ansträngning.
type: docs
weight: 13
url: /sv/java/dgn-export-options/exporting-dgn-to-raster-image/
---
## Introduktion

Välkommen till denna omfattande handledning om att exportera DGN (Design)-filer till Raster Image Format med Aspose.CAD för Java. Aspose.CAD är ett kraftfullt bibliotek som gör det möjligt för Java-utvecklare att arbeta med CAD-filer sömlöst. I den här handledningen guidar vi dig genom processen att konvertera DGN-filer till JPEG-bilder, vilket ger dig steg-för-steg-instruktioner och kodexempel.

## Förutsättningar

Innan du dyker in i handledningen, se till att du har följande förutsättningar på plats:
1.  Aspose.CAD Library: Se till att du har Aspose.CAD för Java-biblioteket installerat. Du kan ladda ner den[här](https://releases.aspose.com/cad/java/).
2. Java Development Kit (JDK): Se till att du har Java installerat på din maskin.
3. Integrated Development Environment (IDE): Använd en Java-kompatibel IDE som IntelliJ eller Eclipse.

## Importera paket

Importera nödvändiga paket för Aspose.CAD i ditt Java-projekt. Lägg till följande rader i din kod:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
```

## Steg 1: Ladda DGN-fil

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
DgnImage dgnImage = (DgnImage) Image.load(dataDir + "Nikon_D90_Camera.dgn");
```

## Steg 2: Skapa JpegOptions-objekt

```java
ImageOptionsBase options = new JpegOptions();
```

## Steg 3: Tilldela rasteriseringsalternativ

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(600);
vectorOptions.setPageHeight(400);
vectorOptions.setNoScaling(true);
vectorOptions.setAutomaticLayoutsScaling(false);
options.setVectorRasterizationOptions(vectorOptions);
```

## Steg 4: Spara den konverterade bilden

```java
OutputStream outStream = new FileOutputStream(dataDir + "ExportDGNToRasterImage_Out.jpg");
dgnImage.save(outStream, options);
```

Upprepa dessa steg för dina specifika DGN-filer och justera filsökvägarna därefter.

## Slutsats

Grattis! Du har framgångsrikt lärt dig hur du exporterar DGN-filer till rasterbildformat med Aspose.CAD för Java. Denna handledning har utrustat dig med kunskapen för att införliva den här funktionen i dina Java-applikationer.

## FAQ's

### F1: Kan jag använda Aspose.CAD för Java med andra CAD-filformat?

S1: Ja, Aspose.CAD stöder olika CAD-format, vilket ger en mångsidig lösning för Java-utvecklare.

### F2: Finns det en gratis testversion tillgänglig för Aspose.CAD för Java?

 A2: Ja, du kan få tillgång till en gratis provperiod[här](https://releases.aspose.com/).

### F3: Var kan jag hitta dokumentation för Aspose.CAD för Java?

 A3: Se dokumentationen[här](https://reference.aspose.com/cad/java/).

### F4: Hur kan jag få support för Aspose.CAD för Java?

 S4: Besök supportforumet[här](https://forum.aspose.com/c/cad/19).

### F5: Var kan jag köpa en licens för Aspose.CAD för Java?

 A5: Du kan köpa en licens[här](https://purchase.aspose.com/buy).