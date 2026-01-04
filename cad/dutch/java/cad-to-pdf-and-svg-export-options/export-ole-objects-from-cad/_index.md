---
date: 2026-01-04
description: Leer hoe je **CAD opslaan als PNG** en moeiteloos OLE‑objecten uit CAD‑bestanden
  kunt exporteren met Aspose.CAD voor Java. Snelle installatie, volledig codevoorbeeld
  en best‑practice‑tips.
linktitle: Export OLE Objects from CAD
second_title: Aspose.CAD Java API
title: CAD opslaan als PNG en OLE‑objecten exporteren met Aspose.CAD voor Java
url: /nl/java/cad-to-pdf-and-svg-export-options/export-ole-objects-from-cad/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD opslaan als PNG en OLE-objecten exporteren met Aspose.CAD voor Java

## Introduction

In de snelbewegende wereld van Computer‑Aided Design (CAD) kan het **opslaan van CAD als PNG** terwijl je ingebedde OLE (Object Linking and Embedding) objecten extraheert, je workflow dramatisch stroomlijnen. Of je nu een batch‑conversietool bouwt, thumbnails genereert voor een webportaal, of simpelweg OLE‑inhoud wilt archiveren, Aspose.CAD voor Java biedt een schone, programmeerbare manier om dit te doen. In deze tutorial lopen we het volledige proces door, van het opzetten van je project tot het exporteren van elk OLE‑object als een PNG‑afbeelding.

## Quick Answers
- **Kan ik OLE-objecten direct naar PNG exporteren?** Ja – Aspose.CAD laadt het CAD‑bestand en laat je elke layout rasteren naar PNG.  
- **Welke Java‑versie is vereist?** Java 8 of hoger.  
- **Heb ik een licentie nodig voor deze functie?** Een gratis proefversie werkt voor evaluatie; een licentie is vereist voor productie.  
- **Wordt vector‑data behouden?** De PNG‑rasterisatie behoudt de visuele nauwkeurigheid, maar de output is raster, niet vector.  
- **Wordt batchverwerking ondersteund?** Absoluut – itereren over een array van bestanden zoals getoond in het code‑voorbeeld.

## Prerequisites

Zorg er vóór je begint voor dat je het volgende hebt:

- **Java Development Kit (JDK)** – Java 8+ geïnstalleerd en geconfigureerd.  
- **Aspose.CAD for Java** – Download de nieuwste bibliotheek via de [download link](https://releases.aspose.com/cad/java/).  
- **CAD‑bronbestanden** – Alle DWG/DXF/DGN‑bestanden die OLE‑objecten bevatten die je wilt exporteren.

## Import Namespaces

Om met CAD‑bestanden te werken moet je de kern‑klassen van Aspose.CAD importeren. Houd het import‑blok precies zoals weergegeven – het levert de klassen die later in de tutorial worden gebruikt.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## How to Save CAD as PNG

Hieronder vind je een beknopte, stapsgewijze handleiding die **laat zien hoe je OLE‑objecten exporteert en CAD opslaat als PNG**. Elke stap bevat een korte uitleg gevolgd door de exacte code die je in je project moet kopiëren.

### Step 1: Set Your Document Directory

Definieer de map die je CAD‑tekeningen bevat. Vervang de placeholder door het werkelijke pad op je machine.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

### Step 2: Define CAD File Names

Som elk CAD‑bestand op dat je wilt verwerken. Je kunt zoveel items toevoegen als nodig.

```java
String[] files = new String[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

### Step 3: Set PNG Export Options

Configureer de rasterisatie‑instellingen. Hier richten we ons op een specifieke layout (`Layout1`) en gebruiken we de standaard PNG‑opties.

```java
PngOptions pngOptions = new PngOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.setLayouts(new String[] { "Layout1" });
```

### Step 4: Iterate Through CAD Files and Save as PNG

Laad elk CAD‑bestand, rasteriseer de OLE‑objecten en schrijf het PNG‑outputbestand weg. Het `_out.png`‑achtervoegsel helpt je de gegenereerde afbeeldingen te identificeren.

```java
for(String file : files)
{
    CadImage cadImage = (CadImage)Image.load(dataDir + file);
    cadImage.save(dataDir + file + "_out.png", pngOptions);
}
```

## Common Issues and Solutions

| Probleem | Waarom het gebeurt | Oplossing |
|----------|--------------------|----------|
| **`Image.load` throws `FileNotFoundException`** | Het `dataDir`‑pad is onjuist of de bestandsnaam bevat een typefout. | Controleer de directory‑string opnieuw en zorg ervoor dat de bestandsnamen exact overeenkomen, inclusief spaties. |
| **Output PNG is blank** | De layout‑naam bestaat niet in het bron‑CAD‑bestand. | Gebruik `cadImage.getLayouts()` om beschikbare layouts weer te geven, en werk vervolgens `rasterizationOptions.setLayouts(...)` bij. |
| **Large CAD files cause OutOfMemoryError** | Het rasteriseren van hoge‑resolutie‑afbeeldingen verbruikt veel heap‑geheugen. | Verhoog de JVM‑heap (`-Xmx2g`) of verlaag de rasterisatie‑resolutie via `rasterizationOptions.setResolution(...)`. |

## FAQ's

### Q1: Is Aspose.CAD compatible with all CAD file formats?

A1: Aspose.CAD ondersteunt verschillende CAD‑formaten, waaronder DWG, DXF en DGN. Zie de [documentatie](https://reference.aspose.com/cad/java/) voor de volledige lijst.

### Q2: Can I customize the export settings for OLE objects?

A2: Ja, Aspose.CAD biedt uitgebreide opties om exportinstellingen aan te passen, zodat je de output kunt afstemmen op je specifieke eisen.

### Q3: Is there a free trial available for Aspose.CAD?

A3: Ja, je kunt de mogelijkheden van Aspose.CAD verkennen door een gratis proefversie te verkrijgen via [hier](https://releases.aspose.com/).

### Q4: Where can I get community support for Aspose.CAD?

A4: Word lid van de Aspose.CAD‑community op het [forum](https://forum.aspose.com/c/cad/19) om hulp te zoeken en je ervaringen te delen.

### Q5: How can I purchase a license for Aspose.CAD?

A5: Bezoek de [aankooppagina](https://purchase.aspose.com/buy) om een licentie te verkrijgen die past bij jouw ontwikkelbehoeften.

## Conclusion

Door deze vijf eenvoudige stappen te volgen kun je **CAD opslaan als PNG** en elk ingebed OLE‑object extraheren met slechts een paar regels Java‑code. Deze aanpak is ideaal voor batch‑conversies, geautomatiseerde rapportage, of elke situatie waarin je raster‑afbeeldingen van CAD‑inhoud nodig hebt zonder handmatig te exporteren. Voel je vrij om te experimenteren met verschillende rasterisatie‑opties om aan je kwaliteit‑ en prestatie‑eisen te voldoen.

---

**Laatst bijgewerkt:** 2026-01-04  
**Getest met:** Aspose.CAD for Java 24.12 (latest op het moment van schrijven)  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}