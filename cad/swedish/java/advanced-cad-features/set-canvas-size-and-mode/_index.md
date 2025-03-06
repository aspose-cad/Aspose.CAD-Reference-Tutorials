---
title: Ställ in dukstorlek och läge
linktitle: Ställ in dukstorlek och läge
second_title: Aspose.CAD Java API
description: Utforska kraften i Aspose.CAD för Java med vår steg-för-steg-guide om hur du ställer in dukens storlek och läge. Konvertera enkelt CAD-filer till PDF- och TIFF-format.
weight: 16
url: /sv/java/advanced-cad-features/set-canvas-size-and-mode/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ställ in dukstorlek och läge

## Introduktion

Vill du utnyttja kraften i Aspose.CAD för Java för att förbättra din CAD-konverteringsprocess? Denna omfattande guide kommer att leda dig genom stegen för att ställa in dukens storlek och läge med Aspose.CAD för Java. Oavsett om du är en erfaren utvecklare eller precis har börjat, kommer den här handledningen att ge dig de insikter du behöver.

## Förutsättningar

Innan du dyker in i handledningen, se till att du har följande förutsättningar på plats:

-  Aspose.CAD för Java: Se till att du har Aspose.CAD-biblioteket installerat i din Java-miljö. Du kan ladda ner den[här](https://releases.aspose.com/cad/java/).

- Dokumentkatalog: Skapa en dokumentkatalog för att lagra dina CAD-filer. Denna katalog kommer att hänvisas till i handledningsstegen.

Låt oss nu komma igång med steg-för-steg-guiden.

## Importera namnområden

det här steget kommer vi att importera de nödvändiga namnrymden för att kickstarta ditt Aspose.CAD-projekt.
```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## Steg 1: Importera Aspose.CAD-klasser

```java
// Sökvägen till resurskatalogen.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

 I det här utdraget ställer vi in sökvägen till resurskatalogen och laddar en DXF-fil med Aspose.CAD:s`Image` klass.

## Steg 2: Ställ in egenskaper för CadRasterizationOptions

```java
// Skapa en instans av CadRasterizationOptions och ställ in dess olika egenskaper
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

 Här skapar vi en instans av`CadRasterizationOptions` och konfigurera egenskaper som sidbredd, sidhöjd och skalningsalternativ.

## Steg 3: Skapa Pdf-alternativ och ställ in VectorRasterizationOptions

```java
// Skapa en instans av PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Ställ in egenskapen VectorRasterizationOptions
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

 Nu skapar vi en`PdfOptions` instans och ställ in dess`VectorRasterizationOptions` egenskapen till den tidigare konfigurerade`CadRasterizationOptions`.

## Steg 4: Exportera till PDF

```java
// Exportera CAD till PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

Slutligen sparar vi CAD-bilden till en PDF-fil med de angivna alternativen.

## Steg 5: Skapa TiffOptions och ställ in VectorRasterizationOptions

```java
// Skapa en instans av TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Ställ in egenskapen VectorRasterizationOptions
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

 det här steget ställer vi in en`TiffOptions` instans och konfigurera dess`VectorRasterizationOptions` fast egendom.

## Steg 6: Exportera till TIFF

```java
// Exportera CAD till TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

Slutligen sparar vi CAD-bilden till en TIFF-fil med de angivna alternativen.

## Slutsats

 Grattis! Du har framgångsrikt ställt in dukens storlek och läge med Aspose.CAD för Java. Denna handledning ger en solid grund för dina CAD-konverteringsprojekt. Utforska fler funktioner och möjligheter i[Aspose.CAD-dokumentation](https://reference.aspose.com/cad/java/).

## FAQ's

### F1: Kan jag använda Aspose.CAD för Java med andra Java-ramverk?

S1: Ja, Aspose.CAD är designat för att sömlöst integreras med olika Java-ramverk.

### F2: Finns en tillfällig licens tillgänglig för Aspose.CAD?

 A2: Ja, du kan få en tillfällig licens[här](https://purchase.aspose.com/temporary-license/).

### F3: Var kan jag få communitysupport för Aspose.CAD?

 A3: Besök[Aspose.CAD-forum](https://forum.aspose.com/c/cad/19) för samhällsstöd och diskussioner.

### F4: Kan jag prova Aspose.CAD gratis?

 A4: Absolut! Få en gratis provperiod[här](https://releases.aspose.com/).

### F5: Hur köper jag Aspose.CAD för Java?

 A5: Köp produkten[här](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
