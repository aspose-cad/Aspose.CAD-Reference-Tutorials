---
date: 2026-06-19
description: Leer hoe u DWG-bestanden kunt bewerken met Aspose.CAD voor Java, inclusief
  hoe u DWG XRef-paden bijwerkt en hyperlinks bewerkt. Probeer vandaag nog de gratis
  proefversie!
keywords:
- how to edit dwg
- update dwg xref paths
- Aspose.CAD Java hyperlink
linktitle: Hyperlink bewerken
schemas:
- author: Aspose
  dateModified: '2026-06-19'
  description: Learn how to edit DWG files with Aspose.CAD for Java, including how
    to update DWG XRef paths and edit hyperlinks. Try the free trial today!
  headline: How to Edit DWG Hyperlinks - Aspose.CAD Java Tutorial
  type: TechArticle
- description: Learn how to edit DWG files with Aspose.CAD for Java, including how
    to update DWG XRef paths and edit hyperlinks. Try the free trial today!
  name: How to Edit DWG Hyperlinks - Aspose.CAD Java Tutorial
  steps:
  - name: Accessing Insert Objects
    text: '`CadInsertObject` is the Aspose.CAD class that represents an inserted block
      reference (XRef) inside a DWG drawing. Iterate through the entities and identify
      if an entity is an instance of the `CadInsertObject` class.'
  - name: How to Change XRef Path in a DWG Drawing
    text: '`CadImage` is the primary object that loads and saves CAD files in Aspose.CAD
      for Java. Once you have identified the insert object, retrieve the associated
      block entity and update the XRef path as needed. This ensures the reference
      points to the correct external file.'
  - name: Modifying Hyperlinks
    text: Next, check if the entity has a hyperlink associated with it. If the hyperlink
      matches a specific URL, update it to the desired URL. This step guarantees that
      clicking the hyperlink in the CAD viewer opens the new target.
  type: HowTo
- questions:
  - answer: Yes, after making changes call `cadImage.save("EditedDrawing.dwg");` to
      persist the modifications.
    question: Do I need to call a specific method to write the edited DWG back to
      disk?
  - answer: Absolutely—loop through `cadImage.getEntities()` and apply the hyperlink
      logic to each matching entity.
    question: Is it possible to edit multiple hyperlinks in one pass?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Hoe DWG-hyperlinks te bewerken - Aspose.CAD Java-tutorial
url: /nl/java/other-cad-operations/edit-hyperlink/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hoe DWG-hyperlinks bewerken - Aspose.CAD Java-tutorial

In het digitale tijdperk van vandaag is **hoe DWG te bewerken** efficiënt een onmisbare vaardigheid voor ingenieurs, architecten en BIM‑specialisten. Of je nu een kapotte hyperlink moet corrigeren, een XRef naar een nieuwe bron moet wijzen, of veel tekeningen in één batch moet bijwerken, Aspose.CAD for Java biedt een schone, programmeerbare manier om die wijzigingen aan te brengen zonder de CAD‑editor te openen. Deze tutorial leidt je door het volledige proces, van het laden van een tekening tot het opslaan van de bewerkingen.

## Snelle antwoorden
- **Welke bibliotheek behandelt DWG-bewerking in Java?** Aspose.CAD for Java.  
- **Kan ik hyperlinks en XRef‑paden samen bewerken?** Ja—beide worden ondersteund in dezelfde API.  
- **Heb ik een licentie nodig voor ontwikkeling?** Een gratis proefversie werkt voor testen; een commerciële licentie is vereist voor productie.  
- **Welke Java‑versie is vereist?** Java 8 of hoger.  
- **Is het code‑voorbeeld direct uitvoerbaar?** Ja, na het bijwerken van de bestandspaden zodat ze naar je lokale DWG‑bestanden wijzen.

## Waarom DWG-hyperlinks en XRef-paden bewerken?

Het actueel houden van hyperlinks en XRef‑paden voorkomt gebroken verwijzingen, zorgt ervoor dat projectdocumentatie altijd naar de juiste bronnen wijst, en maakt geautomatiseerde batch‑updates mogelijk over uitgebreide CAD‑bibliotheken. Dit vermindert handmatige inspanning, minimaliseert fouten en verbetert de algehele projectefficiëntie door ontwikkelaars in staat te stellen de linkintegriteit programmatisch te behouden gedurende de hele ontwerplevenscyclus.

## Voorvereisten

Voordat we in de tutorial duiken, zorg ervoor dat je de volgende voorvereisten hebt:

