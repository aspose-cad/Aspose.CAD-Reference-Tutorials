---
date: 2026-01-10
description: Leer hoe je DGN naar DWG exporteert en MicroStation DGN naar AutoCAD
  DWG converteert met Aspose.CAD voor Java. Stapsgewijze handleiding.
linktitle: Export DGN as Part of DWG
second_title: Aspose.CAD Java API
title: Exporteer DGN naar DWG met Aspose.CAD voor Java
url: /nl/java/dgn-export-options/export-dgn-as-part-of-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export DGN naar DWG met Aspose.CAD voor Java

## Inleiding

In deze tutorial leer je hoe je **export dgn to dwg** kunt uitvoeren en een MicroStation DGN‑ontwerp kunt insluiten in een AutoCAD DWG‑bestand met behulp van de Aspose.CAD‑bibliotheek voor Java. Of je nu legacy MicroStation‑tekeningen migreert of DGN‑onderleggers wilt combineren met DWG‑lay-outs, deze gids leidt je stap voor stap door het proces—van het opzetten van de omgeving tot het genereren van een PDF‑preview van de uiteindelijke DWG.

## Snelle antwoorden
- **Wat doet “export dgn to dwg”?** Het voegt een DGN‑onderlegger toe aan een DWG, waardoor naadloos bekijken in AutoCAD mogelijk is.
- **Naar welk formaat kan ik het resultaat exporteren voor een snelle preview?** Je kunt **export cad file to pdf** gebruiken met `PdfOptions`.
- **Heb ik een licentie nodig om de code uit te voeren?** Een tijdelijke of betaalde Aspose.CAD‑licentie is vereist voor productiegebruik.
- **Welke Java‑versie wordt ondersteund?** Java 8 of hoger werkt met de nieuwste Aspose.CAD voor Java‑release.
- **Is er een gratis proefversie beschikbaar?** Ja – download een proefversie van de Aspose‑website.

## Wat is “export dgn to dwg”?
Exporteren van DGN naar DWG betekent het converteren of insluiten van een MicroStation DGN‑ontwerp als onderlegger in een AutoCAD DWG‑tekening. Dit stelt CAD‑professionals in staat bestaande DGN‑assets te benutten zonder de geometrie vanaf nul opnieuw te maken.

## Waarom MicroStation DGN naar AutoCAD DWG converteren?
- **Samenwerking:** Teams die AutoCAD gebruiken kunnen DGN‑inhoud direct bekijken en bewerken.
- **Standaardisatie:** DWG is het de‑facto formaat voor veel downstream‑workflows (bijv. PDF‑generatie, 3D‑rendering).
- **Behoud:** Houdt de originele DGN‑referenties intact, waardoor gegevensverlies wordt verminderd.

## Vereisten

