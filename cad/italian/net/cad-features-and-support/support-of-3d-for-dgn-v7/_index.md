---
date: 2026-03-29
description: Learn how to configure CAD rasterization options and export DGN to PDF
  with 3D support using Aspose.CAD for .NET.
linktitle: Support of 3D for DGN V7
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Configura le opzioni di rasterizzazione CAD per DGN V7 3D
url: /it/net/cad-features-and-support/support-of-3d-for-dgn-v7/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Configura le opzioni di rasterizzazione CAD per DGN V7 3D

## Introduzione

In questo tutorial completo imparerai **come configurare le opzioni di rasterizzazione CAD** per esportare un file DGN V7 3‑D in PDF utilizzando Aspose.CAD per .NET. Che tu stia creando un visualizzatore CAD, uno strumento di reporting o una pipeline di conversione automatizzata, padroneggiare queste impostazioni ti offre un controllo preciso su dimensioni della pagina, scala del layout, colori di sfondo e le viste specifiche che desideri renderizzare. Procediamo passo dopo passo.

## Risposte rapide
- **Che cosa significa “configure CAD rasterization options”?**  
  Si riferisce all’impostazione di proprietà come dimensioni della pagina, scala, colore di sfondo e selezione del layout prima di convertire un file CAD in un formato raster (ad es., PDF).
- **Come esportare DGN in PDF con supporto 3‑D?**  
  Carica il DGN con `DgnImage`, definisci `PdfOptions` + `CadRasterizationOptions`, quindi chiama `Save`.
- **Ho bisogno di una licenza per l'uso in produzione?**  
  Sì – è necessaria una licenza commerciale per il deployment; è disponibile una prova gratuita.
- **Quali versioni .NET sono supportate?**  
  .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.
- **Posso scegliere viste specifiche da esportare?**  
  Assolutamente – imposta l’array `Layouts` nelle opzioni di rasterizzazione.

## Che cosa è “configure CAD rasterization options”?

Configurare le opzioni di rasterizzazione CAD significa personalizzare il modo in cui un disegno CAD viene rasterizzato (convertito da vettoriale a bitmap o PDF). Regolando queste impostazioni controlli l’output visivo, le prestazioni e la dimensione del file del documento risultante.

## Perché usare Aspose.CAD per l'esportazione DGN V7 3‑D?

- **Integrazione completa .NET** – non sono richiesti COM o DLL native.  
- **Supporta la geometria 3‑D** – conserva le informazioni di profondità durante il rendering in PDF.  
- **Controllo fine** – scegli layout esatti, scala e colori di sfondo.  
- **Cross‑platform** – funziona su Windows, Linux e macOS con .NET Core.

## Prerequisiti

Prima di iniziare, assicurati di avere:

- **Aspose.CAD per .NET** – scaricalo da [here](https://releases.aspose.com/cad/net/).  
- **Visual Studio** o qualsiasi IDE .NET compatibile.  
- **Un file DGN di esempio** – per questa guida useremo `Nikon_D90_Camera.dgn` (incluso nel pacchetto di esempi Aspose).  

Ora che tutto è pronto, immergiamoci nel codice.

## Importa i namespace

Nel tuo progetto .NET, importa gli spazi dei nomi richiesti:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.ImageOptions;
```

## Passo 1: Configura la directory del documento

Crea una variabile che punti alla cartella dove risiederanno il tuo DGN di origine e i file di output.

```csharp
string MyDir = "Your Document Directory";
```

## Passo 2: Carica il file DGN

Carica il file DGN come `DgnImage`. Questo oggetto ti dà accesso ai dati CAD e al pipeline di rasterizzazione.

```csharp
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";
string outFile = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Your code for further processing goes here
}
```

## Passo 3: Configura le opzioni di esportazione PDF (Configura le opzioni di rasterizzazione CAD)

Qui **configuriamo le opzioni di rasterizzazione CAD** che determinano come il modello 3‑D viene renderizzato in PDF. Puoi regolare le dimensioni della pagina, abilitare la scala automatica del layout, impostare un colore di sfondo e scegliere i layout (viste) esatti da esportare.

```csharp
var options = new PdfOptions
{
    VectorRasterizationOptions = new CadRasterizationOptions
    {
        PageWidth = 1500,
        PageHeight = 1500,
        AutomaticLayoutsScaling = true,
        BackgroundColor = Color.Black,
        Layouts = new string[] { "1", "2", "3", "9" } // Only export specified views
    }
};
```

## Passo 4: Salva l'immagine raster

Infine, esporta il DGN in un file PDF usando le opzioni appena configurate.

```csharp
dgnImage.Save(outFile, options);
```

## Problemi comuni e soluzioni

| Problema | Soluzione |
|----------|-----------|
| **PDF vuoto** | Verifica che l'array `Layouts` contenga gli identificatori di vista corretti presenti nel file DGN. |
| **Colori errati** | Assicurati che `BackgroundColor` sia impostato al valore desiderato; usa `Color.White` per uno sfondo chiaro. |
| **Collo di bottiglia delle prestazioni su file di grandi dimensioni** | Abilita `AutomaticLayoutsScaling` e considera di ridurre `PageWidth/PageHeight` per una risoluzione raster più piccola. |
| **Eccezione di licenza** | Installa una licenza valida di Aspose.CAD prima di caricare l'immagine per evitare filigrane di prova. |

## Domande frequenti

**Q: Posso usare Aspose.CAD per .NET con altri formati di file CAD?**  
A: Sì, Aspose.CAD supporta DWG, DXF, DWF, DGN e molti altri formati.

**Q: Come posso gestire le eccezioni quando lavoro con Aspose.CAD?**  
A: Avvolgi il tuo codice in un blocco `try‑catch` e ispeziona `Aspose.CAD.CADException` per informazioni dettagliate sull'errore.

**Q: Aspose.CAD è adatto a progetti commerciali?**  
A: Assolutamente. Puoi acquistare una licenza [here](https://purchase.aspose.com/buy).

**Q: Posso provare Aspose.CAD per .NET prima di acquistare?**  
A: Sì, è disponibile una prova gratuita [here](https://releases.aspose.com/).

**Q: Dove posso trovare supporto della community per Aspose.CAD?**  
A: Unisciti al forum di discussione [here](https://forum.aspose.com/c/cad/19).

---

**Ultimo aggiornamento:** 2026-03-29  
**Testato con:** Aspose.CAD 24.11 per .NET  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}