---
date: 2026-03-02
description: Ontgrendel het potentieel van Aspose.CAD voor Java. Exporteer moeiteloos
  OLE‑objecten en **sla CAD op als PNG**. Download nu voor naadloos CAD‑gegevensbeheer.
linktitle: Export OLE Objects from CAD
second_title: Aspose.CAD Java API
title: CAD opslaan als PNG – OLE-objecten exporteren met Aspose.CAD voor Java
url: /nl/java/cad-to-pdf-and-svg-export-options/export-ole-objects-from-cad/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD opslaan als PNG – OLE-objecten exporteren met Aspose.CAD voor Java

## Inleiding

In de dynamische wereld van Computer-Aided Design (CAD) is het efficiënt beheren en extraheren van OLE (Object Linking and Embedding) objecten—en het kunnen **CAD opslaan als PNG**—cruciaal voor downstream workflows zoals rapportage, webpreview of archivering. Aspose.CAD voor Java biedt een krachtige, code‑first oplossing die je zowel OLE‑objecten laat exporteren als CAD‑tekeningen converteert naar PNG‑afbeeldingen van hoge kwaliteit in slechts een paar regels code.

## Snelle antwoorden
- **Wat doet Aspose.CAD?** Het leest, bewerkt en converteert CAD‑bestanden (DWG, DXF, DGN, etc.) zonder dat native CAD‑software nodig is.  
- **Kan ik CAD opslaan als PNG?** Ja—gebruik `PngOptions` samen met `CadRasterizationOptions` om elke layout te rasteren.  
- **Hoe OLE‑objecten exporteren?** Laad het CAD‑bestand met `Image.load` en sla elke layout die OLE bevat op als PNG.  
- **Heb ik een licentie nodig?** Een gratis proefversie is beschikbaar; een commerciële licentie verwijdert de evaluatiebeperkingen.  
- **Welke Java‑versie is vereist?** Java 8 of hoger wordt volledig ondersteund.

## Wat is **CAD opslaan als PNG**?
CAD opslaan als PNG betekent het rasteren van vector‑gebaseerde CAD‑tekeningen naar een pixel‑gebaseerde PNG‑afbeelding. Deze conversie is nuttig wanneer je een lichtgewicht, universeel bekijkbaar formaat nodig hebt voor webpagina's, mobiele apps of documentatie.

## Waarom Aspose.CAD voor Java gebruiken om **CAD naar PNG te converteren**?
- **Geen CAD‑installatie nodig** – de bibliotheek werkt volledig in Java.  
- **Behoudt lay‑out getrouwheid** – je kunt specifieke lay-outs kiezen, DPI regelen en de lijnkwaliteit behouden.  
- **Batchverwerking** – itereren over meerdere bestanden met een eenvoudige lus.  
- **Export OLE‑objecten** – OLE‑inhoud ingebed in DWG/DXF‑bestanden wordt automatisch gerenderd in de PNG‑output.

## Voorvereisten

Voordat je aan de tutorial begint, zorg ervoor dat je de volgende voorvereisten hebt:

