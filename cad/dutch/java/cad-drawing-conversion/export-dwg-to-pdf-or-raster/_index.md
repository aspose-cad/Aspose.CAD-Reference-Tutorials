---
date: 2025-12-18
description: Ontdek hoe u dwg naar pdf of rasterafbeeldingen kunt exporteren in Java
  met Aspose.CAD. Deze stapsgewijze gids garandeert precisie, efficiëntie en eenvoudige
  conversie van DWG‑bestanden.
linktitle: Export DWG to PDF or Raster
second_title: Aspose.CAD Java API
title: DWG exporteren naar PDF of raster met Aspose.CAD voor Java
url: /nl/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export DWG naar PDF of Raster met Aspose.CAD voor Java

## Introductie

In de dynamische wereld van computer‑aided design (CAD) is efficiënt omgaan met tekeningen cruciaal. Met **Aspose.CAD for Java** kun je **export dwg to pdf** — of rasterafbeeldingen — in slechts een paar regels code. Deze tutorial leidt je door het volledige proces, van het laden van een DWG‑bestand tot het genereren van een PDF van hoge kwaliteit, en benadrukt waarom Aspose.CAD Java de favoriete bibliotheek is voor CAD‑conversietaken.

## Snelle Antwoorden
- **Waar gaat deze tutorial over?** Exporteren van DWG‑bestanden naar PDF of rasterafbeeldingen met Aspose.CAD for Java.  
- **Heb ik een licentie nodig?** Er is een gratis tijdelijke licentie beschikbaar voor evaluatie; een volledige licentie is vereist voor productie.  
- **Welke Java‑versie wordt ondersteund?** Elke Java 8+ runtime werkt met de nieuwste Aspose.CAD Java API.  
- **Kan ik DWG naar andere afbeeldingsformaten converteren?** Ja – dezelfde rasterisatie‑opties laten je PNG, JPEG, BMP, enz. exporteren.  
- **Hoe lang duurt de conversie?** Meestal minder dan een seconde voor standaardtekeningen; grotere bestanden kunnen enkele seconden duren.

## Wat is “export dwg to pdf”?
Exporteren van DWG naar PDF betekent het omzetten van een native AutoCAD‑tekening naar een draagbaar, apparaat‑onafhankelijk PDF‑document. De resulterende PDF behoudt vectorgegevens, lagen en schaal, waardoor het ideaal is voor delen, afdrukken of archiveren.

## Waarom Aspose.CAD Java gebruiken voor deze conversie?
- **Geen externe afhankelijkheden** – pure Java, geen native DLL's.  
- **Nauwkeurige eenheidshandhaving** – respecteert automatisch metrische of imperiale eenheden.  
- **Rasteroutput van hoge kwaliteit** – fijn afgestemde DPI‑ en paginagrootte‑controle.  
- **Volledige PDF‑ondersteuning** – vector‑behoudende PDF‑generatie zonder extra bibliotheken.

## Vereisten

Voordat je in de code duikt, zorg ervoor dat je het volgende hebt:

- Basiskennis van Java‑programmeren.  
- Aspose.CAD for Java‑bibliotheek geïnstalleerd. Als je deze nog niet hebt gedownload, haal hem **[hier](https://releases.aspose.com/cad/java/)**.  
- Een DWG‑bestand voor testen – de voorbeeld‑**Bottom_plate.dwg** wordt in deze gids gebruikt.

## Namespaces importeren

In je Java‑project importeer je de benodigde klassen om de conversie te starten:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## Stapsgewijze Gids

### Stap 1: Laad het DWG‑bestand

Eerst laad je je DWG‑tekening met de `Image`‑klasse. Dit creëert een in‑memory representatie waar Aspose.CAD mee kan werken.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

### Stap 2: Bepaal eenheidstype

Begrijpen of de tekening metrische of imperiale eenheden gebruikt is essentieel voor correcte schaal. De hulpfunctie `IsMetric` (implementatie weggelaten voor beknoptheid) retourneert een boolean‑waarde.

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

### Stap 3: Stel rasterisatie‑opties in

Op basis van het eenhedensysteem configureer je paginagrootte, schaal en het doel‑eenheidstype. Deze opties bepalen hoe de DWG wordt gerasterd voordat deze in een PDF wordt verpakt.

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

### Stap 4: Configureer PDF‑opties

Maak een `PdfOptions`‑instantie aan en koppel de rasterisatie‑instellingen. Dit vertelt Aspose.CAD hoe de gerasterde inhoud in de uiteindelijke PDF moet worden ingebed.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

### Stap 5: Opslaan als PDF

Tot slot exporteer je de tekening naar een PDF‑bestand. De `save`‑methode neemt het uitvoerpad en de geconfigureerde `PdfOptions`.

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

Wanneer de code is voltooid, vind je **Saved.pdf** in je `DWGDrawings`‑map, klaar voor distributie of archivering.

## Veelvoorkomende Problemen & Tips

- **Onjuiste paginagrootte** – Controleer de eenheidsconversielogica; niet‑overeenkomende coëfficiënten kunnen te grote pagina's veroorzaken.  
- **Ontbrekende lettertypen of lijndiktes** – Zorg ervoor dat de DWG eventuele externe bronnen verwijst vóór conversie.  
- **Prestaties bij grote tekeningen** – Verhoog de `DPI`‑instelling in `CadRasterizationOptions` alleen wanneer hogere kwaliteit vereist is; een lagere DPI versnelt de verwerking.

## Veelgestelde Vragen

**Q: Kan ik Aspose.CAD for Java gebruiken met andere Java‑frameworks?**  
A: Ja, Aspose.CAD for Java integreert naadloos met populaire Java‑frameworks zoals Spring, Jakarta EE en Android.

**Q: Is er een tijdelijke licentie beschikbaar voor Aspose.CAD for Java?**  
A: Ja, je kunt een tijdelijke licentie verkrijgen **[hier](https://purchase.aspose.com/temporary-license/)**.

**Q: Waar kan ik ondersteuning vinden voor Aspose.CAD for Java?**  
A: Bezoek het **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)** voor hulp van de community en Aspose‑engineers.

**Q: Hoe kan ik een licentie aanschaffen voor Aspose.CAD for Java?**  
A: Je kunt een licentie kopen **[hier](https://purchase.aspose.com/buy)**.

**Q: Welke eenheden ondersteunt Aspose.CAD for Java?**  
A: Aspose.CAD for Java ondersteunt zowel metrische als imperiale eenheden en detecteert automatisch het eenhedensysteem van de tekening.

**Q: Kan ik DWG naar andere afbeeldingsformaten converteren (bijv. PNG, JPEG) met dezelfde API?**  
A: Absoluut. Vervang `PdfOptions` door de juiste raster‑afbeeldingsopties (bijv. `PngOptions`) en hergebruik dezelfde `CadRasterizationOptions`.

## Conclusie

Deze tutorial toonde hoe je **export dwg to pdf** en rasterafbeeldingen kunt gebruiken met Aspose.CAD for Java. Door de stapsgewijze gids te volgen, kun je betrouwbare CAD‑conversie integreren in elke Java‑applicatie, of je nu PDF's nodig hebt voor documentatie of rasterafbeeldingen voor weergave op het web.

---

**Laatst bijgewerkt:** 2025-12-18  
**Getest met:** Aspose.CAD for Java 24.10  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}