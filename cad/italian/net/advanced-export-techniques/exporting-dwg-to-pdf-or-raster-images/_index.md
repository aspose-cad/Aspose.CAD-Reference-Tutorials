---
date: 2026-03-16
description: Scopri come convertire DWG in PDF o immagini raster con Aspose.CAD per
  .NET. Questo tutorial passo‑passo da CAD a PDF copre l'esportazione di DWG in formati
  immagine come PNG e mostra come esportare i file DWG in immagini in modo efficiente.
linktitle: Exporting DWG to PDF or Raster Images
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Come convertire DWG in PDF e immagini raster utilizzando Aspose.CAD per .NET
url: /it/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/
weight: 11
---

:** 2026-03-16 => "**Ultimo aggiornamento:** 2026-03-16"

**Tested With:** Aspose.CAD 24.11 for .NET => "**Testato con:** Aspose.CAD 24.11 per .NET"

**Author:** Aspose => "**Autore:** Aspose"

Then closing shortcodes unchanged.

Also there is a backtop button shortcode unchanged.

Make sure to keep blank lines.

Now produce final content.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Esportazione di DWG in PDF o Immagini Raster - Guida Aspose.CAD

## Introduzione

Se hai bisogno di **convertire DWG in PDF** (o in formati raster come PNG) direttamente da un'applicazione .NET, sei nel posto giusto. In questo tutorial percorreremo i passaggi esatti necessari per utilizzare Aspose.CAD per .NET per eseguire la conversione, spiegheremo perché la libreria è una scelta solida e ti mostreremo come gestire sia l'output PDF che quello immagine con poche righe di codice.

## Risposte Rapide
- **Quale libreria gestisce la conversione DWG?** Aspose.CAD per .NET  
- **Posso esportare DWG in PNG così come in PDF?** Sì – le stesse opzioni di rasterizzazione funzionano per entrambi i formati.  
- **È necessaria una licenza per lo sviluppo?** Una prova gratuita è sufficiente per i test; è richiesta una licenza commerciale per la produzione.  
- **Quali versioni .NET sono supportate?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **La conversione delle unità è gestita automaticamente?** Puoi definire manualmente il sistema di unità (metrico o imperiale) come mostrato nel codice.

## Cos'è “convertire DWG in PDF”?
Convertire DWG in PDF significa prendere un disegno CAD (DWG) e renderizzarlo in un documento portatile, solo visualizzabile (PDF). Questo è utile per condividere i progetti con stakeholder che non possiedono software CAD, creare documentazione stampabile o archiviare i disegni in un formato universalmente leggibile.

## Perché usare Aspose.CAD per questa conversione?
- **Nessuna dipendenza esterna** – la libreria funziona interamente in codice gestito.  
- **Alta fedeltà** – conserva livelli, spessori delle linee e informazioni di layout.  
- **Opzioni raster integrate** – consente di esportare in PNG, JPEG, BMP, ecc., con un unico oggetto di configurazione.  
- **Cross‑platform** – funziona su Windows, Linux e macOS con .NET Core.

## Prerequisiti

Prima di immergerci nel tutorial, assicurati di avere quanto segue:

- Una conoscenza di base della programmazione .NET.  
- Libreria Aspose.CAD per .NET installata. Se non lo è, scaricala [qui](https://releases.aspose.com/cad/net/).  
- Il tuo IDE preferito configurato per lo sviluppo .NET.

## Importa Namespace

Iniziamo importando i namespace necessari nel tuo progetto .NET. Questo garantisce l'accesso alle funzionalità di Aspose.CAD nel tuo codice.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
```

## Passo 1: Carica il file DWG

Inizia caricando il file DWG che desideri convertire. Sostituisci `"Your Document Directory"` con il percorso del tuo file DWG.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for loading DWG goes here
}
```

## Passo 2: Configura l'esportazione PDF (Come esportare DWG in PDF)

Ora, configuriamo le impostazioni di esportazione PDF. Questo esempio dimostra come impostare il layout e gestire le conversioni delle unità.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };

// Check and define the unit system
bool currentUnitIsMetric = false;
double currentUnitCoefficient = 1.0;
DefineUnitSystem(cadImage.UnitType, out currentUnitIsMetric, out currentUnitCoefficient);

// Your code for setting up PDF export goes here
```

## Passo 3: Esporta in PDF

Esegui l'esportazione in PDF utilizzando le impostazioni configurate.

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath, pdfOptions);
```

## Passo 4: Esporta in Immagini Raster (esporta dwg in immagine)

Estendi la funzionalità per esportare in immagini raster, come PNG.

```csharp
// A4 size at 300 DPI - 2480 x 3508
rasterizationOptions.PageHeight = 3508;
rasterizationOptions.PageWidth = 2480;

PngOptions pngOptions = new PngOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath.Replace("pdf", "png"), pngOptions);
```

## Problemi Comuni e Soluzioni

| Problema | Perché accade | Come risolvere |
|----------|----------------|----------------|
| **Pagine vuote in PDF** | Layout non specificato correttamente | Assicurati che `rasterizationOptions.Layouts` includa il nome del layout corretto (ad es., `"Model"`). |
| **Dimensioni errate** | DPI o dimensione pagina non corrispondenti | Regola `PageHeight`, `PageWidth` e i valori DPI in `CadRasterizationOptions`. |
| **Le unità appaiono errate** | Conversione di unità non definita | Usa `DefineUnitSystem` per impostare `currentUnitIsMetric` e `currentUnitCoefficient` in base a `cadImage.UnitType`. |
| **Eccezione di licenza** | Limiti della versione di prova | Applica una licenza temporanea o permanente prima di chiamare `Image.Load`. |

## Domande Frequenti

### Q1: Posso usare Aspose.CAD per .NET nei miei progetti commerciali?
A1: Sì, è possibile. Visita [purchase.aspose.com/buy](https://purchase.aspose.com/buy) per i dettagli sulla licenza.

### Q2: È disponibile una versione di prova gratuita?
A2: Certamente! Ottieni la tua versione di prova gratuita [qui](https://releases.aspose.com/).

### Q3: Come posso ottenere supporto per Aspose.CAD per .NET?
A3: Vai al [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) per il supporto della community.

### Q4: Posso ottenere una licenza temporanea per scopi di test?
A4: Sì, puoi ottenere una licenza temporanea [qui](https://purchase.aspose.com/temporary-license/).

### Q5: Dove posso trovare la documentazione dettagliata?
A5: La documentazione è disponibile su [Aspose.CAD](https://reference.aspose.com/cad/net/).

### Q6: Come **salvare CAD come PNG** con alta qualità?
A6: Imposta `PageHeight` e `PageWidth` alle dimensioni in pixel desiderate e scegli un DPI di 300 o superiore in `CadRasterizationOptions`.

### Q7: Qual è il modo migliore per **convertire dwg** quando il file sorgente contiene più layout?
A7: Popola `rasterizationOptions.Layouts` con tutti i nomi dei layout che desideri esportare, quindi itera su ciascun layout e chiama `Save` per ogni formato di output.

**Ultimo aggiornamento:** 2026-03-16  
**Testato con:** Aspose.CAD 24.11 per .NET  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}