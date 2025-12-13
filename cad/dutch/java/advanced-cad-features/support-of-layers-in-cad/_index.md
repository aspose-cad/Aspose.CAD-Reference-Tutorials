---
date: 2025-12-13
description: Leer hoe je CAD als JPEG opslaat in Java met Aspose.CAD, meerdere lagen
  toevoegt en CAD-afmetingen aanpast voor een nauwkeurige afbeeldingconversie.
linktitle: Support of Layers in CAD
second_title: Aspose.CAD Java API
title: CAD opslaan als JPEG met ondersteuning voor lagen in Java
url: /nl/java/advanced-cad-features/support-of-layers-in-cad/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD opslaan als JPEG met laagondersteuning in Java

## Introductie

In deze tutorial ontdek je hoe je **CAD als JPEG kunt opslaan** terwijl je volledig gebruik maakt van laagondersteuning in Aspose.CAD voor Java. Lagen stellen je in staat specifieke delen van een tekening te isoleren, waardoor je gemakkelijk alleen kunt exporteren wat je nodig hebt. We lopen elke stap door, van het opzetten van de omgeving tot het exporteren van een JPEG die alleen de door jou gekozen lagen bevat.

## Snelle antwoorden
- **Wat betekent “CAD opslaan als JPEG”?** Het converteert een CAD-tekening naar een raster JPEG‑afbeelding.
- **Kan ik alleen geselecteerde lagen opnemen?** Ja – gebruik de `setLayers`‑methode om op te geven welke lagen gerenderd moeten worden.
- **Hoe wijzig ik de afbeeldingsgrootte?** Pas `setPageWidth` en `setPageHeight` aan in `CadRasterizationOptions`.
- **Is dit een oplossing alleen voor Java?** Het voorbeeld gebruikt Aspose.CAD voor Java, maar dezelfde concepten zijn toepasbaar op andere talen.
- **Heb ik een licentie nodig?** Een gratis proefversie werkt voor testen; een commerciële licentie is vereist voor productie.

## Vereisten

Voordat je begint, zorg ervoor dat je het volgende hebt:

1. **Aspose.CAD for Java Library** – download deze van de [website](https://releases.aspose.com/cad/java/). Volg de installatiehandleiding om de JAR‑bestanden aan de classpath van je project toe te voegen.  
2. **Java Development Environment** – een recente JDK (8 of hoger) geïnstalleerd op je machine.

Nu we klaar zijn, laten we de code verkennen die nodig is om **CAD als JPEG op te slaan** met selectieve laagrendering.

## Namespaces importeren

Begin met het importeren van de vereiste Aspose.CAD‑klassen en standaard Java‑hulpmiddelen:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;
```

## Stapsgewijze gids

### Stap 1: Bestands‑paden instellen

Definieer waar het bron‑DWF‑bestand zich bevindt en waar de uitvoer‑JPEG moet worden weggeschreven.

```java
String dataDir = "Your Document Directory" + "DWFDrawings/";
String srcFile = dataDir + "for_layers_test.dwf";
String outFile = dataDir + "for_layers_test.jpg";
```

### Stap 2: Laad de DWF‑afbeelding

Gebruik de `Image.load`‑methode van Aspose.CAD om de CAD‑tekening te lezen.

```java
Image image = Image.load(srcFile);
```

### Stap 3: Rasterisatie‑opties configureren (CAD‑afmetingen aanpassen)

Maak een `CadRasterizationOptions`‑instantie aan en stel de gewenste uitvoergrootte in. Het wijzigen van deze waarden stelt je in staat om **CAD‑afmetingen aan te passen** voor de uiteindelijke JPEG.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

### Stap 4: Lagen specificeren (Meerdere lagen toevoegen)

Als je meer dan één laag wilt renderen, voeg dan eenvoudig hun namen toe aan de lijst. Hier beginnen we met een enkele laag genaamd “LayerA”.

```java
List<String> stringList = new ArrayList<>(Arrays.asList("LayerA"));
rasterizationOptions.setLayers(stringList);
```

*Pro tip:* Om **meerdere lagen toe te voegen**, breid je de `Arrays.asList`‑aanroep uit, bijv. `Arrays.asList("LayerA", "LayerB", "LayerC")`.

### Stap 5: JPEG‑opties configureren (Java CAD‑afbeelding converteren)

Koppel de rasterisatie‑instellingen aan het JPEG‑uitvoerformaat.

```java
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Stap 6: Exporteren naar JPG (CAD opslaan als JPEG)

Schrijf tenslotte de afbeelding naar schijf. Deze stap **slaat de CAD‑tekening op als een JPEG**‑bestand dat alleen de geselecteerde lagen bevat.

```java
image.save(outFile, jpegOptions);
```

Door deze stappen te volgen heb je met succes **CAD als JPEG opgeslagen** terwijl je controle hebt over welke lagen verschijnen en de afbeeldingsafmetingen hebt aangepast.

## Veelvoorkomende problemen en oplossingen

| Probleem | Oplossing |
|----------|-----------|
| **Layers not appearing** | Controleer of de laagnamen exact overeenkomen met wat er in het DWF‑bestand is opgeslagen (hoofdlettergevoelig). |
| **Output image is blank** | Zorg ervoor dat `setPageWidth` en `setPageHeight` groot genoeg zijn voor de omvang van de tekening. |
| **License exception** | Gebruik een proeflicentie voor testen; verkrijg een volledige licentie voor productieomgevingen. |

## Veelgestelde vragen

**Q: Kan ik meerdere lagen toevoegen aan de rasterisatie‑opties?**  
A: Zeker. Breid de `stringList` uit met extra laagnamen, bijv. `Arrays.asList("LayerA", "LayerB")`.

**Q: Is Aspose.CAD compatibel met andere CAD‑formaten?**  
A: Ja, het ondersteunt DWG, DXF, DWF en nog veel meer formaten.

**Q: Hoe kan ik de afbeeldingsafmetingen van de output wijzigen?**  
A: Pas `setPageWidth` en `setPageHeight` aan in de `CadRasterizationOptions`‑instantie.

**Q: Waar kan ik een licentie voor Aspose.CAD aanschaffen?**  
A: Je kunt de licentie‑opties bekijken [hier](https://purchase.aspose.com/buy).

**Q: Waar kan ik community‑ondersteuning krijgen?**  
A: Word lid van de Aspose.CAD‑community op het [forum](https://forum.aspose.com/c/cad/19) voor hulp en discussies.

**Laatst bijgewerkt:** 2025-12-13  
**Getest met:** Aspose.CAD for Java 24.11  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}