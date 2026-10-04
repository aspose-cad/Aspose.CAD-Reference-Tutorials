---
date: 2026-10-04
description: Scopri come convertire rapidamente DWG in PNG ed esportare CAD in PNG
  o altri formati raster utilizzando Aspose.CAD for Java. Ottieni risultati ad alta
  qualità in poco tempo.
keywords:
- convert dwg to png
- dwg to raster image
- convert cad to pdf
- export cad as png
- convert dwg to jpeg
lastmod: 2026-10-04
linktitle: Converti il layout CAD in formato immagine raster
og_description: Converti DWG in PNG rapidamente con Aspose.CAD for Java. Scopri passo
  passo come esportare CAD in PNG, JPEG, TIFF e altro.
og_image_alt: 'Developer guide: Convert DWG to PNG and other raster formats using
  Aspose.CAD for Java'
og_title: Converti DWG in PNG e altri formati raster utilizzando Aspose.CAD for Java
schemas:
- author: Aspose
  dateModified: '2026-10-04'
  description: Learn how to quickly convert dwg to png and export cad as png or other
    raster formats using Aspose.CAD for Java. Get high‑quality results fast.
  headline: Convert DWG to PNG and other raster formats using Aspose.CAD for Java
  type: TechArticle
- description: Learn how to quickly convert dwg to png and export cad as png or other
    raster formats using Aspose.CAD for Java. Get high‑quality results fast.
  name: Convert DWG to PNG and other raster formats using Aspose.CAD for Java
  steps:
  - name: set up the resource directory
    text: Replace `"Your Document Directory"` with the absolute path where your CAD
      files reside. This directory will be used for both input and output files.
  - name: load the CAD file
    text: '`Image.load` parses the source file and creates an in‑memory representation
      that you can rasterize. You can load any supported format (DWG, DXF, DGN, etc.)
      – this is the **how to convert cad** part.'
  - name: configure rasterization options
    text: '`CadRasterizationOptions` defines how the vector data is turned into pixels.
      `setPageWidth` and `setPageHeight` control output resolution (larger values
      = higher DPI). `setLayouts` lets you **convert CAD to raster** for specific
      layouts; omit it to rasterize the whole drawing.'
  - name: set image options
    text: '`TiffOptions` (or `PngOptions` for PNG) tells Aspose which raster format
      to generate and lets you fine‑tune compression, color depth, and other format‑specific
      settings. Choose the options class that matches your desired output.'
  - name: save the resultant image
    text: Call `save` on the `Image` instance, passing the output file name and the
      options object. Change the file extension to `.png` (and use `PngOptions`) to
      **save CAD as PNG**. The same pattern works for JPEG, BMP, or PDF. > **Common
      pitfall:** Forgetting to match the file extension with the options cla
  type: HowTo
- questions:
  - answer: Yes, it supports over 30 CAD and raster formats, including DWG, DXF, DGN,
      and SVG.
    question: Is Aspose.CAD compatible with different CAD file formats?
  - answer: Absolutely. Adjust `setPageWidth`, `setPageHeight`, or `setResolution`
      in `CadRasterizationOptions` to achieve the desired DPI.
    question: Can I customize the resolution of the output raster image?
  - answer: Provide an array with all layout names to `setLayouts`, e.g., `new String[]{"Model","Layout1","Layout2"}`.
    question: How can I convert multiple CAD layouts in a single run?
  - answer: Yes—PNG, JPEG, BMP, PDF, and more are available via their respective `*Options`
      classes.
    question: Are there output formats besides TIFF supported?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community
      support and official assistance.
    question: Where can I get help or share my experience with Aspose.CAD?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- convert dwg
- Aspose.CAD
- Java raster conversion
- CAD image processing
title: Converti DWG in PNG e altri formati raster utilizzando Aspose.CAD for Java
url: /it/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Converti DWG in PNG e altri formati raster utilizzando Aspose.CAD per Java

## Introduzione

