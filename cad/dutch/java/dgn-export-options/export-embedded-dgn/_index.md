---
date: 2026-01-07
description: Leer hoe u CAD naar PDF exporteert en DGN naar PDF converteert met Aspose.CAD
  voor Java. Stapsgewijze gids voor Java‑ontwikkelaars.
linktitle: Export Embedded DGN
second_title: Aspose.CAD Java API
title: CAD exporteren naar PDF – Ingesloten DGN exporteren met Aspose.CAD voor Java
url: /nl/java/dgn-export-options/export-embedded-dgn/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export CAD naar PDF – Embedded DGN exporteren met Aspose.CAD voor Java

## Inleiding

In deze tutorial ontdek je **hoe je CAD naar PDF exporteert** door een ingebed DGN‑bestand om te zetten naar een PDF‑document van hoge kwaliteit met Aspose.CAD voor Java. Aspose.CAD is een robuuste bibliotheek die Java‑ontwikkelaars volledige controle geeft over het manipuleren van CAD‑bestanden, of je nu **DGN naar PDF wilt converteren**, **DWG naar PDF** wilt omzetten, of simpelweg CAD‑tekeningen in andere formaten wilt renderen. Volg de stap‑voor‑stap‑gids hieronder en je kunt deze functionaliteit binnen enkele minuten in je applicaties integreren.

## Snelle antwoorden
- **Wat betekent “export CAD naar PDF”?** Het zet CAD‑tekeningen (DWG, DGN, enz.) om naar PDF‑bestanden met behoud van vectorkwaliteit.  
- **Welke bibliotheek wordt gebruikt?** Aspose.CAD voor Java.  
- **Heb ik een licentie nodig?** Een licentie is vereist voor productie; een gratis proefversie is beschikbaar.  
- **Wat zijn de belangrijkste vereisten?** Java‑ontwikkelomgeving en de Aspose.CAD voor Java‑JAR.  
- **Kan ik de output aanpassen?** Ja – je kunt lay-outs selecteren, rasterisatie‑opties instellen en PDF‑instellingen beheren.

## Wat is “export CAD naar PDF”?
Exporteren van CAD naar PDF betekent dat je een native CAD‑bestand (zoals DWG of DGN) neemt en een PDF‑document genereert dat de oorspronkelijke geometrie nauwkeurig weergeeft. De PDF kan op elk platform worden bekeken zonder CAD‑software, waardoor het ideaal is voor delen, afdrukken of archiveren.

## Waarom Aspose.CAD voor Java gebruiken om DGN naar PDF te converteren?
- **Geen externe afhankelijkheden** – werkt volledig in Java.  
- **Behoudt vectorgegevens** – PDF‑bestanden blijven scherp bij elke zoom.  
- **Fijnmazige controle** – kies specifieke lay-outs, stel rasterisatie‑DPI in en embed fonts.  
- **Enterprise‑ready** – ondersteunt grote bestanden, batchverwerking en licentie‑opties.

## Vereisten

Zorg ervoor dat je het volgende hebt voordat we beginnen:

