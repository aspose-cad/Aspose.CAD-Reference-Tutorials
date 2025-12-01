---
date: 2025-12-01
description: Leer hoe u de PDF-pagina‑grootte instelt, DWG naar PDF converteert en
  het bijhouden van DWG‑wijzigingen inschakelt met Aspose.CAD voor Java.
language: nl
linktitle: Set PDF Page Size and Track DWG with Java
second_title: Aspose.CAD Java API
title: PDF-paginagrootte instellen en DWG volgen met Aspose.CAD Java
url: /java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Stel PDF-paginaformaat in en volg DWG met Aspose.CAD Java

## Introductie

Bij het samenwerken aan CAD-projecten moet je vaak **PDF-paginaformaat instellen** voor een consistente lay-out, **DWG naar PDF converteren** en elke wijziging in de tekening bijhouden. Aspose.CAD voor Java maakt dit allemaal mogelijk in één gestroomlijnde workflow. In deze tutorial lopen we de exacte stappen door om **PDF-paginaformaat in te stellen**, **DWG-wijzigingen bij te houden**, en de tekening als PDF te exporteren — allemaal met Java.

## Snelle antwoorden
- **Hoe stel ik het PDF-paginaformaat in?** Gebruik `CadRasterizationOptions.setPageWidth()` en `setPageHeight()` vóór het exporteren.  
- **Kan ik wijzigingen bijhouden tijdens het exporteren?** Ja – implementeer een aangepaste `CadRenderHandler` om de trackingresultaten vast te leggen.  
- **Welke methode converteert DWG naar PDF?** Roep `image.save(stream, pdfOptions)` aan na het configureren van de opties.  
- **Wat zijn de belangrijkste vereisten?** JDK, Aspose.CAD voor Java, en een map met DWG/DXF‑bestanden.  
- **Is een licentie vereist voor productie?** Ja, een geldige Aspose.CAD‑licentie is nodig voor niet‑trial‑implementaties.

## Wat betekent “PDF-paginaformaat instellen” in de context van DWG-export?

Het instellen van het PDF-paginaformaat bepaalt de afmetingen van het resulterende PDF‑canvas (breedte × hoogte in pixels). Dit is essentieel wanneer je wilt dat de geëxporteerde tekening past op een specifiek papierformaat of schermlay-out, zodat alle elementen precies verschijnen waar je ze verwacht.

## Waarom tracking inschakelen bij het exporteren van DWG‑bestanden?

Tracking (of wijzigingsbijhouden) registreert eventuele renderingsproblemen, ontbrekende lettertypen of niet‑ondersteunde entiteiten die zich voordoen tijdens de conversie. Door deze informatie vast te leggen kun je:

- Snel problemen identificeren die moeten worden opgelost vóór de uiteindelijke levering.  
- Duidelijke feedback geven aan teamleden over wat er is aangepast of weggelaten.  
- Een audit‑trail behouden voor sectoren met strenge compliance‑eisen.

## Vereisten