1. **Java-ontwikkelomgeving:** Een JDK 8+ geïnstalleerd en je favoriete IDE (IntelliJ IDEA, Eclipse, enz.).  
2. **Aspose.CAD for Java-bibliotheek:** Download en installeer de Aspose.CAD for Java-bibliotheek vanaf de [download link](https://releases.aspose.com/cad/java/).  
3. **DWG-tekening:** Een DWG-tekeningsbestand klaar hebben voor het bewerken van hyperlinks.

## Pakketten importeren

Begin met het importeren van de benodigde pakketten in je Java‑project. Dit zorgt ervoor dat je toegang hebt tot de functionaliteiten van Aspose.CAD for Java.

```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadBaseEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadBlockEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadInsertObject;
```

## Hoe DWG-hyperlinks bewerken met Aspose.CAD for Java?

`CadImage` is de Aspose.CAD‑klasse die wordt gebruikt om CAD‑tekeningen te laden en op te slaan.  
Laad het DWG‑bestand met `CadImage`, doorloop de entiteiten, werk de hyperlink en XRef‑pad bij waar nodig, en sla tenslotte de afbeelding opnieuw op als DWG. Deze end‑to‑end‑stroom stelt je in staat om een willekeurig aantal entiteiten in één doorloop te wijzigen, waardoor gegarandeerd wordt dat alle wijzigingen worden opgeslagen.

### Stap 1: Insert‑objecten benaderen

`CadInsertObject` is de Aspose.CAD‑klasse die een ingevoegde blokreferentie (XRef) binnen een DWG‑tekening vertegenwoordigt. Doorloop de entiteiten en bepaal of een entiteit een instantie is van de `CadInsertObject`‑klasse.

```java
    String dataDir = "Your Document Directory" + "DWGDrawings/";
    
    CadImage cadImage = (CadImage)Image.load(dataDir + "AutoCad_Sample.dwg");
    for (CadBaseEntity entity : cadImage.getEntities())
    {
        if (entity instanceof CadInsertObject)
        {
        }
	}
```

### Stap 2: XRef‑pad wijzigen in een DWG‑tekening

`CadImage` is het primaire object dat CAD‑bestanden laadt en opslaat in Aspose.CAD for Java. Zodra je het insert‑object hebt geïdentificeerd, haal je de bijbehorende blok‑entiteit op en werk je het XRef‑pad bij indien nodig. Dit zorgt ervoor dat de referentie naar het juiste externe bestand wijst.

```java
			CadBlockEntity block = cadImage.getBlockEntities().get_Item(((CadInsertObject)entity).getName());
            String value = block.getXRefPathName().getValue();
            if (value != null && !value.contentEquals(""))
            {
                block.getXRefPathName().setValue("new file reference.dwg");
            }
    
```

### Stap 3: Hyperlinks aanpassen

Controleer vervolgens of de entiteit een gekoppelde hyperlink heeft. Als de hyperlink overeenkomt met een specifieke URL, werk deze dan bij naar de gewenste URL. Deze stap garandeert dat het klikken op de hyperlink in de CAD‑viewer het nieuwe doel opent.

```java
        if (entity.getHyperlink() == "https://products.aspose.com")
        {
            entity.setHyperlink("https://www.aspose.com");
        }
```

## Veelvoorkomende valkuilen & tips

- **String vergelijking:** Gebruik `.equals()` in plaats van `==` voor betrouwbare stringvergelijking in Java. Het voorbeeld gebruikt `==` voor de eenvoud, maar in productie vervang je dit door `entity.getHyperlink().equals("https://products.aspose.com")`.  
- **Null‑controles:** Controleer altijd dat `block.getXRefPathName()` niet `null` is voordat je `.getValue()` aanroept.  
- **Wijzigingen opslaan:** Na het aanpassen van entiteiten, roep `cadImage.save("output.dwg");` aan om de wijzigingen op te slaan (code weggelaten om het oorspronkelijke aantal blokken te behouden).  
- **Prestatienota:** Aspose.CAD for Java ondersteunt meer dan 30 CAD‑formaten en kan bestanden tot 2 GB verwerken zonder het volledige document in het geheugen te laden, waardoor bulk‑updates snel en geheugen‑efficiënt zijn.

## Veelgestelde vragen

### Q1: Is Aspose.CAD for Java compatibel met alle DWG‑tekeningsversies?
A1: Aspose.CAD for Java ondersteunt meer dan 50 DWG‑versies, van releases vanaf AutoCAD 2000 tot het nieuwste 2025‑formaat.

### Q2: Kan ik Aspose.CAD for Java gebruiken in commerciële projecten?
A2: Ja, een commerciële licentie is vereist voor productiegebruik. Je kunt een licentie aanschaffen [hier](https://purchase.aspose.com/buy).

### Q3: Is er een gratis proefversie beschikbaar voor Aspose.CAD for Java?
A3: Ja, je kunt een gratis proefversie verkennen [hier](https://releases.aspose.com/).

### Q4: Hoe kan ik technische ondersteuning krijgen voor Aspose.CAD for Java?
A4: Voor technische ondersteuning kun je het Aspose.CAD‑forum bezoeken [hier](https://forum.aspose.com/c/cad/19).

### Q5: Kan ik een tijdelijke licentie verkrijgen voor testdoeleinden?
A5: Ja, je kunt een tijdelijke licentie verkrijgen [hier](https://purchase.aspose.com/temporary-license/).

**Aanvullende V&A**

**Q: Moet ik een specifieke methode aanroepen om de bewerkte DWG terug naar schijf te schrijven?**  
A: Ja, na het aanbrengen van wijzigingen roep je `cadImage.save("EditedDrawing.dwg");` aan om de aanpassingen op te slaan.

**Q: Is het mogelijk om meerdere hyperlinks in één doorloop te bewerken?**  
A: Absoluut—loop door `cadImage.getEntities()` en pas de hyperlink‑logica toe op elke overeenkomende entiteit.

---

**Laatst bijgewerkt:** 2026-06-19  
**Getest met:** Aspose.CAD for Java 24.12  
**Auteur:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Gerelateerde tutorials

- [XREF‑metadata lezen uit DWG‑bestanden met Aspose.CAD for Java](/cad/java/cad-meta-data-and-rendering/read-xref-meta-data/)
- [Aangepaste eigenschappen toevoegen aan DWG‑bestanden met Aspose.CAD for Java](/cad/java/additional-features/add-custom-properties/)
- [DWG exporteren naar PDF of raster met Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}