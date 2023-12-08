---
title: Esporta DGN incorporato in PDF con Aspose.CAD per Java
linktitle: Esporta DGN incorporato
second_title: API Java Aspose.CAD
description: Esplora la guida passo passo sull'esportazione di file DGN incorporati in PDF utilizzando Aspose.CAD per Java. Migliora le tue applicazioni Java con la manipolazione fluida dei file CAD.
type: docs
weight: 11
url: /it/java/dgn-export-options/export-embedded-dgn/
---
## introduzione

Benvenuti in questo tutorial completo sull'esportazione di file DGN incorporati utilizzando Aspose.CAD per Java. Aspose.CAD è una potente libreria che consente agli sviluppatori Java di lavorare senza problemi con i file CAD. In questo tutorial ti guideremo attraverso il processo di esportazione di file DGN incorporati in PDF utilizzando istruzioni dettagliate. Che tu sia uno sviluppatore esperto o che tu abbia appena iniziato, questo tutorial ti aiuterà a sfruttare le funzionalità di Aspose.CAD per migliorare le tue applicazioni Java.

## Prerequisiti

Prima di immergerci nel tutorial, assicurati di avere i seguenti prerequisiti:
- Ambiente di sviluppo Java: assicurati di avere un ambiente di sviluppo Java configurato sul tuo computer.
-  Aspose.CAD per Java: scarica e installa la libreria Aspose.CAD per Java da[Qui](https://releases.aspose.com/cad/java/).

## Importa pacchetti

Per iniziare, devi importare i pacchetti necessari nel tuo progetto Java. Aggiungi le seguenti istruzioni di importazione al tuo codice:

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

Ora suddividiamo il codice di esempio in più passaggi:

## Passaggio 1: impostare i percorsi di input e output

Definire il percorso della directory in cui si trova il documento e specificare il nome del file DWG di input.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
```

## Passaggio 2: caricare il file DWG

 Caricare il file DWG in un file`Image` oggetto utilizzando Aspose.CAD.

```java
Image objImage = Image.load(fileName);
```

## Passaggio 3: configurare le opzioni di rasterizzazione

Configura le opzioni di rasterizzazione, come i layout da includere nell'esportazione.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setLayouts(new String[] {"Model"});
```

## Passaggio 4: configura le opzioni PDF

Configura le opzioni PDF, comprese le opzioni di rasterizzazione vettoriale.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Passaggio 5: salva il file PDF

Salvare il file PDF con le opzioni configurate.
```java
objImage.save(dataDir + "BlockRefDgn.pdf", pdfOptions);
```

## Conclusione

Congratulazioni! Hai esportato con successo un file DGN incorporato in PDF utilizzando Aspose.CAD per Java. Questo tutorial ha coperto i passaggi essenziali per integrare Aspose.CAD nella tua applicazione Java per un'efficiente manipolazione dei file CAD.

## Domande frequenti

### Q1: Posso utilizzare Aspose.CAD per Java in un progetto commerciale?

 A1: Sì, Aspose.CAD per Java è una libreria commerciale. È possibile ottenere una licenza da[Qui](https://purchase.aspose.com/buy).

### Q2: È disponibile una prova gratuita?

 A2: Sì, puoi accedere a una prova gratuita di Aspose.CAD per Java[Qui](https://releases.aspose.com/).

### Q3: Come posso ottenere supporto per Aspose.CAD per Java?

A3: Puoi chiedere supporto alla comunità Aspose.CAD su[Forum](https://forum.aspose.com/c/cad/19).

### Q4: Cosa succede se ho bisogno di una licenza temporanea?

 A4: È possibile ottenere una licenza temporanea[Qui](https://purchase.aspose.com/temporary-license/).

### Q5: Dove posso trovare la documentazione?

 A5: La documentazione è disponibile[Qui](https://reference.aspose.com/cad/java/).