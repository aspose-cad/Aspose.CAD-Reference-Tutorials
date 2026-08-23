---
date: 2026-08-23
description: Scopri come creare un viewport DWG C# utilizzando Aspose.CAD. Questa
  guida copre il caricamento di un file DWG, la configurazione della rasterizzazione,
  la definizione di un viewport e il salvataggio del risultato in PDF.
keywords:
- create viewport dwg c#
- render dwg c#
- aspose.cad .net
lastmod: 2026-08-23
linktitle: Rendering di documenti DWG in C#
og_description: Scopri come creare un viewport DWG C# utilizzando Aspose.CAD in .NET.
  Questa guida passo‑passo mostra il caricamento, la rasterizzazione, la definizione
  dei viewport e il salvataggio in PDF.
og_image_alt: Guide showing how to create viewport dwg c# with Aspose.CAD in .NET
og_title: Come creare un viewport DWG C# con Aspose.CAD per .NET
schemas:
- author: Aspose
  dateModified: '2026-08-23'
  description: Learn how to create viewport dwg c# using Aspose.CAD. This guide covers
    loading a DWG file, configuring rasterization, defining a viewport, and saving
    the result as PDF.
  headline: How to create viewport dwg c# with Aspose.CAD for .NET
  type: TechArticle
- questions:
  - answer: Load the DWG file with `CadImage.Load`.
    question: What is the first step?
  - answer: '`Viewport` inside `CadRasterizationOptions`.'
    question: Which class defines the view area?
  - answer: Yes, using `PdfOptions` after rasterization.
    question: Can I output to PDF?
  - answer: A commercial license is required; a free trial works for evaluation.
    question: Do I need a license for production?
  - answer: Absolutely – Aspose.CAD works with .NET Framework, .NET Core, and .NET 5/6.
    question: Is .NET Core supported?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- create viewport dwg c#
- Aspose.CAD
- C# CAD rendering
- DWG to PDF
- CAD viewports
title: Come creare un viewport DWG C# con Aspose.CAD per .NET
url: /it/net/image-manipulation-and-rendering/rendering-dwg-documents/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Rendering di documenti DWG in C# – tutorial per creare viewport dwg c# 

## Introduzione

In questo tutorial completo imparerai a **create viewport dwg c#** con Aspose.CAD e a renderizzare un file DWG in PDF. Che tu debba estrarre un layout specifico, generare un foglio stampabile o incorporare una vista CAD in un report, controllare il viewport ti offre un controllo preciso del rendering. Aspose.CAD supporta **20+ formati CAD** e può elaborare file con migliaia di entità senza caricare l'intero documento in memoria, rendendolo ideale per applicazioni .NET ad alte prestazioni.

## Risposte rapide
- **Qual è il primo passo?** Carica il file DWG con `CadImage.Load`.
- **Quale classe definisce l'area di visualizzazione?** `Viewport` all'interno di `CadRasterizationOptions`.
- **Posso esportare in PDF?** Sì, usando `PdfOptions` dopo la rasterizzazione.
- **È necessaria una licenza per la produzione?** È richiesta una licenza commerciale; una versione di prova gratuita è sufficiente per la valutazione.
- **È supportato .NET Core?** Assolutamente – Aspose.CAD funziona con .NET Framework, .NET Core e .NET 5/6.

## Prerequisiti

Prima di immergerti nel codice, assicurati di avere:

- Conoscenza di base della programmazione C#.
- Visual Studio (qualsiasi versione recente) installato.
- Libreria Aspose.CAD aggiunta al tuo progetto. Puoi scaricarla dalla [Aspose.CAD download page](https://releases.aspose.com/cad/net/).
- Un file DWG di esempio, ad esempio **Bottom_plate.dwg**, per seguire il tutorial.

## Importare i namespace

Aggiungi le direttive `using` richieste all'inizio del tuo file C# in modo che il compilatore possa individuare i tipi Aspose.CAD.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.FileFormats.Cad;
```

Ora che l'ambiente è pronto, procediamo passo per passo attraverso l'implementazione.

## Come creare viewport dwg c#?

Per creare un viewport personalizzato, prima carica il file DWG in un oggetto `CadImage`, quindi configura `CadRasterizationOptions` con il layout e la scala desiderati. Definisci la regione da visualizzare, istanzia un `CadVportTableObject` con il centro, l'altezza e il rapporto d'aspetto calcolati, sostituisci il viewport attivo, imposta le opzioni PDF e infine salva il risultato.

## Passo 1: caricare il file dwg

`CadImage.Load` carica un file DWG in un oggetto `CadImage`, che rappresenta il disegno CAD in memoria.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for loading the DWG file goes here.
}
```

## Passo 2: configurare le opzioni di rasterizzazione

`CadRasterizationOptions` specifica come il disegno CAD viene rasterizzato, includendo la selezione del layout, la scala e le dimensioni di output.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };
rasterizationOptions.NoScaling = true;
// Additional rasterization configurations can be added here.
```

## Passo 3: definire la regione da disegnare

`Point` definisce le coordinate X e Y dell'angolo superiore sinistro della regione da renderizzare.

```csharp
Point topLeft = new Point(6156, 7053);
double width = 3108;
double height = 2489;
```

## Passo 4: creare un nuovo viewport

`CadVportTableObject` rappresenta un oggetto viewport che controlla l'area visibile e il rapporto d'aspetto del disegno renderizzato.

```csharp
CadVportTableObject newView = new CadVportTableObject();
newView.Name.Value = "*Active";
newView.CenterPoint.X = topLeft.X + width / 2f;
newView.CenterPoint.Y = topLeft.Y - height / 2f;
newView.ViewHeight.Value = height;
newView.ViewAspectRatio.Value = width / height;
```

## Passo 5: sostituire il viewport attivo

Il ciclo sostituisce il viewport attivo con quello appena creato per applicare le impostazioni di visualizzazione personalizzate.

```csharp
for (int i = 0; i < cadImage.ViewPorts.Count; i++)
{
    CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
    if ((currentView.Name.Value == null && cadImage.ViewPorts.Count == 1) ||
    string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
    {
        cadImage.ViewPorts[i] = newView;
        break;
    }
}
```

## Passo 6: configurare le opzioni PDF

`PdfOptions` configura i parametri di output PDF come compressione e metadati.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Passo 7: salvare il DWG renderizzato come PDF

`image.Save` scrive l'immagine renderizzata su un file usando le opzioni di formato specificate.

```csharp
cadImage.Save(MyDir, pdfOptions);
```

## Perché usare un viewport personalizzato durante il rendering di DWG?

Un viewport personalizzato ti consente di isolare un layout o una regione specifica, riducendo la dimensione del file e migliorando la velocità di rendering. Aspose.CAD può renderizzare un DWG di 300 pagine in meno di 2 secondi quando viene usato un viewport mirato, rispetto al rendering dell'intero disegno che può richiedere diversi secondi in più.

## Problemi comuni e soluzioni

- **Output vuoto** – Assicurati che le coordinate del viewport siano entro i limiti del disegno; usa `CadImage.Size` per verificare i confini.
- **Layer mancanti** – Imposta `CadRasterizationOptions.Layouts` sul nome del layout corretto; altrimenti il layout predefinito potrebbe essere vuoto.
- **Rallentamento delle prestazioni** – Disabilita l'anti‑aliasing in `CadRasterizationOptions` se ti serve solo un'anteprima rapida.

## Domande frequenti

### Q1: Posso usare Aspose.CAD con altri formati di file CAD?

A1: Sì, Aspose.CAD supporta vari formati, inclusi DWG, DXF, DWF e più di 20 altri tipi CAD.

### Q2: Aspose.CAD è compatibile con .NET Core?

A2: Sì, Aspose.CAD funziona con .NET Framework, .NET Core e le ultime versioni di .NET.

### Q3: Come posso gestire diversi layout in un file DWG?

A3: Specifica il layout desiderato usando la proprietà `Layouts` di `CadRasterizationOptions` prima del rendering.

### Q4: Ci sono considerazioni di licenza per l'uso di Aspose.CAD?

A4: Per i dettagli sulla licenza, visita la [Aspose.CAD licensing page](https://purchase.aspose.com/buy).

### Q5: Dove posso trovare supporto aggiuntivo?

A5: Visita il [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) per aiuto e discussioni della community.

### Q6: Posso renderizzare direttamente in PNG invece di PDF?

A6: Sì, cambia `PdfOptions` in `PngOptions` e chiama `image.Save("output.png", pngOptions)`.

### Q7: Come incorporare l'immagine renderizzata in un'applicazione Windows Forms?

A7: Carica l'immagine salvata in un controllo `PictureBox` usando `Image.FromFile("output.png")`.

## Conclusione

Ora sai come **create viewport dwg c#** e renderizzare un file DWG in PDF (o altri formati raster) usando Aspose.CAD. Conoscendo la manipolazione del viewport ottieni un controllo dettagliato sull'output visivo, essenziale per generare disegni ingegneristici accurati, report o miniature. Esplora impostazioni di rasterizzazione aggiuntive, sperimenta con diversi formati di output e integra il codice in servizi .NET più grandi o utility desktop.

---

**Ultimo aggiornamento:** 2026-08-23  
**Testato con:** Aspose.CAD 24.11 per .NET  
**Autore:** Aspose

## Tutorial correlati

- [Come impostare il viewport durante la conversione di DWG in PDF con coordinate in C# - Tutorial Aspose.CAD](/cad/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/)
- [Impara a impostare le opzioni di rasterizzazione CAD – Esporta layout specifici in PDF con Aspose.CAD](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)
- [Come convertire DWG in PDF e immagini raster usando Aspose.CAD per .NET](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}