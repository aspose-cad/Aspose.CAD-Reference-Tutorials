---
date: 2026-02-17
description: Scopri come convertire dwg in png ed esportare CAD in png o altri formati
  raster usando Aspose.CAD per Java. Ottieni risultati di alta qualità rapidamente.
linktitle: Convert CAD Layout to Raster Image Format
second_title: Aspose.CAD Java API
title: Converti DWG in PNG e altri formati raster usando Aspose.CAD per Java
url: /it/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Converti DWG in PNG e altri formati raster usando Aspose.CAD per Java

## Introduction

Convertire DWG in PNG (o altri formati di immagine raster) è una necessità comune quando devi condividere disegni CAD con colleghi che non hanno un visualizzatore CAD, incorporare i progetti nella documentazione o generare miniature per gallerie web. **In questa guida imparerai a convertire dwg in png rapidamente e in modo affidabile**, sia che tu stia lavorando con un file di disegno completo o solo con un layout specifico. Potresti anche dover **convertire CAD in raster** per anteprime web, strumenti di reporting o app mobili. Aspose.CAD per Java rende questa conversione semplice e ti offre il pieno controllo su risoluzione, selezione del layout e formato di output.

## Quick Answers
- **Quale libreria gestisce DWG to PNG?** Aspose.CAD for Java  
- **Quali formati possono essere esportati?** PNG, JPEG, TIFF, PDF, BMP e altri  
- **È necessaria una licenza per i test?** Una prova gratuita funziona per lo sviluppo; è richiesta una licenza per la produzione  
- **Posso scegliere un layout specifico?** Sì, usa `setLayouts` per puntare a “Model”, “Layout1”, ecc.  
- **È possibile ottenere un output ad alta risoluzione?** Assolutamente—regola `setPageWidth` e `setPageHeight` per controllare i DPI  

## What is “convert dwg to png”?

L'espressione “convert dwg to png” descrive il processo di prendere un file DWG basato su vettori (il formato nativo di molte applicazioni CAD) e rasterizzarlo in un'immagine PNG basata su pixel. Le immagini raster sono ideali per la visualizzazione web, la condivisione via email e l'integrazione in software non CAD.

## Why export CAD as PNG (or other raster formats)?

- **Compatibilità universale:** PNG e JPEG sono supportati praticamente da tutti i visualizzatori di immagini e browser.  
- **Caricamento rapido:** Le immagini raster si caricano istantaneamente rispetto all'apertura di un file DWG pesante.  
- **Facile incorporamento:** Inserisci PNG direttamente in Word, PowerPoint o HTML senza plugin aggiuntivi.  
- **Aspetto coerente:** Controlli risoluzione, sfondo e layout, garantendo che ogni stakeholder veda la stessa immagine.  

## Common Use Cases

| Scenario | Perché l'output raster è utile |
|----------|-------------------------------|
| **Documentazione di progetto** | Incorporare PNG in PDF o documenti Word evita di richiedere software CAD per i revisori. |
| **Portali web** | Le miniature generate da file DWG si caricano istantaneamente e migliorano l'esperienza utente. |
| **App mobili** | Le immagini raster vengono visualizzate correttamente su dispositivi che non hanno visualizzatori CAD. |
| **Reportistica automatizzata** | Converti in batch più layout in PNG/JPEG per l'inclusione in grafici o dashboard. |

## Prerequisites

Prima di iniziare, assicurati di avere:

1. **Ambiente di sviluppo Java** – JDK 8 o superiore installato e configurato.  
2. **Aspose.CAD for Java** – Scarica l'ultimo JAR dalla [documentazione di Aspose.CAD for Java](https://reference.aspose.com/cad/java/).  

## Import Namespaces

Per prima cosa, importa le classi di cui avrai bisogno. Queste importazioni ti danno accesso al caricamento delle immagini, alle opzioni di rasterizzazione e alle impostazioni di output TIFF/PNG.

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

