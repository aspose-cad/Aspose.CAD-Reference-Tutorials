---
title: Supporto per DGN V7 in Aspose.CAD per .NET
linktitle: Supporto per DGN V7
second_title: Aspose.CAD .NET - Formato file CAD e BIM
description: Esplora Aspose.CAD per il supporto continuo di .NET per DGN V7. Converti file DGN in immagini raster senza sforzo con una guida passo passo.
weight: 19
url: /it/net/cad-features-and-support/support-for-dgn-v7/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Supporto per DGN V7 in Aspose.CAD per .NET

## introduzione

Nel regno dello sviluppo .NET, Aspose.CAD si distingue come una potente libreria per la gestione di file CAD (Computer-Aided Design). Questo tutorial approfondisce una funzionalità specifica di Aspose.CAD per .NET: supporto per i file DGN V7. DGN, abbreviazione di Design, è un formato di file ampiamente utilizzato nel dominio CAD. Aspose.CAD semplifica il processo di lavoro con i file DGN V7, offrendo agli sviluppatori un'esperienza senza interruzioni.

## Prerequisiti

Prima di approfondire l'implementazione, assicurati di disporre dei seguenti prerequisiti:

-  Aspose.CAD per .NET: assicurati di avere la libreria Aspose.CAD installata. Puoi scaricarlo da[sito web](https://releases.aspose.com/cad/net/).

- Ambiente di sviluppo: configura un ambiente di sviluppo .NET funzionante, incluso Visual Studio o qualsiasi altro IDE preferito.

Ora che abbiamo ordinato i prerequisiti, esploriamo come sfruttare il supporto per DGN V7 in Aspose.CAD per .NET.

## Importa spazi dei nomi

Inizia importando gli spazi dei nomi necessari per accedere alla funzionalità di Aspose.CAD:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Passaggio 1: caricare il file DGN

 Inizia caricando un file DGN esistente come file`CadImage` Sostituire`"Your Document Directory"` E`"Nikon_D90_Camera.dgn"` con il percorso della directory e il nome del file appropriati.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Il codice per ulteriori passaggi va qui...
}
```

## Passaggio 2: configura le opzioni di rasterizzazione

 Creare un`CadRasterizationOptions` oggetto per definire e impostare varie proprietà relative alla rasterizzazione.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions
{
    PageWidth = 600,
    PageHeight = 300,
    NoScaling = true,
    AutomaticLayoutsScaling = false
};
```

## Passaggio 3: imposta le opzioni di rasterizzazione vettoriale

 Creare un`JpegOptions` oggetto poiché intendiamo convertire il file DGN in JPEG. Assegnare quello creato in precedenza`CadRasterizationOptions` opporsi ad esso.

```csharp
ImageOptionsBase options = new JpegOptions
{
    VectorRasterizationOptions = rasterizationOptions
};
```

## Passaggio 4: salva l'immagine rasterizzata

 Chiama il`Save` metodo del`CadImage` class per esportare il file DGN in un'immagine raster, in questo caso JPEG.

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpeg", options);
```

Una volta completati questi passaggi, il file DGN viene esportato correttamente in un'immagine raster.

## Conclusione

In questo tutorial, abbiamo esplorato il supporto continuo per DGN V7 in Aspose.CAD per .NET. Seguendo la guida passo passo, gli sviluppatori possono convertire facilmente i file DGN in immagini raster, espandendo le capacità delle loro applicazioni .NET.

## Domande frequenti

### Q1: Aspose.CAD è compatibile con le ultime specifiche DGN V7?

R1: Sì, Aspose.CAD è progettato per gestire perfettamente i file DGN V7, garantendo la compatibilità con le specifiche più recenti.

### Q2: Posso personalizzare le opzioni di rasterizzazione per la conversione dei file DGN?

 A2: Assolutamente. Il tutorial dimostra come creare e configurare`CadRasterizationOptions` per personalizzare il processo di conversione.

### Q3: Esistono altri formati di output supportati oltre a JPEG?

A3: Sì, Aspose.CAD supporta vari formati di output. È possibile esplorare la documentazione per un elenco completo.

### Q4: Come posso ottenere supporto per le query relative ad Aspose.CAD?

 A4: Visita il[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) per il supporto e le discussioni della comunità.

### Q5: È disponibile una prova gratuita per Aspose.CAD per .NET?

 R5: Sì, puoi accedere a una prova gratuita[Qui](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
