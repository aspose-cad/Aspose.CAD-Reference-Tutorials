---
title: Esporta in PDF con Aspose.CAD per Java
linktitle: Esporta in PDF
second_title: API Java Aspose.CAD
description: Scopri come esportare file CAD in PDF senza sforzo con Aspose.CAD per Java. Segui la nostra guida passo passo per un'integrazione perfetta.
weight: 13
url: /it/java/cad-export-options/export-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Esporta in PDF con Aspose.CAD per Java

## introduzione

Benvenuti in questo tutorial completo sull'esportazione di file CAD in PDF utilizzando Aspose.CAD per Java. Se stai cercando di convertire senza problemi i tuoi disegni CAD nel formato PDF ampiamente supportato, sei nel posto giusto. In questa guida passo passo, analizzeremo il processo, assicurandoti di comprendere ogni passaggio per ottenere un'esportazione PDF di successo.

## Prerequisiti

Prima di immergerti nel tutorial, assicurati di avere i seguenti prerequisiti:

-  Aspose.CAD per Java: assicurati di avere la libreria Aspose.CAD installata nel tuo ambiente Java. Puoi scaricarlo[Qui](https://releases.aspose.com/cad/java/).

- Directory delle risorse: imposta una directory in cui sono archiviati i file CAD. Sostituisci "La tua directory dei documenti" nello snippet di codice fornito con il percorso effettivo.

Adesso passiamo ai passaggi principali.

## Importa spazi dei nomi

Nel tuo progetto Java, inizia importando gli spazi dei nomi necessari per abilitare l'uso delle funzionalità Aspose.CAD.

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

Carica il tuo file CAD nell'oggetto Immagine Aspose.CAD. Sostituisci "site.dwf" con il nome effettivo del file CAD.

```java
String fileName = (dataDir + "site.dwf");
Image image = Image.load(fileName);
```

## Passaggio 2: configura le opzioni PDF

Configura le opzioni di esportazione PDF, comprese le opzioni di rasterizzazione vettoriale come altezza, larghezza e layout della pagina.

```java
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);

rasterizationOptions.setPageHeight(500);
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setLayouts(new String[] { "Model" });
```

## Passaggio 3: esporta in PDF

Specificare il percorso di output per il file PDF generato e salvare l'immagine con le opzioni PDF configurate.

```java
String outPath = dataDir + "site.pdf";
image.save(outPath, pdfOptions);
```

Congratulazioni! Hai esportato con successo il tuo file CAD in un PDF utilizzando Aspose.CAD per Java.

## Conclusione

In questo tutorial, abbiamo esplorato il processo passo passo di esportazione di file CAD in PDF utilizzando Aspose.CAD per Java. Seguendo questi passaggi semplici ma efficaci, puoi integrare perfettamente questa funzionalità nelle tue applicazioni Java.

## Domande frequenti

### Q1: Aspose.CAD è compatibile con tutti i formati di file CAD?

A1: Sì, Aspose.CAD supporta un'ampia gamma di formati CAD, garantendo la compatibilità con vari software di progettazione.

### Q2: Posso personalizzare le impostazioni di output del PDF?

A2: Assolutamente. Il tutorial fornisce un'anteprima delle opzioni di personalizzazione, ma puoi esplorare ulteriormente per personalizzare l'output in base alle tue esigenze.

### Q3: Dove posso trovare ulteriore supporto per Aspose.CAD?

 R3: Per qualsiasi domanda o problema, visitare il[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) chiedere aiuto alla comunità.

### Q4: È disponibile una prova gratuita?

 A4: Sì, puoi accedere a una prova gratuita di Aspose.CAD[Qui](https://releases.aspose.com/).

### Q5: Come posso ottenere una licenza temporanea per Aspose.CAD?

 R5: Per la licenza temporanea, visitare[questo link](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
