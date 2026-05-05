---
date: 2026-04-09
description: Scopri come convertire DWG in immagine e come leggere i flag di sottofondo
  utilizzando Aspose.CAD per .NET in questa guida passo‑passo.
keywords:
- convert dwg to image
- how to read underlay
- Aspose.CAD DWG underlay flags
linktitle: Esplorare i flag di sottofondo dei file DWG
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Converti DWG in immagine – Esplorazione dei flag di sottofondo dei file DWG
  - Tutorial Aspose.CAD
url: /it/net/dwg-file-manipulation/exploring-underlay-flags-of-dwg/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Esplorare i flag di sottofondo dei file DWG - Tutorial Aspose.CAD

## Introduzione

Se ti stai immergendo nel complesso mondo dei file CAD, in particolare i file DWG, e desideri **convert DWG to image** scoprendo anche **how to read underlay** flag, sei nel posto giusto. Questo tutorial ti guida passo passo usando la potente libreria Aspose.CAD per .NET, così potrai estrarre le informazioni di sottofondo e renderizzare il disegno come immagine con fiducia.

## Risposte rapide

- **Cosa significa “convert DWG to image”?**  
  Significa renderizzare un disegno DWG in un formato raster (PNG, JPEG, ecc.) usando Aspose.CAD.
- **Quale metodo rivela i flag di sottofondo?**  
  Accedi alla proprietà `Flags` dell'oggetto `CadUnderlay` dopo aver caricato il DWG.
- **Ho bisogno di una licenza per Aspose.CAD?**  
  È disponibile una licenza temporanea per la valutazione; è necessaria una licenza completa per la produzione.
- **Quali versioni .NET sono supportate?**  
  .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6 and later.
- **Posso estrarre la geometria del sottofondo?**  
  Sì – il percorso del sottofondo, il punto di inserimento, la scala, la rotazione e gli stati dei flag sono tutti accessibili.

## Cos'è “convert DWG to image” e perché è importante?

Convertire un file DWG in un'immagine ti consente di visualizzare i disegni CAD nei browser, incorporarli nei report o condividerli con stakeholder che non hanno un visualizzatore CAD. Durante il rendering, è spesso necessario ispezionare gli oggetti **underlay** (ad es., riferimenti DGN) per assicurarsi che vengano visualizzati correttamente. Comprendere i flag di underlay ti aiuta a risolvere problemi di ritaglio, rendering in bianco e nero e di visibilità prima di generare l'immagine finale.

## Prerequisiti

