---
title: Esporta layout CAD in PDF con Aspose.CAD per Java
linktitle: Esporta layout CAD in PDF
second_title: API Java Aspose.CAD
description: Esplora Aspose.CAD per Java per esportare facilmente layout CAD in PDF. Efficiente, affidabile e facile da usare per gli sviluppatori.
type: docs
weight: 11
url: /it/java/cad-export-options/export-cad-layouts-to-pdf/
---
## introduzione

Nel campo in continua evoluzione della progettazione assistita da computer (CAD), Aspose.CAD per Java si distingue come un potente strumento per manipolare e convertire file CAD. In questo tutorial ti guideremo attraverso il processo di esportazione di layout CAD in PDF utilizzando Aspose.CAD per Java. Che tu sia uno sviluppatore esperto o che tu stia semplicemente immergendoti nel mondo del CAD, questa guida passo passo ti aiuterà a sfruttare tutto il potenziale di questa versatile libreria Java.

## Prerequisiti

Prima di immergerci nel tutorial, assicurati di disporre dei seguenti prerequisiti:

-  Aspose.CAD per Java: assicurati di avere la libreria installata. Puoi scaricarlo dal sito Aspose[Qui](https://releases.aspose.com/cad/java/).

- Ambiente di sviluppo Java: assicurati di avere un ambiente di sviluppo Java configurato sul tuo computer.

Ora che hai impostato tutto, iniziamo con il tutorial.

## Importa spazi dei nomi

Nel tuo codice Java, inizia importando gli spazi dei nomi necessari. Queste importazioni forniscono l'accesso alle classi e ai metodi necessari per lavorare con Aspose.CAD per Java.

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterpolationMode;
import com.aspose.cad.SmoothingMode;
import com.aspose.cad.TextRenderingHint;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//importa com.aspose.cad.imageoptions.TypeOfEntities;
```

## Passaggio 1: caricare il file CAD

 Inizia caricando il file CAD nella tua applicazione Java utilizzando il file`Image.load` metodo. Sostituire`"conic_pyramid.dxf"` con il percorso del file CAD.

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

## Passaggio 2: imposta le opzioni di rasterizzazione

 Crea un'istanza di`CadRasterizationOptions` per definire come devono essere rasterizzate le entità CAD. Regola parametri quali larghezza della pagina, altezza della pagina e ridimensionamento del layout in base alle tue esigenze.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(false);
rasterizationOptions.setContentAsBitmap(true);
rasterizationOptions.setLayouts(new String[]{"Model"});
```

## Passaggio 3: imposta le opzioni PDF

 Crea un'istanza di`PdfOptions` e associarlo alle opzioni di rasterizzazione. Inoltre, imposta le opzioni grafiche per l'esportazione PDF, come la modalità di smussamento, il suggerimento per il rendering del testo e la modalità di interpolazione.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.getGraphicsOptions().setSmoothingMode(SmoothingMode.HighQuality);
rasterizationOptions.getGraphicsOptions().setTextRenderingHint(TextRenderingHint.AntiAliasGridFit);
rasterizationOptions.getGraphicsOptions().setInterpolationMode(InterpolationMode.HighQualityBicubic);
```

## Passaggio 4: esporta in PDF

 Infine, esporta i layout CAD in un file PDF utilizzando il file`save` metodo del`cadImage` oggetto.

```java
cadImage.save(dataDir + "CADLayoutsToPDF_out_.pdf", pdfOptions);
```

Congratulazioni! Hai esportato con successo layout CAD in PDF utilizzando Aspose.CAD per Java. Sentiti libero di esplorare caratteristiche e funzionalità aggiuntive offerte da Aspose.CAD per migliorare la tua esperienza di manipolazione dei file CAD.

## Conclusione

In questo tutorial, abbiamo esaminato il processo di esportazione dei layout CAD in PDF utilizzando Aspose.CAD per Java. Con le sue funzionalità robuste e l'API facile da usare, Aspose.CAD consente agli sviluppatori di lavorare in modo efficiente con i file CAD nelle loro applicazioni Java.

## Domande frequenti

### Q1: Posso utilizzare Aspose.CAD per Java con altri formati di file CAD?

 A1: Sì, Aspose.CAD supporta vari formati CAD, inclusi DWG, DXF, DWF e altri. Controlla la documentazione[Qui](https://reference.aspose.com/cad/java/) per un elenco completo.

### Q2: È disponibile una prova gratuita per Aspose.CAD per Java?

 A2: Sì, puoi esplorare le funzionalità di Aspose.CAD con una prova gratuita[Qui](https://releases.aspose.com/).

### Q3: Come posso ottenere supporto per Aspose.CAD per Java?

 A3: visitare il forum Aspose.CAD[Qui](https://forum.aspose.com/c/cad/19) per il sostegno della comunità. Per il supporto premium, considera l'acquisto di una licenza[Qui](https://purchase.aspose.com/buy).

### Q4: Qual è la differenza tra il ridimensionamento del layout automatico e quello manuale?

A4: il ridimensionamento automatico del layout regola le dimensioni del layout in base alle dimensioni della pagina specificate, mentre il ridimensionamento manuale consente di impostare valori di ridimensionamento personalizzati.

### Q5: Posso personalizzare l'aspetto dei file PDF esportati?

R5: Sì, puoi personalizzare le opzioni grafiche nel codice per controllare la qualità e l'aspetto del PDF esportato.