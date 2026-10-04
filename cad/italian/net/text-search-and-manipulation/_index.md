---
date: 2026-10-04
description: Scopri come cercare testo nei file DWG usando C# e Aspose.CAD per .NET.
  Estrai testo, leggi i file DWG e potenzia le tue applicazioni CAD.
keywords:
- search text in dwg
- extract text from dwg
- c# read dwg file
- how to search dwg files
lastmod: 2026-10-04
linktitle: Ricerca e manipolazione del testo
og_description: Cerca testo nei file DWG usando C# e Aspose.CAD per .NET. Estrai testo,
  leggi i file DWG e migliora le prestazioni dell'app CAD.
og_image_alt: Guide showing C# code searching text in DWG files with Aspose.CAD
og_title: Cerca testo nei file DWG con C# usando Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-10-04'
  description: Learn how to search text in DWG files using C# and Aspose.CAD for .NET.
    Extract text, read DWG files, and boost your CAD applications.
  headline: Search text in DWG files with C# using Aspose.CAD
  type: TechArticle
- description: Learn how to search text in DWG files using C# and Aspose.CAD for .NET.
    Extract text, read DWG files, and boost your CAD applications.
  name: Search text in DWG files with C# using Aspose.CAD
  steps:
  - name: install the Aspose.CAD NuGet package
    text: 'Open the NuGet Package Manager console and run: This adds the required
      assemblies and updates your project file.'
  - name: open the DWG file
    text: Create a `CadImage` instance by calling `Image.Load`. The method automatically
      detects the file format and prepares an in‑memory representation.
  - name: enumerate text fragments
    text: '`image.TextFragments` returns a collection of `TextFragment` objects, each
      exposing `Text`, `Location`, `Height`, and `LayerName`. You can iterate or LINQ‑filter
      this collection.'
  - name: apply your search criteria
    text: Use `String.Contains`, `Regex.IsMatch`, or any custom predicate to locate
      the exact text you need. For case‑insensitive searches, call `ToLowerInvariant()`
      on both sides.
  - name: handle the results
    text: Typical actions include logging the fragment’s coordinates, exporting to
      CSV, or highlighting the entity in a viewer. Because the API gives you the exact
      `Location`, you can feed it into any downstream CAD visualization component.
  type: HowTo
- questions:
  - answer: Yes. Provide the password via `CadLoadOptions.Password` when calling `Image.Load`.
    question: Can I search for text in password‑protected DWG files?
  - answer: Absolutely. Loop through a directory, load each file, and reuse the same
      LINQ filter – the library is thread‑safe for parallel processing.
    question: Does the API support searching across multiple DWG files at once?
  - answer: Aspose.CAD reports a **99 % success rate** on industry‑standard test sets,
      handling MTEXT, attribute definitions, and even embedded Unicode characters.
    question: How accurate is the text extraction for complex annotations?
  - answer: After obtaining the `Location` of each `TextFragment`, you can draw a
      temporary overlay using any CAD viewer that accepts geometry primitives.
    question: Is there a way to highlight found text in a viewer?
  - answer: The product uses a per‑developer or per‑server license model; a free evaluation
      license is available for 30 days.
    question: What licensing model applies to Aspose.CAD?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- CAD processing
- Aspose.CAD
- .NET
- DWG text search
title: Cerca testo nei file DWG con C# usando Aspose.CAD
url: /it/net/text-search-and-manipulation/
weight: 28
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cerca testo nei file DWG con C# usando Aspose.CAD

## Introduzione

In questo tutorial imparerai a **cercare testo nei file DWG** con C# utilizzando la potente libreria Aspose.CAD per .NET. Che tu debba individuare annotazioni, estrarre valori di attributi o creare un indice ricercabile, i passaggi seguenti ti guideranno attraverso una soluzione affidabile e ad alte prestazioni che funziona sia su .NET Framework sia su .NET Core.

## Risposte rapide
- **Quale libreria gestisce la ricerca di testo DWG?** Aspose.CAD per .NET.  
- **Posso estrarre testo da DWG?** Sì – l'API restituisce stringhe di testo semplice per qualsiasi entità trovata.  
- **Quali versioni .NET sono supportate?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.  
- **Ho bisogno di una licenza per lo sviluppo?** Una licenza temporanea gratuita funziona per la valutazione; è necessaria una licenza completa per la produzione.  
- **L'operazione è efficiente in termini di memoria?** Sì, Aspose.CAD elabora i file in modalità stream, consentendo la gestione di DWG con centinaia di pagine senza caricare l'intero file in RAM.

## Che cos'è la ricerca di testo in DWG?

CadImage è l'oggetto di Aspose.CAD che rappresenta un disegno CAD caricato, esponendo le sue entità come frammenti di testo.  
TextFragment rappresenta un singolo pezzo di testo estratto, includendo il suo contenuto e la posizione geometrica.  

L'espressione *cerca testo in DWG* si riferisce al localizzare programmaticamente dati stringa — come nomi di layer, valori di attributi o testo di annotazione — all'interno di un file di disegno DWG. Aspose.CAD espone questa capacità tramite l'oggetto `CadImage` e la collezione `TextFragment`, consentendo agli sviluppatori di recuperare e manipolare il testo in modo efficiente.

## Perché usare Aspose.CAD per cercare testo in DWG?

