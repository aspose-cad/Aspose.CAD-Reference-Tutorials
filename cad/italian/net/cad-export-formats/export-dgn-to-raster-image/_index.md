---
date: 2026-03-24
description: Scopri come convertire dgn in png e salvare cad come jpeg usando Aspose.CAD
  per .NET – una guida rapida per la conversione da CAD a immagine.
linktitle: Export DGN to Raster Image
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Come convertire DGN in PNG con Aspose.CAD per .NET
url: /it/net/cad-export-formats/export-dgn-to-raster-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convertire DGN in PNG con Aspose.CAD per .NET

## Quick Answers
- **Posso convertire DGN in PNG con Aspose.CAD?** Sì – basta configurare le opzioni di rasterizzazione e scegliere l'output PNG o JPEG.  
- **Ho bisogno di una licenza per l'uso in produzione?** È necessaria una licenza valida di Aspose.CAD per le distribuzioni non‑trial.  
- **Quali versioni di .NET sono supportate?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7.  
- **Quali formati immagine sono disponibili?** PNG, JPEG, BMP, GIF, TIFF e altro.  
- **È necessario gestire le eccezioni?** Assolutamente – avvolgi la conversione in try/catch per gestire i problemi di accesso ai file.

## Che cos'è “convert dgn to png”?
Convertire un file DGN (MicroStation) in PNG significa rasterizzare i dati CAD vettoriali in un'immagine basata su pixel. Questo è utile per generare anteprime, incorporare disegni in email HTML o creare miniature per sistemi di gestione documentale.

## Perché usare Aspose.CAD per la conversione CAD‑immagine?
- **Nessuna dipendenza esterna** – funziona interamente in codice gestito.  
- **Alta fedeltà** – preserva spessori delle linee, livelli e colori.  
- **Output flessibile** – passa da PNG, JPEG, BMP, ecc., modificando un'unica opzione.  
- **Ottimizzato per le prestazioni** – la rasterizzazione è veloce anche per disegni di grandi dimensioni.

## Prerequisites

Prima di iniziare, assicurati di avere:

- **Aspose.CAD for .NET** installato nel tuo progetto. Puoi scaricarlo dal [website](https://reference.aspose.com/cad/net/).  
- Un file DGN di esempio (ad es. `Nikon_D90_Camera.dgn`) posizionato in una directory nota.

## Import Namespaces

Inizia aggiungendo le istruzioni `using` necessarie così da poter accedere alle classi Aspose.CAD.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Step 1: Load the DGN File

Carica il DGN di origine in un oggetto `CadImage`. Questo oggetto rappresenta il disegno CAD in memoria e sarà la sorgente per la rasterizzazione.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for further processing goes here
}
```

## Step 2: Define Rasterization Options

Configura come il disegno CAD deve essere rasterizzato. Qui puoi controllare le dimensioni dell'immagine, la scala e il colore di sfondo.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## Step 3: Choose the Output Format (PNG or JPEG)

Sebbene il tutorial si concentri su PNG, potresti anche voler **save cad as jpeg**. Crea l'oggetto delle opzioni immagine appropriato e collega le impostazioni di rasterizzazione.

```csharp
ImageOptionsBase options = new JpegOptions();   // Change to PngOptions() for PNG output
options.VectorRasterizationOptions = rasterizationOptions;
```

> **Suggerimento professionale:** Per generare un file PNG, sostituisci `new JpegOptions()` con `new PngOptions()`.

## Step 4: Save the Raster Image

Infine, chiama `Save` sull'istanza `CadImage`, fornendo il nome file desiderato e l'oggetto delle opzioni configurato.

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpg", options);
```

Se hai cambiato a `PngOptions`, il file verrà salvato come `ExportDGNToRasterImage_out.png`.

## Common Issues and Solutions

| Problema | Causa | Soluzione |
|----------|-------|-----------|
| **Immagine di output vuota** | `NoScaling` impostato in modo errato o layout non selezionato | Imposta `AutomaticLayoutsScaling = true` o specifica il layout desiderato. |
| **Out‑of‑memory per file di grandi dimensioni** | Caricamento di un DGN enorme senza streaming | Usa `Image.Load(sourceFilePath, new LoadOptions { LoadOnDemand = true })`. |
| **Versione DGN non supportata** | Versioni MicroStation più vecchie | Assicurati di avere l'ultima versione di Aspose.CAD che supporta i formati legacy. |

## Frequently Asked Questions

**D: Posso esportare file DGN in formati diversi da JPEG?**  
R: Sì, Aspose.CAD per .NET supporta PNG, BMP, GIF, TIFF e altro – basta sostituire la classe delle opzioni (ad es. `new PngOptions()`).

**D: Come devo gestire le eccezioni durante la conversione?**  
R: Avvolgi il codice di conversione in un blocco `try/catch` e registra `Aspose.CAD.CadException` per informazioni dettagliate sull'errore.

**D: È disponibile una versione di prova per Aspose.CAD per .NET?**  
R: Sì, puoi provare il prodotto con una versione di prova gratuita. Visita [qui](https://releases.aspose.com/) per ulteriori informazioni.

**D: Dove posso chiedere assistenza o discutere problemi relativi ad Aspose.CAD per .NET?**  
R: Vai al [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) per supporto della community e discussioni.

**D: Come posso ottenere una licenza temporanea per Aspose.CAD per .NET?**  
R: Visita [questo link](https://purchase.aspose.com/temporary-license/) per ottenere una licenza temporanea per le tue esigenze di sviluppo.

## Conclusion

Ora hai imparato come **convertire dgn in png** (o JPEG) usando Aspose.CAD per .NET. Regolando le opzioni di rasterizzazione e cambiando la classe delle opzioni immagine, puoi adattare l'output a qualsiasi requisito del progetto. Sentiti libero di sperimentare con diverse dimensioni di pagina, impostazioni DPI e formati di file per ottenere l'immagine raster perfetta per la tua applicazione.

---

**Ultimo aggiornamento:** 2026-03-24  
**Testato con:** Aspose.CAD 24.11 for .NET  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}