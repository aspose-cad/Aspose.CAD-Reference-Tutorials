---
date: 2026-04-06
description: Impara a convertire DWF in JPG in C# con Aspose.CAD e scopri come estrarre
  le dimensioni del layout DWF dai file DWG.
keywords:
- convert dwf to jpg
- how to extract dwf
- convert dwg to jpg
linktitle: Lavorare con file DWG in C# - Ottenere la dimensione del layout DWF
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Converti DWF in JPG in C# – Ottieni le dimensioni del layout DWF da DWG
url: /it/net/dwg-file-manipulation/get-size-of-dwf-layout/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Converti DWF in JPG in C# – Ottieni le dimensioni del layout DWF da DWG

## Introduzione

Se hai bisogno di **convertire DWF in JPG** e allo stesso tempo determinare le dimensioni esatte del layout, sei nel posto giusto. In questo tutorial percorreremo un esempio completo, end‑to‑end, che utilizza Aspose.CAD per .NET per aprire un file DWF derivato da DWG, leggere la dimensione di ogni layout e salvare il layout come immagine JPG ad alta qualità. Alla fine non solo saprai come estrarre le informazioni del layout DWF, ma avrai anche uno snippet di codice riutilizzabile da inserire in qualsiasi progetto C#.

## Risposte rapide
- **Cosa significa “convertire DWF in JPG”?** Significa rasterizzare un layout DWF vettoriale in un'immagine bitmap JPEG.  
- **Perché leggere prima le dimensioni del layout?** Conoscere le dimensioni esatte consente di impostare le corrette dimensioni della pagina, evitando output allungati o ritagliati.  
- **Quale libreria gestisce questo?** Aspose.CAD per .NET fornisce pieno supporto per DWG, DWF e la conversione di immagini raster.  
- **Ho bisogno di una licenza?** Una licenza temporanea funziona per la valutazione; è necessaria una licenza completa per la produzione.  
- **Quali versioni .NET sono supportate?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## Cos'è “convertire DWF in JPG” e perché è importante?

Convertire un file DWF (Design Web Format) in JPG crea un'immagine portatile che può essere visualizzata nei browser, incorporata nei report o condivisa con stakeholder che non possiedono software CAD. La conversione ti offre anche la flessibilità di manipolare l'immagine (ridimensionare, comprimere, aggiungere filigrana) usando strumenti standard di elaborazione delle immagini.

## Perché estrarre le dimensioni del layout DWF?

Un file DWF può contenere più layout, ognuno con il proprio sistema di coordinate e unità (pollici, millimetri, ecc.). Estrarre le dimensioni del layout ti permette di:

1. Preservare il rapporto d'aspetto originale durante la rasterizzazione.  
2. Scegliere il DPI corretto per un output ad alta risoluzione.  
3. Automatizzare l'elaborazione batch di molti layout senza interventi manuali.

## Prerequisiti

Per seguire questo tutorial senza intoppi, assicurati di avere i seguenti prerequisiti:

