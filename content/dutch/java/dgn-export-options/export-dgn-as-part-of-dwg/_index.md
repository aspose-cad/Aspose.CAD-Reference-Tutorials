---
title: Exporteer DGN naar DWG met Aspose.CAD voor Java
linktitle: Exporteer DGN als onderdeel van DWG
second_title: Aspose.CAD Java-API
description: Ontdek hoe u DGN kunt exporteren als onderdeel van DWG met Aspose.CAD voor Java. Volg onze stapsgewijze handleiding voor efficiënte manipulatie van CAD-bestanden.
type: docs
weight: 10
url: /nl/java/dgn-export-options/export-dgn-as-part-of-dwg/
---
## Invoering

In deze zelfstudie onderzoeken we hoe u Aspose.CAD voor Java kunt gebruiken om een DGN-bestand (MicroStation Design) te exporteren als onderdeel van een DWG-bestand (AutoCAD Drawing). Aspose.CAD is een krachtige bibliotheek die uitgebreide functionaliteit biedt om met CAD-bestandsformaten te werken. Deze stapsgewijze handleiding helpt u het proces van het exporteren van DGN als onderdeel van DWG met behulp van Java te begrijpen.

## Vereisten

Voordat we ingaan op de tutorial, zorg ervoor dat je aan de volgende vereisten voldoet:
1. Aspose.CAD-bibliotheek: Download en installeer de Aspose.CAD-bibliotheek voor Java. Je kunt de bibliotheek vinden[hier](https://releases.aspose.com/cad/java/).
2. Java Development Kit (JDK): Zorg ervoor dat Java op uw systeem is geïnstalleerd.
3. Integrated Development Environment (IDE): Kies een Java IDE zoals Eclipse of IntelliJ voor een soepelere ontwikkelervaring.

## Pakketten importeren

Importeer in uw Java-project de benodigde Aspose.CAD-pakketten om manipulatie van CAD-bestanden mogelijk te maken. Hier is een voorbeeld:

```java
import com.aspose.cad;
import com.aspose.cad.imageoptions;
import com.aspose.cad.fileformats.cad.cadconsts;
import com.aspose.cad.fileformats.cad;
import com.aspose.cad.fileformats.cad.cadobjects;
```

## Stap 1: Stel bestandspaden in

 Definieer de invoer- en uitvoerbestandspaden voor het DWG-bestand. Update de`dataDir`, `fileName` , En`outPath` variabelen dienovereenkomstig.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
String outPath = dataDir + "BlockRefDgn.dwg.pdf";
```

## Stap 2: Maak een PdfOptions-instantie

 Maak een exemplaar van de`PdfOptions` class, omdat we het DWG-bestand naar PDF-formaat exporteren.

```java
PdfOptions exportOptions = new PdfOptions();
```

## Stap 3: Laad het DWG-bestand

 Laad het bestaande DWG-bestand als afbeelding en converteer het naar de`CadImage` type.

```java
CadImage cadImage = (CadImage) Image.load(fileName);
```

## Stap 4: Herhaal de entiteiten

Doorloop elke entiteit in het DWG-bestand en controleer of het een afbeeldingsdefinitie is. Als dit het geval is, haalt u de externe verwijzing naar het object op.

```java
for (CadBaseEntity baseEntity : cadImage.getEntities()) {
    if (baseEntity.getTypeName() == CadEntityTypeName.DGNUNDERLAY) {
        CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
        System.out.println(dgnFile.getUnderlayPath());
    }
}
```

## Stap 5: Definieer rasterisatieopties

 Definieer instellingen voor de`CadRasterizationOptions`object, inclusief paginabreedte, hoogte, lay-outs en achtergrondkleur.

```java
CadRasterizationOptions vectorRasterizationOptions = new CadRasterizationOptions();
vectorRasterizationOptions.setPageWidth(1600);
vectorRasterizationOptions.setPageHeight(1600);
vectorRasterizationOptions.setLayouts(new String[] { "Model" });
vectorRasterizationOptions.setAutomaticLayoutsScaling(false);
vectorRasterizationOptions.setNoScaling(true);
vectorRasterizationOptions.setBackgroundColor(Color.getBlack());
vectorRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
```

## Stap 6: Stel opties voor vectorrasterisatie in

Stel de vectorrasteropties voor de export in.

```java
exportOptions.setVectorRasterizationOptions(vectorRasterizationOptions);
```

## Stap 7: Exporteer DWG naar PDF

 Exporteer ten slotte de DWG naar PDF door het bestand`save` methode.

```java
cadImage.save(outPath, exportOptions);
```

## Conclusie

Gefeliciteerd! U hebt met succes geleerd hoe u een DGN-bestand kunt exporteren als onderdeel van een DWG-bestand met Aspose.CAD voor Java. Deze krachtige bibliotheek biedt uitgebreide mogelijkheden voor het werken met CAD-bestanden, waardoor uw CAD-bestandsmanipulatietaken efficiënt en eenvoudig worden.

## Veelgestelde vragen

### V1: Waar kan ik de documentatie voor Aspose.CAD voor Java vinden?

 A1: De documentatie is te vinden[hier](https://reference.aspose.com/cad/java/).

### Vraag 2: Hoe kan ik de Aspose.CAD-bibliotheek voor Java downloaden?

 A2: U kunt de bibliotheek downloaden van[deze link](https://releases.aspose.com/cad/java/).

### V3: Is er een gratis proefversie beschikbaar voor Aspose.CAD voor Java?

 A3: Ja, u kunt de gratis proefversie vinden[hier](https://releases.aspose.com/).

### V4: Waar kan ik een tijdelijke licentie krijgen voor Aspose.CAD voor Java?

 A4: Verkrijg een tijdelijke licentie[hier](https://purchase.aspose.com/temporary-license/).

### Q5: Hulp nodig of vragen?

 A5: Bezoek het Aspose.CAD-communityondersteuningsforum[hier](https://forum.aspose.com/c/cad/19).