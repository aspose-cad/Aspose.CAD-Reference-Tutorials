---
title: Exporteer DWG naar PDF of Raster met Aspose.CAD voor Java
linktitle: Exporteer DWG naar PDF of Raster
second_title: Aspose.CAD Java-API
description: Ontdek het naadloze proces van het exporteren van DWG-bestanden naar PDF of rasterafbeeldingen in Java met behulp van Aspose.CAD. Deze stap-voor-stap handleiding zorgt voor precisie en efficiëntie.
type: docs
weight: 13
url: /nl/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
---
## Invoering

In de dynamische wereld van computerondersteund ontwerp (CAD) is een efficiënte omgang met tekeningen cruciaal. Aspose.CAD voor Java biedt een krachtige oplossing voor het exporteren van DWG-bestanden naar PDF of rasterafbeeldingen. Deze tutorial leidt u door het proces en zorgt ervoor dat u het volledige potentieel van Aspose.CAD voor Java benut.

## Vereisten

Voordat u in de zelfstudie duikt, moet u ervoor zorgen dat u over het volgende beschikt:

- Basiskennis van Java-programmeren.
-  Aspose.CAD voor Java-bibliotheek geïnstalleerd. Zo niet, download het dan[hier](https://releases.aspose.com/cad/java/).
- Een DWG-bestand voor testdoeleinden. U kunt het meegeleverde bestand "Bottom_plate.dwg" gebruiken.

## Naamruimten importeren

Importeer in uw Java-project de benodigde naamruimten om het proces een vliegende start te geven:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## Stap 1: Laad het DWG-bestand

 Begin met het laden van uw DWG-bestand met Aspose.CAD's`Image` klas:

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

## Stap 2: Bepaal het eenheidstype

Controleer vervolgens het eenheidstype van het geladen DWG-bestand:

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

## Stap 3: Rasterisatie-opties instellen

Configureer de rasteropties op basis van het eenheidstype:

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();

if (currentUnitIsMetric) {
    // Metrische eenheden
    double metersCoeff = 1 / 1000.0;
    double scaleFactor = metersCoeff / currentUnitCoefficient;
    rasterizationOptions.setPageWidth((float)(210 * scaleFactor));
    rasterizationOptions.setPageHeight((float)(297 * scaleFactor));
    rasterizationOptions.setUnitType(UnitType.Millimeter);
} else {
    // Imperiale eenheden
    rasterizationOptions.setPageWidth((float)(8.27f / currentUnitCoefficient));
    rasterizationOptions.setPageHeight((float)(11.69f / currentUnitCoefficient));
    rasterizationOptions.setUnitType(UnitType.Inch);
}
```

## Stap 4: Configureer PDF-opties

PDF-exportopties instellen:

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

## Stap 5: Opslaan als PDF

Sla ten slotte het DWG-bestand op als PDF:

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

En daar heb je het! U hebt met succes een DWG-bestand naar PDF geëxporteerd met Aspose.CAD voor Java.

## Conclusie

Deze tutorial biedt een stapsgewijze handleiding voor het gebruik van Aspose.CAD voor Java om DWG-bestanden naar PDF of rasterafbeeldingen te exporteren. Deze bibliotheek vereenvoudigt het proces, waardoor u CAD-tekeningen efficiënt kunt verwerken in uw Java-applicaties.

## Veelgestelde vragen

### V1: Kan ik Aspose.CAD voor Java gebruiken met andere Java-frameworks?

A1: Ja, Aspose.CAD voor Java kan naadloos worden geïntegreerd met populaire Java-frameworks.

### V2: Is er een tijdelijke licentie beschikbaar voor Aspose.CAD voor Java?

 A2: Ja, u kunt een tijdelijke licentie verkrijgen[hier](https://purchase.aspose.com/temporary-license/).

### V3: Waar kan ik ondersteuning vinden voor Aspose.CAD voor Java?

 A3: Bezoek de[Aspose.CAD-forum](https://forum.aspose.com/c/cad/19) om hulp van de gemeenschap.

### V4: Hoe kan ik een licentie kopen voor Aspose.CAD voor Java?

 A4: U kunt een licentie kopen[hier](https://purchase.aspose.com/buy).

### V5: Welke eenheden ondersteunt Aspose.CAD voor Java?

A5: Aspose.CAD voor Java ondersteunt zowel metrische als imperiale eenheden.