Aspose.CAD supporta **oltre 30 formati CAD e BIM** (inclusi DWG, DXF, DGN, DWF) e può elaborare file fino a **500 MB** senza caricamento completo in memoria. La libreria garantisce **il 99 % di precisione nell'estrazione del testo** su disegni complessi, un miglioramento quantificato rispetto a molti parser open‑source che spesso non riconoscono MTEXT incorporato o attributi di blocco.

## Come cercare testo nei file DWG con C#?

`Image.Load` è un metodo statico che legge un file CAD e restituisce un'istanza di CadImage.  

Carica il DWG usando `Image.Load`, recupera la collezione `TextFragments` e filtrala con LINQ in base al termine di ricerca. Questo schema conciso gira in tempo lineare rispetto al numero di entità testuali, non richiede librerie aggiuntive e funziona in modo coerente su ambienti .NET Framework e .NET Core.

### Passo 1: installa il pacchetto NuGet Aspose.CAD
Apri la console del NuGet Package Manager e esegui:

```
Install-Package Aspose.CAD
```

Questo aggiunge gli assembly richiesti e aggiorna il file di progetto.

### Passo 2: apri il file DWG
Crea un'istanza `CadImage` chiamando `Image.Load`. Il metodo rileva automaticamente il formato del file e prepara una rappresentazione in‑memoria.

### Passo 3: elenca i frammenti di testo
`image.TextFragments` restituisce una collezione di oggetti `TextFragment`, ognuno dei quali espone `Text`, `Location`, `Height` e `LayerName`. Puoi iterare o filtrare la collezione con LINQ.

### Passo 4: applica i criteri di ricerca
Usa `String.Contains`, `Regex.IsMatch` o qualsiasi predicato personalizzato per individuare il testo esatto di cui hai bisogno. Per ricerche case‑insensitive, chiama `ToLowerInvariant()` su entrambi i lati.

### Passo 5: gestisci i risultati
Le azioni tipiche includono la registrazione delle coordinate del frammento, l'esportazione in CSV o l'evidenziazione dell'entità in un visualizzatore. Poiché l'API fornisce la `Location` esatta, puoi passarla a qualsiasi componente di visualizzazione CAD a valle.

## Come estrarre testo da DWG?

TextFragment è l'oggetto che contiene il testo estratto e i relativi metadati, come posizione e layer.  

L'estrazione del testo è identica alla ricerca; basta enumerare la collezione `TextFragment` e leggere la proprietà `TextFragment.Text` di ciascuno. Puoi concatenare le stringhe in un unico documento, scriverle in un file CSV o inserirle in un indice di ricerca per un recupero rapido su più disegni.

## Problemi comuni e risoluzione dei problemi
- **Missing MTEXT:** Alcune versioni più vecchie di DWG memorizzano testo multilinea negli attributi di blocco. Assicurati di ispezionare anche `image.Blocks` per oggetti `Attribute`.  
- **Encoding issues:** I file DWG possono utilizzare pagine di codice non Unicode. Imposta `image.LoadOptions.Encoding` sul `System.Text.Encoding` appropriato prima del caricamento.  
- **Large files:** Per file superiori a 200 MB, abilita `image.LoadOptions.Streaming = true` per mantenere l'uso di memoria sotto i 100 MB.

## Domande frequenti

**D: Posso cercare testo in file DWG protetti da password?**  
R: Sì. Fornisci la password tramite `CadLoadOptions.Password` quando chiami `Image.Load`.

**D: L'API supporta la ricerca su più file DWG contemporaneamente?**  
R: Assolutamente. Scorri una directory, carica ogni file e riutilizza lo stesso filtro LINQ – la libreria è thread‑safe per l'elaborazione parallela.

**D: Quanto è accurata l'estrazione del testo per annotazioni complesse?**  
R: Aspose.CAD riporta un **tasso di successo del 99 %** su set di test standard del settore, gestendo MTEXT, definizioni di attributi e persino caratteri Unicode incorporati.

**D: È possibile evidenziare il testo trovato in un visualizzatore?**  
R: Dopo aver ottenuto la `Location` di ciascun `TextFragment`, puoi disegnare una sovrapposizione temporanea usando qualsiasi visualizzatore CAD che accetti primitive geometriche.

**D: Quale modello di licenza si applica ad Aspose.CAD?**  
R: Il prodotto utilizza un modello di licenza per sviluppatore o per server; è disponibile una licenza di valutazione gratuita per 30 giorni.

---

**Last Updated:** 2026-10-04  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

## Tutorial di ricerca e manipolazione del testo
### [Ricerca di testo nei file DWG con C# - Tutorial Aspose.CAD](./searching-text-in-dwg-files/)

```csharp
using Aspose.CAD;
using Aspose.CAD.ImageOptions;

// Load the DWG file
using var image = (CadImage)Image.Load("sample.dwg");

// Retrieve all text fragments
var fragments = image.TextFragments;

// Filter fragments that contain the target string
var matches = fragments.Where(t => t.Text.Contains("TargetString"));
```

## Tutorial correlati

- [Converti DWG in PDF e aggiungi testo in C# – Tutorial Aspose.CAD](/cad/net/dwg-file-manipulation/adding-text-to-dwg/)
- [Come convertire DWG in PDF e immagini raster usando Aspose.CAD per .NET](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [Come renderizzare CAD e convertire DWG – Aspose.CAD .NET](/cad/net/conversion-and-export/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}