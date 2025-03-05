---
title: Java DGN naar JPEG-conversie met Aspose.CAD-zelfstudie
linktitle: DGN exporteren in AutoCAD-formaat naar Raster Image-formaat
second_title: Aspose.CAD Java-API
description: Leer hoe u DGN-bestanden naar JPEG-afbeeldingen in Java kunt exporteren met behulp van Aspose.CAD. Deze stap-voor-stap handleiding begeleidt u moeiteloos door het proces.
type: docs
weight: 13
url: /nl/java/dgn-export-options/exporting-dgn-to-raster-image/
---
## Invoering

Welkom bij deze uitgebreide tutorial over het exporteren van DGN-bestanden (Design) naar Raster Image Format met behulp van Aspose.CAD voor Java. Aspose.CAD is een krachtige bibliotheek waarmee Java-ontwikkelaars naadloos met CAD-bestanden kunnen werken. In deze zelfstudie begeleiden we u bij het converteren van DGN-bestanden naar JPEG-afbeeldingen, waarbij we u stapsgewijze instructies en codevoorbeelden bieden.

## Vereisten

Voordat u in de zelfstudie duikt, moet u ervoor zorgen dat u aan de volgende vereisten voldoet:
1.  Aspose.CAD-bibliotheek: Zorg ervoor dat de Aspose.CAD voor Java-bibliotheek is geïnstalleerd. Je kunt het downloaden[hier](https://releases.aspose.com/cad/java/).
2. Java Development Kit (JDK): Zorg ervoor dat Java op uw computer is geïnstalleerd.
3. Integrated Development Environment (IDE): Gebruik een Java-compatibele IDE zoals IntelliJ of Eclipse.

## Pakketten importeren

Importeer in uw Java-project de benodigde pakketten voor Aspose.CAD. Voeg de volgende regels toe aan uw code:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
```

## Stap 1: Laad het DGN-bestand

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
DgnImage dgnImage = (DgnImage) Image.load(dataDir + "Nikon_D90_Camera.dgn");
```

## Stap 2: Maak een JpegOptions-object

```java
ImageOptionsBase options = new JpegOptions();
```

## Stap 3: Rasterisatieopties toewijzen

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(600);
vectorOptions.setPageHeight(400);
vectorOptions.setNoScaling(true);
vectorOptions.setAutomaticLayoutsScaling(false);
options.setVectorRasterizationOptions(vectorOptions);
```

## Stap 4: Sla de geconverteerde afbeelding op

```java
OutputStream outStream = new FileOutputStream(dataDir + "ExportDGNToRasterImage_Out.jpg");
dgnImage.save(outStream, options);
```

Herhaal deze stappen voor uw specifieke DGN-bestanden en pas de bestandspaden dienovereenkomstig aan.

## Conclusie

Gefeliciteerd! U hebt met succes geleerd hoe u DGN-bestanden kunt exporteren naar Raster Image Format met behulp van Aspose.CAD voor Java. Deze tutorial heeft u de kennis gegeven om deze functionaliteit in uw Java-applicaties te integreren.

## Veelgestelde vragen

### V1: Kan ik Aspose.CAD voor Java gebruiken met andere CAD-bestandsindelingen?

A1: Ja, Aspose.CAD ondersteunt verschillende CAD-formaten en biedt daarmee een veelzijdige oplossing voor Java-ontwikkelaars.

### V2: Is er een gratis proefversie beschikbaar voor Aspose.CAD voor Java?

 A2: Ja, u heeft toegang tot een gratis proefperiode[hier](https://releases.aspose.com/).

### V3: Waar kan ik documentatie vinden voor Aspose.CAD voor Java?

 A3: Raadpleeg de documentatie[hier](https://reference.aspose.com/cad/java/).

### V4: Hoe kan ik ondersteuning krijgen voor Aspose.CAD voor Java?

 A4: Bezoek het ondersteuningsforum[hier](https://forum.aspose.com/c/cad/19).

### V5: Waar kan ik een licentie kopen voor Aspose.CAD voor Java?

 A5: U kunt een licentie kopen[hier](https://purchase.aspose.com/buy).