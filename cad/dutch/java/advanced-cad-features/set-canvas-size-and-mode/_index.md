---
date: 2025-12-10
description: Leer hoe u CAD naar PDF kunt converteren met Aspose.CAD voor Java, terwijl
  u de canvasgrootte instelt, automatische lay-outschaling toepast en exporteert naar
  TIFF.
linktitle: Convert CAD to PDF – Set Canvas Size & Mode
second_title: Aspose.CAD Java API
title: CAD naar PDF converteren – Canvasgrootte en modus instellen (Java)
url: /nl/java/advanced-cad-features/set-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Stel Canvasgrootte en Modus in

## Introductie

Zoek je een manier om **CAD naar PDF te converteren** terwijl je volledige controle hebt over de canvasgrootte en rendermodus? Deze uitgebreide gids leidt je stap voor stap door het instellen van de canvasgrootte in Java, het inschakelen van automatische lay-outschaling, en vervolgens het exporteren van het resultaat naar zowel PDF- als TIFF-formaten met Aspose.CAD. Of je nu een productie‑pipeline verfijnt of experimenteert met een prototype, je vindt hier duidelijke, bruikbare instructies.

## Snelle Antwoorden
- **Wat betekent “CAD naar PDF converteren”?** Het omzetten van een CAD‑tekening (bijv. DXF, DWG) naar een PDF‑document dat op elk platform kan worden bekeken.  
- **Kan ik ook exporteren naar TIFF?** Ja—gebruik `TiffOptions` om hoge‑resolutie rasterafbeeldingen te maken.  
- **Welke optie regelt de canvasgrootte in Java?** `CadRasterizationOptions.setPageWidth/Height`.  
- **Wat is automatische lay-outschaling?** Een vlag (`setAutomaticLayoutsScaling(true)`) die de oorspronkelijke lay‑outverhoudingen behoudt wanneer de canvasgrootte verandert.  
- **Heb ik een licentie nodig voor Aspose.CAD?** Een tijdelijke of permanente licentie is vereist voor productiegebruik.

## Wat is **CAD naar PDF converteren**?

Het converteren van CAD naar PDF betekent dat vector‑gebaseerde technische tekeningen worden gerenderd als PDF‑pagina's, waarbij lijnwerk, lagen en geometrie behouden blijven terwijl het bestand universeel toegankelijk wordt gemaakt.

## Waarom canvasgrootte instellen **java**?

Het instellen van de canvasgrootte in Java laat je de uitvoerresolutie en paginagrootte definiëren, zodat de resulterende PDF of TIFF voldoet aan je druk‑ of weergave‑eisen. Het geeft je ook controle over het schaalgedrag, wat essentieel is voor grote tekeningen.

## Vereisten

Voordat je aan de tutorial begint, zorg dat je de volgende vereisten hebt:

