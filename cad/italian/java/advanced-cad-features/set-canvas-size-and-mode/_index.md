---
title: Imposta le dimensioni e la modalità della tela
linktitle: Imposta le dimensioni e la modalità della tela
second_title: API Java Aspose.CAD
description: Esplora la potenza di Aspose.CAD per Java con la nostra guida passo passo sull'impostazione delle dimensioni e della modalità della tela. Converti facilmente file CAD nei formati PDF e TIFF.
weight: 16
url: /it/java/advanced-cad-features/set-canvas-size-and-mode/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Imposta le dimensioni e la modalità della tela

## introduzione

Stai cercando di sfruttare la potenza di Aspose.CAD per Java per migliorare il tuo processo di conversione CAD? Questa guida completa ti guiderà attraverso i passaggi per impostare le dimensioni e la modalità della tela utilizzando Aspose.CAD per Java. Che tu sia uno sviluppatore esperto o che tu abbia appena iniziato, questo tutorial ti fornirà le informazioni di cui hai bisogno.

## Prerequisiti

Prima di immergerti nel tutorial, assicurati di avere i seguenti prerequisiti:

-  Aspose.CAD per Java: assicurati di avere la libreria Aspose.CAD installata nel tuo ambiente Java. Puoi scaricarlo[Qui](https://releases.aspose.com/cad/java/).

- Directory dei documenti: imposta una directory dei documenti per archiviare i file CAD. A questa directory verrà fatto riferimento nei passaggi del tutorial.

Ora iniziamo con la guida passo passo.

## Importa spazi dei nomi

In questo passaggio, importeremo gli spazi dei nomi necessari per avviare il tuo progetto Aspose.CAD.
```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## Passaggio 1: importare classi Aspose.CAD

```java
// Il percorso della directory delle risorse.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

 In questo frammento, impostiamo il percorso della directory delle risorse e carichiamo un file DXF utilizzando Aspose.CAD`Image` classe.

## Passaggio 2: impostare le proprietà CadRasterizationOptions

```java
// Crea un'istanza di CadRasterizationOptions e imposta le sue varie proprietà
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

 Qui creiamo un'istanza di`CadRasterizationOptions` e configurare proprietà come larghezza della pagina, altezza della pagina e opzioni di ridimensionamento.

## Passaggio 3: crea PdfOptions e imposta VectorRasterizationOptions

```java
// Crea un'istanza di PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Imposta la proprietà VectorRasterizationOptions
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

 Ora creiamo un file`PdfOptions` istanza e impostarla`VectorRasterizationOptions` proprietà a quella precedentemente configurata`CadRasterizationOptions`.

## Passaggio 4: esporta in PDF

```java
// Esporta CAD in PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

Infine, salviamo l'immagine CAD in un file PDF utilizzando le opzioni specificate.

## Passaggio 5: crea TiffOptions e imposta VectorRasterizationOptions

```java
// Crea un'istanza di TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Imposta la proprietà VectorRasterizationOptions
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

In questo passaggio, impostiamo a`TiffOptions` istanza e configurarla`VectorRasterizationOptions` proprietà.

## Passaggio 6: esporta in TIFF

```java
// Esporta CAD in TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

Infine, salviamo l'immagine CAD in un file TIFF utilizzando le opzioni specificate.

## Conclusione

 Congratulazioni! Hai impostato correttamente le dimensioni e la modalità della tela utilizzando Aspose.CAD per Java. Questo tutorial fornisce una solida base per i tuoi progetti di conversione CAD. Esplora ulteriori funzionalità e possibilità nel[Documentazione Aspose.CAD](https://reference.aspose.com/cad/java/).

## Domande frequenti

### Q1: posso utilizzare Aspose.CAD per Java con altri framework Java?

A1: Sì, Aspose.CAD è progettato per integrarsi perfettamente con vari framework Java.

### Q2: È disponibile una licenza temporanea per Aspose.CAD?

 R2: Sì, puoi ottenere una licenza temporanea[Qui](https://purchase.aspose.com/temporary-license/).

### Q3: Dove posso ottenere il supporto della community per Aspose.CAD?

 A3: Visita il[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) per il supporto e le discussioni della comunità.

### Q4: Posso provare Aspose.CAD gratuitamente?

 A4: Assolutamente! Ottieni una prova gratuita[Qui](https://releases.aspose.com/).

### Q5: Come posso acquistare Aspose.CAD per Java?

 A5: Acquista il prodotto[Qui](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
