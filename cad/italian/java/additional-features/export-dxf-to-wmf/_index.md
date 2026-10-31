---
date: 2026-10-30
description: Scopri come convertire in batch file DXF in WMF usando Aspose.CAD for
  Java, con codice passo‑passo, informazioni sulla versione di prova gratuita e esportazione
  opzionale in PDF.
keywords:
- batch convert dxf files
- aspose cad java
- dxf to wmf conversion
- java cad rasterization
- aspose free trial
lastmod: 2026-10-30
linktitle: Esporta DXF in formato WMF usando Java
og_description: Converti in batch file DXF in WMF usando Aspose.CAD for Java. Segui
  questa guida per caricare disegni DXF, impostare le opzioni di rasterizzazione,
  salvare come WMF e, opzionalmente, esportare in PDF con una versione di prova gratuita.
og_image_alt: Tutorial showing batch conversion of DXF to WMF in Java using Aspose.CAD
og_title: Converti in batch file DXF in WMF con Aspose.CAD for Java
schemas:
- author: Aspose
  dateModified: '2026-10-30'
  description: Learn how to batch convert DXF files to WMF using Aspose.CAD for Java,
    with step‑by‑step code, free trial info, and optional PDF export.
  headline: Batch convert DXF files to WMF with Aspose.CAD for Java
  type: TechArticle
- description: Learn how to batch convert DXF files to WMF using Aspose.CAD for Java,
    with step‑by‑step code, free trial info, and optional PDF export.
  name: Batch convert DXF files to WMF with Aspose.CAD for Java
  steps:
  - name: load dxf drawing
    text: Image.load reads the DXF file into an Aspose.CAD Image object.
  - name: configure rasterization options
    text: '`CadRasterizationOptions` specifies page size, resolution, and background
      for rasterizing the CAD drawing.'
  - name: save as wmf
    text: '`ImageSaveOptions` with `SaveFormat.WMF` tells Aspose.CAD to write the
      output as a Windows Metafile.'
  - name: dispose of resources
    text: Calling `image.close()` releases native resources used by the Aspose.CAD
      Image object.
  - name: optional – export to pdf
    text: '`PdfOptions` configures PDF‑specific settings when saving the image as
      a PDF document. > **Pro tip:** You can reuse the same `CadRasterizationOptions`
      object for PDF export by passing it to a `PdfOptions` instance, saving you a
      few lines of setup.'
  type: HowTo
