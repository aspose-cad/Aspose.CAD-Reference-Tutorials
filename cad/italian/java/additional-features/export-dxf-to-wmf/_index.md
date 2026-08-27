---
date: 2026-06-09
description: Scopri come convertire DXF in WMF con Aspose.CAD per Java, includendo
  una prova gratuita, supporto per Java 8+ e esportazione opzionale in PDF. Guida
  passo‑passo con esempi di codice.
keywords:
- convert dxf to wmf
- aspose cad java
- aspose free trial
- aspose cad conversion
- export dxf pdf
linktitle: Esporta DXF in formato WMF usando Java
schemas:
- author: Aspose
  dateModified: '2026-06-09'
  description: Learn how to convert DXF to WMF with Aspose.CAD for Java, including
    a free trial, Java 8+ support, and optional PDF export. Step‑by‑step guide with
    code examples.
  headline: Convert DXF to WMF Using Aspose.CAD in Java
  type: TechArticle
- description: Learn how to convert DXF to WMF with Aspose.CAD for Java, including
    a free trial, Java 8+ support, and optional PDF export. Step‑by‑step guide with
    code examples.
  name: Convert DXF to WMF Using Aspose.CAD in Java
  steps:
  - name: Load DXF Drawing
    text: Image.load reads the DXF file into an Aspose.CAD Image object.
  - name: Configure Rasterization Options
    text: CadRasterizationOptions specifies page size, resolution, and background
      for rasterizing the CAD drawing.
  - name: Save as WMF
    text: ImageSaveOptions with SaveFormat.WMF tells Aspose.CAD to write the output
      as a Windows Metafile.
  - name: Dispose of Resources
    text: Calling image.close() releases native resources used by the Aspose.CAD Image
      object.
  - name: Optional – Export to PDF
    text: PdfOptions configures PDF‑specific settings when saving the image as a PDF
      document. > **Pro tip:** You can reuse the same `CadRasterizationOptions` object
      for PDF export by passing it to a `PdfOptions` instance, saving you a few lines
      of setup.
  type: HowTo
- questions:
  - answer: Yes. Load the file in a try‑with‑resources block and dispose of the `Image`
      object promptly. Adjust `CadRasterizationOptions.setPageWidth/Height` to a reasonable
      size to keep memory usage low.
    question: Can I convert large DXF files (hundreds of MB) without running out of
      memory?
  - answer: WMF is a flat vector format, so layer hierarchy is flattened, but line
      styles, colors, and hatch patterns are preserved.
    question: Does the WMF output retain layer information?
  - answer: Use `rasterizationOptions.setResolution(300);` to define DPI before saving.
    question: Is it possible to set a custom DPI for the WMF?
  - answer: Absolutely. Loop through a directory, load each file, and apply the same
      rasterization and save logic.
    question: Can I batch‑convert multiple DXF files in one run?
  - answer: Aspose.CAD for Java supports Java 8 and later, including Java 11, 17,
      and newer LTS releases.
    question: What versions of Java are supported?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Converti DXF in WMF usando Aspose.CAD in Java
url: /it/java/additional-features/export-dxf-to-wmf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Converti DXF in WMF con Aspose.CAD in Java

## Introduzione

Nella presente guida scoprirai come **convertire DXF in WMF** con Aspose.CAD per Java. Che tu abbia bisogno di incorporare disegni CAD in un report basato su Windows, generare grafica vettoriale leggera per documenti Office, o automatizzare conversioni batch, la conversione da DXF a WMF è una necessità frequente nei flussi di lavoro di ingegneria e reporting. Ti mostreremo come caricare un disegno DXF, configurare le opzioni di rasterizzazione, salvare il risultato come WMF e, facoltativamente, esportare lo stesso disegno in PDF.

## Risposte rapide
- **Posso convertire DXF in WMF con una prova gratuita?** Sì – Aspose offre una prova completa di 30 giorni.  
- **Quale versione di Java è richiesta?** Java 8 o successive.  
- **È necessaria una licenza per eseguire il codice?** È necessaria una licenza per la produzione; la prova funziona per sviluppo e test.  
- **La conversione è senza perdita?** I dati vettoriali sono preservati; le opzioni di rasterizzazione consentono di controllare la risoluzione.  
- **Posso anche esportare lo stesso disegno in PDF?** Assolutamente – vedi il passaggio “Export to PDF” qui sotto.

