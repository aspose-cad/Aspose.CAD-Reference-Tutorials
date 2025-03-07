---
title: Exportera STL till PNG med Aspose.CAD för Java
linktitle: Exportera STL till PNG
second_title: Aspose.CAD Java API
description: Utforska den sömlösa processen att exportera STL-filer till PNG i Java med Aspose.CAD. Förenkla ditt arbetsflöde och förbättra dina Java-projekt utan ansträngning.
weight: 20
url: /sv/java/cad-export-options/export-stl-to-png/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportera STL till PNG med Aspose.CAD för Java

## Introduktion

Vill du exportera STL-filer till PNG med Java? Aspose.CAD för Java är lösningen du behöver! I den här handledningen guidar vi dig genom processen steg för steg. Som en skicklig SEO-skribent ser jag till att innehållet inte bara är informativt utan också optimerat för sökmotorer.

## Förutsättningar

Innan du dyker in i handledningen, se till att du har följande förutsättningar på plats:

- Java Development Kit (JDK) installerat på din maskin.
-  Aspose.CAD för Java-bibliotek nedladdat. Du kan få det[här](https://releases.aspose.com/cad/java/).
-  En giltig licens eller en tillfällig licens från[här](https://purchase.aspose.com/temporary-license/).

## Importera namnområden

Importera de nödvändiga namnrymden i ditt Java-projekt:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Låt oss nu dela upp exemplet i flera steg.

## Steg 1: Konfigurera ditt projekt

Skapa ett nytt Java-projekt och lägg till Aspose.CAD for Java-biblioteket till ditt projekts beroenden.

## Steg 2: Ange din STL-fil

Definiera sökvägen till din STL-fil. Till exempel:

```java
String dataDir = "Your Document Directory" + "ExportingSTL/";
String fileName = dataDir + "example.stl";
```

## Steg 3: Ladda STL-fil

 Ladda STL-filen med hjälp av`Image.load` metod:

```java
CadImage cadImage = (CadImage)Image.load(fileName);
```

## Steg 4: Konfigurera rasteriseringsalternativ

Ställ in rastreringsalternativ för vektorisering:

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

## Steg 5: Konfigurera PNG-alternativ

Ange alternativ för PNG-export:

```java
PngOptions pngOptions = new PngOptions();
// Avkommentera raden nedan om du vill ställa in vektorrasteriseringsalternativ
// pngOptions.setVectorRasterizationOptions(vectorOptions);
```

## Steg 6: Spara som PNG

Spara CAD-bilden som en PNG-fil:

```java
String outPath = dataDir + "galeon.stl.png";
cadImage.save(outPath, pngOptions);
```

Grattis! Du har framgångsrikt exporterat en STL-fil till PNG med Aspose.CAD för Java.

## Slutsats

I den här handledningen undersökte vi hur man kan utnyttja Aspose.CAD för Java för att exportera STL-filer till PNG utan ansträngning. Detta kraftfulla bibliotek förenklar komplexa uppgifter, vilket gör det till en värdefull tillgång för dina Java-projekt.

## FAQ's

### F1: Är Aspose.CAD för Java kompatibel med alla STL-filversioner?

S1: Aspose.CAD för Java stöder olika STL-filversioner, vilket säkerställer kompatibilitet med de vanligaste formaten.

### F2: Kan jag använda Aspose.CAD för Java i ett kommersiellt projekt?

 A2: Ja, det kan du. Skaffa helt enkelt en giltig licens från[här](https://purchase.aspose.com/buy).

### F3: Behöver jag en tillfällig licens för den kostnadsfria provperioden?

 S3: Nej, en tillfällig licens krävs inte för den kostnadsfria provperioden. Du kan komma igång direkt med testversionen[här](https://releases.aspose.com/).

### F4: Var kan jag hitta ytterligare support eller ställa frågor?

 S4: Besök Aspose.CAD-forumet[här](https://forum.aspose.com/c/cad/19) för support eller frågor.

### F5: Finns det någon heltäckande dokumentation tillgänglig?

 S5: Ja, dokumentationen kan hittas[här](https://reference.aspose.com/cad/java/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
