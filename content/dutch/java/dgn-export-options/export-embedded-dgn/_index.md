---
title: Exporteer ingebedde DGN naar PDF met Aspose.CAD voor Java
linktitle: Ingebedde DGN exporteren
second_title: Aspose.CAD Java-API
description: Ontdek de stapsgewijze handleiding voor het exporteren van ingesloten DGN-bestanden naar PDF met Aspose.CAD voor Java. Verbeter uw Java-applicaties met naadloze manipulatie van CAD-bestanden.
type: docs
weight: 11
url: /nl/java/dgn-export-options/export-embedded-dgn/
---
## Invoering

Welkom bij deze uitgebreide tutorial over het exporteren van ingebedde DGN-bestanden met Aspose.CAD voor Java. Aspose.CAD is een krachtige bibliotheek waarmee Java-ontwikkelaars naadloos met CAD-bestanden kunnen werken. In deze zelfstudie begeleiden we u stapsgewijze instructies bij het exporteren van ingesloten DGN-bestanden naar PDF. Of u nu een doorgewinterde ontwikkelaar bent of net begint, deze tutorial helpt u de mogelijkheden van Aspose.CAD te benutten om uw Java-toepassingen te verbeteren.

## Vereisten

Voordat we ingaan op de tutorial, zorg ervoor dat je aan de volgende vereisten voldoet:
- Java-ontwikkelomgeving: Zorg ervoor dat er een Java-ontwikkelomgeving op uw computer is geïnstalleerd.
-  Aspose.CAD voor Java: Download en installeer de Aspose.CAD voor Java-bibliotheek van[hier](https://releases.aspose.com/cad/java/).

## Pakketten importeren

Om aan de slag te gaan, moet u de benodigde pakketten in uw Java-project importeren. Voeg de volgende importinstructies toe aan uw code:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Laten we nu de voorbeeldcode in meerdere stappen opsplitsen:

## Stap 1: Invoer- en uitvoerpaden instellen

Definieer het mappad waar uw document zich bevindt en geef de invoernaam van het DWG-bestand op.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
```

## Stap 2: Laad het DWG-bestand

 Laad het DWG-bestand in een`Image` object met behulp van Aspose.CAD.

```java
Image objImage = Image.load(fileName);
```

## Stap 3: Configureer rasterisatieopties

Configureer rasteropties, zoals lay-outs die moeten worden opgenomen in de export.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setLayouts(new String[] {"Model"});
```

## Stap 4: Configureer PDF-opties

Stel PDF-opties in, inclusief vectorrasteropties.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Stap 5: PDF-bestand opslaan

Sla het PDF-bestand op met de geconfigureerde opties.
```java
objImage.save(dataDir + "BlockRefDgn.pdf", pdfOptions);
```

## Conclusie

Gefeliciteerd! U hebt met succes een ingesloten DGN-bestand naar PDF geëxporteerd met Aspose.CAD voor Java. Deze tutorial behandelde de essentiële stappen om Aspose.CAD te integreren in uw Java-applicatie voor efficiënte manipulatie van CAD-bestanden.

## Veelgestelde vragen

### V1: Kan ik Aspose.CAD voor Java gebruiken in een commercieel project?

 A1: Ja, Aspose.CAD voor Java is een commerciële bibliotheek. Een licentie kunt u verkrijgen bij[hier](https://purchase.aspose.com/buy).

### Vraag 2: Is er een gratis proefversie beschikbaar?

 A2:Ja, u heeft toegang tot een gratis proefversie van Aspose.CAD voor Java[hier](https://releases.aspose.com/).

### V3: Hoe kan ik ondersteuning krijgen voor Aspose.CAD voor Java?

A3: U kunt ondersteuning zoeken bij de Aspose.CAD-gemeenschap op de[forum](https://forum.aspose.com/c/cad/19).

### Vraag 4: Wat moet ik doen als ik een tijdelijke licentie nodig heb?

 A4: U kunt een tijdelijke licentie verkrijgen[hier](https://purchase.aspose.com/temporary-license/).

### Vraag 5: Waar kan ik de documentatie vinden?

 A5: De documentatie is beschikbaar[hier](https://reference.aspose.com/cad/java/).