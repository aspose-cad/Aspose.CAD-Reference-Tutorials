---
title: Exportera IFC till PNG med Aspose.CAD för Java
linktitle: Exportera IFC till PNG
second_title: Aspose.CAD Java API
description: Konvertera IFC till PNG utan ansträngning med Aspose.CAD för Java. Följ vår steg-för-steg handledning.
type: docs
weight: 18
url: /sv/java/cad-export-options/export-ifc-to-png/
---
## Introduktion

Välkommen till denna steg-för-steg handledning om att exportera IFC (Industry Foundation Classes) till PNG med Aspose.CAD för Java. Aspose.CAD är ett kraftfullt Java-bibliotek som ger omfattande möjligheter att arbeta med CAD-filer, inklusive IFC-format. I den här handledningen guidar vi dig genom processen att konvertera en IFC-fil till en PNG-bild med detaljerade förklaringar vid varje steg.

## Förutsättningar

Innan vi börjar, se till att du har följande förutsättningar på plats:

-  Aspose.CAD Library: Ladda ner och installera Aspose.CAD-biblioteket för Java från[nedladdningslänk](https://releases.aspose.com/cad/java/).

- Dokumentkatalog: Förbered en katalog på ditt system där din IFC-fil finns.

## Importera namnområden

I ditt Java-projekt, importera de nödvändiga namnrymden enligt nedan:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## Steg 1: Ladda IFC-filen

```java
String dataDir = "Your Document Directory" + "ExportingIFC/";
String fileName = dataDir + "example.ifc";
IfcImage cadImage = (IfcImage)Image.load(fileName);
```

Detta steg innebär att ladda IFC-filen med Aspose.CAD.

## Steg 2: Ställ in vektoralternativ

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

Konfigurera vektoralternativ för rastrering, ange sidans bredd och höjd.

## Steg 3: Ställ in PNG-alternativ

```java
PngOptions pngOptions = new PngOptions();
pngOptions.setVectorRasterizationOptions(vectorOptions);
```

Ställ in PNG-alternativ, inklusive vektorrastereringsalternativ.

## Steg 4: Spara som PNG

```java
String outPath = dataDir + "example.png";
cadImage.save(outPath, pngOptions);
```

Spara den bearbetade bilden i PNG-format.

## Slutsats

Grattis! Du har framgångsrikt konverterat en IFC-fil till PNG med Aspose.CAD för Java. Denna handledning gav en omfattande guide som säkerställer att du sömlöst kan integrera den här funktionen i dina projekt.

## FAQ's

### F1: Är Aspose.CAD kompatibel med alla versioner av IFC-filer?

 S1: Aspose.CAD stöder olika versioner av IFC-filer. Referera till[dokumentation](https://reference.aspose.com/cad/java/) för kompatibilitetsinformation.

### F2: Kan jag anpassa rastreringsalternativen ytterligare?

 A2: Absolut! Utforska[dokumentation](https://reference.aspose.com/cad/java/) för avancerade anpassningsalternativ.

### F3: Finns det en testversion tillgänglig?

A3: Ja, du kan komma åt den kostnadsfria testversionen[här](https://releases.aspose.com/).

### F4: Hur kan jag få tillfällig licens för Aspose.CAD?

 A4: Skaffa en tillfällig licens från[den här länken](https://purchase.aspose.com/temporary-license/).

### F5: Var kan jag söka hjälp eller diskutera frågor?

A5: Besök[Aspose.CAD-forum](https://forum.aspose.com/c/cad/19) för samhällsstöd.