- Aspose.CAD voor Java: Zorg ervoor dat de Aspose.CAD‑bibliotheek is geïnstalleerd in je Java‑omgeving. Je kunt het downloaden [hier](https://releases.aspose.com/cad/java/).

- Documentdirectory: Maak een documentdirectory aan om je CAD‑bestanden op te slaan. Deze directory wordt in de tutorialstappen gebruikt.

Laten we nu beginnen met de stap‑voor‑stap‑gids.

## Namespaces importeren

In deze stap importeren we de benodigde namespaces om je Aspose.CAD‑project te starten.

```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## Stap 1: Aspose.CAD‑klassen importeren

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

In dit fragment stellen we het pad naar de resource‑directory in en laden we een DXF‑bestand met de `Image`‑klasse van Aspose.CAD.

## Stap 2: **CadRasterizationOptions**‑eigenschappen instellen (canvasgrootte java)

```java
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

Hier maken we een instantie van `CadRasterizationOptions` en configureren we eigenschappen zoals paginabreedte, paginahoogte en **automatische lay‑outschaling**. Dit is de kern van **canvasmodus configureren** voor je conversie.

## Stap 3: PdfOptions maken en VectorRasterizationOptions instellen

```java
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Set the VectorRasterizationOptions property
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Nu maken we een `PdfOptions`‑instantie en stellen we de eigenschap `VectorRasterizationOptions` in op de eerder geconfigureerde `CadRasterizationOptions`.

## Stap 4: Exporteren naar PDF (cad naar pdf converteren)

```java
// Export CAD to PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

Tot slot slaan we de CAD‑afbeelding op als PDF‑bestand met de opgegeven opties, waarmee het **CAD naar PDF converteren** proces voltooid is.

## Stap 5: TiffOptions maken en VectorRasterizationOptions instellen (cad naar tiff exporteren)

```java
// Create an instance of TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Set the VectorRasterizationOptions property
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

In deze stap maken we een `TiffOptions`‑instantie en configureren we de eigenschap `VectorRasterizationOptions`.

## Stap 6: Exporteren naar TIFF

```java
// Export CAD to TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

Tot slot slaan we de CAD‑afbeelding op als TIFF‑bestand met de opgegeven opties, waarmee wordt aangetoond hoe je **CAD naar TIFF exporteert** na het configureren van de canvasgrootte.

## Veelvoorkomende problemen en oplossingen

| Probleem | Oorzaak | Oplossing |
|----------|---------|-----------|
| Uitvoer‑PDF is leeg | `setNoScaling(true)` schakelt rendering uit voor sommige tekeningen | Verwijder `setNoScaling(true)` of stel het in op `false`. |
| TIFF‑resolutie lijkt laag | Paginabreedte/hoogte te klein | Verhoog de waarden van `setPageWidth` / `setPageHeight`. |
| Lay‑out ziet er vervormd uit | Automatische lay‑outschaling uitgeschakeld | Zorg ervoor dat `setAutomaticLayoutsScaling(true)` is ingeschakeld. |

## Conclusie

Gefeliciteerd! Je hebt met succes **CAD naar PDF geconverteerd** en **CAD naar TIFF geëxporteerd** terwijl je **canvasgrootte java** hebt ingesteld, **automatische lay‑outschaling** hebt ingeschakeld, en hebt geleerd hoe je **canvasmodus configureert** voor hoogwaardige uitvoer. Deze tutorial biedt een solide basis voor je CAD‑conversieprojecten. Ontdek meer functies en mogelijkheden in de [Aspose.CAD‑documentatie](https://reference.aspose.com/cad/java/).

## Veelgestelde vragen

### Q1: Kun ik Aspose.CAD voor Java gebruiken met andere Java‑frameworks?

A1: Ja, Aspose.CAD is ontworpen om naadloos te integreren met verschillende Java‑frameworks.

### Q2: Is er een tijdelijke licentie beschikbaar voor Aspose.CAD?

A2: Ja, je kunt een tijdelijke licentie verkrijgen [hier](https://purchase.aspose.com/temporary-license/).

### Q3: Waar kan ik community‑ondersteuning vinden voor Aspose.CAD?

A3: Bezoek het [Aspose.CAD‑forum](https://forum.aspose.com/c/cad/19) voor community‑ondersteuning en discussies.

### Q4: Kan ik Aspose.CAD gratis uitproberen?

A4: Absoluut! Vraag een gratis proefversie aan [hier](https://releases.aspose.com/).

### Q5: Hoe koop ik Aspose.CAD voor Java?

A5: Koop het product [hier](https://purchase.aspose.com/buy).

**Aanvullende V&A**

**V: Heeft de canvasgrootte invloed op de vectorkwaliteit in de PDF?**  
**A:** Nee. De canvasgrootte bepaalt de paginagrootte; vectorgegevens blijven resolutie‑onafhankelijk, waardoor ze scherp blijven bij elke zoomniveau.

**V: Kan ik een andere DPI instellen voor de TIFF‑output?**  
**A:** Ja. Pas `rasterizationOptions.setResolution(dpiValue)` aan voordat je `TiffOptions` maakt.

---

**Laatst bijgewerkt:** 2025-12-10  
**Getest met:** Aspose.CAD voor Java 24.12  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}