> **Consiglio professionale:** se prevedi di **esportare CAD come PNG** invece di TIFF, sostituisci `TiffOptions` con `PngOptions` (situato in `com.aspose.cad.imageoptions.PngOptions`).  

## Step‑by‑Step Guide

### Step 1: Set up the Resource Directory

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";
```

Sostituisci `"Your Document Directory"` con il percorso assoluto in cui risiedono i tuoi file CAD.

### Step 2: Load the CAD File

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

Puoi caricare qualsiasi formato supportato (DWG, DXF, DGN, ecc.). Questa è la parte **come convertire cad**—basta puntare al file e lasciare che Aspose gestisca il parsing.

### Step 3: Configure Rasterization Options

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
rasterizationOptions.setLayouts(new String[] {"Model", "Layout1"});
```

- `setPageWidth` / `setPageHeight` controllano la risoluzione di output (valori più grandi = DPI più alti).  
- `setLayouts` ti permette di **convertire CAD in raster** per layout specifici; omettilo per rasterizzare l'intero disegno.

### Step 4: Set Image Options

```java
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.setVectorRasterizationOptions(rasterizationOptions);
```

Se preferisci PNG, istanzia `PngOptions` invece di `TiffOptions`. Qui è dove **esporti CAD come PNG**.

### Step 5: Save the Resultant Image

```java
image.save(dataDir + "conic_pyramid_layoutstorasterimage_out_.tiff", options);
```

Modifica l'estensione del file in `.png` (e l'oggetto delle opzioni in `PngOptions`) per **salvare CAD come JPEG/PNG**.

> **Errore comune:** dimenticare di far corrispondere l'estensione del file con la classe delle opzioni provocherà un `UnsupportedFormatException`. Mantienili sempre sincronizzati.

## Common Issues and Solutions

| Problema | Soluzione |
|----------|-----------|
| **Immagine di output vuota** | Verifica che i nomi dei layout in `setLayouts` corrispondano esattamente a quelli nel file CAD di origine. |
| **PNG a bassa risoluzione** | Aumenta `setPageWidth` / `setPageHeight` o imposta `setResolution` nelle opzioni di rasterizzazione. |
| **Versione DWG non supportata** | Assicurati di utilizzare l'ultima versione di Aspose.CAD; le versioni più vecchie potrebbero non supportare le versioni più recenti di DWG. |
| **Errori di memoria su file di grandi dimensioni** | Elabora le pagine una alla volta o aumenta l'heap JVM (`-Xmx2g`). |

## Frequently Asked Questions

**D: Aspose.CAD è compatibile con diversi formati di file CAD?**  
R: Sì, supporta DWG, DXF, DGN e molti altri.

**D: Posso personalizzare la risoluzione dell'immagine raster di output?**  
R: Assolutamente. Regola `setPageWidth`, `setPageHeight` o `setResolution` in `CadRasterizationOptions`.

**D: Come posso convertire più layout CAD in un'unica esecuzione?**  
R: Fornisci un array con tutti i nomi dei layout a `setLayouts`, ad esempio `new String[]{"Model","Layout1","Layout2"}`.

**D: Sono supportati formati di output oltre a TIFF?**  
R: Sì—PNG, JPEG, BMP, PDF e altri sono disponibili tramite le rispettive classi `*Options`.

**D: Dove posso ottenere aiuto o condividere la mia esperienza con Aspose.CAD?**  
R: Visita il [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) per supporto della community e assistenza ufficiale.

## Conclusion

Seguendo questi passaggi puoi **convertire DWG in PNG**, **esportare CAD come PNG**, **salvare CAD come JPEG**, o generare qualsiasi altro formato raster di cui hai bisogno. Aspose.CAD per Java si occupa del lavoro pesante, permettendoti di concentrarti sull'integrazione di immagini ad alta qualità nelle tue applicazioni, documentazione o portali web.

---

**Ultimo aggiornamento:** 2026-02-17  
**Testato con:** Aspose.CAD for Java 24.12  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}