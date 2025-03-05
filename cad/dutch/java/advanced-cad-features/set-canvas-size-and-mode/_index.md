---
title: Stel het canvasformaat en de modus in
linktitle: Stel het canvasformaat en de modus in
second_title: Aspose.CAD Java-API
description: Ontdek de kracht van Aspose.CAD voor Java met onze stapsgewijze handleiding voor het instellen van de canvasgrootte en -modus. Converteer CAD-bestanden moeiteloos naar PDF- en TIFF-formaten.
type: docs
weight: 16
url: /nl/java/advanced-cad-features/set-canvas-size-and-mode/
---
## Invoering

Wilt u de kracht van Aspose.CAD voor Java benutten om uw CAD-conversieproces te verbeteren? Deze uitgebreide handleiding leidt u door de stappen voor het instellen van de canvasgrootte en -modus met behulp van Aspose.CAD voor Java. Of je nu een doorgewinterde ontwikkelaar bent of net begint, deze tutorial geeft je de inzichten die je nodig hebt.

## Vereisten

Voordat u in de zelfstudie duikt, moet u ervoor zorgen dat u aan de volgende vereisten voldoet:

-  Aspose.CAD voor Java: Zorg ervoor dat de Aspose.CAD-bibliotheek in uw Java-omgeving is geïnstalleerd. Je kunt het downloaden[hier](https://releases.aspose.com/cad/java/).

- Documentmap: Stel een documentmap in om uw CAD-bestanden op te slaan. Er wordt naar deze map verwezen in de zelfstudiestappen.

Laten we nu aan de slag gaan met de stapsgewijze handleiding.

## Naamruimten importeren

In deze stap importeren we de benodigde naamruimten om uw Aspose.CAD-project een vliegende start te geven.
```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## Stap 1: Aspose.CAD-klassen importeren

```java
// Het pad naar de bronmap.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

 In dit fragment stellen we het pad naar de bronmap in en laden we een DXF-bestand met behulp van Aspose.CAD's`Image` klas.

## Stap 2: Stel CadRasterizationOptions-eigenschappen in

```java
// Maak een exemplaar van CadRasterizationOptions en stel de verschillende eigenschappen ervan in
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

 Hier maken we een exemplaar van`CadRasterizationOptions` en configureer eigenschappen zoals paginabreedte, paginahoogte en schaalopties.

## Stap 3: Maak PdfOptions en stel VectorRasterizationOptions in

```java
// Maak een exemplaar van PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Stel de eigenschap VectorRasterizationOptions in
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

 Nu creëren we een`PdfOptions` exemplaar en stel het in`VectorRasterizationOptions` eigenschap naar de eerder geconfigureerde`CadRasterizationOptions`.

## Stap 4: Exporteren naar PDF

```java
// Exporteer CAD naar PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

Ten slotte slaan we de CAD-afbeelding op in een PDF-bestand met behulp van de opgegeven opties.

## Stap 5: Maak TiffOptions en stel VectorRasterizationOptions in

```java
// Maak een exemplaar van TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Stel de eigenschap VectorRasterizationOptions in
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

In deze stap stellen we een`TiffOptions` exemplaar en configureer het`VectorRasterizationOptions` eigendom.

## Stap 6: Exporteren naar TIFF

```java
// Exporteer CAD naar TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

Ten slotte slaan we de CAD-afbeelding op in een TIFF-bestand met behulp van de opgegeven opties.

## Conclusie

 Gefeliciteerd! U hebt de canvasgrootte en -modus met succes ingesteld met Aspose.CAD voor Java. Deze tutorial biedt een solide basis voor uw CAD-conversieprojecten. Ontdek meer functies en mogelijkheden in de[Aspose.CAD-documentatie](https://reference.aspose.com/cad/java/).

## Veelgestelde vragen

### V1: Kan ik Aspose.CAD voor Java gebruiken met andere Java-frameworks?

A1: Ja, Aspose.CAD is ontworpen om naadloos te integreren met verschillende Java-frameworks.

### Vraag 2: Is er een tijdelijke licentie beschikbaar voor Aspose.CAD?

 A2: Ja, u kunt een tijdelijke licentie verkrijgen[hier](https://purchase.aspose.com/temporary-license/).

### V3: Waar kan ik community-ondersteuning krijgen voor Aspose.CAD?

 A3: Bezoek de[Aspose.CAD-forum](https://forum.aspose.com/c/cad/19) voor gemeenschapsondersteuning en discussies.

### V4: Kan ik Aspose.CAD gratis uitproberen?

 A4: Absoluut! Ontvang een gratis proefperiode[hier](https://releases.aspose.com/).

### V5: Hoe koop ik Aspose.CAD voor Java?

 A5: Koop het product[hier](https://purchase.aspose.com/buy).