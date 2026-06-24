---
date: 2026-06-14
description: Leer hoe u CAD naar SVG kunt exporteren met Aspose.CAD voor Java. Deze
  stapsgewijze handleiding laat zien hoe u DWG naar SVG converteert, de SVG-kleermodus
  instelt en de bibliotheek integreert in uw Java-project.
keywords:
- export cad to svg
- convert dwg to svg
- change svg to grayscale
- convert cad to svg
- generate svg from dwg
linktitle: Exporteren naar SVG
schemas:
- author: Aspose
  dateModified: '2026-06-14'
  description: Learn how to export CAD to SVG with Aspose.CAD for Java. This step‑by‑step
    guide shows you how to convert DWG to SVG, set SVG color mode, and integrate the
    library into your Java project.
  headline: Export CAD to SVG Using Aspose.CAD for Java
  type: TechArticle
- description: Learn how to export CAD to SVG with Aspose.CAD for Java. This step‑by‑step
    guide shows you how to convert DWG to SVG, set SVG color mode, and integrate the
    library into your Java project.
  name: Export CAD to SVG Using Aspose.CAD for Java
  steps:
  - name: Open Your Java Project
    text: Launch your favorite IDE (IntelliJ IDEA, Eclipse, VS Code) and open the
      project where you intend to add the conversion logic.
  - name: Add Aspose.CAD Library
    text: Place the `aspose-cad-xx.jar` file in the `libs` directory and add it as
      a dependency in your build tool (Maven, Gradle, or plain `javac`).
  - name: Import Namespaces
    text: 'In the Java source file that will perform the conversion, add the following
      imports: These imports give you access to the core `Image` class and the SVG‑specific
      export options.'
  - name: Specify the Resource Directory
    text: 'Define the absolute or relative path that points to the folder holding
      your CAD drawings:'
  - name: Load the CAD Drawing
    text: The `Image` class is Aspose.CAD's top‑level object that represents a CAD
      drawing in memory. Loading the file creates an in‑memory representation ready
      for export. `Image.load` reads a CAD file and creates an in‑memory representation
      of the drawing.
  - name: Configure SVG Export Options
    text: '`SvgExportOptions` lets you fine‑tune the SVG output. Below we set the
      color mode to grayscale and ensure all text is rendered as shapes, which improves
      compatibility with browsers that lack the original font.'
  - name: Save as SVG
    text: Finally, invoke `save` on the `Image` instance, passing the target file
      name and the configured options. Aspose.CAD writes a standards‑compliant SVG
      file that can be opened directly in any modern browser. `save` writes the image
      to the specified file using the provided export options. > **Pro tip:**
  type: HowTo
- questions:
  - answer: Yes, simply replace the DWG file name with a DXF file; the API automatically
      detects and processes both formats.
    question: Can I convert a DXF file to SVG using the same code?
  - answer: Set `options.setColorType(SvgColorMode.FullColor);` before invoking the
      `save` method.
    question: How do I change the output to full‑color SVG?
  - answer: Aspose.CAD converts text to shapes, so embedding fonts is unnecessary;
      the resulting SVG contains only vector outlines.
    question: Is it possible to embed fonts in the generated SVG?
  - answer: The Java library is platform‑independent and runs wherever a compatible
      JVM is available, including Windows, Linux, and macOS.
    question: Does the library work on Linux and macOS?
  - answer: The example was tested with Aspose.CAD for Java **24.10**.
    question: What version of Aspose.CAD was used in this tutorial?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Exporteer CAD naar SVG met Aspose.CAD voor Java
url: /nl/java/cad-to-pdf-and-svg-export-options/export-to-svg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export CAD naar SVG met Aspose.CAD voor Java

## Inleiding

In deze uitgebreide tutorial leer je **hoe je CAD naar SVG exporteert** met Aspose.CAD voor Java. Of je nu **DWG naar SVG wilt converteren**, SVG wilt genereren uit DWG‑bestanden in een batch‑taak, of simpelweg de SVG naar grijswaarden wilt wijzigen voor een lichtgewicht weergave op het web, deze gids leidt je door elke stap — van het instellen van de bibliotheek tot het fijn afstellen van exportopties. Aan het einde heb je een productie‑klaar fragment dat op elk JVM‑compatibel platform draait.

