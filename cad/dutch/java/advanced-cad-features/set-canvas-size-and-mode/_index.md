---
date: 2026-02-15
description: Leer hoe u de PDF-paginaformaat instelt en CAD naar PDF converteert met
  Aspose.CAD voor Java, met automatische lay-outschaling en TIFF-export.
linktitle: Set PDF Page Size – Convert CAD to PDF
second_title: Aspose.CAD Java API
title: PDF-paginagrootte instellen – CAD naar PDF converteren (Java)
url: /nl/java/advanced-cad-features/set-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Canvasgrootte en -modus instellen

## Inleiding

Als je **PDF-paginagrootte** moet instellen tijdens het converteren van CAD-tekeningen naar PDF, ben je hier aan het juiste adres. In deze tutorial laten we zien hoe je Aspose.CAD for Java gebruikt om exacte canvasafmetingen te definiëren, automatische lay-outschaling in te schakelen en vervolgens het resultaat zowel naar PDF als TIFF te exporteren. Of je nu technische schema's voorbereidt voor afdrukken of miniaturen genereert voor een webgalerij, het beheersen van de paginagrootte en uitvoerresolutie is essentieel.

## Snelle antwoorden
- **Wat betekent “convert CAD to PDF”?** Het omzetten van een CAD-tekening (bijv. DXF, DWG) naar een PDF‑document dat op elk platform kan worden bekeken.  
- **Kan ik ook exporteren naar TIFF?** Ja—gebruik `TiffOptions` om rasterafbeeldingen met hoge resolutie te maken.  
- **Welke optie regelt de canvasgrootte in Java?** `CadRasterizationOptions.setPageWidth/Height`.  
- **Wat is automatische lay-outschaling?** Een vlag (`setAutomaticLayoutsScaling(true)`) die de oorspronkelijke lay-outverhoudingen behoudt wanneer de canvasgrootte verandert.  
- **Heb ik een licentie nodig voor Aspose.CAD?** Een tijdelijke of permanente licentie is vereist voor productiegebruik.

## Hoe PDF-paginagrootte in te stellen bij het converteren van CAD naar PDF (Java)

Het instellen van de PDF-paginagrootte (of canvasgrootte) stelt je in staat de uiteindelijke afmetingen van het document te bepalen, wat vooral nuttig is wanneer je **PDF-afmetingen moet wijzigen** om te voldoen aan drukstandaarden of UI‑vereisten. Hieronder lopen we elke stap door en leggen we het *waarom* achter elke regel code uit.

## Wat is **convert CAD to PDF**?

Converteren van CAD naar PDF betekent dat je vector‑gebaseerde technische tekeningen rendert als PDF‑pagina's, waarbij lijnwerk, lagen en geometrie behouden blijven terwijl het bestand universeel toegankelijk wordt.

## Waarom canvasgrootte **java** instellen?

Het instellen van de canvasgrootte in Java laat je de uitvoerresolutie en paginagrootte definiëren, zodat de resulterende PDF of TIFF voldoet aan je druk‑ of weergave‑eisen. Het geeft je ook controle over het schaalgedrag, wat essentieel is voor tekeningen in groot formaat.

## Vereisten

Zorg ervoor dat je de volgende zaken klaar hebt staan voordat je aan de tutorial begint:

- Aspose.CAD for Java: Zorg ervoor dat de Aspose.CAD‑bibliotheek is geïnstalleerd in je Java‑omgeving. Je kunt deze downloaden [hier](https://releases.aspose.com/cad/java/).
- Documentdirectory: Maak een documentdirectory aan om je CAD‑bestanden op te slaan. Deze directory wordt in de tutorialstappen gebruikt.

Laten we nu beginnen met de stap‑voor‑stap‑gids.

## Import Namespaces

In deze stap importeren we de benodigde namespaces om je Aspose.CAD‑project op te starten.

```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## Stap 1: Import Aspose.CAD‑klassen

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

In dit fragment stellen we het pad naar de resource‑directory in en laden we een DXF‑bestand met behulp van de `Image`‑klasse van Aspose.CAD.

## Stap 2: **CadRasterizationOptions**‑eigenschappen instellen (set canvas size java)

```java
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

Hier maken we een instantie van `CadRasterizationOptions` en configureren we eigenschappen zoals paginabreedte, paginahoogte en **automatic layout scaling**. Dit is de kern van **configure canvas mode** voor je conversie.

## Stap 3: PdfOptions maken en VectorRasterizationOptions instellen

```java
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Set the VectorRasterizationOptions property
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Nu maken we een `PdfOptions`‑instantie en stellen we de eigenschap `VectorRasterizationOptions` in op de eerder geconfigureerde `CadRasterizationOptions`.

## Stap 4: Exporteren naar PDF (convert cad to pdf)

```java
// Export CAD to PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

Tot slot slaan we de CAD‑afbeelding op als een PDF‑bestand met de opgegeven opties, waarmee het **convert CAD to PDF**‑proces wordt voltooid.

## Stap 5: TiffOptions maken en VectorRasterizationOptions instellen (export cad to tiff)

```java
// Create an instance of TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Set the VectorRasterizationOptions property
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

In deze stap configureren we een `TiffOptions`‑instantie en stellen we de eigenschap `VectorRasterizationOptions` in.

## Stap 6: Exporteren naar TIFF

```java
// Export CAD to TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

Tot slot slaan we de CAD‑afbeelding op als een TIFF‑bestand met de opgegeven opties, waarmee wordt aangetoond hoe je **export CAD to TIFF** kunt uitvoeren na het configureren van de canvasgrootte.

## Veelvoorkomende problemen en oplossingen

| Probleem | Oorzaak | Oplossing |
|----------|---------|-----------|
| Uitvoer‑PDF is leeg | `setNoScaling(true)` schakelt rendering uit voor sommige tekeningen | Verwijder `setNoScaling(true)` of stel het in op `false`. |
| TIFF‑resolutie is laag | Paginabreedte/-hoogte te klein | Verhoog de waarden van `setPageWidth` / `setPageHeight`. |
| Lay-out is vervormd | Automatische lay-outschaling uitgeschakeld | Zorg ervoor dat `setAutomaticLayoutsScaling(true)` is ingeschakeld. |

## Waarom canvasgrootte en DPI aanpassen?

Het wijzigen van de canvasgrootte beïnvloedt direct de rasterisatie‑resolutie van de uitvoer. Als je de **TIFF‑resolutie wilt verhogen**, vergroot je simpelweg de waarden van `setPageWidth` / `setPageHeight` of roep je `rasterizationOptions.setResolution(300)` aan voordat je de `TiffOptions` maakt. Dit levert rasterafbeeldingen van hoge kwaliteit die geschikt zijn voor afdrukken of gedetailleerde inspectie.

## Veelgestelde vragen

### Q1: Kan ik Aspose.CAD for Java gebruiken met andere Java‑frameworks?

A1: Ja, Aspose.CAD is ontworpen om naadloos te integreren met diverse Java‑frameworks.

### Q2: Is er een tijdelijke licentie beschikbaar voor Aspose.CAD?

A2: Ja, je kunt een tijdelijke licentie verkrijgen [hier](https://purchase.aspose.com/temporary-license/).

### Q3: Waar kan ik community‑ondersteuning vinden voor Aspose.CAD?

A3: Bezoek het [Aspose.CAD‑forum](https://forum.aspose.com/c/cad/19) voor community‑ondersteuning en discussies.

### Q4: Kan ik Aspose.CAD gratis uitproberen?

A4: Absoluut! Vraag een gratis proefversie aan [hier](https://releases.aspose.com/).

### Q5: Hoe koop ik Aspose.CAD for Java?

A5: Koop het product [hier](https://purchase.aspose.com/buy).

**Aanvullende Q&A**

**Q: Heeft de canvasgrootte invloed op de vectorkwaliteit in de PDF?**  
A: Nee. Canvasgrootte bepaalt de paginagrootte; vectorgegevens blijven resolutie‑onafhankelijk, waardoor ze scherp blijven ongeacht het zoomniveau.

**Q: Kan ik een andere DPI instellen voor de TIFF‑uitvoer?**  
A: Ja. Pas `rasterizationOptions.setResolution(dpiValue)` aan voordat je `TiffOptions` maakt.

**Q: Hoe kan ik **change PDF dimensions** voor een bestaande PDF aanpassen zonder de CAD opnieuw te renderen?**  
A: Gebruik Aspose.PDF om de gegenereerde PDF te laden en roep `pdf.getPages().setPageSize(PageSize.A4)` of een aangepaste grootte aan.

**Q: Wat is de beste manier om **convert dxf to pdf** uit te voeren terwijl lagen behouden blijven?**  
A: Houd `setAutomaticLayoutsScaling(true)` ingeschakeld en vermijd `setNoScaling(true)`; dit behoudt de zichtbaarheid van lagen en de lay‑outintegriteit.

## Conclusie

Gefeliciteerd! Je hebt met succes **convert CAD to PDF** en **export CAD to TIFF** uitgevoerd terwijl je **set canvas size java** hebt toegepast, **automatic layout scaling** hebt ingeschakeld en hebt geleerd hoe je **configure canvas mode** kunt gebruiken voor uitvoer van hoge kwaliteit. Deze tutorial biedt een solide basis voor je CAD‑conversieprojecten. Ontdek meer functies en mogelijkheden in de [Aspose.CAD‑documentatie](https://reference.aspose.com/cad/java/).

---

**Laatst bijgewerkt:** 2026-02-15  
**Getest met:** Aspose.CAD for Java 24.12  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}