---
title: Justera CAD-ritningsstorlek med hjälp av enhetstyp med Aspose.CAD för Java
linktitle: Justera CAD-ritningsstorlek med hjälp av enhetstyp
second_title: Aspose.CAD Java API
description: Utforska kraften i Aspose.CAD för Java för att enkelt justera CAD-ritningsstorlekar. Följ vår steg-för-steg-guide för precision och anpassningsförmåga.
weight: 14
url: /sv/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Justera CAD-ritningsstorlek med hjälp av enhetstyp med Aspose.CAD för Java

## Introduktion

den ständigt föränderliga sfären av datorstödd design (CAD) är precision och anpassningsförmåga avgörande. Ett vanligt krav är att anpassa storleken på CAD-ritningar utifrån specifika enhetstyper. Aspose.CAD för Java framstår som en kraftfull allierad, vilket ger sömlösa möjligheter att manipulera CAD-filer programmatiskt.

## Förutsättningar

Innan du dyker in i handledningen, se till att du har följande förutsättningar på plats:

- Java-utvecklingsmiljö: Se till att du har en fungerande Java-utvecklingsmiljö inställd på din maskin.

-  Aspose.CAD for Java Library: Ladda ner och integrera Aspose.CAD-biblioteket i ditt Java-projekt. Du kan skaffa biblioteket[här](https://releases.aspose.com/cad/java/).

## Importera namnområden

I din Java-kod, inkludera de nödvändiga namnområdena för att komma åt Aspose.CAD-funktioner. Lägg till följande importer:

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Låt oss nu dela upp processen att justera CAD-ritningsstorleken med hjälp av enhetstyp i hanterbara steg:

## Steg 1: Definiera datakatalog

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

Ställ in sökvägen för katalogen där dina CAD-filer finns.

## Steg 2: Ladda CAD-ritning

```java
String sourceFilePath = dataDir + "sample.dwg";
Image image = Image.load(sourceFilePath);
```

 Ladda CAD-ritningen med Aspose.CAD:s`Image` klass.

## Steg 3: Skapa BMP-alternativ

```java
BmpOptions bmpOptions = new BmpOptions();
```

 Instantiera`BmpOptions` klass för att exportera CAD-layouten till BMP-format.

## Steg 4: Konfigurera rasteriseringsalternativ

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

 Skapa en instans av`CadRasterizationOptions` och associera det med`BmpOptions` för vektorrasterisering.

## Steg 5: Ställ in enhetstyp

```java
cadRasterizationOptions.setUnitType(UnitType.Centimeter);
```

Ange önskad enhetstyp för CAD-ritningen. I det här exemplet har vi ställt in den på Centimeter.

## Steg 6: Ställ in layouter

```java
cadRasterizationOptions.setLayouts(new String[] { "Model" });
```

Definiera layouterna som ska beaktas under exporten. I det här fallet har vi valt layouten "Modell".

## Steg 7: Exportera till BMP

```java
String outPath = sourceFilePath + ".bmp";
image.save(outPath, bmpOptions);
```

Spara slutligen den modifierade CAD-ritningen i BMP-format.

## Slutsats

Med Aspose.CAD för Java blir det enkelt att justera CAD-ritningsstorlekar. Denna handledning har lett dig genom processen och betonat varje stegs betydelse för att uppnå exakta resultat.

## FAQ's

### F1: Kan jag använda Aspose.CAD för Java med andra programmeringsspråk?

S1: Aspose.CAD stöder i första hand Java, men det finns versioner tillgängliga för andra språk som .NET.

### F2: Finns det några licensalternativ för Aspose.CAD?

 S2: Ja, du kan utforska licensalternativ och köpa Aspose.CAD[här](https://purchase.aspose.com/buy).

### F3: Finns det en gratis testversion tillgänglig för Aspose.CAD?

 S3: Visst, du kan få tillgång till en gratis provperiod[här](https://releases.aspose.com/).

### F4: Hur kan jag få support för Aspose.CAD för Java?

 S4: Besök Aspose.CAD-forumet[här](https://forum.aspose.com/c/cad/19) för omfattande stöd.

### F5: Kan jag få en tillfällig licens för Aspose.CAD?

 S5: Ja, du kan skaffa en tillfällig licens[här](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
