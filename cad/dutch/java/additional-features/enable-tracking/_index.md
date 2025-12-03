---
date: 2025-12-03
description: Leer hoe u de PDF-paginaformaat instelt bij het converteren van DWG naar
  PDF en tracking in DWG‑bestanden inschakelt met Aspose.CAD voor Java – een complete
  gids voor het nauwkeurig exporteren van CAD‑tekeningen naar PDF.
language: nl
linktitle: Set PDF Page Size and Enable Tracking in DWG Files Using Java
second_title: Aspose.CAD Java API
title: PDF-paginagrootte instellen en tracking inschakelen in DWG‑bestanden met Aspose.CAD
  in Java
url: /java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PDF-paginaformaat instellen en tracking inschakelen in DWG‑bestanden met Aspose.CAD in Java

## Inleiding

Als je **PDF-paginaformaat moet instellen** bij het *converteren van DWG naar PDF* en tegelijkertijd eventuele weergave‑problemen wilt bijhouden, biedt Aspose.CAD voor Java een nette, programmeerbare manier om beide taken uit te voeren. In deze tutorial lopen we stap voor stap door hoe je de paginadimensies configureert, tracking inschakelt en een CAD‑tekening exporteert naar PDF – alles vanuit Java. Aan het einde begrijp je waarom het juiste paginaformaat belangrijk is voor CAD‑tekeningen en hoe je gedetailleerde tracking‑informatie kunt vastleggen tijdens het exportproces.

## Snelle antwoorden
- **Wat beïnvloedt “PDF-paginaformaat instellen”?** Het bepaalt de breedte en hoogte van het resulterende PDF‑canvas, zodat je tekening perfect past.  
- **Heb ik een licentie nodig om deze functie te gebruiken?** Een proefversie werkt voor testen; een commerciële licentie is vereist voor productie.  
- **Welke Aspose.CAD‑versie is vereist?** Elke recente versie die `CadRasterizationOptions` ondersteunt.  
- **Kan ik dit gebruiken met andere CAD‑formaten?** Het voorbeeld toont DWG/DXF, maar dezelfde aanpak werkt voor de meeste ondersteunde formaten.  
- **Hoe lang duurt de conversie?** Meestal minder dan een seconde voor bescheiden bestanden; grotere tekeningen kunnen langer duren.

## Wat betekent “PDF-paginaformaat instellen” in de context van CAD‑export?
Het instellen van het PDF‑paginaformaat vertelt de renderer de exacte afmetingen (in pixels of points) van het uitvoercanvas. Dit is vooral belangrijk voor technische tekeningen waarbij schaal en lay‑out behouden moeten blijven. Zonder expliciete pagina‑formaatinstellingen kan de PDF standaard een formaat krijgen dat de tekening afsnijdt of vervormt.

## Waarom PDF-paginaformaat instellen bij het exporteren van CAD‑tekeningen?
- **Schaal behouden** – Ingenieurs vertrouwen op schaalgetrouwe afdrukken.  
- **Op papier passen** – Kies A4, Letter of een aangepast formaat dat overeenkomt met de projectspecificaties.  
- **Leesbaarheid verbeteren** – Grotere pagina’s kunnen fijne details tonen zonder in te zoomen.  
- **Consistente output** – Geautomatiseerde pipelines produceren elke keer PDFs met identieke afmetingen.

## Hoe PDF-paginaformaat instellen bij het converteren van DWG naar PDF?
Hieronder configureren we `CadRasterizationOptions` met aangepaste breedte‑ en hoogte‑waarden vóór het exporteren. Deze stap richt zich direct op het primaire trefwoord **PDF-paginaformaat instellen**.

## Voorvereisten

