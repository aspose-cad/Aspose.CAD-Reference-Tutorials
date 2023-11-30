---
title: Creazione di PDF singoli con layout diversi - Guida Aspose.CAD
linktitle: Creazione di PDF singoli con layout diversi
second_title: Aspose.CAD .NET - Formato file CAD e BIM
description: Crea un singolo PDF con layout diversi utilizzando Aspose.CAD per .NET. Segui la nostra guida passo passo per un'integrazione perfetta e una generazione efficiente di PDF.
type: docs
weight: 13
url: /it/net/advanced-cad-techniques/creating-single-pdf-with-different-layouts/
---
## introduzione

Stai cercando di generare un singolo documento PDF da un disegno CAD con layout diversi utilizzando Aspose.CAD per .NET? Questa guida passo passo ti guiderà attraverso il processo, aiutandoti a ottenere un'integrazione perfetta e una creazione PDF efficiente. Aspose.CAD per .NET fornisce potenti funzionalità per manipolare i disegni CAD a livello di codice e in questo tutorial ci concentreremo sulla creazione di un singolo PDF con layout diversi.

## Prerequisiti

Prima di immergerti nel tutorial, assicurati di possedere i seguenti prerequisiti:

-  Aspose.CAD per .NET: assicurati di avere Aspose.CAD per .NET installato. Puoi scaricarlo da[Qui](https://releases.aspose.com/cad/net/).

- Ambiente di sviluppo: configura un ambiente di sviluppo .NET e acquisisci una conoscenza di base della programmazione C#.

## Importa spazi dei nomi

Nel tuo progetto C#, includi gli spazi dei nomi necessari per sfruttare le funzionalità di Aspose.CAD per .NET:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Passaggio 1: caricare l'immagine CAD

```csharp
// Il percorso della directory dei documenti.
string MyDir = "Your Document Directory";

using (CadImage cadImage = (CadImage)Image.Load(MyDir + "City skyway map.dwg"))
{
    // Il tuo codice per il passaggio 1 va qui
}
```

## Passaggio 2: personalizzare le opzioni di rasterizzazione

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1000;
rasterizationOptions.PageHeight = 1000;

// Dimensioni personalizzate per diversi layout
rasterizationOptions.LayoutPageSizes.Add("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.LayoutPageSizes.Add("8.5 x 11 Plot", new SizeF(1000, 100));
```

## Passaggio 3: definire le opzioni PDF

```csharp
PdfOptions pdfOptions = new PdfOptions() { VectorRasterizationOptions = rasterizationOptions };
```

## Passaggio 4: salva come PDF

```csharp
cadImage.Save(MyDir + "singlePDF_out.pdf", pdfOptions);
```

Ora hai creato con successo un singolo documento PDF con diversi layout utilizzando Aspose.CAD per .NET. Sentiti libero di esplorare più funzionalità e personalizzare il codice in base alle tue esigenze specifiche.

## Conclusione

In questo tutorial, abbiamo trattato il processo di creazione di un singolo PDF da un disegno CAD con diversi layout utilizzando Aspose.CAD per .NET. Questa potente libreria semplifica le attività di manipolazione CAD e offre flessibilità per vari scenari.

## Domande frequenti

### Q1: posso utilizzare Aspose.CAD per .NET con altri formati CAD?

A1: Sì, Aspose.CAD per .NET supporta vari formati CAD come DWG, DXF, DGN e altri.

### Q2: È disponibile una prova gratuita?

 A2: Sì, puoi esplorare una prova gratuita[Qui](https://releases.aspose.com/).

### Q3: Come posso ottenere supporto per Aspose.CAD per .NET?

 A3: Visita il[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) per il sostegno della comunità.

### Q4: Dove posso trovare la documentazione dettagliata?

 R4: Fare riferimento alla documentazione[Qui](https://reference.aspose.com/cad/net/).

### Q5: Posso acquistare una licenza per Aspose.CAD per .NET?

 A5: Sì, puoi acquistare una licenza[Qui](https://purchase.aspose.com/buy).