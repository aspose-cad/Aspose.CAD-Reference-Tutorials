---
date: 2026-03-29
description: Scopri come convertire DGN in PNG usando Aspose.CAD per .NET. Questa
  guida copre anche il supporto dei formati di file CAD e l'intero set di elementi
  DGN supportati.
linktitle: Supported DGN Elements
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Converti DGN in PNG con Aspose.CAD per .NET
url: /it/net/cad-features-and-support/supported-dgn-elements/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Converti DGN in PNG con Aspose.CAD per .NET

## Introduzione

Sei uno sviluppatore .NET alla ricerca di un modo per **convertire DGN in PNG** senza problemi? Aspose.CAD per .NET offre una soluzione solida per gestire i file DGN in modo efficiente. In questo tutorial, approfondiremo gli elementi DGN supportati, guidandoti attraverso il processo di utilizzo di Aspose.CAD per .NET e mostrandoti esattamente come esportare tali elementi in immagini PNG.

## Risposte rapide
- **Cosa fa Aspose.CAD?** Legge, modifica e converte file CAD/BIM (inclusi DGN) in formati raster come PNG.  
- **Posso convertire elementi DGN 2D e 3D?** Sì – sono supportate sia entità 2‑D che 3‑D.  
- **Quali versioni .NET sono richieste?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Ho bisogno di una licenza per i test?** È disponibile una prova gratuita; è necessaria una licenza per la produzione.  
- **Dove posso ottenere la libreria?** Scaricala dal sito ufficiale di Aspose (link sotto).

## Cos'è “convertire DGN in PNG”?
Convertire DGN in PNG significa renderizzare il disegno DGN basato su vettori (2‑D o 3‑D) in un formato immagine raster (PNG). Questo è utile quando è necessario visualizzare disegni CAD sul web, incorporarli in report o generare miniature senza richiedere un visualizzatore CAD.

## Perché usare Aspose.CAD per .NET per il supporto dei formati di file CAD?
- **Supporto completo dei formati di file CAD** – DGN, DWG, DXF, DWF e altri.  
- **Nessuna dipendenza esterna** – libreria .NET pura, senza installazioni CAD native.  
- **Rendering ad alta fedeltà** – preserva spessori delle linee, colori e geometria 3‑D.  
- **Elaborazione batch** – itera facilmente su molti file in un'applicazione lato server.

## Prerequisiti

- Conoscenza di base della programmazione .NET.  
- Visual Studio installato sulla tua macchina.  
- Libreria Aspose.CAD per .NET, che puoi scaricare [qui](https://releases.aspose.com/cad/net/).

## Importa spazi dei nomi

Per avviare il tuo progetto, importa gli spazi dei nomi necessari nella tua applicazione .NET. Questo passaggio garantisce l'accesso alle funzionalità offerte da Aspose.CAD per .NET.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.FileFormats.Dgn.DgnElements;
```

## Come convertire DGN in PNG

Di seguito trovi una guida passo‑passo che ti accompagna nel caricamento di un file DGN, nell'iterazione dei suoi elementi, nella gestione di entità 2‑D e 3‑D e, infine, nell'esportazione del risultato in un'immagine raster PNG.

### Passo 1: Carica il file DGN

Inizia caricando un file DGN esistente come `DgnImage` nella tua applicazione .NET.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Your code here
}
```

### Passo 2: Itera attraverso gli elementi DGN

Itera attraverso gli elementi DGN usando un ciclo `foreach`. Aspose.CAD per .NET fornisce una varietà di tipi di elementi DGN con cui puoi lavorare.

```csharp
foreach (DgnDrawingElementBase element in dgnImage.Elements)
{
    // Your code here
}
```

### Passo 3: Gestisci le entità 2‑D precedentemente supportate

Queste entità sono ora supportate anche per il rendering 3‑D. L'istruzione switch ti consente di ramificare la logica in base al tipo di elemento.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.Line:
    case DgnElementType.Ellipse:
    case DgnElementType.Curve:
    // Additional cases
        {
            // Your code here
            break;
        }
}
```

### Passo 4: Gestisci le entità 3‑D supportate

Aspose.CAD aggiunge il supporto completo per diversi elementi DGN 3‑D. Estendi lo switch per elaborarli secondo necessità.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.SolidHeader3D:
    case DgnElementType.Cone:
    case DgnElementType.CellHeader:
        {
            // Your code here
            break;
        }
}
```

### Passo 5: Esporta e salva come PNG

Dopo eventuali manipolazioni necessarie, esporta il disegno DGN in un'immagine raster PNG e salvalo nella directory specificata.

```csharp
Console.WriteLine("\nThe DGN file exported successfully to raster image.\nFile saved at " + MyDir);
```

> **Consiglio professionale:** Usa `Image.Save` con `new PngOptions()` per controllare la risoluzione, il colore di sfondo e altre impostazioni specifiche di PNG.

## Panoramica del supporto dei formati di file CAD

Aspose.CAD per .NET non è limitato a DGN. Supporta anche DWG, DXF, DWF e molti altri formati CAD, fornendoti un'unica API per gestire un ampio spettro di disegni ingegneristici. Questo lo rende ideale per progetti che richiedono **supporto dei formati di file CAD** su più standard.

## Problemi comuni e soluzioni

| Problema | Motivo | Soluzione |
|----------|--------|-----------|
| **L'immagine appare vuota** | Esportata con DPI zero | Specifica `ResolutionX` e `ResolutionY` in `PngOptions`. |
| **Geometria 3‑D mancante** | Tipo di elemento non gestito nello switch | Aggiungi il caso `DgnElementType` mancante e renderizza di conseguenza. |
| **Memoria esaurita su file di grandi dimensioni** | Caricamento dell'intero file in una volta | Elabora gli elementi in batch o usa lo streaming dove possibile. |

## Domande frequenti

### Q1: Dove posso trovare la documentazione per Aspose.CAD per .NET?
A1: Puoi trovare la documentazione [qui](https://reference.aspose.com/cad/net/).

### Q2: Come scarico Aspose.CAD per .NET?
A2: Puoi scaricare la libreria [qui](https://releases.aspose.com/cad/net/).

### Q3: È disponibile una prova gratuita per Aspose.CAD per .NET?
A3: Sì, puoi accedere alla prova gratuita [qui](https://releases.aspose.com/).

### Q4: Dove posso ottenere licenze temporanee per Aspose.CAD per .NET?
A4: Le licenze temporanee sono disponibili [qui](https://purchase.aspose.com/temporary-license/).

### Q5: Hai bisogno di aiuto o hai domande?
A5: Visita il forum di supporto della community Aspose.CAD per .NET [forum di supporto](https://forum.aspose.com/c/cad/19).

---

**Ultimo aggiornamento:** 2026-03-29  
**Testato con:** Aspose.CAD per .NET 24.11  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}