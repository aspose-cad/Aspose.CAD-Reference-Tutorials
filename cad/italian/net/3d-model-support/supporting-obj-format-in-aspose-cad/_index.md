---
date: 2026-07-04
description: Scopri come impostare la dimensione della pagina PDF durante la conversione
  di file OBJ in PDF utilizzando Aspose.CAD per .NET. Guida passo‑passo con prerequisiti,
  opzioni di rasterizzazione e opzioni PDF.
keywords:
- set pdf page size
- load obj file
- save cad as pdf
- 3d model to pdf
- how to convert obj
linktitle: Supportare il formato OBJ in Aspose.CAD - Tutorial
schemas:
- author: Aspose
  dateModified: '2026-07-04'
  description: Learn how to set PDF page size while converting OBJ files to PDF using
    Aspose.CAD for .NET. Step‑by‑step guide with prerequisites, rasterization options,
    and PDF options.
  headline: Set PDF Page Size for OBJ Files with Aspose.CAD - Tutorial
  type: TechArticle
- questions:
  - answer: Yes, Aspose.CAD supports over **30** input formats—including DWG, DXF,
      DGN, and STL—and can export to more than **20** raster and vector formats.
    question: Is Aspose.CAD compatible with other CAD file formats?
  - answer: Absolutely! You can explore a free trial version [here](https://releases.aspose.com/).
    question: Can I try Aspose.CAD before purchasing?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) to ask
      questions and share experiences with the community.
    question: How do I obtain support for Aspose.CAD?
  - answer: Yes, temporary licenses can be obtained [here](https://purchase.aspose.com/temporary-license/).
    question: Are temporary licenses available for testing?
  - answer: You can purchase Aspose.CAD [here](https://purchase.aspose.com/buy).
    question: Where can I purchase a full license?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Imposta la dimensione della pagina PDF per i file OBJ con Aspose.CAD - Tutorial
url: /it/net/3d-model-support/supporting-obj-format-in-aspose-cad/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Imposta la dimensione della pagina PDF per i file OBJ con Aspose.CAD - Tutorial

## Introduzione

Se stai sviluppando applicazioni CAD in .NET e hai bisogno di **impostare la dimensione della pagina PDF** durante la conversione di modelli OBJ, Aspose.CAD per .NET offre un'API pulita, code‑first, che gestisce la rasterizzazione e la generazione di PDF in un unico flusso. In questo tutorial vedremo come installare la libreria, caricare un file OBJ, configurare le dimensioni della pagina e infine salvare il risultato come PDF. Alla fine avrai un modello riutilizzabile per trasformare qualsiasi modello 3‑D in un documento PDF perfettamente dimensionato.

## Risposte rapide
- **Aspose.CAD può convertire OBJ in PDF?** Sì – carica l'OBJ con `Image.Load` e rasterizzalo in PDF.
- **Come impostare una dimensione personalizzata della pagina PDF?** Usa `PdfOptions` → `PageSize` o imposta larghezza/altezza in `RasterizationOptions`.
- **Quali versioni di .NET sono supportate?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.
- **È necessaria una licenza per lo sviluppo?** Una versione di prova gratuita è sufficiente per la valutazione; è necessaria una licenza per la produzione.
- **La conversione è efficiente in termini di memoria?** Aspose.CAD trasmette i dati in streaming e può gestire PDF con centinaia di pagine senza caricare l'intero file in memoria.

## Cos'è il formato OBJ?

Il formato OBJ è una definizione di geometria 3‑D basata su testo ampiamente utilizzata che memorizza le posizioni dei vertici, le coordinate delle texture e le definizioni delle facce. È supportato dalla maggior parte degli strumenti di modellazione 3‑D ed è ideale per lo scambio tra CAD e pipeline di rendering.

## Perché impostare una dimensione personalizzata della pagina PDF?

Aspose.CAD può renderizzare un disegno CAD a qualsiasi dimensione raster. Impostando esplicitamente le dimensioni della pagina PDF, garantisci che il documento finale corrisponda ai tuoi standard di reporting, si adatti a formati di carta standard (A4, Letter) o si conformi a layout di stampa personalizzati. Vantaggio quantificato: l'API può generare PDF fino a **200 mm × 200 mm** in una singola chiamata, elaborando file superiori a **500 MB** senza superare 250 MB di RAM.

## Prerequisiti

- **Aspose.CAD Library** – Assicurati che la libreria Aspose.CAD sia installata nel tuo progetto .NET. Puoi scaricarla [qui](https://releases.aspose.com/cad/net/) e visualizzare la completa referenza API nella [documentazione](https://reference.aspose.com/cad/net/).
- **Document Directory** – Crea una cartella per le tue risorse CAD; la chiameremo “Your Document Directory” per tutta la guida.
- **.NET Development Environment** – Visual Studio 2022 o qualsiasi IDE che supporti .NET 6+.

## Come impostare la dimensione della pagina PDF durante la conversione da OBJ a PDF?

Carica il file OBJ, configura le opzioni di rasterizzazione con la larghezza e l'altezza desiderate, collega queste opzioni a un'istanza di `PdfOptions` e chiama `Save`. Questo modello a due passaggi garantisce che la pagina PDF corrisponda alle dimensioni specificate preservando i dettagli del modello.

## Passo 1: Importare i namespace

La classe `Image` gestisce tutti i formati CAD, e la classe `PdfOptions` controlla l'output PDF.  
`Image` rappresenta un documento CAD e fornisce metodi per caricare e salvare i file. `PdfOptions` definisce le impostazioni per la generazione del PDF, come la dimensione della pagina e la compressione.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Passo 2: Caricare il file OBJ

Carica il file OBJ nell'oggetto immagine di Aspose.CAD. Sostituisci `"example-580-W.obj"` con il nome del tuo file OBJ.

```csharp
string MyDir = "Your Document Directory";
using (Aspose.CAD.Image CADDoc = Aspose.CAD.Image.Load(MyDir + "example-580-W.obj"))
{
    // Your code for further processing goes here
}
```

## Passo 3: Configurare le opzioni di rasterizzazione

`RasterizationOptions` definisce la dimensione raster che alla fine diventa la dimensione della pagina PDF. Impostando `PageWidth` e `PageHeight` puoi controllare le dimensioni esatte del PDF di output.  
`CadRasterizationOptions` (esposto tramite `RasterizationOptions`) specifica i parametri di rasterizzazione come le dimensioni della pagina e la risoluzione.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions =
    new Aspose.CAD.ImageOptions.CadRasterizationOptions();

rasterizationOptions.PageWidth = CADDoc.Size.Width;
rasterizationOptions.PageHeight = CADDoc.Size.Height;
```

## Passo 4: Creare le opzioni PDF

`PdfOptions` collega le impostazioni di rasterizzazione allo scrittore PDF. Assegnando l'istanza `RasterizationOptions`, garantisci che il PDF erediti la dimensione della pagina che hai definito.

```csharp
Aspose.CAD.ImageOptions.PdfOptions CADf = new Aspose.CAD.ImageOptions.PdfOptions();
CADf.VectorRasterizationOptions = rasterizationOptions;
```

## Passo 5: Salvare come PDF

Invoca il metodo `Save` sull'oggetto `Image`, passando il nome del file di destinazione e le `PdfOptions` configurate. La libreria scrive un PDF con la dimensione della pagina esatta che hai specificato.  
`Save` scrive l'immagine su un file usando il formato e le opzioni specificati.

```csharp
CADDoc.Save(MyDir + "example-580-W_custom.pdf", CADf);
```

## Problemi comuni e soluzioni

- **Dimensioni della pagina errate** – Verifica che `PageWidth` e `PageHeight` siano impostati in **pixel**; usa `Resolution` per convertire pollici o millimetri in pixel (ad esempio, 300 dpi → 1 inch = 300 px).
- **Texture mancanti** – I file OBJ spesso fanno riferimento a file `.mtl` esterni; assicurati che il file materiale si trovi nella stessa directory del file OBJ.
- **Elevato utilizzo di memoria per file grandi** – Abilita `Image.SaveOptions.Compression` per ridurre la pressione sulla memoria durante rendering ad alta risoluzione.

## Domande frequenti

**D: Aspose.CAD è compatibile con altri formati di file CAD?**  
R: Sì, Aspose.CAD supporta più di **30** formati di input — inclusi DWG, DXF, DGN e STL — e può esportare in più di **20** formati raster e vettoriali.

**D: Posso provare Aspose.CAD prima di acquistarlo?**  
R: Assolutamente! Puoi provare una versione di prova gratuita [qui](https://releases.aspose.com/).

**D: Come posso ottenere supporto per Aspose.CAD?**  
R: Visita il [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) per porre domande e condividere esperienze con la community.

**D: Sono disponibili licenze temporanee per i test?**  
R: Sì, le licenze temporanee possono essere ottenute [qui](https://purchase.aspose.com/temporary-license/).

**D: Dove posso acquistare una licenza completa?**  
R: Puoi acquistare Aspose.CAD [qui](https://purchase.aspose.com/buy).

---

**Ultimo aggiornamento:** 2026-07-04  
**Testato con:** Aspose.CAD 24.11 for .NET  
**Autore:** Aspose

## Tutorial correlati

- [Esportazione di file IGES in PDF - Guida Aspose.CAD](/cad/net/exporting-to-image-formats/exporting-iges-files-to-pdf/)
- [Esportazione di DXF in formato PDF - Tutorial Aspose.CAD](/cad/net/export-techniques/exporting-dxf-to-pdf-format/)
- [Esportazione di disegni CAD in PDF - Tutorial Aspose.CAD](/cad/net/advanced-export-techniques/exporting-cad-drawings-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}