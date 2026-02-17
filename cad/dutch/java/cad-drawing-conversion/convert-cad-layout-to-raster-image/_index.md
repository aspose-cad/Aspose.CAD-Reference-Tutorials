---
date: 2026-02-17
description: Leer hoe u DWG naar PNG kunt converteren en CAD kunt exporteren als PNG
  of andere rasterformaten met Aspose.CAD voor Java. Verkrijg snel resultaten van
  hoge kwaliteit.
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

## Inleiding

Het converteren van DWG naar PNG (of andere rasterafbeeldingsformaten) is een veelvoorkomende behoefte wanneer je CAD‑tekeningen moet delen met teamleden die geen CAD‑viewer hebben, ontwerpen in documentatie wilt insluiten, of miniaturen voor webgalerijen wilt genereren. **In deze gids leer je hoe je dwg naar png snel en betrouwbaar kunt converteren**, of je nu werkt met een volledig tekenbestand of slechts een specifieke lay‑out. Mogelijk moet je ook **CAD naar raster converteren** voor webvoorbeelden, rapportagetools of mobiele apps. Aspose.CAD voor Java maakt deze conversie eenvoudig en geeft je volledige controle over resolutie, lay‑outselectie en uitvoerformaat.

## Quick Answers
- **Welke bibliotheek verwerkt DWG naar PNG?** Aspose.CAD for Java  
- **Welke formaten kunnen worden geëxporteerd?** PNG, JPEG, TIFF, PDF, BMP, en meer  
- **Heb ik een licentie nodig voor testen?** Een gratis proefversie werkt voor ontwikkeling; een licentie is vereist voor productie  
- **Kan ik een specifieke lay‑out kiezen?** Ja, gebruik `setLayouts` om “Model”, “Layout1”, enz. te targeten.  
- **Is output met hoge resolutie mogelijk?** Absoluut—pas `setPageWidth` en `setPageHeight` aan om DPI te regelen  

## Wat is “convert dwg to png”?

De zin “convert dwg to png” beschrijft het proces waarbij een vector‑gebaseerd DWG‑bestand (het native formaat voor veel CAD‑toepassingen) wordt gerasterd tot een pixel‑gebaseerde PNG‑afbeelding. Rasterafbeeldingen zijn ideaal voor weergave op het web, e‑maildeling en integratie in niet‑CAD‑software.

## Waarom CAD exporteren als PNG (of andere rasterformaten)?

- **Universele compatibiliteit:** PNG en JPEG worden ondersteund door vrijwel elke afbeeldingsviewer en browser.  
- **Snelle laadtijd:** Rasterafbeeldingen laden direct in vergelijking met het openen van een zwaar DWG‑bestand.  
- **Eenvoudig insluiten:** Voeg PNG's direct in Word, PowerPoint of HTML in zonder extra plug‑ins.  
- **Consistente weergave:** Je beheert resolutie, achtergrond en lay‑out, zodat elke belanghebbende dezelfde visual ziet.  

## Veelvoorkomende gebruikssituaties

| Scenario | Waarom rasteroutput helpt |
|----------|---------------------------|
| **Projectdocumentatie** | PNG's insluiten in PDF's of Word‑documenten voorkomt dat reviewers CAD‑software nodig hebben. |
| **Webportalen** | Miniaturen gegenereerd uit DWG‑bestanden laden direct en verbeteren de gebruikerservaring. |
| **Mobiele apps** | Rasterafbeeldingen worden correct weergegeven op apparaten zonder CAD‑viewers. |
| **Geautomatiseerde rapportage** | Batch‑conversie van meerdere lay‑outs naar PNG/JPEG voor opname in grafieken of dashboards. |

## Voorvereisten

Zorg ervoor dat je het volgende hebt voordat je begint:

1. **Java-ontwikkelomgeving** – JDK 8 of nieuwer geïnstalleerd en geconfigureerd.  
2. **Aspose.CAD for Java** – Download de nieuwste JAR van de [Aspose.CAD for Java documentation](https://reference.aspose.com/cad/java/).  

## Importer namespaces

Eerst importeer je de klassen die je nodig hebt. Deze imports geven je toegang tot het laden van afbeeldingen, rasterisatie‑opties en de TIFF/PNG‑uitvoerinstellingen.

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

> **Pro tip:** Als je van plan bent **CAD als PNG te exporteren** in plaats van TIFF, vervang dan `TiffOptions` door `PngOptions` (gevonden in `com.aspose.cad.imageoptions.PngOptions`).  

## Stapsgewijze handleiding

### Stap 1: Stel de resource‑directory in

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";
```

Vervang `"Your Document Directory"` door het absolute pad waar je CAD‑bestanden zich bevinden.

### Stap 2: Laad het CAD‑bestand

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

Je kunt elk ondersteund formaat laden (DWG, DXF, DGN, enz.). Dit is het **hoe je CAD converteert**‑deel—wijs simpelweg naar het bestand en laat Aspose het parsen.

### Stap 3: Configureer rasterisatie‑opties

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
rasterizationOptions.setLayouts(new String[] {"Model", "Layout1"});
```

- `setPageWidth` / `setPageHeight` regelen de uitvoerresolutie (grotere waarden = hogere DPI).  
- `setLayouts` stelt je in staat **CAD naar raster te converteren** voor specifieke lay‑outs; laat het weg om de volledige tekening te rasteren.

### Stap 4: Stel afbeeldingsopties in

```java
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.setVectorRasterizationOptions(rasterizationOptions);
```

Als je PNG verkiest, instantieer dan `PngOptions` in plaats van `TiffOptions`. Dit is waar je **CAD als PNG exporteert**.

### Stap 5: Sla de resulterende afbeelding op

```java
image.save(dataDir + "conic_pyramid_layoutstorasterimage_out_.tiff", options);
```

Verander de bestandsextensie naar `.png` (en het optiesobject naar `PngOptions`) om **CAD op te slaan als JPEG/PNG**.

> **Veelvoorkomende valkuil:** Als je de bestandsextensie niet afstemt op de opties‑klasse, ontstaat een `UnsupportedFormatException`. Houd ze altijd synchroon.

## Veelvoorkomende problemen en oplossingen

| Probleem | Oplossing |
|----------|-----------|
| **Lege uitvoerafbeelding** | Controleer of de lay‑outnamen in `setLayouts` exact overeenkomen met die in het bron‑CAD‑bestand. |
| **PNG met lage resolutie** | Verhoog `setPageWidth` / `setPageHeight` of stel `setResolution` in op de rasterisatie‑opties. |
| **Niet‑ondersteunde DWG‑versie** | Zorg dat je de nieuwste Aspose.CAD‑versie gebruikt; oudere versies ondersteunen mogelijk geen nieuwere DWG‑releases. |
| **Geheugenfouten bij grote bestanden** | Verwerk pagina’s één voor één of vergroot de JVM‑heap (`-Xmx2g`). |

## Veelgestelde vragen

**Q: Is Aspose.CAD compatibel met verschillende CAD‑bestandformaten?**  
A: Ja, het ondersteunt DWG, DXF, DGN en vele anderen.

**Q: Kan ik de resolutie van de uitvoer‑rasterafbeelding aanpassen?**  
A: Absoluut. Pas `setPageWidth`, `setPageHeight` of `setResolution` aan in `CadRasterizationOptions`.

**Q: Hoe kan ik meerdere CAD‑lay-outs in één keer converteren?**  
A: Geef een array met alle lay‑outnamen aan `setLayouts`, bijvoorbeeld `new String[]{"Model","Layout1","Layout2"}`.

**Q: Zijn er naast TIFF ook andere ondersteunde uitvoerformaten?**  
A: Ja—PNG, JPEG, BMP, PDF en meer zijn beschikbaar via hun respectieve `*Options`‑klassen.

**Q: Waar kan ik hulp krijgen of mijn ervaring met Aspose.CAD delen?**  
A: Bezoek het [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) voor community‑ondersteuning en officiële assistentie.

## Conclusie

Door deze stappen te volgen kun je **DWG naar PNG converteren**, **CAD als PNG exporteren**, **CAD als JPEG opslaan**, of elk ander rasterformaat genereren dat je nodig hebt. Aspose.CAD voor Java neemt het zware werk uit handen, zodat je je kunt concentreren op het integreren van hoogwaardige afbeeldingen in je applicaties, documentatie of webportalen.

**Laatst bijgewerkt:** 2026-02-17  
**Getest met:** Aspose.CAD for Java 24.12  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}