---
date: 2025-12-22
description: Leer hoe u een DWG‑bestand laadt en onderleggerinformatie extraheert
  met Aspose.CAD voor Java – een stapsgewijze handleiding die onderlegger‑vlaggen
  behandelt.
linktitle: Accessing Underlay Flags of DWG
second_title: Aspose.CAD Java API
title: DWG-bestand laden & onderlegger‑vlaggen openen – Aspose.CAD voor Java
url: /nl/java/cad-file-manipulation/accessing-underlay-flags-of-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG-bestand laden & onderlegger‑vlaggen openen – Aspose.CAD voor Java

In moderne CAD‑workflows is **een DWG‑bestand laden** snel en het ophalen van onderlegger‑details een veelvoorkomende eis. Of je nu een viewer bouwt, batchverwerking automatiseert of metadata extraheert voor GIS‑integratie, Aspose.CAD voor Java biedt een nette, code‑first manier om dit te doen. In deze tutorial lopen we stap voor stap door hoe je een **DWG‑bestand laadt**, de entiteiten doorloopt en de onderlegger‑vlaggen leest die veel ontwikkelaars over het hoofd zien.

## Snelle antwoorden
- **Welke klasse gebruik je primair om een DWG te openen?** `com.aspose.cad.Image.load()` retourneert een `CadImage`.
- **Welk object bevat onderlegger‑informatie?** `CadUnderlay` (of afgeleide types zoals `CadDgnUnderlay`).
- **Heb ik een licentie nodig voor ontwikkeling?** Een gratis proefversie werkt voor testen; een commerciële licentie is vereist voor productie.
- **Kan ik meerdere DWG‑bestanden in een lus verwerken?** Ja – herhaal gewoon het laad‑en‑doorloop‑patroon.
- **Is deze aanpak compatibel met Java 11+?** Absoluut, Aspose.CAD ondersteunt Java 8 tot en met de nieuwste LTS‑releases.

## Wat is “load dwg file” in Aspose.CAD?
`Image.load()` leest de binaire DWG‑inhoud en maakt een `CadImage`‑object in het geheugen. Vanaf daar kun je lagen, blokken en onderlegger‑entiteiten verkennen zonder zelf met het DWG‑bestandformaat te hoeven werken.

## Waarom onderlegger‑vlaggen uit een DWG extraheren?
Onderlegger‑vlaggen geven aan hoe een externe referentie (zoals een DGN‑ of PDF‑onderlegger) gepositioneerd, geschaald en geroteerd is binnen de tekening. Het kennen van deze waarden stelt je in staat om:

- De exacte visuele lay-out opnieuw te creëren in een aangepaste viewer.
- Onderleggers om te zetten naar native CAD‑entiteiten voor verdere bewerking.
- Rapporten te genereren die onderlegger‑metadata bevatten voor compliance of documentatie.

## Vereisten
- **Aspose.CAD‑bibliotheek** – download van de [releases](https://releases.aspose.com/cad/java/) pagina.
- **Java Development Kit** – JDK 8 of nieuwer.
- **Een map** met de DWG‑bestanden die je wilt analyseren. Vervang `"Your Document Directory"` in de code door je eigen pad.

## Import Namespaces

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
Definieer waar je DWG‑bestanden zich bevinden. Het gebruik van een speciale map houdt het voorbeeld overzichtelijk en draagbaar.

### Stap 2: Het DWG‑bestand laden
```java
// Input file name and path
String fileName = dataDir + "BlockRefDgn.dwg";

// Load an existing DWG file and convert it into CadImage 
CadImage image = (CadImage)Image.load(fileName);
```
Hier **laden we het DWG‑bestand** `BlockRefDgn.dwg` in een `CadImage`‑instantie, klaar voor inspectie.

### Stap 3: Door DWG‑entiteiten itereren
```java
// Go through each entity inside the DWG file
for(CadBaseEntity entity : image.getEntities())
```
De lus doorloopt elke entiteit – lijnen, cirkels, blokken en onderleggers – zodat we de gewenste items kunnen selecteren.

### Stap 4: CadDgnUnderlay‑entiteiten identificeren
```java
// Check if entity is of CadDgnUnderlay type
if (entity instanceof CadDgnUnderlay)
```
Alleen `CadDgnUnderlay`‑objecten bevatten de onderlegger‑vlaggen die we zoeken, dus filteren we op deze type.

### Stap 5: Onderlegger‑informatie benaderen
```java
// Access different underlay flags 
CadUnderlay underlay = (CadUnderlay) entity;
System.out.println(underlay.getUnderlayPath());
System.out.println(underlay.getUnderlayName());
// ... (Additional underlay properties)
break;
```
Zodra we een `CadUnderlay` hebben, kunnen we het pad, de naam, het invoegpunt, de rotatie, schaalfactoren en de `UnderlayFlags`‑enum lezen die zichtbaarheid, clipping en andere renderopties aangeeft.

## Veelvoorkomende problemen & tips
- **Null onderlegger‑pad** – Zorg ervoor dat de DWG daadwerkelijk een extern bestand referereert; anders blijft het pad leeg.
- **Niet‑ondersteund onderlegger‑type** – Aspose.CAD ondersteunt momenteel DGN‑onderleggers; PDF‑onderleggers zijn nog niet via de API beschikbaar.
- **Licentie‑uitzonderingen** – Het uitvoeren van de code zonder geldige licentie voegt een watermerk toe aan geëxporteerde afbeeldingen.

## Veelgestelde vragen

**V: Kan ik Aspose.CAD voor Java gebruiken met andere CAD‑bestandsformaten?**  
A: Aspose.CAD richt zich voornamelijk op het DWG‑formaat, maar ondersteunt ook DXF, DWF en andere CAD‑formaten.

**V: Is er een proefversie beschikbaar voor Aspose.CAD voor Java?**  
A: Ja, je kunt de functies verkennen met een gratis proefversie via [hier](https://releases.aspose.com/).

**V: Hoe kan ik ondersteuning krijgen of hulp zoeken voor Aspose.CAD voor Java?**  
A: Bezoek het [Aspose.CAD‑forum](https://forum.aspose.com/c/cad/19) voor community‑ondersteuning en discussies.

**V: Zijn tijdelijke licenties beschikbaar voor Aspose.CAD voor Java?**  
A: Ja, je kunt een tijdelijke licentie verkrijgen [hier](https://purchase.aspose.com/temporary-license/).

**V: Waar vind ik de volledige documentatie voor Aspose.CAD voor Java?**  
A: Raadpleeg de [documentatie](https://reference.aspose.com/cad/java/) voor gedetailleerde informatie.

---

**Laatst bijgewerkt:** 2025-12-22  
**Getest met:** Aspose.CAD 24.12 for Java  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}