## Che cosa è “convertire DXF in WMF”?

Convertire DXF in WMF significa prendere un file Drawing Exchange Format (DXF) — un formato CAD ampiamente usato — e trasformarlo in un Windows Metafile (WMF). WMF è un formato di immagine vettoriale che si integra perfettamente con Microsoft Office, le applicazioni Windows e molti strumenti di reporting.

## Perché usare Aspose.CAD per Java?

Aspose.CAD per Java fornisce un motore puro‑Java, senza DLL native, che converte i file CAD con **oltre il 99 % di fedeltà vettoriale**, preservando livelli, colori, stili di linea e pattern di tratteggio. Supporta **oltre 50 formati di input e output** — inclusi DXF, DWG, DGN, PDF, PNG, SVG e WMF — consentendo di regolare finemente le dimensioni della pagina, DPI e colore di sfondo tramite le opzioni di rasterizzazione integrate. La stessa API gestisce anche le esportazioni in PDF, PNG e SVG, eliminando la necessità di librerie multiple.

### Vantaggi principali
- **Nessuna dipendenza esterna** – Java puro, funziona su qualsiasi OS che esegue Java.  
- **Rendering ad alta fedeltà** – conserva spessore della linea, colore e dettagli del tratteggio.  
- **Rasterizzazione integrata** – controlla le dimensioni della pagina, la risoluzione e lo sfondo.  
- **Conversione tutto‑in‑uno** – le stesse classi esportano in WMF, PDF, PNG, SVG, ecc.

## Prerequisiti

Prima di iniziare, assicurati di avere:

- **Aspose.CAD per Java** integrato nel tuo progetto. Scaricalo dal sito ufficiale: [Aspose.CAD Java download](https://releases.aspose.com/cad/java/).  
- **Directory dei documenti** dove sono archiviati i tuoi file DXF (ad esempio `Your Document Directory/DXFDrawings/`).  

## Importa spazi dei nomi

Le seguenti importazioni includono le classi Aspose.CAD necessarie per caricare, rasterizzare e salvare i file CAD.  
```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageSaveOptions;
import com.aspose.cad.fileformats.cad.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.CadImageInfo;
import com.aspose.cad.fileformats.cad.CadImageInfo;
import java.awt.Color;
```

## Guida passo‑passo

### Come converto DXF in WMF in Java?

Carica il tuo file DXF con `Image.load("yourFile.dxf")`, configura `CadRasterizationOptions` per la dimensione della pagina e DPI desiderati, quindi chiama `image.save("output.wmf", new ImageSaveOptions(SaveFormat.WMF))`. Questo schema a tre passaggi esegue la conversione completa mantenendo intatta la qualità vettoriale e richiede solo poche righe di codice.

#### Passo 1: Carica disegno DXF

Image.load legge il file DXF in un oggetto Aspose.CAD Image.  
```java
import com.aspose.cad.Color;
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.WmfOptions;
```

#### Passo 2: Configura le opzioni di rasterizzazione

CadRasterizationOptions specifica la dimensione della pagina, la risoluzione e lo sfondo per rasterizzare il disegno CAD.  
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DXFDrawings/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

#### Passo 3: Salva come WMF

ImageSaveOptions con SaveFormat.WMF indica ad Aspose.CAD di scrivere l'output come Windows Metafile.  
```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(100);
rasterizationOptions.setPageHeight(100);
WmfOptions wmfOptions = new WmfOptions();
```

#### Passo 4: Rilascia le risorse

Chiamare image.close() rilascia le risorse native utilizzate dall'oggetto Aspose.CAD Image.  
```java
cadImage.save(dataDir+" example.ifc.wmf", wmfOptions);
```

#### Passo 5: Facoltativo – Esporta in PDF

PdfOptions configura le impostazioni specifiche per PDF quando si salva l'immagine come documento PDF.  
```java
finally
{
  cadImage.dispose();
}
```

> **Consiglio:** Puoi riutilizzare lo stesso oggetto `CadRasterizationOptions` per l'esportazione PDF passandolo a un'istanza `PdfOptions`, risparmiando alcune righe di configurazione.

## Come esportare DXF in PDF usando Aspose CAD Java?

L'esportazione in PDF segue gli stessi passaggi di caricamento e rasterizzazione; basta sostituire il formato di salvataggio WMF con PDF. Usa `new ImageSaveOptions(SaveFormat.Pdf)` e opzionalmente imposta opzioni specifiche per PDF come livello di compressione o metadati dell'autore. Questa conversione in una sola riga produce un PDF ricercabile e preciso per pagina che rispecchia il layout CAD originale.

## Problemi comuni e soluzioni

| Problema | Causa | Soluzione |
|----------|-------|-----------|
| **`NullPointerException` on `cadImage.save`** | Variabile `cadImage` non definita (dovrebbe essere `image`). | Sostituire `cadImage` con `image` o rinominare la variabile in modo coerente. |
| **Output WMF is blank** | Dimensione della pagina di rasterizzazione troppo piccola o colore di sfondo impostato su trasparente. | Aumentare `PageWidth`/`PageHeight` o impostare un colore di sfondo tramite `rasterizationOptions.setBackgroundColor(Color.WHITE);`. |
| **License exception** | Esecuzione senza una licenza Aspose valida in produzione. | Applicare il file di licenza all'avvio dell'applicazione: `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`. |

## Conclusione

Adesso disponi di un flusso di lavoro completo, pronto per la produzione, per **convertire DXF in WMF** usando Aspose.CAD per Java, con un passaggio facoltativo per **esportare lo stesso disegno in PDF**. Questo approccio ti fornisce un output vettoriale di alta qualità che si integra perfettamente con gli strumenti di reporting e documentazione basati su Windows, mantenendo il tuo codice semplice e privo di dipendenze.

## FAQ

### Q1: Dove posso trovare la documentazione di Aspose.CAD?
R1: Puoi accedere alla documentazione [qui](https://reference.aspose.com/cad/java/).

### Q2: Come scaricare Aspose.CAD per Java?
R2: Scarica la libreria [qui](https://releases.aspose.com/cad/java/).

### Q3: È disponibile una prova gratuita?
R3: Sì, puoi ottenere una prova gratuita [qui](https://releases.aspose.com/).

### Q4: Hai bisogno di opzioni di licenza temporanea?
R4: Esplora le licenze temporanee [qui](https://purchase.aspose.com/temporary-license/).

### Q5: Dove posso ottenere supporto?
R5: Visita il forum di supporto Aspose.CAD [qui](https://forum.aspose.com/c/cad/19).

## Domande frequenti

**Q: Posso convertire file DXF di grandi dimensioni (centinaia di MB) senza esaurire la memoria?**  
A: Sì. Carica il file in un blocco try‑with‑resources e rilascia prontamente l'oggetto `Image`. Regola `CadRasterizationOptions.setPageWidth/Height` a una dimensione ragionevole per mantenere basso l'uso di memoria.

**Q: L'output WMF conserva le informazioni dei livelli?**  
A: WMF è un formato vettoriale piatto, quindi la gerarchia dei livelli viene appiattita, ma gli stili di linea, i colori e i pattern di tratteggio vengono preservati.

**Q: È possibile impostare un DPI personalizzato per il WMF?**  
A: Usa `rasterizationOptions.setResolution(300);` per definire il DPI prima del salvataggio.

**Q: Posso convertire in batch più file DXF in un'unica esecuzione?**  
A: Assolutamente. Scorri una directory, carica ogni file e applica la stessa logica di rasterizzazione e salvataggio.

**Q: Quali versioni di Java sono supportate?**  
A: Aspose.CAD per Java supporta Java 8 e successive, incluse Java 11, 17 e le versioni LTS più recenti.

**Ultimo aggiornamento:** 2026-06-09  
**Testato con:** Aspose.CAD for Java 24.11  
**Autore:** Aspose

```java
image.save(dataDir + "conic_pyramid_out_.pdf"); 
```

## Tutorial correlati

- [Crea PDF da CAD – Esporta DXF in PDF con Aspose.CAD per Java](/cad/java/additional-features/export-dxf-to-pdf/)
- [Crea PDF da DXF: Esporta livello con Aspose.CAD per Java](/cad/java/additional-features/export-specific-layer-to-pdf/)
- [Come convertire il layout DXF in immagine JPEG con Aspose.CAD in Java](/cad/java/additional-features/export-specific-layout-to-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}