---
date: 2026-03-05
description: Scopri come impostare il timeout nelle operazioni di salvataggio durante
  la conversione da DWG a PDF con Aspose.CAD per .NET. Aumenta l'efficienza e il controllo
  nelle tue applicazioni .NET.
linktitle: Setting Timeout on Save Operation
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Come impostare il timeout sull'operazione di salvataggio - Tutorial Aspose.CAD
url: /it/net/advanced-cad-techniques/setting-timeout-on-save-operation/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come impostare il timeout sull'operazione di salvataggio - Tutorial Aspose.CAD

## Introduzione

In questa guida imparerai **come impostare il timeout** sulle operazioni di salvataggio CAD, una tecnica che ti aiuta a evitare che conversioni lunghe diventino processi non responsivi. Gestire il timeout è particolarmente utile quando **converti DWG in PDF** o **esporti file CAD PDF** in lavori batch o servizi web. Aspose.CAD per .NET fornisce un'API pulita che ti consente di controllare l'operazione di salvataggio mantenendo tutti i vantaggi del suo potente motore di rasterizzazione.

## Risposte rapide
- **Cosa controlla il timeout?** Interrompe l'operazione di salvataggio/esportazione se supera il periodo specificato.  
- **Quali formati ne traggono maggior beneficio?** La conversione di grandi file DWG in PDF o immagini raster dove il tempo di elaborazione può variare.  
- **È necessaria una licenza?** È richiesta una licenza valida di Aspose.CAD per l'uso in produzione; una versione di prova gratuita è sufficiente per la valutazione.  
- **Posso personalizzare la durata?** Sì—basta modificare il valore di `Thread.Sleep` (in millisecondi) per adattarlo al tuo scenario.  
- **Questo approccio è compatibile con async?** L'esempio utilizza `Task.Factory.StartNew`, facilitando l'integrazione in flussi di lavoro asincroni.

## Che cosa significa “come impostare il timeout” nel contesto del salvataggio CAD?
Impostare un timeout significa allegare un `InterruptionToken` alle opzioni di salvataggio e attivare un'interruzione dopo un intervallo predefinito. Questo impedisce che l'operazione rimanga in sospeso indefinitamente, garantendo prestazioni prevedibili e una migliore gestione delle risorse.

## Perché usare Aspose.CAD per convertire DWG in PDF con un timeout?
- **Affidabilità:** Garantisce che una conversione fuori controllo non blocchi il tuo servizio.  
- **Scalabilità:** Ti permette di elaborare molti file in parallelo senza temere che un singolo file blocchi la pipeline.  
- **Qualità:** Mantiene la rasterizzazione ad alta fedeltà di Aspose.CAD aggiungendo controlli di sicurezza.

## Prerequisiti

Prima di iniziare, assicurati di avere quanto segue:

- **Aspose.CAD for .NET** – integrato nel tuo progetto. Puoi scaricarlo [qui](https://releases.aspose.com/cad/net/).
- **Document Directory** – una cartella dove risiederanno i tuoi file DWG di origine e i PDF di output.

## Importa gli spazi dei nomi

Per prima cosa, importa gli spazi dei nomi che forniscono le classi necessarie per la rasterizzazione, le opzioni PDF e il meccanismo di interruzione.

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Threading;
using System.Threading.Tasks;
```

## Come impostare il timeout sull'operazione di salvataggio

Di seguito trovi una guida passo‑a‑passo. Ogni passaggio include una breve spiegazione seguita dal blocco di codice originale (invariato).

### Passo 1: Carica il disegno CAD

Carichiamo il file DWG di origine dalla directory designata. Il metodo `Image.Load` restituisce un oggetto `Image` che rappresenta il disegno CAD.

```csharp
// Example: Loading CAD Drawing
string SourceDir = "Your Document Directory";
string OutputDir = "Your Document Directory";

using (Image cadDrawing = Image.Load(SourceDir + "Drawing11.dwg"))
{
    // Code for subsequent steps will be placed here
}
```

### Passo 2: Configura le opzioni di rasterizzazione

Imposta le opzioni di rasterizzazione in modo che il PDF esportato corrisponda alle dimensioni originali del disegno. Qui controlli larghezza pagina, altezza e altre impostazioni di rendering.

```csharp
// Example: Configuring Rasterization Options
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = cadDrawing.Size.Width;
rasterizationOptions.PageHeight = cadDrawing.Size.Height;
```

### Passo 3: Crea le opzioni PDF (Esporta CAD PDF)

Crea un'istanza `PdfOptions` e allega le impostazioni di rasterizzazione. Questo oggetto verrà passato al metodo `Save` per generare una versione PDF del file DWG.

```csharp
// Example: Creating PDF Options
PdfOptions CADf = new PdfOptions();
CADf.VectorRasterizationOptions = rasterizationOptions;
```

### Passo 4: Implementa il meccanismo di timeout

Utilizziamo `InterruptionTokenSource` per ottenere un token che può interrompere l'operazione di salvataggio. Un task in background esegue l'esportazione, mentre il thread principale dorme per la durata del timeout desiderata (ad esempio, 10 secondi). Dopo il sonno, chiamiamo `Interrupt()` per annullare l'operazione se è ancora in esecuzione.

```csharp
// Example: Implementing Timeout Mechanism
using (var its = new InterruptionTokenSource())
{
    CADf.InterruptionToken = its.Token;

    var exportTask = Task.Factory.StartNew(() =>
    {
        cadDrawing.Save(OutputDir + "PutTimeoutOnSave_out.pdf", CADf);
    });

    Thread.Sleep(10000); // Set your desired timeout duration in milliseconds
    its.Interrupt();

    exportTask.Wait();
}
```

### Passo 5: Finalizza e conferma

Dopo l'esportazione (o l'interruzione), scrivi un messaggio di conferma sulla console. In un'applicazione reale potresti registrare il risultato o generare un evento.

```csharp
// Example: Finalizing and Confirming
Console.WriteLine("PutTimeoutOnSave executed successfully");
```

## Problemi comuni e soluzioni

| Problema | Causa | Soluzione |
|----------|-------|-----------|
| L'esportazione si blocca indefinitamente | Nessun token di interruzione allegato | Assicurati che `CADf.InterruptionToken = its.Token;` sia impostato prima di avviare il task. |
| Il PDF è vuoto o corrotto | Percorso della directory di output errato | Verifica che `OutputDir` termini con un separatore di percorso e che il nome del file sia valido. |
| Timeout troppo breve, causando interruzione prematura | Valore di `Thread.Sleep` troppo basso per file grandi | Aumenta la durata del sonno o calcola un timeout adattivo in base alle dimensioni del file. |

## Domande frequenti

**Q1: Posso personalizzare la durata del timeout?**  
A: Assolutamente. Modifica il valore passato a `Thread.Sleep` (in millisecondi) per adeguarlo alle tue aspettative di prestazione.

**Q2: Ci sono altre opzioni per la rasterizzazione?**  
A: Sì. `CadRasterizationOptions` offre proprietà come `Resolution`, `BackgroundColor` e `DrawType` per affinare l'output PDF.

**Q3: Come posso gestire le interruzioni nella mia applicazione?**  
A: Usa le classi `InterruptionToken` e `InterruptionTokenSource` come mostrato. Forniscono un modo thread‑safe per abortire operazioni di lunga durata.

**Q4: Aspose.CAD è adatto sia per file CAD 2D che 3D?**  
A: Supporta un'ampia gamma di formati 2D e 3D, inclusi DWG, DXF, DGN e molti altri.

**Q5: Dove posso trovare ulteriore assistenza o supporto della community?**  
A: Visita il [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) per discussioni della community, esempi di codice e consigli di risoluzione problemi.

## Conclusione

Seguendo i passaggi sopra, ora sai **come impostare il timeout** sulle operazioni di salvataggio CAD, consentendoti di convertire in modo affidabile **DWG in PDF** o **esportare CAD PDF** senza rischiare processi non responsivi. Integra questo modello in convertitori batch, servizi web o qualsiasi pipeline automatizzata dove la prevedibilità è fondamentale.

---

**Last Updated:** 2026-03-05  
**Tested With:** Aspose.CAD 24.12 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}