---
title: De CAD-tekeninggrootte aanpassen met behulp van Unit Type met Aspose.CAD voor Java
linktitle: De grootte van de CAD-tekening aanpassen met behulp van het eenheidstype
second_title: Aspose.CAD Java-API
description: Ontdek de kracht van Aspose.CAD voor Java bij het moeiteloos aanpassen van CAD-tekeningformaten. Volg onze stapsgewijze handleiding voor precisie en aanpassingsvermogen.
type: docs
weight: 14
url: /nl/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/
---
## Invoering

In het steeds evoluerende domein van Computer-Aided Design (CAD) zijn precisie en aanpassingsvermogen van het grootste belang. Een veel voorkomende vereiste is het aanpassen van de grootte van CAD-tekeningen op basis van specifieke eenheidstypen. Aspose.CAD voor Java komt naar voren als een krachtige bondgenoot en biedt naadloze mogelijkheden voor het programmatisch manipuleren van CAD-bestanden.

## Vereisten

Voordat u in de zelfstudie duikt, moet u ervoor zorgen dat u aan de volgende vereisten voldoet:

- Java-ontwikkelomgeving: Zorg ervoor dat u een functionele Java-ontwikkelomgeving op uw machine hebt geïnstalleerd.

-  Aspose.CAD voor Java-bibliotheek: Download en integreer de Aspose.CAD-bibliotheek in uw Java-project. U kunt de bibliotheek verkrijgen[hier](https://releases.aspose.com/cad/java/).

## Naamruimten importeren

Neem in uw Java-code de benodigde naamruimten op om toegang te krijgen tot de Aspose.CAD-functionaliteiten. Voeg de volgende importen toe:

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Laten we nu het proces van het aanpassen van de CAD-tekeninggrootte met behulp van het eenheidstype opsplitsen in beheersbare stappen:

## Stap 1: Definieer de gegevensdirectory

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

Stel het pad in voor de map waar uw CAD-bestanden zich bevinden.

## Stap 2: CAD-tekening laden

```java
String sourceFilePath = dataDir + "sample.dwg";
Image image = Image.load(sourceFilePath);
```

 Laad de CAD-tekening met Aspose.CAD's`Image` klas.

## Stap 3: Maak BMP-opties

```java
BmpOptions bmpOptions = new BmpOptions();
```

 Instantieer de`BmpOptions` klasse voor het exporteren van de CAD-lay-out naar BMP-formaat.

## Stap 4: Configureer rasterisatieopties

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

 Maak een exemplaar van`CadRasterizationOptions` en associeer het met de`BmpOptions` voor vectorrastering.

## Stap 5: Stel het eenheidstype in

```java
cadRasterizationOptions.setUnitType(UnitType.Centimeter);
```

Geef het gewenste eenheidstype voor de CAD-tekening op. In dit voorbeeld hebben we dit ingesteld op Centimeter.

## Stap 6: Lay-outs instellen

```java
cadRasterizationOptions.setLayouts(new String[] { "Model" });
```

Definieer de lay-outs waarmee rekening moet worden gehouden tijdens de export. In dit geval hebben we de lay-out "Model" geselecteerd.

## Stap 7: Exporteren naar BMP

```java
String outPath = sourceFilePath + ".bmp";
image.save(outPath, bmpOptions);
```

Sla ten slotte de gewijzigde CAD-tekening op in BMP-formaat.

## Conclusie

Met Aspose.CAD voor Java wordt het aanpassen van CAD-tekeningformaten een fluitje van een cent. In deze tutorial wordt u door het proces geleid, waarbij de betekenis van elke stap voor het bereiken van nauwkeurige resultaten wordt benadrukt.

## Veelgestelde vragen

### V1: Kan ik Aspose.CAD voor Java gebruiken met andere programmeertalen?

A1: Aspose.CAD ondersteunt voornamelijk Java, maar er zijn versies beschikbaar voor andere talen zoals .NET.

### Vraag 2: Zijn er licentieopties voor Aspose.CAD?

 A2: Ja, u kunt licentieopties verkennen en Aspose.CAD kopen[hier](https://purchase.aspose.com/buy).

### V3: Is er een gratis proefversie beschikbaar voor Aspose.CAD?

 A3: Zeker, u heeft toegang tot een gratis proefperiode[hier](https://releases.aspose.com/).

### V4: Hoe kan ik ondersteuning krijgen voor Aspose.CAD voor Java?

 A4: Bezoek het Aspose.CAD-forum[hier](https://forum.aspose.com/c/cad/19) voor uitgebreide ondersteuning.

### V5: Kan ik een tijdelijke licentie verkrijgen voor Aspose.CAD?

 A5: Ja, u kunt een tijdelijke licentie aanschaffen[hier](https://purchase.aspose.com/temporary-license/).