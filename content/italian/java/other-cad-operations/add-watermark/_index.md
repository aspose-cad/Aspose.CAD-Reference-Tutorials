---
title: Aggiungi filigrane ai disegni CAD - Aspose.CAD per Java Tutorial
linktitle: Aggiungi filigrana
second_title: API Java Aspose.CAD
description: Migliora i tuoi disegni CAD con filigrane personalizzate utilizzando Aspose.CAD per Java. Segui la nostra guida passo passo per un'integrazione perfetta.
type: docs
weight: 12
url: /it/java/other-cad-operations/add-watermark/
---
## introduzione

Benvenuti in questa guida completa sull'aggiunta di filigrane ai disegni CAD utilizzando Aspose.CAD per Java. In questo tutorial imparerai come integrare le filigrane in modo efficiente, migliorando i tuoi documenti CAD con messaggi o marchi personalizzati. Aspose.CAD per Java fornisce un potente set di funzionalità, rendendo semplice il processo di aggiunta della filigrana.

## Prerequisiti

Prima di immergerci nel tutorial, assicurati di possedere i seguenti prerequisiti:

-  Aspose.CAD per Java: assicurati di avere la libreria Aspose.CAD installata nel tuo ambiente Java. Puoi scaricarlo[Qui](https://releases.aspose.com/cad/java/).
- Java Development Kit (JDK): assicurati di avere la versione più recente di JDK installata sul tuo sistema.

## Importa pacchetti

Nel tuo progetto Java, importa i pacchetti Aspose.CAD necessari per iniziare:

```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.Cad3DPoint;
import com.aspose.cad.fileformats.cad.cadobjects.CadMText;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Passaggio 1: aggiungi nuovo TESTOM

```java
//aggiungi nuovo TESTOM
CadMText watermark = new CadMText();
watermark.setText("Watermark message");
watermark.setInitialTextHeight(40);
watermark.setInsertionPoint(new Cad3DPoint(300, 40));
watermark.setLayerName("0");
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(watermark);
```

## Passaggio 2: aggiungi un'entità semplice come il testo

Puoi anche aggiungere un'entità più semplice come il testo:

```java
// o aggiungi entità più semplici come Testo
CadText text = new CadText();
text.setDefaultValue("Watermark text");
text.setTextHeight(40);
text.setFirstAlignment(new Cad3DPoint(300, 40));
text.setLayerName("0") ;
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(text);
```

## Passaggio 3: esporta in PDF

Esporta il disegno CAD con la filigrana aggiunta in un file PDF:

```java
// esportare in pdf
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setLayouts(new String[]{"Model"});
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
cadImage.save(dataDir + "AddWatermark_out.pdf", pdfOptions);

```

## Conclusione

Congratulazioni! Hai aggiunto con successo filigrane ai tuoi disegni CAD utilizzando Aspose.CAD per Java. Questo processo semplice ma potente ti consente di personalizzare i tuoi progetti o proteggerli con il marchio.

## Domande frequenti

### Q1: Aspose.CAD è compatibile con tutti i formati di file CAD?

A1: Aspose.CAD supporta vari formati CAD, inclusi DWG, DXF, DWT e DWF.

### Q2: Posso personalizzare l'aspetto del testo della filigrana?

R2: Sì, hai il pieno controllo sull'aspetto della filigrana, comprese le dimensioni, il colore e la posizione del testo.

### Q3: È disponibile una versione di prova per Aspose.CAD per Java?

 R3: Sì, puoi scaricare la versione di prova[Qui](https://releases.aspose.com/).

### Q4: Come posso ottenere supporto per Aspose.CAD?

 A4: Visita il[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) per il sostegno della comunità.

### Q5: Dove posso trovare la documentazione completa per Aspose.CAD per Java?

 A5: Fare riferimento a[documentazione](https://reference.aspose.com/cad/java/) per informazioni dettagliate.