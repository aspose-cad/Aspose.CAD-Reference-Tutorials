---
date: 2026-02-17
description: Scopri come la libreria CAD Java Aspose.CAD per Java può esportare i
  file DWG in PDF o immagini raster in modo rapido e preciso.
linktitle: Export DWG to PDF or Raster
second_title: Aspose.CAD Java API
title: Esporta DWG in PDF o raster usando la libreria CAD Java Aspose.CAD per Java
url: /it/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Esporta DWG in PDF o Raster utilizzando la java cad library Aspose.CAD per Java

## Introduzione

Nel mondo dinamico del computer‑aided design (CAD), una gestione efficiente dei disegni è fondamentale. Con la **java cad library** **Aspose.CAD per Java** puoi **export dwg to pdf** — o immagini raster — in poche righe di codice. Questo tutorial ti guida attraverso l’intero processo, dal caricamento di un file DWG alla generazione di un PDF ad alta qualità, evidenziando perché Aspose.CAD Java è la libreria di riferimento per le attività di conversione CAD.

## Risposte rapide
- **Di cosa tratta questo tutorial?** Esportare file DWG in PDF o immagini raster utilizzando Aspose.CAD per Java.  
- **Ho bisogno di una licenza?** È disponibile una licenza temporanea gratuita per la valutazione; è necessaria una licenza completa per la produzione.  
- **Quale versione di Java è supportata?** Qualsiasi runtime Java 8+ funziona con l'ultima API Aspose.CAD Java.  
- **Posso convertire DWG in altri formati immagine?** Sì – le stesse opzioni di rasterizzazione consentono di generare PNG, JPEG, BMP, ecc.  
- **Quanto tempo richiede la conversione?** Tipicamente meno di un secondo per disegni standard; file più grandi possono richiedere qualche secondo.

## Perché la java cad library è la scelta migliore per la conversione DWG?

- **Implementazione pure Java** – nessun DLL nativo o strumenti esterni.  
- **Gestione accurata delle unità** – le unità metriche e imperiali vengono rilevate automaticamente.  
- **Output raster di alta qualità** – DPI e controllo delle dimensioni della pagina ottimizzati.  
- **Supporto PDF completo** – generazione di PDF che preserva i vettori senza dipendenze aggiuntive.  
- **Licenza flessibile** – inizia con una **temporary license aspose** per i test, poi effettua l'upgrade quando vai in produzione.

## Che cosa è “export dwg to pdf”?

L’esportazione di DWG in PDF significa convertire un disegno AutoCAD nativo in un documento PDF portatile e indipendente dal dispositivo. Il PDF risultante preserva i dati vettoriali, i layer e la scala, rendendolo ideale per condivisione, stampa o archiviazione.

## Perché usare Aspose.CAD Java per questa conversione?

Perché la **java cad library** gestisce internamente tutto, dalla conversione delle unità alla rasterizzazione, evitando la complessità di strumenti di terze parti e garantendo risultati coerenti su tutte le piattaforme.

## Prerequisiti

Prima di immergerti nel codice, assicurati di avere:

- Conoscenza di base della programmazione Java.  
- Libreria Aspose.CAD per Java installata. Se non l'hai ancora scaricata, ottienila **[qui](https://releases.aspose.com/cad/java/)**.  
- Un file DWG per i test – il campione **Bottom_plate.dwg** è utilizzato in questa guida.

## Importa gli spazi dei nomi

Nel tuo progetto Java, importa le classi necessarie per avviare la conversione:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## Guida passo‑passo

### Passo 1: Carica il file DWG

Per prima cosa, carica il tuo disegno DWG usando la classe `Image`. Questo crea una rappresentazione in memoria con cui Aspose.CAD può lavorare.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

### Passo 2: Determina il tipo di unità

Comprendere se il disegno utilizza unità metriche o imperiali è essenziale per una corretta scalatura. Il metodo di supporto `IsMetric` (implementazione omessa per brevità) restituisce un valore booleano.

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

