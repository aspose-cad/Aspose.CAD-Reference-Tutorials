---
title: Timeout su salvataggio per CAD con Aspose.CAD
linktitle: Metti Timeout su Salva
second_title: API Java Aspose.CAD
description: Scopri come migliorare le prestazioni della tua applicazione Java con Aspose.CAD. Imposta un timeout per il salvataggio dei disegni CAD. Segui la nostra guida passo passo.
weight: 15
url: /it/java/other-cad-operations/put-timeout-on-save/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Timeout su salvataggio per CAD con Aspose.CAD

## introduzione

Benvenuti nel tutorial su come impostare un timeout durante il salvataggio utilizzando Aspose.CAD per Java. In questa guida ti guideremo attraverso il processo di impostazione di un timeout per il salvataggio dei disegni CAD per migliorare le prestazioni della tua applicazione. Aspose.CAD per Java è una potente libreria che ti consente di lavorare senza problemi con i file CAD nelle tue applicazioni Java.

## Prerequisiti

Prima di immergerti nel tutorial, assicurati di avere i seguenti prerequisiti:
-  Libreria Aspose.CAD per Java: assicurati di avere la libreria Aspose.CAD per Java integrata nel tuo progetto. È possibile scaricare la libreria da[sito web](https://releases.aspose.com/cad/java/).
- Ambiente di sviluppo: configura il tuo ambiente di sviluppo Java con tutti gli strumenti e le dipendenze necessari.

## Importa pacchetti

Per iniziare, importa i pacchetti richiesti nel tuo progetto Java. Aggiungi le seguenti righe all'inizio del tuo file Java:

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterruptionTokenSource;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.concurrent.TimeUnit;
```

Ora suddividiamo il codice di esempio in istruzioni passo passo:

## Passaggio 1: imposta le directory di origine e di output

```java
final String SourceDir = Utils.getDataDir_DWGDrawings();
final String OutputDir = Utils.getDataDir_Output();
```

Assicurati di disporre delle directory di origine e di output corrette per i tuoi disegni CAD.

## Passaggio 2: crea la sorgente del token di interruzione

```java
final InterruptionTokenSource source = new com.aspose.cad.InterruptionTokenSource();
```

Inizializza un'origine token di interruzione per gestire le interruzioni durante l'operazione di salvataggio.

## Passaggio 3: caricare il disegno CAD

```java
final CadImage cadImageBig = (CadImage)Image.load(SourceDir + "Drawing11.dwg");
```

 Caricare il disegno CAD in a`CadImage` oggetto.

## Passaggio 4: configurare le opzioni di rasterizzazione

```java
CadRasterizationOptions rasterizationOptionsBig = new CadRasterizationOptions();
rasterizationOptionsBig.setPageWidth(cadImageBig.getSize().getWidth() / 2);
rasterizationOptionsBig.setPageHeight(cadImageBig.getSize().getHeight() / 2);
```

Configura le opzioni di rasterizzazione per il disegno CAD.

## Passaggio 5: configura le opzioni PDF

```java
final PdfOptions CADfBig = new PdfOptions();
CADfBig.setVectorRasterizationOptions(rasterizationOptionsBig);
CADfBig.setInterruptionToken(source.getToken());
```

Configura le opzioni PDF con le opzioni di rasterizzazione vettoriale e il token di interruzione.

## Passaggio 6: salva il disegno con timeout

```java
cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
```

Salva il disegno CAD in un file PDF con il timeout specificato.

## Passaggio 7: gestire l'interruzione

```java
java.lang.Thread thread = new java.lang.Thread(new Runnable() {
    @Override
    public void run() {
        try {
            cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
        } catch (Throwable th) {
            System.out.println("interrupted !!!");
        }
    }
});
thread.start();
TimeUnit.SECONDS.sleep(3);
source.interrupt();
thread.join();
```

Crea un thread per gestire l'operazione di salvataggio e interromperla dopo un timeout specificato.

## Conclusione

Congratulazioni! Hai imparato con successo come inserire un timeout durante il salvataggio utilizzando Aspose.CAD per Java. Questa funzionalità può migliorare notevolmente l'efficienza delle applicazioni relative al CAD.

## Domande frequenti

### Q1: Come posso scaricare Aspose.CAD per Java?

 A1: Puoi scaricarlo da[pagina delle uscite](https://releases.aspose.com/cad/java/).

### Q2: Dove posso trovare la documentazione per Aspose.CAD per Java?

 A2: Fare riferimento a[documentazione](https://reference.aspose.com/cad/java/) per informazioni complete.

### Q3: È disponibile una prova gratuita?

R3: Sì, puoi ottenere una prova gratuita da[questo link](https://releases.aspose.com/).

### Q4: Come posso ottenere una licenza temporanea?

 A4: Visita[Qui](https://purchase.aspose.com/temporary-license/) per i dettagli della licenza temporanea.

### Q5: Hai bisogno di aiuto o hai domande?

 A5: Vai al[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) per il sostegno della comunità.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