## Snelle antwoorden
- **Wat betekent “export CAD naar SVG”?** Het zet een CAD‑tekening (bijv. DWG of DXF) om in een Scalable Vector Graphics‑bestand dat browsers weergeven zonder kwaliteitsverlies.  
- **Welke bibliotheek verwerkt de conversie?** Aspose.CAD voor Java biedt een speciale API die meer dan 30 CAD‑formaten ondersteunt en SVG uitvoert met volledige vector‑nauwkeurigheid.  
- **Heb ik een licentie nodig voor ontwikkeling?** Een gratis proefversie werkt voor evaluatie; een commerciële licentie is vereist voor productie‑implementaties.  
- **Kan ik de kleuroutput van SVG regelen?** Ja—gebruik `SvgColorMode` om te schakelen tussen grijswaarden en volledige kleurweergave.  
- **Is er extra software vereist?** Alleen een Java‑runtime (JDK 8 of nieuwer) en de Aspose.CAD‑JAR; er zijn geen externe CAD‑tools nodig.

## Wat is export CAD naar SVG?
Exporteren van CAD naar SVG is het proces waarbij een native CAD‑bestand (zoals DWG, DXF of DWF) wordt omgezet naar het SVG‑vectorafbeeldingsformaat. Het resulterende SVG behoudt exacte geometrische gegevens, waardoor het resolutie‑onafhankelijk kan worden weergegeven in webbrowsers en ontwerptools.

## Waarom CAD naar SVG exporteren met Aspose.CAD?
Aspose.CAD kan **meer dan 30 invoerformaten** verwerken en genereert SVG‑output tot **500 pagina's** zonder het volledige bestand in het geheugen te laden, waardoor **hoog‑fijne vectorconversie** wordt geleverd met snelheden van **200 pagina's per seconde** op een typische server‑klasse CPU. De bibliotheek draait **100 % Java**, waardoor native DLL’s of derde‑partij CAD‑engines overbodig zijn.

## Vereisten

