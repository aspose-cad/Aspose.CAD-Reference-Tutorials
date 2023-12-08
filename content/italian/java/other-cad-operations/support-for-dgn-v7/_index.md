---
title: Guida alla conversione da DGN a PDF - Aspose.CAD per Java
linktitle: Supporto per DGN V7
second_title: API Java Aspose.CAD
description: Converti facilmente file DGN in PDF utilizzando Aspose.CAD per Java. Segui la nostra guida passo passo per un'integrazione perfetta e un flusso di lavoro efficiente.
type: docs
weight: 11
url: /it/java/other-cad-operations/support-for-dgn-v7/
---
## introduzione

Nel dinamico mondo del CAD (Computer-Aided Design), la conversione efficiente dei file DGN (Design) in PDF (Portable Document Format) è un requisito cruciale. Aspose.CAD per Java emerge come una soluzione potente, offrendo una perfetta integrazione e solide funzionalità. Questa guida passo passo ha lo scopo di guidarti attraverso il processo di esportazione di file DGN in PDF utilizzando Aspose.CAD per Java, garantendo un flusso di lavoro fluido ed efficiente.

## Prerequisiti

Prima di immergerti nel tutorial, assicurati di disporre dei seguenti prerequisiti:
-  Aspose.CAD per Java Library: scarica e installa la libreria da[Pagina di download di Aspose.CAD per Java](https://releases.aspose.com/cad/java/).
- Ambiente di sviluppo Java: assicurati di avere un ambiente di sviluppo Java configurato sul tuo computer.

## Importa pacchetti

Inizia importando i pacchetti necessari nel tuo progetto Java:

## Passaggio 1: importa i pacchetti necessari

Nel tuo progetto Java, importa i pacchetti richiesti per Aspose.CAD per Java.
```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.cadobjects.DgnImage;
import com.aspose.cad.imageoptions.PdfOptions;
import java.awt.Color;
```

## Passaggio 2: imposta i percorsi dei file

Definire i percorsi per il file DGN di input e il file PDF di output.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

## Passaggio 3: caricare l'immagine DGN

Carica l'immagine DGN utilizzando la libreria Aspose.CAD.

```java
DgnImage objImage = (DgnImage)Image.load(fileName);
```

## Passaggio 4: configura le opzioni di esportazione PDF

Configura le opzioni per l'esportazione in PDF, comprese le dimensioni della pagina, il ridimensionamento automatico del layout, il colore dello sfondo e layout specifici da esportare.

```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setBackgroundColor(Color.getBlack());
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); //esportare solo 4 (1,2,3 e 9) visualizzazioni
options.setVectorRasterizationOptions(vectorOptions);
```

## Passaggio 5: salva il file PDF

Salvare l'immagine DGN come file PDF con le opzioni specificate.

```java
objImage.save(outFile, options);
```

Ripetere questi passaggi per file DGN diversi, modificando i percorsi e le opzioni dei file secondo necessità.

## Conclusione

Con Aspose.CAD per Java, convertire i file DGN in PDF diventa un processo semplice. Questa guida ti fornisce le conoscenze per integrare perfettamente la libreria nei tuoi progetti Java, facilitando conversioni efficienti di file CAD.

## Domande frequenti

### Q1: Posso utilizzare Aspose.CAD per Java con altri formati di file CAD?

R1: Sì, Aspose.CAD supporta vari formati CAD, fornendo funzionalità versatili oltre la conversione da DGN a PDF.

### Q2: È disponibile una licenza temporanea per Aspose.CAD per Java?

 R2: Sì, puoi ottenere una licenza temporanea[Qui](https://purchase.aspose.com/temporary-license/) a scopo di test.

### Q3: Come posso chiedere supporto o porre domande su Aspose.CAD per Java?

 A3: Visita il[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19)connettersi con la comunità e cercare assistenza.

### D4: Quali layout posso esportare durante la conversione da DGN a PDF?

 R4: È possibile specificare i layout da esportare personalizzando il file`setLayouts` matrice nel codice.

### Q5: Dove posso trovare la documentazione completa per Aspose.CAD per Java?

 A5: Fare riferimento a[Aspose.CAD per la documentazione Java](https://reference.aspose.com/cad/java/) per informazioni dettagliate.