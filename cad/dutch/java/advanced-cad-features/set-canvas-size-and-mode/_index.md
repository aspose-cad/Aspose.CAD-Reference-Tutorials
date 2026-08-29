---
date: 2026-08-29
description: Leer hoe u het PDF-paginaformaat instelt en CAD naar PDF converteert
  met Aspose.CAD voor Java, met automatische lay-outschaling en TIFF-export.
keywords:
- set pdf page size
- convert cad to pdf
- canvas size java
- high resolution tiff
- change pdf dimensions
lastmod: 2026-08-29
linktitle: PDF-paginaformaat instellen – CAD naar PDF converteren
og_description: Leer hoe u het PDF-paginaformaat instelt tijdens het converteren van
  CAD-tekeningen naar PDF in Java met Aspose.CAD. Deze gids behandelt canvasafmetingen,
  automatische lay-outschaling en export naar hoge‑resolutie TIFF.
og_image_alt: Tutorial showing how to set pdf page size and convert CAD to PDF in
  Java
og_title: PDF-paginaformaat instellen – CAD naar PDF converteren met Aspose in Java
schemas:
- author: Aspose
  dateModified: '2026-08-29'
  description: Learn how to set pdf page size and convert CAD to PDF using Aspose.CAD
    for Java, with automatic layout scaling and TIFF export.
  headline: Set pdf page size – convert cad to pdf (Java)
  type: TechArticle
- questions:
  - answer: No. Canvas size controls page dimensions; vector data remains resolution‑independent,
      ensuring crisp rendering at any zoom level.
    question: does the canvas size affect vector quality in the PDF?
  - answer: Yes. Adjust `rasterizationOptions.setResolution(dpiValue)` before creating
      `TiffOptions`.
    question: can I set a different DPI for the TIFF output?
  - answer: Use Aspose.PDF to load the generated PDF and call `pdf.getPages().setPageSize(PageSize.A4)`
      or a custom size.
    question: how can I change PDF dimensions for an existing PDF without re‑rendering
      the CAD?
  - answer: Keep `setAutomaticLayoutsScaling(true)` and avoid `setNoScaling(true)`;
      this retains layer visibility and layout fidelity.
    question: what is the best way to convert dxf to pdf while preserving layers?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- set pdf page size
- convert cad
- Aspose.CAD
- Java
- high resolution tiff
title: PDF-paginaformaat instellen – CAD naar PDF converteren (Java)
url: /nl/java/advanced-cad-features/set-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Instellen pdf-paginaformaat – CAD naar pdf converteren (Java)

## Inleiding

Als je **pdf-paginaformaat wilt instellen** tijdens het converteren van CAD-tekeningen naar PDF, ben je op de juiste plek. In deze tutorial laten we zien hoe je Aspose.CAD voor Java kunt gebruiken om exacte canvasafmetingen te definiëren, automatische lay-outschaling in te schakelen en vervolgens het resultaat zowel naar PDF als TIFF te exporteren. Of je nu technische schema's voorbereidt voor afdrukken of miniaturen genereert voor een webgalerij, het beheersen van de paginagrootte en de uitvoerresolutie is essentieel.

## Snelle antwoorden
- **Wat betekent “CAD naar PDF converteren”?** Het omzetten van een CAD-tekening (bijv. DXF, DWG) naar een PDF-document dat op elk platform kan worden bekeken.  
- **Kan ik ook exporteren naar TIFF?** Ja—gebruik `TiffOptions` om hoge‑resolutie rasterafbeeldingen te maken.  
- **Welke optie regelt de canvasgrootte in Java?** `CadRasterizationOptions.setPageWidth/Height`.  
- **Wat is automatische lay-outschaling?** Een vlag (`setAutomaticLayoutsScaling(true)`) die de oorspronkelijke lay-outverhoudingen behoudt wanneer de canvasgrootte verandert.  
- **Heb ik een licentie nodig voor Aspose.CAD?** Een tijdelijke of permanente licentie is vereist voor productiegebruik.

## Hoe pdf-paginaformaat in te stellen bij het converteren van CAD naar PDF in Java

