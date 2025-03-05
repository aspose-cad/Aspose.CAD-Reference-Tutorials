---
title: Esportazione in formato BMP - Tutorial Aspose.CAD
linktitle: Esportazione in formato BMP
second_title: Aspose.CAD .NET - Formato file CAD e BIM
description: Esplora il mondo senza soluzione di continuità dell'esportazione di immagini 3D in BMP utilizzando Aspose.CAD per .NET. Segui il nostro tutorial per un'esperienza senza problemi.
type: docs
weight: 11
url: /it/net/file-format-conversion/exporting-to-bmp-format/
---
## introduzione

Nel dinamico mondo dello sviluppo software, Aspose.CAD per .NET si distingue come un potente strumento per la gestione di file CAD (Computer-Aided Design). Se stai cercando di esportare immagini CAD nel formato BMP ampiamente utilizzato, questo tutorial è la tua guida di riferimento. In questa procedura dettagliata, esploreremo il processo di esportazione di immagini 3D in BMP utilizzando Aspose.CAD per .NET. Immergiamoci!

## Prerequisiti

Prima di intraprendere questo tutorial, assicurati di disporre dei seguenti prerequisiti:

-  Aspose.CAD per .NET: scarica e installa la libreria Aspose.CAD da[Qui](https://releases.aspose.com/cad/net/).
- Ambiente di sviluppo: configurare un ambiente di sviluppo .NET.
- File CAD: avere un file CAD pronto per l'esportazione. Per questo esempio utilizzeremo "18-12-11 9644 - site.dwf".

## Importa spazi dei nomi

Nel tuo progetto .NET, assicurati di importare gli spazi dei nomi necessari:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

## Passaggio 1: caricare l'immagine CAD

Inizia caricando l'immagine CAD nel tuo progetto. Sostituisci "La tua directory dei documenti" con il percorso effettivo della directory.

```csharp
string MyDir = "Your Document Directory";
string inputFile = MyDir + "18-12-11 9644 - site.dwf";

using (Image image = Image.Load(inputFile))
{
    // Il tuo codice per caricare l'immagine va qui
}
```

## Passaggio 2: configura le opzioni di esportazione BMP

Configura le opzioni di esportazione BMP, comprese le opzioni di rasterizzazione vettoriale per i file CAD.

```csharp
BmpOptions bmpOptions = new BmpOptions();
var dwfRasterizationOptions = new CadRasterizationOptions();
bmpOptions.VectorRasterizationOptions = dwfRasterizationOptions;

dwfRasterizationOptions.PageHeight = 500;
dwfRasterizationOptions.PageWidth = 500;
```

## Passaggio 3: esporta in BMP

Esegui il processo di esportazione, specificando il percorso di output per il file BMP.

```csharp
string outPath = MyDir + "18-12-11 9644 - site.bmp";
image.Save(outPath, bmpOptions);
```

## Conclusione

Congratulazioni! Hai esportato con successo un'immagine 3D in BMP utilizzando Aspose.CAD per .NET. Questo tutorial offre uno sguardo sulla versatilità di Aspose.CAD, rendendo le attività complesse un gioco da ragazzi.

## Domande frequenti

### Q1: Posso utilizzare Aspose.CAD per .NET con qualsiasi formato di file CAD?

A1: Sì, Aspose.CAD supporta vari formati di file CAD, offrendo flessibilità nei tuoi progetti.

### Q2: È disponibile una licenza temporanea a scopo di test?

 A2: Certamente! È possibile ottenere una licenza temporanea[Qui](https://purchase.aspose.com/temporary-license/) Per la valutazione.

### Q3: Dove posso trovare la documentazione completa per Aspose.CAD?

 R3: Fare riferimento alla documentazione[Qui](https://reference.aspose.com/cad/net/) per informazioni dettagliate ed esempi.

### Q4: Come posso cercare supporto o connettermi con la comunità?

 A4: visitare il forum Aspose.CAD[Qui](https://forum.aspose.com/c/cad/19) porre domande e interagire con la comunità.

### Q5: Posso acquistare Aspose.CAD per .NET?

 A5: Sì, puoi acquistare Aspose.CAD[Qui](https://purchase.aspose.com/buy) per sbloccare tutto il suo potenziale per i tuoi progetti.
