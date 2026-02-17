---
date: 2026-02-17
description: Leer hoe je DWG als JPEG opslaat in Java met Aspose.CAD, meerdere lagen
  toevoegt en CAD-afmetingen aanpast voor een nauwkeurige afbeeldingconversie.
linktitle: Support of Layers in CAD
second_title: Aspose.CAD Java API
title: DWG opslaan als JPEG met laagondersteuning in Java
url: /nl/java/advanced-cad-features/support-of-layers-in-cad/
weight: 18
---

}}

Make sure to keep all shortcodes unchanged.

Now produce final content.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG opslaan als JPEG met laagondersteuning in Java

## Introductie

## Snelle antwoorden
- **Wat betekent “save DWG as JPEG”?** Het converteert een DWG (of andere CAD) tekening naar een raster JPEG‑afbeelding.  
- **Kan ik alleen geselecteerde lagen opnemen?** Ja – gebruik de `setLayers`‑methode om op te geven welke lagen gerenderd moeten worden.  
- **Hoe wijzig ik de afbeeldingsgrootte?** Pas `setPageWidth` en `setPageHeight` aan in `CadRasterizationOptions`.  
- **Is dit een alleen‑Java‑oplossing?** Het voorbeeld gebruikt Aspose.CAD voor Java, maar dezelfde concepten zijn van toepassing op andere talen.  
- **Heb ik een licentie nodig?** Een gratis proefversie werkt voor testen; een commerciële licentie is vereist voor productie.

## Wat is “save DWG as JPEG”?
DWG opslaan als JPEG betekent het rasteren van een vector‑gebaseerd CAD‑bestand (DWG, DWF, DXF, enz.) naar een standaard JPEG‑bitmap. Dit is handig wanneer je CAD‑tekeningen moet insluiten in webpagina’s, e‑mails of rapporten die alleen rasterafbeeldingen ondersteunen.

## Waarom een laag‑bewuste JPEG‑conversie gebruiken?
- **Focus op relevante gegevens:** Exporteer alleen de lagen die je nodig hebt, waardoor de bestandsgrootte en visuele rommel worden verminderd.  
- **Behoud ontwerpintentie:** Lagen behouden de logische groepering van objecten, zodat je hetzelfde bronbestand voor verschillende uitvoer kunt hergebruiken.  
- **Volledige controle over afmetingen:** Door rasterisatie‑opties aan te passen kun je high‑resolution afbeeldingen produceren die voldoen aan je publicatie‑eisen.

## Voorvereisten

Voordat je begint, zorg ervoor dat je het volgende hebt:

1. **Aspose.CAD for Java Library** – download deze van de [website](https://releases.aspose.com/cad/java/). Volg de installatiehandleiding om de JAR‑bestanden aan de classpath van je project toe te voegen.  
2. **Java Development Environment** – een recente JDK (8 of hoger) geïnstalleerd op je machine.

Nu we klaar zijn, laten we de code verkennen die nodig is om **DWG opslaan als JPEG** met selectieve laagrendering.

## Importeer namespaces

Begin met het importeren van de benodigde Aspose.CAD‑klassen en standaard Java‑hulpmiddelen:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;
```

## Stapsgewijze handleiding

### Stap 1: Stel bestands‑paden in

Definieer waar het bron‑DWF‑bestand zich bevindt en waar de uitvoer‑JPEG wordt weggeschreven.

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

### Stap 3: Configureer rasterisatie‑opties (pas CAD‑afmetingen aan)

Maak een `CadRasterizationOptions`‑instantie aan en stel de gewenste uitvoergrootte in. Het wijzigen van deze waarden stelt je in staat om **CAD‑afmetingen** voor de uiteindelijke JPEG aan te passen.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

### Stap 4: Specificeer lagen (voeg meerdere lagen toe)

Als je meer dan één laag wilt renderen, voeg dan eenvoudig hun namen toe aan de lijst. Hier beginnen we met een enkele laag genaamd “LayerA”.

```java
List<String> stringList = new ArrayList<>(Arrays.asList("LayerA"));
rasterizationOptions.setLayers(stringList);
```

*Pro tip:* Om **meerdere lagen toe te voegen**, breid je de `Arrays.asList`‑aanroep uit, bijv. `Arrays.asList("LayerA", "LayerB", "LayerC")`. Hiermee kun je **specifieke CAD‑lagen** voor de conversie selecteren.

### Stap 5: Configureer JPEG‑opties (Java converteert CAD‑afbeelding)

Koppel de rasterisatie‑instellingen aan het JPEG‑uitvoerformaat.

```java
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Stap 6: Exporteer naar JPG (DWG opslaan als JPEG)

Schrijf tenslotte de afbeelding naar de schijf. Deze stap **slaat de CAD‑tekening op als een JPEG**‑bestand dat alleen de geselecteerde lagen bevat.

```java
image.save(outFile, jpegOptions);
```

Door deze stappen te volgen heb je met succes **DWG opgeslagen als JPEG** terwijl je controle hebt over welke lagen verschijnen en de afbeeldingsafmetingen hebt aangepast.

## Hoe DWF naar JPEG converteren met laagselectie

Hoewel het voorbeeld een DWF‑bron gebruikt, werkt dezelfde rasterisatie‑pipeline voor elk ondersteund CAD‑formaat (DWG, DXF, DGN, enz.). Verander eenvoudig de bestandsextensie in `srcFile` en de bibliotheek zal de **conversie van DWF naar JPEG** (of een ander formaat) automatisch afhandelen.

## Veelvoorkomende problemen en oplossingen

| Probleem | Oplossing |
|----------|-----------|
| **Layers not appearing** | Controleer of de laagnamen exact overeenkomen met wat in het DWF‑bestand is opgeslagen (hoofdlettergevoelig). |
| **Output image is blank** | Zorg ervoor dat `setPageWidth` en `setPageHeight` groot genoeg zijn voor de omvang van de tekening. |
| **License exception** | Gebruik een proeflicentie voor testen; verkrijg een volledige licentie voor productie‑omgevingen. |

## Veelgestelde vragen

**V: Kan ik meerdere lagen toevoegen aan de rasterisatie‑opties?**  
A: Absoluut. Breid de `stringList` uit met extra laagnamen, bijv. `Arrays.asList("LayerA", "LayerB")`.

**V: Is Aspose.CAD compatibel met andere CAD‑formaten?**  
A: Ja, het ondersteunt DWG, DXF, DWF en nog veel meer formaten.

**V: Hoe kan ik de afmetingen van de uitvoerafbeelding wijzigen?**  
A: Pas `setPageWidth` en `setPageHeight` aan in de `CadRasterizationOptions`‑instantie.

**V: Waar kan ik een licentie voor Aspose.CAD aanschaffen?**  
A: Je kunt de licentie‑opties bekijken [hier](https://purchase.aspose.com/buy).

**V: Waar kan ik community‑ondersteuning krijgen?**  
A: Word lid van de Aspose.CAD‑community op het [forum](https://forum.aspose.com/c/cad/19) voor hulp en discussies.

---

**Laatst bijgewerkt:** 2026-02-17  
**Getest met:** Aspose.CAD for Java 24.11  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}