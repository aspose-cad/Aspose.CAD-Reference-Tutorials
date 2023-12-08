---
title: Skapa dynamiska PDF-filer med Aspose.CAD för Java
linktitle: Enskild PDF med olika layouter
second_title: Aspose.CAD Java API
description: Skapa fantastiska PDF-filer med olika layouter från CAD-ritningar med Aspose.CAD för Java. Enkel integration och kraftfulla funktioner för Java-utvecklare.
type: docs
weight: 16
url: /sv/java/other-cad-operations/single-pdf-different-layouts/
---
## Introduktion

Välkommen till världen av Aspose.CAD för Java, ett kraftfullt bibliotek som ger utvecklare möjlighet att manipulera CAD-ritningar utan ansträngning. I den här handledningen kommer vi att dyka ner i att skapa enskilda PDF-filer med olika layouter med Aspose.CAD för Java. Oavsett om du är en erfaren utvecklare eller precis har börjat, kommer den här steg-för-steg-guiden att leda dig genom processen.

## Förutsättningar

Innan vi ger oss ut på denna resa, se till att du har följande förutsättningar på plats:
- Java-miljö: Se till att du har Java installerat på din maskin.
-  Aspose.CAD Library: Ladda ner och installera Aspose.CAD-biblioteket för Java från[nedladdningslänk](https://releases.aspose.com/cad/java/).
- Dokumentkatalog: Skapa en katalog för dina DWG-ritningar.

## Importera paket

Importera nödvändiga paket i ditt Java-projekt:

```java
import com.aspose.cad.Image;
import com.aspose.cad.SizeF;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.VectorRasterizationOptions;
```

## Steg 1: Ladda CAD-ritning

 Börja med att ladda din CAD-ritning i en`CadImage` objekt:

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
CadImage cadImage = (CadImage)Image.load(dataDir + "City skyway map.dwg");
```

## Steg 2: Konfigurera rasteriseringsalternativ

Ställ in rastreringsalternativen för CAD-bilden:

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1000);
rasterizationOptions.setPageHeight(1000);
```

## Steg 3: Anpassa sidstorlekar för layout

Definiera anpassade storlekar för flera layouter i CAD-ritningen:

```java
rasterizationOptions.getLayoutPageSizes().addItem("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.getLayoutPageSizes().addItem("8.5 x 11 Plot", new SizeF(1000, 100));
```

## Steg 4: Ställ in PDF-alternativ

Konfigurera PDF-alternativ, med rastreringsinställningarna:

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Steg 5: Spara som PDF

Spara den bearbetade CAD-bilden som en PDF:

```java
cadImage.save(dataDir + "singlePDF_out.pdf", pdfOptions);
```

Grattis! Du har framgångsrikt skapat en enda PDF med olika layouter med Aspose.CAD för Java.

## Slutsats

I den här handledningen utforskade vi den sömlösa integrationen av Aspose.CAD för Java för att generera PDF-filer med olika layouter från CAD-ritningar. Bibliotekets flexibilitet och robusta funktioner gör det till ett bra val för CAD-manipulationsuppgifter.

## FAQ's

### F1: Kan jag använda Aspose.CAD för Java med andra Java-bibliotek?

S1: Ja, Aspose.CAD för Java är utformad för att sömlöst integreras med andra Java-bibliotek, vilket ger omfattande funktionalitet.

### F2: Finns det en testversion tillgänglig?

 A2: Absolut! Du kan få tillgång till en gratis testversion[här](https://releases.aspose.com/).

### F3: Var kan jag hitta ytterligare support?

 A3: Besök[Aspose.CAD-forum](https://forum.aspose.com/c/cad/19) för samhällsstöd och diskussioner.

### F4: Hur får jag en tillfällig licens?

 S4: Du kan få en tillfällig licens[här](https://purchase.aspose.com/temporary-license/).

### F5: Var kan jag köpa den fullständiga versionen?

S5: Köp den fullständiga versionen av Aspose.CAD för Java[här](https://purchase.aspose.com/buy).