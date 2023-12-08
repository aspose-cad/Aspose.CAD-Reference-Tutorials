---
title: Esporta STL in PNG con Aspose.CAD per Java
linktitle: Esporta STL in PNG
second_title: API Java Aspose.CAD
description: Esplora il processo senza interruzioni di esportazione di file STL in PNG in Java con Aspose.CAD. Semplifica il tuo flusso di lavoro e migliora i tuoi progetti Java senza sforzo.
type: docs
weight: 20
url: /it/java/cad-export-options/export-stl-to-png/
---
## introduzione

Stai cercando di esportare file STL in PNG utilizzando Java? Aspose.CAD per Java è la soluzione di cui hai bisogno! In questo tutorial ti guideremo attraverso il processo passo dopo passo. In qualità di abile scrittore SEO, mi assicurerò che il contenuto non sia solo informativo ma anche ottimizzato per i motori di ricerca.

## Prerequisiti

Prima di immergerti nel tutorial, assicurati di avere i seguenti prerequisiti:

- Java Development Kit (JDK) installato sul tuo computer.
-  Aspose.CAD per la libreria Java scaricata. Puoi prenderlo[Qui](https://releases.aspose.com/cad/java/).
-  Una licenza valida o una licenza temporanea da[Qui](https://purchase.aspose.com/temporary-license/).

## Importa spazi dei nomi

Nel tuo progetto Java, importa gli spazi dei nomi necessari:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Ora suddividiamo l'esempio in più passaggi.

## Passaggio 1: imposta il tuo progetto

Crea un nuovo progetto Java e aggiungi la libreria Aspose.CAD per Java alle dipendenze del tuo progetto.

## Passaggio 2: specifica il file STL

Definisci il percorso del tuo file STL. Per esempio:

```java
String dataDir = "Your Document Directory" + "ExportingSTL/";
String fileName = dataDir + "example.stl";
```

## Passaggio 3: caricare il file STL

 Caricare il file STL utilizzando il file`Image.load` metodo:

```java
CadImage cadImage = (CadImage)Image.load(fileName);
```

## Passaggio 4: configurare le opzioni di rasterizzazione

Configura le opzioni di rasterizzazione per la vettorizzazione:

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

## Passaggio 5: configura le opzioni PNG

Specifica le opzioni per l'esportazione PNG:

```java
PngOptions pngOptions = new PngOptions();
// Decommenta la riga seguente se desideri impostare le opzioni di rasterizzazione vettoriale
// pngOptions.setVectorRasterizationOptions(vettoreOpzioni);
```

## Passaggio 6: salva come PNG

Salva l'immagine CAD come file PNG:

```java
String outPath = dataDir + "galeon.stl.png";
cadImage.save(outPath, pngOptions);
```

Congratulazioni! Hai esportato con successo un file STL in PNG utilizzando Aspose.CAD per Java.

## Conclusione

In questo tutorial, abbiamo esplorato come sfruttare Aspose.CAD per Java per esportare file STL in PNG senza sforzo. Questa potente libreria semplifica le attività complesse, rendendola una risorsa preziosa per i tuoi progetti Java.

## Domande frequenti

### Q1: Aspose.CAD per Java è compatibile con tutte le versioni di file STL?

A1: Aspose.CAD per Java supporta varie versioni di file STL, garantendo la compatibilità con i formati più comuni.

### Q2: Posso utilizzare Aspose.CAD per Java in un progetto commerciale?

 A2: Sì, puoi. Basta ottenere una licenza valida da[Qui](https://purchase.aspose.com/buy).

### Q3: Ho bisogno di una licenza temporanea per la prova gratuita?

 R3: No, per la prova gratuita non è necessaria una licenza temporanea. Puoi iniziare subito con la versione di prova[Qui](https://releases.aspose.com/).

### Q4: Dove posso trovare ulteriore supporto o porre domande?

 A4: visitare il forum Aspose.CAD[Qui](https://forum.aspose.com/c/cad/19) per qualsiasi supporto o domanda.

### Q5: È disponibile documentazione completa?

 R5: Sì, è possibile trovare la documentazione[Qui](https://reference.aspose.com/cad/java/).