Laad je CAD‑bestand, configureer `CadRasterizationOptions` met de gewenste breedte en hoogte, schakel automatische lay-outschaling in en sla vervolgens het resultaat op als PDF. Deze twee‑stappenbenadering stelt je in staat de exacte afmetingen van de uitvoerpagina te beheersen zonder concessies te doen aan de vectorkwaliteit.

## Wat betekent CAD naar PDF converteren?

Het converteren van CAD naar PDF houdt in dat vector‑gebaseerde technische tekeningen worden gerenderd als PDF‑pagina's, waarbij lijnwerk, lagen en geometrie behouden blijven terwijl het bestand universeel toegankelijk wordt gemaakt. Het proces rastert de tekening volgens de opgegeven opties, waardoor een PDF ontstaat die op elk apparaat kan worden geopend zonder CAD‑software, en behoudt de visuele getrouwheid van het oorspronkelijke ontwerp.

## Waarom canvasgrootte instellen in Java?

Het instellen van de canvasgrootte in Java laat je de uitvoerresolutie en paginagrootte definiëren, zodat de resulterende PDF of TIFF voldoet aan je afdruk‑ of weergave‑eisen. Het geeft ook controle over het schaalgedrag, wat essentieel is voor tekeningen op groot formaat.

## Vereisten

