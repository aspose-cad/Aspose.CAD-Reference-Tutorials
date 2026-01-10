---
date: 2026-01-10
description: Scopri come esportare DGN in DWG e convertire MicroStation DGN in AutoCAD
  DWG usando Aspose.CAD per Java. Guida passo‑passo.
linktitle: Export DGN as Part of DWG
second_title: Aspose.CAD Java API
title: Esporta DGN in DWG con Aspose.CAD per Java
url: /it/java/dgn-export-options/export-dgn-as-part-of-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Esporta DGN in DWG con Aspose.CAD per Java

## Introduzione

In questo tutorial imparerai a **esportare dgn in dwg** e a incorporare un progetto MicroStation DGN all'interno di un file AutoCAD DWG utilizzando la libreria Aspose.CAD per Java. Che tu stia migrando disegni legacy di MicroStation o abbia bisogno di combinare sottofondi DGN con layout DWG, questa guida ti accompagna passo dopo passo — dall'impostazione dell'ambiente alla generazione di un'anteprima PDF del DWG finale.

## Risposte Rapide
- **Cosa ottieni con “export dgn to dwg”?** Inserisce un sottofondo DGN in un DWG, consentendo una visualizzazione fluida in AutoCAD.
- **In quale formato posso esportare il risultato per un'anteprima veloce?** Puoi **esportare il file CAD in pdf** usando `PdfOptions`.
- **È necessaria una licenza per eseguire il codice?** È richiesta una licenza temporanea o a pagamento di Aspose.CAD per l'uso in produzione.
- **Quale versione di Java è supportata?** Java 8 o successive funzionano con l'ultima versione di Aspose.CAD per Java.
- **È disponibile una versione di prova gratuita?** Sì — scarica una trial dal sito Aspose.

## Cos'è “export dgn to dwg”?
Esportare DGN in DWG significa convertire o incorporare un progetto MicroStation DGN come sottofondo all'interno di un disegno AutoCAD DWG. Questo permette ai professionisti CAD di sfruttare le risorse DGN esistenti senza dover ricreare la geometria da zero.

## Perché convertire MicroStation DGN in AutoCAD DWG?
- **Collaborazione:** I team che usano AutoCAD possono visualizzare e modificare direttamente i contenuti DGN.
- **Standardizzazione:** DWG è il formato de‑facto per molti flussi di lavoro successivi (ad es., generazione di PDF, rendering 3D).
- **Conservazione:** Mantiene intatti i riferimenti DGN originali, riducendo la perdita di dati.

## Prerequisiti