- **Java‑ontwikkelomgeving** – JDK 8 of hoger geïnstalleerd en geconfigureerd.  
- **Aspose.CAD voor Java** – download de nieuwste JAR van [hier](https://releases.aspose.com/cad/java/).  

## Pakketten importeren

Om te beginnen moet je de benodigde klassen in je Java‑project importeren. Voeg de volgende import‑statements toe aan je bronbestand:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Hoe DGN naar PDF exporteren met Aspose.CAD voor Java?

Hieronder vind je een duidelijke, genummerde walkthrough die precies laat zien hoe je een ingebed DGN‑bestand (opgeslagen in een DWG) naar een PDF converteert.

### Stap 1: Invoer‑ en uitvoer‑paden instellen

Definieer de map die je bronbestand bevat en specificeer de DWG die de ingebedde DGN bevat.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
```

### Stap 2: DWG‑bestand laden

Laad het DWG‑bestand in een `Image`‑object. Aspose.CAD detecteert automatisch de ingebedde DGN‑gegevens.

```java
Image objImage = Image.load(fileName);
```

### Stap 3: Rasterisatie‑opties configureren

Selecteer welke lay-out(s) je in de PDF wilt opnemen. In dit voorbeeld exporteren we alleen de **Model**‑lay-out.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setLayouts(new String[] {"Model"});
```

### Stap 4: PDF‑opties configureren

Koppel de rasterisatie‑instellingen aan de PDF‑exportopties.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Stap 5: PDF‑bestand opslaan

Schrijf tenslotte de PDF naar schijf met de geconfigureerde opties.

```java
objImage.save(dataDir + "BlockRefDgn.pdf", pdfOptions);
```

## DWG naar PDF converteren – een extra tip

Als je bronbestand een gewone DWG is (zonder ingebedde DGN), kun je dezelfde code hergebruiken – wijzig simpelweg de `fileName` zodat deze naar de DWG wijst die je wilt converteren. De rasterisatie‑ en PDF‑opties blijven identiek, waardoor je een consistente **DWG naar PDF**‑workflow krijgt.

## Veelvoorkomende problemen en oplossingen

| Probleem | Reden | Oplossing |
|----------|-------|-----------|
| **Lege PDF‑output** | Lay‑naam komt niet overeen | Controleer of de lay‑naam die aan `setLayouts` wordt doorgegeven exact overeenkomt met de lay‑naam in het bronbestand (hoofdlettergevoelig). |
| **Licentie‑exception** | De proefversie wordt gebruikt zonder licentie | Pas een geldige Aspose.CAD‑licentie toe vóór het laden van de afbeelding (`License license = new License(); license.setLicense("Aspose.CAD.lic");`). |
| **Bestand niet gevonden** | Onjuist `dataDir`‑pad | Gebruik een absoluut pad of zorg dat het relatieve pad correct is ten opzichte van de werkmap van het project. |
| **Grafieken met lage resolutie** | Standaard rasterisatie‑DPI is laag | Stel `rasterizationOptions.setPageWidth/Height` of `setResolution` in om de DPI te verhogen. |

## Veelgestelde vragen

**V: Kan ik Aspose.CAD voor Java gebruiken in een commercieel project?**  
A: Ja, Aspose.CAD voor Java is een commerciële bibliotheek. Je kunt een licentie verkrijgen via [hier](https://purchase.aspose.com/buy).

**V: Is er een gratis proefversie beschikbaar?**  
A: Ja, je kunt een gratis proefversie van Aspose.CAD voor Java krijgen [hier](https://releases.aspose.com/).

**V: Hoe kan ik ondersteuning krijgen voor Aspose.CAD voor Java?**  
A: Je kunt ondersteuning zoeken bij de Aspose.CAD‑community op het [forum](https://forum.aspose.com/c/cad/19).

**V: Wat als ik een tijdelijke licentie nodig heb?**  
A: Je kunt een tijdelijke licentie verkrijgen [hier](https://purchase.aspose.com/temporary-license/).

**V: Waar vind ik de documentatie?**  
A: De documentatie is beschikbaar [hier](https://reference.aspose.com/cad/java/).

## Conclusie

Je hebt nu geleerd hoe je **CAD naar PDF exporteert**, specifiek hoe je **DGN naar PDF** en zelfs **DWG naar PDF** kunt converteren met Aspose.CAD voor Java. Door de bovenstaande stappen te volgen, kun je naadloze CAD‑naar‑PDF‑conversie in elke Java‑gebaseerde oplossing integreren, waardoor je gebruikers hoogwaardige PDF‑bestanden krijgen zonder extra CAD‑software.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Laatst bijgewerkt:** 2026-01-07  
**Getest met:** Aspose.CAD voor Java 24.12  
**Auteur:** Aspose