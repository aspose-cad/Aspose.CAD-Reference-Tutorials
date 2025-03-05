---
title: Impostazione delle dimensioni e della modalità della tela in Aspose.CAD per .NET
linktitle: Impostazione delle dimensioni e della modalità della tela
second_title: Aspose.CAD .NET - Formato file CAD e BIM
description: Esplora la guida passo passo sull'impostazione delle dimensioni e della modalità della tela in Aspose.CAD per .NET. Ottimizza facilmente il tuo rendering CAD utilizzando questo tutorial completo.
type: docs
weight: 16
url: /it/net/cad-features-and-support/setting-canvas-size-and-mode/
---
## introduzione

Sei pronto a sbloccare tutto il potenziale di Aspose.CAD per .NET e rivoluzionare la tua esperienza di rendering CAD? In questo tutorial passo passo, approfondiremo le complessità dell'impostazione delle dimensioni e della modalità della tela utilizzando la potente libreria Aspose.CAD. Che tu sia uno sviluppatore esperto o che tu abbia appena iniziato, questa guida ti guiderà attraverso il processo, assicurandoti di sfruttare le funzionalità di Aspose.CAD in modo efficace.

## Prerequisiti

Prima di immergerci nel tutorial, assicurati di disporre dei seguenti prerequisiti:

-  Libreria Aspose.CAD: scarica e installa la libreria Aspose.CAD dal file[Sito web Aspose.CAD](https://releases.aspose.com/cad/net/).

- Ambiente di sviluppo: assicurati di avere un ambiente di sviluppo .NET configurato sul tuo computer.

-  File CAD di esempio: per questo tutorial utilizzeremo un file DXF di esempio. Puoi trovarne uno in[Documentazione Aspose.CAD](https://reference.aspose.com/cad/net/).

## Importa spazi dei nomi

Per iniziare, importa gli spazi dei nomi necessari all'inizio della tua applicazione .NET:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Passaggio 1: caricare il file CAD

Inizia caricando il file CAD utilizzando il seguente codice:

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    //Il tuo codice per i passaggi successivi verrà inserito qui
}
```

## Passaggio 2: crea CadRasterizationOptions

 Crea un'istanza di`CadRasterizationOptions` e impostarne le proprietà:

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
rasterizationOptions.NoScaling = false;
```

## Passaggio 3: crea PdfOptions

 Crea un'istanza di`PdfOptions` e impostarlo`VectorRasterizationOptions` proprietà:

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Passaggio 4: esporta in PDF

Esporta il file CAD in PDF utilizzando le opzioni configurate:

```csharp
image.Save(MyDir + "result_out.pdf", pdfOptions);
```

## Passaggio 5: crea TiffOptions

 Crea un'istanza di`TiffOptions` e impostarlo`VectorRasterizationOptions` proprietà:

```csharp
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Passaggio 6: esporta in TIFF

Esporta il file CAD in TIFF utilizzando le opzioni configurate:

```csharp
image.Save(MyDir + "result_out.tiff", tiffOptions);
```

## Conclusione

Congratulazioni! Hai impostato correttamente le dimensioni e la modalità della tela in Aspose.CAD per .NET. Questa potente funzionalità apre un mondo di possibilità per il rendering CAD. Sperimenta diverse opzioni e scopri tutto il potenziale di Aspose.CAD nelle tue applicazioni .NET.

## Domande frequenti

### Q1: posso utilizzare Aspose.CAD con altre librerie .NET?

A1: Sì, Aspose.CAD si integra perfettamente con altre librerie .NET, fornendo funzionalità avanzate per la manipolazione CAD.

### Q2: È disponibile una prova gratuita per Aspose.CAD?

 A2: Sì, puoi esplorare le funzionalità di Aspose.CAD con una prova gratuita. Visita[Qui](https://releases.aspose.com/) per iniziare.

### Q3: Come posso ottenere supporto per Aspose.CAD?

 R3: Per supporto e discussioni, visitare il[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19).

### Q4: Dove posso trovare la documentazione completa per Aspose.CAD?

 R4: Fare riferimento a[Documentazione Aspose.CAD](https://reference.aspose.com/cad/net/) per informazioni dettagliate ed esempi.

### Q5: Come posso acquistare Aspose.CAD per .NET?

 A5: Per acquistare Aspose.CAD, visitare il[pagina di acquisto](https://purchase.aspose.com/buy).