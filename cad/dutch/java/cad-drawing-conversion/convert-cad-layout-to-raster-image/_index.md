---
date: 2026-10-04
description: Leer hoe u snel dwg naar png kunt converteren en CAD kunt exporteren
  als png of andere rasterformaten met Aspose.CAD for Java. Verkrijg snel resultaten
  van hoge kwaliteit.
keywords:
- convert dwg to png
- dwg to raster image
- convert cad to pdf
- export cad as png
- convert dwg to jpeg
lastmod: 2026-10-04
linktitle: CAD-indeling naar rasterafbeeldingsformaat converteren
og_description: Converteer DWG snel naar PNG met Aspose.CAD for Java. Leer stap voor
  stap hoe u CAD exporteert als PNG, JPEG, TIFF en meer.
og_image_alt: 'Developer guide: Convert DWG to PNG and other raster formats using
  Aspose.CAD for Java'
og_title: DWG naar PNG en andere rasterformaten converteren met Aspose.CAD for Java
schemas:
- author: Aspose
  dateModified: '2026-10-04'
  description: Learn how to quickly convert dwg to png and export cad as png or other
    raster formats using Aspose.CAD for Java. Get high‑quality results fast.
  headline: Convert DWG to PNG and other raster formats using Aspose.CAD for Java
  type: TechArticle
- description: Learn how to quickly convert dwg to png and export cad as png or other
    raster formats using Aspose.CAD for Java. Get high‑quality results fast.
  name: Convert DWG to PNG and other raster formats using Aspose.CAD for Java
  steps:
  - name: set up the resource directory
    text: Replace `"Your Document Directory"` with the absolute path where your CAD
      files reside. This directory will be used for both input and output files.
  - name: load the CAD file
    text: '`Image.load` parses the source file and creates an in‑memory representation
      that you can rasterize. You can load any supported format (DWG, DXF, DGN, etc.)
      – this is the **how to convert cad** part.'
  - name: configure rasterization options
    text: '`CadRasterizationOptions` defines how the vector data is turned into pixels.
      `setPageWidth` and `setPageHeight` control output resolution (larger values
      = higher DPI). `setLayouts` lets you **convert CAD to raster** for specific
      layouts; omit it to rasterize the whole drawing.'
  - name: set image options
    text: '`TiffOptions` (or `PngOptions` for PNG) tells Aspose which raster format
      to generate and lets you fine‑tune compression, color depth, and other format‑specific
      settings. Choose the options class that matches your desired output.'
  - name: save the resultant image
    text: Call `save` on the `Image` instance, passing the output file name and the
      options object. Change the file extension to `.png` (and use `PngOptions`) to
      **save CAD as PNG**. The same pattern works for JPEG, BMP, or PDF. > **Common
      pitfall:** Forgetting to match the file extension with the options cla
  type: HowTo
- questions:
  - answer: Yes, it supports over 30 CAD and raster formats, including DWG, DXF, DGN,
      and SVG.
    question: Is Aspose.CAD compatible with different CAD file formats?
  - answer: Absolutely. Adjust `setPageWidth`, `setPageHeight`, or `setResolution`
      in `CadRasterizationOptions` to achieve the desired DPI.
    question: Can I customize the resolution of the output raster image?
  - answer: Provide an array with all layout names to `setLayouts`, e.g., `new String[]{"Model","Layout1","Layout2"}`.
    question: How can I convert multiple CAD layouts in a single run?
  - answer: Yes—PNG, JPEG, BMP, PDF, and more are available via their respective `*Options`
      classes.
    question: Are there output formats besides TIFF supported?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community
      support and official assistance.
    question: Where can I get help or share my experience with Aspose.CAD?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- convert dwg
- Aspose.CAD
- Java raster conversion
- CAD image processing
title: DWG naar PNG en andere rasterformaten converteren met Aspose.CAD for Java
url: /nl/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Converteer DWG naar PNG en andere rasterformaten met Aspose.CAD voor Java

## Introductie

`Aspose.CAD for Java` is een bibliotheek die programmatische conversie van CAD‑bestanden naar rasterafbeeldingen zoals PNG, JPEG en TIFF mogelijk maakt. Het converteren van DWG naar PNG (of andere raster‑image‑formaten) is een veelvoorkomende eis wanneer je CAD‑tekeningen moet delen met teamleden die geen CAD‑viewer hebben, ontwerpen moet insluiten in documentatie, of miniaturen moet genereren voor webgalerijen. In deze gids leer je hoe je dwg naar png snel en betrouwbaar kunt converteren, of je nu werkt met een volledig tekenbestand of slechts een specifieke layout. Je hebt mogelijk ook **CAD naar raster** nodig voor web‑previews, rapportagetools of mobiele apps.

