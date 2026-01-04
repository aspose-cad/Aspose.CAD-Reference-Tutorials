---
date: 2026-01-04
description: Scopri come **salvare CAD come PNG** ed esportare senza sforzo gli oggetti
  OLE dai file CAD usando Aspose.CAD per Java. Configurazione rapida, esempio di codice
  completo e consigli sulle migliori pratiche.
linktitle: Export OLE Objects from CAD
second_title: Aspose.CAD Java API
title: Salva CAD come PNG ed esporta oggetti OLE con Aspose.CAD per Java
url: /it/java/cad-to-pdf-and-svg-export-options/export-ole-objects-from-cad/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Salva CAD come PNG ed esporta oggetti OLE con Aspose.CAD per Java

## Introduzione

Nel mondo in rapida evoluzione del Computer‑Aided Design (CAD), la possibilità di **salvare CAD come PNG** estraendo al contempo gli oggetti OLE (Object Linking and Embedding) incorporati può semplificare notevolmente il tuo flusso di lavoro. Che tu stia costruendo uno strumento di conversione batch, generando miniature per un portale web o semplicemente abbia bisogno di archiviare contenuti OLE, Aspose.CAD per Java ti offre un modo pulito e programmatico per farlo. In questo tutorial percorreremo l’intero processo, dalla configurazione del progetto all’esportazione di ciascun oggetto OLE come immagine PNG.

## Risposte rapide
- **Posso esportare gli oggetti OLE direttamente in PNG?** Sì – Aspose.CAD carica il file CAD e consente di rasterizzare ogni layout in PNG.  
- **Quale versione di Java è richiesta?** Java 8 o successiva.  
- **È necessaria una licenza per questa funzionalità?** Una versione di prova gratuita è sufficiente per la valutazione; è necessaria una licenza per la produzione.  
- **I dati vettoriali saranno preservati?** La rasterizzazione PNG mantiene la fedeltà visiva, ma l'output è raster, non vettoriale.  
- **È supportata l'elaborazione batch?** Assolutamente – iterare su un array di file come mostrato nell'esempio di codice.

## Prerequisiti

Prima di iniziare, assicurati di avere quanto segue:

- **Java Development Kit (JDK)** – Java 8+ installato e configurato.  
- **Aspose.CAD for Java** – Scarica la libreria più recente dal [download link](https://releases.aspose.com/cad/java/).  
- **File sorgente CAD** – Qualsiasi file DWG/DXF/DGN che contenga oggetti OLE da esportare.

## Importazione dei namespace

Per lavorare con i file CAD è necessario importare le classi core di Aspose.CAD. Mantieni il blocco di import esattamente come mostrato – fornisce le classi utilizzate più avanti nel tutorial.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## Come salvare CAD come PNG

Di seguito trovi una guida concisa, passo‑passo, che mostra **come esportare gli oggetti OLE e salvare CAD come PNG**. Ogni passaggio include una breve spiegazione seguita dal codice esatto da copiare nel tuo progetto.

### Passo 1: Imposta la directory dei documenti

Definisci la cartella che contiene i tuoi disegni CAD. Sostituisci il segnaposto con il percorso reale sul tuo computer.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

### Passo 2: Definisci i nomi dei file CAD

Elenca tutti i file CAD che desideri elaborare. Puoi aggiungere quante voci vuoi.

```java
String[] files = new String[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

### Passo 3: Imposta le opzioni di esportazione PNG

Configura le impostazioni di rasterizzazione. Qui puntiamo a un layout specifico (`Layout1`) e utilizziamo le opzioni PNG predefinite.

```java
PngOptions pngOptions = new PngOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.setLayouts(new String[] { "Layout1" });
```

### Passo 4: Itera sui file CAD e salva come PNG

Carica ogni file CAD, rasterizza gli oggetti OLE e scrivi il file PNG di output. Il suffisso `_out.png` ti aiuta a identificare le immagini generate.

```java
for(String file : files)
{
    CadImage cadImage = (CadImage)Image.load(dataDir + file);
    cadImage.save(dataDir + file + "_out.png", pngOptions);
}
```

## Problemi comuni e soluzioni

| Problema | Perché accade | Soluzione |
|----------|----------------|----------|
| **`Image.load` throws `FileNotFoundException`** | Il percorso `dataDir` è errato o il nome del file contiene un errore di battitura. | Verifica la stringa della directory e assicurati che i nomi dei file corrispondano esattamente, spazi inclusi. |
| **Output PNG is blank** | Il nome del layout non esiste nel file CAD di origine. | Usa `cadImage.getLayouts()` per elencare i layout disponibili, quindi aggiorna `rasterizationOptions.setLayouts(...)`. |
| **Large CAD files cause OutOfMemoryError** | Rasterizzare immagini ad alta risoluzione consuma molta memoria heap. | Aumenta l'heap JVM (`-Xmx2g`) o riduci la risoluzione di rasterizzazione tramite `rasterizationOptions.setResolution(...)`. |

## FAQ

### Q1: Aspose.CAD è compatibile con tutti i formati di file CAD?

A1: Aspose.CAD supporta vari formati CAD, inclusi DWG, DXF e DGN. Consulta la [documentazione](https://reference.aspose.com/cad/java/) per l'elenco completo.

### Q2: Posso personalizzare le impostazioni di esportazione per gli oggetti OLE?

A2: Sì, Aspose.CAD fornisce ampie opzioni per personalizzare le impostazioni di esportazione, consentendoti di adattare l'output alle tue esigenze specifiche.

### Q3: È disponibile una versione di prova gratuita per Aspose.CAD?

A3: Sì, puoi esplorare le funzionalità di Aspose.CAD ottenendo una prova gratuita da [qui](https://releases.aspose.com/).

### Q4: Dove posso ottenere supporto dalla community per Aspose.CAD?

A4: Unisciti alla community di Aspose.CAD sul [forum](https://forum.aspose.com/c/cad/19) per chiedere assistenza e condividere le tue esperienze.

### Q5: Come posso acquistare una licenza per Aspose.CAD?

A5: Visita la [pagina di acquisto](https://purchase.aspose.com/buy) per ottenere una licenza adatta alle tue esigenze di sviluppo.

## Conclusione

Seguendo questi cinque semplici passaggi puoi **salvare CAD come PNG** ed estrarre ogni oggetto OLE incorporato con poche righe di codice Java. Questo approccio è ideale per conversioni batch, report automatizzati o qualsiasi scenario in cui siano necessarie immagini raster del contenuto CAD senza esportazioni manuali. Sentiti libero di sperimentare diverse opzioni di rasterizzazione per adattarle ai requisiti di qualità e prestazioni.

---

**Ultimo aggiornamento:** 2026-01-04  
**Testato con:** Aspose.CAD for Java 24.12 (latest at time of writing)  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}