- **Java Development Kit (JDK)** – elke recente versie (8+).  
- **Aspose.CAD for Java** – download van de officiële [Aspose CAD downloadpagina](https://releases.aspose.com/cad/java/).  
- **Document Directory** – een map die de DWG/DXF‑bestanden bevat die je wilt verwerken.

## Namespaces importeren

Begin met het importeren van de benodigde Aspose.CAD‑klassen en standaard Java I/O‑klassen.

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

## Stap 1: Laad het DWG (of DXF) bestand

Laad je brontekening in een `Image`‑object. Pas het pad aan zodat het naar jouw eigen map wijst.

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## Stap 2: Configureer PDF‑exportopties (inclusief paginagrootte)

Hier stellen we de PDF‑opties in en **zetten we expliciet het PDF-paginaformaat** op 800 × 600 pixels. Dit is waar het primaire trefwoord wordt toegepast.

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);   // set PDF page width
cadRasterizationOptions.setPageHeight(600);  // set PDF page height
```

## Stap 3: Implementeer tracking

Maak een aangepaste fout‑handler die trackinginformatie ontvangt tijdens het conversieproces.

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## Stap 4: Exporteren naar PDF

Met de opties en tracking‑handler ingesteld, exporteer je de tekening. Deze stap **converteert DWG naar PDF** (of DXF naar PDF in ons voorbeeld).

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## Stap 5: CadRenderHandler‑klasse – Trackingresultaten vastleggen

De `ErrorHandler`‑klasse breidt `CadRenderHandler` uit en print eventuele renderingsproblemen die zich voordeden tijdens het **bijhouden van wijzigingen in DWG**‑bestanden.

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

## Veelvoorkomende problemen & hoe ze op te lossen

| Probleem | Waarom het gebeurt | Oplossing |
|----------|--------------------|-----------|
| **Ontbrekende lettertypen** | CAD‑bestand verwijst naar lettertypen die niet op de server zijn geïnstalleerd. | Installeer de benodigde lettertypen of embed ze in het brontekening. |
| **Niet‑ondersteunde entiteiten** | Bepaalde DWG‑entiteiten worden nog niet ondersteund door Aspose.CAD. | Gebruik de trackingoutput om ze te identificeren en vereenvoudig de tekening. |
| **Onjuiste paginagrootte** | `setPageWidth/Height` niet aangeroepen vóór export. | Zorg ervoor dat de paginagrootte is ingesteld in `CadRasterizationOptions` zoals hierboven getoond. |

## Veelgestelde vragen

### Q1: Kan ik tracking inschakelen voor andere CAD‑bestandsformaten met Aspose.CAD voor Java?

A1: Aspose.CAD ondersteunt tracking voornamelijk voor DWG/DXF‑bestanden. Voor andere formaten raadpleeg je de officiële documentatie om te zien welke functies beschikbaar zijn.

### Q2: Hoe kan ik extra exportopties verwerken in Aspose.CAD voor Java?

A2: De bibliotheek biedt veel opties zoals DPI, achtergrondkleur en vectorrasterisatie. Verken ze in de [Aspose.CAD Java-documentatie](https://reference.aspose.com/cad/java/).

### Q3: Is er een proefversie beschikbaar voor Aspose.CAD voor Java?

A3: Ja, je kunt een gratis proefversie downloaden via de [Aspose.CAD Free Trial](https://releases.aspose.com/).

### Q4: Waar kan ik hulp zoeken of discussiëren over problemen met Aspose.CAD voor Java?

A4: Het community‑forum op het [Aspose.CAD‑forum](https://forum.aspose.com/c/cad/19) is een uitstekende plek om vragen te stellen en ervaringen te delen.

### Q5: Hoe verkrijg ik een tijdelijke licentie voor Aspose.CAD voor Java?

A5: Volg de stappen op de pagina [Temporary License](https://purchase.aspose.com/temporary-license/) om een tijdelijk licentie‑verzoek voor evaluatie in te dienen.

### Q6: Kan ik **DWG naar PDF converteren** terwijl ik lagen behoud?

A6: Ja. Door `CadRasterizationOptions` te configureren kun je laag‑informatie behouden in de resulterende PDF.

### Q7: Wat is de beste manier om **DWG als PDF te exporteren** met aangepaste paginadimensies?

A7: Stel de gewenste breedte en hoogte in met `setPageWidth` en `setPageHeight` vóór het aanroepen van `image.save()` – precies zoals gedemonstreerd in Stap 2.

## Conclusie

Door de bovenstaande stappen te volgen kun je **PDF-paginaformaat instellen**, **DWG naar PDF converteren** en **wijzigingen in DWG‑bestanden bijhouden** met Aspose.CAD voor Java. Deze workflow geeft je volledige controle over de uitvoerlay-out en biedt waardevolle diagnostiek die je CAD‑samenwerking soepel en foutloos houdt. Voel je vrij om extra renderopties te verkennen en deze code te integreren in grotere automatiseringspijplijnen.

---

**Laatst bijgewerkt:** 2025-12-01  
**Getest met:** Aspose.CAD for Java 24.12 (latest at time of writing)  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}