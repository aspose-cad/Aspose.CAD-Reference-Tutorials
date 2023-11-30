---
title: Esporta DGN come parte di DWG in Aspose.CAD per .NET
linktitle: Esporta DGN come parte di DWG
second_title: Aspose.CAD .NET - Formato file CAD e BIM
description: Scopri come esportare DGN come parte di DWG in Aspose.CAD per .NET. Segui la nostra guida passo passo per un'integrazione perfetta.
type: docs
weight: 11
url: /it/net/cad-export-formats/export-dgn-as-part-of-dwg/
---
## introduzione

Nel mondo dello sviluppo .NET, Aspose.CAD si distingue come una potente libreria per lavorare con file CAD (Computer-Aided Design). Questo tutorial ti guiderà attraverso il processo di esportazione di un file DGN (disegno) come parte di un file DWG (disegno) utilizzando Aspose.CAD per .NET. Che tu sia uno sviluppatore esperto o che tu abbia appena iniziato, questa guida passo passo ti aiuterà a sfruttare le funzionalità di Aspose.CAD per raggiungere questo compito specifico in modo efficiente.

## Prerequisiti

Prima di immergerti nel tutorial, assicurati di avere i seguenti prerequisiti:

-  Aspose.CAD per .NET: assicurati di avere la libreria Aspose.CAD per .NET installata. Puoi scaricarlo[Qui](https://releases.aspose.com/cad/net/).

- Ambiente di sviluppo: configura il tuo ambiente di sviluppo .NET preferito, come Visual Studio.

- Conoscenza di base di C#: familiarizzare con il linguaggio di programmazione C#.

## Importa spazi dei nomi

Nel tuo progetto C#, includi gli spazi dei nomi necessari per accedere alla funzionalità Aspose.CAD. Aggiungi le seguenti direttive using all'inizio del file di codice:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

Ora suddividiamo il codice fornito in più passaggi:

## Passaggio 1: definire i percorsi dei file

```csharp
//Percorsi dei file di input e output
string fileName = "BlockRefDgn.dwg";
string outPath = fileName + ".pdf";
```

## Passaggio 2: crea un'istanza PdfOptions

```csharp
// Crea un'istanza della classe PdfOptions per esportare DWG in PDF
PdfOptions exportOptions = new PdfOptions();
```

## Passaggio 3: caricare il file DWG

```csharp
// Carica il file DWG esistente come immagine e convertilo nel tipo CadImage
using (CadImage cadImage = (CadImage)Image.Load(fileName))
```

## Passaggio 4: scorrere le entità

```csharp
// Scorrere ogni entità all'interno del file DWG
foreach (CadBaseEntity baseEntity in cadImage.Entities)
```

## Passaggio 5: controlla il tipo di entità

```csharp
// Controlla se l'entità è una definizione di immagine
if (baseEntity.TypeName == CadEntityTypeName.DGNUNDERLAY)
```

## Passaggio 6: ottieni il percorso sottostante

```csharp
// Se si tratta di una definizione di immagine, ottieni il riferimento esterno all'oggetto
CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
Console.WriteLine(dgnFile.UnderlayPath);
```

## Passaggio 7: definire le opzioni di rasterizzazione

```csharp
// Definire le impostazioni per l'oggetto CadRasterizationOptions
exportOptions.VectorRasterizationOptions = new CadRasterizationOptions()
{
    PageWidth = 1600,
    PageHeight = 1600,
    Layouts = new string[] { "Model" },
    AutomaticLayoutsScaling = false,
    NoScaling = true,
    BackgroundColor = Color.Black,
    DrawType = CadDrawTypeMode.UseObjectColor
};
```

## Passaggio 8: esporta DWG in PDF

```csharp
// Esporta il DWG in PDF chiamando il metodo Salva
cadImage.Save(outPath, exportOptions);
```

## Conclusione

Congratulazioni! Hai seguito con successo il processo di esportazione di un file DGN come parte di un file DWG utilizzando Aspose.CAD per .NET. Questo tutorial ti ha fornito i passaggi fondamentali e gli snippet di codice per realizzare questa attività specifica senza problemi.

## Domande frequenti

### Q1: Posso utilizzare Aspose.CAD per .NET nei miei progetti commerciali?
 A1: Sì, puoi. Visita[Qui](https://purchase.aspose.com/buy) per esplorare le opzioni di licenza.

### D2: Esistono limitazioni sulla dimensione dei file DWG che posso elaborare?
A2: Aspose.CAD supporta la gestione di file DWG di grandi dimensioni, ma potrebbero essere applicate limitazioni hardware.

### Q3: È disponibile una versione di prova?
 R3: Sì, puoi ottenere una prova gratuita[Qui](https://releases.aspose.com/).

### Q4: Come posso ottenere licenze temporanee?
 A4: È possibile ottenere licenze temporanee[Qui](https://purchase.aspose.com/temporary-license/).

### Q5: Dove posso chiedere assistenza se riscontro problemi?
 A5: È possibile visitare il forum Aspose.CAD[Qui](https://forum.aspose.com/c/cad/19) per supporto.