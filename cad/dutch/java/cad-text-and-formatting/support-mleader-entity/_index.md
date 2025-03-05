---
title: Ondersteuning van MLeader Entity voor DWG-formaat met Aspose.CAD voor Java
linktitle: Ondersteuning van MLeader Entity voor DWG-formaat met Java
second_title: Aspose.CAD Java-API
description: Ontgrendel de kracht van Aspose.CAD voor Java met onze stapsgewijze zelfstudie over het ondersteunen van MLeader-entiteiten in DWG-indeling.
type: docs
weight: 12
url: /nl/java/cad-text-and-formatting/support-mleader-entity/
---
## Invoering

Op het gebied van computerondersteund ontwerp (CAD) met Java is het begrijpen en implementeren van ondersteuning voor MLeader-entiteiten in DWG-formaat een waardevolle vaardigheid. Aspose.CAD voor Java biedt een robuuste oplossing voor dergelijke taken en biedt een reeks krachtige tools en functionaliteiten. Deze tutorial leidt u door het proces van het ondersteunen van MLeader-entiteiten binnen DWG-bestanden met behulp van Java met Aspose.CAD.

## Vereisten

Voordat we dieper ingaan op de zelfstudie, moet u ervoor zorgen dat u aan de volgende vereisten voldoet:

1. Java-ontwikkelomgeving: Zorg ervoor dat er een Java-ontwikkelomgeving op uw systeem is geïnstalleerd.

2.  Aspose.CAD-bibliotheek: Download en installeer de Aspose.CAD-bibliotheek voor Java vanaf de[download link](https://releases.aspose.com/cad/java/).

## Naamruimten importeren

Importeer in uw Java-project de benodigde naamruimten om de mogelijkheden van Aspose.CAD effectief te benutten. Neem de volgende regels op in uw code:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeader;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeaderContextData;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeaderLine;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeaderNode;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;

```

Laten we nu de code opsplitsen in een stapsgewijze handleiding om MLeader-entiteiten voor DWG-indeling te ondersteunen met behulp van Java met Aspose.CAD.

## 1. Laad het DWG-bestand en open CadImage

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String file = dataDir + "Multileaders.dwg";
Image image = Image.load(file);
CadImage cadImage = (CadImage) image;
```

## 2. Valideer MLeader-entiteiten

```java
Assert.areNotEqual(cadImage.getEntities().length, 0);
CadMLeader cadMLeader = (CadMLeader) cadImage.getEntities()[2];
```

### 3. Controleer de stijl en kenmerken van MLeader

```java
Assert.areEqual(cadMLeader.getStyleDescription(), "Standard");
Assert.areEqual(cadMLeader.getLeaderStyleId(), "12E");
Assert.areEqual(cadMLeader.getArrowHeadId1(), "639");
Assert.areEqual(cadMLeader.getLeaderLineTypeID(), "14");
```

## 4. Toegang tot MLeader-contextgegevens

```java
CadMLeaderContextData context = cadMLeader.getContextData();
```

## 5. Valideer contextkenmerken

```java
Assert.areEqual(context.getArrowHeadSize(), 30.0, 0.1);
Assert.areEqual(context.getBasePoint().getX(), 481, 1);
Assert.areEqual(context.getContentScale(), 1.0, 0.01);
Assert.areEqual(context.getDefaultText().getValue(), "This is multileader with huge text\\P{\\H1.5x;6666666666666666666666666666\\P}bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb");
Assert.areEqual(context.hasMText(), true);
```

## 6. Ga naar MLeader Node en Leader Line

```java
CadMLeaderNode mleaderNode = context.getLeaderNode();
Assert.areEqual(mleaderNode.getLastLeaderLinePoint().getX(), 473, 1);

CadMLeaderLine leaderLine = mleaderNode.getLeaderLine();
Assert.areEqual(leaderLine.getBreakEndPoint().toString(), null);
Assert.areEqual(Integer.toString(leaderLine.getBreakPointIndex().getValue()), Integer.toString(0));
Assert.areEqual(leaderLine.getBreakStartPoint().toString(), null);
Assert.areEqual(Integer.toString(leaderLine.getLeaderLineIndex().getValue()), Integer.toString(0));
Assert.areEqual(Integer.toString(leaderLine.getLeaderPoints().size()), Integer.toString(4));
```

## 7. Valideer aanvullende MLeader-attributen

```java
Assert.areEqual(Integer.toString(mleaderNode.getBranchIndex()), Integer.toString(0));
Assert.areEqual(mleaderNode.getDogLegLength(), 8.0, 0.1);
Assert.areEqual(context.hasMText(), true);
```

## 8. Valideer tekstkenmerken

```java
Assert.areEqual(context.getTextAttachmentType().getValue(), (short) 1);
Assert.areEqual(context.getTextBackgroundColor().getValue(), 18);
Assert.areEqual(context.getTextHeight(), 20.0, 0.1);
Assert.areEqual(context.getTextStyleID().getValue(), "11");
Assert.areEqual(context.getTextRotation().getValue(), 0.0, 0.01);
```

## 9. Aanvullende MLeader-attributen

```java
Assert.areEqual(cadMLeader.getArrowHeadId1(), "639");
Assert.areEqual(cadMLeader.getLeaderType(), 1);
Assert.areEqual(cadMLeader.getBlockContentColor(), 0);
Assert.areEqual(cadMLeader.getLeaderLineColor(), 0);
Assert.areEqual(cadMLeader.getTextHeight(), 1.0, 0.01);
```

## Conclusie

Gefeliciteerd! U heeft met succes door de uitgebreide handleiding genavigeerd over het ondersteunen van MLeader-entiteiten voor de DWG-indeling met behulp van Java en Aspose.CAD. Deze mogelijkheid opent deuren voor geavanceerde CAD-manipulaties en verbetert uw Java-ontwikkeltoolkit.

## Veelgestelde vragen

### V1: Kan ik Aspose.CAD voor Java gebruiken met andere CAD-formaten?

A1: Ja, Aspose.CAD ondersteunt verschillende CAD-formaten naast DWG, wat veelzijdigheid in uw projecten biedt.

### V2: Waar kan ik gedetailleerde documentatie vinden voor Aspose.CAD voor Java?

 A2: Raadpleeg de[documentatie](https://reference.aspose.com/cad/java/) voor diepgaande inzichten in de mogelijkheden van Aspose.CAD.

### Vraag 3: Is er een gratis proefversie beschikbaar?

 A3: Ja, verken de functionaliteiten uit de eerste hand met de[gratis proefperiode](https://releases.aspose.com/).

### V4: Hoe kan ik tijdelijke licenties krijgen voor Aspose.CAD?

A4: Verkrijg een tijdelijke licentie via[deze link](https://purchase.aspose.com/temporary-license/).

### Vraag 5: Waar kan ik gemeenschapssteun en hulp zoeken?

A5: Bezoek de[Aspose.CAD-forum](https://forum.aspose.com/c/cad/19) om verbinding te maken met de gemeenschap en hulp te krijgen.