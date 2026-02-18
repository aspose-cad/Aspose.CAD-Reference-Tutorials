---
date: 2026-01-07
description: Scopri come esportare CAD in PDF e convertire DGN in PDF usando Aspose.CAD
  per Java. Guida passo‑passo per gli sviluppatori Java.
linktitle: Export Embedded DGN
second_title: Aspose.CAD Java API
title: Esporta CAD in PDF – Esporta DGN incorporato con Aspose.CAD per Java
url: /it/java/dgn-export-options/export-embedded-dgn/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Esporta CAD in PDF – Esporta DGN incorporato con Aspose.CAD per Java

## Introduzione

In questo tutorial scoprirai **come esportare CAD in PDF** convertendo un file DGN incorporato in un documento PDF ad alta qualità con Aspose.CAD per Java. Aspose.CAD è una libreria robusta che offre agli sviluppatori Java il pieno controllo sulla manipolazione dei file CAD, sia che tu abbia bisogno di **convertire DGN in PDF**, **convertire DWG in PDF**, o semplicemente di renderizzare disegni CAD in altri formati. Segui la guida passo‑passo qui sotto e potrai integrare questa funzionalità nelle tue applicazioni in pochi minuti.

## Risposte rapide
- **Che cosa significa “export CAD to PDF”?** Converte i disegni CAD (DWG, DGN, ecc.) in file PDF preservando la qualità vettoriale.  
- **Quale libreria viene utilizzata?** Aspose.CAD per Java.  
- **È necessaria una licenza?** È necessaria una licenza per la produzione; è disponibile una versione di prova gratuita.  
- **Quali sono i prerequisiti principali?** Ambiente di sviluppo Java e il JAR di Aspose.CAD per Java.  
- **Posso personalizzare l'output?** Sì – è possibile selezionare layout, impostare le opzioni di rasterizzazione e controllare le impostazioni PDF.

## Che cos'è “export CAD to PDF”?

Esportare CAD in PDF significa prendere un file CAD nativo (come DWG o DGN) e generare un documento PDF che rappresenta fedelmente la geometria originale. Il PDF può essere visualizzato su qualsiasi piattaforma senza necessità di software CAD, rendendolo ideale per la condivisione, la stampa o l'archiviazione.

## Perché usare Aspose.CAD per Java per convertire DGN in PDF?

- **Nessuna dipendenza esterna** – funziona interamente in Java.  
- **Preserva i dati vettoriali** – i PDF rimangono nitidi a qualsiasi livello di zoom.  
- **Controllo granulare** – scegli layout specifici, imposta DPI di rasterizzazione e incorpora font.  
- **Pronto per l'impresa** – supporta file di grandi dimensioni, elaborazione batch e opzioni di licenza.

## Prerequisiti

Prima di iniziare, assicurati di avere quanto segue:

- **Ambiente di sviluppo Java** – JDK 8 o superiore installato e configurato.  
- **Aspose.CAD per Java** – scarica l'ultimo JAR da [qui](https://releases.aspose.com/cad/java/).

## Importa pacchetti

Per iniziare, è necessario importare le classi necessarie nel tuo progetto Java. Aggiungi le seguenti istruzioni di importazione al tuo file sorgente:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Come esportare DGN in PDF usando Aspose.CAD per Java?

Di seguito trovi una chiara procedura numerata che mostra esattamente come convertire un file DGN incorporato (memorizzato all'interno di un DWG) in un PDF.

### Passo 1: Configura i percorsi di input e output

Definisci la directory che contiene il tuo file di origine e specifica il DWG che contiene il DGN incorporato.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
```

### Passo 2: Carica il file DWG

Carica il file DWG in un oggetto `Image`. Aspose.CAD rileva automaticamente i dati DGN incorporati.

```java
Image objImage = Image.load(fileName);
```

### Passo 3: Configura le opzioni di rasterizzazione

Seleziona quale layout (o layout) desideri includere nel PDF. In questo esempio esportiamo solo il layout **Model**.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setLayouts(new String[] {"Model"});
```

### Passo 4: Configura le opzioni PDF

Allega le impostazioni di rasterizzazione alle opzioni di esportazione PDF.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Passo 5: Salva il file PDF

Infine, scrivi il PDF su disco utilizzando le opzioni configurate.

```java
objImage.save(dataDir + "BlockRefDgn.pdf", pdfOptions);
```

## Converti DWG in PDF – un suggerimento aggiuntivo

Se il tuo file di origine è un semplice DWG (senza DGN incorporato), puoi riutilizzare lo stesso codice – basta cambiare `fileName` per puntare al DWG che desideri convertire. Le opzioni di rasterizzazione e PDF rimangono identiche, offrendoti un flusso di lavoro **convert DWG to PDF** coerente.

## Problemi comuni e soluzioni

| Problema | Motivo | Soluzione |
|----------|--------|-----------|
| **PDF vuoto** | Nome del layout non corrispondente | Verifica che il nome del layout passato a `setLayouts` corrisponda esattamente al layout nel file di origine (case‑sensitive). |
| **Eccezione di licenza** | Uso della versione di prova senza licenza | Applica una licenza valida di Aspose.CAD prima di caricare l'immagine (`License license = new License(); license.setLicense("Aspose.CAD.lic");`). |
| **File non trovato** | Percorso `dataDir` errato | Usa un percorso assoluto o assicurati che il percorso relativo sia corretto rispetto alla directory di lavoro del progetto. |
| **Grafica a bassa risoluzione** | Il DPI di rasterizzazione predefinito è basso | Imposta `rasterizationOptions.setPageWidth/Height` o `setResolution` per aumentare il DPI. |

## Domande frequenti

**D: Posso usare Aspose.CAD per Java in un progetto commerciale?**  
R: Sì, Aspose.CAD per Java è una libreria commerciale. Puoi ottenere una licenza da [qui](https://purchase.aspose.com/buy).

**D: È disponibile una versione di prova gratuita?**  
R: Sì, puoi accedere a una versione di prova gratuita di Aspose.CAD per Java [qui](https://releases.aspose.com/).

**D: Come posso ottenere supporto per Aspose.CAD per Java?**  
R: Puoi richiedere supporto alla community di Aspose.CAD sul [forum](https://forum.aspose.com/c/cad/19).

**D: Cosa fare se ho bisogno di una licenza temporanea?**  
R: Puoi ottenere una licenza temporanea [qui](https://purchase.aspose.com/temporary-license/).

**D: Dove posso trovare la documentazione?**  
R: La documentazione è disponibile [qui](https://reference.aspose.com/cad/java/).

## Conclusione

Ora hai imparato come **esportare CAD in PDF**, in particolare come **convertire DGN in PDF** e persino **convertire DWG in PDF** usando Aspose.CAD per Java. Seguendo i passaggi sopra, puoi integrare una conversione CAD‑to‑PDF senza soluzione di continuità in qualsiasi soluzione basata su Java, fornendo PDF di alta qualità ai tuoi utenti senza la necessità di software CAD aggiuntivo.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Ultimo aggiornamento:** 2026-01-07  
**Testato con:** Aspose.CAD for Java 24.12  
**Autore:** Aspose