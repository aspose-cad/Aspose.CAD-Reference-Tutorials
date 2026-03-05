---
date: 2026-03-05
description: Scopri come esportare DWG in PDF, abilitare le linee nascoste e convertire
  DWG in PDF con Aspose.CAD per Java in questo tutorial passo‑passo.
linktitle: Export DWG as PDF Using Java
second_title: Aspose.CAD Java API
title: Esporta DWG in PDF con linee nascoste – Aspose.CAD per Java
url: /it/java/cad-text-and-formatting/support-hidden-lines-in-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Esporta DWG in PDF con linee nascoste – Aspose.CAD per Java

## Introduzione

In questo tutorial imparerai a **export dwg to pdf** preservando le linee nascoste usando Aspose.CAD per Java. Che tu abbia bisogno di **convert DWG to PDF**, generare una guida in stile **dwg to pdf tutorial**, o semplicemente **save DWG as PDF** con supporto per le linee nascoste, ti guideremo passo passo. Alla fine, avrai una soluzione pronta all'uso che potrai inserire in qualsiasi progetto Java.

## Risposte rapide
- **Di cosa tratta questo tutorial?** Abilitare il rendering delle linee nascoste durante l'esportazione di DWG in PDF con Aspose.CAD per Java.  
- **Quale operazione principale viene eseguita?** `export dwg to pdf`.  
- **Ho bisogno di una licenza?** Una versione di prova gratuita è sufficiente per i test; è necessaria una licenza commerciale per la produzione.  
- **Quali sono i prerequisiti?** Ambiente di sviluppo Java, libreria Aspose.CAD per Java e file DWG.  
- **Quanto tempo richiede l'implementazione?** Circa 10‑15 minuti per una configurazione di base.

## Cos'è “export dwg to pdf”?

Esportare un file DWG in PDF converte il disegno CAD basato su vettori in un formato di documento portatile, preservando i layer, i tipi di linea e il rendering opzionale delle linee nascoste. Questo rende più semplice condividere i progetti CAD con le parti interessate che potrebbero non avere un software CAD.

## Come abilitare le linee nascoste durante l'esportazione di DWG in PDF

Le linee nascoste sono controllate tramite l'impostazione del layout nelle opzioni di rasterizzazione. Selezionando il layout **Model**, Aspose.CAD indica al renderer di trattare i bordi nascosti come invisibili, fornendo una rappresentazione 2‑D pulita di un modello 3‑D.

## Perché abilitare le linee nascoste durante l'esportazione?

Le linee nascoste offrono una rappresentazione visiva più chiara di modelli 3‑D complessi su una pagina 2‑D, garantendo che vengano enfatizzati solo i bordi visibili. Questo migliora la leggibilità ed è spesso richiesto nella documentazione ingegneristica.

## Prerequisiti

1. **Aspose.CAD for Java** – scarica la libreria dal sito ufficiale [qui](https://releases.aspose.com/cad/java/).  
2. **DWG files** – assicurati che i disegni DWG sorgente siano memorizzati in una directory nota.  
3. **Java development environment** – JDK 8+ e il tuo IDE preferito (Eclipse, IntelliJ, ecc.).  

Ora che sei pronto, immergiamoci nel codice.

## Importa spazi dei nomi

Inizia importando le classi necessarie per poter lavorare con le immagini CAD e le opzioni PDF.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.Arrays;
import java.util.List;
```

## Passo 1: Configura il tuo progetto

Crea un progetto Java e aggiungi il JAR di Aspose.CAD al tuo percorso di compilazione. Quindi definisci la directory che contiene i tuoi file DWG.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

> **Consiglio:** Usa un percorso assoluto o configura un percorso relativo basato sulla cartella delle risorse del tuo progetto.

## Passo 2: Carica il file DWG

Carica il file DWG sorgente in un oggetto `CadImage` così da poterlo manipolare.

```java
String sourceFilePath = dataDir + "Bottom_plate.dwg";
String outPath = dataDir + "Bottom_plate.pdf";
CadImage cadImage = (CadImage)Image.load(sourceFilePath);
```

## Passo 3: Configura le opzioni di rasterizzazione

Seleziona i layer che desideri includere e imposta le dimensioni della pagina per corrispondere al disegno originale. Qui è dove abilitiamo il rendering delle linee nascoste specificando il layout.

```java
List<String> list = Arrays.asList("Print","L1_RegMark","L2_RegMark");
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageHeight(cadImage.getHeight());
rasterizationOptions.setPageWidth(cadImage.getWidth()) ;
rasterizationOptions.setLayers(list);
```

## Passo 4: Imposta le opzioni PDF

Indica ad Aspose.CAD di rasterizzare i dati vettoriali in un PDF, usando il layout “Model” per mantenere le linee nascoste nascoste.

```java
PdfOptions pdfOptions = new PdfOptions();
rasterizationOptions.setLayouts(new String[] { "Model" });
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Passo 5: Salva il risultato

Infine, esporta il DWG come file PDF. Le linee nascoste saranno rispettate secondo il layout impostato.

```java
cadImage.save(outPath, pdfOptions);
System.out.println("\nThe DWG file exported successfully to PDF.\nFile saved at " + dataDir);
```

> **Errore comune:** Dimenticare di impostare il layout su `"Model"` farà sì che tutte le linee (incluse quelle nascoste) appaiano solide nel PDF.

## Problemi comuni e soluzioni

| Problema | Perché succede | Come risolvere |
|----------|----------------|----------------|
| Il PDF mostra tutte le linee solide | Layout non impostato su **Model** | Assicurati che `rasterizationOptions.setLayouts(new String[] { "Model" });` sia chiamato prima del salvataggio. |
| Layer mancanti nell'output | Nomi dei layer errati | Verifica i nomi dei layer nel file DWG e corrispondi esattamente nella `list`. |
| Errore di out‑of‑memory su file di grandi dimensioni | Dimensione di rasterizzazione elevata | Riduci le dimensioni della pagina o elabora il disegno a blocchi, se possibile. |

## Domande frequenti

### Q1: Posso usare Aspose.CAD per Java con altri formati di file CAD?
A1: Sì, Aspose.CAD supporta vari formati CAD come DWG, DXF, DWF e altri.

### Q2: È disponibile una versione di prova gratuita per Aspose.CAD per Java?
A2: Sì, puoi trovare la versione di prova gratuita [qui](https://releases.aspose.com/).

### Q3: Come posso ottenere supporto per Aspose.CAD per Java?
A3: Visita il forum di Aspose.CAD [qui](https://forum.aspose.com/c/cad/19) per il supporto della community.

### Q4: Dove posso trovare la documentazione dettagliata per Aspose.CAD per Java?
A4: Consulta la documentazione [qui](https://reference.aspose.com/cad/java/).

### Q5: Posso acquistare una licenza temporanea per Aspose.CAD per Java?
A5: Sì, puoi ottenere una licenza temporanea [qui](https://purchase.aspose.com/temporary-license/).

### Q6: Questo metodo funziona anche per convertire DWG in PDF in un ambiente server headless?
A6: Assolutamente. Poiché il codice utilizza solo l'API di Aspose.CAD, funziona senza dipendenze UI, rendendolo ideale per l'automazione lato server.

## Conclusione

Ora disponi di un metodo completo e pronto per la produzione per **export dwg to pdf** con supporto per le linee nascoste usando Aspose.CAD per Java. Questo approccio può essere integrato in strumenti di elaborazione batch, servizi web o applicazioni desktop per automatizzare la conversione CAD‑to‑PDF.

---

**Last Updated:** 2026-03-05  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}