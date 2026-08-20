---
date: 2026-04-09
description: Scopri come esportare i layer DWG, convertire l'immagine DWG e salvare
  il JPEG DWG usando C# con Aspose.CAD per .NET. Guida passo‑passo per una manipolazione
  efficiente dei file CAD.
keywords:
- export dwg layers
- convert dwg image
- dwg layer visibility
- save dwg jpeg
linktitle: Gestione dei layer nei file DWG con C#
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Esporta i layer DWG con C# – Tutorial Aspose.CAD
url: /it/net/dwg-file-manipulation/support-of-layers/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Esporta i layer DWG con C# – Tutorial Aspose.CAD

## Introduzione

In questa guida completa imparerai **come esportare i layer DWG** usando C# e la libreria Aspose.CAD. Che tu abbia bisogno di **convertire immagini DWG**, controllare la **visibilità dei layer DWG**, o semplicemente **salvare file DWG JPEG**, i passaggi seguenti ti mostreranno esattamente come farlo in modo efficiente. Alla fine del tutorial avrai uno snippet pronto all'uso che isola un layer specifico e lo rende come un JPEG ad alta qualità.

## Risposte rapide
- **Cosa significa “export dwg layers”?** Significa rasterizzare i layer selezionati di un file DWG in un formato immagine come JPEG o PNG.  
- **Quale libreria è la migliore per questo compito?** Aspose.CAD per .NET fornisce supporto completo senza richiedere AutoCAD.  
- **Posso esportare più layer contemporaneamente?** Sì – passa un array di nomi di layer alle opzioni di rasterizzazione.  
- **È necessaria una licenza per l'uso in produzione?** È richiesta una licenza commerciale; è disponibile una versione di prova gratuita per la valutazione.  
- **Quali formati di output sono supportati?** JPEG, PNG, BMP, TIFF e diversi altri tramite le classi ImageOptions.

## Cos'è l'esportazione dei layer DWG?
Esportare i layer DWG significa prendere i dati vettoriali che appartengono a uno o più layer all'interno di un disegno DWG e rasterizzarli in un'immagine bitmap. Questo è utile quando vuoi condividere una vista di una parte specifica di un disegno senza esporre l'intero file CAD.

## Perché controllare la visibilità dei layer DWG?
Controllare la visibilità dei layer DWG ti permette di:

- Creare risorse visive pulite per presentazioni o documentazione.  
- Ridurre le dimensioni del file esportando solo la geometria necessaria.  
- Proteggere i dettagli di progetto proprietari nascondendo i layer riservati.  

## Prerequisiti

Prima di approfondire, verifica di avere:

- Conoscenza di base del linguaggio di programmazione C#.  
- Visual Studio installato sulla tua macchina.  
- Libreria Aspose.CAD per .NET, che puoi scaricare dal [sito Aspose.CAD](https://releases.aspose.com/cad/net/).

## Importa gli spazi dei nomi

Per iniziare, importa gli spazi dei nomi che ti danno accesso alle funzionalità di rasterizzazione e esportazione delle immagini.

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

## Passo 1: Carica il file DWG

Carica il file DWG (o DWF) sorgente in un oggetto `Image`. Questo oggetto rappresenta l'intero disegno in memoria.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "for_layers_test.dwf";

using (Aspose.CAD.Image image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // Your code for subsequent steps goes here
}
```

*Perché è importante:* Caricare il file una sola volta ti consente di riutilizzare la stessa istanza `image` per qualsiasi numero di esportazioni specifiche per layer, migliorando le prestazioni.

## Passo 2: Configura le opzioni di rasterizzazione

Crea un'istanza `CadRasterizationOptions` per indicare ad Aspose.CAD come renderizzare il disegno. Qui impostiamo un'alta risoluzione (1600 × 1600) per garantire che il JPEG esportato sia nitido.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
```

Puoi anche regolare il colore di sfondo, la scala del peso delle linee o le impostazioni di anti‑aliasing se necessario.

## Passo 3: Specifica i layer (visibilità dei layer DWG)

Aggiungi i layer per i quali desideri **esportare i layer DWG**. In questo esempio esportiamo solo “LayerA”. Per esportare più layer, elencali semplicemente nell'array.

```csharp
rasterizationOptions.Layers = new string[] { "LayerA" };
```

*Consiglio professionale:* Usa il nome esatto del layer così come appare nel disegno; i nomi dei layer sono sensibili al maiuscolo/minuscolo.

## Passo 4: Configura le opzioni di esportazione immagine

Scegli il formato immagine che desideri creare. Useremo `JpegOptions` perché JPEG offre un buon equilibrio tra qualità e dimensione del file, ideale quando devi **salvare file dwg jpeg** per l'anteprima web.

```csharp
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.VectorRasterizationOptions = rasterizationOptions;
```

Se hai bisogno di **convertire immagine dwg** in PNG o TIFF, sostituisci `JpegOptions` con la classe di opzioni corrispondente.

## Passo 5: Salva l'immagine esportata

Definisci il percorso del file di output e invoca `Save`. Il motore di rasterizzazione rispetta l'elenco dei layer fornito, quindi solo “LayerA” appare nel JPEG finale.

```csharp
MyDir = MyDir + "for_layers_test.jpg";
image.Save(MyDir, jpegOptions);
```

Dopo l'esecuzione di questa riga, troverai `for_layers_test.jpg` nella directory del tuo documento, contenente solo il layer selezionato.

## Problemi comuni e soluzioni

| Problema | Risoluzione |
|----------|-------------|
| **Nome del layer non trovato** | Verifica l'ortografia esatta e il caso del layer nel DWG originale. Usa un visualizzatore CAD per elencare i nomi dei layer. |
| **Immagine di output vuota** | Assicurati che le opzioni di rasterizzazione abbiano uno sfondo non trasparente e che i layer selezionati contengano effettivamente geometria. |
| **Output a bassa risoluzione** | Aumenta `PageWidth` e `PageHeight` o imposta `Resolution` in `CadRasterizationOptions`. |
| **Versione DWG non supportata** | Aggiorna all'ultima versione di Aspose.CAD; aggiunge il supporto per le versioni più recenti di AutoCAD. |

## Domande frequenti

### Q1: Posso gestire più layer simultaneamente?
A1: Sì, puoi. Basta aggiungere i nomi dei layer all'array `rasterizationOptions.Layers`.

### Q2: È disponibile una versione di prova di Aspose.CAD?
A2: Sì, puoi ottenere una versione di prova gratuita da [qui](https://releases.aspose.com/).

### Q3: Dove posso trovare la documentazione?
A3: La documentazione è disponibile [qui](https://reference.aspose.com/cad/net/).

### Q4: Come posso ottenere supporto per Aspose.CAD?
A4: Puoi cercare supporto sul [forum Aspose.CAD](https://forum.aspose.com/c/cad/19).

### Q5: Quali sono le opzioni di licenza per Aspose.CAD?
A5: Puoi esplorare le opzioni di licenza e i dettagli di acquisto [qui](https://purchase.aspose.com/buy).

**Domande aggiuntive**

**Q: Posso esportare il disegno in PNG invece di JPEG?**  
A: Assolutamente. Sostituisci `JpegOptions` con `PngOptions` e regola l'estensione del file di conseguenza.

**Q: La libreria preserva gli stili di linea e i colori?**  
A: Sì. Tutte le proprietà vettoriali vengono renderizzate fedelmente durante la rasterizzazione.

**Ultimo aggiornamento:** 2026-04-09  
**Testato con:** Aspose.CAD per .NET (ultima versione)  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}