## Snelle antwoorden
- **Welke bibliotheek verwerkt DWG naar PNG?** Aspose.CAD for Java levert de conversie‑engine.  
- **Welke rasterformaten kan ik exporteren?** PNG, JPEG, TIFF, PDF, BMP en meer dan 30 extra formaten.  
- **Heb ik een licentie nodig voor testen?** Een gratis proefversie werkt voor ontwikkeling; een commerciële licentie is vereist voor productie.  
- **Kan ik een specifieke layout kiezen?** Ja – gebruik `setLayouts` om “Model”, “Layout1”, enz. te targeten.  
- **Is output met hoge resolutie mogelijk?** Absoluut – pas `setPageWidth` en `setPageHeight` (of `setResolution`) aan om DPI te regelen.

## Wat is “convert dwg to png”?

Convert dwg to png betekent het omzetten van een DWG‑vectortekening naar een pixel‑gebaseerde PNG‑afbeelding die door elke standaard afbeeldingsviewer kan worden weergegeven. Dit proces rasteriseert vector‑entiteiten, behoudt lijndikte, kleuren en lagen, en zet ze om in een bitmap met vaste resolutie. Het resultaat is ideaal om in te sluiten in PDF‑bestanden, Word‑documenten of webpagina's waar vectorondersteuning beperkt is.

## Waarom CAD exporteren als PNG (of andere rasterformaten)?

Het exporteren van CAD als PNG biedt universele compatibiliteit, snelle laadtijden en eenvoudige integratie op alle belangrijke platforms. Rasterafbeeldingen laden direct in vergelijking met het openen van een zwaar DWG‑bestand, en de verliesloze compressie van PNG zorgt voor visuele getrouwheid. Door resolutie, achtergrondkleur en layout te beheersen, garandeer je dat elke belanghebbende dezelfde weergave ziet, ongeacht of het bestand wordt bekeken op een desktop, mobiel apparaat of in een browser.

## Veelvoorkomende gebruikssituaties

| Scenario | Waarom rasteroutput helpt |
|----------|----------------------------|
| **Projectdocumentatie** | PNG's insluiten in PDF's of Word‑documenten voorkomt dat reviewers CAD‑software nodig hebben. |
| **Webportalen** | Miniaturen gegenereerd uit DWG‑bestanden laden direct en verbeteren de gebruikerservaring. |
| **Mobiele apps** | Rasterafbeeldingen worden correct weergegeven op apparaten zonder CAD‑viewers. |
| **Geautomatiseerde rapportage** | Batch‑conversie van meerdere layouts naar PNG/JPEG voor opname in grafieken of dashboards. |

## Voorvereisten

Voordat je begint, zorg dat je het volgende hebt:

