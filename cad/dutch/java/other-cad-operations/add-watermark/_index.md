---
title: Watermerken toevoegen aan CAD-tekeningen - Aspose.CAD voor Java-zelfstudie
linktitle: Voeg een watermerk toe
second_title: Aspose.CAD Java-API
description: Verbeter uw CAD-tekeningen met gepersonaliseerde watermerken met Aspose.CAD voor Java. Volg onze stapsgewijze handleiding voor een naadloze integratie.
type: docs
weight: 12
url: /nl/java/other-cad-operations/add-watermark/
---
## Invoering

Welkom bij deze uitgebreide handleiding over het toevoegen van watermerken aan CAD-tekeningen met Aspose.CAD voor Java. In deze zelfstudie leert u hoe u watermerken efficiënt kunt integreren en uw CAD-documenten kunt verbeteren met gepersonaliseerde berichten of branding. Aspose.CAD voor Java biedt een krachtige reeks functies, waardoor het toevoegen van watermerken eenvoudig is.

## Vereisten

Voordat we in de tutorial duiken, moet je ervoor zorgen dat je aan de volgende vereisten voldoet:

-  Aspose.CAD voor Java: Zorg ervoor dat de Aspose.CAD-bibliotheek in uw Java-omgeving is geïnstalleerd. Je kunt het downloaden[hier](https://releases.aspose.com/cad/java/).
- Java Development Kit (JDK): Zorg ervoor dat de nieuwste versie van JDK op uw systeem is geïnstalleerd.

## Pakketten importeren

Importeer in uw Java-project de benodigde Aspose.CAD-pakketten om aan de slag te gaan:

```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.Cad3DPoint;
import com.aspose.cad.fileformats.cad.cadobjects.CadMText;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Stap 1: Voeg nieuwe MTEXT toe

```java
//nieuwe MTEXT toevoegen
CadMText watermark = new CadMText();
watermark.setText("Watermark message");
watermark.setInitialTextHeight(40);
watermark.setInsertionPoint(new Cad3DPoint(300, 40));
watermark.setLayerName("0");
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(watermark);
```

## Stap 2: Voeg een eenvoudige entiteit zoals tekst toe

Je kunt ook een eenvoudiger entiteit, zoals tekst, toevoegen:

```java
// of voeg een eenvoudiger entiteit toe, zoals Tekst
CadText text = new CadText();
text.setDefaultValue("Watermark text");
text.setTextHeight(40);
text.setFirstAlignment(new Cad3DPoint(300, 40));
text.setLayerName("0") ;
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(text);
```

## Stap 3: Exporteren naar PDF

Exporteer de CAD-tekening met het toegevoegde watermerk naar een PDF-bestand:

```java
// exporteren naar pdf
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setLayouts(new String[]{"Model"});
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
cadImage.save(dataDir + "AddWatermark_out.pdf", pdfOptions);

```

## Conclusie

Gefeliciteerd! U hebt met succes watermerken aan uw CAD-tekeningen toegevoegd met Aspose.CAD voor Java. Met dit eenvoudige maar krachtige proces kunt u uw ontwerpen personaliseren of beschermen met branding.

## Veelgestelde vragen

### V1: Is Aspose.CAD compatibel met alle CAD-bestandsformaten?

A1: Aspose.CAD ondersteunt verschillende CAD-formaten, waaronder DWG, DXF, DWT en DWF.

### Vraag 2: Kan ik het uiterlijk van de watermerktekst aanpassen?

A2: Ja, u heeft volledige controle over het uiterlijk van het watermerk, inclusief tekstgrootte, kleur en positie.

### V3: Is er een proefversie beschikbaar voor Aspose.CAD voor Java?

 A3: Ja, u kunt de proefversie downloaden[hier](https://releases.aspose.com/).

### V4: Hoe kan ik ondersteuning krijgen voor Aspose.CAD?

 A4: Bezoek de[Aspose.CAD-forum](https://forum.aspose.com/c/cad/19) voor gemeenschapssteun.

### V5: Waar kan ik de volledige documentatie voor Aspose.CAD voor Java vinden?

 A5: Raadpleeg de[documentatie](https://reference.aspose.com/cad/java/) voor gedetailleerde informatie.