Voordat we aan de tutorial beginnen, zorg ervoor dat je de volgende vereisten hebt:
1. **Aspose.CAD‑bibliotheek:** Download en installeer de Aspose.CAD‑bibliotheek voor Java. Je kunt de bibliotheek vinden [hier](https://releases.aspose.com/cad/java/).
2. **Java Development Kit (JDK):** Zorg ervoor dat Java op je systeem is geïnstalleerd.
3. **Integrated Development Environment (IDE):** Kies een Java‑IDE zoals Eclipse of IntelliJ voor een soepelere ontwikkelervaring.

## Importeer pakketten

Importeer in je Java‑project de benodigde Aspose.CAD‑pakketten om CAD‑bestanden te manipuleren. Hieronder een voorbeeld:

```java
import com.aspose.cad;
import com.aspose.cad.imageoptions;
import com.aspose.cad.fileformats.cad.cadconsts;
import com.aspose.cad.fileformats.cad;
import com.aspose.cad.fileformats.cad.cadobjects;
```

## Stap 1: Stel bestands‑paden in

Definieer de invoer‑ en uitvoer‑bestands‑paden voor het DWG‑bestand. Werk de variabelen `dataDir`, `fileName` en `outPath` dienovereenkomstig bij.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
String outPath = dataDir + "BlockRefDgn.dwg.pdf";
```

## Stap 2: Maak een PdfOptions‑instantie

Maak een instantie van de `PdfOptions`‑klasse, omdat we **export the CAD file to PDF** uitvoeren voor snelle verificatie.

```java
PdfOptions exportOptions = new PdfOptions();
```

## Stap 3: Laad DWG‑bestand

Laad het bestaande DWG‑bestand als een afbeelding en converteer het naar het type `CadImage`.

```java
CadImage cadImage = (CadImage) Image.load(fileName);
```

## Stap 4: Doorloop entiteiten

Loop door elke entiteit in het DWG‑bestand en controleer of het een afbeeldingdefinitie is. Indien ja, haal de externe referentie naar het object op.

```java
for (CadBaseEntity baseEntity : cadImage.getEntities()) {
    if (baseEntity.getTypeName() == CadEntityTypeName.DGNUNDERLAY) {
        CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
        System.out.println(dgnFile.getUnderlayPath());
    }
}
```

## Stap 5: Definieer rasterisatie‑opties

Definieer de instellingen voor het `CadRasterizationOptions`‑object, inclusief paginabreedte, -hoogte, lay-outs en achtergrondkleur.

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

## Stap 6: Stel vector‑rasterisatie‑opties in

Stel de vector‑rasterisatie‑opties in voor de export.

```java
exportOptions.setVectorRasterizationOptions(vectorRasterizationOptions);
```

## Stap 7: Exporteer DWG naar PDF

Exporteer tenslotte de DWG naar PDF door de `save`‑methode aan te roepen.

```java
cadImage.save(outPath, exportOptions);
```

## Veelvoorkomende problemen en oplossingen

| Probleem | Oorzaak | Oplossing |
|----------|---------|-----------|
| **Geen DGN‑onderlegger zichtbaar** | De DWG bevat geen `DGNUNDERLAY`‑entity. | Controleer of de bron‑DWG een DGN‑referentie bevat. |
| **PDF is leeg** | Rasterisatie‑opties ingesteld op nul grootte of verkeerde lay-out. | Zorg ervoor dat `setPageWidth`/`setPageHeight` positief zijn en `setLayouts` overeenkomt met de DWG‑lay-outnaam. |
| **Licentie‑exceptie** | Uitvoeren zonder een geldige Aspose.CAD‑licentie. | Pas een tijdelijke of aangeschafte licentie toe voordat je API‑methoden aanroept. |

## Veelgestelde vragen

### Q1: Waar kan ik de documentatie voor Aspose.CAD voor Java vinden?

A1: De documentatie is te vinden [hier](https://reference.aspose.com/cad/java/).

### Q2: Hoe kan ik de Aspose.CAD‑bibliotheek voor Java downloaden?

A2: Je kunt de bibliotheek downloaden via [deze link](https://releases.aspose.com/cad/java/).

### Q3: Is er een gratis proefversie beschikbaar voor Aspose.CAD voor Java?

A3: Ja, je kunt de gratis proefversie vinden [hier](https://releases.aspose.com/).

### Q4: Waar kan ik een tijdelijke licentie voor Aspose.CAD voor Java verkrijgen?

A4: Verkrijg een tijdelijke licentie [hier](https://purchase.aspose.com/temporary-license/).

### Q5: Hulp nodig of vragen?

A5: Bezoek het Aspose.CAD‑community‑ondersteuningsforum [hier](https://forum.aspose.com/c/cad/19).

### Q6: Kan ik de resulterende PDF terug converteren naar DWG?

A6: De PDF is een raster‑preview; terug converteren naar DWG vereist een apart reverse‑engineering‑tool.

### Q7: Werkt deze aanpak met andere CAD‑formaten zoals DWF of DXF?

A7: Ja, Aspose.CAD ondersteunt vele formaten; je hoeft alleen de bestandsextensies en rasterisatie‑instellingen aan te passen.

---

**Laatst bijgewerkt:** 2026-01-10  
**Getest met:** Aspose.CAD for Java 24.11  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}