---
title: Ställa in bakgrund och rita färg med Aspose.CAD för Java
linktitle: Ställa in bakgrund och ritfärg
second_title: Aspose.CAD Java API
description: Konvertera enkelt CAD-filer till PDF och TIFF med Aspose.CAD för Java. Ställ in anpassade bakgrunds- och ritfärger för visuellt fantastiska resultat.
type: docs
weight: 15
url: /sv/java/advanced-cad-features/setting-background-and-drawing-color/
---
## Introduktion

den dynamiska världen av datorstödd design (CAD) är effektiv filkonvertering avgörande för sömlöst samarbete och kommunikation. Aspose.CAD för Java framstår som ett kraftfullt verktyg som erbjuder robusta möjligheter för att konvertera CAD-filer till PDF- och TIFF-format. I den här handledningen kommer vi att fördjupa oss i processen att ställa in bakgrund och rita färg med Aspose.CAD för Java, vilket ger dig en steg-för-steg-guide för optimala resultat.

## Förutsättningar

Innan vi ger oss ut på denna resa, se till att du har följande förutsättningar på plats:

-  Aspose.CAD for Java Library: Se till att du har Aspose.CAD for Java-biblioteket installerat. Du kan ladda ner den[här](https://releases.aspose.com/cad/java/).

-  Dokumentkatalog: Ha en dedikerad katalog för dina CAD-filer. Byta ut`"Your Document Directory" + "CADConversion/"` med sökvägen till din katalog.

Låt oss nu dyka in i processen.

## Importera namnområden

Se till att du importerar de nödvändiga namnområdena för att utnyttja funktionerna i Aspose.CAD för Java. I vårt exempel använder vi följande:

```java
import java.awt.Color;
import java.awt.Image;

import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## Steg 1: Ladda CAD-fil

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image objImage = Image.load(srcFile);
```

## Steg 2: Ställ in bakgrunds- och ritfärg

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setBackgroundColor(com.aspose.cad.Color.getBeige());
rasterizationOptions.setDrawType(CadDrawTypeMode.UseDrawColor);
rasterizationOptions.setBackgroundColor(com.aspose.cad.Color.getBlue());
```

## Steg 3: Skapa PDF och spara

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

## Steg 4: Skapa TIFF och spara

```java
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

Följ dessa steg noggrant för att uppnå optimala resultat vid konvertering av CAD till PDF och TIFF med Aspose.CAD för Java.

## Slutsats

Aspose.CAD för Java ger utvecklare en mångsidig verktygsuppsättning för CAD-filmanipulation. Genom att bemästra krångligheterna med att ställa in bakgrund och rita färg, förbättrar du din förmåga att producera visuellt tilltalande och korrekta omvandlingar.

## FAQ's

### F1: Är Aspose.CAD för Java lämplig för masskonverteringar?

A1: Absolut! Aspose.CAD för Java utmärker sig i bulkkonverteringar, vilket ger effektivitet och noggrannhet.

### F2: Kan jag anpassa bakgrundsfärgen i de genererade filerna?

S2: Ja, handledningen visar hur man ställer in anpassade bakgrundsfärger för både PDF- och TIFF-utdata.

### F3: Var kan jag hitta omfattande dokumentation för Aspose.CAD för Java?

 A3: Se[dokumentation](https://reference.aspose.com/cad/java/) för djupgående insikter och exempel.

### F4: Finns det en gratis provperiod?

 S4: Ja, utforska funktionerna med[gratis provperiod](https://releases.aspose.com/).

### F5: Hur kan jag få support för Aspose.CAD för Java?

A5: Besök[Aspose.CAD-forum](https://forum.aspose.com/c/cad/19) att söka hjälp och engagera sig i samhället.
