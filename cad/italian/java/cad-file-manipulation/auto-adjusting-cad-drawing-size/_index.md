---
date: 2025-12-22
description: Scopri come esportare disegni CAD e convertire DWG in BMP in Java con
  Aspose.CAD. Segui questa guida passo passo per una manipolazione efficiente dei
  file CAD.
linktitle: Auto Adjusting CAD Drawing Size
second_title: Aspose.CAD Java API
title: Come esportare un disegno CAD in BMP usando Aspose.CAD per Java
url: /it/java/cad-file-manipulation/auto-adjusting-cad-drawing-size/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come esportare un disegno CAD in BMP usando Aspose.CAD per Java

## Introduzione

Se stai cercando un modo chiaro e affidabile per **esportare CAD** da Java, sei nel posto giusto. Con Aspose.CAD per Java puoi non solo regolare automaticamente le dimensioni del disegno, ma anche **convertire DWG in BMP** in poche righe di codice. Questo tutorial ti guida attraverso l’intero processo, dalla configurazione dell’ambiente alla generazione di un’immagine BMP che preserva il layout CAD originale.

## Risposte rapide
- **Cosa significa “how to export cad”?** Si riferisce alla conversione di file CAD (DWG, DXF, ecc.) in un altro formato come BMP, PNG o PDF.  
- **Quale libreria gestisce la conversione?** Aspose.CAD per Java fornisce un’API semplice per questo compito.  
- **È necessaria una licenza?** Una licenza temporanea è sufficiente per i test; una licenza completa è richiesta per la produzione.  
- **Posso esportare più layout contemporaneamente?** Sì – impostando la proprietà `Layouts` è possibile specificare quali layout renderizzare.  
- **Il BMP è l’unico formato di output?** No – è possibile esportare anche in PNG, JPEG, TIFF e altri.

## Cos’è “how to export cad” con Aspose.CAD?
Esportare CAD significa prendere un disegno CAD nativo (ad esempio un file DWG) e renderizzarlo in un’immagine raster o in un altro formato vettoriale. Aspose.CAD si occupa di tutto il lavoro pesante: analizza la struttura CAD, rasterizza le entità vettoriali e scrive il risultato nel formato immagine scelto.

## Perché usare Aspose.CAD per Java per **convertire DWG in BMP**?
- **Nessuna dipendenza esterna** – puro Java, senza DLL native.  
- **Supporto completo per DWG, DXF, DGN e altri formati**.  
- **Controllo fine** sulle opzioni di rasterizzazione come selezione del layout, scala e colore di sfondo.  
- **Alte prestazioni** adatte al batch processing su server.

## Prerequisiti

Prima di iniziare, assicurati di avere quanto segue:

1. **Java Development Kit** – scaricalo [qui](https://www.java.com/en/download/).  
2. **Libreria Aspose.CAD per Java** – ottieni l’ultimo JAR da [qui](https://releases.aspose.com/cad/java/).  
3. **File CAD di esempio** – un file DWG (ad esempio `sample.dwg`) posizionato nella cartella `document` del tuo progetto.

## Importare i namespace

Nella tua applicazione Java, includi i namespace necessari per utilizzare le funzionalità di Aspose.CAD. Ecco un esempio:

```java

import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Ora, analizziamo il processo di **esportare CAD** in passaggi gestibili.

## Guida passo‑passo

### Passo 1: Caricare il disegno CAD

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String sourceFilePath = dataDir + "sample.dwg";
Image objImage = Image.load(sourceFilePath);
```

Carichiamo il file DWG sorgente in un oggetto `Image`, che funge da punto di ingresso per tutte le operazioni successive.

### Passo 2: Creare `BmpOptions`

```java
BmpOptions bmpOptions = new BmpOptions();
```

`BmpOptions` conterrà le impostazioni di rasterizzazione specifiche per l’output BMP.

### Passo 3: Configurare le impostazioni di rasterizzazione

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

Qui colleghiamo le opzioni di rasterizzazione alle opzioni BMP, consentendoci di controllare come le entità CAD vengono renderizzate.

### Passo 4: Impostare il/i layout da esportare

```java
cadRasterizationOptions.setLayouts(new String[]{"Model"});
```

La proprietà `Layouts` indica ad Aspose.CAD quali layout di disegno includere. Nella maggior parte dei casi, `"Model"` è il layout principale da convertire.

### Passo 5: Esportare in formato BMP

```java
String outPath = sourceFilePath + ".bmp";
objImage.save(outPath, bmpOptions);
```

Chiamando `save` con le `BmpOptions` configurate, il file BMP viene scritto su disco. Questo completa il flusso di lavoro **convertire DWG in BMP**.

## Problemi comuni e soluzioni

| Problema | Motivo | Soluzione |
|----------|--------|-----------|
| L’immagine di output è vuota | Nome del layout errato o layout mancante | Verifica che il nome del layout corrisponda al file CAD (ad es., `"Model"`). |
| Bassa risoluzione | DPI predefinito troppo basso | Imposta `cadRasterizationOptions.setResolution(300);` prima del salvataggio. |
| Errore di out‑of‑memory per file di grandi dimensioni | I disegni grandi richiedono più heap | Aumenta la dimensione dell’heap JVM (`-Xmx2g`) o elabora le pagine singolarmente. |

## Domande frequenti

**D: Aspose.CAD è compatibile con diversi formati di file CAD?**  
R: Sì, Aspose.CAD supporta DWG, DXF, DGN e molti altri formati.

**D: Posso usare Aspose.CAD per progetti commerciali?**  
R: Assolutamente. Acquista una licenza [qui](https://purchase.aspose.com/buy) per l’uso in produzione.

**D: Come ottengo una licenza temporanea per i test?**  
R: Puoi ottenere una licenza temporanea [qui](https://purchase.aspose.com/temporary-license/).

**D: Dove posso trovare supporto dalla community?**  
R: Unisciti al forum della community Aspose.CAD su [forum](https://forum.aspose.com/c/cad/19).

**D: È disponibile una versione di prova gratuita per Aspose.CAD per Java?**  
R: Sì, scarica la prova gratuita [qui](https://releases.aspose.com/).

## Conclusione

In questa guida abbiamo dimostrato **come esportare CAD** da Java e **convertire DWG in BMP** usando Aspose.CAD. Seguendo i cinque passaggi sopra, puoi integrare la conversione CAD‑immagine in qualsiasi applicazione Java, sia essa uno strumento desktop, un servizio web o una pipeline di elaborazione batch. Esplora altri formati di output (PNG, JPEG, PDF) cambiando la classe delle opzioni e sfrutta l’ampio set di funzionalità di Aspose.CAD per soddisfare tutte le tue esigenze di manipolazione CAD.

---

**Ultimo aggiornamento:** 2025-12-22  
**Testato con:** Aspose.CAD per Java 24.12  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}