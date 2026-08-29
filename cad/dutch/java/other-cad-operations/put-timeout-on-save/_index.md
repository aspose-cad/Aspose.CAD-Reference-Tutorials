---
date: 2026-06-19
description: Leer hoe u een time-out instelt bij het opslaan van CAD-tekeningen met
  Aspose.CAD voor Java. Verhoog de prestaties, voorkom vastlopers en exporteer CAD
  efficiënt naar PDF.
keywords:
- how to set timeout
- convert dwg to pdf
- export cad to pdf
linktitle: Time-out instellen bij opslaan
schemas:
- author: Aspose
  dateModified: '2026-06-19'
  description: Learn how to set timeout on saving CAD drawings with Aspose.CAD for
    Java. Boost performance, avoid hangs, and export CAD to PDF efficiently.
  headline: How to Set Timeout on Save for CAD with Aspose.CAD
  type: TechArticle
- description: Learn how to set timeout on saving CAD drawings with Aspose.CAD for
    Java. Boost performance, avoid hangs, and export CAD to PDF efficiently.
  name: How to Set Timeout on Save for CAD with Aspose.CAD
  steps:
  - name: Set Source and Output Directories
    text: Ensure you have the correct source and output directories for your CAD drawings.
  - name: Create Interruption Token Source
    text: Initialize an interruption token source to manage interruptions during the
      save operation.
  - name: Load CAD Drawing
    text: The `CadImage` class is Aspose.CAD's core object that represents a CAD drawing
      in memory, offering methods for rendering and conversion.
  - name: Configure Rasterization Options
    text: '`CadRasterizationOptions` specifies how the CAD drawing is rasterized into
      an image. Configure rasterization options for the CAD drawing.'
  - name: Configure PDF Options
    text: '`PdfOptions` defines settings for saving a CAD drawing as a PDF document.
      Set up PDF options with vector rasterization options and the interruption token.'
  - name: Save Drawing with Timeout
    text: Save the CAD drawing to a PDF file with the specified timeout.
  - name: Handle Interruption
    text: '`OperationCanceledException` is thrown when a save operation exceeds the
      specified timeout. Create a thread to handle the save operation and interrupt
      it after a specified timeout.'
  type: HowTo
- questions:
  - answer: Yes, wrap each conversion in its own thread with a separate interruption
      token to enforce per‑file time limits.
    question: Can I use this feature to convert DWG to PDF in a batch job?
  - answer: The timeout mechanism is tied to the `InterruptionTokenSource` and works
      with any format that respects the token, including PDF, PNG, and SVG.
    question: Does the timeout work on all output formats?
  - answer: Aspose.CAD automatically discards incomplete output, so you won’t end
      up with corrupted PDFs.
    question: What happens to partially written files after a timeout?
  - answer: Yes, a valid Aspose.CAD license is required for commercial deployments;
      a free trial is available for evaluation.
    question: Is a license required for production use?
  - answer: The official Aspose.CAD documentation provides additional code snippets
      and best‑practice guidelines.
    question: Where can I find more examples of using interruption tokens?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Hoe een time-out instellen bij opslaan voor CAD met Aspose.CAD
url: /nl/java/other-cad-operations/put-timeout-on-save/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hoe stel je een time-out in bij het opslaan voor CAD met Aspose.CAD

## Inleiding

In deze uitgebreide gids leer je **how to set timeout** bij het opslaan van CAD-tekeningen met Aspose.CAD voor Java. Het toepassen van een time‑out voorkomt dat langdurige opslaan‑bewerkingen je applicatie laten hangen, wat vooral belangrijk is wanneer je **export CAD to PDF** of **convert DWG to PDF** moet uitvoeren in batch‑verwerkingsscenario's. Aspose.CAD voor Java ondersteunt meer dan 50 CAD-formaten en kan multi‑honderd‑pagina bestanden verwerken zonder het volledige document in het geheugen te laden, waardoor je voorspelbare prestaties en resource‑gebruik krijgt.

