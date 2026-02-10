---
date: 2025-12-28
description: Leer hoe je DWG‑bestanden in Java‑projecten laadt en de primaire lettertype‑naam
  instelt met Aspose.CAD voor Java. Stapsgewijze gids voor perfecte CAD‑visuals.
linktitle: Substitute Font in DWG
second_title: Aspose.CAD Java API
title: Hoe een DWG‑bestand te laden in Java en het lettertype te vervangen met Aspose.CAD
url: /nl/java/cad-text-and-annotation/substitute-font-in-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hoe DWG-bestand laden in Java en lettertype vervangen met Aspose.CAD

## Introductie

Als u **load DWG file Java** applicaties nodig heeft en uw tekeningen een gepolijste uitstraling wilt geven, is het vervangen van het lettertype een snelle winst. Met Aspose.CAD voor Java kunt u de standaard tekststijl vervangen door elk systeem‑geïnstalleerd lettertype, zodat elke annotatie precies verschijnt zoals u verwacht. In deze tutorial lopen we het volledige proces door — van het laden van een DWG-bestand in Java tot het gebruik van de `setPrimaryFontName` methode om het lettertype te wijzigen.

## Snelle antwoorden
- **Welke bibliotheek heb ik nodig?** Aspose.CAD for Java.
- **Kan ik een DWG-bestand laden in Java?** Ja, roep simpelweg `Image.load()` aan op het DWG‑pad.
- **Welke methode verandert het lettertype?** `setPrimaryFontName`.
- **Heb ik een licentie nodig voor productie?** Ja, een commerciële licentie is vereist.
- **Is batchverwerking mogelijk?** Absoluut – loop door meerdere bestanden met dezelfde code.

## Wat is “load dwg file java”?

Het laden van een DWG-bestand in een Java‑omgeving betekent het lezen van de binaire CAD‑gegevens in een `Image`‑object dat Aspose.CAD kan manipuleren. Zodra het bestand is geladen, heeft u volledige programmatische toegang tot lagen, stijlen en tekstelementen.

## Waarom lettertypen vervangen in een DWG-bestand?

- **Consistentie:** Garandeert dat alle medewerkers hetzelfde lettertype zien, ongeacht hun lokale lettertype‑instelling.  
- **Leesbaarheid:** Sommige standaard CAD‑lettertypen zijn moeilijk leesbaar op schermen; overschakelen naar een helder lettertype zoals Arial verbetert de duidelijkheid.  
- **Branding:** Stem technische tekeningen af op de corporate style guides.

## Vereisten

- **Java Development Kit (JDK)** – elke recente versie (8+ aanbevolen).  
- **Aspose.CAD for Java** – download van de [website](https://releases.aspose.com/cad/java/).  
- **Voorbeeld DWG‑bestand** – een tekening die u wilt aanpassen (u kunt elk DWG‑ of DXF‑bestand gebruiken voor testen).

## Namespaces importeren

Importeer in uw Java‑project de benodigde klassen om met Aspose.CAD te werken. Deze imports geven u toegang tot het laden van afbeeldingen, CAD‑specifieke objecten en stijlmanipulatie.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject;
```

## Stapsgewijze handleiding om het lettertype te vervangen

### Stap 1: Laad uw DWG‑bestand (load dwg file java)

Eerst wijst u de API naar de locatie van uw DWG‑ (of DXF‑) bestand en laadt u het in een `CadImage`‑object.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage) Image.load(srcFile);
```

> **Pro tip:** Als u direct met DWG‑bestanden werkt, vervang dan de `.dxf`‑extensie door `.dwg` in de `srcFile`‑variabele.

### Stap 2: Doorloop de stijltabel en stel de primaire letternaam in

Elke CAD‑tekening bevat een verzameling stijlobjecten. Loop erdoorheen en gebruik de `setPrimaryFontName`‑methode (de API‑aanroep die **de primaire letternaam instelt**) om het lettertype te vervangen.

```java
for(Object style : cadImage.getStyles())
{
    // Set the font name
    ((com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject)style).setPrimaryFontName("Arial");
}
```

U kunt `"Arial"` wijzigen naar elk lettertype dat op de machine waarop de code draait geïnstalleerd is.

### Stap 3: Sla de aangepaste tekening op

Na het bijwerken van het lettertype, schrijft u de wijzigingen terug naar een nieuw DWG‑bestand (of overschrijft u het origineel).

```java
cadImage.save(dataDir + "output.dwg", new DwgOptions());
```

Het opgeslagen bestand gebruikt nu het door u opgegeven lettertype, en elke tekstannotatie wordt weergegeven met dat lettertype.

## Veelvoorkomende problemen en oplossingen

| Probleem | Oplossing |
|----------|-----------|
| **Lettertype niet toegepast** | Controleer of het lettertype is geïnstalleerd op het host‑OS en dat de spelling exact overeenkomt. |
| **`Image.load` werpt een uitzondering** | Zorg ervoor dat het bestandspad correct is en dat het bestand een ondersteund DWG/DXF‑formaat is. |
| **Prestatievertraging bij grote bestanden** | Verwerk bestanden in een aparte thread of batch ze om UI‑blokkering te voorkomen. |

## Veelgestelde vragen

**V: Heeft de `setPrimaryFontName`‑methode alleen invloed op textelementen?**  
A: Het werkt het primaire lettertype van de stijltabel bij, wat op zijn beurt alle textelementen beïnvloedt die naar die stijl verwijzen.

**V: Kan ik een aangepast lettertype gebruiken dat niet op het systeem is geïnstalleerd?**  
A: Aspose.CAD maakt gebruik van het lettertype‑register van het besturingssysteem. Om een aangepast lettertype te gebruiken, installeert u het op de machine waarop de code draait.

**V: Is het mogelijk om het lettertype alleen voor één laag te wijzigen?**  
A: Ja, u kunt stijlen filteren op laagnaam voordat u `setPrimaryFontName` aanroept.

**V: Welke versie van Aspose.CAD is vereist voor DWG 2022‑bestanden?**  
A: De nieuwste release (vanaf 2025) ondersteunt DWG 2022 volledig. Controleer altijd de release‑notes voor specifieke formatondersteuning.

**V: Hoe ga ik om met licenties in een ontwikkelomgeving?**  
A: Gebruik een tijdelijke evaluatielicentie voor testen. Voor productie embedt u uw aangeschafte licentiebestand met `License.setLicense("Aspose.Total.Java.lic");`.

**Laatst bijgewerkt:** 2025-12-28  
**Getest met:** Aspose.CAD for Java 24.11  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}