---
title: Esportazione semplice di DGN in AutoCAD PDF con Aspose.CAD per Java
linktitle: Esportazione di DGN in formato AutoCAD in PDF
second_title: API Java Aspose.CAD
description: Esplora la guida passo passo sull'esportazione di file DGN in formato AutoCAD in PDF utilizzando Aspose.CAD per Java. Migliora facilmente le capacità di gestione CAD della tua applicazione Java.
weight: 12
url: /it/java/dgn-export-options/exporting-dgn-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Esportazione semplice di DGN in AutoCAD PDF con Aspose.CAD per Java

## introduzione

Benvenuti in questo tutorial completo sull'utilizzo di Aspose.CAD per Java per esportare file DGN in formato AutoCAD in PDF. Se stai cercando di migliorare la capacità della tua applicazione Java di gestire file CAD, Aspose.CAD è una scelta eccellente. In questo tutorial ti guideremo passo dopo passo attraverso il processo di esportazione dei file DGN.


## Prerequisiti
Prima di immergerci nel tutorial, assicurati di avere i seguenti prerequisiti:
-  Libreria Aspose.CAD: assicurarsi di avere installata la libreria Aspose.CAD per Java. Puoi scaricarlo[Qui](https://releases.aspose.com/cad/java/).
- Directory dei documenti: imposta una directory dei documenti in cui verranno archiviati i file di input e output.

## Importa pacchetti

Nel tuo progetto Java, importa i pacchetti necessari per accedere alle funzionalità Aspose.CAD:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Ora suddividiamo il codice di esempio in più passaggi:

## Passaggio 1: definire i percorsi dei file

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

Assicurati di sostituire "La tua directory dei documenti" con il percorso effettivo in cui si trovano i tuoi file.

## Passaggio 2: caricare l'immagine DGN

```java
DgnImage objImage = (DgnImage) Image.load(fileName);
```

Caricare il file DGN utilizzando Aspose.CAD.

## Passaggio 3: imposta le opzioni di esportazione PDF

```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); // Esporta visualizzazioni specifiche
options.setVectorRasterizationOptions(vectorOptions);
```

Definisci le opzioni di esportazione PDF, comprese le dimensioni della pagina e le preferenze di layout.

## Passaggio 4: salva il file PDF

```java
objImage.save(outFile, options);
```

Salva il file PDF esportato.

Ripeti questi passaggi per eventuali file DGN aggiuntivi che desideri convertire. Congratulazioni! Hai esportato con successo file DGN in formato AutoCAD in PDF utilizzando Aspose.CAD per Java.

## Conclusione

In questo tutorial, abbiamo esplorato come sfruttare Aspose.CAD per Java per migliorare le capacità di gestione dei file CAD della tua applicazione. Con passaggi facili da seguire ed esempi di codice, ora puoi esportare facilmente file DGN in formato AutoCAD in PDF.

## Domande frequenti

### Q1: Aspose.CAD è compatibile con tutti i formati di file CAD?

A1: Sì, Aspose.CAD supporta un'ampia gamma di formati CAD, garantendo versatilità nella gestione di vari tipi di file.

### Q2: Posso personalizzare le impostazioni di esportazione PDF?

A2: Assolutamente. Come mostrato nel tutorial, puoi regolare opzioni come dimensioni della pagina e layout in base alle tue esigenze.

### Q3: Dove posso trovare ulteriore supporto o assistenza?

 A3: Visita il[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) per il supporto e le discussioni della comunità.

### Q4: È disponibile una prova gratuita?

 R4: Sì, puoi accedere alla prova gratuita[Qui](https://releases.aspose.com/).

### Q5: Come posso ottenere una licenza temporanea?

 A5: ottieni una licenza temporanea[Qui](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