### Passo 4: Configura le opzioni PDF (pdf options cad)

Crea un’istanza `PdfOptions` e allega le impostazioni di rasterizzazione. Questo indica ad Aspose.CAD come incorporare il contenuto rasterizzato nel PDF finale.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

### Passo 5: Salva come PDF

Infine, esporta il disegno in un file PDF. Il metodo `save` accetta il percorso di output e le `PdfOptions` configurate.

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

Al termine dell’esecuzione, troverai **Saved.pdf** nella cartella `DWGDrawings`, pronto per la distribuzione o l’archiviazione.

## Come convertire immagini raster dwg con la java cad library

Se ti servono immagini raster invece di un PDF, sostituisci semplicemente `PdfOptions` con le opzioni immagine raster appropriate (ad es., `PngOptions`, `JpegOptions`). La stessa istanza `CadRasterizationOptions` può essere riutilizzata, permettendoti di **convert dwg raster** con minime modifiche al codice.

## Come generare pdf dwg usando pdf options cad

L’esempio sopra già **generates pdf dwg**. Modificando `pdfOptions`—ad esempio impostando `pdfOptions.setCompress(true)`—puoi controllare dimensione e qualità del PDF. Questo dimostra la flessibilità dell’API **pdf options cad**.

## Problemi comuni e suggerimenti

- **Dimensione pagina errata** – Ricontrolla la logica di conversione delle unità; coefficienti non corrispondenti possono produrre pagine troppo grandi.  
- **Font o spessori di linea mancanti** – Assicurati che il DWG faccia riferimento a tutte le risorse esterne prima della conversione.  
- **Prestazioni su disegni grandi** – Aumenta l’impostazione `DPI` in `CadRasterizationOptions` solo quando è necessaria una qualità superiore; DPI più basso velocizza l’elaborazione.  
- **Problemi di licenza** – Per la valutazione puoi usare una **temporary license aspose**; è necessaria una licenza completa per le distribuzioni in produzione.

## Domande frequenti

**D: Posso usare Aspose.CAD per Java con altri framework Java?**  
R: Sì, Aspose.CAD per Java si integra perfettamente con i framework Java più diffusi come Spring, Jakarta EE e Android.

**D: È disponibile una licenza temporanea per Aspose.CAD per Java?**  
R: Sì, puoi ottenere una licenza temporanea **[qui](https://purchase.aspose.com/temporary-license/)**.

**D: Dove posso trovare supporto per Aspose.CAD per Java?**  
R: Visita il **[forum Aspose.CAD](https://forum.aspose.com/c/cad/19)** per assistenza dalla community e dagli ingegneri Aspose.

**D: Come posso acquistare una licenza per Aspose.CAD per Java?**  
R: Puoi acquistare una licenza **[qui](https://purchase.aspose.com/buy)**.

**D: Quali unità supporta Aspose.CAD per Java?**  
R: Aspose.CAD per Java supporta sia unità metriche sia imperiali, rilevando automaticamente il sistema di unità del disegno.

**D: Posso convertire DWG in altri formati immagine (ad es., PNG, JPEG) usando la stessa API?**  
R: Assolutamente. Sostituisci `PdfOptions` con le opzioni immagine raster appropriate (ad es., `PngOptions`) e riutilizza la stessa `CadRasterizationOptions`.

## Conclusione

Questo tutorial ha dimostrato come **export dwg to pdf** e immagini raster utilizzando la **java cad library** Aspose.CAD per Java. Seguendo la guida passo‑passo, puoi integrare una conversione CAD affidabile in qualsiasi applicazione Java, sia che tu abbia bisogno di PDF per la documentazione sia di immagini raster per la visualizzazione web.

---

**Ultimo aggiornamento:** 2026-02-17  
**Testato con:** Aspose.CAD per Java 24.10  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}