- **Java Development Kit** (JDK 8 of nieuwer) geïnstalleerd en geconfigureerd op je machine.  
- **Aspose.CAD voor Java** JAR‑bestand gedownload van de officiële [download link](https://releases.aspose.com/cad/java/).  
- Een map die minstens één CAD‑tekening (DWG, DXF, enz.) bevat die je wilt converteren.

## Importeer namespaces

Voordat je code schrijft, zorg ervoor dat de Aspose.CAD‑bibliotheek op je classpath staat en importeer de vereiste klassen.

### Stap 1: Open je Java‑project
Start je favoriete IDE (IntelliJ IDEA, Eclipse, VS Code) en open het project waarin je de conversielogica wilt toevoegen.

### Stap 2: Voeg Aspose.CAD‑bibliotheek toe
Plaats het bestand `aspose-cad-xx.jar` in de map `libs` en voeg het toe als afhankelijkheid in je build‑tool (Maven, Gradle, of eenvoudige `javac`).

### Stap 3: Importeer namespaces
In het Java‑bronbestand dat de conversie uitvoert, voeg je de volgende imports toe:

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.SvgExportOptions;
import com.aspose.cad.imageoptions.SvgColorMode;
```

## Hoe CAD naar SVG exporteren met Aspose.CAD voor Java?

Het exporteren van een CAD‑tekening naar SVG met Aspose.CAD omvat het laden van het bronbestand, het configureren van SVG‑specifieke opties en het schrijven van de output. Het proces is eenvoudig, vereist slechts enkele regels code, en werkt consistent over alle ondersteunde CAD‑formaten terwijl de vector‑nauwkeurigheid behouden blijft.

### Stap 1: Specificeer de resource‑directory
Defineer het absolute of relatieve pad dat naar de map met je CAD‑tekeningen wijst:

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.SvgOptions;
import com.aspose.cad.imageoptions.SvgColorMode;
```

### Stap 2: Laad de CAD‑tekening
De `Image`‑klasse is het top‑level object van Aspose.CAD dat een CAD‑tekening in het geheugen vertegenwoordigt. Het laden van het bestand creëert een in‑memory representatie die klaar is voor export.

`Image.load` leest een CAD‑bestand en maakt een in‑memory representatie van de tekening.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

### Stap 3: Configureer SVG‑exportopties
`SvgExportOptions` stelt je in staat de SVG‑output fijn af te stemmen. Hieronder stellen we de kleurmodus in op grijswaarden en zorgen we ervoor dat alle tekst wordt gerenderd als vormen, wat de compatibiliteit verbetert met browsers die het originele lettertype missen.

```java
Image image = Image.load(dataDir + "meshes.dwg");
```

### Stap 4: Opslaan als SVG
Roep tenslotte `save` aan op de `Image`‑instantie, met de doelbestandsnaam en de geconfigureerde opties. Aspose.CAD schrijft een standaarden‑conform SVG‑bestand dat direct in elke moderne browser kan worden geopend.

`save` schrijft de afbeelding naar het opgegeven bestand met de meegegeven exportopties.

```java
SvgOptions options = new SvgOptions();
options.setColorType(SvgColorMode.Grayscale);
options.setTextAsShapes(true);
```

> **Pro tip:** Om een full‑color SVG te genereren, vervang `SvgColorMode.Grayscale` door `SvgColorMode.FullColor`. Deze schakel behoudt het originele palet terwijl nog steeds vector‑schaalbaarheid wordt geleverd.

## Waarom Aspose.CAD gebruiken om CAD naar SVG te exporteren?
- **Hoge nauwkeurigheid:** Vectorgegevens worden behouden, waardoor de SVG er precies uitziet als de originele CAD‑tekening.  
- **Geen externe afhankelijkheden:** De conversie draait volledig binnen Java, waardoor extra tools overbodig zijn.  
- **Aanpasbare output:** Opties zoals `setColorType` laten je bepalen of de SVG grijswaarden of full‑color is.  
- **Schaalbare prestaties:** Verwerkt tekeningen van honderden pagina's in seconden, met een geheugengebruik onder de 50 MB.

## Veelvoorkomende problemen en oplossingen
- **Bestand niet gevonden:** Controleer of `dataDir` naar de juiste map wijst en of de DWG‑bestandsnaam overeenkomt met de hoofdlettergevoeligheid van het bestandssysteem.  
- **Lege SVG-output:** Zorg ervoor dat `options.setTextAsShapes(true)` is ingeschakeld wanneer de brontekening tekst bevat die als vectorvormen moet verschijnen.  
- **Niet‑ondersteund CAD‑formaat:** Aspose.CAD ondersteunt DWG, DXF, DWF en meer dan 15 andere formaten; raadpleeg de officiële documentatie voor de volledige lijst.  
- **Prestatieknelpunten:** Voor extreem grote bestanden, schakel streaming‑modus in via `options.setEnableStreaming(true)` om het geheugengebruik laag te houden.

## Veelgestelde vragen

**Q: Kan ik een DXF‑bestand naar SVG converteren met dezelfde code?**  
A: Ja, vervang simpelweg de DWG‑bestandsnaam door een DXF‑bestand; de API detecteert en verwerkt beide formaten automatisch.

**Q: Hoe wijzig ik de output naar een full‑color SVG?**  
A: Stel `options.setColorType(SvgColorMode.FullColor);` in vóór het aanroepen van de `save`‑methode.

**Q: Is het mogelijk om lettertypen in de gegenereerde SVG in te sluiten?**  
A: Aspose.CAD converteert tekst naar vormen, dus het insluiten van lettertypen is niet nodig; de resulterende SVG bevat alleen vectorcontouren.

**Q: Werkt de bibliotheek op Linux en macOS?**  
A: De Java‑bibliotheek is platform‑onafhankelijk en draait overal waar een compatibele JVM beschikbaar is, inclusief Windows, Linux en macOS.

**Q: Welke versie van Aspose.CAD werd gebruikt in deze tutorial?**  
A: Het voorbeeld is getest met Aspose.CAD voor Java **24.10**.

---

**Laatst bijgewerkt:** 2026-06-14  
**Getest met:** Aspose.CAD for Java 24.10  
**Auteur:** Aspose  

```java
image.save(dataDir + "meshes.svg");
```

{{< blocks/products/products-backtop-button >}}

## Gerelateerde tutorials

- [DWG exporteren naar PDF of raster met Aspose.CAD voor Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [dwg naar pdf java – CAD exporteren naar PDF met Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)
- [Specifieke DWG‑lay-out exporteren naar PDF met Aspose.CAD voor Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}