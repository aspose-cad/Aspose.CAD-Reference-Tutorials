---
title: Pennstöd vid export
linktitle: Pennstöd vid export
second_title: Aspose.CAD Java API
description: Masterpenna anpassning i CAD-export med Aspose.CAD för Java. Följ vår steg-för-steg-guide för sömlös integration.
type: docs
weight: 13
url: /sv/java/advanced-cad-features/pen-support-in-export/
---
## Introduktion

det ständigt föränderliga landskapet av CAD-konverteringar (Computer-Aided Design) framstår Aspose.CAD för Java som ett kraftfullt verktyg som erbjuder omfattande möjligheter för att manipulera CAD-filer. Bland dess mångsidiga funktioner sticker stödet för pennanpassning under export ut, vilket gör att användarna kan skräddarsy utseendet på exporterade bilder. Den här handledningen går igenom processen att utnyttja pennstödet i exportfunktionen, med fokus på praktisk implementering med Java.

## Förutsättningar

Innan du fördjupar dig i handledningen, se till att du har följande förutsättningar på plats:

- Java-utvecklingsmiljö: Se till att du har en fungerande Java-utvecklingsmiljö inställd på din maskin.

-  Aspose.CAD Library: Ladda ner och integrera Aspose.CAD-biblioteket i ditt Java-projekt. Du hittar biblioteket[här](https://releases.aspose.com/cad/java/).

Låt oss nu hoppa in i handledningen och utforska stegen för att utnyttja pennstöd under CAD-export.

## Importera namnområden

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.PenOptions;
import com.aspose.cad.internal.imaging.LineCap;
```

## Steg 1: Definiera din dokumentkatalog

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

Se till att ersätta "Din dokumentkatalog" med den faktiska sökvägen till dina CAD-dokument.

## Steg 2: Ladda CAD-filen

```java
String srcFile = dataDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage) Image.load(srcFile);
```

Detta steg innebär att ladda CAD-filen, i det här fallet "conic_pyramid.dxf," med hjälp av Aspose.CAD-biblioteket.

## Steg 3: Konfigurera rasteriseringsalternativ

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(cadImage.getWidth() * 100);
rasterizationOptions.setPageHeight(cadImage.getHeight() * 100);
```

Justera sidans bredd och höjd enligt dina specifika krav. Dessa värden bestämmer dimensionerna på den exporterade bilden.

## Steg 4: Anpassa pennalternativ

```java
PenOptions penOts = new PenOptions();
penOts.setStartCap(LineCap.Flat);
penOts.setEndCap(LineCap.Flat);
```

Anpassa start- och ändlocken på pennorna efter behov. Denna anpassning gäller vid export av CadImage-objektet till olika bildformat.

## Steg 5: Konfigurera PDF-exportalternativ

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Ange vektorrasteriseringsalternativen, inklusive de tidigare konfigurerade rasteriseringsalternativen.

## Steg 6: Spara den exporterade PDF-filen

```java
cadImage.save((dataDir + "9LHATT-A56_generated.pdf"), pdfOptions);
```

Spara den exporterade PDF-filen med det angivna filnamnet ("9LHATT-A56_generated.pdf" i det här exemplet) och de konfigurerade alternativen.

## Slutsats

Sammanfattningsvis, utnyttjande av pennstöd under CAD-export med Aspose.CAD för Java ger användare möjlighet att anpassa utseendet på exporterade bilder. Genom att följa den här steg-för-steg-guiden har du lärt dig hur du sömlöst integrerar pennanpassning i ditt CAD-konverteringsarbetsflöde.

## FAQ's

### F1: Kan jag anpassa pennalternativ för andra format än PDF?

S1: Ja, pennanpassningen som visas i denna handledning är tillämplig på olika bildformat, inklusive PDF, PNG, BMP, GIF, JPEG2000, JPEG, PSD, TIFF och WMF.

### F2: Hur kan jag hantera olika start- och ändlock för pennor?

 A2: Använd`PenOptions` klass för att ställa in önskade start- och slutkapslar, vilket ger flexibilitet när det gäller att definiera utseendet på linjer.

### F3: Vad händer om jag inte anger pennalternativ?

S3: Om pennalternativen inte är explicit inställda kommer systemet att använda sina standardpennor, som kan variera i olika sammanhang.

### F4: Finns det specifika överväganden för rastreringsalternativ?

A4: Justera sidbredden och höjden i rastreringsalternativen för att kontrollera dimensionerna på den exporterade bilden.

### F5: Var kan jag hitta ytterligare stöd eller diskussioner i samhället?

 S5: Utforska Aspose.CAD-gemenskapsforumet på[här](https://forum.aspose.com/c/cad/19) för stöd och diskussioner.