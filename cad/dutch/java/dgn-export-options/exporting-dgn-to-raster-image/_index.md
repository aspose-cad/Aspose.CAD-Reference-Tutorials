---
date: 2026-01-10
description: Leer hoe u JPEG-bestanden kunt maken van DGN-bestanden met Aspose.CAD
  voor Java. Deze stapsgewijze tutorial laat u zien hoe u DGN efficiënt naar JPEG
  kunt converteren.
linktitle: Exporting DGN in AutoCAD Format to Raster Image Format
second_title: Aspose.CAD Java API
title: Hoe JPEG maken van DGN met Aspose.CAD voor Java
url: /nl/java/dgn-export-options/exporting-dgn-to-raster-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Maak JPEG van DGN met Aspose.CAD voor Java

## Introduction

In deze uitgebreide gids maak je **JPEG van DGN** bestanden met slechts een paar regels Java-code. Of je nu een batchconversietool bouwt of CAD-tekeningen als web‑vriendelijke afbeeldingen wilt weergeven, het converteren van DGN naar JPEG is een veelvoorkomende vereiste voor vele engineering‑ en ontwerp‑workflows. We lopen elke stap door—van het instellen van de Aspose.CAD‑bibliotheek tot het opslaan van de uiteindelijke rasterafbeelding—zodat je de oplossing direct in je eigen applicaties kunt integreren.

## Quick Answers
- **Welke bibliotheek is nodig?** Aspose.CAD for Java  
- **Kan ik andere CAD‑formaten naar JPEG converteren?** Ja, Aspose.CAD ondersteunt veel formaten (zie secundaire trefwoord *convert cad to jpeg*)  
- **Heb ik een licentie nodig voor productie?** Een commerciële licentie is vereist voor niet‑trial gebruik  
- **Welke Java‑versie wordt ondersteund?** Java 8 of hoger  
- **Hoe lang duurt een typische conversie?** Meestal minder dan een seconde voor tekeningen van standaardformaat  

## Wat betekent “create JPEG from DGN”?

Een JPEG maken van een DGN‑bestand betekent het rasteren van de vector‑gebaseerde DGN‑tekening naar een pixel‑gebaseerde afbeelding (JPEG). Dit proces behoudt de visuele getrouwheid terwijl het een lichtgewicht bestand oplevert dat in browsers, e‑mail of rapporten kan worden weergegeven zonder CAD‑software.

## Why convert DGN to JPEG?
- **Gemakkelijk delen:** JPEG's zijn universeel zichtbaar op elk apparaat.  
- **Prestaties:** Rasterafbeeldingen laden sneller in webpagina's dan vector‑CAD‑bestanden.  
- **Compatibiliteit:** Veel downstream‑tools (bijv. rapportage‑engines) accepteren alleen rasterformaten.  

## Prerequisites

Zorg er vóór je begint voor dat je het volgende hebt:

1. **Aspose.CAD Library** – Download deze van de officiële site **[here](https://releases.aspose.com/cad/java/)**.  
2. **Java Development Kit (JDK)** – Java 8 of nieuwer geïnstalleerd op je machine.  
3. **IDE** – Elke Java‑compatibele IDE zoals IntelliJ IDEA of Eclipse.

## Import Packages

Voeg de benodigde imports toe aan je Java‑klasse:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
```

## Step‑by‑Step Guide

### Stap 1: Laad het DGN‑bestand

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
DgnImage dgnImage = (DgnImage) Image.load(dataDir + "Nikon_D90_Camera.dgn");
```

*Uitleg:* De `Image.load`‑methode leest het bron‑DGN‑bestand en retourneert een `DgnImage`‑object dat we later kunnen rasteren.

### Stap 2: Maak een JpegOptions‑object

```java
ImageOptionsBase options = new JpegOptions();
```

*Uitleg:* `JpegOptions` geeft Aspose.CAD aan dat het uitvoerformaat JPEG moet zijn. Het stelt ons ook in staat rasterisatie‑instellingen toe te voegen.

### Stap 3: Configureer rasterisatie‑instellingen

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(600);
vectorOptions.setPageHeight(400);
vectorOptions.setNoScaling(true);
vectorOptions.setAutomaticLayoutsScaling(false);
options.setVectorRasterizationOptions(vectorOptions);
```

*Uitleg:* Deze opties bepalen de grootte van de resulterende afbeelding en regelen het schaalgedrag. Pas `PageWidth` en `PageHeight` aan op basis van je gewenste resolutie.

### Stap 4: Sla de geconverteerde afbeelding op

```java
OutputStream outStream = new FileOutputStream(dataDir + "ExportDGNToRasterImage_Out.jpg");
dgnImage.save(outStream, options);
```

*Uitleg:* De `save`‑methode schrijft de gerasterde JPEG naar de opgegeven output‑stream. Na deze stap heb je een kant‑klaar JPEG‑bestand.

> **Pro tip:** Plaats de conversiecode in een try‑with‑resources‑blok om ervoor te zorgen dat streams automatisch worden gesloten.

## Veelvoorkomende gebruikssituaties

- **Miniaturen genereren** voor CAD‑bestandbrowsers.  
- **Tekeningen insluiten** in PDF‑rapporten of HTML‑pagina's.  
- **Geautomatiseerde batchverwerking** van ontwerp‑archieven.

## Problemen oplossen & Veelvoorkomende valkuilen

| Probleem | Oorzaak | Oplossing |
|----------|---------|-----------|
| Lege of witte uitvoerafbeelding | Onjuiste rasterisatie‑opties (bijv. `NoScaling` ingesteld op true met een niet‑overeenkomende paginagrootte) | Pas `PageWidth`/`PageHeight` aan of stel `NoScaling` in op false |
| Out‑of‑memory‑fout voor grote DGN‑bestanden | Het laden van zeer grote bestanden zonder streaming | Verhoog de JVM‑heap (`-Xmx`) of verwerk bestanden in kleinere delen |
| JPEG‑kwaliteit onvoldoende | Standaard JPEG‑kwaliteit is laag | Gebruik `((JpegOptions)options).setQuality(100);` vóór het opslaan |

## Veelgestelde vragen

### V1: Kan ik Aspose.CAD voor Java gebruiken met andere CAD‑bestandformaten?

A1: Ja, Aspose.CAD ondersteunt een breed scala aan formaten, waardoor je **CAD naar JPEG** kunt **converteren** en vele andere raster‑ of vector‑uitvoer kunt genereren.

### V2: Is er een gratis proefversie beschikbaar voor Aspose.CAD voor Java?

A2: Ja, je kunt een gratis proefversie krijgen **[hier](https://releases.aspose.com/)**.

### V3: Waar kan ik documentatie vinden voor Aspose.CAD voor Java?

A3: Raadpleeg de documentatie **[hier](https://reference.aspose.com/cad/java/)**.

### V4: Hoe kan ik ondersteuning krijgen voor Aspose.CAD voor Java?

A4: Bezoek het ondersteuningsforum **[hier](https://forum.aspose.com/c/cad/19)**.

### V5: Waar kan ik een licentie kopen voor Aspose.CAD voor Java?

A5: Je kunt een licentie kopen **[hier](https://purchase.aspose.com/buy)**.

## Conclusie

Je hebt nu geleerd hoe je **JPEG van DGN** bestanden maakt met Aspose.CAD voor Java. Door de bovenstaande stappen te volgen, kun je DGN‑naar‑JPEG‑conversie naadloos integreren in elke Java‑applicatie, of het nu gaat om desktop‑tools, webservices of geautomatiseerde pipelines.

---

**Laatst bijgewerkt:** 2026-01-10  
**Getest met:** Aspose.CAD for Java 24.11 (latest at time of writing)  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}