## Snelle antwoorden
- **What does the timeout do?** Het onderbreekt de opslaan‑operatie na een gespecificeerde periode, waardoor de thread wordt vrijgegeven en resource‑lekken worden voorkomen.  
- **Which class controls the timeout?** `InterruptionTokenSource` levert het annulerings‑token dat door de opslaan‑routine wordt gebruikt.  
- **Can I still export CAD to PDF after a timeout?** Ja – je kunt de onderbrekings‑exception opvangen en opnieuw proberen of de fout loggen.  
- **Do I need a special license?** Een reguliere Aspose.CAD‑licentie is voldoende; de time‑out‑functie is ingebouwd.  
- **Is this approach thread‑safe?** Ja, wanneer elke opslaan in zijn eigen thread met zijn eigen token wordt uitgevoerd.

## Wat is een time-out bij CAD‑opslaan‑operaties?
Een time‑out is een configureerbare tijdslimiet die, wanneer overschreden, het opslaan‑proces dwingt te stoppen en een onderbrekings‑exception te genereren. Dit beschermt je Java‑applicatie tegen oneindige vastlopers veroorzaakt door complexe tekeningen of I/O‑knelpunten.

## Waarom een time‑out instellen bij het opslaan van CAD‑bestanden?
Aspose.CAD kan **convert DWG to PDF** en **export CAD to PDF** in minder dan een seconde voor typische tekeningen, maar extreem grote of corrupte bestanden kunnen minuten duren. Door een time‑out te definiëren, garandeer je dat elke enkele opslaan bijvoorbeeld niet langer dan 30 seconden duurt, waardoor de algehele batch‑doorvoer stabiel blijft en thread‑verarming wordt voorkomen.

## Voorvereisten

