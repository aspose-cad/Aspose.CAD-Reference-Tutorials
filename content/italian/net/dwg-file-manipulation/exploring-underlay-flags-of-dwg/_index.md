---
title: Esplorazione dei flag underlay dei file DWG - Tutorial Aspose.CAD
linktitle: Esplorazione dei flag di underlay dei file DWG
second_title: Aspose.CAD .NET - Formato file CAD e BIM
description: Sblocca la potenza di Aspose.CAD per .NET nell'esplorazione dei flag di sottoposizione dei file DWG. Segui la nostra guida passo passo.
type: docs
weight: 13
url: /it/net/dwg-file-manipulation/exploring-underlay-flags-of-dwg/
---
## introduzione

Se stai addentrandoti nell'intricato mondo dei file CAD, in particolare dei file DWG, e desideri svelare i misteri delle bandiere del underlay, sei nel posto giusto. Questo tutorial ti guiderà attraverso il processo di esplorazione dei flag di underlay nei file DWG utilizzando la potente libreria Aspose.CAD per .NET.

## Prerequisiti

Prima di immergerci nel tutorial, assicurati di avere quanto segue:

- Una conoscenza di base della programmazione C# e .NET.
-  Aspose.CAD per la libreria .NET installata. In caso contrario, puoi scaricarlo[Qui](https://releases.aspose.com/cad/net/).
- Un file DWG per il test. È possibile utilizzare il file di esempio "BlockRefDgn.dwg" fornito nel tutorial.

## Importa spazi dei nomi

Per iniziare, devi importare gli spazi dei nomi necessari. Ecco uno snippet per aiutarti:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;

```

## Passaggio 1: carica il file DWG e converti in CadImage

Inizia caricando il file DWG esistente e convertendolo in CadImage:

```csharp
string fileName = MyDir + "BlockRefDgn.dwg";

// Carica il file DWG e convertilo in CadImage
using (CadImage image = (CadImage)Image.Load(fileName))
{
    // Il tuo codice per i passaggi successivi andrà qui
}
```

## Passaggio 2: scorrere le entità

Successivamente, scorrere ciascuna entità all'interno del file DWG:

```csharp
foreach (CadBaseEntity entity in image.Entities)
{
    // Il tuo codice per i passaggi successivi andrà qui
}
```

## Passaggio 3: verificare il tipo CadDgnUnderlay

Controlla se l'entità è di tipo CadDgnUnderlay:

```csharp
if (entity is CadDgnUnderlay)
{
    // Il tuo codice per i passaggi successivi andrà qui
}
```

## Passaggio 4: accedi ai flag del underlay

Accedi a diversi flag di underlay ed estrai informazioni rilevanti:

```csharp
CadUnderlay underlay = entity as CadUnderlay;

Console.WriteLine(underlay.UnderlayPath);
Console.WriteLine(underlay.UnderlayName);
Console.WriteLine(underlay.InsertionPoint.X);
Console.WriteLine(underlay.InsertionPoint.Y);
Console.WriteLine(underlay.RotationAngle);
Console.WriteLine(underlay.ScaleX);
Console.WriteLine(underlay.ScaleY);
Console.WriteLine(underlay.ScaleZ);
Console.WriteLine((underlay.Flags & UnderlayFlags.UnderlayIsOn) == UnderlayFlags.UnderlayIsOn);
Console.WriteLine((underlay.Flags & UnderlayFlags.ClippingIsOn) == UnderlayFlags.ClippingIsOn);
Console.WriteLine((underlay.Flags & UnderlayFlags.Monochrome) != UnderlayFlags.Monochrome);
```

## Conclusione

Congratulazioni! Hai esplorato con successo i flag underlay dei file DWG utilizzando Aspose.CAD per .NET. Questo tutorial ti ha fornito le conoscenze necessarie per navigare tra le entità ed estrarre informazioni cruciali sugli underlay.

## Domande frequenti

### Q1: Posso utilizzare Aspose.CAD per .NET con altri formati di file CAD?

A1: Aspose.CAD supporta vari formati CAD, inclusi DWG, DXF, DGN e altri. Controlla la documentazione per l'elenco completo.

### Q2: È disponibile una licenza temporanea per Aspose.CAD per .NET?

 R2: Sì, puoi ottenere una licenza temporanea[Qui](https://purchase.aspose.com/temporary-license/).

### Q3: Dove posso trovare supporto per Aspose.CAD per .NET?

 R3: Visita il forum di supporto[Qui](https://forum.aspose.com/c/cad/19) per assistenza.

### Q4: Come posso acquistare Aspose.CAD per .NET?

A4: Acquista la libreria[Qui](https://purchase.aspose.com/buy).

### Q5: È disponibile una prova gratuita?

 R5: Sì, puoi accedere alla prova gratuita[Qui](https://releases.aspose.com/).
