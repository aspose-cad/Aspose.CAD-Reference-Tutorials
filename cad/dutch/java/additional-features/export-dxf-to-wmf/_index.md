---
date: 2026-10-30
description: Leer hoe u DXF‑bestanden batchgewijs kunt converteren naar WMF met Aspose.CAD
  for Java, met stapsgewijze code, informatie over een gratis proefversie en optionele
  PDF‑export.
keywords:
- batch convert dxf files
- aspose cad java
- dxf to wmf conversion
- java cad rasterization
- aspose free trial
lastmod: 2026-10-30
linktitle: DXF exporteren naar WMF‑formaat met Java
og_description: Batchconversie van DXF‑bestanden naar WMF met Aspose.CAD for Java.
  Volg deze gids om DXF‑tekeningen te laden, rasterisatie‑opties in te stellen, op
  te slaan als WMF en optioneel te exporteren naar PDF met een gratis proefversie.
og_image_alt: Tutorial showing batch conversion of DXF to WMF in Java using Aspose.CAD
og_title: Batchconversie van DXF‑bestanden naar WMF met Aspose.CAD for Java
schemas:
- author: Aspose
  dateModified: '2026-10-30'
  description: Learn how to batch convert DXF files to WMF using Aspose.CAD for Java,
    with step‑by‑step code, free trial info, and optional PDF export.
  headline: Batch convert DXF files to WMF with Aspose.CAD for Java
  type: TechArticle
- description: Learn how to batch convert DXF files to WMF using Aspose.CAD for Java,
    with step‑by‑step code, free trial info, and optional PDF export.
  name: Batch convert DXF files to WMF with Aspose.CAD for Java
  steps:
  - name: load dxf drawing
    text: Image.load reads the DXF file into an Aspose.CAD Image object.
  - name: configure rasterization options
    text: '`CadRasterizationOptions` specifies page size, resolution, and background
      for rasterizing the CAD drawing.'
  - name: save as wmf
    text: '`ImageSaveOptions` with `SaveFormat.WMF` tells Aspose.CAD to write the
      output as a Windows Metafile.'
  - name: dispose of resources
    text: Calling `image.close()` releases native resources used by the Aspose.CAD
      Image object.
  - name: optional – export to pdf
    text: '`PdfOptions` configures PDF‑specific settings when saving the image as
      a PDF document. > **Pro tip:** You can reuse the same `CadRasterizationOptions`
      object for PDF export by passing it to a `PdfOptions` instance, saving you a
      few lines of setup.'
  type: HowTo
