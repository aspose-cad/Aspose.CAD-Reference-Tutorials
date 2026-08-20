---
date: 2026-04-09
description: Scopri come caricare file DWFX in C# e convertire CAD in PDF usando Aspose.CAD
  per .NET. Guida passo‑passo per un'integrazione senza problemi.
keywords:
- load dwfx file c#
- c# convert cad to pdf
- aspose.cad dwfx
linktitle: Apertura e accesso ai file DWFX in C#
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Come caricare un file DWFX in C# con la guida Aspose.CAD
url: /it/net/dwg-file-manipulation/opening-and-accessing-dwfx-files/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come caricare un file DWFX in C# con la guida Aspose.CAD

## Introduzione

Se hai bisogno di **caricare un file DWFX C#** e trasformarlo in PDF, sei nel posto giusto. In questo tutorial percorreremo i passaggi esatti necessari per aprire un disegno DWFX con Aspose.CAD per .NET, configurare la rasterizzazione e infine **c# convert CAD to PDF**. Che tu stia creando un'utilità desktop o un servizio web, l'approccio rimane lo stesso e funziona con qualsiasi versione .NET supportata da Aspose.CAD.

## Risposte rapide
- **Quale libreria è necessaria?** Aspose.CAD per .NET  
- **Posso convertire DWFX in PDF?** Sì – basta configurare `CadRasterizationOptions` e usare `PdfOptions`.  
- **Quali versioni .NET sono supportate?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Ho bisogno di una licenza per i test?** Una versione di prova gratuita funziona per lo sviluppo; è necessaria una licenza permanente per la produzione.  
- **Quanto tempo impiega il codice ad eseguire?** Il caricamento e la conversione di un tipico file DWFX terminano in meno di un secondo su una CPU moderna.

## Cos'è un file DWFX?

DWFX (Design Web Format XPS) è una rappresentazione basata su XML di un disegno CAD che può essere visualizzata nei browser e in altri visualizzatori. Poiché memorizza dati vettoriali, è ideale per la conversione PDF di alta qualità senza perdita di dettagli.

## Perché usare Aspose.CAD per caricare file DWFX in C#?

* **Supporto completo dei formati** – Aspose.CAD comprende DWFX insieme a decine di altri formati CAD.  
* **Nessuna dipendenza esterna** – Pure .NET, senza necessità di AutoCAD o altri componenti nativi.  
* **Facile conversione raster‑a‑vettore** – Passa tra immagini raster e PDF vettoriali con poche righe di codice.  

## Prerequisiti

Prima di immergerci nel codice, assicurati di avere:

1. **Aspose.CAD per .NET** installato. Puoi scaricarlo [qui](https://releases.aspose.com/cad/net/).  
2. Una cartella che contiene i file DWFX che desideri elaborare. Nota il percorso completo sia per la sorgente sia per la destinazione.

## Come caricare un file DWFX in C#

Di seguito è riportata la guida passo‑passo. Ogni passaggio è accompagnato da una breve spiegazione, seguita dal blocco di codice esatto da copiare.

### Importa spazi dei nomi

```csharp
using Aspose.CAD.ImageOptions;
using System;
```

Questi spazi dei nomi ti danno accesso alla classe `Image` per caricare i file CAD e alle opzioni necessarie per la rasterizzazione e l'output PDF.

### Passo 1: Configura le directory di origine e destinazione

```csharp
string SourceDir = "Your Document Directory";
string OutputDir = "Your Document Directory";
```

Sostituisci `"Your Document Directory"` con il percorso in cui si trova il tuo file DWFX e dove vuoi salvare il PDF.

### Passo 2: Carica il file DWFX

```csharp
using (Image cadDrawing = Image.Load(SourceDir + "Tyrannosaurus.dwfx"))
```

`Image.Load` legge il file DWFX in un oggetto `Image` con cui Aspose.CAD può lavorare. Cambia `"Tyrannosaurus.dwfx"` con il nome del tuo disegno.

### Passo 3: Configura le opzioni di rasterizzazione

```csharp
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = cadDrawing.Size.Width;
rasterizationOptions.PageHeight = cadDrawing.Size.Height;
```

Le opzioni di rasterizzazione indicano ad Aspose.CAD quanto grande deve essere la pagina risultante. Utilizzare le dimensioni originali del disegno preserva la scala esatta.

### Passo 4: Salva come PDF (c# convert CAD to PDF)

```csharp
PdfOptions CADf = new PdfOptions();
CADf.VectorRasterizationOptions = rasterizationOptions;
cadDrawing.Save(OutputDir + "OpenDwfxFile_out.pdf", CADf);
```

Qui **c# convert CAD to PDF** collegando le impostazioni di rasterizzazione a un oggetto `PdfOptions` e chiamando `Save`. Il file di output verrà posizionato nella cartella specificata.

### Passo 5: Visualizza il messaggio di successo

```csharp
Console.WriteLine("OpenDwfxFile executed successfully");
```

Un semplice messaggio nella console ti informa che la conversione è terminata senza errori.

## Problemi comuni e consigli

* **File non trovato** – Verifica il percorso `SourceDir` e assicurati che il nome del file corrisponda esattamente, includendo maiuscole/minuscole.  
* **PDF vuoto** – Accertati che il file DWFX contenga effettivamente dati vettoriali; alcuni strumenti di esportazione generano disegni vuoti.  
* **Prestazioni** – Per disegni molto grandi, considera di ridurre `PageWidth`/`PageHeight` o impostare una `Resolution` più bassa in `CadRasterizationOptions`.

## Domande frequenti

### Q1: Aspose.CAD per .NET è compatibile con tutti i file DWFX?

A1: Aspose.CAD per .NET supporta un'ampia gamma di formati CAD, incluso DWFX. Tuttavia, è consigliabile consultare la documentazione per dettagli specifici di compatibilità.

### Q2: Dove posso trovare la documentazione per Aspose.CAD per .NET?

A2: La documentazione è disponibile [qui](https://reference.aspose.com/cad/net/).

### Q3: Posso provare Aspose.CAD per .NET prima di acquistare?

A3: Sì, puoi scaricare una versione di prova gratuita [qui](https://releases.aspose.com/).

### Q4: Come ottengo una licenza temporanea per Aspose.CAD per .NET?

A4: Le licenze temporanee possono essere ottenute [qui](https://purchase.aspose.com/temporary-license/).

### Q5: Hai bisogno di supporto o hai altre domande?

A5: Visita il [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) per assistenza.

### Q6: Posso elaborare in batch più file DWFX?

A6: Assolutamente. Avvolgi la logica di caricamento e salvataggio all'interno di un ciclo `foreach` che itera sui file in una directory.

### Q7: La conversione preserva livelli e colori?

A7: Le informazioni vettoriali come livelli e colori vengono mantenute nel PDF quando il DWFX di origine contiene tali dati.

---

**Ultimo aggiornamento:** 2026-04-09  
**Testato con:** Aspose.CAD per .NET 24.11  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}