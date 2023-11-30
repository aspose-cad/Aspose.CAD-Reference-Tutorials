---
title: Conversione di DWG in PDF di conformità - Tutorial Aspose.CAD
linktitle: Conversione di DWG in PDF di conformità
second_title: Aspose.CAD .NET - Formato file CAD e BIM
description: Converti DWG in PDF di conformità con Aspose.CAD per .NET. Segui il nostro tutorial per una guida passo passo.
type: docs
weight: 13
url: /it/net/conversion-and-export/converting-dwg-to-compliance-pdf/
---
## introduzione

Benvenuti nel nostro tutorial passo passo sulla conversione di file DWG in PDF di conformità utilizzando Aspose.CAD per .NET. Aspose.CAD è una potente API .NET che consente agli sviluppatori di lavorare senza sforzo con i formati di file CAD. In questo tutorial ti guideremo attraverso il processo di conversione di un file DWG in PDF di conformità con esempi e spiegazioni dettagliate.

## Prerequisiti

Prima di iniziare, assicurati di disporre dei seguenti prerequisiti:

-  Aspose.CAD per .NET: assicurati di avere la libreria Aspose.CAD integrata nel tuo progetto .NET. Puoi scaricarlo[Qui](https://releases.aspose.com/cad/net/).

- Ambiente di sviluppo: disporre di un ambiente di sviluppo .NET funzionante installato e assicurarsi che sia configurato correttamente.

- File DWG di esempio: scarica un file DWG di esempio che desideri convertire in PDF di conformità.

## Importa spazi dei nomi

Nel tuo progetto .NET, importa gli spazi dei nomi necessari per utilizzare le funzionalità Aspose.CAD.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

Ora suddividiamo il processo di conversione di un file DWG in PDF di conformità in più passaggi.

## Passaggio 1: caricare il file DWG

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

Aspose.CAD.Image cadImage = Aspose.CAD.Image.Load(sourceFilePath);
```

## Passaggio 2: imposta le opzioni di rasterizzazione

 Crea un'istanza di`CadRasterizationOptions` e configurarne le proprietà, come il colore di sfondo, la larghezza della pagina e l'altezza della pagina.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions
{
    BackgroundColor = Aspose.CAD.Color.White,
    PageWidth = 1600,
    PageHeight = 1600
};
```

## Passaggio 3: crea opzioni PDF

 Crea un'istanza di`PdfOptions` e impostare le opzioni di rasterizzazione vettoriale.

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions,
    CorePdfOptions = new PdfDocumentOptions { Compliance = PdfCompliance.PdfA1a }
};
```

## Passaggio 4: salvare come PDF (conformità A1a)

Salva l'immagine CAD come PDF di conformità con conformità A1a.

```csharp
cadImage.Save(MyDir + "PDFA1_A.pdf", pdfOptions);
```

## Passaggio 5: salva come PDF (conformità A1b)

Modificare il tipo di conformità in A1b e salvare l'immagine CAD come PDF di conformità.

```csharp
pdfOptions.CorePdfOptions.Compliance = PdfCompliance.PdfA1b;
cadImage.Save(MyDir + "PDFA1_B.pdf", pdfOptions);
```

## Conclusione

Congratulazioni! Hai convertito con successo un file DWG in PDF conformità utilizzando Aspose.CAD per .NET. Questo tutorial fornisce una guida completa per gli sviluppatori che desiderano integrare le funzionalità di conversione CAD nelle proprie applicazioni.

## Domande frequenti

### Q1: Posso convertire altri formati CAD in PDF conformità utilizzando Aspose.CAD?

A1: Sì, Aspose.CAD supporta vari formati CAD, consentendo la conversione in PDF conformità.

### Q2: Aspose.CAD è compatibile con .NET Core?

A2: Sì, Aspose.CAD è compatibile sia con .NET Framework che con .NET Core.

### Q3: Esistono opzioni di licenza per Aspose.CAD?

 R3: Sì, puoi esplorare le opzioni di licenza[Qui](https://purchase.aspose.com/buy).

### Q4: È disponibile una prova gratuita?

 R4: Sì, puoi ottenere una prova gratuita[Qui](https://releases.aspose.com/).

### Q5: Dove posso ottenere supporto per Aspose.CAD?

 A5: Visita il[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) per qualsiasi domanda relativa al supporto.