Voordat je aan de tutorial begint, zorg ervoor dat je de volgende voorvereisten hebt:
- **Aspose.CAD for Java Library** – Zorg ervoor dat je de Aspose.CAD for Java‑bibliotheek in je project hebt geïntegreerd. Je kunt de bibliotheek downloaden van de [website](https://releases.aspose.com/cad/java/).
- **Development Environment** – Richt je Java‑ontwikkelomgeving in met alle benodigde tools en afhankelijkheden.

## Importeer pakketten

Om te beginnen, importeer je de vereiste pakketten in je Java‑project. Voeg de volgende regels toe aan het begin van je Java‑bestand:

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterruptionTokenSource;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.concurrent.TimeUnit;
```

Laten we nu de voorbeeldcode stap‑voor‑stap ontleden:

## Hoe stel je een time‑out in bij het opslaan van CAD‑tekeningen?

Laad je CAD‑bestand, maak een `InterruptionTokenSource` aan met de gewenste time‑out, en geef het token door aan de PDF‑opslaan‑opties. Als de bewerking de time‑out overschrijdt, gooit Aspose.CAD een `OperationCanceledException`, die je kunt opvangen om de fout op een nette manier af te handelen.

### Stap 1: Stel bron‑ en uitvoermappen in

```java
final String SourceDir = Utils.getDataDir_DWGDrawings();
final String OutputDir = Utils.getDataDir_Output();
```

Zorg ervoor dat je de juiste bron‑ en uitvoermappen voor je CAD‑tekeningen hebt.

### Stap 2: Maak Interruption Token Source aan

```java
final InterruptionTokenSource source = new com.aspose.cad.InterruptionTokenSource();
```

Initialiseer een interruption token source om onderbrekingen tijdens de opslaan‑operatie te beheren.

### Stap 3: Laad CAD‑tekening

De `CadImage`‑klasse is het kernobject van Aspose.CAD dat een CAD‑tekening in het geheugen vertegenwoordigt, en biedt methoden voor rendering en conversie.

```java
final CadImage cadImageBig = (CadImage)Image.load(SourceDir + "Drawing11.dwg");
```

### Stap 4: Configureer rasterisatie‑opties

`CadRasterizationOptions` specificeert hoe de CAD‑tekening wordt gerasterd naar een afbeelding.

```java
CadRasterizationOptions rasterizationOptionsBig = new CadRasterizationOptions();
rasterizationOptionsBig.setPageWidth(cadImageBig.getSize().getWidth() / 2);
rasterizationOptionsBig.setPageHeight(cadImageBig.getSize().getHeight() / 2);
```

Configureer rasterisatie‑opties voor de CAD‑tekening.

### Stap 5: Configureer PDF‑opties

`PdfOptions` definieert instellingen voor het opslaan van een CAD‑tekening als een PDF‑document.

```java
final PdfOptions CADfBig = new PdfOptions();
CADfBig.setVectorRasterizationOptions(rasterizationOptionsBig);
CADfBig.setInterruptionToken(source.getToken());
```

Stel PDF‑opties in met vector‑rasterisatie‑opties en het interruption token.

### Stap 6: Sla tekening op met time‑out

```java
cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
```

Sla de CAD‑tekening op als een PDF‑bestand met de opgegeven time‑out.

### Stap 7: Handel onderbreking af

`OperationCanceledException` wordt gegooid wanneer een opslaan‑operatie de opgegeven time‑out overschrijdt.

```java
java.lang.Thread thread = new java.lang.Thread(new Runnable() {
    @Override
    public void run() {
        try {
            cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
        } catch (Throwable th) {
            System.out.println("interrupted !!!");
        }
    }
});
thread.start();
TimeUnit.SECONDS.sleep(3);
source.interrupt();
thread.join();
```

Maak een thread aan om de opslaan‑operatie af te handelen en onderbreek deze na een opgegeven time‑out.

## Veelvoorkomende problemen en oplossingen

- **Timeout Too Short** – Als je vaak onderbrekingen krijgt, verhoog dan de time‑out‑waarde om grotere tekeningen te kunnen verwerken.  
- **InterruptedException Not Caught** – Zorg ervoor dat je de opslaan‑aanroep altijd in een try‑catch‑blok voor `OperationCanceledException` wikkelt om te voorkomen dat de applicatie crasht.  
- **Memory Consumption** – Gebruik `PdfOptions.setVectorRasterizationOptions` om de output te streamen in plaats van het hele bestand in het geheugen te laden.

## Veelgestelde vragen

**Q: Kan ik deze functie gebruiken om DWG naar PDF te converteren in een batch‑taak?**  
A: Ja, plaats elke conversie in zijn eigen thread met een apart interruption token om per‑bestand tijdslimieten af te dwingen.

**Q: Werkt de time‑out voor alle uitvoerformaten?**  
A: Het time‑out‑mechanisme is gekoppeld aan de `InterruptionTokenSource` en werkt met elk formaat dat het token respecteert, inclusief PDF, PNG en SVG.

**Q: Wat gebeurt er met gedeeltelijk geschreven bestanden na een time‑out?**  
A: Aspose.CAD verwijdert automatisch onvolledige output, zodat je geen corrupte PDF‑bestanden krijgt.

**Q: Is een licentie vereist voor productiegebruik?**  
A: Ja, een geldige Aspose.CAD‑licentie is vereist voor commerciële implementaties; een gratis proefversie is beschikbaar voor evaluatie.

**Q: Waar kan ik meer voorbeelden vinden van het gebruik van interruption tokens?**  
A: De officiële Aspose.CAD‑documentatie biedt extra code‑fragmenten en best‑practice richtlijnen.

## Aanvullende bronnen

- [releases page](https://releases.aspose.com/cad/java/) – Direct downloadpagina voor de nieuwste Aspose.CAD voor Java releases.  
- [documentation](https://reference.aspose.com/cad/java/) – Volledige API-referentie en ontwikkelaarsgidsen.  
- [this link](https://releases.aspose.com/) – Algemene Aspose productreleases.  
- [here](https://purchase.aspose.com/temporary-license/) – Verkrijg een tijdelijke licentie voor testen.  
- [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) – Community‑ondersteuning en discussies.

## Conclusie

Je hebt nu geleerd **how to set timeout** voor het opslaan van CAD‑tekeningen met Aspose.CAD voor Java. Door een `InterruptionTokenSource` in je workflow te integreren kun je betrouwbaar **export CAD to PDF** of **convert DWG to PDF** uitvoeren zonder risico op langdurige vastlopers, waardoor je applicatie responsief en schaalbaar blijft.

---

**Laatst bijgewerkt:** 2026-06-19  
**Getest met:** Aspose.CAD for Java 24.12  
**Auteur:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Gerelateerde tutorials

- [Export DWG naar PDF of raster met Aspose.CAD voor Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Export specifieke DWG‑lay-out naar PDF met Aspose.CAD voor Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Converteer DWG naar PNG en andere rasterformaten met Aspose.CAD voor Java](/cad/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}