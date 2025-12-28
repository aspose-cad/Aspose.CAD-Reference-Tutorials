---
date: 2025-12-28
description: Leer hoe je PDF maakt van DWG, DWG opslaat als PDF en tekst toevoegt
  aan DWG-tekeningen met Aspose.CAD voor Java—stap‑voor‑stap gids.
linktitle: Add Text in DWG
second_title: Aspose.CAD Java API
title: PDF maken van DWG en tekst toevoegen met Aspose.CAD voor Java
url: /nl/java/cad-text-and-annotation/add-text-in-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PDF maken van DWG en tekst toevoegen met Aspose.CAD voor Java

## Inleiding

Als je **PDF wilt maken van DWG**‑bestanden en tegelijkertijd aangepaste tekst wilt invoegen, ben je hier op de juiste plek. In deze tutorial lopen we het volledige proces door—een DWG‑tekening laden, een tekstaanduiding toevoegen, en uiteindelijk het resultaat opslaan als PDF met Aspose.CAD voor Java. Aan het einde begrijp je hoe je **DWG als PDF opslaat**, de teksthoogte aanpast, en zelfs eenvoudige annotaties toevoegt.

## Snelle antwoorden
- **Kan ik DWG naar PDF converteren in Java?** Ja, Aspose.CAD voor Java biedt een eenvoudige API.  
- **Heb ik een licentie nodig voor productiegebruik?** Een commerciële licentie is vereist; een gratis proefversie is beschikbaar.  
- **Welke methode voegt tekst toe aan een DWG?** Gebruik het `CadText`‑object en voeg het toe aan de modelruimte.  
- **Kan ik de teksthoogte instellen?** Absoluut—gebruik `setTextHeight()` op de `CadText`‑instantie.  
- **Is de output vector‑gebaseerd?** Wanneer rasterisatie‑opties zijn ingesteld op `UseObjectColor`, behoudt de PDF hoogwaardige vectorgegevens.

## Vereisten

Zorg ervoor dat je de volgende zaken klaar hebt staan voordat je aan de tutorial begint:

- Aspose.CAD voor Java‑bibliotheek: Download en installeer de bibliotheek vanaf de [Aspose.CAD for Java‑pagina](https://releases.aspose.com/cad/java/).

- Java Development Kit (JDK): Zorg dat de nieuwste JDK op je systeem is geïnstalleerd.

- DWG‑tekening: Bereid een DWG‑tekeningsbestand voor waarin je tekst wilt toevoegen.

## Namespaces importeren

Importeer in je Java‑code de benodigde namespaces voor Aspose.CAD:

```java
import com.aspose.cad.Image;


import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Laten we nu de meegeleverde code‑snippet opsplitsen in meerdere stappen:

## Stap 1: Documentmap en DWG‑bestandspad instellen

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String dwgPathToFile = dataDir + "SimpleEntites.dwg";
```

## Stap 2: DWG‑afbeelding laden

```java
Image image = Image.load(dwgPathToFile);
```

## Stap 3: CadText‑object maken (tekst toevoegen aan DWG)

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

## Stap 4: Tekst toevoegen aan CadImage (annotatie invoegen)

```java
CadImage cadImage = ((CadImage)(image));
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(cadText);
```

## Stap 5: PDF‑opties instellen (voorbereiden om PDF te maken van DWG)

```java
PdfOptions pdfOptions = new PdfOptions();
```

## Stap 6: CadRasterizationOptions configureren (PDF‑rendering regelen)

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

## Stap 7: De aangepaste DWG opslaan als PDF (dwg to pdf java)

```java
image.save(dataDir + "SimpleEntites_generated.dwg.pdf", pdfOptions);
```

Door deze stappen te volgen, kun je **PDF maken van DWG**, aangepaste tekst toevoegen en de teksthoogte regelen—allemaal met slechts een paar regels Java‑code.

## Waarom tekst toevoegen aan DWG en converteren naar PDF?

Tekst direct aan een DWG‑bestand toevoegen is nuttig voor:

- **Ontwerpen markeren** met notities of onderdeelnummers.  
- **Printbare documentatie maken** waarbij de PDF fungeert als een alleen‑lezen, breed ondersteund formaat.  
- **Batchverwerking automatiseren** van grote CAD‑bibliotheken zonder handmatige bewerking.

## Veelvoorkomende problemen & tips

- **Tekst verschijnt niet?** Controleer of de X/Y‑coördinaten binnen de tekeningsomvang liggen en of de laag zichtbaar is.  
- **Onjuiste teksthoogte?** Pas `setTextHeight()` aan; de waarde is in het eenheidssysteem van de tekening.  
- **PDF ziet er gerasterd uit?** Zorg ervoor dat `CadDrawTypeMode.UseObjectColor` is ingesteld om vectorinformatie te behouden.  
- **Prestaties bij grote bestanden?** Verhoog `pageHeight`/`pageWidth` alleen indien nodig; grotere waarden verbruiken meer geheugen.

## Veelgestelde vragen

**V: Is Aspose.CAD compatibel met alle versies van DWG‑bestanden?**  
A: Aspose.CAD ondersteunt verschillende versies van DWG‑bestanden, waardoor compatibiliteit met een breed scala aan CAD‑software wordt gegarandeerd.

**V: Kan ik het lettertype en de opmaak van de toegevoegde tekst aanpassen?**  
A: Ja, je kunt het lettertype, de stijl en andere opmaakopties van de tekst die aan DWG‑bestanden wordt toegevoegd, aanpassen met Aspose.CAD.

**V: Is er een gratis proefversie beschikbaar voor Aspose.CAD voor Java?**  
A: Ja, je kunt de functies van Aspose.CAD verkennen door een gratis proefversie te verkrijgen via [hier](https://releases.aspose.com/).

**V: Waar vind ik gedetailleerde documentatie voor Aspose.CAD voor Java?**  
A: Raadpleeg de documentatie [hier](https://reference.aspose.com/cad/java/) voor uitgebreide informatie en voorbeelden.

**V: Hoe kan ik ondersteuning krijgen of hulp zoeken voor Aspose.CAD?**  
A: Bezoek het [Aspose.CAD‑forum](https://forum.aspose.com/c/cad/19) voor assistentie en om in contact te komen met de community.

---

**Laatst bijgewerkt:** 2025-12-28  
**Getest met:** Aspose.CAD voor Java 24.12  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}