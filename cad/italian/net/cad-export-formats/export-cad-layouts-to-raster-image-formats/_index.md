---
date: 2026-03-21
description: Scopri come convertire i file dxf in png e altri formati raster usando
  Aspose.CAD per .NET. Segui la nostra guida passo‑passo per un'esportazione senza
  problemi dei layer CAD.
linktitle: Export CAD Layouts to Raster Image Formats
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Converti DXF in PNG con Aspose.CAD per .NET
url: /it/net/cad-export-formats/export-cad-layouts-to-raster-image-formats/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Esporta layout CAD in formati immagine raster in Aspose.CAD per .NET

## Introduzione

Stai cercando di **convert dxf to png** e altri formati immagine raster in modo efficiente utilizzando Aspose.CAD per .NET? Questa guida passo‑passo ti accompagnerà attraverso il processo, fornendo istruzioni dettagliate e frammenti di codice per rendere il compito fluido. Che tu sia uno sviluppatore esperto o un neofita di Aspose.CAD, questo tutorial è adatto a tutti i livelli di competenza.

### Risposte rapide
- **Quale libreria gestisce la conversione?** Aspose.CAD for .NET  
- **Formato principale supportato subito?** JPEG, PNG, BMP e TIFF raster images  
- **Posso esportare specifici layer CAD?** Sì – usa `CadRasterizationOptions.Layers` per mirare a layer individuali  
- **È necessaria una licenza per la produzione?** È richiesta una licenza valida di Aspose.CAD per l'uso non‑trial  
- **Versioni .NET supportate?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7  

## Che cos'è **convert dxf to png**?

Convertire un file DXF (Drawing Exchange Format) in PNG significa rasterizzare dati CAD basati su vettori in un'immagine basata su pixel. Questo è utile quando è necessario incorporare disegni CAD in pagine web, report o qualsiasi ambiente che supporta solo grafica raster.

## Perché esportare i layer CAD separatamente?

Esportare i layer CAD singolarmente ti offre un controllo granulare sull'output visivo, riduce le dimensioni del file per ogni immagine e ti consente di applicare stili o post‑processing specifici per layer. Questo è particolarmente utile per grandi disegni ingegneristici dove solo un sottoinsieme di layer è rilevante per un determinato pubblico.

## Prerequisiti