- **Java Development Kit (JDK)** – Java 8 of nieuwer geïnstalleerd op je machine.  
- **Aspose.CAD voor Java** – Download van de officiële [Aspose CAD downloadpagina](https://releases.aspose.com/cad/java/).  
- **Documentdirectory** – Een map die de DWG/DXF‑bestanden bevat die je wilt verwerken.

## Namespaces importeren

Importeer eerst de klassen die je nodig hebt. Het code‑blok blijft ongewijzigd ten opzichte van de originele tutorial.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.CadRenderResult;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.RenderResult;
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
```

## Stap 1: Het DWG/DXF‑bestand laden

Laad je bron‑tekening. Pas het pad aan zodat het naar jouw bestand wijst.

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## Stap 2: PDF‑exportopties configureren (inclusief paginaformaat)

Hier stellen we de paginabreedte en -hoogte in – dit is waar we **PDF-paginaformaat instellen**. De waarden zijn in pixels; je kunt ze naar behoefte omrekenen van inches of millimeters.

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);   // <-- custom width
cadRasterizationOptions.setPageHeight(600);  // <-- custom height
```

> **Tip:** Als je standaard papierformaten wilt gebruiken, hanteer dan de conversie `1 inch = 72 points`. Voor een A4‑pagina (8,27 × 11,69 in) stel je `pageWidth = 595` en `pageHeight = 842` in.

## Stap 3: Tracking implementeren

Tracking legt eventuele weergaveproblemen vast. We koppelen een aangepaste handler die wordt aangeroepen na de export.

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## Stap 4: Exporteren naar PDF

Voer nu de conversie uit. De PDF wordt aangemaakt met de door jou opgegeven afmetingen, en eventuele tracking‑informatie wordt naar de console geschreven.

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## Stap 5: CadRenderHandler‑klasse

De handler print alle fouten die tijdens het renderen zijn opgetreden. Dit helpt je bij het debuggen van problemen bij het **exporteren van CAD‑tekening PDF**.

```java
public static class ErrorHandler extends CadRasterizationOptions.CadRenderHandler {
    @Override
    public void invoke(CadRenderResult result) {
        System.out.println("Tracking results of exporting");

        if (result.isRenderComplete())
            return;

        System.out.println("Have some problems:");

        int idxError = 1;
        for (RenderResult rr : result.getFailures()) {
            System.out.printf("{0}. {1}, {2}", idxError, rr.getRenderCode(), rr.getMessage());
            idxError++;
        }
    }
}
```

## Veelvoorkomende problemen en oplossingen

| Probleem | Oorzaak | Oplossing |
|----------|---------|-----------|
| **Lege PDF** | Paginaformaat ingesteld op 0 of te klein | Controleer of `setPageWidth` en `setPageHeight` positieve waarden hebben. |
| **Ontbrekende geometrie** | Renderfouten vastgelegd door de handler | Bekijk de console‑output van `ErrorHandler` en los de specifieke `RenderCode` op. |
| **Bestand niet gevonden** | Onjuist `dataDir`‑pad | Gebruik een absoluut pad of zorg dat de map bestaat. |
| **Licentie‑exception** | De proefversie gebruiken zonder geldige licentie voor grote bestanden | Pas je Aspose.CAD‑licentie toe vóór het laden van de afbeelding. |

## Veelgestelde vragen

**V: Kan ik tracking inschakelen voor andere CAD‑bestandsformaten met Aspose.CAD voor Java?**  
A: Aspose.CAD ondersteunt voornamelijk DWG/DXF voor tracking. Voor andere formaten raadpleeg je de officiële documentatie.

**V: Hoe kan ik extra exportopties beheren in Aspose.CAD voor Java?**  
A: De bibliotheek biedt vele opties zoals DPI, achtergrondkleur en vector‑rasterisatie. Zie de [Aspose.CAD Java‑documentatie](https://reference.aspose.com/cad/java/) voor details.

**V: Is er een proefversie beschikbaar voor Aspose.CAD voor Java?**  
A: Ja, je kunt een gratis proefversie downloaden via de [Aspose.CAD Free Trial](https://releases.aspose.com/).

**V: Waar kan ik hulp zoeken of discussiëren over problemen met Aspose.CAD voor Java?**  
A: Bezoek het [Aspose.CAD‑forum](https://forum.aspose.com/c/cad/19) voor community‑ondersteuning en officiële antwoorden.

**V: Hoe verkrijg ik een tijdelijke licentie voor Aspose.CAD voor Java?**  
A: Volg de stappen op de pagina [Temporary License](https://purchase.aspose.com/temporary-license/).

---

**Laatst bijgewerkt:** 2025-12-03  
**Getest met:** Aspose.CAD voor Java 24.11 (latest at time of writing)  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}