- Aspose.CAD voor Java: Zorg ervoor dat je de Aspose.CAD‑bibliotheek hebt geïnstalleerd in je Java‑omgeving. Je kunt de Aspose.CAD voor Java‑bibliotheek [hier](https://releases.aspose.com/cad/java/) downloaden.  
- Documentdirectory: Maak een documentdirectory aan om je CAD‑bestanden op te slaan. Deze directory wordt in de tutorialstappen gebruikt.

Laten we nu beginnen met de stap‑voor‑stap gids.

## Namespaces importeren

In deze stap importeren we de benodigde namespaces om je Aspose.CAD‑project op te starten.

`Image` is de hoofdklasse die wordt gebruikt om CAD‑bestanden te laden.

```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## Stap 1: Aspose.CAD-klassen importeren

De `Image`‑klasse biedt methoden om CAD‑tekeningen te laden en op te slaan.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

In dit fragment stellen we het pad naar de resource‑directory in en laden we een DXF‑bestand met behulp van de `Image`‑klasse van Aspose.CAD.

## Stap 2: CadRasterizationOptions-eigenschappen instellen (canvasgrootte java)

`CadRasterizationOptions` specificeert rasterisatie‑instellingen zoals paginagrootte en schaal voor CAD‑naar‑raster conversie.

```java
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

Hier maken we een instantie van `CadRasterizationOptions` en configureren we eigenschappen zoals pagina‑breedte, pagina‑hoogte en **automatische lay-outschaling**. Dit is de kern van **configure canvas mode** voor je conversie.

## Stap 3: PdfOptions maken en vectorRasterizationOptions instellen

`PdfOptions` definieert PDF‑uitvoerinstellingen voor de conversie.

```java
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Set the VectorRasterizationOptions property
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Nu maken we een `PdfOptions`‑instantie en stellen we de eigenschap `VectorRasterizationOptions` in op de eerder geconfigureerde `CadRasterizationOptions`.

## Stap 4: exporteren naar PDF (CAD naar PDF converteren)

```java
// Export CAD to PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

Tot slot slaan we de CAD‑afbeelding op als PDF‑bestand met de opgegeven opties, waarmee het **CAD naar PDF converteren** proces voltooid is.

## Stap 5: TiffOptions maken en vectorRasterizationOptions instellen (CAD naar TIFF exporteren)

`TiffOptions` configureert TIFF‑uitvoerparameters zoals compressie en resolutie.

```java
// Create an instance of TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Set the VectorRasterizationOptions property
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Stap 6: exporteren naar TIFF

```java
// Export CAD to TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

Tot slot slaan we de CAD‑afbeelding op als TIFF‑bestand met de opgegeven opties, waarmee wordt aangetoond hoe je **CAD naar TIFF kunt exporteren** na het configureren van de canvasgrootte.

## Veelvoorkomende problemen en oplossingen

| Probleem | Oorzaak | Oplossing |
|----------|---------|-----------|
| Uitvoer‑PDF is leeg | `setNoScaling(true)` schakelt rendering uit voor sommige tekeningen | Verwijder `setNoScaling(true)` of stel het in op `false`. |
| TIFF‑resolutie ziet er laag uit | Pagina breedte/hoogte te klein | Verhoog de waarden van `setPageWidth` / `setPageHeight`. |
| Lay‑out ziet er vervormd uit | Automatische lay‑outschaling uitgeschakeld | Zorg ervoor dat `setAutomaticLayoutsScaling(true)` is ingeschakeld. |

## Waarom canvasgrootte en DPI aanpassen?

Het aanpassen van de canvasgrootte beïnvloedt direct de rasterisatie‑resolutie van de uitvoer. Als je de **TIFF‑resolutie wilt verhogen**, verhoog dan simpelweg de `setPageWidth` / `setPageHeight` waarden of roep `rasterizationOptions.setResolution(300)` aan voordat je `TiffOptions` maakt. Dit levert rasterafbeeldingen van hoge kwaliteit die geschikt zijn voor afdrukken of gedetailleerde inspectie.

## Veelgestelde vragen

**Q1: kan ik Aspose.CAD voor Java gebruiken met andere Java‑frameworks?**  
A: Ja, Aspose.CAD is ontworpen om naadloos te integreren met verschillende Java‑frameworks.

**Q2: is er een tijdelijke licentie beschikbaar voor Aspose.CAD?**  
A: Ja, je kunt een tijdelijke licentiepagina [hier](https://purchase.aspose.com/temporary-license/) verkrijgen.

**Q3: waar kan ik community‑ondersteuning krijgen voor Aspose.CAD?**  
A: Bezoek het Aspose.CAD‑forum [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) voor community‑ondersteuning en discussies.

**Q4: kan ik Aspose.CAD gratis proberen?**  
A: Absoluut! Download een gratis proefversie via de pagina [hier](https://releases.aspose.com/).

**Q5: hoe koop ik Aspose.CAD voor Java?**  
A: Koop Aspose.CAD voor Java via [hier](https://purchase.aspose.com/buy).

**Q: beïnvloedt de canvasgrootte de vectorkwaliteit in de PDF?**  
A: Nee. Canvasgrootte bepaalt de paginagrootte; vectorgegevens blijven resolutie‑onafhankelijk, waardoor ze scherp blijven bij elke zoom.

**Q: kan ik een andere DPI instellen voor de TIFF‑uitvoer?**  
A: Ja. Pas `rasterizationOptions.setResolution(dpiValue)` aan voordat je `TiffOptions` maakt.

**Q: hoe kan ik PDF‑afmetingen wijzigen voor een bestaande PDF zonder de CAD opnieuw te renderen?**  
A: Gebruik Aspose.PDF om de gegenereerde PDF te laden en roep `pdf.getPages().setPageSize(PageSize.A4)` of een aangepaste grootte aan.

**Q: wat is de beste manier om dxf naar pdf te converteren terwijl lagen behouden blijven?**  
A: Houd `setAutomaticLayoutsScaling(true)` ingeschakeld en vermijd `setNoScaling(true)`; dit behoudt de zichtbaarheid van lagen en lay‑outfidelity.

## Conclusie

Gefeliciteerd! Je hebt met succes **CAD naar PDF geconverteerd** en **CAD naar TIFF geëxporteerd** terwijl je **canvasgrootte in Java hebt ingesteld**, automatische lay‑outschaling hebt ingeschakeld, en geleerd hoe je **canvas‑modus kunt configureren** voor uitvoer van hoge kwaliteit. Deze tutorial biedt een solide basis voor je CAD‑conversieprojecten. Ontdek meer functies en mogelijkheden in de [Aspose.CAD-documentatie](https://reference.aspose.com/cad/java/).

---

**Laatst bijgewerkt:** 2026-08-29  
**Getest met:** Aspose.CAD for Java 24.12  
**Auteur:** Aspose

## Gerelateerde tutorials

- [Canvasgrootte instellen – Geavanceerde CAD-functies met Aspose.CAD voor Java](/cad/java/advanced-cad-features/)
- [DWG exporteren naar PDF in Java – PDF-paginaformaat instellen met Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)
- [Aangepaste paginagrootte instellen – PDF vanuit CAD met automatische lay‑outschaling](/cad/java/advanced-cad-features/setting-auto-layout-scaling/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}