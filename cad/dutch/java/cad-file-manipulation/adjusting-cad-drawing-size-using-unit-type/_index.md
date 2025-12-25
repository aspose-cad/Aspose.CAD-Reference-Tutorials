---
date: 2025-12-25
description: Leer hoe u DWG naar BMP exporteert met Aspose.CAD voor Java. Deze stapsgewijze
  handleiding laat zien hoe u de grootte van CAD-tekeningen aanpast en CAD efficiënt
  naar BMP converteert.
linktitle: Adjusting CAD Drawing Size Using Unit Type
second_title: Aspose.CAD Java API
title: DWG exporteren naar BMP – CAD-grootte aanpassen met eenheidstype (Java)
url: /nl/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG exporteren naar BMP – CAD‑tekeningsgrootte aanpassen met Unit Type met Aspose.CAD voor Java

## Inleiding

Wanneer je **DWG naar BMP moet exporteren**, is het essentieel om de uitvoergrootte en meeteenheid te beheersen voor verdere verwerking of afdrukken. In deze tutorial leer je hoe je de CAD‑tekeningsgrootte aanpast en CAD naar BMP converteert met Aspose.CAD voor Java, waarbij de eigenschap `UnitType` wordt gebruikt om de meeteenheid te definiëren. De stappen worden in eenvoudige bewoordingen uitgelegd, zodat je kunt volgen, zelfs als je nieuw bent met de bibliotheek.

## Snelle antwoorden
- **Wat betekent “export DWG to BMP”?** Een DWG‑tekening omzetten naar een BMP‑rasterafbeelding.  
- **Welke eigenschap bepaalt de uitvoergrootte?** `CadRasterizationOptions.setUnitType()` stelt de eenheid in (bijv. centimeter).  
- **Heb ik een licentie nodig om de code uit te voeren?** Een gratis proefversie werkt voor evaluatie; een licentie is vereist voor productie.  
- **Kan ik andere lay-outs kiezen?** Ja, gebruik `setLayouts()` om model‑ of paperspace‑lay-outs op te geven.  
- **Welke uitvoerformaten worden ondersteund?** Naast BMP kun je exporteren naar PNG, JPEG, TIFF, enz., door de opties‑klasse aan te passen.

## Wat is **export DWG to BMP**?

Exporteren van DWG naar BMP betekent het rasteren van een vector‑gebaseerd DWG‑bestand naar een bitmap‑afbeelding (BMP). Dit is nuttig wanneer je een pixel‑perfecte weergave nodig hebt voor legacy‑systemen, beeldverwerkings‑pipelines of eenvoudige weergavescenario’s.

## Waarom CAD‑tekeningsgrootte aanpassen met **Unit Type**?

Het instellen van het eenheidstype laat je de fysieke afmetingen van de geëxporteerde afbeelding bepalen zonder handmatig schaalfactoren te berekenen. Dit zorgt ervoor dat de bitmap overeenkomt met werkelijke afmetingen (bijv. centimeters), wat cruciaal is voor technische tekeningen en gedrukte documentatie.

## Voorvereisten

Zorg ervoor dat je de volgende voorvereisten hebt voordat je aan de tutorial begint:

- **Java‑ontwikkelomgeving** – Een werkende JDK (8 of hoger) en een IDE of build‑tool (Maven/Gradle).  
- **Aspose.CAD voor Java‑bibliotheek** – Download en integreer de Aspose.CAD‑bibliotheek in je Java‑project. Je kunt de bibliotheek verkrijgen [hier](https://releases.aspose.com/cad/java/).

## Namespaces importeren

Voeg in je Java‑code de benodigde namespaces toe om toegang te krijgen tot de Aspose.CAD‑functionaliteit. Voeg de volgende imports toe:

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Laten we nu het proces van het aanpassen van de CAD‑tekeningsgrootte met unit type in beheersbare stappen opdelen:

## Stap 1: Data‑directory definiëren

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

Stel het pad in voor de map waarin je CAD‑bestanden zich bevinden.

## Stap 2: CAD‑tekening laden

```java
String sourceFilePath = dataDir + "sample.dwg";
Image image = Image.load(sourceFilePath);
```

Laad de CAD‑tekening met behulp van de `Image`‑klasse van Aspose.CAD.

## Stap 3: BMP‑opties maken

```java
BmpOptions bmpOptions = new BmpOptions();
```

Instantieer de `BmpOptions`‑klasse voor het exporteren van de CAD‑lay-out naar BMP‑formaat.

## Stap 4: Rasterisatie‑opties configureren

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

Maak een instantie van `CadRasterizationOptions` en koppel deze aan de `BmpOptions` voor vector‑rasterisatie.

## Stap 5: Unit Type instellen

```java
cadRasterizationOptions.setUnitType(UnitType.Centimeter);
```

Geef het gewenste eenheidstype op voor de CAD‑tekening. In dit voorbeeld hebben we het ingesteld op **Centimeter**, wat de geëxporteerde afbeeldingsgrootte direct beïnvloedt wanneer je **CAD‑tekeningsgrootte aanpast**.

## Stap 6: Lay-outs instellen

```java
cadRasterizationOptions.setLayouts(new String[] { "Model" });
```

Definieer de lay-outs die tijdens de export in aanmerking worden genomen. In dit geval hebben we de **"Model"**‑lay-out geselecteerd, maar je kunt overschakelen naar paperspace‑lay-outs indien nodig.

## Stap 7: Exporteren naar BMP

```java
String outPath = sourceFilePath + ".bmp";
image.save(outPath, bmpOptions);
```

Sla tenslotte de gewijzigde CAD‑tekening op in BMP‑formaat. Deze stap voltooit de **export DWG to BMP**‑workflow terwijl de door jou geconfigureerde grootte‑aanpassingen behouden blijven.

## Veelvoorkomende problemen en oplossingen

| Probleem | Oorzaak | Oplossing |
|----------|---------|-----------|
| **Uitvoerafbeelding is te klein** | Eenheidstype niet ingesteld of standaard (pixel) gebruikt | Roep `setUnitType()` aan met de gewenste meeteenheid (bijv. `UnitType.Centimeter`). |
| **Verkeerde lay-out geëxporteerd** | Typfout in lay-outnaam | Controleer lay-outnamen met een CAD‑viewer; gebruik de exacte tekenreeks in `setLayouts()`. |
| **Licentie‑exception** | Uitvoeren zonder geldige licentie in productie | Pas een tijdelijke of permanente licentie toe zoals beschreven in de FAQ. |

## Veelgestelde vragen (uitgebreid)

**V: Kan ik Aspose.CAD voor Java gebruiken met andere programmeertalen?**  
A: Aspose.CAD ondersteunt voornamelijk Java, maar er zijn versies beschikbaar voor andere talen zoals .NET.

**V: Zijn er licentie‑opties voor Aspose.CAD?**  
A: Ja, je kunt licentie‑opties verkennen en Aspose.CAD aanschaffen [hier](https://purchase.aspose.com/buy).

**V: Is er een gratis proefversie beschikbaar voor Aspose.CAD?**  
A: Zeker, je kunt een gratis proefversie krijgen [hier](https://releases.aspose.com/).

**V: Hoe krijg ik ondersteuning voor Aspose.CAD voor Java?**  
A: Bezoek het Aspose.CAD‑forum [hier](https://forum.aspose.com/c/cad/19) voor uitgebreide ondersteuning.

**V: Kan ik een tijdelijke licentie voor Aspose.CAD verkrijgen?**  
A: Ja, je kunt een tijdelijke licentie verkrijgen [hier](https://purchase.aspose.com/temporary-license/).

---

**Laatst bijgewerkt:** 2025-12-25  
**Getest met:** Aspose.CAD voor Java 24.10  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}