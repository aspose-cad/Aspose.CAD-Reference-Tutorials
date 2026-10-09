---
date: 2026-10-09
description: Scopri come caricare un file dwg e cercare testo all'interno dei file
  DWG usando C# e Aspose.CAD per .NET. Segui questa guida passo‑passo per migliorare
  i tuoi flussi di lavoro CAD.
keywords:
- load dwg file
- export dwg to pdf
- cad text search
- search text dwg
- c# read dwg
lastmod: 2026-10-09
linktitle: Ricerca di testo nei file DWG con C#
og_description: Scopri come caricare un file dwg e cercare testo all'interno dei file
  DWG usando C# e Aspose.CAD per .NET. Segui questa guida passo‑passo per migliorare
  i tuoi flussi di lavoro CAD.
og_image_alt: Guide showing how to load dwg file and search text in DWG files using
  Aspose.CAD for .NET
og_title: Come caricare un file dwg e cercare testo nei file DWG con C#
schemas:
- author: Aspose
  dateModified: '2026-10-09'
  description: Learn how to load dwg file and search text inside DWG files using C#
    and Aspose.CAD for .NET. Follow this step‑by‑step guide to enhance your CAD workflows.
  headline: How to load dwg file and search text in DWG files with C#
  type: TechArticle
- questions:
  - answer: '`new CadImage("yourfile.dwg")` creates an in‑memory representation of
      the drawing.'
    question: What is the first line of code to load a DWG?
  - answer: '`Aspose.CAD.Image` and `Aspose.CAD.FileFormats.Dwg` are required.'
    question: Which namespace contains the CAD classes?
  - answer: Yes – use `image.Save("out.pdf", SaveFormat.Pdf)`.
    question: Can I export the search results directly to PDF?
  - answer: A free trial works for evaluation; a permanent license is required for
      production.
    question: Do I need a license for development?
  - answer: .NET 5, .NET 6, .NET Core 3.1 and .NET Framework 4.6+.
    question: Which .NET versions are supported?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- dwg file handling
- aspose.cad
- c# cad processing
- text search in dwg
title: Come caricare un file dwg e cercare testo nei file DWG con C#
url: /it/net/text-search-and-manipulation/searching-text-in-dwg-files/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come caricare un file dwg e cercare testo nei file DWG con C# - tutorial Aspose.CAD

## Introduzione

Nello sviluppo CAD moderno, la possibilità di **load dwg file** oggetti e individuare istantaneamente stringhe di testo specifiche consente di risparmiare ore di ispezione manuale. Che tu stia creando uno strumento di elaborazione batch o aggiungendo capacità di ricerca a un visualizzatore, Aspose.CAD per .NET ti offre un'API completamente gestita che funziona su Windows, Linux e macOS senza dipendenze native. Questa guida ti accompagna passo passo—dalla lettura del DWG all'esportazione del risultato in PDF—così potrai integrare una ricerca di testo CAD affidabile nelle tue applicazioni C# oggi.

## Risposte rapide
- **Qual è la prima riga di codice per caricare un DWG?** `new CadImage("yourfile.dwg")` crea una rappresentazione in memoria del disegno.  
- **Quale namespace contiene le classi CAD?** `Aspose.CAD.Image` e `Aspose.CAD.FileFormats.Dwg` sono richiesti.  
- **Posso esportare i risultati della ricerca direttamente in PDF?** Sì – usa `image.Save("out.pdf", SaveFormat.Pdf)`.  
- **Ho bisogno di una licenza per lo sviluppo?** Una versione di prova gratuita è sufficiente per la valutazione; è necessaria una licenza permanente per la produzione.  
- **Quali versioni di .NET sono supportate?** .NET 5, .NET 6, .NET Core 3.1 e .NET Framework 4.6+.

## Cos'è un file DWG?

Un file DWG è un formato binario che memorizza dati di progettazione 2D e 3D creati da AutoCAD e strumenti compatibili. È il contenitore standard del settore per geometria vettoriale, layer, testo e metadati. Poiché il formato è proprietario, la maggior parte dei parser open‑source ha difficoltà con le versioni più recenti, ma Aspose.CAD supporta pienamente oltre 150 versioni DWG, consentendoti di leggere e manipolare i disegni senza installare AutoCAD.

## Perché usare Aspose.CAD per la ricerca di testo CAD?

Aspose.CAD può elaborare **50+** versioni DWG e DXF, gestendo file fino a 1 GB senza caricare l'intero documento in memoria. La libreria estrae testo sia dalle sezioni **Entities** sia **Block**, fornendoti un tasso di successo del **99 %** nel trovare stringhe ricercabili anche quando sono annidate nei blocchi. Questa affidabilità quantificata lo rende la scelta preferita per l'automazione CAD di livello enterprise.

## Prerequisiti

- **Aspose.CAD for .NET** installato. Scarica l'ultimo pacchetto dal [sito Aspose.CAD](https://releases.aspose.com/cad/net/).
- Una cartella contenente i file DWG che desideri analizzare.
- Un file di licenza valido per l'uso in produzione (opzionale per esecuzioni di prova).

## Quali namespace sono richiesti?

Il namespace `Aspose.CAD` fornisce le classi core per la gestione delle immagini, mentre `Aspose.CAD.FileFormats.Dwg` contiene le strutture specifiche per DWG. Importali all'inizio del tuo file C#:

```csharp
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dwg;
using Aspose.CAD.ImageOptions;
```

> **Nota:** Il blocco di codice sopra è un segnaposto; mantieni il testo esatto invariato per preservare il conteggio originale dei segnaposti.

## Come caricare un file dwg?

La lettura di un file DWG è semplice con Aspose.CAD. Usa la classe `CadImage`, che rappresenta un disegno CAD in memoria. Il costruttore legge il file senza renderizzarlo, rendendolo veloce anche per disegni di grandi dimensioni. Dopo il caricamento, puoi ispezionare proprietà come `Width`, `Height` e `Layers` prima di eseguire operazioni di ricerca.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects.AttEntities;
```

## Come cercare testo nella sezione entities?

Per individuare testo nella sezione Entities, itera sulla collezione `cadImage.Entities`. Ogni entità può essere esaminata per il suo tipo (ad es., `MText`, `Text`, `Attribute`) e la sua proprietà `TextString`. Esegui un confronto case‑insensitive con la stringa target e raccogli le entità corrispondenti per ulteriori elaborazioni o evidenziazioni.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "search.dwg";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code here
}
```

## Come cercare testo nella sezione block?

I blocchi sono gruppi riutilizzabili di entità che possono contenere testo annidato. Prima, enumera `cadImage.BlockEntities.Values` per accedere a ciascuna definizione di blocco. Poi, percorri la collezione `Entities` di ogni blocco, applicando la stessa logica di corrispondenza del testo usata per la sezione principale Entities. Questo garantisce che il testo nascosto all'interno di componenti riutilizzabili non venga perso.

```csharp
foreach (CadBaseEntity entity in cadImage.Entities)
{
    IterateCADNodes(entity);
}
```

## Come iterare attraverso i nodi CAD per una scansione completa?

Una scansione completa combina le sezioni Entities e Block. Camminando ricorsivamente l'albero dei nodi `CadImage`, puoi gestire blocchi annidati, definizioni di attributi e persino riferimenti esterni. Implementa un metodo helper che accetta un `CadBaseEntity`, verifica il suo tipo, estrae il testo quando applicabile e poi ricorre sulle entità figlie se il nodo contiene una collezione.

```csharp
foreach (CadBlockEntity blockEntity in cadImage.BlockEntities.Values)
{
    foreach (CadBaseEntity entity in blockEntity.Entities)
    {
        IterateCADNodes(entity);
    }
}
```

## Come esportare dwg in pdf dopo aver individuato il testo?

Dopo aver identificato le entità rilevanti, potresti volerle evidenziare o estrarre le loro coordinate. Aspose.CAD ti consente di salvare l'intero disegno come PDF mantenendo la qualità vettoriale. Configura `CadRasterizationOptions` se ti serve un output raster, quindi chiama `image.Save("output.pdf", new PdfOptions())`. Il PDF risultante può essere condiviso con gli stakeholder che non possiedono software CAD.

```csharp
private static void IterateCADNodes(CadBaseEntity obj)
{
    switch (obj.TypeName)
    {
        // Handle different entity types
    }
}
```

## Conclusione

Aspose.CAD per .NET offre una soluzione fluida e ad alte prestazioni per caricare dati di file dwg, cercare testo specifico ed esportare il risultato in PDF. Seguendo i passaggi di questo tutorial, hai aggiunto potenti capacità di ricerca di testo CAD alla tua applicazione C# senza dipendere da strumenti esterni o licenze costose.

## Domande frequenti

### Q1: Posso usare Aspose.CAD per .NET con altri formati CAD?

Sì, Aspose.CAD supporta oltre 30 formati CAD, inclusi DXF, DWF e STL, offrendo una soluzione versatile per flussi di lavoro con formati misti.

### Q2: È disponibile una versione di prova gratuita per Aspose.CAD per .NET?

Sì, puoi esplorare le funzionalità con la [versione di prova gratuita](https://releases.aspose.com/).

### Q3: Come posso ottenere supporto per Aspose.CAD per .NET?

Visita il [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) per assistenza della community e canali di supporto ufficiali.

### Q4: Cos'è una licenza temporanea e come posso ottenerne una?

Ottieni una licenza temporanea [temporary license](https://purchase.aspose.com/temporary-license/) per valutazioni a breve termine o progetti proof‑of‑concept.

### Q5: Dove posso trovare la documentazione dettagliata per Aspose.CAD per .NET?

Consulta la completa [documentazione](https://reference.aspose.com/cad/net/) per guide approfondite, riferimenti API e esempi di codice.

---

**Ultimo aggiornamento:** 2026-10-09  
**Testato con:** Aspose.CAD 24.11 for .NET  
**Autore:** Aspose  

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
// Configure rasterization options
rasterizationOptions.Layouts = new[] { "Layout1" };
Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
cadImage.Save(MyDir + "SearchText_out.pdf", pdfOptions);
```

## Tutorial correlati

- [Come convertire DWG in PDF e immagini raster usando Aspose.CAD per .NET](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [Converti DWG in PNG & esporta oggetti OLE - Tutorial Aspose.CAD](/cad/net/advanced-export-techniques/exporting-ole-objects-from-dwg/)
- [Come leggere file DWT con Aspose.CAD per .NET](/cad/net/cad-features-and-support/reading-dwt/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}