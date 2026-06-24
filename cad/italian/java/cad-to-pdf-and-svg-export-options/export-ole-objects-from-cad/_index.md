---
date: 2026-03-02
description: Sblocca il potenziale di Aspose.CAD per Java. Esporta facilmente gli
  oggetti OLE e **salva CAD come PNG**. Scarica ora per una gestione fluida dei dati
  CAD.
linktitle: Export OLE Objects from CAD
second_title: Aspose.CAD Java API
title: Salva CAD come PNG – Esporta oggetti OLE usando Aspose.CAD per Java
url: /it/java/cad-to-pdf-and-svg-export-options/export-ole-objects-from-cad/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Salva CAD come PNG – Esporta oggetti OLE usando Aspose.CAD per Java

## Introduzione

Nel mondo dinamico della Computer‑Aided Design (CAD), gestire ed estrarre oggetti OLE (Object Linking and Embedding) in modo efficiente — e poter **salvare CAD come PNG** — è fondamentale per i flussi di lavoro successivi, come report, anteprime web o archiviazione. Aspose.CAD per Java fornisce una soluzione potente, code‑first, che consente sia di esportare oggetti OLE sia di convertire disegni CAD in immagini PNG ad alta qualità con poche righe di codice.

## Risposte rapide
- **Cosa fa Aspose.CAD?** Legge, manipola e converte file CAD (DWG, DXF, DGN, ecc.) senza la necessità di software CAD nativo.  
- **Posso salvare CAD come PNG?** Sì — utilizza `PngOptions` insieme a `CadRasterizationOptions` per rasterizzare qualsiasi layout.  
- **Come esportare oggetti OLE?** Carica il file CAD con `Image.load` e salva ogni layout contenente OLE come PNG.  
- **È necessaria una licenza?** È disponibile una versione di prova gratuita; una licenza commerciale rimuove le limitazioni di valutazione.  
- **Quale versione di Java è richiesta?** Java 8 o superiore è pienamente supportata.

## Che cosa è **salvare CAD come PNG**?
Salvare CAD come PNG significa rasterizzare i disegni CAD basati su vettori in un’immagine PNG basata su pixel. Questa conversione è utile quando è necessario un formato leggero, universalmente visualizzabile per pagine web, app mobili o documentazione.

## Perché usare Aspose.CAD per Java per **convertire CAD in PNG**?
- **Nessuna installazione CAD necessaria** – la libreria funziona interamente in Java.  
- **Preserva la fedeltà del layout** – è possibile scegliere layout specifici, controllare DPI e mantenere la qualità delle linee.  
- **Elaborazione batch** – itera su più file con un semplice ciclo.  
- **Esporta oggetti OLE** – il contenuto OLE incorporato nei file DWG/DXF viene renderizzato automaticamente nell’output PNG.

## Prerequisiti

Prima di immergerti nel tutorial, assicurati di avere i seguenti prerequisiti:

- **Ambiente Java** – Verifica di avere un ambiente di sviluppo Java configurato sulla tua macchina.  
- **Aspose.CAD per Java** – Scarica e installa la libreria Aspose.CAD per Java. Puoi trovare la libreria al [link di download](https://releases.aspose.com/cad/java/).  
- **File CAD** – Prepara i file CAD contenenti oggetti OLE che desideri esportare.

## Importare gli spazi dei nomi

Per iniziare, importa gli spazi dei nomi necessari nel tuo progetto Java. Questi spazi dei nomi forniscono le classi e le funzionalità essenziali per lavorare con i file CAD usando Aspose.CAD.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Ora, analizziamo il processo di esportazione degli oggetti OLE da CAD in più passaggi:

## Come **salvare CAD come PNG** ed esportare oggetti OLE

### Passo 1: Imposta la directory del documento

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

Assicurati di sostituire `"Your Document Directory"` con il percorso della directory contenente i tuoi file CAD.

### Passo 2: Definisci i nomi dei file CAD

```java
String[] files = new String[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

Specifica i nomi dei file CAD che vuoi elaborare nell’array `files`.

### Passo 3: Imposta le opzioni di esportazione PNG

```java
PngOptions pngOptions = new PngOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.setLayouts(new String[] { "Layout1" });
```

Configura le opzioni di esportazione PNG, inclusa la rasterizzazione vettoriale e le impostazioni del layout. Queste opzioni ti permettono di **convertire CAD in PNG** con la qualità desiderata.

### Passo 4: Itera sui file CAD

```java
for(String file : files)
{
    CadImage cadImage = (CadImage)Image.load(dataDir + file);
    cadImage.save(dataDir + file + "_out.png", pngOptions);
}
```

Itera su ciascun file CAD specificato, caricalo usando Aspose.CAD e salva gli oggetti OLE come immagini PNG. Questo ciclo dimostra un modo semplice per **convertire DWG in PNG** in blocco.

## Problemi comuni e soluzioni

| Problema | Causa | Soluzione |
|----------|-------|-----------|
| **Output PNG vuoto** | Nome del layout non corrispondente | Verifica che il nome del layout (`"Layout1"`) esista nel DWG di origine. |
| **Grafica OLE mancante** | Gli oggetti OLE sono memorizzati in un layout diverso | Includi tutti i layout pertinenti in `rasterizationOptions.setLayouts(...)`. |
| **Errore di out‑of‑memory su file grandi** | Impostazioni DPI elevate | Riduci DPI tramite `rasterizationOptions.setResolution(...)` o elabora i file uno alla volta. |

## Domande frequenti

**D: Aspose.CAD è compatibile con tutti i formati di file CAD?**  
R: Aspose.CAD supporta vari formati CAD, inclusi DWG, DXF e DGN. Consulta la [documentazione](https://reference.aspose.com/cad/java/) per l’elenco completo.

**D: Posso personalizzare le impostazioni di esportazione per gli oggetti OLE?**  
R: Sì, Aspose.CAD offre ampie opzioni per personalizzare le impostazioni di esportazione, consentendoti di adattare l’output alle tue esigenze specifiche.

**D: È disponibile una versione di prova gratuita per Aspose.CAD?**  
R: Sì, puoi esplorare le funzionalità di Aspose.CAD ottenendo una prova gratuita [qui](https://releases.aspose.com/).

**D: Dove posso trovare supporto della community per Aspose.CAD?**  
R: Unisciti alla community Aspose.CAD sul [forum](https://forum.aspose.com/c/cad/19) per chiedere assistenza e condividere le tue esperienze.

**D: Come posso acquistare una licenza per Aspose.CAD?**  
R: Visita la [pagina di acquisto](https://purchase.aspose.com/buy) per ottenere una licenza adatta alle tue esigenze di sviluppo.

## Conclusione

Con questi semplici ma potenti passaggi, puoi facilmente **salvare CAD come PNG** esportando al contempo oggetti OLE dai file CAD usando Aspose.CAD per Java. Questo strumento versatile consente agli sviluppatori di gestire i dati CAD in modo efficiente, aprendo nuove possibilità nello sviluppo di applicazioni CAD e nei flussi di lavoro basati su immagini.

---

**Ultimo aggiornamento:** 2026-03-02  
**Testato con:** Aspose.CAD per Java 24.12  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}