- **Aspose.CAD for .NET Library** – scaricala dal [sito Aspose.CAD](https://releases.aspose.com/cad/net/).  
- **File di disegno CAD** – un file DXF (ad es., `conic_pyramid.dxf`) che desideri convertire in formati raster.  

## Importa gli spazi dei nomi

Nel tuo progetto .NET, importa gli spazi dei nomi necessari per sfruttare le funzionalità di Aspose.CAD. Includi i seguenti spazi dei nomi all'inizio del tuo codice:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Come **convert dxf to png** – Guida passo‑passo

### Passo 1: Carica il disegno CAD

Per prima cosa, carica il file DXF in un oggetto `Image`. Questo oggetto rappresenta l'intero disegno CAD in memoria.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

// Load a CAD drawing in an instance of Image
using (var image = Image.Load(sourceFilePath))
{
    // Your code for loading the CAD drawing goes here
}
```

### Passo 2: Crea `CadRasterizationOptions`

Configura le impostazioni di rasterizzazione come dimensioni di output e risoluzione. Queste opzioni controllano come i dati vettoriali vengono rasterizzati.

```csharp
// Create an instance of CadRasterizationOptions
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
```

### Passo 3: Specifica i layer (Esporta layer CAD)

Se ti serve solo un layer specifico, elenca qui il suo nome. Questo dimostra **export cad layers** individualmente.

```csharp
// Add the layer name to the CadRasterizationOptions's layer list
rasterizationOptions.Layers = new string[] { "LayerA" };
```

### Passo 4: Scegli un formato immagine – Salva CAD come PNG (o JPEG)

Crea un oggetto di opzioni specifico per il formato immagine. Sostituisci `JpegOptions` con `PngOptions` quando vuoi **save cad as png**.

```csharp
// Create an instance of JpegOptions (or any ImageOptions for raster formats)
var options = new JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
```

> **Suggerimento professionale:** Per generare file PNG, basta istanziare `new PngOptions()` invece di `JpegOptions`.

### Passo 5: Esporta in formato JPEG (o PNG)

Infine, salva l'immagine rasterizzata su disco. L'estensione del file determina il formato di output.

```csharp
// Export each layer to Jpeg format
MyDir = MyDir + "CADLayersToRasterImageFormats_out.jpg";
image.Save(MyDir, options);
```

Quando sostituisci `JpegOptions` con `PngOptions`, lo stesso codice **convert dxf to png** e produrrà un file `.png`.

### Passo aggiuntivo: Converti tutti i layer

Se hai bisogno di **convert cad to raster** per ogni layer del disegno, chiama il metodo di supporto qui sotto. Esso itera su tutti i layer e salva ciascuno come immagine separata.

```csharp
ConvertAllLayersToRasterImageFormats();
```

> *Nota:* L'implementazione di `ConvertAllLayersToRasterImageFormats` fa parte della suite completa di esempi Aspose.CAD e dimostra l'elaborazione batch dei layer.

## Problemi comuni e risoluzione

| Sintomo | Probabile causa | Correzione |
|---------|-----------------|------------|
| Immagine vuota o bianca | Opzioni di rasterizzazione non impostate (es., `PageWidth`/`PageHeight` = 0) | Assicurati che `PageWidth` e `PageHeight` abbiano valori positivi |
| Layer mancanti | Nome layer errato nell'array `Layers` | Verifica il nome esatto del layer nel file CAD (case‑sensitive) |
| PNG a bassa qualità | DPI predefinito è basso | Imposta `rasterizationOptions.Resolution = 300;` per una qualità superiore |

## Domande frequenti (Originale)

### Q1: Posso usare altri formati immagine per l'esportazione?

A1: Sì, puoi. Basta sostituire `JpegOptions` con le opzioni del formato desiderato, come `PngOptions` o `BmpOptions`.

### Q2: È disponibile una versione di prova?

A2: Sì, puoi esplorare le funzionalità di Aspose.CAD scaricando la versione di prova [qui](https://releases.aspose.com/).

### Q3: Come posso ottenere supporto per Aspose.CAD?

A3: Visita il [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) per supporto della community o considera l'acquisto di una licenza per supporto dedicato.

### Q4: Sono disponibili licenze temporanee?

A4: Sì, puoi ottenere una licenza temporanea [qui](https://purchase.aspose.com/temporary-license/).

### Q5: Dove posso trovare la documentazione?

A5: Consulta la documentazione dettagliata [qui](https://reference.aspose.com/cad/net/).

## FAQ aggiuntive

**Q: Posso esportare tutti i layer in un unico comando?**  
A: Sì, usa il metodo `ConvertAllLayersToRasterImageFormats` mostrato sopra.

**Q: Aspose.CAD supporta formati vettoriali come SVG?**  
A: Si concentra principalmente sui formati raster, ma puoi esportare in PDF che conserva i dati vettoriali.

**Q: Come controllo il colore di sfondo del PNG esportato?**  
A: Imposta `rasterizationOptions.BackgroundColor` al `Color` desiderato prima di salvare.

**Q: È possibile esportare un singolo layout invece dell'intero disegno?**  
A: Sì, configura `rasterizationOptions.Layouts` per specificare il nome(i) del layout che desideri rasterizzare.

## Conclusione

Ora hai imparato come **convert dxf to png**, **export cad layers** e **save cad as png** o JPEG usando Aspose.CAD per .NET. Regolando `CadRasterizationOptions` e scambiando le opzioni del formato immagine, puoi personalizzare la conversione per praticamente qualsiasi output raster di cui hai bisogno. Esplora le altre opzioni di formato nell'API Aspose.CAD per ampliare il tuo flusso di lavoro CAD‑to‑raster.

---

**Ultimo aggiornamento:** 2026-03-21  
**Testato con:** Aspose.CAD for .NET 24.11 (ultima versione al momento della scrittura)  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}