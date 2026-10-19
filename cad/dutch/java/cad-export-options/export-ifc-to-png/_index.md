---
date: 2026-10-19
description: Leer hoe je PNG-miniatuur‑IFC‑bestanden maakt met Aspose.CAD for Java
  in slechts een paar regels code.
keywords:
- create png thumbnail ifc
- ifc to png conversion
- aspose cad java
- java image processing
- bIM visualization
lastmod: 2026-10-19
linktitle: Exporteren van IFC naar PNG
og_description: Maak PNG-miniatuur‑IFC‑bestanden moeiteloos met Aspose.CAD for Java.
  Deze stapsgewijze gids laat zien hoe je IFC-modellen laadt, rastert en opslaat als
  PNG‑afbeeldingen van hoge kwaliteit.
og_image_alt: Developer guide showing Java code that converts IFC files to PNG thumbnails
  using Aspose.CAD
og_title: Maak een PNG-miniatuur van IFC met Aspose.CAD for Java
schemas:
- author: Aspose
  dateModified: '2026-10-19'
  description: Learn how to create PNG thumbnail IFC files with Aspose.CAD for Java
    in just a few lines of code.
  headline: How to create PNG thumbnail IFC with Aspose.CAD for Java
  type: TechArticle
- description: Learn how to create PNG thumbnail IFC files with Aspose.CAD for Java
    in just a few lines of code.
  name: How to create PNG thumbnail IFC with Aspose.CAD for Java
  steps:
  - name: load the IFC file
    text: First, point to the folder where your IFC file lives and load it with `CadImage.load`.
      `CadImage.load` reads a CAD file and returns an image object that can be rasterized.
      > **Why this matters:** Loading the file as a `CadImage` gives you access to
      vector‑raster conversion options that control resol
  - name: set rasterization options
    text: Define the output dimensions and any other vector‑related settings through
      `VectorRasterizationOptions`. `VectorRasterizationOptions` lets you specify
      output size, background color, and other rasterization parameters. > Adjust
      `PageWidth` and `PageHeight` to control the final PNG resolution, which i
  - name: configure PNG options
    text: Link the rasterization options to the PNG exporter by creating a `PngOptions`
      instance.
  - name: save the image as PNG
    text: Finally, write the rasterized image to disk using the `save` method. `save`
      writes the rasterized image to the specified file path in the chosen format.
      > After this step you have successfully **created a PNG thumbnail IFC** and
      can use the resulting `example.png` anywhere you need a raster image.
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD supports many formats (DWG, DXF, DGN, etc.). Simply change
      the file extension and load the appropriate image class.
    question: Can I use this approach to convert other CAD formats to PNG?
  - answer: DPI is controlled indirectly via `PageWidth`/`PageHeight`. Adjust these
      values relative to the desired physical size to achieve the required DPI.
    question: Does the library let me set a custom DPI?
  - answer: PNG is a lossless format, so the rasterized image retains the full visual
      fidelity of the original vector data.
    question: Is the PNG output loss‑less?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- ifc conversion
- png thumbnail
- aspose.cad
- java image processing
- bim visualization
title: Hoe maak je een PNG-miniatuur van IFC met Aspose.CAD for Java
url: /nl/java/cad-export-options/export-ifc-to-png/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export IFC naar PNG met Aspose.CAD voor Java

## Introductie

In deze tutorial leer je hoe je **PNG‑miniatuur‑IFC**‑bestanden maakt met Aspose.CAD voor Java. Of je nu snelle previews nodig hebt voor een BIM‑portaal, miniaturen wilt genereren voor een documentbeheersysteem, of batch‑conversies wilt automatiseren, de onderstaande stappen laten je een 3‑D‑IFC‑model rasteren naar een scherpe 2‑D‑PNG‑afbeelding in slechts een paar regels Java‑code.

## Snelle antwoorden
- **Welke bibliotheek is vereist?** Aspose.CAD for Java.  
- **Kan ik een PNG‑miniatuur‑IFC maken in een paar regels code?** Ja – de volledige workflow past in minder dan 20 regels.  
- **Heb ik een licentie nodig voor productie?** Een tijdelijke licentie werkt voor testen; een volledige licentie is vereist voor commerciële inzet.  
- **Is de output schaalbaar?** Je kunt elke pixelafmeting instellen, zodat de PNG schaalt naar elke gewenste grootte.  
- **Welke Java‑versie wordt ondersteund?** Java 8 of hoger.

