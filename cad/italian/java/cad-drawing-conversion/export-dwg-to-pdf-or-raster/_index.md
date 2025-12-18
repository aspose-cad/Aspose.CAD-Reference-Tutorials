---
date: 2025-12-18
description: Scopri come esportare i file DWG in PDF o immagini raster in Java usando
  Aspose.CAD. Questa guida passo passo garantisce precisione, efficienza e una conversione
  facile dei file DWG.
linktitle: Export DWG to PDF or Raster
second_title: Aspose.CAD Java API
title: Esporta DWG in PDF o Raster utilizzando Aspose.CAD per Java
url: /it/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Esporta DWG in PDF o Raster utilizzando Aspose.CAD per Java

## Introduzione

Nel mondo dinamico del computer‑aided design (CAD), la gestione efficiente dei disegni è fondamentale. Con **Aspose.CAD for Java** puoi **export dwg to pdf** — o immagini raster — con poche righe di codice. Questo tutorial ti guida attraverso l’intero processo, dal caricamento di un file DWG alla generazione di un PDF di alta qualità, evidenziando perché Aspose.CAD Java è la libreria di riferimento per le attività di conversione CAD.

## Risposte Rapide
- **Di cosa tratta questo tutorial?** Esportazione di file DWG in PDF o immagini raster utilizzando Aspose.CAD per Java.  
- **È necessaria una licenza?** È disponibile una licenza temporanea gratuita per la valutazione; è necessaria una licenza completa per la produzione.  
- **Quale versione di Java è supportata?** Qualsiasi runtime Java 8+ funziona con l'ultima API di Aspose.CAD per Java.  
- **Posso convertire DWG in altri formati immagine?** Sì – le stesse opzioni di rasterizzazione consentono di generare PNG, JPEG, BMP, ecc.  
- **Quanto tempo richiede la conversione?** Tipicamente meno di un secondo per disegni standard; file più grandi possono richiedere qualche secondo.

## Cos'è “export dwg to pdf”?

Esportare DWG in PDF significa convertire un disegno AutoCAD nativo in un documento PDF portatile e indipendente dal dispositivo. Il PDF risultante conserva i dati vettoriali, i layer e la scala, rendendolo ideale per la condivisione, la stampa o l’archiviazione.

## Perché usare Aspose.CAD Java per questa conversione?
- **Nessuna dipendenza esterna** – Java puro, senza DLL native.  
- **Gestione accurata delle unità** – rispetta automaticamente le unità metriche o imperiali.  
- **Output raster di alta qualità** – DPI e controllo delle dimensioni della pagina ottimizzati.  
- **Supporto PDF completo** – generazione di PDF che preserva i vettori senza librerie aggiuntive.

## Prerequisiti

Prima di immergerti nel codice, assicurati di avere:

- Conoscenza di base della programmazione Java.  
- Libreria Aspose.CAD per Java installata. Se non l'hai ancora scaricata, ottienila **[qui](https://releases.aspose.com/cad/java/)**.  
- Un file DWG per i test – il campione **Bottom_plate.dwg** è usato in questa guida.

## Importa Namespace

Nel tuo progetto Java, importa le classi necessarie per avviare la conversione:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## Guida Passo‑Passo

### Passo 1: Carica il file DWG

Per prima cosa, carica il tuo disegno DWG usando la classe `Image`. Questo crea una rappresentazione in memoria con cui Aspose.CAD può lavorare.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

### Passo 2: Determina il tipo di unità

Comprendere se il disegno utilizza unità metriche o imperiali è essenziale per una corretta scalatura. Il metodo di supporto `IsMetric` (implementazione omessa per brevità) restituisce un flag booleano.

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

### Passo 3: Imposta le opzioni di rasterizzazione

In base al sistema di unità, configura la dimensione della pagina, la scalatura e il tipo di unità di destinazione. Queste opzioni determinano come il DWG viene rasterizzato prima di essere inserito in un PDF.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();

if (currentUnitIsMetric) {
    // Metric units
    double metersCoeff = 1 / 1000.0;
    double scaleFactor = metersCoeff / currentUnitCoefficient;
    rasterizationOptions.setPageWidth((float)(210 * scaleFactor));
    rasterizationOptions.setPageHeight((float)(297 * scaleFactor));
    rasterizationOptions.setUnitType(UnitType.Millimeter);
} else {
    // Imperial units
    rasterizationOptions.setPageWidth((float)(8.27f / currentUnitCoefficient));
    rasterizationOptions.setPageHeight((float)(11.69f / currentUnitCoefficient));
    rasterizationOptions.setUnitType(UnitType.Inch);
}
```

### Passo 4: Configura le opzioni PDF

Crea un'istanza di `PdfOptions` e allega le impostazioni di rasterizzazione. Questo indica ad Aspose.CAD come incorporare il contenuto rasterizzato nel PDF finale.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

### Passo 5: Salva come PDF

Infine, esporta il disegno in un file PDF. Il metodo `save` accetta il percorso di output e le `PdfOptions` configurate.

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

Al termine dell'esecuzione del codice, troverai **Saved.pdf** nella cartella `DWGDrawings`, pronto per la distribuzione o l'archiviazione.

## Problemi Comuni e Suggerimenti

- **Dimensione pagina errata** – Ricontrolla la logica di conversione delle unità; coefficienti non corrispondenti possono produrre pagine sovradimensionate.  
- **Caratteri o spessori di linea mancanti** – Assicurati che il DWG faccia riferimento a eventuali risorse esterne prima della conversione.  
- **Prestazioni su disegni grandi** – Aumenta l'impostazione `DPI` in `CadRasterizationOptions` solo quando è richiesta una qualità superiore; DPI più basso velocizza l'elaborazione.

## Domande Frequenti

**Q: Posso usare Aspose.CAD per Java con altri framework Java?**  
A: Sì, Aspose.CAD per Java si integra perfettamente con i framework Java più popolari come Spring, Jakarta EE e Android.

**Q: È disponibile una licenza temporanea per Aspose.CAD per Java?**  
A: Sì, puoi ottenere una licenza temporanea **[qui](https://purchase.aspose.com/temporary-license/)**.

**Q: Dove posso trovare supporto per Aspose.CAD per Java?**  
A: Visita il **[forum Aspose.CAD](https://forum.aspose.com/c/cad/19)** per assistenza dalla community e dagli ingegneri di Aspose.

**Q: Come posso acquistare una licenza per Aspose.CAD per Java?**  
A: Puoi acquistare una licenza **[qui](https://purchase.aspose.com/buy)**.

**Q: Quali unità supporta Aspose.CAD per Java?**  
A: Aspose.CAD per Java supporta sia unità metriche che imperiali, rilevando automaticamente il sistema di unità del disegno.

**Q: Posso convertire DWG in altri formati immagine (es. PNG, JPEG) usando la stessa API?**  
A: Assolutamente. Sostituisci `PdfOptions` con le opzioni di immagine raster appropriate (es. `PngOptions`) e riutilizza le stesse `CadRasterizationOptions`.

## Conclusione

Questo tutorial ha dimostrato come **export dwg to pdf** e immagini raster utilizzando Aspose.CAD per Java. Seguendo la guida passo‑passo, puoi integrare una conversione CAD affidabile in qualsiasi applicazione Java, sia che tu abbia bisogno di PDF per la documentazione o di immagini raster per la visualizzazione web.

---

**Last Updated:** 2025-12-18  
**Tested With:** Aspose.CAD for Java 24.10  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}