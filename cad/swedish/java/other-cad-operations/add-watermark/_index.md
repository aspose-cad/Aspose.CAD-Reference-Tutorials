---
title: Lägg till vattenstämplar till CAD-ritningar - Aspose.CAD för Java Tutorial
linktitle: Lägg till vattenstämpel
second_title: Aspose.CAD Java API
description: Förbättra dina CAD-ritningar med personliga vattenstämplar med Aspose.CAD för Java. Följ vår steg-för-steg-guide för sömlös integration.
weight: 12
url: /sv/java/other-cad-operations/add-watermark/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Lägg till vattenstämplar till CAD-ritningar - Aspose.CAD för Java Tutorial

## Introduktion

Välkommen till den här omfattande guiden om att lägga till vattenstämplar till CAD-ritningar med Aspose.CAD för Java. I den här handledningen kommer du att lära dig hur du integrerar vattenstämplar effektivt och förbättrar dina CAD-dokument med personliga meddelanden eller varumärke. Aspose.CAD för Java tillhandahåller en kraftfull uppsättning funktioner, vilket gör processen för tillägg av vattenstämpel enkel.

## Förutsättningar

Innan vi dyker in i handledningen, se till att du har följande förutsättningar:

-  Aspose.CAD för Java: Se till att du har Aspose.CAD-biblioteket installerat i din Java-miljö. Du kan ladda ner den[här](https://releases.aspose.com/cad/java/).
- Java Development Kit (JDK): Se till att du har den senaste versionen av JDK installerad på ditt system.

## Importera paket

Importera de nödvändiga Aspose.CAD-paketen i ditt Java-projekt för att komma igång:

```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.Cad3DPoint;
import com.aspose.cad.fileformats.cad.cadobjects.CadMText;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Steg 1: Lägg till ny MTEXT

```java
//lägg till ny MTEXT
CadMText watermark = new CadMText();
watermark.setText("Watermark message");
watermark.setInitialTextHeight(40);
watermark.setInsertionPoint(new Cad3DPoint(300, 40));
watermark.setLayerName("0");
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(watermark);
```

## Steg 2: Lägg till enkel enhet som text

Du kan också lägga till en enklare enhet som text:

```java
// eller lägg till enklare enhet som Text
CadText text = new CadText();
text.setDefaultValue("Watermark text");
text.setTextHeight(40);
text.setFirstAlignment(new Cad3DPoint(300, 40));
text.setLayerName("0") ;
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(text);
```

## Steg 3: Exportera till PDF

Exportera CAD-ritningen med den tillagda vattenstämpeln till en PDF-fil:

```java
// exportera till pdf
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setLayouts(new String[]{"Model"});
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
cadImage.save(dataDir + "AddWatermark_out.pdf", pdfOptions);

```

## Slutsats

Grattis! Du har framgångsrikt lagt till vattenstämplar till dina CAD-ritningar med Aspose.CAD för Java. Denna enkla men kraftfulla process låter dig anpassa dina mönster eller skydda dem med varumärke.

## FAQ's

### F1: Är Aspose.CAD kompatibel med alla CAD-filformat?

S1: Aspose.CAD stöder olika CAD-format, inklusive DWG, DXF, DWT och DWF.

### F2: Kan jag anpassa utseendet på vattenstämpeltexten?

S2: Ja, du har full kontroll över vattenstämpelns utseende, inklusive textstorlek, färg och position.

### F3: Finns det en testversion tillgänglig för Aspose.CAD för Java?

 A3: Ja, du kan ladda ner testversionen[här](https://releases.aspose.com/).

### F4: Hur kan jag få support för Aspose.CAD?

 A4: Besök[Aspose.CAD-forum](https://forum.aspose.com/c/cad/19) för samhällsstöd.

### F5: Var kan jag hitta den fullständiga dokumentationen för Aspose.CAD för Java?

 A5: Se[dokumentation](https://reference.aspose.com/cad/java/) för detaljerad information.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
