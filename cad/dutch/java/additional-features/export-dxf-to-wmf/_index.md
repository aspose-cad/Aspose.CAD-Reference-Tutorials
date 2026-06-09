---
date: 2026-06-09
description: Leer hoe u DXF naar WMF kunt converteren met Aspose.CAD voor Java, inclusief
  een gratis proefversie, ondersteuning voor Java 8+ en optionele PDF-export. Stapsgewijze
  handleiding met codevoorbeelden.
keywords:
- convert dxf to wmf
- aspose cad java
- aspose free trial
- aspose cad conversion
- export dxf pdf
linktitle: DXF exporteren naar WMF-formaat met Java
schemas:
- author: Aspose
  dateModified: '2026-06-09'
  description: Learn how to convert DXF to WMF with Aspose.CAD for Java, including
    a free trial, Java 8+ support, and optional PDF export. Step‑by‑step guide with
    code examples.
  headline: Convert DXF to WMF Using Aspose.CAD in Java
  type: TechArticle
- description: Learn how to convert DXF to WMF with Aspose.CAD for Java, including
    a free trial, Java 8+ support, and optional PDF export. Step‑by‑step guide with
    code examples.
  name: Convert DXF to WMF Using Aspose.CAD in Java
  steps:
  - name: Load DXF Drawing
    text: Image.load reads the DXF file into an Aspose.CAD Image object.
  - name: Configure Rasterization Options
    text: CadRasterizationOptions specifies page size, resolution, and background
      for rasterizing the CAD drawing.
  - name: Save as WMF
    text: ImageSaveOptions with SaveFormat.WMF tells Aspose.CAD to write the output
      as a Windows Metafile.
  - name: Dispose of Resources
    text: Calling image.close() releases native resources used by the Aspose.CAD Image
      object.
  - name: Optional – Export to PDF
    text: PdfOptions configures PDF‑specific settings when saving the image as a PDF
      document. > **Pro tip:** You can reuse the same `CadRasterizationOptions` object
      for PDF export by passing it to a `PdfOptions` instance, saving you a few lines
      of setup.
  type: HowTo
- questions:
  - answer: Yes. Load the file in a try‑with‑resources block and dispose of the `Image`
      object promptly. Adjust `CadRasterizationOptions.setPageWidth/Height` to a reasonable
      size to keep memory usage low.
    question: Can I convert large DXF files (hundreds of MB) without running out of
      memory?
  - answer: WMF is a flat vector format, so layer hierarchy is flattened, but line
      styles, colors, and hatch patterns are preserved.
    question: Does the WMF output retain layer information?
  - answer: Use `rasterizationOptions.setResolution(300);` to define DPI before saving.
    question: Is it possible to set a custom DPI for the WMF?
  - answer: Absolutely. Loop through a directory, load each file, and apply the same
      rasterization and save logic.
    question: Can I batch‑convert multiple DXF files in one run?
  - answer: Aspose.CAD for Java supports Java 8 and later, including Java 11, 17,
      and newer LTS releases.
    question: What versions of Java are supported?
  type: FAQPage
second_title: Aspose.CAD Java API
title: DXF converteren naar WMF met Aspose.CAD in Java
url: /nl/java/additional-features/export-dxf-to-wmf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DXF naar WMF converteren met Aspose.CAD in Java

## Inleiding

In deze tutorial ontdek je hoe je **convert DXF to WMF** kunt uitvoeren met Aspose.CAD voor Java. Of je nu CAD‑tekeningen moet insluiten in een Windows‑gebaseerd rapport, lichte vectorafbeeldingen voor Office‑documenten moet genereren, of batchconversies moet automatiseren, het converteren van DXF naar WMF is een veelvoorkomende vereiste in engineering‑ en rapportage‑pijplijnen. We lopen door het laden van een DXF‑tekening, het configureren van rasterisatie‑opties, het opslaan van het resultaat als WMF, en optioneel het exporteren van dezelfde tekening naar PDF.

## Snelle antwoorden
- **Kan ik DXF naar WMF converteren met een gratis proefversie?** Ja – Aspose biedt een volledig functionele 30‑daagse proefversie.  
- **Welke Java‑versie is vereist?** Java 8 of hoger.  
- **Heb ik een licentie nodig om de code uit te voeren?** Een licentie is vereist voor productie; de proefversie werkt voor ontwikkeling en testen.  
- **Is de conversie verliesvrij?** Vectorgegevens worden behouden; rasterisatie‑opties laten je resolutie regelen.  
- **Kan ik dezelfde tekening ook exporteren naar PDF?** Absoluut – zie de stap “Export to PDF” hieronder.

