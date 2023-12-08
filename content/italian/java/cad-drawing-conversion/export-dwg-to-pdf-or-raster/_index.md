---
title: Esporta DWG in PDF o Raster utilizzando Aspose.CAD per Java
linktitle: Esporta DWG in PDF o Raster
second_title: API Java Aspose.CAD
description: Esplora il processo continuo di esportazione di file DWG in PDF o immagini raster in Java utilizzando Aspose.CAD. Questa guida passo passo garantisce precisione ed efficienza.
type: docs
weight: 13
url: /it/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
---
## introduzione

Nel mondo dinamico della progettazione assistita da computer (CAD), la gestione efficiente dei disegni è fondamentale. Aspose.CAD per Java fornisce una potente soluzione per esportare file DWG in PDF o immagini raster. Questo tutorial ti guiderà attraverso il processo, assicurandoti di sfruttare tutto il potenziale di Aspose.CAD per Java.

## Prerequisiti

Prima di immergerti nel tutorial, assicurati di avere quanto segue:

- Conoscenza di base della programmazione Java.
-  Aspose.CAD per la libreria Java installata. In caso contrario, scaricalo[Qui](https://releases.aspose.com/cad/java/).
- Un file DWG a scopo di test. È possibile utilizzare il file "Bottom_plate.dwg" fornito.

## Importa spazi dei nomi

Nel tuo progetto Java, importa gli spazi dei nomi necessari per avviare il processo:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## Passaggio 1: caricare il file DWG

 Inizia caricando il tuo file DWG utilizzando Aspose.CAD`Image` classe:

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

## Passaggio 2: determinare il tipo di unità

Successivamente, controlla il tipo di unità del file DWG caricato:

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

## Passaggio 3: imposta le opzioni di rasterizzazione

In base al tipo di unità, configurare le opzioni di rasterizzazione:

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();

if (currentUnitIsMetric) {
    // Unità metrica
    double metersCoeff = 1 / 1000.0;
    double scaleFactor = metersCoeff / currentUnitCoefficient;
    rasterizationOptions.setPageWidth((float)(210 * scaleFactor));
    rasterizationOptions.setPageHeight((float)(297 * scaleFactor));
    rasterizationOptions.setUnitType(UnitType.Millimeter);
} else {
    // unità imperiali
    rasterizationOptions.setPageWidth((float)(8.27f / currentUnitCoefficient));
    rasterizationOptions.setPageHeight((float)(11.69f / currentUnitCoefficient));
    rasterizationOptions.setUnitType(UnitType.Inch);
}
```

## Passaggio 4: configura le opzioni PDF

Configura le opzioni di esportazione PDF:

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

## Passaggio 5: salva come PDF

Infine, salva il file DWG come PDF:

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

E il gioco è fatto! Hai esportato con successo un file DWG in PDF utilizzando Aspose.CAD per Java.

## Conclusione

Questo tutorial ha fornito una guida passo passo su come sfruttare Aspose.CAD per Java per esportare file DWG in PDF o immagini raster. Questa libreria semplifica il processo, consentendoti di gestire in modo efficiente i disegni CAD nelle tue applicazioni Java.

## Domande frequenti

### Q1: posso utilizzare Aspose.CAD per Java con altri framework Java?

A1: Sì, Aspose.CAD per Java si integra perfettamente con i più diffusi framework Java.

### Q2: È disponibile una licenza temporanea per Aspose.CAD per Java?

 R2: Sì, puoi ottenere una licenza temporanea[Qui](https://purchase.aspose.com/temporary-license/).

### Q3: Dove posso trovare supporto per Aspose.CAD per Java?

 A3: Visita il[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) per l'aiuto della comunità.

### Q4: Come posso acquistare una licenza per Aspose.CAD per Java?

 A4: È possibile acquistare una licenza[Qui](https://purchase.aspose.com/buy).

### Q5: Quali unità supporta Aspose.CAD per Java?

A5: Aspose.CAD per Java supporta sia le unità metriche che quelle imperiali.