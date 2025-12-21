---
date: 2025-12-21
description: Converteer IFC naar PNG moeiteloos met Aspose.CAD voor Java. Volg onze
  stapsgewijze tutorial.
linktitle: Export IFC to PNG
second_title: Aspose.CAD Java API
title: Converteer IFC naar PNG met Aspose.CAD voor Java
url: /nl/java/cad-export-options/export-ifc-to-png/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# IFC naar PNG converteren met Aspose.CAD voor Java

## Introductie

In deze tutorial leer je **hoe je IFC naar PNG kunt converteren** met de krachtige Aspose.CAD bibliotheek voor Java. Of je nu een BIM-viewer bouwt, miniatuurafbeeldingen genereert voor een bouwportaal, of documentatie‑pijplijnen automatiseert, het converteren van IFC (Industry Foundation Classes) bestanden naar rasterafbeeldingen is een veelvoorkomende vereiste. We lopen elke stap door, leggen de reden achter de instellingen uit en geven je tips om de beste visuele resultaten te behalen.

## Snelle antwoorden
- **Welke bibliotheek is nodig?** Aspose.CAD for Java (gratis proefversie beschikbaar).  
- **Ondersteunde IFC‑versies?** De meeste IFC 2x3‑ en IFC4‑bestanden worden verwerkt.  
- **Typische conversietijd?** Enkele seconden voor standaardmodellen; hangt af van de bestandsgrootte.  
- **Heb ik een licentie nodig?** Een tijdelijke licentie is vereist voor productiegebruik.  
- **Kan ik de afbeeldingsgrootte aanpassen?** Ja – gebruik `CadRasterizationOptions` om breedte en hoogte in te stellen.

## Wat betekent “IFC naar PNG converteren”?
IFC naar PNG converteren betekent het rasteren van een 3‑D bouwmodel (IFC) naar een 2‑D bitmap‑afbeelding (PNG). Dit proces vlakt de geometrie af, past standaard visuele stijlen toe en produceert een draagbare afbeelding die kan worden weergegeven in browsers, rapporten of mobiele apps zonder dat een CAD‑viewer nodig is.

## Waarom Aspose.CAD voor Java gebruiken?
- **Geen externe CAD‑software** – pure Java‑API, werkt op elk platform.  
- **Hoge‑fidelity weergave** – behoudt lijndiktes, kleuren en lagen.  
- **Volledige controle** – rasterisatie‑opties laten je resolutie, achtergrond en meer definiëren.  
- **Eenvoudige licenties** – proef‑ en tijdelijke licenties vereenvoudigen evaluatie.

## Voorvereisten

Voordat we beginnen, zorg ervoor dat je het volgende hebt:

- **Aspose.CAD Bibliotheek** – download en installeer deze via de [download link](https://releases.aspose.com/cad/java/).  
- **Java Development Kit (JDK)** – versie 8 of hoger.  
- **Een map** die het IFC‑bestand bevat dat je wilt converteren.

## Namespaces importeren

Importeer in je Java‑project de benodigde klassen:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## Stapsgewijze handleiding

### Stap 1: Het IFC‑bestand laden

```java
String dataDir = "Your Document Directory" + "ExportingIFC/";
String fileName = dataDir + "example.ifc";
IfcImage cadImage = (IfcImage)Image.load(fileName);
```

Hier laden we het bron‑IFC‑bestand in een `IfcImage`‑object. Aspose.CAD parseert automatisch de IFC‑structuur en maakt deze klaar voor rasterisatie.

### Stap 2: Vector‑ (Rasterisatie)‑opties instellen

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

`CadRasterizationOptions` bepaalt hoe de 3‑D‑geometrie wordt afgevlakt. Pas `PageWidth` en `PageHeight` aan om de gewenste PNG‑resolutie te krijgen. Grotere waarden geven meer detail, maar verhogen het geheugenverbruik.

### Stap 3: PNG‑exportinstellingen configureren

```java
PngOptions pngOptions = new PngOptions();
pngOptions.setVectorRasterizationOptions(vectorOptions);
```

`PngOptions` geeft Aspose.CAD de instructie om een PNG‑bestand te genereren en koppelt de rasterisatie‑instellingen die in de vorige stap zijn gedefinieerd.

### Stap 4: De afbeelding opslaan als PNG

```java
String outPath = dataDir + "example.png";
cadImage.save(outPath, pngOptions);
```

De `save`‑methode schrijft de gerasterde afbeelding naar schijf. Na het uitvoeren van deze regel vind je `example.png` in dezelfde map als je bron‑IFC‑bestand.

## Veelvoorkomende problemen en oplossingen

| Issue | Why it Happens | Fix |
|-------|----------------|-----|
| **Lege PNG‑output** | Rasterisatie‑opties breedte/hoogte zijn ingesteld op 0 of zeer klein. | Zorg ervoor dat `PageWidth` en `PageHeight` positieve gehele getallen zijn (bijv. 1500). |
| **Ontbrekende lagen of kleuren** | Standaardweergave kan bepaalde lagen verbergen. | Gebruik `vectorOptions.setRenderMode(CadRenderMode.Wireframe)` of pas de laag‑zichtbaarheid aan via de API (indien nodig). |
| **Out‑of‑memory‑fouten** voor enorme IFC‑bestanden | Een zeer hoge resolutie verbruikt veel RAM. | Verlaag de resolutie of verwerk het model in secties. |

## Veelgestelde vragen

### Q1: Is Aspose.CAD compatibel met alle versies van IFC‑bestanden?
A1: Aspose.CAD ondersteunt verschillende versies van IFC‑bestanden. Raadpleeg de [documentatie](https://reference.aspose.com/cad/java/) voor compatibiliteitsdetails.

### Q2: Kan ik de rasterisatie‑opties verder aanpassen?
A2: Zeker! Bekijk de [documentatie](https://reference.aspose.com/cad/java/) voor geavanceerde aanpassingsopties.

### Q3: Is er een proefversie beschikbaar?
A3: Ja, je kunt de gratis proefversie hier vinden [here](https://releases.aspose.com/).

### Q4: Hoe kan ik een tijdelijke licentie voor Aspose.CAD verkrijgen?
A4: Verkrijg een tijdelijke licentie via [this link](https://purchase.aspose.com/temporary-license/).

### Q5: Waar kan ik hulp zoeken of problemen bespreken?
A5: Bezoek het [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) voor community‑ondersteuning.

## Veelgestelde vragen (extra)

**Q: Kan ik meerdere IFC‑bestanden in één batch converteren?**  
A: Ja. Plaats de laad‑ en opslaalogica in een lus die over een lijst met bestandspaden iterereert.

**Q: Hoe wijzig ik de achtergrondkleur van de PNG?**  
A: Stel `vectorOptions.setBackgroundColor(Color.getWhite())` in (of een andere `java.awt.Color`) vóór het aanmaken van `PngOptions`.

**Q: Is het mogelijk om te exporteren naar andere rasterformaten zoals JPEG of BMP?**  
A: Zeker. Vervang `PngOptions` door `JpegOptions` of `BmpOptions` en pas eventuele formaat‑specifieke instellingen aan.

**Q: Moet ik bronnen vrijgeven na conversie?**  
A: Roep `cadImage.dispose()` aan wanneer je klaar bent om native geheugen vrij te maken.

**Laatst bijgewerkt:** 2025-12-21  
**Getest met:** Aspose.CAD for Java 24.12 (latest at time of writing)  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}