`Aspose.CAD for Java` è una libreria che consente la conversione programmatica di file CAD in immagini raster come PNG, JPEG e TIFF. Convertire DWG in PNG (o altri formati di immagine raster) è una necessità comune quando devi condividere disegni CAD con colleghi che non hanno un visualizzatore CAD, incorporare i progetti nella documentazione o generare miniature per gallerie web. In questa guida imparerai a convertire dwg in png rapidamente e in modo affidabile, sia che tu stia lavorando con un file di disegno completo sia con un layout specifico. Potresti anche aver bisogno di **convertire CAD in raster** per anteprime web, strumenti di reporting o app mobili.

## Risposte rapide
- **Quale libreria gestisce DWG in PNG?** Aspose.CAD for Java fornisce il motore di conversione.  
- **Quali formati raster posso esportare?** PNG, JPEG, TIFF, PDF, BMP e oltre 30 formati aggiuntivi.  
- **Ho bisogno di una licenza per i test?** Una prova gratuita funziona per lo sviluppo; è necessaria una licenza commerciale per la produzione.  
- **Posso scegliere un layout specifico?** Sì – usa `setLayouts` per puntare a “Model”, “Layout1”, ecc.  
- **È possibile un output ad alta risoluzione?** Assolutamente – regola `setPageWidth` e `setPageHeight` (o `setResolution`) per controllare DPI.

## Cos'è “convert dwg to png”?

Convertire dwg in png significa trasformare un disegno vettoriale DWG in un'immagine PNG basata su pixel che può essere visualizzata da qualsiasi visualizzatore di immagini standard. Questo processo rasterizza le entità vettoriali, preservando spessore delle linee, colori e livelli, traducendole in una bitmap a risoluzione fissa. Il risultato è ideale per l'inserimento in PDF, documenti Word o pagine web dove il supporto vettoriale è limitato.

## Perché esportare CAD come PNG (o altri formati raster)?

Esportare CAD come PNG ti offre compatibilità universale, caricamento rapido e facile integrazione su tutte le principali piattaforme. Le immagini raster si caricano istantaneamente rispetto all'apertura di un pesante file DWG, e la compressione loss‑less di PNG garantisce fedeltà visiva. Controllando risoluzione, colore di sfondo e layout, assicuri che ogni stakeholder veda la stessa apparizione, sia che il file venga visualizzato su desktop, dispositivo mobile o all'interno di un browser.

## Casi d'uso comuni

| Scenario | Perché l'output raster è utile |
|----------|-------------------------------|
| **Documentazione di progetto** | Inserire PNG in PDF o documenti Word evita di richiedere software CAD ai revisori. |
| **Portali web** | Le miniature generate da file DWG si caricano istantaneamente e migliorano l'esperienza utente. |
| **App mobili** | Le immagini raster vengono visualizzate correttamente su dispositivi che non hanno visualizzatori CAD. |
| **Reporting automatizzato** | Converti in batch più layout in PNG/JPEG per includerli in grafici o dashboard. |

## Prerequisiti

Prima di iniziare, assicurati di avere:

1. **Ambiente di sviluppo Java** – JDK 8 o versioni successive installate e configurate.  
2. **Aspose.CAD for Java** – Scarica l'ultima JAR dalla [documentazione di Aspose.CAD per Java](https://reference.aspose.com/cad/java/).  

## Importa spazi dei nomi

`com.aspose.cad.Image` è la classe principale che rappresenta qualsiasi file CAD in memoria. `com.aspose.cad.imageoptions.*` fornisce oggetti di opzione per ciascun formato raster. Importa le classi necessarie per caricare un disegno, configurare la rasterizzazione e salvare l'output.

> **Suggerimento:** Se prevedi di **esportare CAD come PNG** invece di TIFF, sostituisci `TiffOptions` con `PngOptions` (trovato in `com.aspose.cad.imageoptions.PngOptions`).

## Guida passo‑passo

### Passo 1: configura la directory delle risorse

Sostituisci `"Your Document Directory"` con il percorso assoluto dove risiedono i tuoi file CAD. Questa directory sarà usata sia per i file di input che di output.

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

### Passo 2: carica il file CAD

