---
date: 2026-02-17
description: Leer hoe de Java CAD‑bibliotheek Aspose.CAD for Java DWG snel en nauwkeurig
  kan exporteren naar PDF of rasterafbeeldingen.
linktitle: Export DWG to PDF or Raster
second_title: Aspose.CAD Java API
title: DWG exporteren naar PDF of raster met Java CAD‑bibliotheek Aspose.CAD voor
  Java
url: /nl/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG exporteren naar PDF of Raster met java cad library Aspose.CAD voor Java

## Introductie

In de dynamische wereld van computer‑aided design (CAD) is efficiënt omgaan met tekeningen cruciaal. Met de **java cad library** **Aspose.CAD for Java** kun je **export dwg to pdf** — of rasterafbeeldingen — in slechts een paar regels code. Deze tutorial leidt je door het volledige proces, van het laden van een DWG‑bestand tot het genereren van een PDF van hoge kwaliteit, en laat zien waarom Aspose.CAD Java de favoriete bibliotheek is voor CAD‑conversietaken.

## Snelle antwoorden
- **Waar gaat deze tutorial over?** Exporteren van DWG‑bestanden naar PDF of rasterafbeeldingen met Aspose.CAD voor Java.  
- **Heb ik een licentie nodig?** Er is een gratis tijdelijke licentie beschikbaar voor evaluatie; een volledige licentie is vereist voor productie.  
- **Welke Java‑versie wordt ondersteund?** Elke Java 8+ runtime werkt met de nieuwste Aspose.CAD Java‑API.  
- **Kan ik DWG naar andere afbeeldingsformaten converteren?** Ja – dezelfde rasterisatie‑opties laten je PNG, JPEG, BMP, enz. exporteren.  
- **Hoe lang duurt de conversie?** Meestal minder dan een seconde voor standaardtekeningen; grotere bestanden kunnen enkele seconden duren.

## Waarom java cad library de beste keuze is voor DWG-conversie?

- **Pure Java‑implementatie** – geen native DLL’s of externe tools.  
- **Nauwkeurige eenheidshandeling** – metrische en imperiale eenheden worden automatisch gedetecteerd.  
- **Rasteroutput van hoge kwaliteit** – fijn afgestelde DPI‑ en paginagrootte‑controle.  
- **Volledige PDF‑ondersteuning** – vector‑behoudende PDF‑generatie zonder extra afhankelijkheden.  
- **Flexibele licentiëring** – begin met een **temporary license aspose** voor testen, upgrade vervolgens wanneer u live gaat.

## Wat is “export dwg to pdf”?

Exporteren van DWG naar PDF betekent het omzetten van een native AutoCAD‑tekening naar een draagbaar, apparaat‑onafhankelijk PDF‑document. De resulterende PDF behoudt vectorgegevens, lagen en schaal, waardoor het ideaal is voor delen, afdrukken of archiveren.

## Waarom Aspose.CAD Java gebruiken voor deze conversie?

Omdat de **java cad library** alles van eenheidconversie tot rasterisatie intern afhandelt, vermijd je de complexiteit van tools van derden en krijg je consistente resultaten op alle platforms.

## Voorvereisten

