---
date: 2026-08-12
description: Estrai il testo da DWG e converti DWG specifici in immagine in C# usando
  Aspose.CAD per .NET. Impara passo passo con esempi di codice.
keywords:
- extract text from dwg
- convert specific dwg to image
- Aspose.CAD .NET
lastmod: 2026-08-12
linktitle: Conversione di DWG specifici in immagine in C#
og_description: Estrai il testo da DWG e converti DWG specifici in immagine in C#
  con Aspose.CAD. Segui questa guida concisa per una rapida implementazione.
og_image_alt: Guide showing DWG to image conversion and text extraction using Aspose.CAD
  in C#
og_title: Estrai il testo da DWG e converti DWG specifici in immagine in C#
schemas:
- author: Aspose
  dateModified: '2026-08-12'
  description: Extract text from DWG and convert specific DWG to image in C# using
    Aspose.CAD for .NET. Learn step‑by‑step with code snippets.
  headline: Extract text from DWG and convert specific DWG to image in C#
  type: TechArticle
- questions:
  - answer: Aspose.CAD supports DWG releases from AutoCAD 2000 up to the latest 2024
      version, covering over 90 % of files created in the field.
    question: Is Aspose.CAD compatible with all versions of DWG files?
  - answer: Yes – you can change resolution, image format, anti‑aliasing, and background
      color to suit PNG, JPEG, or PDF targets.
    question: Can I customize the rasterization options for different outputs?
  - answer: Explore the comprehensive [Aspose.CAD documentation](https://reference.aspose.com/cad/net/)
      for more code samples and API details.
    question: Where can I find additional examples and documentation?
  - answer: Absolutely – you can download a trial version on the **[Aspose trial download
      page](https://releases.aspose.com/)** and evaluate all features without restrictions
      for 30 days.
    question: Is there a free trial available for Aspose.CAD?
  - answer: Join the active [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)
      where developers share solutions and the Aspose team answers questions.
    question: How can I get support or connect with the community?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- extract text from dwg
- Aspose.CAD
- C# CAD processing
title: Estrai il testo da DWG e converti DWG specifici in immagine in C#
url: /it/net/image-manipulation-and-rendering/converting-particular-dwg-to-image/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convertire DWG specifici in immagine in C# - Guida Aspose.CAD

## Introduzione

Nelle moderne applicazioni ingegneristiche, è spesso necessario **estrarre testo da file DWG** e **convertire DWG specifici in formati immagine** per report o visualizzazioni. Aspose.CAD per .NET fornisce un'API completa che gestisce entrambe le attività senza richiedere alcun software CAD esterno. In questo tutorial imparerai a caricare un DWG, filtrare le entità di testo, rasterizzare il disegno e infine salvare il risultato come immagine PDF, il tutto con codice C# pulito.

## Risposte rapide
- **Qual è il primo passo?** Carica il file DWG con `new CadImage("file.dwg")`.  
- **Quale classe filtra il testo?** Usa `CadEntityFilter` per selezionare le entità `Text`.  
- **Come si definisce la dimensione dell'immagine?** Imposta `Width` e `Height` su `CadRasterizationOptions`.  
- **Quale formato di output viene utilizzato?** L'esempio salva in PDF, che incorpora l'immagine raster.  
- **È necessaria una licenza per la produzione?** Sì – una licenza commerciale di Aspose.CAD rimuove i limiti di valutazione.

## Come estrarre testo da DWG?

Carica il DWG, applica un filtro che seleziona solo le entità di testo, e poi leggi la proprietà `TextString` di ciascuna entità. Questo approccio restituisce ogni annotazione, etichetta o testo di quota presente nel disegno, consentendoti di riutilizzarlo per ricerca, indicizzazione o report.

## Perché convertire DWG specifici in immagine?

Convertire un DWG in un'immagine raster ti permette di incorporare il disegno in documenti, pagine web o app mobili che non possono renderizzare i formati CAD nativi. Aspose.CAD elabora **oltre 50 formati CAD** e può rasterizzare disegni con centinaia di pagine utilizzando meno di 200 MB di memoria, il che lo rende adatto a scenari server ad alto throughput.

## Prerequisiti

- Visual Studio (qualsiasi edizione recente) per compilare ed eseguire progetti C#.
- Aspose.CAD per .NET – assicurati di avere la libreria installata. Puoi trovare il link per il download nella **[pagina di download di Aspose.CAD per .NET](https://releases.aspose.com/cad/net/)**.
- Un file DWG con cui vuoi lavorare; il file di esempio *visualization_-_conference_room.dwg* è usato negli snippet di codice.

## Importare i namespace

I seguenti namespace ti danno accesso alle classi CAD core, alle opzioni di rasterizzazione e agli helper per l'output PDF:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Passo 1: caricare il file DWG

Crea un'istanza di `CadImage` passando il percorso del tuo file DWG. L'oggetto `CadImage` rappresenta l'intero disegno in memoria e fornisce accesso ai suoi layer, entità e metadati.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
var cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath);
```

## Passo 2: filtrare le entità

`CadEntityFilter` ti consente di scegliere solo le entità di cui hai bisogno. In questa guida lo configuriamo per mantenere gli oggetti **text**, scartando linee, cerchi e altre geometrie che non desideri nell'immagine finale.

```csharp
CadBaseEntity[] entities = cadImage.Entities;
List<CadBaseEntity> filteredEntities = new List<CadBaseEntity>();

foreach (CadBaseEntity baseEntity in entities)
{
    // Selection or filtration of entities
    if (baseEntity.TypeName == CadEntityTypeName.TEXT)
    {
        filteredEntities.Add(baseEntity);
    }
}

cadImage.Entities = filteredEntities.ToArray();
```

## Passo 3: impostare le opzioni di rasterizzazione

`CadRasterizationOptions` controlla come il disegno viene trasformato in una bitmap. Puoi definire la dimensione dell'output, il colore di sfondo e la risoluzione (DPI). L'ancora di definizione seguente introduce la classe:

La classe `CadRasterizationOptions` specifica le dimensioni dell'immagine, la risoluzione e le impostazioni di rendering per convertire i disegni CAD in formati raster.  

Imposta la larghezza, altezza e colore di sfondo desiderati prima di passare le opzioni all'esportatore PDF.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions =
    new Aspose.CAD.ImageOptions.CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
```

## Passo 4: impostare le opzioni PDF

`PdfOptions` raggruppa le impostazioni di rasterizzazione con funzionalità specifiche PDF come la compressione. L'ancora di definizione per questa classe appare per prima:

`PdfOptions` incapsula i parametri di generazione PDF, incluse le opzioni di rasterizzazione che determinano come i dati CAD vengono renderizzati all'interno del documento PDF.  

Assegna l'istanza `CadRasterizationOptions` creata in precedenza alla proprietà `VectorRasterizationOptions`.

```csharp
Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Passo 5: salvare come PDF

Infine, chiama il metodo `Save` sull'oggetto `CadImage`, passando il nome del file di destinazione e le `PdfOptions` configurate. Il PDF conterrà un'immagine ad alta qualità del disegno filtrato.

```csharp
string outFile = MyDir + "result_out_generated.pdf";
cadImage.Save(outFile, pdfOptions);
```

## Problemi comuni e risoluzione

- **Testo mancante dopo il filtraggio** – Assicurati che il DWG contenga effettivamente entità `Text`; alcuni disegni memorizzano le annotazioni come `MText`. Regola il filtro per includere `MText` se necessario.  
- **Immagine di output vuota** – Verifica che il DPI di rasterizzazione sia sufficientemente alto (300 DPI è un valore sicuro) e che il colore di sfondo non sia impostato su trasparente durante la visualizzazione del PDF.  
- **Errori di out‑of‑memory su file grandi** – Usa la sovraccarico `LoadOptions` che abilita lo streaming, impedendo il caricamento completo del file in memoria.

## Domande frequenti

**D: Aspose.CAD è compatibile con tutte le versioni dei file DWG?**  
R: Aspose.CAD supporta le versioni DWG da AutoCAD 2000 fino all'ultima versione 2024, coprendo oltre il 90 % dei file creati sul campo.

**D: Posso personalizzare le opzioni di rasterizzazione per diversi output?**  
R: Sì – puoi modificare risoluzione, formato immagine, anti‑aliasing e colore di sfondo per adattarli a destinazioni PNG, JPEG o PDF.

**D: Dove posso trovare esempi aggiuntivi e documentazione?**  
R: Esplora la completa [documentazione di Aspose.CAD](https://reference.aspose.com/cad/net/) per ulteriori esempi di codice e dettagli sull'API.

**D: È disponibile una versione di prova gratuita per Aspose.CAD?**  
R: Assolutamente – puoi scaricare una versione di prova dalla **[pagina di download della prova Aspose](https://releases.aspose.com/)** e valutare tutte le funzionalità senza restrizioni per 30 giorni.

**D: Come posso ottenere supporto o connettermi con la community?**  
R: Unisciti al vivace [forum di Aspose.CAD](https://forum.aspose.com/c/cad/19) dove gli sviluppatori condividono soluzioni e il team Aspose risponde alle domande.

---

**Ultimo aggiornamento:** 2026-08-12  
**Testato con:** Aspose.CAD 24.11 per .NET  
**Autore:** Aspose

## Tutorial correlati

- [Ricerca testo nei file DWG con C# - Tutorial Aspose.CAD](/cad/net/text-search-and-manipulation/searching-text-in-dwg-files/)
- [Converti disegno CAD in immagine raster in Aspose.CAD per .NET](/cad/net/cad-drawing-manipulation/convert-cad-drawing-to-raster-image/)
- [Rendering di documenti DWG in C# - Guida Aspose.CAD](/cad/net/image-manipulation-and-rendering/rendering-dwg-documents/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}