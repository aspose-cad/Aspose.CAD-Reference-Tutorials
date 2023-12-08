---
title: Esporta IFC in PNG con Aspose.CAD per Java
linktitle: Esporta IFC in PNG
second_title: API Java Aspose.CAD
description: Converti IFC in PNG senza sforzo con Aspose.CAD per Java. Segui il nostro tutorial passo dopo passo.
type: docs
weight: 18
url: /it/java/cad-export-options/export-ifc-to-png/
---
## introduzione

Benvenuti in questo tutorial passo passo sull'esportazione di IFC (Industry Foundation Classes) in PNG utilizzando Aspose.CAD per Java. Aspose.CAD è una potente libreria Java che fornisce ampie funzionalità per lavorare con file CAD, incluso il formato IFC. In questo tutorial ti guideremo attraverso il processo di conversione di un file IFC in un'immagine PNG con spiegazioni dettagliate su ogni passaggio.

## Prerequisiti

Prima di iniziare, assicurati di disporre dei seguenti prerequisiti:

-  Libreria Aspose.CAD: scarica e installa la libreria Aspose.CAD per Java da[Link per scaricare](https://releases.aspose.com/cad/java/).

- Directory dei documenti: prepara una directory sul tuo sistema in cui si trova il tuo file IFC.

## Importa spazi dei nomi

Nel tuo progetto Java, importa gli spazi dei nomi necessari come mostrato di seguito:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## Passaggio 1: caricare il file IFC

```java
String dataDir = "Your Document Directory" + "ExportingIFC/";
String fileName = dataDir + "example.ifc";
IfcImage cadImage = (IfcImage)Image.load(fileName);
```

Questo passaggio prevede il caricamento del file IFC utilizzando Aspose.CAD.

## Passaggio 2: imposta le opzioni del vettore

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

Configura le opzioni vettoriali per la rasterizzazione, specificando la larghezza e l'altezza della pagina.

## Passaggio 3: imposta le opzioni PNG

```java
PngOptions pngOptions = new PngOptions();
pngOptions.setVectorRasterizationOptions(vectorOptions);
```

Imposta le opzioni PNG, incluse le opzioni di rasterizzazione vettoriale.

## Passaggio 4: salva come PNG

```java
String outPath = dataDir + "example.png";
cadImage.save(outPath, pngOptions);
```

Salva l'immagine elaborata in formato PNG.

## Conclusione

Congratulazioni! Hai convertito con successo un file IFC in PNG utilizzando Aspose.CAD per Java. Questo tutorial ha fornito una guida completa, assicurandoti di poter integrare perfettamente questa funzionalità nei tuoi progetti.

## Domande frequenti

### Q1: Aspose.CAD è compatibile con tutte le versioni dei file IFC?

 A1: Aspose.CAD supporta varie versioni di file IFC. Fare riferimento al[documentazione](https://reference.aspose.com/cad/java/) per i dettagli sulla compatibilità.

### Q2: Posso personalizzare ulteriormente le opzioni di rasterizzazione?

 A2: Assolutamente! Esplorare la[documentazione](https://reference.aspose.com/cad/java/) per opzioni di personalizzazione avanzate.

### Q3: È disponibile una versione di prova?

R3: Sì, puoi accedere alla versione di prova gratuita[Qui](https://releases.aspose.com/).

### Q4: Come posso ottenere una licenza temporanea per Aspose.CAD?

 A4: Ottieni una licenza temporanea da[questo link](https://purchase.aspose.com/temporary-license/).

### Q5: Dove posso chiedere aiuto o discutere i problemi?

A5: Visita il[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) per il sostegno della comunità.