Prima di immergerti nel tutorial, assicurati di avere i seguenti prerequisiti:
1. **Libreria Aspose.CAD:** Scarica e installa la libreria Aspose.CAD per Java. Puoi trovare la libreria [qui](https://releases.aspose.com/cad/java/).
2. **Java Development Kit (JDK):** Verifica di avere Java installato sul tuo sistema.
3. **Integrated Development Environment (IDE):** Scegli un IDE Java come Eclipse o IntelliJ per un'esperienza di sviluppo più fluida.

## Importa Pacchetti

Nel tuo progetto Java, importa i pacchetti Aspose.CAD necessari per abilitare la manipolazione dei file CAD. Ecco un esempio:

```java
import com.aspose.cad;
import com.aspose.cad.imageoptions;
import com.aspose.cad.fileformats.cad.cadconsts;
import com.aspose.cad.fileformats.cad;
import com.aspose.cad.fileformats.cad.cadobjects;
```

## Passo 1: Imposta i Percorsi dei File

Definisci i percorsi di input e output per il file DWG. Aggiorna le variabili `dataDir`, `fileName` e `outPath` di conseguenza.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
String outPath = dataDir + "BlockRefDgn.dwg.pdf";
```

## Passo 2: Crea un'Istanza di PdfOptions

Crea un'istanza della classe `PdfOptions`, poiché **esporteremo il file CAD in PDF** per una verifica rapida.

```java
PdfOptions exportOptions = new PdfOptions();
```

## Passo 3: Carica il File DWG

Carica il file DWG esistente come immagine e convertilo al tipo `CadImage`.

```java
CadImage cadImage = (CadImage) Image.load(fileName);
```

## Passo 4: Itera Attraverso le Entità

Scorri ogni entità all'interno del file DWG e verifica se è una definizione di immagine. In tal caso, recupera il riferimento esterno all'oggetto.

```java
for (CadBaseEntity baseEntity : cadImage.getEntities()) {
    if (baseEntity.getTypeName() == CadEntityTypeName.DGNUNDERLAY) {
        CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
        System.out.println(dgnFile.getUnderlayPath());
    }
}
```

## Passo 5: Definisci le Opzioni di Rasterizzazione

Definisci le impostazioni per l'oggetto `CadRasterizationOptions`, includendo larghezza pagina, altezza, layout e colore di sfondo.

```java
CadRasterizationOptions vectorRasterizationOptions = new CadRasterizationOptions();
vectorRasterizationOptions.setPageWidth(1600);
vectorRasterizationOptions.setPageHeight(1600);
vectorRasterizationOptions.setLayouts(new String[] { "Model" });
vectorRasterizationOptions.setAutomaticLayoutsScaling(false);
vectorRasterizationOptions.setNoScaling(true);
vectorRasterizationOptions.setBackgroundColor(Color.getBlack());
vectorRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
```

## Passo 6: Imposta le Opzioni di Rasterizzazione Vettoriale

Imposta le opzioni di rasterizzazione vettoriale per l'esportazione.

```java
exportOptions.setVectorRasterizationOptions(vectorRasterizationOptions);
```

## Passo 7: Esporta DWG in PDF

Infine, esporta il DWG in PDF chiamando il metodo `save`.

```java
cadImage.save(outPath, exportOptions);
```

## Problemi Comuni e Soluzioni

| Problema | Causa | Soluzione |
|----------|-------|-----------|
| **Nessun sottofondo DGN appare** | Il DWG non contiene un'entità `DGNUNDERLAY`. | Verifica che il DWG di origine includa un riferimento DGN. |
| **Il PDF è vuoto** | Opzioni di rasterizzazione impostate a dimensioni zero o layout errato. | Assicurati che `setPageWidth`/`setPageHeight` siano valori positivi e che `setLayouts` corrisponda al nome del layout DWG. |
| **Eccezione di licenza** | Esecuzione senza una licenza valida di Aspose.CAD. | Applica una licenza temporanea o acquistata prima di chiamare qualsiasi metodo API. |

## Domande Frequenti

### Q1: Dove posso trovare la documentazione per Aspose.CAD per Java?

A1: La documentazione è disponibile [qui](https://reference.aspose.com/cad/java/).

### Q2: Come posso scaricare la libreria Aspose.CAD per Java?

A2: Puoi scaricare la libreria da [questo link](https://releases.aspose.com/cad/java/).

### Q3: È disponibile una versione di prova gratuita per Aspose.CAD per Java?

A3: Sì, puoi trovare la trial gratuita [qui](https://releases.aspose.com/).

### Q4: Dove posso ottenere una licenza temporanea per Aspose.CAD per Java?

A4: Ottieni una licenza temporanea [qui](https://purchase.aspose.com/temporary-license/).

### Q5: Hai bisogno di aiuto o hai domande?

A5: Visita il forum di supporto della community Aspose.CAD [qui](https://forum.aspose.com/c/cad/19).

### Q6: Posso convertire il PDF risultante nuovamente in DWG?

A6: Il PDF è un'anteprima raster; la conversione back to DWG richiede uno strumento di reverse‑engineering separato.

### Q7: Questo approccio funziona con altri formati CAD come DWF o DXF?

A7: Sì, Aspose.CAD supporta molti formati; è sufficiente adeguare le estensioni dei file e le impostazioni di rasterizzazione di conseguenza.

---

**Ultimo Aggiornamento:** 2026-01-10  
**Testato Con:** Aspose.CAD per Java 24.11  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}