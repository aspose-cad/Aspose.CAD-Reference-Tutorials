---
date: 2026-01-02
description: Leer hoe u DWG als PDF exporteert, verborgen lijnen inschakelt en DWG
  naar PDF converteert met Aspose.CAD voor Java in deze stapsgewijze tutorial.
linktitle: Export DWG as PDF with Hidden Lines Using Java
second_title: Aspose.CAD Java API
title: DWG exporteren als PDF met verborgen lijnen – Aspose.CAD voor Java
url: /nl/java/cad-text-and-formatting/support-hidden-lines-in-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export DWG als PDF met Verborgen Lijnen – Aspose.CAD voor Java

## Inleiding

In deze tutorial leer je hoe je **DWG als PDF** kunt **exporteren** terwijl je verborgen lijnen behoudt met Aspose.CAD voor Java. Of je nu **DWG naar PDF moet converteren**, een **dwg to pdf tutorial**‑stijl gids wilt maken, of simpelweg **DWG als PDF** wilt opslaan met ondersteuning voor verborgen lijnen, we lopen elke stap met je door. Aan het einde heb je een kant‑klaar oplossing die je in elk Java‑project kunt gebruiken.

## Snelle antwoorden
- **Waar gaat deze tutorial over?** Het inschakelen van verborgen‑lijn rendering tijdens het exporteren van DWG naar PDF met Aspose.CAD voor Java.  
- **Welke primaire bewerking wordt uitgevoerd?** `export dwg as pdf`.  
- **Heb ik een licentie nodig?** Een gratis proefversie werkt voor testen; een commerciële licentie is vereist voor productie.  
- **Wat zijn de vereisten?** Java‑ontwikkelomgeving, Aspose.CAD voor Java‑bibliotheek en DWG‑bestanden.  
- **Hoe lang duurt de implementatie?** Ongeveer 10‑15 minuten voor een basisopzet.

## Wat is “export dwg as pdf”?
Het exporteren van een DWG‑bestand naar PDF zet de vector‑gebaseerde CAD‑tekening om naar een draagbaar documentformaat, terwijl lagen, lijntypen en optionele rendering van verborgen lijnen behouden blijven. Dit maakt het eenvoudig om CAD‑ontwerpen te delen met belanghebbenden die mogelijk geen CAD‑software hebben.

## Waarom verborgen lijnen inschakelen bij het exporteren?
Verborgen lijnen zorgen voor een duidelijkere visuele weergave van complexe 3D‑modellen op een 2‑D‑pagina, zodat alleen zichtbare randen worden benadrukt. Dit verbetert de leesbaarheid en wordt vaak vereist voor technische documentatie.

## Vereisten

1. **Aspose.CAD voor Java** – download de bibliotheek van de officiële site [hier](https://releases.aspose.com/cad/java/).  
2. **DWG‑bestanden** – zorg dat de bron‑DWG‑tekeningen in een bekende map staan.  
3. **Java‑ontwikkelomgeving** – JDK 8+ en je favoriete IDE (Eclipse, IntelliJ, enz.).  

Nu je alles klaar hebt, duiken we in de code.

## Importeer Namespaces

Begin met het importeren van de benodigde klassen zodat je kunt werken met CAD‑afbeeldingen en PDF‑opties.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.Arrays;
import java.util.List;
```

## Stap 1: Stel je project in

Maak een Java‑project aan en voeg de Aspose.CAD‑JAR toe aan je build‑path. Definieer vervolgens de map die je DWG‑bestanden bevat.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

> **Pro tip:** Gebruik een absoluut pad of configureer een relatief pad op basis van de resources‑map van je project.

## Stap 2: Laad DWG‑bestand

Laad het bron‑DWG‑bestand in een `CadImage`‑object zodat je het kunt manipuleren.

```java
String sourceFilePath = dataDir + "Bottom_plate.dwg";
String outPath = dataDir + "Bottom_plate.pdf";
CadImage cadImage = (CadImage)Image.load(sourceFilePath);
```

## Stap 3: Configureer rasterisatie‑opties

Selecteer de lagen die je wilt opnemen en stel de paginagrootte in op de originele tekening. Hier schakelen we verborgen‑lijn rendering in door de layout te specificeren.

```java
List<String> list = Arrays.asList("Print","L1_RegMark","L2_RegMark");
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageHeight(cadImage.getHeight());
rasterizationOptions.setPageWidth(cadImage.getWidth()) ;
rasterizationOptions.setLayers(list);
```

## Stap 4: Stel PDF‑opties in

Vertel Aspose.CAD om de vectorgegevens te rasteriseren naar een PDF, gebruikmakend van de “Model”‑layout om verborgen lijnen verborgen te houden.

```java
PdfOptions pdfOptions = new PdfOptions();
rasterizationOptions.setLayouts(new String[] { "Model" });
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Stap 5: Sla het resultaat op

Exporteer tenslotte de DWG als een PDF‑bestand. De verborgen lijnen worden gerespecteerd volgens de ingestelde layout.

```java
cadImage.save(outPath, pdfOptions);
System.out.println("\nThe DWG file exported successfully to PDF.\nFile saved at " + dataDir);
```

> **Veelvoorkomende valkuil:** Het vergeten instellen van de layout op `"Model"` zorgt ervoor dat alle lijnen (inclusief verborgen) solide verschijnen in de PDF.

## Conclusie

Je hebt nu een volledige, productie‑klare methode om **DWG als PDF** te exporteren met ondersteuning voor verborgen lijnen met behulp van Aspose.CAD voor Java. Deze aanpak kan worden geïntegreerd in batch‑verwerkingstools, webservices of desktop‑applicaties om CAD‑naar‑PDF‑conversie te automatiseren.

## Veelgestelde vragen

### Q1: Kan ik Aspose.CAD voor Java gebruiken met andere CAD‑bestandsformaten?
A1: Ja, Aspose.CAD ondersteunt diverse CAD‑formaten zoals DWG, DXF, DWF en meer.

### Q2: Is er een gratis proefversie beschikbaar voor Aspose.CAD voor Java?
A2: Ja, je kunt de gratis proefversie vinden [hier](https://releases.aspose.com/).

### Q3: Hoe krijg ik ondersteuning voor Aspose.CAD voor Java?
A3: Bezoek het Aspose.CAD‑forum [hier](https://forum.aspose.com/c/cad/19) voor community‑ondersteuning.

### Q4: Waar vind ik gedetailleerde documentatie voor Aspose.CAD voor Java?
A4: Raadpleeg de documentatie [hier](https://reference.aspose.com/cad/java/).

### Q5: Kan ik een tijdelijke licentie aanschaffen voor Aspose.CAD voor Java?
A5: Ja, je kunt een tijdelijke licentie verkrijgen [hier](https://purchase.aspose.com/temporary-license/).

### Q6: Werkt deze methode ook voor het converteren van DWG naar PDF in een headless server‑omgeving?
A6: Absoluut. Omdat de code alleen de Aspose.CAD‑API gebruikt, draait hij zonder UI‑afhankelijkheden, wat ideaal is voor server‑side automatisering.

**Laatst bijgewerkt:** 2026-01-02  
**Getest met:** Aspose.CAD voor Java 24.12  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}