## Wat betekent “convert IFC to PNG”?
Het converteren van IFC (Industry Foundation Classes) naar PNG betekent het rasteren van het 3‑D‑bouwmodel naar een 2‑D‑bitmapafbeelding. Dit proces creëert een visuele miniatuur die kan worden weergegeven in browsers, rapporten of mobiele apps zonder dat een volledige CAD‑viewer nodig is.

## Waarom Aspose.CAD voor Java gebruiken?
Aspose.CAD ondersteunt **meer dan 30 CAD‑ en BIM‑formaten**, waaronder IFC, DWG, DXF en DGN, en kan bestanden tot **2 GB** verwerken zonder het volledige document in het geheugen te laden. De bibliotheek is pure Java, heeft **geen externe afhankelijkheden** en draait op Windows, Linux en macOS, waardoor hij ideaal is voor server‑side afbeeldingengeneratie.  
Hij biedt rasterisatie met hoge prestaties, uitgebreide formatondersteuning en eenvoudige integratie in Java‑applicaties.

## Vereisten

- **Aspose.CAD Library** – download de nieuwste JAR van de [download link](https://releases.aspose.com/cad/java/).  
- **Java Development Kit** – JDK 8 of nieuwer geïnstalleerd op je machine.  
- **IFC‑bronbestand** – plaats het bestand in een map die je vanuit je code kunt refereren.

## Import namespaces

Het `com.aspose.cad`‑pakket levert alle klassen die je nodig hebt. `CadImage` is het toegangspunt voor het laden van CAD‑bestanden, terwijl `PngOptions` de rasterisatie‑instellingen configureert.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## Hoe PNG‑miniatuur‑IFC maken in Java?

Laad het IFC‑bestand, definieer rasterisatie‑opties en sla het resultaat op als een PNG‑afbeelding – dat is de volledige conversieworkflow. De volgende secties splitsen elke stap op, zodat je de fragmenten kunt kopiëren‑plakken in je project en ze direct kunt uitvoeren.

### Stap 1: laad het IFC‑bestand
Eerst, wijs naar de map waarin je IFC‑bestand zich bevindt en laad het met `CadImage.load`.  
`CadImage.load` leest een CAD‑bestand en retourneert een afbeeldingobject dat kan worden gerasterd.

```java
String dataDir = "Your Document Directory" + "ExportingIFC/";
String fileName = dataDir + "example.ifc";
IfcImage cadImage = (IfcImage)Image.load(fileName);
```

> **Waarom dit belangrijk is:** Het laden van het bestand als een `CadImage` geeft je toegang tot vector‑raster‑conversie‑opties die de resolutie, achtergrondkleur en lijndikte regelen.

### Stap 2: stel rasterisatie‑opties in
Definieer de uitvoerafmetingen en andere vector‑gerelateerde instellingen via `VectorRasterizationOptions`.  
`VectorRasterizationOptions` stelt je in staat de uitvoergrootte, achtergrondkleur en andere rasterisatie‑parameters op te geven.

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

> Pas `PageWidth` en `PageHeight` aan om de uiteindelijke PNG‑resolutie te regelen, wat essentieel is wanneer je **PNG‑java**‑bestanden opslaat voor afdrukken van hoge kwaliteit of web‑miniaturen.

### Stap 3: configureer PNG‑opties
Koppel de rasterisatie‑opties aan de PNG‑exporteur door een `PngOptions`‑instance te maken.

```java
PngOptions pngOptions = new PngOptions();
pngOptions.setVectorRasterizationOptions(vectorOptions);
```

### Stap 4: sla de afbeelding op als PNG
Schrijf tenslotte de gerasterde afbeelding naar schijf met de `save`‑methode.  
`save` schrijft de gerasterde afbeelding naar het opgegeven bestandspad in het gekozen formaat.

```java
String outPath = dataDir + "example.png";
cadImage.save(outPath, pngOptions);
```

> Na deze stap heb je succesvol een **PNG‑miniatuur‑IFC** gemaakt en kun je de resulterende `example.png` overal gebruiken waar je een rasterafbeelding nodig hebt.

## Veelvoorkomende gebruikssituaties
- **Miniaturen genereren** voor BIM‑modellen in webportalen.  
- **Vloerplan‑snapshots insluiten** in PDF‑ of Word‑rapporten.  
- **Geautomatiseerde batch‑conversie** van grote IFC‑bibliotheken voor archiverings‑ of migratieprojecten.

## Problemen oplossen & tips
- **Geheugenproblemen:** Voor zeer grote IFC‑bestanden, vergroot de JVM‑heap (`-Xmx2g` of hoger).  
- **Ontbrekende textures:** Zorg ervoor dat de externe bronnen van het IFC‑bestand bereikbaar zijn vanuit de `dataDir`.  
- **Pro‑tip:** Gebruik `vectorOptions.setBackgroundColor(Color.getWhite())` als je een witte achtergrond wilt in plaats van de standaard transparante PNG.

## Veelgestelde vragen

### Q1: Is Aspose.CAD compatibel met alle versies van IFC‑bestanden?
A1: Aspose.CAD ondersteunt verschillende IFC‑versies. Raadpleeg de [documentatie](https://reference.aspose.com/cad/java/) voor gedetailleerde compatibiliteitsinformatie.

### Q2: Kan ik de rasterisatie‑opties verder aanpassen?
A2: Zeker! Bekijk de [documentatie](https://reference.aspose.com/cad/java/) voor geavanceerde instellingen zoals DPI‑controle, anti‑aliasing en lijndikte.

### Q3: Is er een proefversie beschikbaar?
A3: Ja, je kunt de gratis proefversie downloaden via de [Aspose.CAD free trial](https://releases.aspose.com/).

### Q4: Hoe kan ik een tijdelijke licentie voor testen verkrijgen?
A4: Verkrijg een tijdelijke licentie via de [Aspose.CAD temporary license page](https://purchase.aspose.com/temporary-license/).

### Q5: Waar kan ik vragen stellen of problemen melden?
A5: Word lid van de community op het [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) voor ondersteuning van zowel Aspose‑engineers als mede‑ontwikkelaars.

## Veelgestelde vragen

**Q: Kan ik deze aanpak gebruiken om andere CAD‑formaten naar PNG te converteren?**  
A: Ja, Aspose.CAD ondersteunt veel formaten (DWG, DXF, DGN, enz.). Verander simpelweg de bestandsextensie en laad de juiste image‑klasse.

**Q: Laat de bibliotheek me een aangepaste DPI instellen?**  
A: DPI wordt indirect geregeld via `PageWidth`/`PageHeight`. Pas deze waarden aan ten opzichte van de gewenste fysieke grootte om de vereiste DPI te bereiken.

**Q: Is de PNG‑output verliesvrij?**  
A: PNG is een verliesvrij formaat, dus de gerasterde afbeelding behoudt de volledige visuele getrouwheid van de oorspronkelijke vectorgegevens.

## Conclusie

Je hebt nu een volledige, productie‑klare methode om **PNG‑miniatuur‑IFC**‑bestanden te maken met Aspose.CAD voor Java. Integreer deze stappen in desktop‑tools, server‑side services of cloud‑functies om BIM‑visualisatie‑pijplijnen te automatiseren en snelle, hoogwaardige miniaturen aan eindgebruikers te leveren.

---

**Last Updated:** 2026-10-19  
**Tested With:** Aspose.CAD for Java 24.11  
**Author:** Aspose

## Gerelateerde tutorials

- [Hoe STL naar PNG te converteren met Aspose.CAD voor Java](/cad/java/cad-export-options/export-stl-to-png/)
- [DWG naar PNG converteren – CAD opslaan als PNG met Aspose.CAD voor Java](/cad/java/cad-drawing-conversion/convert-cad-drawing-to-raster-image/)
- [DWG naar PDF exporteren in Java – PDF-paginaformaat instellen met Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}