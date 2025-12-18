---
date: 2025-12-18
description: Leer hoe u DWG naar PNG en andere rasterafbeeldingsformaten kunt converteren
  met Aspose.CAD voor Java. Exporteer CAD als PNG met resultaten van hoge kwaliteit.
linktitle: Convert CAD Layout to Raster Image Format
second_title: Aspose.CAD Java API
title: DWG converteren naar PNG en andere rasterformaten met Aspose.CAD voor Java
url: /nl/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG naar PNG en andere rasterformaten converteren met Aspose.CAD voor Java

## Introductie

Het converteren van DWG naar PNG (of andere raster‑beeldformaten) is een veelvoorkomende behoefte wanneer je CAD‑tekeningen wilt delen met teamleden die geen CAD‑viewer hebben, ontwerpen wilt insluiten in documentatie, of miniatuur‑afbeeldingen wilt genereren voor webgalerijen. Aspose.CAD voor Java maakt deze conversie eenvoudig, of je nu werkt met een volledig tekenbestand of alleen een specifieke layout. In deze tutorial lopen we de exacte stappen door om **een CAD‑layout naar een raster‑afbeelding te converteren** — dezelfde techniek die je kunt toepassen om PNG, JPEG, TIFF of PDF uit te geven.

## Snelle antwoorden
- **Welke bibliotheek verwerkt DWG naar PNG?** Aspose.CAD for Java  
- **Welke formaten kunnen worden geëxporteerd?** PNG, JPEG, TIFF, PDF, BMP, en meer  
- **Heb ik een licentie nodig voor testen?** Een gratis proefversie werkt voor ontwikkeling; een licentie is vereist voor productie  
- **Kan ik een specifieke layout kiezen?** Ja, gebruik `setLayouts` om “Model”, “Layout1”, enz. te targeten.  
- **Is output met hoge resolutie mogelijk?** Absoluut—pas `setPageWidth` en `setPageHeight` aan om DPI te regelen  

## Wat is “convert dwg to png”?

De uitdrukking “convert dwg to png” beschrijft het proces waarbij een vector‑gebaseerd DWG‑bestand (het native formaat voor veel CAD‑toepassingen) wordt gerasterd tot een pixel‑gebaseerde PNG‑afbeelding. Raster‑afbeeldingen zijn ideaal voor weergave op het web, e‑maildeling en integratie in niet‑CAD‑software.

## Waarom CAD exporteren als PNG (of andere rasterformaten)?

- **Universele compatibiliteit:** PNG en JPEG worden ondersteund door vrijwel elke afbeeldingsviewer en browser.  
- **Snelle laadtijd:** Rasterafbeeldingen laden onmiddellijk in vergelijking met het openen van een zwaar DWG‑bestand.  
- **Eenvoudige insluiting:** Voeg PNG's direct in Word, PowerPoint of HTML in zonder extra plug‑ins.  
- **Consistente weergave:** Je beheert resolutie, achtergrond en layout, zodat elke belanghebbende dezelfde visual ziet.  

## Voorvereisten

1. **Java‑ontwikkelomgeving** – JDK 8 of nieuwer geïnstalleerd en geconfigureerd.  
2. **Aspose.CAD for Java** – Download de nieuwste JAR van de [Aspose.CAD for Java documentatie](https://reference.aspose.com/cad/java/).  

## Namespaces importeren

Eerst importeer je de klassen die je nodig hebt. Deze imports geven je toegang tot het laden van afbeeldingen, rasterisatie‑opties en de TIFF/PNG‑uitvoersettings.

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

> **Pro tip:** Als je PNG wilt exporteren in plaats van TIFF, vervang je `TiffOptions` door `PngOptions` (te vinden in `com.aspose.cad.imageoptions.PngOptions`).

## Stapsgewijze handleiding

### Stap 1: De resource‑directory instellen

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";
```

Vervang `"Your Document Directory"` door het absolute pad waar je CAD‑bestanden zich bevinden.

### Stap 2: Het CAD‑bestand laden

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

Je kunt elk ondersteund formaat laden (DWG, DXF, DGN, enz.). Dit is het **hoe je cad converteert**‑deel — wijs simpelweg naar het bestand en laat Aspose de parsing afhandelen.

### Stap 3: Rasterisatie‑opties configureren

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
rasterizationOptions.setLayouts(new String[] {"Model", "Layout1"});
```

- `setPageWidth` / `setPageHeight` regelen de uitvoerresolutie (grotere waarden = hogere DPI).  
- `setLayouts` laat je **cad naar raster converteren** voor specifieke layouts; laat het weg om de hele tekening te rasteren.

### Stap 4: Afbeeldingsopties instellen

```java
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.setVectorRasterizationOptions(rasterizationOptions);
```

Als je PNG verkiest, instantiateer je `PngOptions` in plaats van `TiffOptions`. Hier kun je **cad als png exporteren**.

### Stap 5: Het resulterende beeld opslaan

```java
image.save(dataDir + "conic_pyramid_layoutstorasterimage_out_.tiff", options);
```

Verander de bestandsextensie naar `.png` (en het opties‑object naar `PngOptions`) om **CAD als JPEG/PNG op te slaan**.

> **Veelvoorkomende valkuil:** Het niet laten overeenkomen van de bestandsextensie met de opties‑klasse veroorzaakt een `UnsupportedFormatException`. Houd ze altijd synchroon.

## Veelvoorkomende problemen en oplossingen

| Probleem | Oplossing |
|----------|-----------|
| **Lege uitvoerafbeelding** | Controleer of de layout‑namen in `setLayouts` exact overeenkomen met die in het bron‑CAD‑bestand. |
| **Lage resolutie PNG** | Verhoog `setPageWidth` / `setPageHeight` of stel `setResolution` in op de rasterisatie‑opties. |
| **Niet‑ondersteunde DWG‑versie** | Zorg dat je de nieuwste Aspose.CAD‑versie gebruikt; oudere versies ondersteunen mogelijk geen nieuwere DWG‑releases. |
| **Geheugenfouten bij grote bestanden** | Verwerk pagina’s één voor één of vergroot de JVM‑heap (`-Xmx2g`). |

## Veelgestelde vragen

**Q: Is Aspose.CAD compatible with different CAD file formats?**  
A: Ja, het ondersteunt DWG, DXF, DGN en vele andere.

**Q: Can I customize the resolution of the output raster image?**  
A: Absoluut. Pas `setPageWidth`, `setPageHeight` of `setResolution` aan in `CadRasterizationOptions`.

**Q: How can I convert multiple CAD layouts in a single run?**  
A: Geef een array met alle layout‑namen door aan `setLayouts`, bijv. `new String[]{"Model","Layout1","Layout2"}`.

**Q: Are there output formats besides TIFF supported?**  
A: Ja—PNG, JPEG, BMP, PDF en meer zijn beschikbaar via hun respectieve `*Options`‑klassen.

**Q: Where can I get help or share my experience with Aspose.CAD?**  
A: Bezoek het [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) voor community‑ondersteuning en officiële assistentie.

## Conclusie

Door deze stappen te volgen kun je **DWG naar PNG converteren**, **CAD als PNG exporteren**, **CAD als JPEG opslaan**, of elk ander rasterformaat genereren dat je nodig hebt. Aspose.CAD voor Java doet het zware werk, zodat jij je kunt richten op het integreren van hoogwaardige afbeeldingen in je applicaties, documentatie of webportalen.

---

**Last Updated:** 2025-12-18  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}