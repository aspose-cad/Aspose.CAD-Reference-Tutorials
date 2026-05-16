---
date: 2026-02-23
description: Leer hoe je dwg‑bestanden kunt laden met Aspose CAD DWG voor Java en
  onderlegger‑vlaggen kunt extraheren – een stapsgewijze gids voor ontwikkelaars.
linktitle: Accessing Underlay Flags of DWG
second_title: Aspose.CAD Java API
title: aspose cad dwg – DWG laden & toegang tot onderleggervlaggen (Java)
url: /nl/java/cad-file-manipulation/accessing-underlay-flags-of-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG-bestand laden & onderlegger‑vlaggen benaderen – Aspose.CAD voor Java

In moderne CAD‑workflows kun je **met aspose cad dwg snel een DWG‑bestand laden** en onderlegger‑details ophalen die vaak verborgen blijven voor gewone kijkers. Of je nu een Java DWG‑viewer bouwt, een batch‑verwerkings‑dwg‑pipeline automatiseert, of metadata extraheert voor GIS‑integratie, Aspose.CAD voor Java biedt je een schone, code‑first manier om dit te doen. In deze tutorial lopen we de exacte stappen door om **een DWG‑bestand te laden**, de entiteiten te itereren en de onderlegger‑vlaggen te lezen die veel ontwikkelaars over het hoofd zien.

## Snelle antwoorden
- **Wat is de primaire klasse om een DWG te openen?** `com.aspose.cad.Image.load()` retourneert een `CadImage`.
- **Welk object bevat onderlegger‑informatie?** `CadUnderlay` (of afgeleide typen zoals `CadDgnUnderlay`).
- **Heb ik een licentie nodig voor ontwikkeling?** Een gratis proefversie werkt voor testen; een commerciële licentie is vereist voor productie.
- **Kan ik meerdere DWG‑bestanden in een lus verwerken?** Ja – herhaal gewoon het laad‑en‑iteratie‑patroon.
- **Is deze aanpak compatibel met Java 11+?** Absoluut, Aspose.CAD ondersteunt Java 8 tot en met de nieuwste LTS‑releases.

## aspose cad dwg – Een DWG‑bestand laden (Java)

`Image.load()` leest de binaire DWG‑inhoud en creëert een `CadImage`‑object in het geheugen. Vanaf daar kun je lagen, blokken en onderlegger‑entiteiten verkennen zonder zelf met het DWG‑bestandsformaat om te gaan.

## Waarom onderlegger‑vlaggen uit een DWG extraheren?

Onderlegger‑vlaggen vertellen je hoe een externe referentie (zoals een DGN‑ of PDF‑onderlegger) gepositioneerd, geschaald en geroteerd is binnen de tekening. Het kennen van deze waarden stelt je in staat om:

- De exacte visuele lay-out opnieuw te creëren in een aangepaste **java dwg viewer**.
- Onderleggers om te zetten naar native CAD‑entiteiten voor verdere bewerking.
- Rapporten te genereren die onderlegger‑metadata bevatten voor naleving of documentatie.
- **Batch‑verwerken van dwg**‑bestanden en hun onderlegger‑metadata opslaan in een database voor latere analyse.