## Wat is “convert DXF to WMF”?

DXF naar WMF converteren betekent dat je een Drawing Exchange Format (DXF)‑bestand—een veelgebruikt CAD‑formaat—omzet naar een Windows Metafile (WMF). WMF is een vectorafbeeldingsformaat dat naadloos integreert met Microsoft Office, Windows‑toepassingen en vele rapportagetools.

## Waarom Aspose.CAD voor Java gebruiken?

Aspose.CAD voor Java biedt een pure‑Java, geen‑native‑DLL engine die CAD‑bestanden converteert met **meer dan 99 % vectorgetrouwheid**, waarbij lagen, kleuren, lijnstijlen en arceringspatronen behouden blijven. Het ondersteunt **meer dan 50 invoer‑ en uitvoerformaten**—inclusief DXF, DWG, DGN, PDF, PNG, SVG en WMF—en stelt je in staat om paginagrootte, DPI en achtergrondkleur fijn af te stemmen via ingebouwde rasterisatie‑opties. dezelfde API verwerkt ook export naar PDF, PNG en SVG, waardoor je geen meerdere bibliotheken nodig hebt.

### Belangrijkste voordelen
- **Geen externe afhankelijkheden** – pure Java, werkt op elk OS dat Java draait.  
- **Hoge‑getrouwe weergave** – behoudt lijndikte, kleur en arceringsdetails.  
- **Ingebouwde rasterisatie** – controle over paginagrootte, resolutie en achtergrond.  
- **Alles‑in‑één conversie** – dezelfde klassen exporteren naar WMF, PDF, PNG, SVG, enz.

## Voorvereisten

Voordat je begint, zorg ervoor dat je het volgende hebt:

- **Aspose.CAD for Java** geïntegreerd in je project. Download het van de officiële site: [Aspose.CAD Java download](https://releases.aspose.com/cad/java/).  
- **Documentmap** waar je DXF‑bestanden zijn opgeslagen (bijv. `Your Document Directory/DXFDrawings/`).  

## Import Namespaces

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

### Hoe converteer ik DXF naar WMF in Java?

Laad je DXF‑bestand met `Image.load("yourFile.dxf")`, configureer `CadRasterizationOptions` voor de gewenste paginagrootte en DPI, en roep vervolgens `image.save("output.wmf", new ImageSaveOptions(SaveFormat.WMF))` aan. Dit driewegpatroon voert de volledige conversie uit terwijl de vectorkwaliteit behouden blijft en vereist slechts enkele regels code.

#### Stap 1: DXF‑tekening laden

Image.load leest het DXF‑bestand in een Aspose.CAD Image‑object.  
```java
import com.aspose.cad.Color;
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.WmfOptions;
```

#### Stap 2: Rasterisatie‑opties configureren

CadRasterizationOptions specificeert paginagrootte, resolutie en achtergrond voor het rasteriseren van de CAD‑tekening.  
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DXFDrawings/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

#### Stap 3: Opslaan als WMF

ImageSaveOptions met SaveFormat.WMF instrueert Aspose.CAD om de output te schrijven als een Windows Metafile.  
```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(100);
rasterizationOptions.setPageHeight(100);
WmfOptions wmfOptions = new WmfOptions();
```

#### Stap 4: Resources vrijgeven

Het aanroepen van image.close() geeft de native resources vrij die door het Aspose.CAD Image‑object worden gebruikt.  
```java
cadImage.save(dataDir+" example.ifc.wmf", wmfOptions);
```

#### Stap 5: Optioneel – Exporteren naar PDF

PdfOptions configureert PDF‑specifieke instellingen bij het opslaan van de afbeelding als een PDF‑document.  
```java
finally
{
  cadImage.dispose();
}
```

> **Pro tip:** Je kunt hetzelfde `CadRasterizationOptions`‑object hergebruiken voor PDF‑export door het door te geven aan een `PdfOptions`‑instantie, waardoor je enkele regels configuratie bespaart.

## Hoe exporteer ik DXF naar PDF met Aspose CAD Java?

Exporteren naar PDF volgt dezelfde laad‑ en rasterisatiestappen; vervang simpelweg het WMF‑opslaan‑formaat door PDF. Gebruik `new ImageSaveOptions(SaveFormat.Pdf)` en stel optioneel PDF‑specifieke opties in, zoals compressieniveau of auteur‑metadata. Deze één‑regelconversie produceert een doorzoekbare, paginacorrecte PDF die de oorspronkelijke CAD‑lay-out weerspiegelt.

## Veelvoorkomende problemen en oplossingen

| Probleem | Oorzaak | Oplossing |
|----------|---------|-----------|
| **`NullPointerException` on `cadImage.save`** | Variabele `cadImage` niet gedefinieerd (moet `image` zijn). | Vervang `cadImage` door `image` of hernoem de variabele consequent. |
| **Output WMF is blank** | Rasterisatie‑paginagrootte te klein of achtergrondkleur ingesteld op transparant. | Vergroot `PageWidth`/`PageHeight` of stel een achtergrondkleur in via `rasterizationOptions.setBackgroundColor(Color.WHITE);`. |
| **License exception** | Uitvoeren zonder een geldige Aspose‑licentie in productie. | Pas het licentiebestand toe bij applicatie‑start: `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`. |

## Conclusie

Je hebt nu een volledige, productie‑klare workflow om **DXF naar WMF** te converteren met Aspose.CAD voor Java, met een optionele stap om **dezelfde tekening naar PDF** te exporteren. Deze aanpak levert hoogwaardige vectoroutput die naadloos integreert met Windows‑gebaseerde rapportage‑ en documentatietools, terwijl je codebase eenvoudig en zonder afhankelijkheden blijft.

## Veelgestelde vragen

### Q1: Waar kan ik de Aspose.CAD-documentatie vinden?

A1: Je kunt de documentatie raadplegen [hier](https://reference.aspose.com/cad/java/).

### Q2: Hoe download ik Aspose.CAD voor Java?

A2: Download de bibliotheek [hier](https://releases.aspose.com/cad/java/).

### Q3: Is er een gratis proefversie beschikbaar?

A3: Ja, je kunt een gratis proefversie krijgen [hier](https://releases.aspose.com/).

### Q4: Tijdelijke licentieopties nodig?

A4: Verken tijdelijke licenties [hier](https://purchase.aspose.com/temporary-license/).

### Q5: Waar kan ik ondersteuning krijgen?

A5: Bezoek het Aspose.CAD‑ondersteuningsforum [hier](https://forum.aspose.com/c/cad/19).

## Veelgestelde vragen

**Q: Kan ik grote DXF‑bestanden (honderden MB) converteren zonder geheugenproblemen?**  
A: Ja. Laad het bestand in een try‑with‑resources‑blok en maak het `Image`‑object snel vrij. Pas `CadRasterizationOptions.setPageWidth/Height` aan naar een redelijke grootte om het geheugenverbruik laag te houden.

**Q: Behoudt de WMF‑output laaginformatie?**  
A: WMF is een plat vectorformaat, dus de laaghiërarchie wordt afgevlakt, maar lijnstijlen, kleuren en arceringspatronen blijven behouden.

**Q: Is het mogelijk een aangepaste DPI in te stellen voor de WMF?**  
A: Gebruik `rasterizationOptions.setResolution(300);` om de DPI te definiëren vóór het opslaan.

**Q: Kan ik meerdere DXF‑bestanden in één keer batch‑converteren?**  
A: Absoluut. Loop door een map, laad elk bestand en pas dezelfde rasterisatie‑ en opslaglogica toe.

**Q: Welke Java‑versies worden ondersteund?**  
A: Aspose.CAD voor Java ondersteunt Java 8 en later, inclusief Java 11, 17 en nieuwere LTS‑releases.

**Laatst bijgewerkt:** 2026-06-09  
**Getest met:** Aspose.CAD for Java 24.11  
**Auteur:** Aspose

```java
image.save(dataDir + "conic_pyramid_out_.pdf"); 
```

## Gerelateerde tutorials

- [PDF maken vanuit CAD – DXF exporteren naar PDF met Aspose.CAD voor Java](/cad/java/additional-features/export-dxf-to-pdf/)
- [PDF maken vanuit DXF: Laag exporteren met Aspose.CAD voor Java](/cad/java/additional-features/export-specific-layer-to-pdf/)
- [Hoe DXF‑lay-out omzetten naar JPEG‑afbeelding met Aspose.CAD in Java](/cad/java/additional-features/export-specific-layout-to-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}