- **Java‑omgeving** – Zorg ervoor dat je een Java‑ontwikkelomgeving op je machine hebt ingesteld.  
- **Aspose.CAD voor Java** – Download en installeer de Aspose.CAD voor Java‑bibliotheek. Je kunt de bibliotheek vinden op de [download link](https://releases.aspose.com/cad/java/).  
- **CAD‑bestanden** – Bereid de CAD‑bestanden voor die OLE‑objecten bevatten die je wilt exporteren.

## Namespaces importeren

Om te beginnen, importeer je de benodigde namespaces in je Java‑project. Deze namespaces bieden de essentiële klassen en functionaliteiten die nodig zijn voor het werken met CAD‑bestanden met Aspose.CAD.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Laten we nu het proces van het exporteren van OLE‑objecten uit CAD in meerdere stappen uiteenzetten:

## Hoe **CAD opslaan als PNG** en OLE‑objecten exporteren

### Stap 1: Stel je documentdirectory in

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

Zorg ervoor dat je `"Your Document Directory"` vervangt door het pad naar de directory die je CAD‑bestanden bevat.

### Stap 2: Definieer CAD‑bestandsnamen

```java
String[] files = new String[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

Specificeer de namen van de CAD‑bestanden die je wilt verwerken in de `files`‑array.

### Stap 3: Stel PNG‑exportopties in

```java
PngOptions pngOptions = new PngOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.setLayouts(new String[] { "Layout1" });
```

Configureer de PNG‑exportopties, inclusief vector‑rasterisatie en lay‑outinstellingen. Deze opties maken het mogelijk om **CAD naar PNG te converteren** met de gewenste kwaliteit.

### Stap 4: Doorloop CAD‑bestanden

```java
for(String file : files)
{
    CadImage cadImage = (CadImage)Image.load(dataDir + file);
    cadImage.save(dataDir + file + "_out.png", pngOptions);
}
```

Doorloop elk opgegeven CAD‑bestand, laad het met Aspose.CAD en sla de OLE‑objecten op als PNG‑afbeeldingen. Deze lus toont een eenvoudige manier om **DWG naar PNG te converteren** in bulk.

## Veelvoorkomende problemen en oplossingen

| Issue | Cause | Solution |
|-------|-------|----------|
| **Lege PNG-uitvoer** | Lay-outnaam komt niet overeen | Controleer of de lay-outnaam (`"Layout1"`) bestaat in de bron‑DWG. |
| **Ontbrekende OLE‑graphics** | OLE‑objecten zijn opgeslagen in een andere lay-out | Neem alle relevante lay-outs op in `rasterizationOptions.setLayouts(...)`. |
| **Out‑of‑memory‑fout bij grote bestanden** | Hoge DPI‑instellingen | Verlaag DPI via `rasterizationOptions.setResolution(...)` of verwerk bestanden één voor één. |

## Veelgestelde vragen

**V: Is Aspose.CAD compatibel met alle CAD‑bestandsformaten?**  
A: Aspose.CAD ondersteunt verschillende CAD‑formaten, waaronder DWG, DXF en DGN. Raadpleeg de [documentation](https://reference.aspose.com/cad/java/) voor de volledige lijst.

**V: Kan ik de exportinstellingen voor OLE‑objecten aanpassen?**  
A: Ja, Aspose.CAD biedt uitgebreide opties om exportinstellingen aan te passen, zodat je de output kunt afstemmen op je specifieke eisen.

**V: Is er een gratis proefversie beschikbaar voor Aspose.CAD?**  
A: Ja, je kunt de mogelijkheden van Aspose.CAD verkennen door een gratis proefversie te verkrijgen via [hier](https://releases.aspose.com/).

**V: Waar kan ik community‑ondersteuning krijgen voor Aspose.CAD?**  
A: Word lid van de Aspose.CAD‑community op het [forum](https://forum.aspose.com/c/cad/19) om hulp te zoeken en je ervaringen te delen.

**V: Hoe kan ik een licentie voor Aspose.CAD aanschaffen?**  
A: Bezoek de [aankooppagina](https://purchase.aspose.com/buy) om een licentie te verkrijgen die past bij je ontwikkelbehoeften.

## Conclusie

Met deze eenvoudige maar krachtige stappen kun je moeiteloos **CAD opslaan als PNG** terwijl je OLE‑objecten exporteert uit CAD‑bestanden met Aspose.CAD voor Java. Deze veelzijdige tool stelt ontwikkelaars in staat CAD‑gegevens efficiënt te beheren, waardoor nieuwe mogelijkheden ontstaan in CAD‑applicatieontwikkeling en downstream beeld‑gebaseerde workflows.

---

**Laatst bijgewerkt:** 2026-03-02  
**Getest met:** Aspose.CAD for Java 24.12  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}