## Vereisten
- **Aspose.CAD Library** – download van de [releases](https://releases.aspose.com/cad/java/) pagina.  
- **Java Development Kit** – JDK 8 of nieuwer.  
- **Een map** die de DWG‑bestanden bevat die je wilt analyseren. Vervang `"Your Document Directory"` in de code door je eigen pad.

## Namespaces importeren

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadBaseEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadDgnUnderlay;
import com.aspose.cad.fileformats.cad.cadobjects.CadUnderlay;
import com.aspose.cad.fileformats.cad.cadobjects.UnderlayFlags;
```

## Stapsgewijze handleiding

### Stap 1: De resource‑directory instellen
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DWGDrawings/";
```
Definieer waar je DWG‑bestanden zich bevinden. Het gebruik van een speciale map houdt het voorbeeld schoon en draagbaar.

### Stap 2: Het DWG‑bestand laden
```java
// Input file name and path
String fileName = dataDir + "BlockRefDgn.dwg";

// Load an existing DWG file and convert it into CadImage 
CadImage image = (CadImage)Image.load(fileName);
```
Hier **laden we het dwg‑bestand** `BlockRefDgn.dwg` in een `CadImage`‑instantie, klaar voor inspectie.

### Stap 3: Door DWG‑entiteiten itereren
```java
// Go through each entity inside the DWG file
for(CadBaseEntity entity : image.getEntities())
```
De lus doorloopt elke entiteit — lijnen, cirkels, blokken en onderleggers — zodat we de benodigde kunnen selecteren.

### Stap 4: CadDgnUnderlay‑entiteiten identificeren
```java
// Check if entity is of CadDgnUnderlay type
if (entity instanceof CadDgnUnderlay)
```
Alleen `CadDgnUnderlay`‑objecten bevatten de onderlegger‑vlaggen die we zoeken, dus filteren we daarop.

### Stap 5: Toegang tot onderlegger‑informatie
```java
// Access different underlay flags 
CadUnderlay underlay = (CadUnderlay) entity;
System.out.println(underlay.getUnderlayPath());
System.out.println(underlay.getUnderlayName());
// ... (Additional underlay properties)
break;
```
Zodra we een `CadUnderlay` hebben, kunnen we het pad, de naam, het invoerpunt, de rotatie, de schaalfactoren en de `UnderlayFlags`‑enum lezen die zichtbaarheid, bijsnijden en andere renderopties aangeeft.

## Hoe dwg‑bestanden in een batch‑proces te laden

Als je **dwg‑bestanden batch‑gewijs wilt verwerken**, wikkel je de bovenstaande stappen in een eenvoudige `for`‑lus die over alle bestanden in `dataDir` iterereert. Dezelfde `Image.load()`‑aanroep werkt voor elk bestand, en je kunt de geëxtraheerde vlaggen opslaan in een CSV‑bestand of een database voor vervolgrapportage.

## Veelvoorkomende problemen & tips
- **Null onderlegger‑pad** – Zorg ervoor dat de DWG daadwerkelijk naar een extern bestand verwijst; anders is het pad leeg.
- **Niet‑ondersteund onderlegger‑type** – Aspose.CAD ondersteunt momenteel DGN‑onderleggers; PDF‑onderleggers zijn nog niet via de API beschikbaar.
- **Licentie‑uitzonderingen** – Het uitvoeren van de code zonder geldige licentie voegt een watermerk toe aan geëxporteerde afbeeldingen.
- **Prestatie‑tip:** Hergebruik één `Image`‑instantie bij het verwerken van veel bestanden in een batch om de GC‑belasting te verminderen.

## Veelgestelde vragen

**Q: Kan ik Aspose.CAD voor Java gebruiken met andere CAD‑bestandsformaten?**  
A: Aspose.CAD richt zich voornamelijk op het DWG‑formaat, maar ondersteunt ook DXF, DWF en andere CAD‑formaten.

**Q: Is er een proefversie beschikbaar voor Aspose.CAD voor Java?**  
A: Ja, je kunt de functies verkennen met een gratis proefversie via [hier](https://releases.aspose.com/).

**Q: Hoe kan ik ondersteuning krijgen of hulp zoeken voor Aspose.CAD voor Java?**  
A: Bezoek het [Aspose.CAD‑forum](https://forum.aspose.com/c/cad/19) voor community‑ondersteuning en discussies.

**Q: Zijn tijdelijke licenties beschikbaar voor Aspose.CAD voor Java?**  
A: Ja, je kunt een tijdelijke licentie verkrijgen [hier](https://purchase.aspose.com/temporary-license/).

**Q: Waar kan ik de uitgebreide documentatie voor Aspose.CAD voor Java vinden?**  
A: Raadpleeg de [documentatie](https://reference.aspose.com/cad/java/) voor gedetailleerde informatie.

---

**Laatste update:** 2026-02-23  
**Getest met:** Aspose.CAD 24.12 voor Java  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}