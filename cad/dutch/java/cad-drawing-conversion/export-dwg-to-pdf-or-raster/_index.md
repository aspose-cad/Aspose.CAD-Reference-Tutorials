---
date: 2026-10-14
description: Leer hoe de Java CAD-bibliotheek Aspose.CAD voor Java DWG snel en nauwkeurig
  kan exporteren naar PDF of rasterafbeeldingen.
keywords:
- export dwg pdf
- high quality pdf
- dwg to pdf tutorial
- aspose cad java
- java cad library
lastmod: 2026-10-14
linktitle: DWG, PDF en rasterafbeeldingen exporteren
og_description: Exporteer DWG PDF snel met Aspose.CAD voor Java. Leer over hoogwaardige
  PDF-conversie, rasteropties en licenties in deze stapsgewijze handleiding.
og_image_alt: Tutorial showing Java code to convert DWG drawings to PDF and raster
  formats with Aspose.CAD
og_title: DWG, PDF en rasterafbeeldingen exporteren met Java CAD-bibliotheek Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-10-14'
  description: Learn how the Java CAD library Aspose.CAD for Java can export DWG to
    PDF or raster images quickly and accurately.
  headline: Export DWG PDF and raster images using Java CAD library Aspose.CAD
  type: TechArticle
- description: Learn how the Java CAD library Aspose.CAD for Java can export DWG to
    PDF or raster images quickly and accurately.
  name: Export DWG PDF and raster images using Java CAD library Aspose.CAD
  steps:
  - name: Load the DWG file
    text: First, load your DWG drawing using the `Image` class. This creates an in‑memory
      representation that Aspose.CAD can work with.
  - name: Determine unit type
    text: Understanding whether the drawing uses metric or imperial units is essential
      for correct scaling. The helper method `IsMetric` (implementation omitted for
      brevity) returns a boolean flag.
  - name: Set rasterization options
    text: The `CadRasterizationOptions` class defines rasterization parameters such
      as DPI, page size, and unit conversion. Based on the unit system, configure
      page size, scaling, and the target unit type. These options drive how the DWG
      is rasterized before being wrapped into a PDF.
  - name: Configure PDF options (pdf options cad)
    text: The `PdfOptions` class specifies PDF‑specific settings, including compression
      and metadata. Create a `PdfOptions` instance and attach the rasterization settings.
      This tells Aspose.CAD how to embed the rasterized content into the final PDF.
  - name: Save as PDF
    text: The `save` method writes the image to the given file path using the supplied
      options. Finally, export the drawing to a PDF file. The `save` method takes
      the output path and the configured `PdfOptions`. When the code finishes, you’ll
      find **Saved.pdf** in your `DWGDrawings` folder, ready for distribu
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD for Java seamlessly integrates with popular Java frameworks
      such as Spring, Jakarta EE, and Android.
    question: Can I use Aspose.CAD for Java with other Java frameworks?
  - answer: Yes, you can obtain a temporary license **[obtain a temporary license](https://purchase.aspose.com/temporary-license/)**.
    question: Is a temporary license available for Aspose.CAD for Java?
  - answer: Visit the **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)** for
      assistance from the community and Aspose engineers.
    question: Where can I find support for Aspose.CAD for Java?
  - answer: You can purchase a license **[purchase a license](https://purchase.aspose.com/buy)**.
    question: How can I purchase a license for Aspose.CAD for Java?
  - answer: Aspose.CAD for Java supports both metric and imperial units, automatically
      detecting the drawing’s unit system.
    question: What units does Aspose.CAD for Java support?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- export dwg
- aspose.cad
- java cad conversion
title: DWG, PDF en rasterafbeeldingen exporteren met Java CAD-bibliotheek Aspose.CAD
url: /nl/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export DWG PDF en rasterafbeeldingen met Java CAD-bibliotheek Aspose.CAD

## Introductie

Het exporteren van DWG naar PDF is een veelvoorkomende eis voor ingenieurs, architecten en iedereen die CAD‑tekeningen wil delen zonder het oorspronkelijke bestandsformaat bloot te stellen. Met **Aspose.CAD for Java** kun je **export dwg pdf** — of rasterafbeeldingen — in slechts een paar regels Java‑code, waarbij vectorfidelity en lay‑outprecisie behouden blijven. Deze tutorial leidt je door het laden van een DWG‑bestand, het configureren van rasterisatie en het opslaan van het resultaat als een PDF of afbeelding van hoge kwaliteit. Je ziet ook waarom Aspose.CAD de voorkeurs‑Java‑CAD‑bibliotheek is voor betrouwbare, cross‑platform conversie.

Voor een gerichte gids over alleen PDF‑conversie, zie de [Export DWG to PDF tutorial](/java/cad-drawing-conversion/export-dwg-to-pdf/).

## Snelle antwoorden
- **Waar gaat deze tutorial over?** DWG‑bestanden exporteren naar PDF of rasterafbeeldingen met Aspose.CAD for Java.  
- **Heb ik een licentie nodig?** Er is een gratis tijdelijke licentie beschikbaar voor evaluatie; een volledige licentie is vereist voor productie.  
- **Welke Java‑versie wordt ondersteund?** Elke Java 8+ runtime werkt met de nieuwste Aspose.CAD Java API.  
- **Kan ik DWG naar andere afbeeldingsformaten converteren?** Ja – dezelfde rasterisatie‑opties laten je PNG, JPEG, BMP, enz. exporteren.  
- **Hoe lang duurt de conversie?** Meestal minder dan een seconde voor standaardtekeningen; grotere bestanden kunnen enkele seconden duren.

## Waarom Java CAD‑bibliotheek de beste keuze is voor DWG‑conversie?

Aspose.CAD for Java is de beste keuze omdat het een pure‑Java‑implementatie biedt die geen native DLL's vereist, automatisch metrische of imperiale eenheden detecteert, rasteroutput levert tot 1200 DPI, en vector‑behoudende PDF's genereert zonder externe afhankelijkheden. De bibliotheek biedt ook een flexibel licentiemodel waarmee je kunt beginnen met een tijdelijke licentie en kunt opschalen naar enterprise‑gebruik.

## Wat is “export dwg to pdf”?

`Export dwg pdf` is het proces van het converteren van een native DWG‑tekeningsbestand naar een PDF‑document, waarbij vectorgegevens, lagen en schaal behouden blijven. Deze conversie produceert een apparaat‑onafhankelijk bestand dat op elk platform kan worden bekeken zonder AutoCAD. Omdat de PDF vectorinformatie behoudt, blijft tekst doorzoekbaar en blijven grafische elementen scherp op elk zoomniveau, wat het ideaal maakt voor documentatie, klantbeoordeling en archivering.

## Waarom Aspose.CAD Java gebruiken voor deze conversie?

Je moet Aspose.CAD Java gebruiken omdat de bibliotheek intern eenheidsconversie, rasterisatie en PDF‑inbedding afhandelt, waardoor de noodzaak voor tools van derden of complexe command‑line‑pijplijnen wegvalt. De API is ontworpen voor ontwikkelaars: een enkel `Image`‑object vertegenwoordigt de tekening, en enkele configuratie‑objecten laten je DPI, paginagrootte en compressie fijn afstellen. Het resultaat is consistente, herhaalbare output op Windows-, Linux- en macOS‑omgevingen.

## Vereisten

Voordat je in de code duikt, zorg dat je het volgende hebt:

- Basiskennis van Java‑programmeren.  
- Aspose.CAD for Java‑bibliotheek geïnstalleerd. Als je deze nog niet hebt gedownload, haal hem op via **[download Aspose.CAD for Java](https://releases.aspose.com/cad/java/)**.  
- Een DWG‑bestand voor testen – de voorbeeld **Bottom_plate.dwg** wordt in deze gids gebruikt.

## Import namespaces

In je Java‑project importeer je de benodigde klassen om de conversie op gang te brengen:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## Stapsgewijze handleiding

### Stap 1: Laad het DWG‑bestand

Laad eerst je DWG‑tekening met de `Image`‑klasse. Dit creëert een in‑memory representatie waar Aspose.CAD mee kan werken.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

### Stap 2: Bepaal eenheidstype

Begrijpen of de tekening metrische of imperiale eenheden gebruikt is essentieel voor correcte schaal. De hulpmethode `IsMetric` (implementatie weggelaten voor beknoptheid) retourneert een boolean‑waarde.

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

### Stap 3: Stel rasterisatie‑opties in

De `CadRasterizationOptions`‑klasse definieert rasterisatie‑parameters zoals DPI, paginagrootte en eenheidsconversie. Op basis van het eenhedensysteem configureer je paginagrootte, schaal en het doel‑eenheidstype. Deze opties bepalen hoe de DWG wordt gerasterd voordat deze in een PDF wordt verpakt.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();

if (currentUnitIsMetric) {
    // Metric units
    double metersCoeff = 1 / 1000.0;
    double scaleFactor = metersCoeff / currentUnitCoefficient;
    rasterizationOptions.setPageWidth((float)(210 * scaleFactor));
    rasterizationOptions.setPageHeight((float)(297 * scaleFactor));
    rasterizationOptions.setUnitType(UnitType.Millimeter);
} else {
    // Imperial units
    rasterizationOptions.setPageWidth((float)(8.27f / currentUnitCoefficient));
    rasterizationOptions.setPageHeight((float)(11.69f / currentUnitCoefficient));
    rasterizationOptions.setUnitType(UnitType.Inch);
}
```

### Stap 4: Configureer PDF‑opties (pdf options cad)

De `PdfOptions`‑klasse specificeert PDF‑specifieke instellingen, waaronder compressie en metadata. Maak een `PdfOptions`‑instantie aan en koppel de rasterisatie‑instellingen. Dit vertelt Aspose.CAD hoe de gerasterde inhoud in de uiteindelijke PDF moet worden ingebed.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

### Stap 5: Opslaan als PDF

De `save`‑methode schrijft de afbeelding naar het opgegeven bestandspad met de meegegeven opties. Exporteer tenslotte de tekening naar een PDF‑bestand. De `save`‑methode neemt het uitvoerpad en de geconfigureerde `PdfOptions`.

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

Wanneer de code klaar is, vind je **Saved.pdf** in je `DWGDrawings`‑map, klaar voor distributie of archivering.

## Hoe DWG‑rasterafbeeldingen te converteren met Java CAD‑bibliotheek?

Je kunt DWG naar rasterformaten converteren door `PdfOptions` te vervangen door een raster‑specifieke opties‑klasse zoals `PngOptions` of `JpegOptions`. Hergebruik dezelfde `CadRasterizationOptions`‑instantie, pas het uitvoerformaat aan en roep de `save`‑methode aan met het nieuwe opties‑object. Deze aanpak stelt je in staat PNG, JPEG, BMP of TIFF‑bestanden te genereren met één regel wijziging, waardoor de workflow consistent blijft.

## Hoe PDF‑DWG te genereren met PDF‑opties CAD?

Het bovenstaande voorbeeld **genereert pdf dwg**‑output al. Om de PDF‑grootte fijn af te stellen, schakel compressie in door `pdfOptions.setCompress(true)` aan te roepen. Je kunt ook aangepaste metadata insluiten, de PDF‑versie instellen of wachtwoordbeveiliging toevoegen via extra `PdfOptions`‑eigenschappen. Deze aanpassingen geven je volledige controle over de uiteindelijke PDF zonder de Java‑code te verlaten.

## Veelvoorkomende problemen & tips

- **Onjuiste paginagrootte** – Controleer de eenheidsconversielogica; niet‑overeenkomende coëfficiënten kunnen te grote pagina's opleveren.  
- **Ontbrekende lettertypen of lijndiktes** – Zorg ervoor dat de DWG eventuele externe bronnen verwijst vóór conversie.  
- **Prestaties bij grote tekeningen** – Verhoog de `DPI`‑instelling in `CadRasterizationOptions` alleen wanneer hogere kwaliteit vereist is; een lagere DPI versnelt de verwerking.  
- **Licentie‑zorgen** – Voor evaluatie kun je een **temporary license Aspose** gebruiken; een volledige licentie is vereist voor productie‑implementaties.

## Veelgestelde vragen

**Q: Kan ik Aspose.CAD for Java gebruiken met andere Java‑frameworks?**  
A: Ja, Aspose.CAD for Java integreert naadloos met populaire Java‑frameworks zoals Spring, Jakarta EE en Android.

**Q: Is er een tijdelijke licentie beschikbaar voor Aspose.CAD for Java?**  
A: Ja, je kunt een tijdelijke licentie verkrijgen **[obtain a temporary license](https://purchase.aspose.com/temporary-license/)**.

**Q: Waar kan ik ondersteuning vinden voor Aspose.CAD for Java?**  
A: Bezoek het **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)** voor hulp van de community en Aspose‑engineers.

**Q: Hoe kan ik een licentie kopen voor Aspose.CAD for Java?**  
A: Je kunt een licentie aanschaffen via **[purchase a license](https://purchase.aspose.com/buy)**.

**Q: Welke eenheden ondersteunt Aspose.CAD for Java?**  
A: Aspose.CAD for Java ondersteunt zowel metrische als imperiale eenheden en detecteert automatisch het eenheidssysteem van de tekening.

**Q: Kan ik DWG naar andere afbeeldingsformaten converteren (bijv. PNG, JPEG) met dezelfde API?**  
A: Absoluut. Vervang `PdfOptions` door de juiste raster‑afbeeldingsopties (bijv. `PngOptions`) en hergebruik dezelfde `CadRasterizationOptions`.

## Conclusie

Deze tutorial heeft laten zien hoe je **export dwg pdf** en rasterafbeeldingen kunt gebruiken met de **java cad library** Aspose.CAD for Java. Door de stapsgewijze handleiding te volgen, kun je betrouwbare CAD‑conversie integreren in elke Java‑applicatie, of je nu PDF's nodig hebt voor documentatie of rasterafbeeldingen voor weergave op het web. De pure‑Java‑aard van de bibliotheek, de hoogwaardige output en het flexibele licentiemodel maken het een solide keuze voor zowel kleine hulpprogramma's als grootschalige enterprise‑pijplijnen.

---

**Laatst bijgewerkt:** 2026-10-14  
**Getest met:** Aspose.CAD for Java 24.10  
**Auteur:** Aspose

## Gerelateerde tutorials

- [Export DWG naar PDF: Specifieke lay-out met Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Export DWG naar PDF in Java – Stel PDF-paginagrootte in met Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)
- [Export DWG naar PDF met verborgen lijnen – Aspose.CAD for Java](/cad/java/cad-text-and-formatting/support-hidden-lines-in-dwg/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}