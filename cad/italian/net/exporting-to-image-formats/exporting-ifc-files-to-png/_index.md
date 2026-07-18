---
date: 2026-07-18
description: Come esportare CAD in PNG usando Aspose.CAD per .NET. Converti i file
  IFC in immagini PNG ad alta qualità rapidamente e in modo affidabile.
keywords:
- how to export cad to png
- Aspose.CAD IFC conversion
- CAD to PNG .NET
lastmod: 2026-07-18
linktitle: Esportazione di file IFC in PNG
og_description: Come esportare CAD in PNG usando Aspose.CAD per .NET. Scopri la conversione
  passo‑passo dei file IFC in immagini PNG senza necessità di codice.
og_image_alt: Guide showing IFC to PNG conversion with Aspose.CAD for .NET
og_title: Come esportare CAD in PNG – Guida Aspose.CAD .NET
schemas:
- author: Aspose
  dateModified: '2026-07-18'
  description: How to export CAD to PNG using Aspose.CAD for .NET. Convert IFC files
    to high‑quality PNG images quickly and reliably.
  headline: How to Export CAD to PNG – Exporting IFC Files with Aspose.CAD
  type: TechArticle
- questions:
  - answer: No, Aspose.CAD for .NET is specifically designed for Windows environments.
    question: Can I use Aspose.CAD for .NET on macOS or Linux?
  - answer: Yes, you can obtain a temporary license from [here](https://purchase.aspose.com/temporary-license/)
      for evaluation.
    question: Is a temporary license available for testing purposes?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community
      support and discussions.
    question: How can I get support for Aspose.CAD?
  - answer: Refer to the [Aspose.CAD documentation](https://reference.aspose.com/cad/net/)
      for detailed information and examples.
    question: Where can I find comprehensive documentation?
  - answer: Check the documentation or seek assistance on the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19).
    question: What if I encounter issues during installation?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- export cad
- Aspose.CAD
- IFC to PNG
- .NET image conversion
title: Come esportare CAD in PNG – Esportazione di file IFC con Aspose.CAD
url: /it/net/exporting-to-image-formats/exporting-ifc-files-to-png/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come esportare CAD in PNG – Esportazione di file IFC con Aspose.CAD

## Introduzione

Se hai bisogno di **how to export cad to png**, Aspose.CAD per .NET offre un modo affidabile, senza codice, per trasformare i modelli IFC (Industry Foundation Classes) in immagini raster PNG nitide. In questo tutorial percorreremo l'intero flusso di lavoro — dall'installazione della libreria al salvataggio del PNG finale — così potrai integrare la conversione in qualsiasi applicazione .NET con fiducia.

## Risposte rapide
- **Quale libreria gestisce la conversione?** Aspose.CAD per .NET.
- **Formato sorgente supportato?** File IFC (Industry Foundation Classes).
- **Formato immagine di destinazione?** PNG, con pieno controllo su dimensione e risoluzione.
- **Versione minima di .NET?** .NET Framework 4.5+ o .NET Core 3.1+.
- **Requisito di licenza?** Una licenza valida di Aspose.CAD per l'uso in produzione.

## Che cos'è “how to export cad to png”?

La frase si riferisce al processo di conversione di formati di file basati su CAD, come IFC, in immagini raster Portable Network Graphics (PNG). Questa conversione consente una facile visualizzazione, condivisione e incorporamento di visualizzazioni CAD in pagine web, documentazione o report, fornendo un formato leggero e ampiamente supportato che preserva la fedeltà visiva senza richiedere visualizzatori CAD specializzati.

## Perché utilizzare Aspose.CAD per questa conversione?

Aspose.CAD supporta **50+ CAD and BIM formats** e può elaborare modelli IFC di centinaia di pagine senza caricare l'intero file in memoria. Offre conversioni rapide ed efficienti in termini di memoria su hardware server standard, gestendo automaticamente livelli, spessori di linea e mappatura dei colori, offrendo al contempo ampie opzioni di configurazione per la qualità e le dimensioni dell'output.

## Prerequisiti

### 1. Installazione di Aspose.CAD
Assicurati di avere Aspose.CAD per .NET installato. Puoi scaricarlo dalla pagina di rilascio [qui](https://releases.aspose.com/cad/net/).

### 2. Directory dei documenti
Crea una directory designata per i tuoi documenti. Nell'esempio fornito, la variabile `MyDir` rappresenta la directory dei documenti.

## Importa gli spazi dei nomi
Ora che i prerequisiti sono pronti, importa gli spazi dei nomi necessari per lavorare con Aspose.CAD nel tuo progetto .NET.

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using Aspose.CAD.FileFormats.Ifc;
```

## Come esportare CAD in PNG?

`IfcImage` rappresenta un'immagine CAD IFC che può essere rasterizzata in formati raster come PNG. Carica il tuo file IFC con `new IfcImage("source.ifc")`, configura la rasterizzazione tramite `RasterizationOptions`, imposta le impostazioni specifiche per PNG con `PngOptions` e infine chiama `Save(outputPath, pngOptions)`. Questo flusso end‑to‑end converte il modello CAD in un PNG ad alta risoluzione in poche righe di codice, gestendo automaticamente livelli, colori e spessori di linea.

## Passo 1: Carica il file IFC
La classe `IfcImage` carica un modello IFC e lo prepara per la rasterizzazione.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "example.ifc";
using (IfcImage cadImage = (IfcImage)Image.Load(sourceFilePath))
{
```

In questo passaggio inizializziamo l'oggetto Aspose.CAD `IfcImage` e carichiamo il file IFC al suo interno.

## Passo 2: Imposta le opzioni di rasterizzazione
La classe `RasterizationOptions` definisce come i dati vettoriali vengono convertiti in immagini raster, includendo larghezza, altezza della pagina e colore di sfondo.

```csharp
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
   
    rasterizationOptions.PageWidth = 100;
    rasterizationOptions.PageHeight = 100;
```

Definisci le opzioni di rasterizzazione per configurare larghezza e altezza della pagina per l'output PNG.

## Passo 3: Imposta le opzioni PNG
La classe `PngOptions` contiene le impostazioni specifiche per l'output PNG, come livello di compressione e profondità di colore.

```csharp
    PngOptions pngOptions = new PngOptions();
    pngOptions.VectorRasterizationOptions = rasterizationOptions;
```

Crea le opzioni PNG e associa le opzioni di rasterizzazione definite in precedenza.

## Passo 4: Specifica il percorso di output
Il percorso di output determina dove verrà salvato il file PNG generato.

```csharp
    // Set output path as well
    string outPath = sourceFilePath + ".png";
    cadImage.Save(outPath, pngOptions);
}
```

Definisci il percorso di output per il file PNG, assicurandoti che abbia lo stesso nome del file sorgente con l'estensione ".png". Infine, salva l'immagine convertita.

## Problemi comuni e soluzioni
- **Font o stili di linea mancanti:** Assicurati che l'IFC sorgente faccia riferimento a tutte le risorse necessarie; Aspose.CAD incorpora le risorse mancanti quando possibile.
- **File di grandi dimensioni causano picchi di memoria:** Usa la proprietà `MemoryLimit` su `RasterizationOptions` per limitare l'uso della memoria.
- **Colori errati:** Verifica che le definizioni di colore dell'IFC sorgente siano conformi allo schema IFC; Aspose.CAD rispetta la mappatura dei colori standard.

## Domande frequenti

**Q: Posso usare Aspose.CAD per .NET su macOS o Linux?**  
A: No, Aspose.CAD per .NET è specificamente progettato per ambienti Windows.

**Q: È disponibile una licenza temporanea per scopi di test?**  
A: Sì, è possibile ottenere una licenza temporanea da [qui](https://purchase.aspose.com/temporary-license/) per la valutazione.

**Q: Come posso ottenere supporto per Aspose.CAD?**  
A: Visita il [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) per supporto della community e discussioni.

**Q: Dove posso trovare una documentazione completa?**  
A: Consulta la [documentazione Aspose.CAD](https://reference.aspose.com/cad/net/) per informazioni dettagliate ed esempi.

**Q: Cosa fare se incontro problemi durante l'installazione?**  
A: Controlla la documentazione o richiedi assistenza sul [forum Aspose.CAD](https://forum.aspose.com/c/cad/19).

---

**Ultimo aggiornamento:** 2026-07-18  
**Testato con:** Aspose.CAD 24.11 per .NET  
**Autore:** Aspose

## Tutorial correlati

- [Converti disegno CAD in immagine raster in Aspose.CAD per .NET](/cad/net/cad-drawing-manipulation/convert-cad-drawing-to-raster-image/)
- [Conversione da STL a PNG semplificata con Aspose.CAD per .NET](/cad/net/stl-file-export/exporting-stl-files-to-png/)
- [Esporta layout CAD in formati immagine raster in Aspose.CAD per .NET](/cad/net/cad-export-formats/export-cad-layouts-to-raster-image-formats/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}