- Una conoscenza di base di C# e della programmazione .NET.  
- **Aspose.CAD for .NET** library installed. If you don’t have it yet, download it **[qui](https://releases.aspose.com/cad/net/)**.  
- Un file DWG per i test – il file di esempio **“BlockRefDgn.dwg”** è usato in tutta la guida.

## Importare gli spazi dei nomi

To get started, import the necessary namespaces:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Passo 1: Caricare il file DWG e convertire in `CadImage`

Per prima cosa, carica il file DWG e castalo a `CadImage`. Questo oggetto ti dà accesso a tutte le entità del disegno, incluse le sottofondi.

```csharp
string fileName = MyDir + "BlockRefDgn.dwg";

// Load DWG file and convert to CadImage
using (CadImage image = (CadImage)Image.Load(fileName))
{
    // Your code for subsequent steps will go here
}
```

## Passo 2: Iterare attraverso le entità

Successivamente, cicla attraverso ogni entità del disegno. Qui individuerai gli oggetti underlay.

```csharp
foreach (CadBaseEntity entity in image.Entities)
{
    // Your code for subsequent steps will go here
}
```

## Passo 3: Verificare il tipo `CadDgnUnderlay`

Identifica le entità underlay controllando il loro tipo a runtime. La classe `CadDgnUnderlay` rappresenta i sottofondi DGN incorporati in un DWG.

```csharp
if (entity is CadDgnUnderlay)
{
    // Your code for subsequent steps will go here
}
```

## Passo 4: Accedere ai flag di underlay

Una volta ottenuto un `CadDgnUnderlay`, castalo a `CadUnderlay` per leggere le sue proprietà e gli stati dei flag. I flag indicano se il sottofondo è visibile, ritagliato o renderizzato in bianco e nero.

```csharp
CadUnderlay underlay = entity as CadUnderlay;

Console.WriteLine(underlay.UnderlayPath);
Console.WriteLine(underlay.UnderlayName);
Console.WriteLine(underlay.InsertionPoint.X);
Console.WriteLine(underlay.InsertionPoint.Y);
Console.WriteLine(underlay.RotationAngle);
Console.WriteLine(underlay.ScaleX);
Console.WriteLine(underlay.ScaleY);
Console.WriteLine(underlay.ScaleZ);
Console.WriteLine((underlay.Flags & UnderlayFlags.UnderlayIsOn) == UnderlayFlags.UnderlayIsOn);
Console.WriteLine((underlay.Flags & UnderlayFlags.ClippingIsOn) == UnderlayFlags.ClippingIsOn);
Console.WriteLine((underlay.Flags & UnderlayFlags.Monochrome) != UnderlayFlags.Monochrome);
```

### Cosa indica l'output

- **UnderlayPath / UnderlayName** – dove si trova il file DGN esterno.  
- **InsertionPoint (X, Y)** – coordinate in cui il sottofondo è posizionato nello spazio DWG.  
- **RotationAngle** – rotazione applicata al sottofondo.  
- **ScaleX / ScaleY / ScaleZ** – fattori di scala per ciascun asse.  
- **Flags** – valori booleani che indicano visibilità (`UnderlayIsOn`), ritaglio (`ClippingIsOn`) e rendering in bianco e nero (`Monochrome`).

## Problemi comuni e soluzioni

| Problema | Motivo | Soluzione |
|----------|--------|-----------|
| Nessun output per i controlli dei flag | I flag di underlay sono impostati a 0 quando il sottofondo è disattivato. | Assicurati che il DWG contenga effettivamente un sottofondo attivo o attiva la visibilità nel file CAD di origine. |
| `Invalid cast` exception | L'entità non è un `CadDgnUnderlay`. | Verifica la guardia `if (entity is CadDgnUnderlay)` prima del cast. |
| Il rendering dell'immagine fallisce dopo l'estrazione dei flag | Il sottofondo potrebbe essere ritagliato o disattivato, causando un'area vuota. | Regola i flag (`UnderlayIsOn = true`, `ClippingIsOn = false`) prima di renderizzare l'immagine finale. |

## Domande frequenti

### Q1: Posso usare Aspose.CAD per .NET con altri formati di file CAD?

A1: Aspose.CAD supporta vari formati CAD, tra cui DWG, DXF, DGN e altri. Consulta la documentazione per l'elenco completo.

### Q2: È disponibile una licenza temporanea per Aspose.CAD per .NET?

A2: Sì, puoi ottenere una licenza temporanea **[qui](https://purchase.aspose.com/temporary-license/)**.

### Q3: Dove posso trovare supporto per Aspose.CAD per .NET?

A3: Visita il forum di supporto **[qui](https://forum.aspose.com/c/cad/19)** per assistenza.

### Q4: Come posso acquistare Aspose.CAD per .NET?

A4: Acquista la libreria **[qui](https://purchase.aspose.com/buy)**.

### Q5: È disponibile una versione di prova gratuita?

A5: Sì, puoi accedere alla versione di prova gratuita **[qui](https://releases.aspose.com/)**.

## Conclusione

Congratulazioni! Hai imparato con successo **how to convert DWG to image** mentre hai anche padroneggiato **how to read underlay** flag usando Aspose.CAD per .NET. Con questa conoscenza puoi:

- Renderizzare i disegni DWG come immagini raster per scenari web o di reporting.  
- Ispezionare e manipolare le proprietà del sottofondo per garantire una visualizzazione corretta.  
- Debuggare problemi di visibilità, ritaglio e rendering in bianco e nero prima della generazione dell'immagine finale.

Sentiti libero di esplorare altre funzionalità di Aspose.CAD come la gestione dei layer, l'estrazione di testo e la conversione batch per estendere ulteriormente i tuoi flussi di lavoro di automazione CAD.

---

**Ultimo aggiornamento:** 2026-04-09  
**Testato con:** Aspose.CAD for .NET 24.11  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}