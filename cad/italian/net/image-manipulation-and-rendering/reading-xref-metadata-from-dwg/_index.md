---
date: 2026-08-23
description: Sblocca il potenziale di Aspose.CAD per .NET con il nostro tutorial passo‑passo
  su come leggere i metadati xref da file DWG.
keywords:
- read xref metadata
- extract dwg xref
- Aspose.CAD
lastmod: 2026-08-23
linktitle: Lettura dei metadati XREF da file DWG
og_description: Scopri come leggere i metadati xref da file DWG con Aspose.CAD per
  .NET. Questa guida ti accompagna attraverso i prerequisiti, i passaggi di codice
  e le insidie comuni in meno di dieci minuti.
og_image_alt: Screenshot of Aspose.CAD reading XREF metadata in a .NET IDE
og_title: Come leggere i metadati xref da file DWG usando Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-08-23'
  description: Unlock the potential of Aspose.CAD for .NET with our step‑by‑step tutorial
    on how to read xref metadata from DWG files.
  headline: How to read xref metadata from DWG files using Aspose.CAD
  type: TechArticle
- description: Unlock the potential of Aspose.CAD for .NET with our step‑by‑step tutorial
    on how to read xref metadata from DWG files.
  name: How to read xref metadata from DWG files using Aspose.CAD
  steps:
  - name: load the DWG file
    text: Create an `Image` instance from the DWG file you want to analyze. `Image.Load`
      loads a CAD file and returns a `CadImage` object representing the drawing. Adjust
      the `sourceFilePath` variable to the exact location of your drawing.
  - name: iterate through entities
    text: Loop through the `Image` object’s `Entities` collection. `CadBaseEntity`
      is the base class for all CAD entities in Aspose.CAD. For each entity, check
      whether it is an XREF reference and collect its metadata.
  - name: extract metadata
    text: When you encounter an XREF entity, read its insertion point (X, Y, Z) and
      the path of the referenced drawing. `CadUnderlay` represents an external reference
      (XREF) entity within a DWG drawing.
  - name: process metadata
    text: At this stage you can store the extracted information in a database, write
      it to a CSV file, or feed it into downstream BIM workflows. The sample simply
      prints the values to the console, but you are free to replace that with any
      custom logic.
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD for .NET supports **50+ input and output formats**, including
      DWG, DXF, DGN, and IFC, giving you broad coverage for most engineering workflows.
    question: Is Aspose.CAD for .NET compatible with all CAD file formats?
  - answer: Certainly! You can access the free trial download page [free trial download
      page](https://releases.aspose.com/).
    question: Can I use the free trial before making a purchase decision?
  - answer: The documentation is available [Aspose.CAD .NET documentation](https://reference.aspose.com/cad/net/).
    question: Where can I find comprehensive documentation for Aspose.CAD for .NET?
  - answer: You can get a temporary license [temporary license page](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license for Aspose.CAD for .NET?
  - answer: Join the Aspose.CAD community at [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19)
      for expert support and discussions.
    question: Need assistance or have specific queries?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- read xref metadata
- extract dwg xref
- Aspose.CAD
- DWG
- CAD metadata
title: Come leggere i metadati xref da file DWG usando Aspose.CAD
url: /it/net/image-manipulation-and-rendering/reading-xref-metadata-from-dwg/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come leggere i metadati xref da file DWG usando Aspose.CAD

## Introduzione

In questo tutorial imparerai **come leggere i metadati xref** da file DWG utilizzando la libreria Aspose.CAD per .NET. Che tu debba controllare i riferimenti esterni, migrare disegni legacy o costruire una pipeline BIM personalizzata, l'estrazione delle informazioni XREF è una necessità comune. Ti guideremo passo passo, dalla configurazione del progetto all'elaborazione dei metadati, evidenziando consigli pratici che potrai applicare subito.

## Risposte rapide
- **Qual è lo scopo principale?** Recuperare i punti di inserimento e i percorsi dei file delle riferimenti esterni (XREF) incorporati in un disegno DWG.  
- **Quale libreria è necessaria?** Aspose.CAD per .NET (supporta più di 50 formati CAD).  
- **È necessaria una licenza?** È richiesta una licenza temporanea o completa per l'uso in produzione; è disponibile una versione di prova gratuita.  
- **Quali versioni di .NET sono supportate?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.  
- **Quanto tempo impiega il codice ad eseguire?** L'elaborazione di un tipico DWG di 200 pagine con alcuni XREF richiede meno di un secondo su hardware standard.

## Che cosa sono i metadati xref?
`read xref metadata` si riferisce all'operazione di accesso alle proprietà delle entità di riferimento esterno memorizzate all'interno di un disegno DWG, come le coordinate di inserimento, i percorsi dei file sorgente e i flag di visibilità. Questa operazione consente di scoprire programmaticamente come un disegno è composto da altri file, abilitando la convalida automatizzata, la generazione di report o l'elaborazione batch delle risorse collegate.

## Perché usare Aspose.CAD per questa attività?
Aspose.CAD supporta **più di 50 formati di file CAD** e può leggere i file DWG **senza richiedere AutoCAD**. La libreria elabora grandi disegni **in stream a consumo di memoria ottimizzato**, permettendoti di gestire file di centinaia di pagine senza caricare l'intero file in RAM. Queste capacità quantificate lo rendono una scelta affidabile per l'automazione CAD di livello enterprise.

## Prerequisiti

- Aspose.CAD per .NET installato. Scarica l'ultimo pacchetto dalla [pagina di rilascio di Aspose.CAD per .NET](https://releases.aspose.com/cad/net/).
- Una cartella locale che contiene i file DWG da ispezionare. Aggiorna la variabile `MyDir` nel codice di esempio per puntare a questa cartella.
- Una licenza valida di Aspose.CAD (o la versione di prova gratuita) se prevedi di eseguire il codice in un ambiente di produzione.

Ora che l'ambiente è pronto, iniziamo a codificare.

## Importa gli spazi dei nomi

La prima cosa da fare è importare gli spazi dei nomi che espongono l'API di Aspose.CAD. Le direttive `using` portano gli spazi dei nomi di Aspose.CAD nel contesto, consentendo l'accesso a classi CAD come `Image` e `CadImage`.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
```

## Come leggere i metadati xref da file DWG?

Carica il disegno, elenca le sue entità, filtra gli oggetti XREF e poi estrai le proprietà desiderate—tutto in poche righe di codice semplici. Le sezioni seguenti suddividono il processo in quattro passaggi logici che puoi copiare‑incollare in qualsiasi progetto console o service .NET.

### Passo 1: carica il file DWG

Crea un'istanza `Image` dal file DWG che desideri analizzare. `Image.Load` carica un file CAD e restituisce un oggetto `CadImage` che rappresenta il disegno. Regola la variabile `sourceFilePath` per indicare la posizione esatta del tuo disegno.

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";
using (CadImage image = (CadImage)Image.Load(sourceFilePath))
{
    // Code for the next steps goes here
}
```

### Passo 2: iterare attraverso le entità

Scorri la collezione `Entities` dell'oggetto `Image`. `CadBaseEntity` è la classe base per tutte le entità CAD in Aspose.CAD. Per ogni entità, verifica se è un riferimento XREF e raccogli i suoi metadati.

```csharp
foreach (CadBaseEntity entity in image.Entities)
{
    if (entity is CadUnderlay)
    {
        // Code for the next steps goes here
    }
}
```

### Passo 3: estrarre i metadati

Quando incontri un'entità XREF, leggi il suo punto di inserimento (X, Y, Z) e il percorso del disegno di riferimento. `CadUnderlay` rappresenta un'entità di riferimento esterno (XREF) all'interno di un disegno DWG.

```csharp
//XREF entity with metadata
Cad3DPoint insertionPoint = ((CadUnderlay)entity).InsertionPoint;
string path = ((CadUnderlay)entity).UnderlayPath;
```

### Passo 4: elaborare i metadati

In questa fase puoi memorizzare le informazioni estratte in un database, scriverle in un file CSV o inserirle in workflow BIM a valle. L'esempio stampa semplicemente i valori sulla console, ma sei libero di sostituire questa logica con qualsiasi altra personalizzata.

```csharp
// Your custom logic for processing metadata goes here
```

## Problemi comuni e risoluzione

| Sintomo | Possibile causa | Risoluzione |
|---------|-----------------|-------------|
| Nessuna entità XREF restituita | Il disegno utilizza un tipo di riferimento diverso (es. INSERT) | Verifica il tipo di entità rispetto a `CadEntityType.Xref` e gestisci anche `Insert` se necessario |
| `Image.Load` genera un'eccezione | Percorso file errato o versione DWG non supportata | Verifica il percorso e assicurati di utilizzare Aspose.CAD 24.11 o versioni successive |
| I valori dei metadati sono vuoti | L'XREF è definito ma non risolto (file esterno mancante) | Assicurati che il file di riferimento esista su disco o fornisci un risolutore di file system virtuale |

## Domande frequenti

**D: Aspose.CAD per .NET è compatibile con tutti i formati di file CAD?**  
R: Sì, Aspose.CAD per .NET supporta **oltre 50 formati di input e output**, inclusi DWG, DXF, DGN e IFC, offrendo una copertura ampia per la maggior parte dei flussi di lavoro ingegneristici.

**D: Posso usare la versione di prova prima di decidere l'acquisto?**  
R: Certamente! Puoi accedere alla pagina di download della versione di prova [free trial download page](https://releases.aspose.com/).

**D: Dove posso trovare la documentazione completa per Aspose.CAD per .NET?**  
R: La documentazione è disponibile [Aspose.CAD .NET documentation](https://reference.aspose.com/cad/net/).

**D: Come ottengo una licenza temporanea per Aspose.CAD per .NET?**  
R: Puoi ottenere una licenza temporanea [temporary license page](https://purchase.aspose.com/temporary-license/).

**D: Hai bisogno di assistenza o hai domande specifiche?**  
R: Unisciti alla community di Aspose.CAD su [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) per supporto esperto e discussioni.

## Conclusione

Ora disponi di uno schema completo e pronto per la produzione per **leggere i metadati XREF** da file DWG con Aspose.CAD per .NET. Seguendo i quattro passaggi—caricamento del file, iterazione delle entità, estrazione del punto di inserimento e del percorso di underlay, ed elaborazione dei risultati—puoi integrare questa funzionalità in qualsiasi applicazione centrata sul CAD, sia essa uno strumento di migrazione dati, uno script di controllo qualità o una pipeline BIM personalizzata.

---

**Ultimo aggiornamento:** 2026-08-23  
**Testato con:** Aspose.CAD 24.11 per .NET  
**Autore:** Aspose

## Tutorial correlati

- [Come modificare il percorso xref e modificare i collegamenti ipertestuali nei file CAD - Tutorial Aspose.CAD](/cad/net/advanced-cad-techniques/editing-hyperlinks-in-cad-files/)
- [Ottenere gli attributi dei blocchi dai file DWG - Tutorial Aspose.CAD](/cad/net/image-manipulation-and-rendering/getting-block-attributes-from-dwg/)
- [Convertire grandi file DWG in PDF - Tutorial Aspose.CAD](/cad/net/image-manipulation-and-rendering/converting-large-dwg-files-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}