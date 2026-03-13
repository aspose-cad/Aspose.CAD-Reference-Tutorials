---
description: Scopri come convertire DWG in PNG ed estrarre oggetti OLE dai file DWG
  usando Aspose.CAD per .NET – una guida rapida e incentrata sul codice.
linktitle: Exporting OLE Objects from DWG Files
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Converti DWG in PNG ed esporta oggetti OLE – Tutorial Aspose.CAD
url: /it/net/advanced-export-techniques/exporting-ole-objects-from-dwg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Esportazione di oggetti OLE da file DWG - Tutorial Aspose.CAD

## Introduzione

Se hai bisogno di **convertire DWG in PNG** estraendo gli oggetti OLE incorporati, sei nel posto giusto. Aspose.CAD per .NET rende questo processo a due passaggi semplice, consentendoti di automatizzare l'estrazione e la rasterizzazione con poche righe di C#. Nei prossimi minuti percorreremo l'intero flusso di lavoro, dalla configurazione dell'ambiente al salvataggio di ogni DWG come PNG contenente i dati OLE estratti.

## Risposte rapide
- **Di cosa tratta questo tutorial?** Conversione di DWG in PNG ed estrazione di oggetti OLE usando Aspose.CAD per .NET.  
- **È necessaria una licenza?** Una versione di prova gratuita è sufficiente per lo sviluppo; è necessaria una licenza commerciale per la produzione.  
- **Quali versioni di .NET sono supportate?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Posso elaborare più file DWG contemporaneamente?** Sì – l'esempio itera su un array di nomi file.  
- **Dove posso trovare altri esempi?** Consulta la documentazione ufficiale di Aspose.CAD e i link al forum qui sotto.

## Cos'è **convert DWG to PNG**?
Convertire un DWG (disegno AutoCAD) in un'immagine PNG rasterizza i dati vettoriali, rendendo più semplice la visualizzazione o l'incorporamento in pagine web, report o altre applicazioni che non supportano nativamente il DWG. Quando sono presenti oggetti OLE, questi possono essere estratti e salvati come risorse separate durante la conversione.

## Perché estrarre oggetti OLE da file CAD?
Molti disegni DWG incorporano fogli di calcolo, grafici o altri documenti Office come oggetti OLE. Estrarli consente di riutilizzare i dati originali, automatizzare i report o migrare i contenuti verso formati più recenti senza perdere le informazioni incorporate.

## Prerequisiti

- Aspose.CAD per .NET Library: assicurati di aver installato la libreria. Puoi scaricarla dalla [pagina di download di Aspose.CAD per .NET](https://releases.aspose.com/cad/net/).
- Directory dei documenti: configura una cartella dove sono archiviati i tuoi file DWG. Sostituisci `"Your Document Directory"` nello snippet di codice fornito con il percorso reale.

## Importare gli spazi dei nomi

Nel tuo progetto .NET, importa gli spazi dei nomi richiesti:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Guida passo‑passo

### Passo 1: Impostare la directory dei documenti

```csharp
string MyDir = "Your Document Directory";
```

Sostituisci `"Your Document Directory"` con il percorso dove si trovano i tuoi file DWG.

### Passo 2: Elencare i file DWG da elaborare

```csharp
string[] files = new string[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

### Passo 3: Configurare le opzioni di esportazione per la conversione PNG

```csharp
PngOptions pngOptions = new PngOptions { };
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.VectorRasterizationOptions = rasterizationOptions;
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

Puoi modificare `CadRasterizationOptions` (ad esempio `PageWidth`, `PageHeight`, `BackgroundColor`) per adattarle alla risoluzione di output desiderata.

### Passo 4: Iterare su ogni DWG ed eseguire la conversione

```csharp
foreach (string file in files)
{
    using (CadImage cadImage = (CadImage)Image.Load(MyDir + file))
    {
        cadImage.Save(MyDir + file + "_out.png", pngOptions);
    }
}
```

Durante questo ciclo la libreria estrae automaticamente **oggetti OLE** incorporati in ogni disegno e li include nel PNG generato. Se ti servono i flussi OLE grezzi, puoi accedere alla collezione `cadImage.OleObjects` – un modo pratico per **come estrarre ole** dati programmaticamente.

## Problemi comuni e risoluzione

- **Nome layout mancante** – Assicurati che il layout specificato (`"Layout1"` nell'esempio) esista nel DWG di origine; altrimenti il rasterizzatore utilizza lo spazio modello predefinito.
- **File di grandi dimensioni causano pressione sulla memoria** – Elabora i file uno alla volta (come mostrato) e rilascia gli oggetti `CadImage` tempestivamente con `using`.
- **Colori inattesi** – Imposta `rasterizationOptions.BackgroundColor` per corrispondere allo sfondo del disegno se è necessaria la trasparenza.

## Domande frequenti

### Q1: Aspose.CAD per .NET è adatto sia a file CAD junior che senior?
A1: Sì, Aspose.CAD per .NET è versatile e può gestire un'ampia gamma di file CAD, inclusi sia varianti junior che senior.

### Q2: Posso personalizzare le opzioni di esportazione per layout diversi?
A2: Assolutamente! Come mostrato nel tutorial, puoi personalizzare le opzioni di esportazione, inclusi i layout, per soddisfare le tue esigenze specifiche.

### Q3: Dove posso trovare la documentazione dettagliata per Aspose.CAD per .NET?
A3: Consulta la [documentazione di Aspose.CAD per .NET](https://reference.aspose.com/cad/net/) per informazioni approfondite ed esempi.

### Q4: È disponibile una versione di prova gratuita?
A4: Sì, puoi provare le funzionalità di Aspose.CAD per .NET con una versione di prova gratuita. Visita [questo link](https://releases.aspose.com/) per iniziare.

### Q5: Come posso ottenere supporto o entrare in contatto con la community?
A5: Per supporto e interazione con la community, visita il [forum di Aspose.CAD](https://forum.aspose.com/c/cad/19).

### Q6: Come **estrarre OLE da file CAD** senza convertire in PNG?
A6: Usa la collezione `CadImage.OleObjects` dopo aver caricato il DWG; puoi iterare su ogni `OleObject` e salvare i dati grezzi in un file.

## Conclusione

Ora hai visto come **convertire DWG in PNG** estraendo senza problemi gli **oggetti OLE** usando Aspose.CAD per .NET. Questo approccio fa risparmiare tempo, elimina le operazioni manuali di copia‑incolla e si integra perfettamente in pipeline automatizzate. Sentiti libero di sperimentare altri formati raster (JPEG, BMP) o di esplorare l'ampia gamma di funzionalità di manipolazione CAD offerte da Aspose.

---

**Ultimo aggiornamento:** 2026-03-13  
**Testato con:** Aspose.CAD 24.11 per .NET  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}