---
date: 2026-02-28
description: Leer hoe u PDF's maakt van DWG, DWG opslaat als PDF en tekst toevoegt
  aan DWG-tekeningen met Aspose.CAD voor Java—stapsgewijze handleiding.
linktitle: Add Text in DWG
second_title: Aspose.CAD Java API
title: PDF maken van DWG en tekst toevoegen met Aspose.CAD voor Java
url: /nl/java/cad-text-and-annotation/add-text-in-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Maak PDF van DWG en Voeg Tekst Toe met Aspose.CAD voor Java

## Introductie

Als je **PDF van DWG** bestanden moet maken en tegelijkertijd aangepaste tekst wilt invoegen, ben je hier op de juiste plek. In deze tutorial lopen we het volledige proces door—het laden van een DWG-tekening, het toevoegen van een tekstaanduiding, en uiteindelijk het opslaan van het resultaat als PDF met Aspose.CAD voor Java. Aan het einde begrijp je hoe je **DWG als PDF opslaat**, de teksthoogte aanpast, en zelfs basisannotaties toevoegt.

## Snelle Antwoorden
- **Kan ik DWG naar PDF converteren in Java?** Ja, Aspose.CAD voor Java biedt een eenvoudige API.  
- **Heb ik een licentie nodig voor productiegebruik?** Een commerciële licentie is vereist; een gratis proefversie is beschikbaar.  
- **Welke methode voegt tekst toe aan een DWG?** Gebruik het `CadText` object en voeg het toe aan de modelruimte.  
- **Kan ik de teksthoogte instellen?** Absoluut—gebruik `setTextHeight()` op de `CadText` instantie.  
- **Is de output vector‑gebaseerd?** Wanneer rasterisatie‑opties zijn ingesteld op `UseObjectColor`, behoudt de PDF hoogwaardige vectorgegevens.

## Wat is “PDF maken van DWG”?
Een PDF maken van een DWG-tekening betekent het converteren van het native CAD‑formaat naar een breed ondersteund, alleen‑lezen document, terwijl de oorspronkelijke geometrie behouden blijft. Deze conversie is essentieel wanneer je ontwerpen wilt delen met belanghebbenden die geen CAD‑software hebben.

## Waarom Aspose.CAD voor Java gebruiken om DWG naar PDF te converteren?
Aspose.CAD biedt een pure‑Java oplossing die geen externe CAD‑installatie vereist. Het ondersteunt **DWG naar PDF converteren**, behoudt vector‑fidelity, en stelt je in staat programmatisch annotaties zoals tekst, afmetingen of aangepaste grafische elementen toe te voegen vóór de conversie.

## Vereisten

Voordat je aan de tutorial begint, zorg dat je de volgende zaken gereed hebt:

- Aspose.CAD voor Java Bibliotheek: Download en installeer de bibliotheek vanaf de [Aspose.CAD for Java page](https://releases.aspose.com/cad/java/).

- Java Development Kit (JDK): Zorg ervoor dat je de nieuwste JDK op je systeem hebt geïnstalleerd.

- DWG-tekening: Bereid een DWG-tekeningsbestand voor waarin je tekst wilt toevoegen.

## Import Namespaces

In je Java‑code importeer je de benodigde namespaces voor Aspose.CAD:

```java
import com.aspose.cad.Image;


import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Nu splitsen we de meegeleverde code‑snippet op in meerdere stappen:

## Stap 1: Stel Documentmap en DWG-bestandspad in

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String dwgPathToFile = dataDir + "SimpleEntites.dwg";
```

## Stap 2: Laad DWG-afbeelding

```java
Image image = Image.load(dwgPathToFile);
```

## Stap 3: Maak CadText-object (Voeg Tekst toe aan DWG)

```java
CadText cadText = new CadText();
cadText.setStyleType("Standard");
cadText.setDefaultValue("Some custom text");
cadText.setColorId(256);
cadText.setLayerName("0");
cadText.getFirstAlignment().setX(47.9);
cadText.getFirstAlignment().setY(5.56);
cadText.setTextHeight(0.8);          // set text height in DWG units
cadText.setScaleX(0);
```

## Stap 4: Voeg Tekst toe aan CadImage (Plaats Annotatie)

```java
CadImage cadImage = ((CadImage)(image));
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(cadText);
```

## Stap 5: Stel PDF-opties in (Voorbereiden om PDF te maken van DWG)

```java
PdfOptions pdfOptions = new PdfOptions();
```

## Stap 6: Configureer CadRasterizationOptions (Beheer PDF-rendering)

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

## Stap 7: Sla de aangepaste DWG op als PDF (dwg naar pdf java)

```java
image.save(dataDir + "SimpleEntites_generated.dwg.pdf", pdfOptions);
```

Door deze stappen te volgen, kun je **PDF van DWG** maken, aangepaste tekst toevoegen, en de teksthoogte regelen—alles met slechts een paar regels Java‑code.

## Hoe DWG naar PDF converteren in Java op schaal?
Als je **DWG PDF** bestanden in batch wilt converteren, wikkel je de bovenstaande code in een lus die over een map met DWG‑tekeningen itereren. Pas `pageHeight`/`pageWidth` alleen aan wanneer nodig om het geheugenverbruik laag te houden, en hergebruik dezelfde `PdfOptions`‑instantie voor elk bestand om de prestaties te verbeteren.

## Veelvoorkomende Problemen & Tips

- **Tekst verschijnt niet?** Controleer of de X/Y-coördinaten binnen de tekening liggen en of de laag zichtbaar is.
- **Onjuiste teksthoogte?** Pas `setTextHeight()` aan; de waarde is in het eenhedensysteem van de tekening.
- **PDF ziet er gerasterd uit?** Zorg ervoor dat `CadDrawTypeMode.UseObjectColor` is ingesteld om vectorinformatie te behouden.
- **Prestaties bij grote bestanden?** Verhoog `pageHeight`/`pageWidth` alleen indien nodig; grotere waarden verbruiken meer geheugen.

## Veelgestelde Vragen

**Q: Is Aspose.CAD compatibel met alle versies van DWG‑bestanden?**  
A: Aspose.CAD ondersteunt verschillende versies van DWG‑bestanden, waardoor compatibiliteit met een breed scala aan CAD‑software wordt gegarandeerd.

**Q: Kan ik het lettertype en de opmaak van de toegevoegde tekst aanpassen?**  
A: Ja, je kunt het lettertype, de stijl en andere opmaakopties voor de tekst die aan DWG‑bestanden wordt toegevoegd aanpassen met Aspose.CAD.

**Q: Is er een gratis proefversie beschikbaar voor Aspose.CAD voor Java?**  
A: Ja, je kunt de functies van Aspose.CAD verkennen door een gratis proefversie te verkrijgen via [hier](https://releases.aspose.com/).

**Q: Waar kan ik gedetailleerde documentatie vinden voor Aspose.CAD voor Java?**  
A: Raadpleeg de documentatie [hier](https://reference.aspose.com/cad/java/) voor diepgaande informatie en voorbeelden.

**Q: Hoe kan ik ondersteuning krijgen of hulp zoeken voor Aspose.CAD?**  
A: Bezoek het [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) om assistentie te krijgen en in contact te komen met de community.

---

**Last Updated:** 2026-02-28  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}