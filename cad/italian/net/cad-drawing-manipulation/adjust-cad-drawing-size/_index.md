---
title: Regolazione delle dimensioni del disegno CAD in Aspose.CAD per .NET
linktitle: Regolazione delle dimensioni del disegno CAD
second_title: Aspose.CAD .NET - Formato file CAD e BIM
description: Scopri come regolare facilmente le dimensioni dei disegni CAD in .NET utilizzando Aspose.CAD. Segui la nostra guida passo passo per un ridimensionamento senza interruzioni.
type: docs
weight: 10
url: /it/net/cad-drawing-manipulation/adjust-cad-drawing-size/
---
## introduzione

Desideri regolare facilmente le dimensioni dei disegni CAD nelle tue applicazioni .NET? Aspose.CAD per .NET fornisce una soluzione solida, che consente di gestire senza sforzo il ridimensionamento dei disegni CAD. In questo tutorial, ti guideremo attraverso il processo, analizzando ogni passaggio per assicurarti di cogliere le complessità del ridimensionamento dei disegni CAD utilizzando Aspose.CAD.

## Prerequisiti

Prima di immergerci nel tutorial, assicurati di disporre dei seguenti prerequisiti:

- Aspose.CAD per .NET Library: scarica e installa la libreria da[Pagina di download di Aspose.CAD per .NET](https://releases.aspose.com/cad/net/).
- Disegno CAD di esempio: assicurati di avere un file di disegno CAD di esempio (ad esempio, "sample.dwg") nella directory dei documenti.

## Importa spazi dei nomi

Inizia importando gli spazi dei nomi necessari nell'applicazione .NET. Questo passaggio è fondamentale per accedere alle funzionalità fornite da Aspose.CAD per .NET.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Passaggio 1: caricare il disegno CAD

Inizia caricando il disegno CAD in un'istanza della classe Aspose.CAD.Image. Assicurati di avere il percorso file corretto per il tuo disegno di esempio.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "sample.dwg";

// Carica un disegno CAD in un'istanza di Immagine
using (var image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // Il tuo codice qui...
}
```

## Passaggio 2: crea BmpOptions

Crea un'istanza della classe BmpOptions, responsabile della specifica delle opzioni durante il salvataggio del disegno CAD come file BMP.

```csharp
Aspose.CAD.ImageOptions.BmpOptions bmpOptions = new Aspose.CAD.ImageOptions.BmpOptions();
```

## Passaggio 3: imposta le opzioni di CadRasterizzazione

Creare un'istanza della classe CadRasterizationOptions e configurarne le proprietà per la rasterizzazione vettoriale.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions cadRasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
bmpOptions.VectorRasterizationOptions = cadRasterizationOptions;
```

## Passaggio 4: imposta la proprietà UnitType

Imposta la proprietà UnitType di CadRasterizationOptions per specificare il tipo di unità per il ridimensionamento. In questo esempio è impostato su Centimetro.

```csharp
cadRasterizationOptions.UnitType = Aspose.CAD.ImageOptions.UnitType.Centimeter;
```

## Passaggio 5: imposta la proprietà dei layout

Specifica i layout che desideri includere nel disegno ridimensionato impostando la proprietà Layouts.

```csharp
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## Passaggio 6: esporta in BMP

Infine, salva il layout ridimensionato come file BMP utilizzando il metodo Salva.

```csharp
string outPath = sourceFilePath + ".bmp";
image.Save(outPath, bmpOptions);
```

Ora hai modificato con successo le dimensioni del tuo disegno CAD utilizzando Aspose.CAD per .NET!

## Conclusione

In questo tutorial, abbiamo esaminato il processo di ridimensionamento dei disegni CAD in .NET utilizzando Aspose.CAD. Seguendo questi passaggi, puoi integrare perfettamente questa funzionalità nelle tue applicazioni, offrendo un'esperienza utente fluida.

## Domande frequenti

### Q1: Aspose.CAD per .NET è compatibile con tutti i formati CAD?

 A1: Aspose.CAD per .NET supporta un'ampia gamma di formati CAD, inclusi DWG, DXF, DWF e altri. Controlla il[documentazione](https://reference.aspose.com/cad/net/) per l'elenco completo.

### Q2: Posso ridimensionare più layout contemporaneamente?

R2: Sì, puoi ridimensionare più layout regolando la matrice dei layout in CadRasterizationOptions.

### Q3: Dove posso ottenere supporto per Aspose.CAD per .NET?

 A3: Visita il[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) per il sostegno e l'assistenza della comunità.

### Q4: È disponibile una prova gratuita?

 A4: Sì, puoi esplorare a[prova gratuita](https://releases.aspose.com/) per valutare le funzionalità di Aspose.CAD per .NET.

### Q5: Come posso ottenere una licenza temporanea per Aspose.CAD per .NET?

 A5: ottenere una licenza temporanea a scopo di test[Qui](https://purchase.aspose.com/temporary-license/).