---
title: Time-out bij opslaan voor CAD met Aspose.CAD
linktitle: Zet Time-out op Opslaan
second_title: Aspose.CAD Java-API
description: Leer hoe u de prestaties van uw Java-applicatie kunt verbeteren met Aspose.CAD. Stel een time-out in voor het opslaan van CAD-tekeningen. Volg onze stapsgewijze handleiding.
type: docs
weight: 15
url: /nl/java/other-cad-operations/put-timeout-on-save/
---
## Invoering

Welkom bij de tutorial over het instellen van een time-out bij het opslaan met Aspose.CAD voor Java. In deze handleiding begeleiden we u bij het instellen van een time-out voor het opslaan van CAD-tekeningen om de prestaties van uw toepassing te verbeteren. Aspose.CAD voor Java is een krachtige bibliotheek waarmee u naadloos met CAD-bestanden in uw Java-toepassingen kunt werken.

## Vereisten

Voordat u in de zelfstudie duikt, moet u ervoor zorgen dat u aan de volgende vereisten voldoet:
-  Aspose.CAD voor Java-bibliotheek: Zorg ervoor dat de Aspose.CAD voor Java-bibliotheek in uw project is geïntegreerd. U kunt de bibliotheek downloaden via de[website](https://releases.aspose.com/cad/java/).
- Ontwikkelomgeving: Richt uw Java-ontwikkelomgeving in met alle benodigde tools en afhankelijkheden.

## Pakketten importeren

Importeer om te beginnen de vereiste pakketten in uw Java-project. Voeg de volgende regels toe aan het begin van uw Java-bestand:

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterruptionTokenSource;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.concurrent.TimeUnit;
```

Laten we nu de voorbeeldcode opsplitsen in stapsgewijze instructies:

## Stap 1: Stel de bron- en uitvoermappen in

```java
final String SourceDir = Utils.getDataDir_DWGDrawings();
final String OutputDir = Utils.getDataDir_Output();
```

Zorg ervoor dat u over de juiste bron- en uitvoermappen voor uw CAD-tekeningen beschikt.

## Stap 2: Maak een onderbrekingstokenbron

```java
final InterruptionTokenSource source = new com.aspose.cad.InterruptionTokenSource();
```

Initialiseer een onderbrekingstokenbron om onderbrekingen tijdens de opslagbewerking te beheren.

## Stap 3: CAD-tekening laden

```java
final CadImage cadImageBig = (CadImage)Image.load(SourceDir + "Drawing11.dwg");
```

 Laad de CAD-tekening in een`CadImage` voorwerp.

## Stap 4: Configureer rasterisatieopties

```java
CadRasterizationOptions rasterizationOptionsBig = new CadRasterizationOptions();
rasterizationOptionsBig.setPageWidth(cadImageBig.getSize().getWidth() / 2);
rasterizationOptionsBig.setPageHeight(cadImageBig.getSize().getHeight() / 2);
```

Configureer rasteropties voor de CAD-tekening.

## Stap 5: Configureer PDF-opties

```java
final PdfOptions CADfBig = new PdfOptions();
CADfBig.setVectorRasterizationOptions(rasterizationOptionsBig);
CADfBig.setInterruptionToken(source.getToken());
```

Stel PDF-opties in met vectorrasteropties en het onderbrekingstoken.

## Stap 6: Tekening opslaan met time-out

```java
cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
```

Sla de CAD-tekening op in een PDF-bestand met de opgegeven time-out.

## Stap 7: Handel de onderbreking af

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

Maak een thread om de opslagbewerking af te handelen en onderbreek deze na een opgegeven time-out.

## Conclusie

Gefeliciteerd! U hebt met succes geleerd hoe u een time-out kunt instellen bij het opslaan met Aspose.CAD voor Java. Deze functie kan de efficiëntie van uw CAD-gerelateerde toepassingen aanzienlijk verbeteren.

## Veelgestelde vragen

### V1: Hoe kan ik Aspose.CAD voor Java downloaden?

 A1: U kunt het downloaden van de[releases pagina](https://releases.aspose.com/cad/java/).

### V2: Waar kan ik de documentatie voor Aspose.CAD voor Java vinden?

 A2: Raadpleeg de[documentatie](https://reference.aspose.com/cad/java/) voor uitgebreide informatie.

### Vraag 3: Is er een gratis proefversie beschikbaar?

A3: Ja, u kunt een gratis proefperiode krijgen van[deze link](https://releases.aspose.com/).

### Vraag 4: Hoe verkrijg ik een tijdelijke licentie?

 A4: Bezoek[hier](https://purchase.aspose.com/temporary-license/) voor tijdelijke licentiegegevens.

### Q5: Hulp nodig of vragen?

 A5: Ga naar de[Aspose.CAD-forum](https://forum.aspose.com/c/cad/19) voor gemeenschapssteun.