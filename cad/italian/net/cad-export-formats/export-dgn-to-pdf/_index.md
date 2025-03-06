---
title: Esporta DGN in PDF in Aspose.CAD per .NET
linktitle: Esporta DGN in PDF
second_title: Aspose.CAD .NET - Formato file CAD e BIM
description: Scopri come esportare file DGN in PDF senza sforzo con Aspose.CAD per .NET. Una guida passo passo per una manipolazione fluida dei file CAD.
weight: 12
url: /it/net/cad-export-formats/export-dgn-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Esporta DGN in PDF in Aspose.CAD per .NET

## introduzione

Nel mondo dello sviluppo .NET, Aspose.CAD è una potente libreria che facilita la manipolazione e la conversione dei file CAD. Un'attività comune che gli sviluppatori incontrano spesso è l'esportazione di file DGN in formato PDF. In questo tutorial, esamineremo il processo passo dopo passo, utilizzando Aspose.CAD per .NET.

## Prerequisiti

Prima di immergerti nel tutorial, assicurati di avere a disposizione quanto segue:

- Una conoscenza pratica di C# e del framework .NET.
-  Aspose.CAD per la libreria .NET installata. Puoi scaricarlo[Qui](https://releases.aspose.com/cad/net/).
- Un file DGN di esempio, ad esempio "Nikon_D90_Camera.dgn" per questo tutorial.

## Importa spazi dei nomi

Nel tuo progetto C#, inizia importando gli spazi dei nomi necessari:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Passaggio 1: caricare il file DGN

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage cadImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Il tuo codice qui...
}
```

## Passaggio 2: configura le opzioni di rasterizzazione

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## Passaggio 3: crea opzioni PDF

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Passaggio 4: salva come PDF

```csharp
cadImage.Save(MyDir + "ExportDGNToPdf_out.pdf", pdfOptions);
```

## Conclusione

Congratulazioni! Hai esportato con successo un file DGN in PDF utilizzando Aspose.CAD per .NET. Questo tutorial ha trattato i passaggi essenziali, dal caricamento del file DGN alla configurazione delle opzioni di rasterizzazione e al salvataggio dell'output come PDF.

## Domande frequenti

### Q1: Posso utilizzare Aspose.CAD per .NET senza una conoscenza preliminare del CAD?

R1: Assolutamente! Aspose.CAD semplifica le attività CAD complesse, rendendolo accessibile a sviluppatori con background diversi.

### Q2: Dove posso trovare altri esempi e documentazione per Aspose.CAD?

 A2: Esplora il[documentazione](https://reference.aspose.com/cad/net/) per guide ed esempi completi.

### Q3: È disponibile una prova gratuita per Aspose.CAD?

R3: Sì, puoi ottenere una prova gratuita[Qui](https://releases.aspose.com/).

### Q4: Come posso ottenere licenze temporanee per Aspose.CAD?

 A4: ottenere licenze temporanee[Qui](https://purchase.aspose.com/temporary-license/).

### Q5: Hai bisogno di aiuto o hai domande?

A5: Visita il[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) per il sostegno della comunità.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
