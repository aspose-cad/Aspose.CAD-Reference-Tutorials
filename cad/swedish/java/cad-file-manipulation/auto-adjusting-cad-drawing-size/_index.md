---
title: Autojustering av CAD-ritningsstorlek med Aspose.CAD för Java
linktitle: Autojustering av CAD-ritningsstorlek
second_title: Aspose.CAD Java API
description: Utforska den sömlösa processen att automatiskt justera CAD-ritningsstorlekar i Java med Aspose.CAD. Följ vår steg-för-steg-guide för effektiv CAD-filmanipulation.
weight: 13
url: /sv/java/cad-file-manipulation/auto-adjusting-cad-drawing-size/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Autojustering av CAD-ritningsstorlek med Aspose.CAD för Java

## Introduktion

I CAD-världen (Computer Aided Design) är justering av ritstorlekar ett vanligt krav, och med Aspose.CAD för Java blir det en sömlös process. Detta kraftfulla bibliotek tillhandahåller omfattande verktyg för att hantera CAD-filer i Java-applikationer. I den här handledningen kommer vi att utforska steg-för-steg-processen för att automatiskt justera CAD-ritningsstorlekar med Aspose.CAD.

## Förutsättningar

Innan du dyker in i handledningen, se till att du har följande förutsättningar på plats:

1.  Java Development Environment: Se till att du har Java installerat på din maskin. Du kan ladda ner den[här](https://www.java.com/en/download/).

2.  Aspose.CAD Library: Ladda ner och installera Aspose.CAD-biblioteket för Java från[här](https://releases.aspose.com/cad/java/).

3. Exempel CAD-fil: Ha en exempel-CAD-fil (t.ex. sample.dwg) tillgänglig i din dokumentkatalog.

## Importera namnområden

din Java-applikation, inkludera de nödvändiga namnområdena för att använda Aspose.CAD-funktionalitet. Här är ett exempel:

```java

import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Låt oss nu dela upp processen för automatisk justering av CAD-ritningsstorlekar i hanterbara steg.

## Steg 1: Ladda CAD-ritningen

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String sourceFilePath = dataDir + "sample.dwg";
Image objImage = Image.load(sourceFilePath);
```

Det här steget innebär att CAD-ritningen laddas från den angivna sökvägen.

## Steg 2: Skapa BmpOptions

```java
BmpOptions bmpOptions = new BmpOptions();
```

 Instantiera`BmpOptions` klass, som kommer att användas för att ställa in olika alternativ för BMP-format.

## Steg 3: Skapa CadRasterizationOptions

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

 Skapa en instans av`CadRasterizationOptions` för att anpassa rastreringsinställningarna för CAD-filen.

## Steg 4: Ställ in layoutegenskaper

```java
cadRasterizationOptions.setLayouts(new String[]{"Model"});
```

Ange de layouter du vill inkludera i utdata. I det här fallet använder vi layouten "Modell".

## Steg 5: Exportera till BMP-format

```java
String outPath = sourceFilePath + ".bmp";
objImage.save(outPath, bmpOptions);
```

Spara slutligen den justerade CAD-ritningen i BMP-format till den angivna utmatningsvägen.

Upprepa dessa steg i din Java-applikation så har du framgångsrikt automatiskt justerat CAD-ritningsstorleken med Aspose.CAD för Java.

## Slutsats

den här handledningen har vi gått igenom processen att automatiskt justera CAD-ritningsstorlekar med Aspose.CAD för Java. Detta bibliotek förenklar CAD-filmanipulation, vilket ger en robust lösning för utvecklare.

## FAQ's

### F1: Är Aspose.CAD kompatibel med olika CAD-filformat?

S1: Ja, Aspose.CAD stöder olika CAD-format, inklusive DWG, DXF, DGN och mer.

### F2: Kan jag använda Aspose.CAD för kommersiella projekt?

 A2: Absolut! Besök[här](https://purchase.aspose.com/buy) för att utforska licensalternativ.

### F3: Hur kan jag få tillfälliga licenser för teständamål?

 A3: Skaffa en tillfällig licens[här](https://purchase.aspose.com/temporary-license/) för testning och utvärdering.

### F4: Var kan jag hitta support för Aspose.CAD?

 S4: Gå med i Aspose.CAD-communityt[forum](https://forum.aspose.com/c/cad/19) för hjälp och diskussioner.

### F5: Finns det en gratis testversion tillgänglig för Aspose.CAD för Java?

 A5: Ja, du kan komma åt den kostnadsfria provperioden[här](https://releases.aspose.com/) att utforska bibliotekets möjligheter.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
