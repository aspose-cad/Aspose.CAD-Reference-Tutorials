---
title: Exporteer IFC naar PNG met Aspose.CAD voor Java
linktitle: Exporteer IFC naar PNG
second_title: Aspose.CAD Java-API
description: Converteer IFC moeiteloos naar PNG met Aspose.CAD voor Java. Volg onze stap-voor-stap handleiding.
type: docs
weight: 18
url: /nl/java/cad-export-options/export-ifc-to-png/
---
## Invoering

Welkom bij deze stapsgewijze zelfstudie over het exporteren van IFC (Industry Foundation Classes) naar PNG met behulp van Aspose.CAD voor Java. Aspose.CAD is een krachtige Java-bibliotheek die uitgebreide mogelijkheden biedt voor het werken met CAD-bestanden, inclusief IFC-formaat. In deze zelfstudie begeleiden we u door het proces van het converteren van een IFC-bestand naar een PNG-afbeelding, met gedetailleerde uitleg bij elke stap.

## Vereisten

Voordat we beginnen, zorg ervoor dat u aan de volgende vereisten voldoet:

-  Aspose.CAD-bibliotheek: Download en installeer de Aspose.CAD-bibliotheek voor Java vanaf de[download link](https://releases.aspose.com/cad/java/).

- Documentmap: bereid een map op uw systeem voor waar uw IFC-bestand zich bevindt.

## Naamruimten importeren

Importeer in uw Java-project de benodigde naamruimten, zoals hieronder weergegeven:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## Stap 1: Laad het IFC-bestand

```java
String dataDir = "Your Document Directory" + "ExportingIFC/";
String fileName = dataDir + "example.ifc";
IfcImage cadImage = (IfcImage)Image.load(fileName);
```

Deze stap omvat het laden van het IFC-bestand met Aspose.CAD.

## Stap 2: Stel vectoropties in

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

Configureer vectoropties voor rastering, waarbij u de paginabreedte en -hoogte opgeeft.

## Stap 3: Stel PNG-opties in

```java
PngOptions pngOptions = new PngOptions();
pngOptions.setVectorRasterizationOptions(vectorOptions);
```

Stel PNG-opties in, inclusief vectorrasteropties.

## Stap 4: Opslaan als PNG

```java
String outPath = dataDir + "example.png";
cadImage.save(outPath, pngOptions);
```

Sla de verwerkte afbeelding op in PNG-indeling.

## Conclusie

Gefeliciteerd! U hebt met succes een IFC-bestand naar PNG geconverteerd met Aspose.CAD voor Java. Deze tutorial biedt een uitgebreide handleiding, zodat u deze functionaliteit naadloos in uw projecten kunt integreren.

## Veelgestelde vragen

### V1: Is Aspose.CAD compatibel met alle versies van IFC-bestanden?

 A1: Aspose.CAD ondersteunt verschillende versies van IFC-bestanden. Verwijs naar de[documentatie](https://reference.aspose.com/cad/java/) voor compatibiliteitsdetails.

### Vraag 2: Kan ik de rasteropties verder aanpassen?

 A2: Absoluut! Ontdek de[documentatie](https://reference.aspose.com/cad/java/) voor geavanceerde aanpassingsmogelijkheden.

### Q3: Is er een proefversie beschikbaar?

A3: Ja, u heeft toegang tot de gratis proefversie[hier](https://releases.aspose.com/).

### V4: Hoe kan ik tijdelijke licenties krijgen voor Aspose.CAD?

 A4: Verkrijg een tijdelijke licentie van[deze link](https://purchase.aspose.com/temporary-license/).

### Vraag 5: Waar kan ik hulp zoeken of problemen bespreken?

A5: Bezoek de[Aspose.CAD-forum](https://forum.aspose.com/c/cad/19) voor gemeenschapssteun.