- Basiskennis van Java‑programmeren.  
- Aspose.CAD for Java‑bibliotheek geïnstalleerd. Als u deze nog niet hebt gedownload, haal hem **[hier](https://releases.aspose.com/cad/java/)**.  
- Een DWG‑bestand voor testen – de voorbeeld‑**Bottom_plate.dwg** wordt in deze gids gebruikt.

## Namespaces importeren

In uw Java‑project importeert u de benodigde klassen om de conversie op te starten:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## Stapsgewijze handleiding

### Stap 1: Laad het DWG‑bestand

Laad eerst uw DWG‑tekening met de `Image`‑klasse. Dit creëert een in‑memory representatie waarmee Aspose.CAD kan werken.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

### Stap 2: Bepaal eenheidstype

Het begrijpen of de tekening metrisch of imperiaal is, is essentieel voor correcte schaal. De hulpfunctie `IsMetric` (implementatie weggelaten voor beknoptheid) retourneert een boolean‑waarde.

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

### Stap 3: Rasterisatie‑opties instellen

Op basis van het eenheidssysteem configureert u paginagrootte, schaal en het doel‑eenheidstype. Deze opties bepalen hoe de DWG wordt gerasterd voordat deze in een PDF wordt verpakt.

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

### Stap 4: PDF‑opties configureren (pdf options cad)

Maak een `PdfOptions`‑instantie aan en koppel de rasterisatie‑instellingen. Dit vertelt Aspose.CAD hoe de gerasterde inhoud in de uiteindelijke PDF moet worden ingebed.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

### Stap 5: Opslaan als PDF

Exporteer tenslotte de tekening naar een PDF‑bestand. De `save`‑methode neemt het uitvoerpad en de geconfigureerde `PdfOptions`.

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

Wanneer de code is voltooid, vindt u **Saved.pdf** in uw `DWGDrawings`‑map, klaar voor distributie of archivering.

## Hoe dwg rasterafbeeldingen te converteren met java cad library

Als u rasterafbeeldingen in plaats van een PDF nodig heeft, vervangt u eenvoudig `PdfOptions` door de juiste rasterafbeeldingsopties (bijv. `PngOptions`, `JpegOptions`). Dezelfde `CadRasterizationOptions`‑instantie kan opnieuw worden gebruikt, waardoor u **convert dwg raster**‑bestanden met minimale code‑aanpassingen kunt uitvoeren.

## Hoe pdf dwg te genereren met pdf options cad

Het bovenstaande voorbeeld genereert al **pdf dwg**‑output. Door `pdfOptions` aan te passen — bijvoorbeeld `pdfOptions.setCompress(true)` — kunt u de PDF‑grootte en -kwaliteit regelen. Dit toont de flexibiliteit van de **pdf options cad**‑API.

## Veelvoorkomende problemen & tips

- **Onjuiste paginagrootte** – Controleer de eenheidsconversielogica; niet‑overeenkomende coëfficiënten kunnen te grote pagina's veroorzaken.  
- **Ontbrekende lettertypen of lijndiktes** – Zorg ervoor dat de DWG eventuele externe bronnen verwijst vóór conversie.  
- **Prestaties bij grote tekeningen** – Verhoog de `DPI`‑instelling in `CadRasterizationOptions` alleen wanneer hogere kwaliteit vereist is; lagere DPI versnelt de verwerking.  
- **Licentie‑zorgen** – Voor evaluatie kunt u een **temporary license aspose** gebruiken; een volledige licentie is vereist voor productie‑implementaties.

## Veelgestelde vragen

**V: Kan ik Aspose.CAD voor Java gebruiken met andere Java‑frameworks?**  
A: Ja, Aspose.CAD for Java integreert naadloos met populaire Java‑frameworks zoals Spring, Jakarta EE en Android.

**V: Is er een tijdelijke licentie beschikbaar voor Aspose.CAD voor Java?**  
A: Ja, u kunt een tijdelijke licentie **[hier](https://purchase.aspose.com/temporary-license/)** verkrijgen.

**V: Waar kan ik ondersteuning vinden voor Aspose.CAD voor Java?**  
A: Bezoek het **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)** voor hulp van de community en Aspose‑engineers.

**V: Hoe kan ik een licentie aanschaffen voor Aspose.CAD voor Java?**  
A: U kunt een licentie **[hier](https://purchase.aspose.com/buy)** aanschaffen.

**V: Welke eenheden ondersteunt Aspose.CAD voor Java?**  
A: Aspose.CAD for Java ondersteunt zowel metrische als imperiale eenheden en detecteert automatisch het eenheidssysteem van de tekening.

**V: Kan ik DWG naar andere afbeeldingsformaten converteren (bijv. PNG, JPEG) met dezelfde API?**  
A: Absoluut. Vervang `PdfOptions` door de juiste rasterafbeeldingsopties (bijv. `PngOptions`) en hergebruik dezelfde `CadRasterizationOptions`.

## Conclusie

Deze tutorial heeft laten zien hoe u **export dwg to pdf** en rasterafbeeldingen kunt uitvoeren met de **java cad library** Aspose.CAD voor Java. Door de stapsgewijze gids te volgen, kunt u betrouwbare CAD‑conversie integreren in elke Java‑applicatie, of u nu PDF's voor documentatie of rasterafbeeldingen voor weergave op het web nodig heeft.

---

**Last Updated:** 2026-02-17  
**Tested With:** Aspose.CAD for Java 24.10  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}