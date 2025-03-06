---
title: Esporta oggetti OLE da CAD utilizzando Aspose.CAD per Java
linktitle: Esporta oggetti OLE da CAD
second_title: API Java Aspose.CAD
description: Sblocca il potenziale di Aspose.CAD per Java. Esporta facilmente oggetti OLE da file CAD. Scaricalo ora per una gestione semplificata dei dati CAD.
weight: 10
url: /it/java/cad-to-pdf-and-svg-export-options/export-ole-objects-from-cad/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Esporta oggetti OLE da CAD utilizzando Aspose.CAD per Java

## introduzione

Nel dinamico mondo della progettazione assistita da computer (CAD), gestire ed estrarre oggetti OLE (Object Linking and Embedding) in modo efficiente è fondamentale. Aspose.CAD per Java fornisce una potente soluzione per esportare oggetti OLE da file CAD. Questa guida passo passo ti guiderà attraverso il processo, assicurandoti di sfruttare tutto il potenziale di questo strumento.

## Prerequisiti

Prima di immergerti nel tutorial, assicurati di avere i seguenti prerequisiti:

- Ambiente Java: assicurati di avere un ambiente di sviluppo Java configurato sul tuo computer.
-  Aspose.CAD per Java: scarica e installa la libreria Aspose.CAD per Java. Puoi trovare la biblioteca presso il[Link per scaricare](https://releases.aspose.com/cad/java/).
- File CAD: prepara i file CAD contenenti oggetti OLE che desideri esportare.

## Importa spazi dei nomi

Per iniziare, importa gli spazi dei nomi necessari nel tuo progetto Java. Questi spazi dei nomi forniscono le classi e le funzionalità essenziali richieste per lavorare con file CAD utilizzando Aspose.CAD.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Ora suddividiamo il processo di esportazione di oggetti OLE da CAD in più passaggi:

## Passaggio 1: imposta la directory dei documenti

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

Assicurati di sostituire "La tua directory dei documenti" con il percorso della directory contenente i tuoi file CAD.

## Passaggio 2: definire i nomi dei file CAD

```java
String[] files = new String[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

 Specificare i nomi dei file CAD che si desidera elaborare nel file`files` vettore.

## Passaggio 3: imposta le opzioni di esportazione PNG

```java
PngOptions pngOptions = new PngOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.setLayouts(new String[] { "Layout1" });
```

Configura le opzioni di esportazione PNG, incluse la rasterizzazione vettoriale e le impostazioni di layout.

## Passaggio 4: scorrere i file CAD

```java
for(String file : files)
{
    CadImage cadImage = (CadImage)Image.load(dataDir + file);
    cadImage.save(dataDir + file + "_out.png", pngOptions);
}
```

Scorrere ogni file CAD specificato, caricarlo utilizzando Aspose.CAD e salvare gli oggetti OLE come immagini PNG.

## Conclusione

Con questi passaggi semplici ma potenti, puoi esportare senza problemi oggetti OLE da file CAD utilizzando Aspose.CAD per Java. Questo strumento versatile consente agli sviluppatori di gestire i dati CAD in modo efficiente, aprendo nuove possibilità nello sviluppo di applicazioni CAD.

## Domande frequenti

### Q1: Aspose.CAD è compatibile con tutti i formati di file CAD?

 A1: Aspose.CAD supporta vari formati CAD, inclusi DWG, DXF e DGN. Fare riferimento al[documentazione](https://reference.aspose.com/cad/java/) per l'elenco completo.

### Q2: posso personalizzare le impostazioni di esportazione per gli oggetti OLE?

A2: Sì, Aspose.CAD offre ampie opzioni per personalizzare le impostazioni di esportazione, consentendo di adattare l'output alle proprie esigenze specifiche.

### Q3: È disponibile una prova gratuita per Aspose.CAD?

 A3: Sì, puoi esplorare le funzionalità di Aspose.CAD ottenendo una prova gratuita da[Qui](https://releases.aspose.com/).

### Q4: Dove posso ottenere il supporto della community per Aspose.CAD?

 A4: Unisciti alla comunità Aspose.CAD su[Forum](https://forum.aspose.com/c/cad/19) per chiedere assistenza e condividere le tue esperienze.

### Q5: Come posso acquistare una licenza per Aspose.CAD?

A5: Visita il[pagina di acquisto](https://purchase.aspose.com/buy) per acquisire una licenza adatta alle tue esigenze di sviluppo.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
