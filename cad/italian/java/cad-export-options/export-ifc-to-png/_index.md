---
date: 2025-12-21
description: Converti IFC in PNG senza sforzo con Aspose.CAD per Java. Segui il nostro
  tutorial passo passo.
linktitle: Export IFC to PNG
second_title: Aspose.CAD Java API
title: Converti IFC in PNG con Aspose.CAD per Java
url: /it/java/cad-export-options/export-ifc-to-png/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Converti IFC in PNG con Aspose.CAD per Java

## Introduzione

In questo tutorial imparerai **come convertire IFC in PNG** usando la potente libreria Aspose.CAD per Java. Che tu stia costruendo un visualizzatore BIM, generando miniature per un portale di costruzione, o automatizzando pipeline di documentazione, convertire file IFC (Industry Foundation Classes) in immagini raster è una necessità comune. Ti guideremo passo passo, spiegheremo le ragioni delle impostazioni e ti daremo consigli per ottenere i migliori risultati visivi.

## Risposte rapide
- **Quale libreria è necessaria?** Aspose.CAD per Java (disponibile versione di prova gratuita).  
- **Versioni IFC supportate?** La maggior parte dei file IFC 2x3 e IFC4 sono gestiti.  
- **Tempo tipico di conversione?** Pochi secondi per modelli standard; dipende dalle dimensioni del file.  
- **È necessaria una licenza?** È necessaria una licenza temporanea per l'uso in produzione.  
- **Posso personalizzare le dimensioni dell'immagine?** Sì – usa `CadRasterizationOptions` per impostare larghezza e altezza.

## Che cosa significa “convertire IFC in PNG”?
Convertire IFC in PNG significa rasterizzare un modello edilizio 3‑D (IFC) in un'immagine bitmap 2‑D (PNG). Questo processo appiattisce la geometria, applica stili visivi predefiniti e produce un'immagine portabile che può essere visualizzata in browser, report o app mobile senza necessità di un visualizzatore CAD.

## Perché usare Aspose.CAD per Java?
- **Nessun software CAD esterno** – API Java pura, funziona su qualsiasi piattaforma.  
- **Rendering ad alta fedeltà** – preserva spessori delle linee, colori e livelli.  
- **Controllo totale** – le opzioni di rasterizzazione consentono di definire risoluzione, sfondo e altro.  
- **Licenze facili** – versioni di prova e licenze temporanee semplificano la valutazione.

## Prerequisiti

Prima di iniziare, assicurati di avere:

- **Libreria Aspose.CAD** – scaricala e installala dal [download link](https://releases.aspose.com/cad/java/).  
- **Java Development Kit (JDK)** – versione 8 o successiva.  
- **Una cartella** che contiene il file IFC da convertire.

## Importa spazi dei nomi

Nel tuo progetto Java, importa le classi necessarie:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## Guida passo‑passo

### Passo 1: Carica il file IFC

```java
String dataDir = "Your Document Directory" + "ExportingIFC/";
String fileName = dataDir + "example.ifc";
IfcImage cadImage = (IfcImage)Image.load(fileName);
```

Qui carichiamo il file IFC sorgente in un oggetto `IfcImage`. Aspose.CAD analizza automaticamente la struttura IFC e la prepara per la rasterizzazione.

### Passo 2: Imposta le opzioni vettoriali (di rasterizzazione)

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

`CadRasterizationOptions` controlla come la geometria 3‑D viene appiattita. Regola `PageWidth` e `PageHeight` per corrispondere alla risoluzione PNG desiderata. Valori più alti producono immagini più dettagliate ma aumentano l'uso di memoria.

### Passo 3: Configura le impostazioni di esportazione PNG

```java
PngOptions pngOptions = new PngOptions();
pngOptions.setVectorRasterizationOptions(vectorOptions);
```

`PngOptions` indica ad Aspose.CAD di generare un file PNG e collega le impostazioni di rasterizzazione definite nel passo precedente.

### Passo 4: Salva l'immagine come PNG

```java
String outPath = dataDir + "example.png";
cadImage.save(outPath, pngOptions);
```

Il metodo `save` scrive l'immagine rasterizzata su disco. Dopo l'esecuzione di questa riga, troverai `example.png` nella stessa directory del tuo file IFC sorgente.

## Problemi comuni e soluzioni

| Problema | Perché accade | Soluzione |
|----------|----------------|-----------|
| **Output PNG vuoto** | Le opzioni di rasterizzazione larghezza/altezza sono impostate a 0 o molto piccole. | Assicurati che `PageWidth` e `PageHeight` siano interi positivi (es., 1500). |
| **Layer o colori mancanti** | La vista predefinita può nascondere alcuni layer. | Usa `vectorOptions.setRenderMode(CadRenderMode.Wireframe)` o regola la visibilità dei layer tramite API (se necessario). |
| **Errori di out‑of‑memory** per file IFC molto grandi | Una risoluzione molto alta consuma molta RAM. | Riduci la risoluzione o elabora il modello a sezioni. |

## FAQ

### D1: Aspose.CAD è compatibile con tutte le versioni dei file IFC?

A1: Aspose.CAD supporta varie versioni di file IFC. Consulta la [documentazione](https://reference.aspose.com/cad/java/) per i dettagli di compatibilità.

### D2: Posso personalizzare ulteriormente le opzioni di rasterizzazione?

A2: Assolutamente! Esplora la [documentazione](https://reference.aspose.com/cad/java/) per opzioni di personalizzazione avanzate.

### D3: È disponibile una versione di prova?

A3: Sì, puoi accedere alla versione di prova gratuita [qui](https://releases.aspose.com/).

### D4: Come posso ottenere una licenza temporanea per Aspose.CAD?

A4: Ottieni una licenza temporanea da [questo link](https://purchase.aspose.com/temporary-license/).

### D5: Dove posso cercare aiuto o discutere problemi?

A5: Visita il [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) per supporto della community## Domande frequenti (Aggiuntive)

**D: Posso convertire più file IFC in batch?**  
**R:** Sì. Avvolgi la logica di caricamento e salvataggio all'interno di un ciclo che itera su un elenco di percorsi file.

**D: Come posso cambiare il colore di sfondo del PNG?**  
**R:** ImpostavectorOptions.setBackgroundColor(Color.getWhite())` (o qualsiasi `java.awt.Color`) prima di creare `PngOptions`.

**D: È possibile esportare in altri formati raster come JPEG o BMP?**  
**R:** Assolutamente. Sostituisci `PngOptions` con `JpegOptions` o `BmpOptions` e regola le impostazioni specifiche del formato.

**D: Devo rilasciare le risorse dopo la conversione?**  
**R:** Chiama `cadImage.dispose()` quando hai finito per liberare la memoria nativa.

---

**Ultimo aggiornamento:** 2025-12-21  
**Testato con:** Aspose.CAD per Java 24.12 (ultima versione al momento della scrittura)  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}