- Aspose.CAD per .NET: Assicurati di avere Aspose.CAD per .NET installato. Puoi scaricarlo dalla [pagina di download di Aspose.CAD per .NET](https://releases.aspose.com/cad/net/).

Avere la libreria pronta ti permette di concentrarti sul codice invece di cercare dipendenze.

## Importa spazi dei nomi

Prima di iniziare a scrivere il codice, importa gli spazi dei nomi richiesti. Questi forniscono le classi di cui avremo bisogno per lavorare con file CAD, opzioni di rasterizzazione e I/O dei file.

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Dwf;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

## Passo 1: Configura l'ambiente

Crea un nuovo progetto console o class‑library C#, aggiungi un riferimento a **Aspose.CAD.dll** e assicurati che il progetto punti a una versione .NET compatibile.

## Passo 2: Definisci i percorsi dei file (come estrarre DWF)

Specifica dove si trova il tuo file DWF sorgente e dove devono essere scritti i file JPG generati.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "blocks_and_tables.dwf";
```

> **Suggerimento:** Usa `Path.Combine(MyDir, "blocks_and_tables.dwf")` per una gestione dei percorsi più sicura su diversi OS.

## Passo 3: Carica l'immagine DWF

Carica il file DWF in un oggetto `Aspose.CAD.Image`. Lo castiamo a `DwfImage` perché abbiamo bisogno di accedere alle proprietà specifiche della pagina.

```csharp
using (DwfImage image = (DwfImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    // Code for further steps will go here
}
```

## Passo 4: Itera attraverso le pagine

Un DWF può contenere diverse pagine (layout). Itera su ciascuna in modo da poterle elaborare singolarmente.

```csharp
foreach (var page in image.Pages)
{
    // Code for further steps will go here
}
```

## Passo 5: Ottieni le informazioni del layout

All'interno del ciclo, recupera il nome del layout. Questo nome sarà usato sia per il logging sia per nominare il file JPG di output.

```csharp
var layout = page.Name;
System.Console.WriteLine("Layout= " + layout);
```

## Passo 6: Configura le opzioni JPG

Crea un'istanza `JpegOptions` e configura le opzioni di rasterizzazione. La proprietà `Layouts` indica ad Aspose.CAD quale layout renderizzare.

```csharp
using (FileStream fs = new FileStream(MyDir + "layout_" + layout + ".jpg", FileMode.Create))
{
    JpegOptions jpegOptions = new JpegOptions();
    CadRasterizationOptions options = new CadRasterizationOptions();
    options.Layouts = new string[] { layout };
    // Code for further steps will go here
}
```

## Passo 7: Determina le dimensioni della pagina (converti dwg in jpg)

Calcola la larghezza e l'altezza del layout nelle sue unità native. Queste informazioni sono essenziali per impostare correttamente le dimensioni della pagina raster.

```csharp
double sizeExtX = page.MaxPoint.X - page.MinPoint.X;
double sizeExtY = page.MaxPoint.Y - page.MinPoint.Y;
// Code for further steps will go here
```

## Passo 8: Configura le dimensioni della pagina

Converti le unità native (pollici o millimetri) in pixel usando i metodi di supporto forniti da Aspose.CAD. Se il tipo di unità non è né uno né l'altro, ricadiamo sull'uso dei valori grezzi.

```csharp
if (page.UnitType == UnitType.Inch)
{
    options.PageHeight = CommonHelper.INtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.INtoPixels(sizeExtX, CommonHelper.DPI);
}
else if (page.UnitType == UnitType.Millimeter)
{
    options.PageHeight = CommonHelper.MMtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.MMtoPixels(sizeExtX, CommonHelper.DPI);
}
else
{
    options.PageHeight = (float)sizeExtY;
    options.PageWidth = (float)sizeExtX;
}
```

## Passo 9: Salva il file JPG

Infine, associa le opzioni di rasterizzazione alle opzioni JPEG e salva l'immagine su disco.

```csharp
jpegOptions.VectorRasterizationOptions = options;
image.Save(fs, jpegOptions);
}
```

Quando il ciclo termina, avrai un file JPG per ogni layout, ciascuno dimensionato esattamente per corrispondere alle dimensioni originali del DWF.

## Problemi comuni e soluzioni

| Sintomo | Causa probabile | Correzione |
|---------|-----------------|------------|
| Output JPG vuoto | `options.Layouts` non impostato correttamente | Verifica che il nome del layout corrisponda a `page.Name`. |
| Immagine distorta | Conversione DPI errata | Usa `CommonHelper.DPI = 300` (o il DPI desiderato) prima della conversione. |
| File non trovato | Percorso `MyDir` errato | Usa percorsi assoluti o `Path.Combine`. |
| Eccezione di licenza | Nessuna licenza applicata | Carica una licenza temporanea o permanente prima di chiamare `Image.Load`. |

## Domande frequenti

### Q1: Aspose.CAD è compatibile con gli ultimi formati di file DWG?

A1: Aspose.CAD supporta vari formati di file DWG, incluse le versioni più recenti. Consulta la [documentazione](https://reference.aspose.com/cad/net/) per i dettagli specifici di compatibilità.

### Q2: Posso usare Aspose.CAD sia per progetti commerciali che personali?

A2: Sì, Aspose.CAD offre opzioni di licenza flessibili sia per uso commerciale che personale. Visita la [pagina di acquisto](https://purchase.aspose.com/buy) per maggiori dettagli.

### Q3: Come posso ottenere una licenza temporanea per Aspose.CAD?

A3: Puoi ottenere una licenza temporanea da [qui](https://purchase.aspose.com/temporary-license/) per scopi di valutazione.

### Q4: Dove posso trovare supporto per Aspose.CAD?

A4: Per qualsiasi domanda o assistenza, visita il [forum di Aspose.CAD](https://forum.aspose.com/c/cad/19).

### Q5: È disponibile una versione di prova gratuita per Aspose.CAD?

A5: Sì, puoi accedere a una versione di prova gratuita di Aspose.CAD [qui](https://releases.aspose.com/).

### Q6: Come converto un file DWG direttamente in JPG senza estrarre prima il DWF?

A6: Puoi caricare il file DWG con `Aspose.CAD.Image.Load` e utilizzare lo stesso flusso di lavoro di rasterizzazione; basta impostare `options.Layouts` sui nomi dei layout desiderati dal DWG.

### Q7: La conversione preserva la qualità vettoriale?

A7: Una volta rasterizzata in JPG, l'immagine è basata su bitmap, quindi la scalabilità vettoriale viene persa. Per una scalatura senza perdita, considera l'esportazione in PNG o SVG.

**Ultimo aggiornamento:** 2026-04-06  
**Testato con:** Aspose.CAD 24.11 for .NET  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}