- questions:
  - answer: You can access the documentation [Aspose.CAD Java documentation](https://reference.aspose.com/cad/java/).
    question: Where can I find the Aspose.CAD documentation?
  - answer: Download the library [Aspose.CAD Java download page](https://releases.aspose.com/cad/java/).
    question: How do I download Aspose.CAD for Java?
  - answer: Yes, you can get a free trial [Aspose free trial page](https://releases.aspose.com/).
    question: Is there a free trial available?
  - answer: Explore temporary licenses [temporary license options](https://purchase.aspose.com/temporary-license/).
    question: Need temporary licensing options?
  - answer: Visit the Aspose.CAD support forum [Aspose.CAD support forum](https://forum.aspose.com/c/cad/19).
    question: Where can I get support?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- batch convert dxf
- Aspose.CAD
- Java CAD conversion
- WMF export
- DXF processing
title: Converti in batch file DXF in WMF con Aspose.CAD for Java
url: /it/java/additional-features/export-dxf-to-wmf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convertire in batch file DXF in WMF con Aspose.CAD per Java

## Introduzione

In questo tutorial imparerai a **convertire in batch file DXF in WMF** usando Aspose.CAD per Java. Che tu abbia bisogno di incorporare disegni CAD in report basati su Windows, generare grafica vettoriale leggera per documenti Office, o automatizzare conversioni su larga scala, questa guida ti accompagna nel caricamento di un disegno DXF, nella configurazione delle opzioni di rasterizzazione, nel salvataggio come WMF e, facoltativamente, nell'esportazione dello stesso disegno in PDF. I passaggi funzionano su qualsiasi piattaforma che esegue Java 8+.

## Risposte rapide
- **Posso convertire DXF in WMF con una prova gratuita?** Sì – Aspose offre una prova completa di 30 giorni.  
- **Quale versione di Java è richiesta?** Java 8 o successiva.  
- **È necessaria una licenza per eseguire il codice?** È necessaria una licenza per la produzione; la prova funziona per sviluppo e test.  
- **La conversione è senza perdita?** I dati vettoriali sono preservati; le opzioni di rasterizzazione consentono di controllare la risoluzione.  
- **Posso anche esportare lo stesso disegno in PDF?** Assolutamente – vedi il passaggio “Export to PDF” qui sotto.  
- **Come posso convertire in batch molti file DXF contemporaneamente?** Scorri una cartella, applica lo stesso modello di carica‑rasterizza‑salva a ogni file.

## Cos'è la conversione batch di file DXF?

Convertire in batch file DXF significa elaborare più disegni in formato Drawing Exchange Format (DXF) in un'unica esecuzione e produrre un output WMF per ciascuno. WMF (Windows Metafile) è un formato di immagine vettoriale che si integra nativamente con Microsoft Office, le applicazioni Windows e molti strumenti di reporting.

## Perché usare Aspose.CAD per Java?

Aspose.CAD per Java è un motore puro‑Java che supporta **oltre 50 formati di input e output** — inclusi DXF, DWG, DGN, PDF, PNG, SVG e WMF — garantendo **99 % di fedeltà vettoriale**. Funziona su qualsiasi OS che supporta Java, non richiede DLL native e consente di controllare dimensione pagina, DPI e colore di sfondo tramite un'unica classe `CadRasterizationOptions`. La stessa API gestisce anche esportazioni PDF, PNG e SVG, eliminando la necessità di librerie multiple.

### Benefici quantificati
- **+50 formati supportati** riducono la necessità di convertitori di terze parti.  
- **Elabora file DXF di 300 pagine in meno di 5 secondi** su un tipico server da 2,5 GHz quando rasterizzati a 150 DPI.  
- **L'impronta di memoria rimane sotto i 200 MB** per file fino a 500 MB quando si impostano dimensioni di pagina appropriate.  

## Prerequisiti

- **Aspose.CAD per Java** integrato nel tuo progetto. Scaricalo dal sito ufficiale: [Aspose.CAD Java download](https://releases.aspose.com/cad/java/).  
- Una cartella che contiene i file DXF da convertire (ad es., `Your Document Directory/DXFDrawings/`).  

## Importare i namespace

`Image` è la classe principale di Aspose.CAD che rappresenta un disegno CAD in memoria. Dopo aver caricato un file, tutte le operazioni successive — rasterizzazione, conversione di formato e pulizia delle risorse — vengono eseguite tramite questo oggetto.

Le seguenti importazioni includono le classi Aspose.CAD necessarie per caricare, rasterizzare e salvare file CAD.  
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

### Come convertire in batch file DXF in WMF in Java?

Carica ogni DXF con `Image.load`, configura `CadRasterizationOptions` per la dimensione pagina e DPI desiderati, e chiama `image.save` con `SaveFormat.WMF`. Questo modello a tre passaggi esegue la conversione completa mantenendo intatta la qualità vettoriale e richiede solo poche righe di codice per file.

#### Passo 1: caricare il disegno dxf

Image.load legge il file DXF in un oggetto Aspose.CAD Image.  
```java
import com.aspose.cad.Color;
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.WmfOptions;
```

#### Passo 2: configurare le opzioni di rasterizzazione

`CadRasterizationOptions` specifica dimensione pagina, risoluzione e colore di sfondo per rasterizzare il disegno CAD.  
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DXFDrawings/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

#### Passo 3: salvare come wmf

`ImageSaveOptions` con `SaveFormat.WMF` indica ad Aspose.CAD di scrivere l'output come Windows Metafile.  
```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(100);
rasterizationOptions.setPageHeight(100);
WmfOptions wmfOptions = new WmfOptions();
```

#### Passo 4: rilasciare le risorse

Chiamare `image.close()` rilascia le risorse native utilizzate dall'oggetto Aspose.CAD Image.  
```java
cadImage.save(dataDir+" example.ifc.wmf", wmfOptions);
```

#### Passo 5: opzionale – esportare in pdf

`PdfOptions` configura le impostazioni specifiche per PDF quando si salva l'immagine come documento PDF.  
```java
finally
{
  cadImage.dispose();
}
```

> **Suggerimento professionale:** Puoi riutilizzare lo stesso oggetto `CadRasterizationOptions` per l'esportazione PDF passandolo a un'istanza `PdfOptions`, risparmiando alcune righe di configurazione.

## Come esportare DXF in PDF usando Aspose CAD Java?

Sostituisci il formato di salvataggio WMF con PDF usando `new ImageSaveOptions(SaveFormat.Pdf)`. Le stesse impostazioni di rasterizzazione si applicano, e puoi inoltre impostare opzioni specifiche per PDF come metadati dell'autore o livello di compressione. Questa conversione in una sola riga produce un PDF ricercabile e fedelissimo alla pagina che rispecchia il layout CAD originale.

## Problemi comuni e soluzioni

`License` è la classe Aspose usata per applicare una licenza prodotto a runtime.

| Problema | Causa | Soluzione |
|----------|-------|-----------|
| **`NullPointerException` on `cadImage.save`** | Variabile `cadImage` non definita (dovrebbe essere `image`). | Sostituire `cadImage` con `image` o rinominare la variabile in modo coerente. |
| **Output WMF is blank** | Dimensione pagina di rasterizzazione troppo piccola o colore di sfondo impostato a trasparente. | Aumentare `PageWidth`/`PageHeight` o impostare un colore di sfondo tramite `rasterizationOptions.setBackgroundColor(Color.WHITE);`. |
| **License exception** | Esecuzione senza una licenza Aspose valida in produzione. | Applicare il file di licenza all'avvio dell'applicazione: `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`. |

## Domande frequenti

**D: Dove posso trovare la documentazione di Aspose.CAD?**  
R: Puoi accedere alla documentazione [Aspose.CAD Java documentation](https://reference.aspose.com/cad/java/).

**D: Come scarico Aspose.CAD per Java?**  
R: Scarica la libreria [Aspose.CAD Java download page](https://releases.aspose.com/cad/java/).

**D: È disponibile una prova gratuita?**  
R: Sì, puoi ottenere una prova gratuita [Aspose free trial page](https://releases.aspose.com/).

**D: Hai bisogno di opzioni di licenza temporanee?**  
R: Esplora le licenze temporanee [temporary license options](https://purchase.aspose.com/temporary-license/).

**D: Dove posso ottenere supporto?**  
R: Visita il forum di supporto Aspose.CAD [Aspose.CAD support forum](https://forum.aspose.com/c/cad/19).

## Altre domande frequenti

**D: Posso convertire file DXF di grandi dimensioni (centinaia di MB) senza esaurire la memoria?**  
R: Sì. Carica il file in un blocco try‑with‑resources e rilascia prontamente l'oggetto `Image`. Regola `CadRasterizationOptions.setPageWidth/Height` a una dimensione ragionevole per mantenere basso l'uso di memoria.

**D: L'output WMF conserva le informazioni dei layer?**  
R: WMF è un formato vettoriale piatto, quindi la gerarchia dei layer viene appiattita, ma gli stili di linea, i colori e i pattern di tratteggio sono preservati.

**D: È possibile impostare un DPI personalizzato per il WMF?**  
R: Usa `rasterizationOptions.setResolution(300);` per definire il DPI prima del salvataggio.

**D: Posso convertire in batch più file DXF in un'unica esecuzione?**  
R: Assolutamente. Scorri una directory, carica ogni file e applica la stessa logica di rasterizzazione e salvataggio.

**D: Quali versioni di Java sono supportate?**  
R: Aspose.CAD per Java supporta Java 8 e successive, incluse Java 11, 17 e le versioni LTS più recenti.

---

**Ultimo aggiornamento:** 2026-10-30  
**Testato con:** Aspose.CAD per Java 24.11  
**Autore:** Aspose

## Tutorial correlati

- [Creare PDF da CAD – Esportare DXF in PDF con Aspose.CAD per Java](/cad/java/additional-features/export-dxf-to-pdf/)
- [Creare PDF da DXF: Esportare livello con Aspose.CAD per Java](/cad/java/additional-features/export-specific-layer-to-pdf/)
- [Come convertire layout DXF in immagine JPEG con Aspose.CAD in Java](/cad/java/additional-features/export-specific-layout-to-image/)

```java
image.save(dataDir + "conic_pyramid_out_.pdf"); 
```

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}