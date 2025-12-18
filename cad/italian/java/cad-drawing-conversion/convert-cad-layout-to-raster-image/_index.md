---
date: 2025-12-18
description: Scopri come convertire DWG in PNG e altri formati di immagine raster
  con Aspose.CAD per Java. Esporta CAD in PNG con risultati ad alta qualità.
linktitle: Convert CAD Layout to Raster Image Format
second_title: Aspose.CAD Java API
title: Converti DWG in PNG e altri formati raster usando Aspose.CAD per Java
url: /it/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convertire DWG in PNG e altri formati raster usando Aspose.CAD per Java

## Introduzione

Convertire DWG in PNG (o altri formati di immagine raster) è una necessità comune quando è necessario condividere disegni CAD con colleghi che non hanno un visualizzatore CAD, incorporare i progetti nella documentazione o generare miniature per gallerie web. Aspose.CAD per Java rende questa conversione semplice, sia che si lavori con un file di disegno completo sia con un layout specifico. In questo tutorial illustreremo i passaggi esatti per **convertire un layout CAD in un'immagine raster**—la stessa tecnica che potete applicare per produrre output PNG, JPEG, TIFF o PDF.

## Risposte rapide
- **Quale libreria gestisce DWG to PNG?** Aspose.CAD for Java  
- **Quali formati possono essere esportati?** PNG, JPEG, TIFF, PDF, BMP e altri  
- **È necessaria una licenza per i test?** Una prova gratuita funziona per lo sviluppo; è richiesta una licenza per la produzione  
- **Posso scegliere un layout specifico?** Sì, usate `setLayouts` per puntare a “Model”, “Layout1”, ecc.  
- **È possibile ottenere un output ad alta risoluzione?** Assolutamente—regolate `setPageWidth` e `setPageHeight` per controllare i DPI  

## Che cos'è “convert dwg to png”?

La frase “convert dwg to png” descrive il processo di prendere un file DWG basato su vettori (il formato nativo per molte applicazioni CAD) e rasterizzarlo in un'immagine PNG basata su pixel. Le immagini raster sono ideali per la visualizzazione web, la condivisione via email e l'integrazione in software non‑CAD.

## Perché esportare CAD come PNG (o altri formati raster)?

- **Compatibilità universale:** PNG e JPEG sono supportati praticamente da tutti i visualizzatori di immagini e browser.  
- **Caricamento rapido:** Le immagini raster si caricano istantaneamente rispetto all'apertura di un file DWG pesante.  
- **Facile incorporamento:** Inserite PNG direttamente in Word, PowerPoint o HTML senza plugin aggiuntivi.  
- **Aspetto coerente:** Controllate risoluzione, sfondo e layout, garantendo che ogni stakeholder veda la stessa immagine.  

## Prerequisiti

Prima di iniziare, assicuratevi di avere:

1. **Ambiente di sviluppo Java** – JDK 8 o successivo installato e configurato.  
2. **Aspose.CAD per Java** – Scaricate l'ultimo JAR dalla [documentazione di Aspose.CAD per Java](https://reference.aspose.com/cad/java/).  

## Importare i namespace

Prima, importate le classi necessarie. Queste importazioni vi danno accesso al caricamento delle immagini, alle opzioni di rasterizzazione e alle impostazioni di output TIFF/PNG.

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

> **Consiglio professionale:** Se prevedete di esportare in PNG invece di TIFF, sostituite `TiffOptions` con `PngOptions` (trovato in `com.aspose.cad.imageoptions.PngOptions`).  

## Guida passo‑passo

### Passo 1: Configurare la directory delle risorse

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";
```

Sostituite `"Your Document Directory"` con il percorso assoluto dove risiedono i vostri file CAD.

### Passo 2: Caricare il file CAD

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

Potete caricare qualsiasi formato supportato (DWG, DXF, DGN, ecc.). Questa è la parte **how to convert cad**—basta puntare al file e lasciare che Aspose gestisca il parsing.

### Passo 3: Configurare le opzioni di rasterizzazione

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
rasterizationOptions.setLayouts(new String[] {"Model", "Layout1"});
```

- `setPageWidth` / `setPageHeight` controllano la risoluzione di output (valori più alti = DPI più elevati).  
- `setLayouts` consente di **convert cad to raster** per layout specifici; omettetelo per rasterizzare l'intero disegno.  

### Passo 4: Impostare le opzioni immagine

```java
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.setVectorRasterizationOptions(rasterizationOptions);
```

Se preferite PNG, istanziate `PngOptions` invece di `TiffOptions`. Qui è dove **export cad as png**.

### Passo 5: Salvare l'immagine risultante

```java
image.save(dataDir + "conic_pyramid_layoutstorasterimage_out_.tiff", options);
```

Modificate l'estensione del file in `.png` (e l'oggetto delle opzioni in `PngOptions`) per **save CAD as JPEG/PNG**.

> **Problema comune:** Dimenticare di far corrispondere l'estensione del file con la classe delle opzioni causerà un `UnsupportedFormatException`. Teneteli sempre sincronizzati.

## Problemi comuni e soluzioni

| Problema | Soluzione |
|----------|-----------|
| **Immagine di output vuota** | Verificate che i nomi dei layout in `setLayouts` corrispondano esattamente a quelli nel file CAD di origine. |
| **PNG a bassa risoluzione** | Aumentate `setPageWidth` / `setPageHeight` o impostate `setResolution` nelle opzioni di rasterizzazione. |
| **Versione DWG non supportata** | Assicuratevi di utilizzare l'ultima versione di Aspose.CAD; le versioni più vecchie potrebbero non supportare le versioni più recenti di DWG. |
| **Errori di memoria su file grandi** | Processate le pagine una alla volta o aumentate l'heap JVM (`-Xmx2g`). |

## Domande frequenti

**D: Aspose.CAD è compatibile con diversi formati di file CAD?**  
R: Sì, supporta DWG, DXF, DGN e molti altri.

**D: Posso personalizzare la risoluzione dell'immagine raster di output?**  
R: Assolutamente. Regolate `setPageWidth`, `setPageHeight` o `setResolution` in `CadRasterizationOptions`.

**D: Come posso convertire più layout CAD in un'unica esecuzione?**  
R: Fornite un array con tutti i nomi dei layout a `setLayouts`, ad esempio `new String[]{"Model","Layout1","Layout2"}`.

**D: Sono supportati formati di output oltre a TIFF?**  
R: Sì—PNG, JPEG, BMP, PDF e altri sono disponibili tramite le rispettive classi `*Options`.

**D: Dove posso ottenere aiuto o condividere la mia esperienza con Aspose.CAD?**  
R: Visitate il [forum di Aspose.CAD](https://forum.aspose.com/c/cad/19) per supporto della community e assistenza ufficiale.

## Conclusione

Seguendo questi passaggi potete **convertire DWG in PNG**, **esportare CAD come PNG**, **salvare CAD come JPEG**, o generare qualsiasi altro formato raster di cui avete bisogno. Aspose.CAD per Java si occupa del lavoro pesante, permettendovi di concentrarvi sull'integrazione di immagini ad alta qualità nelle vostre applicazioni, documentazione o portali web.

---

**Ultimo aggiornamento:** 2025-12-18  
**Testato con:** Aspose.CAD for Java 24.12  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}