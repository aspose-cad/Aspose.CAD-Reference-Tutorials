---
title: Exportera DGN till DWG med Aspose.CAD för Java
linktitle: Exportera DGN som en del av DWG
second_title: Aspose.CAD Java API
description: Utforska hur du exporterar DGN som en del av DWG med Aspose.CAD för Java. Följ vår steg-för-steg-guide för effektiv CAD-filmanipulation.
type: docs
weight: 10
url: /sv/java/dgn-export-options/export-dgn-as-part-of-dwg/
---
## Introduktion

I den här handledningen kommer vi att utforska hur man använder Aspose.CAD för Java för att exportera en DGN-fil (MicroStation Design) som en del av en DWG-fil (AutoCAD-ritning). Aspose.CAD är ett kraftfullt bibliotek som ger omfattande funktionalitet för att arbeta med CAD-filformat. Den här steg-för-steg-guiden hjälper dig att förstå processen att exportera DGN som en del av DWG med Java.

## Förutsättningar

Innan vi dyker in i handledningen, se till att du har följande förutsättningar på plats:
1. Aspose.CAD Library: Ladda ner och installera Aspose.CAD-biblioteket för Java. Du hittar biblioteket[här](https://releases.aspose.com/cad/java/).
2. Java Development Kit (JDK): Se till att du har Java installerat på ditt system.
3. Integrated Development Environment (IDE): Välj en Java IDE som Eclipse eller IntelliJ för en smidigare utvecklingsupplevelse.

## Importera paket

Importera de nödvändiga Aspose.CAD-paketen i ditt Java-projekt för att möjliggöra CAD-filmanipulation. Här är ett exempel:

```java
import com.aspose.cad;
import com.aspose.cad.imageoptions;
import com.aspose.cad.fileformats.cad.cadconsts;
import com.aspose.cad.fileformats.cad;
import com.aspose.cad.fileformats.cad.cadobjects;
```

## Steg 1: Ställ in filsökvägar

 Definiera in- och utdatafilsökvägarna för DWG-filen. Uppdatera`dataDir`, `fileName` , och`outPath` variabler i enlighet därmed.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
String outPath = dataDir + "BlockRefDgn.dwg.pdf";
```

## Steg 2: Skapa PdfOptions-instans

 Skapa en instans av`PdfOptions` klass, eftersom vi exporterar DWG-filen till PDF-format.

```java
PdfOptions exportOptions = new PdfOptions();
```

## Steg 3: Ladda DWG-fil

 Ladda den befintliga DWG-filen som en bild och konvertera den till`CadImage` typ.

```java
CadImage cadImage = (CadImage) Image.load(fileName);
```

## Steg 4: Iterera genom enheter

Gå igenom varje entitet i DWG-filen och kontrollera om det är en bilddefinition. Om så är fallet, hämta den externa referensen till objektet.

```java
for (CadBaseEntity baseEntity : cadImage.getEntities()) {
    if (baseEntity.getTypeName() == CadEntityTypeName.DGNUNDERLAY) {
        CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
        System.out.println(dgnFile.getUnderlayPath());
    }
}
```

## Steg 5: Definiera rasteriseringsalternativ

 Definiera inställningar för`CadRasterizationOptions`objekt, inklusive sidbredd, höjd, layouter och bakgrundsfärg.

```java
CadRasterizationOptions vectorRasterizationOptions = new CadRasterizationOptions();
vectorRasterizationOptions.setPageWidth(1600);
vectorRasterizationOptions.setPageHeight(1600);
vectorRasterizationOptions.setLayouts(new String[] { "Model" });
vectorRasterizationOptions.setAutomaticLayoutsScaling(false);
vectorRasterizationOptions.setNoScaling(true);
vectorRasterizationOptions.setBackgroundColor(Color.getBlack());
vectorRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
```

## Steg 6: Ställ in vektorrasteriseringsalternativ

Ställ in vektorrasteriseringsalternativen för exporten.

```java
exportOptions.setVectorRasterizationOptions(vectorRasterizationOptions);
```

## Steg 7: Exportera DWG till PDF

 Exportera slutligen DWG till PDF genom att anropa`save` metod.

```java
cadImage.save(outPath, exportOptions);
```

## Slutsats

Grattis! Du har framgångsrikt lärt dig hur du exporterar en DGN-fil som en del av en DWG-fil med Aspose.CAD för Java. Detta kraftfulla bibliotek ger omfattande möjligheter att arbeta med CAD-filer, vilket gör dina CAD-filmanipuleringsuppgifter effektiva och enkla.

## FAQ's

### F1: Var kan jag hitta dokumentationen för Aspose.CAD för Java?

 S1: Dokumentationen kan hittas[här](https://reference.aspose.com/cad/java/).

### F2: Hur kan jag ladda ner Aspose.CAD-biblioteket för Java?

 A2: Du kan ladda ner biblioteket från[den här länken](https://releases.aspose.com/cad/java/).

### F3: Finns det en gratis testversion tillgänglig för Aspose.CAD för Java?

 A3: Ja, du kan hitta den kostnadsfria provperioden[här](https://releases.aspose.com/).

### F4: Var kan jag få en tillfällig licens för Aspose.CAD för Java?

 A4: Skaffa en tillfällig licens[här](https://purchase.aspose.com/temporary-license/).

### F5: Behöver du hjälp eller har frågor?

 S5: Besök Aspose.CAD-gemenskapens supportforum[här](https://forum.aspose.com/c/cad/19).