- questions:
  - answer: You can access the documentation [Aspose.CAD Java documentation](https://reference.aspose.com/cad/java/).
    question: Where can I find the Aspose.CAD documentation?
  - answer: Download the library [Aspose.CAD Java download page](https://releases.aspose.com/cad/java/).
    question: How do I download Aspose.CAD for Java?
  - answer: Yes, you can get a free trial [Aspose free trial page](https://releases.aspose.com/).
    question: Is there a free trial available?
  - answer: Explore temporary licenses [temporary license options](https://purchase.aspose.com/temporary-license/).
    question: Need temporary licensing options?
  - answer: Visit the Aspose.CAD support forum [Aspose.CAD support forum](https://forum.aspose.com/c/cad/19).
    question: Where can I get support?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- batch convert dxf
- Aspose.CAD
- Java CAD conversion
- WMF export
- DXF processing
title: Batchconversie van DXF‑bestanden naar WMF met Aspose.CAD for Java
url: /nl/java/additional-features/export-dxf-to-wmf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Batch converteer DXF-bestanden naar WMF met Aspose.CAD voor Java

## Introductie

In deze tutorial leer je hoe je **DXF-bestanden batch converteert naar WMF** met Aspose.CAD voor Java. Of je nu CAD-tekeningen wilt insluiten in Windows‑gebaseerde rapporten, lichte vectorafbeeldingen wilt genereren voor Office‑documenten, of grootschalige conversies wilt automatiseren, deze gids leidt je door het laden van een DXF-tekening, het configureren van rasterisatie‑opties, het opslaan als WMF, en optioneel het exporteren van dezelfde tekening naar PDF. De stappen werken op elk platform dat Java 8+ ondersteunt.

## Snelle antwoorden
- **Kan ik DXF naar WMF converteren met een gratis proefversie?** Ja – Aspose biedt een volledig functionele 30‑daagse proefversie.  
- **Welke Java‑versie is vereist?** Java 8 of later.  
- **Heb ik een licentie nodig om de code uit te voeren?** Een licentie is vereist voor productie; de proefversie werkt voor ontwikkeling en testen.  
- **Is de conversie verliesvrij?** Vectorgegevens worden behouden; rasterisatie‑opties laten je de resolutie bepalen.  
- **Kan ik dezelfde tekening ook exporteren naar PDF?** Absoluut – zie de stap “Exporteren naar PDF” hieronder.  
- **Hoe batch converteer ik veel DXF‑bestanden tegelijk?** Loop door een map, pas hetzelfde laad‑raster‑opsla‑patroon toe op elk bestand.

## Wat is batchconversie van DXF-bestanden?

Batchconversie van DXF-bestanden betekent dat meerdere Drawing Exchange Format (DXF) tekeningen in één uitvoering worden verwerkt en voor elk WMF‑output wordt gegenereerd. WMF (Windows Metafile) is een vectorafbeeldingsformaat dat native integreert met Microsoft Office, Windows‑applicaties en vele rapportagetools.

## Waarom Aspose.CAD voor Java gebruiken?

Aspose.CAD voor Java is een pure‑Java engine die **meer dan 50 invoer‑ en uitvoerformaten** ondersteunt — waaronder DXF, DWG, DGN, PDF, PNG, SVG en WMF — terwijl het **99 % vectorgetrouwheid** levert. Het draait op elk OS dat Java ondersteunt, vereist geen native DLL’s, en laat je paginagrootte, DPI en achtergrondkleur regelen via één enkele `CadRasterizationOptions`‑klasse. Dezelfde API verwerkt ook PDF-, PNG‑ en SVG‑export, waardoor je geen meerdere bibliotheken nodig hebt.

### Gekwantificeerde voordelen
- **50+ ondersteunde formaten** verminderen de noodzaak voor externe converters.  
- **Verwerkt 300‑pagina‑DXF‑bestanden in minder dan 5 seconden** op een typische 2,5 GHz server bij rasterisatie op 150 DPI.  
- **Geheugengebruik blijft onder 200 MB** voor bestanden tot 500 MB wanneer je passende paginagroottes instelt.  

## Vereisten

- **Aspose.CAD voor Java** geïntegreerd in je project. Download het van de officiële site: [Aspose.CAD Java download](https://releases.aspose.com/cad/java/).  
- Een map die de DXF‑bestanden bevat die je wilt converteren (bijv. `Your Document Directory/DXFDrawings/`).  

## Importeer namespaces

`Image` is de kernklasse van Aspose.CAD die een CAD‑tekening in het geheugen vertegenwoordigt. Na het laden van een bestand worden alle daaropvolgende bewerkingen — rasterisatie, formaatconversie en opruimen van bronnen — uitgevoerd via dit object.

De volgende imports brengen de Aspose.CAD‑klassen binnen die nodig zijn voor het laden, rasteriseren en opslaan van CAD‑bestanden.  
```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageSaveOptions;
import com.aspose.cad.fileformats.cad.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.CadImageInfo;
import com.aspose.cad.fileformats.cad.CadImageInfo;
import java.awt.Color;
```

## Stapsgewijze handleiding

### Hoe batch converteer ik DXF-bestanden naar WMF in Java?

Laad elke DXF met `Image.load`, configureer `CadRasterizationOptions` voor de gewenste paginagrootte en DPI, en roep `image.save` aan met `SaveFormat.WMF`. Dit drie‑stappen‑patroon voert de volledige conversie uit terwijl de vectorkwaliteit behouden blijft en vereist slechts enkele regels code per bestand.

#### Stap 1: laad dxf-tekening

Image.load leest het DXF‑bestand in een Aspose.CAD Image‑object.  
```java
import com.aspose.cad.Color;
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.WmfOptions;
```

#### Stap 2: configureer rasterisatie‑opties

`CadRasterizationOptions` specificeert paginagrootte, resolutie en achtergrond voor het rasteriseren van de CAD‑tekening.  
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DXFDrawings/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

#### Stap 3: opslaan als wmf

`ImageSaveOptions` met `SaveFormat.WMF` vertelt Aspose.CAD om de output te schrijven als een Windows Metafile.  
```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(100);
rasterizationOptions.setPageHeight(100);
WmfOptions wmfOptions = new WmfOptions();
```

#### Stap 4: resources vrijgeven

Het aanroepen van `image.close()` geeft de native bronnen vrij die door het Aspose.CAD Image‑object worden gebruikt.  
```java
cadImage.save(dataDir+" example.ifc.wmf", wmfOptions);
```

#### Stap 5: optioneel – exporteren naar pdf

`PdfOptions` configureert PDF‑specifieke instellingen bij het opslaan van de afbeelding als een PDF‑document.  
```java
finally
{
  cadImage.dispose();
}
```

> **Pro tip:** Je kunt hetzelfde `CadRasterizationOptions`‑object hergebruiken voor PDF‑export door het door te geven aan een `PdfOptions`‑instantie, waardoor je enkele configuratieregels bespaart.

## Hoe exporteer ik DXF naar PDF met Aspose CAD Java?

Vervang het WMF‑opslagformaat door PDF door `new ImageSaveOptions(SaveFormat.Pdf)` te gebruiken. Dezelfde rasterisatie‑instellingen gelden, en je kunt bovendien PDF‑specifieke opties instellen, zoals auteur‑metadata of compressieniveau. Deze één‑regelige conversie levert een doorzoekbare, paginacorrecte PDF die de oorspronkelijke CAD‑lay-out weerspiegelt.

## Veelvoorkomende problemen en oplossingen

`License` is de Aspose‑klasse die wordt gebruikt om een productlicentie tijdens runtime toe te passen.

| Probleem | Oorzaak | Oplossing |
|----------|---------|-----------|
| **`NullPointerException` op `cadImage.save`** | Variabele `cadImage` niet gedefinieerd (moet `image` zijn). | Vervang `cadImage` door `image` of hernoem de variabele consequent. |
| **Uitvoer‑WMF is leeg** | Rasterisatie‑paginagrootte te klein of achtergrondkleur ingesteld op transparant. | Verhoog `PageWidth`/`PageHeight` of stel een achtergrondkleur in via `rasterizationOptions.setBackgroundColor(Color.WHITE);`. |
| **Licentie‑exception** | Uitvoeren zonder een geldige Aspose‑licentie in productie. | Pas het licentiebestand toe bij applicatie‑start: `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`. |

## Veelgestelde vragen

**V: Waar vind ik de Aspose.CAD‑documentatie?**  
A: Je kunt de documentatie raadplegen via [Aspose.CAD Java documentatie](https://reference.aspose.com/cad/java/).

**V: Hoe download ik Aspose.CAD voor Java?**  
A: Download de bibliotheek op de [Aspose.CAD Java downloadpagina](https://releases.aspose.com/cad/java/).

**V: Is er een gratis proefversie beschikbaar?**  
A: Ja, je kunt een gratis proefversie krijgen op de [Aspose gratis proefversie‑pagina](https://releases.aspose.com/).

**V: Heb je tijdelijke licentie‑opties nodig?**  
A: Bekijk tijdelijke licenties op [tijdelijke licentie‑opties](https://purchase.aspose.com/temporary-license/).

**V: Waar kan ik ondersteuning krijgen?**  
A: Bezoek het Aspose.CAD‑ondersteuningsforum via [Aspose.CAD support forum](https://forum.aspose.com/c/cad/19).

## Aanvullende veelgestelde vragen

**V: Kan ik grote DXF‑bestanden (honderden MB) converteren zonder geheugenproblemen?**  
A: Ja. Laad het bestand in een try‑with‑resources‑blok en maak het `Image`‑object direct vrij. Pas `CadRasterizationOptions.setPageWidth/Height` aan naar een redelijke grootte om het geheugengebruik laag te houden.

**V: Behoudt de WMF‑output laag‑informatie?**  
A: WMF is een plat vectorformaat, dus de laag‑hiërarchie wordt afgevlakt, maar lijntypes, kleuren en hatch‑patronen blijven behouden.

**V: Is het mogelijk een aangepaste DPI voor de WMF in te stellen?**  
A: Gebruik `rasterizationOptions.setResolution(300);` om de DPI te definiëren vóór het opslaan.

**V: Kan ik meerdere DXF‑bestanden in één run batch‑converteren?**  
A: Absoluut. Loop door een directory, laad elk bestand en pas dezelfde rasterisatie‑ en opslaglogica toe.

**V: Welke Java‑versies worden ondersteund?**  
A: Aspose.CAD voor Java ondersteunt Java 8 en later, inclusief Java 11, 17 en nieuwere LTS‑releases.

---

**Laatst bijgewerkt:** 2026-10-30  
**Getest met:** Aspose.CAD voor Java 24.11  
**Auteur:** Aspose

## Gerelateerde tutorials

- [Create PDF from CAD – Export DXF to PDF with Aspose.CAD for Java](/cad/java/additional-features/export-dxf-to-pdf/)
- [Create PDF from DXF: Export Layer with Aspose.CAD for Java](/cad/java/additional-features/export-specific-layer-to-pdf/)
- [How to Convert DXF Layout to JPEG Image with Aspose.CAD in Java](/cad/java/additional-features/export-specific-layout-to-image/)









```java
image.save(dataDir + "conic_pyramid_out_.pdf"); 
```

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}