1. **Java‑ontwikkelomgeving** – JDK 8 of nieuwer geïnstalleerd en geconfigureerd.  
2. **Aspose.CAD for Java** – Download de nieuwste JAR van de [Aspose.CAD for Java documentation](https://reference.aspose.com/cad/java/).  

## Namespaces importeren

`com.aspose.cad.Image` is de kernklasse die elk CAD‑bestand in het geheugen vertegenwoordigt. `com.aspose.cad.imageoptions.*` levert optie‑objecten voor elk rasterformaat. Importeer de klassen die je nodig hebt om een tekening te laden, rasterisatie te configureren en de output op te slaan.

> **Pro tip:** Als je van plan bent **CAD als PNG te exporteren** in plaats van TIFF, vervang dan `TiffOptions` door `PngOptions` (gevonden in `com.aspose.cad.imageoptions.PngOptions`).

## Stapsgewijze handleiding

### Stap 1: stel de resource‑directory in

Vervang `"Your Document Directory"` door het absolute pad waar je CAD‑bestanden zich bevinden. Deze directory wordt gebruikt voor zowel invoer‑ als uitvoerbestanden.

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

### Stap 2: laad het CAD‑bestand

`Image.load` parseert het bronbestand en maakt een in‑memory representatie die je kunt rasteriseren. Je kunt elk ondersteund formaat laden (DWG, DXF, DGN, enz.) – dit is het **hoe je CAD converteert** gedeelte.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";
```

### Stap 3: configureer rasterisatie‑opties

`CadRasterizationOptions` definieert hoe de vectordata wordt omgezet in pixels. `setPageWidth` en `setPageHeight` regelen de output‑resolutie (grotere waarden = hogere DPI). `setLayouts` stelt je in staat **CAD naar raster** te converteren voor specifieke layouts; laat het weg om de volledige tekening te rasteriseren.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### Stap 4: stel afbeeldingsopties in

`TiffOptions` (of `PngOptions` voor PNG) geeft Aspose aan welk rasterformaat moet worden gegenereerd en laat je compressie, kleurdiepte en andere formatspecifieke instellingen fijn afstemmen. Kies de opties‑klasse die overeenkomt met je gewenste output.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
rasterizationOptions.setLayouts(new String[] {"Model", "Layout1"});
```

### Stap 5: sla de resulterende afbeelding op

Roep `save` aan op de `Image`‑instantie, waarbij je de bestandsnaam voor de output en het opties‑object doorgeeft. Verander de bestandsextensie naar `.png` (en gebruik `PngOptions`) om **CAD als PNG op te slaan**. Hetzelfde patroon werkt voor JPEG, BMP of PDF.

```java
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.setVectorRasterizationOptions(rasterizationOptions);
```

> **Veelvoorkomende valkuil:** Het vergeten af te stemmen van de bestandsextensie op de opties‑klasse veroorzaakt een `UnsupportedFormatException`. Houd ze altijd synchroon.

## Veelvoorkomende problemen en oplossingen

| Probleem | Oplossing |
|----------|-----------|
| **Lege uitvoerafbeelding** | Controleer of de layoutnamen in `setLayouts` exact overeenkomen met die in het bron‑CAD‑bestand. |
| **Lage‑resolutie PNG** | Verhoog `setPageWidth` / `setPageHeight` of stel `setResolution` in op de rasterisatie‑opties. |
| **Niet‑ondersteunde DWG‑versie** | Zorg ervoor dat je de nieuwste Aspose.CAD‑versie gebruikt; oudere releases ondersteunen mogelijk geen nieuwere DWG‑versies. |
| **Geheugenfouten bij grote bestanden** | Verwerk pagina's één voor één of vergroot de JVM‑heap (`-Xmx2g`). |

## Veelgestelde vragen

**V: Is Aspose.CAD compatibel met verschillende CAD‑bestandformaten?**  
A: Ja, het ondersteunt meer dan 30 CAD‑ en rasterformaten, waaronder DWG, DXF, DGN en SVG.

**V: Kan ik de resolutie van de uitvoer‑rasterafbeelding aanpassen?**  
A: Absoluut. Pas `setPageWidth`, `setPageHeight` of `setResolution` in `CadRasterizationOptions` aan om de gewenste DPI te bereiken.

**V: Hoe kan ik meerdere CAD‑layouts in één run converteren?**  
A: Geef een array met alle layoutnamen door aan `setLayouts`, bv. `new String[]{"Model","Layout1","Layout2"}`.

**V: Zijn er naast TIFF nog andere ondersteunde uitvoerformaten?**  
A: Ja—PNG, JPEG, BMP, PDF en meer zijn beschikbaar via hun respectieve `*Options`‑klassen.

**V: Waar kan ik hulp krijgen of mijn ervaring delen met Aspose.CAD?**  
A: Bezoek het [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) voor community‑ondersteuning en officiële assistentie.

## Conclusie

Door deze stappen te volgen kun je **DWG naar PNG converteren**, **CAD als PNG exporteren**, **CAD als JPEG opslaan**, of elk ander rasterformaat genereren dat je nodig hebt. Aspose.CAD voor Java doet het zware werk, zodat je je kunt richten op het integreren van hoogwaardige afbeeldingen in je applicaties, documentatie of webportalen. De ondersteuning van de bibliotheek voor meer dan 30 formaten en het vermogen om tekeningen met honderden pagina's te renderen zonder het volledige bestand in het geheugen te laden, maken het een robuuste keuze voor CAD‑rasterisatie op ondernemingsniveau.

---

**Laatst bijgewerkt:** 2026-10-04  
**Getest met:** Aspose.CAD for Java 24.12  
**Auteur:** Aspose  







```java
image.save(dataDir + "conic_pyramid_layoutstorasterimage_out_.tiff", options);
```

```bash
java -jar aspose-cad.jar -i input.dwg -o output.png -w 1200 -h 1200
```

## Gerelateerde tutorials

- [Snel DWG exporteren naar PDF of raster met java cad bibliotheek Aspose.CAD voor Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [DWG converteren naar BMP met Aspose.CAD voor Java](/cad/java/cad-export-options/export-to-bmp/)
- [DWG exporteren naar PDF: Specifieke layout met Aspose.CAD voor Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}