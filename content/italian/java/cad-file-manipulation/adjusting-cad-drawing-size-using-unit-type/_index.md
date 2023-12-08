---
title: Regolazione delle dimensioni del disegno CAD utilizzando il tipo di unità con Aspose.CAD per Java
linktitle: Regolazione delle dimensioni del disegno CAD utilizzando il tipo di unità
second_title: API Java Aspose.CAD
description: Esplora la potenza di Aspose.CAD per Java nella regolazione delle dimensioni dei disegni CAD senza sforzo. Segui la nostra guida passo passo per precisione e adattabilità.
type: docs
weight: 14
url: /it/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/
---
## introduzione

Nel campo in continua evoluzione della progettazione assistita da computer (CAD), precisione e adattabilità sono fondamentali. Un requisito comune è la regolazione delle dimensioni dei disegni CAD in base a tipi di unità specifici. Aspose.CAD per Java emerge come un potente alleato, fornendo funzionalità continue per manipolare i file CAD a livello di programmazione.

## Prerequisiti

Prima di immergerti nel tutorial, assicurati di avere i seguenti prerequisiti:

- Ambiente di sviluppo Java: assicurati di avere un ambiente di sviluppo Java funzionale configurato sul tuo computer.

-  Aspose.CAD per libreria Java: scarica e integra la libreria Aspose.CAD nel tuo progetto Java. È possibile ottenere la libreria[Qui](https://releases.aspose.com/cad/java/).

## Importa spazi dei nomi

Nel tuo codice Java, includi gli spazi dei nomi necessari per accedere alle funzionalità Aspose.CAD. Aggiungi le seguenti importazioni:

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Ora suddividiamo il processo di regolazione delle dimensioni del disegno CAD utilizzando il tipo di unità in passaggi gestibili:

## Passaggio 1: definire la directory dei dati

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

Imposta il percorso della directory in cui si trovano i file CAD.

## Passaggio 2: caricare il disegno CAD

```java
String sourceFilePath = dataDir + "sample.dwg";
Image image = Image.load(sourceFilePath);
```

 Caricare il disegno CAD utilizzando Aspose.CAD`Image` classe.

## Passaggio 3: crea opzioni BMP

```java
BmpOptions bmpOptions = new BmpOptions();
```

 Istanziare il`BmpOptions` classe per esportare il layout CAD in formato BMP.

## Passaggio 4: configurare le opzioni di rasterizzazione

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

 Crea un'istanza di`CadRasterizationOptions` e associarlo a`BmpOptions` per la rasterizzazione vettoriale.

## Passaggio 5: impostare il tipo di unità

```java
cadRasterizationOptions.setUnitType(UnitType.Centimeter);
```

Specificare il tipo di unità desiderato per il disegno CAD. In questo esempio, lo abbiamo impostato su Centimetro.

## Passaggio 6: imposta i layout

```java
cadRasterizationOptions.setLayouts(new String[] { "Model" });
```

Definire i layout da considerare durante l'esportazione. In questo caso, abbiamo selezionato il layout "Modello".

## Passaggio 7: esporta in BMP

```java
String outPath = sourceFilePath + ".bmp";
image.save(outPath, bmpOptions);
```

Infine, salva il disegno CAD modificato in formato BMP.

## Conclusione

Con Aspose.CAD per Java, la regolazione delle dimensioni del disegno CAD diventa un gioco da ragazzi. Questo tutorial ti ha guidato attraverso il processo, sottolineando l'importanza di ogni passaggio per ottenere risultati precisi.

## Domande frequenti

### Q1: posso utilizzare Aspose.CAD per Java con altri linguaggi di programmazione?

A1: Aspose.CAD supporta principalmente Java, ma sono disponibili versioni per altri linguaggi come .NET.

### Q2: Esistono opzioni di licenza per Aspose.CAD?

 A2: Sì, puoi esplorare le opzioni di licenza e acquistare Aspose.CAD[Qui](https://purchase.aspose.com/buy).

### Q3: È disponibile una prova gratuita per Aspose.CAD?

 R3: Certamente puoi accedere a una prova gratuita[Qui](https://releases.aspose.com/).

### Q4: Come posso ottenere supporto per Aspose.CAD per Java?

 A4: visitare il forum Aspose.CAD[Qui](https://forum.aspose.com/c/cad/19) per un supporto completo.

### Q5: Posso ottenere una licenza temporanea per Aspose.CAD?

 R5: Sì, puoi acquisire una licenza temporanea[Qui](https://purchase.aspose.com/temporary-license/).