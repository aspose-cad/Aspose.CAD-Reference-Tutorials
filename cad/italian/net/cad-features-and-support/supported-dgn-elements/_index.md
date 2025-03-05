---
title: Elementi DGN supportati in Aspose.CAD per .NET
linktitle: Elementi DGN supportati
second_title: Aspose.CAD .NET - Formato file CAD e BIM
description: Esplora Aspose.CAD per le potenti funzionalità di .NET per la gestione dei file DGN. Segui la nostra guida passo passo per lavorare senza problemi con elementi 2D e 3D.
type: docs
weight: 18
url: /it/net/cad-features-and-support/supported-dgn-elements/
---
## introduzione

Sei uno sviluppatore .NET che desidera lavorare senza problemi con i file DGN? Aspose.CAD per .NET fornisce una soluzione solida per gestire i file DGN in modo efficiente. In questo tutorial, approfondiremo gli elementi DGN supportati, guidandoti attraverso il processo di lavoro con Aspose.CAD per .NET.

## Prerequisiti

Prima di iniziare, assicurati di avere quanto segue:

- Conoscenza base della programmazione .NET.
- Visual Studio installato sul tuo computer.
-  Libreria Aspose.CAD per .NET, che puoi scaricare[Qui](https://releases.aspose.com/cad/net/).

## Importa spazi dei nomi

Per avviare il tuo progetto, importa gli spazi dei nomi necessari nella tua applicazione .NET. Questo passaggio garantisce l'accesso alle funzionalità fornite da Aspose.CAD per .NET.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.FileFormats.Dgn.DgnElements;
```

## Passaggio 1: caricare il file DGN

Inizia caricando un file DGN esistente come CadImage nella tua applicazione .NET.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Il tuo codice qui
}
```

## Passaggio 2: scorrere gli elementi DGN

Scorrere gli elementi DGN utilizzando un ciclo foreach. Aspose.CAD per .NET fornisce una varietà di tipi di elementi DGN con cui è possibile lavorare.

```csharp
foreach (DgnDrawingElementBase element in dgnImage.Elements)
{
    // Il tuo codice qui
}
```

## Passaggio 3: gestire le entità supportate in precedenza

Gestisci le entità 2D precedentemente supportate, che ora sono supportate anche per il 3D.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.Line:
    case DgnElementType.Ellipse:
    case DgnElementType.Curve:
    // Casi aggiuntivi
        {
            // Il tuo codice qui
            break;
        }
}
```

## Passaggio 4: gestire le entità 3D supportate

Gestisci le entità 3D supportate fornite da Aspose.CAD per .NET.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.SolidHeader3D:
    case DgnElementType.Cone:
    case DgnElementType.CellHeader:
        {
            // Il tuo codice qui
            break;
        }
}
```

## Passaggio 5: esporta e salva

Infine, esporta il file DGN modificato in un'immagine raster e salvalo nella directory specificata.

```csharp
Console.WriteLine("\nThe DGN file exported successfully to raster image.\nFile saved at " + MyDir);
```

## Conclusione

In questo tutorial, abbiamo esplorato le funzionalità di Aspose.CAD per .NET nella gestione e manipolazione dei file DGN. Seguendo la guida passo passo, puoi lavorare in modo efficiente con gli elementi DGN supportati, siano essi entità 2D o 3D. Aspose.CAD per .NET ti consente di integrare perfettamente l'elaborazione dei file DGN nelle tue applicazioni .NET.

## Domande frequenti

### Q1: Dove posso trovare la documentazione per Aspose.CAD per .NET?

 A1: È possibile trovare la documentazione[Qui](https://reference.aspose.com/cad/net/).

### Q2: Come posso scaricare Aspose.CAD per .NET?

 A2: È possibile scaricare la libreria[Qui](https://releases.aspose.com/cad/net/).

### Q3: È disponibile una prova gratuita per Aspose.CAD per .NET?

 R3: Sì, puoi accedere alla prova gratuita[Qui](https://releases.aspose.com/).

### Q4: Dove posso ottenere licenze temporanee per Aspose.CAD per .NET?

 A4: Sono disponibili licenze temporanee[Qui](https://purchase.aspose.com/temporary-license/).

### Q5: Hai bisogno di aiuto o hai domande?

 A5: Visita la comunità Aspose.CAD per .NET[Forum di assistenza](https://forum.aspose.com/c/cad/19).