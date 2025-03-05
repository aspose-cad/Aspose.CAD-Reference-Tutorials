---
title: Exportera DWG till PDF eller Raster med Aspose.CAD för Java
linktitle: Exportera DWG till PDF eller Raster
second_title: Aspose.CAD Java API
description: Utforska den sömlösa processen att exportera DWG-filer till PDF- eller rasterbilder i Java med Aspose.CAD. Denna steg-för-steg-guide säkerställer precision och effektivitet.
type: docs
weight: 13
url: /sv/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
---
## Introduktion

den dynamiska världen av datorstödd design (CAD) är effektiv hantering av ritningar avgörande. Aspose.CAD för Java tillhandahåller en kraftfull lösning för att exportera DWG-filer till PDF- eller rasterbilder. Denna handledning guidar dig genom processen och säkerställer att du utnyttjar Aspose.CADs fulla potential för Java.

## Förutsättningar

Innan du dyker in i handledningen, se till att du har följande:

- Grundläggande förståelse för Java-programmering.
-  Aspose.CAD för Java-biblioteket installerat. Om inte, ladda ner den[här](https://releases.aspose.com/cad/java/).
- En DWG-fil för teständamål. Du kan använda den medföljande filen "Bottom_plate.dwg".

## Importera namnområden

Importera de nödvändiga namnrymden i ditt Java-projekt för att kickstarta processen:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## Steg 1: Ladda DWG-filen

 Börja med att ladda din DWG-fil med Aspose.CAD:s`Image` klass:

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

## Steg 2: Bestäm enhetstyp

Kontrollera sedan enhetstypen för den laddade DWG-filen:

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

## Steg 3: Ställ in rasteriseringsalternativ

Baserat på enhetstypen, konfigurera rastreringsalternativen:

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();

if (currentUnitIsMetric) {
    // Metriska enheter
    double metersCoeff = 1 / 1000.0;
    double scaleFactor = metersCoeff / currentUnitCoefficient;
    rasterizationOptions.setPageWidth((float)(210 * scaleFactor));
    rasterizationOptions.setPageHeight((float)(297 * scaleFactor));
    rasterizationOptions.setUnitType(UnitType.Millimeter);
} else {
    // Imperialistiska enheter
    rasterizationOptions.setPageWidth((float)(8.27f / currentUnitCoefficient));
    rasterizationOptions.setPageHeight((float)(11.69f / currentUnitCoefficient));
    rasterizationOptions.setUnitType(UnitType.Inch);
}
```

## Steg 4: Konfigurera PDF-alternativ

Ställ in PDF-exportalternativ:

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

## Steg 5: Spara som PDF

Slutligen, spara DWG-filen som en PDF:

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

Och där har du det! Du har framgångsrikt exporterat en DWG-fil till PDF med Aspose.CAD för Java.

## Slutsats

Den här handledningen gav en steg-för-steg-guide om hur du använder Aspose.CAD för Java för att exportera DWG-filer till PDF- eller rasterbilder. Detta bibliotek förenklar processen, vilket gör att du effektivt kan hantera CAD-ritningar i dina Java-applikationer.

## FAQ's

### F1: Kan jag använda Aspose.CAD för Java med andra Java-ramverk?

S1: Ja, Aspose.CAD för Java integreras sömlöst med populära Java-ramverk.

### F2: Finns en tillfällig licens tillgänglig för Aspose.CAD för Java?

 A2: Ja, du kan få en tillfällig licens[här](https://purchase.aspose.com/temporary-license/).

### F3: Var kan jag hitta stöd för Aspose.CAD för Java?

 A3: Besök[Aspose.CAD-forum](https://forum.aspose.com/c/cad/19) för hjälp från samhället.

### F4: Hur kan jag köpa en licens för Aspose.CAD för Java?

 S4: Du kan köpa en licens[här](https://purchase.aspose.com/buy).

### F5: Vilka enheter stöder Aspose.CAD för Java?

S5: Aspose.CAD för Java stöder både metriska och imperialistiska enheter.