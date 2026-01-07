---
date: 2026-01-07
description: Leer hoe u CAD naar SVG kunt exporteren met Aspose.CAD voor Java. Deze
  stapsgewijze handleiding laat zien hoe u DWG naar SVG converteert, de SVG‑kleermodus
  instelt en de bibliotheek integreert in uw Java‑project.
linktitle: Export to SVG
second_title: Aspose.CAD Java API
title: CAD exporteren naar SVG met Aspose.CAD voor Java
url: /nl/java/cad-to-pdf-and-svg-export-options/export-to-svg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD exporteren naar SVG met Aspose.CAD voor Java

## Inleiding

Welkom in de wereld van Aspose.CAD voor Java, een krachtige bibliotheek die ontwikkelaars in staat stelt CAD-tekeningen moeiteloos te manipuleren. Of je nu een ervaren ontwikkelaar bent of nieuw bent in het CAD-gebied, deze uitgebreide gids leidt je stap voor stap door **CAD exporteren naar SVG**, laat zien hoe je DWG naar SVG converteert, de SVG-kleurmodus instelt en de API integreert in je Java‑project.

## Snelle antwoorden
- **Wat betekent “export CAD to SVG”?** Het converteert een CAD‑tekening (bijv. DWG) naar een Scalable Vector Graphics‑bestand dat in browsers kan worden weergegeven.  
- **Welke bibliotheek verzorgt de conversie?** Aspose.CAD voor Java biedt een eenvoudige API voor deze taak.  
- **Heb ik een licentie nodig voor ontwikkeling?** Een gratis proefversie werkt voor testen; een commerciële licentie is vereist voor productie.  
- **Kan ik de SVG‑kleuropbrengst regelen?** Ja, je kunt de SVG‑kleurmodus instellen (bijv. grijstinten).  
- **Is er extra software nodig?** Alleen een Java‑runtime en het Aspose.CAD‑JAR‑bestand.

## Vereisten

Voordat je aan de tutorial begint, zorg dat je de volgende zaken hebt:

- Java‑ontwikkelomgeving: Zorg dat Java op je systeem is geïnstalleerd.  
- Aspose.CAD‑bibliotheek: Download en installeer de Aspose.CAD voor Java‑bibliotheek vanaf de [downloadlink](https://releases.aspose.com/cad/java/).  
- Documentmap: Maak een map aan voor je CAD‑tekeningen en noteer het pad.

## Namespaces importeren

In deze stap importeren we de benodigde namespaces om onze Aspose.CAD‑reis te starten. Volg deze stappen:

### Stap 1: Open je Java‑project
Open je Java‑project in de IDE van je keuze.

### Stap 2: Voeg Aspose.CAD‑bibliotheek toe
Voeg de Aspose.CAD‑bibliotheek toe aan je project. Dit kun je doen door het JAR‑bestand op te nemen in de afhankelijkheden van je project.

### Stap 3: Importeren van namespaces
Importeer in je Java‑klasse de vereiste namespaces:

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.SvgOptions;
import com.aspose.cad.imageoptions.SvgColorMode;
```

## CAD exporteren naar SVG

Nu de basis is gelegd, duiken we in het stap‑voor‑stap proces van **CAD exporteren naar SVG** met Aspose.CAD voor Java.

### Stap 1: Specificeer de resource‑directory
Definieer het pad naar je resource‑directory, waar je CAD‑tekeningen zich bevinden:

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

### Stap 2: Laad de CAD‑tekening
Laad de CAD‑tekening met behulp van de Aspose.CAD‑bibliotheek:

```java
Image image = Image.load(dataDir + "meshes.dwg");
```

### Stap 3: Configureer SVG‑exportopties
Stel de SVG‑exportopties in om de uitvoer aan te passen. Hier **stellen we de SVG‑kleurmodus** in op grijstinten en vertellen we de exporter om tekst om te zetten naar vormen:

```java
SvgOptions options = new SvgOptions();
options.setColorType(SvgColorMode.Grayscale);
options.setTextAsShapes(true);
```

### Stap 4: Opslaan als SVG
Sla de CAD‑tekening op als een SVG‑bestand:

```java
image.save(dataDir + "meshes.svg");
```

> **Pro tip:** Als je **DWG naar SVG** wilt converteren met behoud van kleuren, wijzig je `SvgColorMode.Grayscale` naar `SvgColorMode.FullColor`.

Gefeliciteerd! Je hebt succesvol een CAD‑tekening geëxporteerd naar SVG met Aspose.CAD voor Java.

## Waarom Aspose.CAD gebruiken voor CAD exporteren naar SVG?
- **Hoge nauwkeurigheid:** Vectorgegevens blijven behouden, waardoor de SVG er precies uitziet als de originele CAD‑tekening.  
- **Geen externe afhankelijkheden:** De conversie draait volledig binnen Java, zonder extra tools.  
- **Aanpasbare uitvoer:** Opties zoals `setColorType` laten je bepalen of de SVG grijstinten of volledige kleur heeft.

## Veelvoorkomende problemen en oplossingen
- **Bestand niet gevonden:** Controleer of `dataDir` naar de juiste map wijst en of de DWG‑bestandsnaam klopt.  
- **Lege SVG‑output:** Zorg ervoor dat je `options.setTextAsShapes(true)` hebt ingesteld als de tekening tekst bevat die als vormen moet verschijnen.  
- **Niet‑ondersteund CAD‑formaat:** Aspose.CAD ondersteunt DWG, DXF, DWF en diverse andere formaten; raadpleeg de documentatie voor de volledige lijst.

## Conclusie

In deze tutorial hebben we het naadloze proces verkend van het benutten van Aspose.CAD voor Java om **CAD te exporteren naar SVG**. Met de intuïtieve API en robuuste functies vereenvoudigt Aspose.CAD complexe taken en biedt het ontwikkelaars een veelzijdig hulpmiddel voor CAD‑manipulatie.

## Veelgestelde vragen

### Q1: Kan ik Aspose.CAD voor Java gebruiken met andere CAD‑formaten?

A1: Ja, Aspose.CAD ondersteunt diverse CAD‑formaten, waaronder DWG, DXF, DWF en meer.

### Q2: Is Aspose.CAD geschikt voor zowel beginners als ervaren ontwikkelaars?

A2: Absoluut! Aspose.CAD biedt een gebruiksvriendelijke API, toegankelijk voor beginners, terwijl het geavanceerde functies biedt voor ervaren ontwikkelaars.

### Q3: Waar kan ik extra ondersteuning of community‑discussies vinden?

A3: Bezoek het [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) voor ondersteuning en discussies.

### Q4: Is er een gratis proefversie beschikbaar?

A4: Ja, je kunt Aspose.CAD uitproberen met een [gratis proefversie](https://releases.aspose.com/).

### Q5: Hoe kan ik een licentie aanschaffen voor Aspose.CAD voor Java?

A5: Je kunt een licentie kopen via de [aankooppagina](https://purchase.aspose.com/buy).

## Frequently Asked Questions

**Q: Kan ik een DXF‑bestand naar SVG converteren met dezelfde code?**  
A: Ja, vervang simpelweg de bestandsnaam door een DXF‑bestand; de API verwerkt beide formaten.

**Q: Hoe wijzig ik de uitvoer naar een full‑color SVG?**  
A: Stel `options.setColorType(SvgColorMode.FullColor);` in vóór het opslaan.

**Q: Is het mogelijk om lettertypen in de gegenereerde SVG in te sluiten?**  
A: Aspose.CAD converteert momenteel tekst naar vormen; het insluiten van lettertypen is niet nodig.

**Q: Werkt de bibliotheek op Linux en macOS?**  
A: De Java‑bibliotheek is platform‑onafhankelijk en draait overal waar een compatibele JVM beschikbaar is.

**Q: Welke versie van Aspose.CAD werd gebruikt in deze tutorial?**  
A: Het voorbeeld is getest met Aspose.CAD voor Java 24.10.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Laatst bijgewerkt:** 2026-01-07  
**Getest met:** Aspose.CAD voor Java 24.10  
**Auteur:** Aspose  

---