`Image.load` analizza il file sorgente e crea una rappresentazione in memoria che puoi rasterizzare. Puoi caricare qualsiasi formato supportato (DWG, DXF, DGN, ecc.) – questa è la parte **come convertire cad**.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";
```

### Passo 3: configura le opzioni di rasterizzazione

`CadRasterizationOptions` definisce come i dati vettoriali vengono trasformati in pixel. `setPageWidth` e `setPageHeight` controllano la risoluzione di output (valori più alti = DPI più elevato). `setLayouts` ti consente di **convertire CAD in raster** per layout specifici; omettilo per rasterizzare l'intero disegno.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### Passo 4: imposta le opzioni immagine

`TiffOptions` (o `PngOptions` per PNG) indica ad Aspose quale formato raster generare e ti permette di affinare compressione, profondità di colore e altre impostazioni specifiche del formato. Scegli la classe di opzioni che corrisponde al tuo output desiderato.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
rasterizationOptions.setLayouts(new String[] {"Model", "Layout1"});
```

### Passo 5: salva l'immagine risultante

Chiama `save` sull'istanza `Image`, passando il nome del file di output e l'oggetto opzioni. Cambia l'estensione del file in `.png` (e usa `PngOptions`) per **salvare CAD come PNG**. Lo stesso schema funziona per JPEG, BMP o PDF.

```java
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.setVectorRasterizationOptions(rasterizationOptions);
```

> **Errore comune:** Dimenticare di far corrispondere l'estensione del file con la classe delle opzioni provocherà un `UnsupportedFormatException`. Mantienile sempre sincronizzate.

## Problemi comuni e soluzioni

| Problema | Soluzione |
|----------|-----------|
| **Immagine di output vuota** | Verifica che i nomi dei layout in `setLayouts` corrispondano esattamente a quelli nel file CAD sorgente. |
| **PNG a bassa risoluzione** | Aumenta `setPageWidth` / `setPageHeight` o imposta `setResolution` sulle opzioni di rasterizzazione. |
| **Versione DWG non supportata** | Assicurati di usare l'ultima versione di Aspose.CAD; le versioni più vecchie potrebbero non supportare le release DWG più recenti. |
| **Errori di memoria su file grandi** | Processa le pagine una alla volta o aumenta l'heap JVM (`-Xmx2g`). |

## Domande frequenti

**D: È Aspose.CAD compatibile con diversi formati di file CAD?**  
R: Sì, supporta oltre 30 formati CAD e raster, inclusi DWG, DXF, DGN e SVG.

**D: Posso personalizzare la risoluzione dell'immagine raster di output?**  
R: Assolutamente. Regola `setPageWidth`, `setPageHeight` o `setResolution` in `CadRasterizationOptions` per ottenere il DPI desiderato.

**D: Come posso convertire più layout CAD in un'unica esecuzione?**  
R: Fornisci un array con tutti i nomi dei layout a `setLayouts`, ad esempio `new String[]{"Model","Layout1","Layout2"}`.

**D: Ci sono formati di output oltre a TIFF supportati?**  
R: Sì—PNG, JPEG, BMP, PDF e molti altri sono disponibili tramite le rispettive classi `*Options`.

**D: Dove posso ottenere aiuto o condividere la mia esperienza con Aspose.CAD?**  
R: Visita il [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) per supporto della community e assistenza ufficiale.

## Conclusione

Seguendo questi passaggi puoi **convertire DWG in PNG**, **esportare CAD come PNG**, **salvare CAD come JPEG** o generare qualsiasi altro formato raster di cui hai bisogno. Aspose.CAD for Java gestisce il lavoro pesante, permettendoti di concentrarti sull'integrazione di immagini di alta qualità nelle tue applicazioni, documentazione o portali web. Il supporto della libreria per più di 30 formati e la capacità di renderizzare disegni con centinaia di pagine senza caricare l'intero file in memoria la rendono una scelta solida per la rasterizzazione CAD di livello enterprise.

---

**Last Updated:** 2026-10-04  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  







```java
image.save(dataDir + "conic_pyramid_layoutstorasterimage_out_.tiff", options);
```

```bash
java -jar aspose-cad.jar -i input.dwg -o output.png -w 1200 -h 1200
```

## Tutorial correlati

- [Esporta rapidamente DWG in PDF o raster usando la libreria Java CAD Aspose.CAD per Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Converti DWG in BMP con Aspose.CAD per Java](/cad/java/cad-export-options/export-to-bmp/)
- [Esporta DWG in PDF: layout specifico usando Aspose.CAD per Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}