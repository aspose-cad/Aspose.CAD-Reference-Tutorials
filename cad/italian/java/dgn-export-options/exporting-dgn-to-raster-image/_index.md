---
title: Conversione da Java DGN a JPEG con Aspose.CAD Tutorial
linktitle: Esportazione di DGN dal formato AutoCAD al formato immagine raster
second_title: API Java Aspose.CAD
description: Scopri come esportare file DGN in immagini JPEG in Java utilizzando Aspose.CAD. Questo tutorial passo passo ti guida attraverso il processo senza sforzo.
weight: 13
url: /it/java/dgn-export-options/exporting-dgn-to-raster-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Conversione da Java DGN a JPEG con Aspose.CAD Tutorial

## introduzione

Benvenuti in questo tutorial completo sull'esportazione di file DGN (Design) in formato immagine raster utilizzando Aspose.CAD per Java. Aspose.CAD è una potente libreria che consente agli sviluppatori Java di lavorare senza problemi con i file CAD. In questo tutorial ti guideremo attraverso il processo di conversione dei file DGN in immagini JPEG, fornendoti istruzioni dettagliate ed esempi di codice.

## Prerequisiti

Prima di immergerti nel tutorial, assicurati di avere i seguenti prerequisiti:
1.  Libreria Aspose.CAD: assicurarsi di avere installata la libreria Aspose.CAD per Java. Puoi scaricarlo[Qui](https://releases.aspose.com/cad/java/).
2. Java Development Kit (JDK): assicurati di avere Java installato sul tuo computer.
3. Ambiente di sviluppo integrato (IDE): utilizzare un IDE compatibile con Java come IntelliJ o Eclipse.

## Importa pacchetti

Nel tuo progetto Java, importa i pacchetti necessari per Aspose.CAD. Aggiungi le seguenti righe al tuo codice:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
```

## Passaggio 1: caricare il file DGN

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
DgnImage dgnImage = (DgnImage) Image.load(dataDir + "Nikon_D90_Camera.dgn");
```

## Passaggio 2: crea l'oggetto JpegOptions

```java
ImageOptionsBase options = new JpegOptions();
```

## Passaggio 3: assegnare le opzioni di rasterizzazione

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(600);
vectorOptions.setPageHeight(400);
vectorOptions.setNoScaling(true);
vectorOptions.setAutomaticLayoutsScaling(false);
options.setVectorRasterizationOptions(vectorOptions);
```

## Passaggio 4: salva l'immagine convertita

```java
OutputStream outStream = new FileOutputStream(dataDir + "ExportDGNToRasterImage_Out.jpg");
dgnImage.save(outStream, options);
```

Ripeti questi passaggi per i tuoi file DGN specifici, regolando di conseguenza i percorsi dei file.

## Conclusione

Congratulazioni! Hai imparato con successo come esportare file DGN in formato immagine raster utilizzando Aspose.CAD per Java. Questo tutorial ti ha fornito le conoscenze per incorporare questa funzionalità nelle tue applicazioni Java.

## Domande frequenti

### Q1: Posso utilizzare Aspose.CAD per Java con altri formati di file CAD?

A1: Sì, Aspose.CAD supporta vari formati CAD, fornendo una soluzione versatile per gli sviluppatori Java.

### Q2: È disponibile una prova gratuita per Aspose.CAD per Java?

 R2: Sì, puoi accedere a una prova gratuita[Qui](https://releases.aspose.com/).

### Q3: Dove posso trovare la documentazione per Aspose.CAD per Java?

 R3: Fare riferimento alla documentazione[Qui](https://reference.aspose.com/cad/java/).

### Q4: Come posso ottenere supporto per Aspose.CAD per Java?

 R4: Visita il forum di supporto[Qui](https://forum.aspose.com/c/cad/19).

### Q5: Dove posso acquistare una licenza per Aspose.CAD per Java?

 A5: È possibile acquistare una licenza[Qui](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
