---
title: Exportera OLE-objekt från CAD med Aspose.CAD för Java
linktitle: Exportera OLE-objekt från CAD
second_title: Aspose.CAD Java API
description: Lås upp potentialen hos Aspose.CAD för Java. Exportera enkelt OLE-objekt från CAD-filer. Ladda ner nu för sömlös CAD-datahantering.
weight: 10
url: /sv/java/cad-to-pdf-and-svg-export-options/export-ole-objects-from-cad/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportera OLE-objekt från CAD med Aspose.CAD för Java

## Introduktion

I den dynamiska världen av datorstödd design (CAD) är det avgörande att hantera och extrahera OLE-objekt (Object Linking and Embedding) effektivt. Aspose.CAD för Java tillhandahåller en kraftfull lösning för att exportera OLE-objekt från CAD-filer. Den här steg-för-steg-guiden leder dig genom processen och säkerställer att du drar nytta av det här verktygets fulla potential.

## Förutsättningar

Innan du dyker in i handledningen, se till att du har följande förutsättningar på plats:

- Java-miljö: Se till att du har en Java-utvecklingsmiljö inställd på din maskin.
-  Aspose.CAD for Java: Ladda ner och installera Aspose.CAD for Java-biblioteket. Du hittar biblioteket på[nedladdningslänk](https://releases.aspose.com/cad/java/).
- CAD-filer: Förbered CAD-filerna som innehåller OLE-objekt som du vill exportera.

## Importera namnområden

För att börja, importera de nödvändiga namnrymden till ditt Java-projekt. Dessa namnområden tillhandahåller de väsentliga klasserna och funktionerna som krävs för att arbeta med CAD-filer med Aspose.CAD.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Låt oss nu dela upp processen för att exportera OLE-objekt från CAD i flera steg:

## Steg 1: Ställ in din dokumentkatalog

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

Se till att ersätta "Din dokumentkatalog" med sökvägen till katalogen som innehåller dina CAD-filer.

## Steg 2: Definiera CAD-filnamn

```java
String[] files = new String[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

 Ange namnen på de CAD-filer som du vill bearbeta i`files` array.

## Steg 3: Ställ in PNG-exportalternativ

```java
PngOptions pngOptions = new PngOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.setLayouts(new String[] { "Layout1" });
```

Konfigurera PNG-exportalternativen, inklusive vektorrasterisering och layoutinställningar.

## Steg 4: Iterera genom CAD-filer

```java
for(String file : files)
{
    CadImage cadImage = (CadImage)Image.load(dataDir + file);
    cadImage.save(dataDir + file + "_out.png", pngOptions);
}
```

Iterera genom varje specificerad CAD-fil, ladda den med Aspose.CAD och spara OLE-objekten som PNG-bilder.

## Slutsats

Med dessa enkla men kraftfulla steg kan du sömlöst exportera OLE-objekt från CAD-filer med Aspose.CAD för Java. Detta mångsidiga verktyg ger utvecklare möjlighet att hantera CAD-data effektivt, vilket öppnar upp för nya möjligheter inom CAD-applikationsutveckling.

## FAQ's

### F1: Är Aspose.CAD kompatibel med alla CAD-filformat?

 S1: Aspose.CAD stöder olika CAD-format, inklusive DWG, DXF och DGN. Referera till[dokumentation](https://reference.aspose.com/cad/java/) för hela listan.

### F2: Kan jag anpassa exportinställningarna för OLE-objekt?

S2: Ja, Aspose.CAD erbjuder omfattande alternativ för att anpassa exportinställningar, så att du kan skräddarsy utskriften efter dina specifika krav.

### F3: Finns det en gratis testversion tillgänglig för Aspose.CAD?

 S3: Ja, du kan utforska funktionerna i Aspose.CAD genom att få en gratis provperiod från[här](https://releases.aspose.com/).

### F4: Var kan jag få communitysupport för Aspose.CAD?

 S4: Gå med i Aspose.CAD-communityt på[forum](https://forum.aspose.com/c/cad/19) att söka hjälp och dela dina erfarenheter.

### F5: Hur kan jag köpa en licens för Aspose.CAD?

A5: Besök[köpsidan](https://purchase.aspose.com/buy) att skaffa en licens som passar dina utvecklingsbehov.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
