---
title: Esporta DGN in immagine raster in Aspose.CAD per .NET
linktitle: Esporta DGN in immagine raster
second_title: Aspose.CAD .NET - Formato file CAD e BIM
description: Converti DGN in immagini raster senza sforzo utilizzando Aspose.CAD per .NET. Esplora la guida passo passo e libera la potenza di .NET nella manipolazione dei file CAD.
weight: 13
url: /it/net/cad-export-formats/export-dgn-to-raster-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Esporta DGN in immagine raster in Aspose.CAD per .NET

## introduzione

Nel regno dinamico dello sviluppo .NET, Aspose.CAD emerge come un potente strumento per la gestione di file CAD (Computer-Aided Design). Questo tutorial approfondisce il processo di esportazione di file DGN in immagini raster utilizzando Aspose.CAD per .NET. Se desideri trasformare senza problemi i tuoi file DGN in immagini raster visivamente accattivanti, sei nel posto giusto.

## Prerequisiti

Prima di intraprendere questo viaggio, assicurati di disporre dei seguenti prerequisiti:

-  Aspose.CAD per .NET: assicurati di avere la libreria Aspose.CAD installata nel tuo progetto .NET. Puoi trovare la libreria e la documentazione pertinente su[sito web](https://reference.aspose.com/cad/net/).

- File DGN di esempio: avere un file DGN pronto per la conversione. Nel nostro esempio utilizzeremo "Nikon_D90_Camera.dgn".

Ora tuffiamoci nella guida passo passo.

## Importa spazi dei nomi

Nel tuo progetto .NET, inizia importando gli spazi dei nomi necessari per Aspose.CAD. Questo passaggio consente di accedere alle classi e ai metodi richiesti per la conversione di immagini DGN in raster.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Passaggio 1: caricare il file DGN

 Inizia caricando il file DGN in un file`CadImage` oggetto. Ciò fornisce una base per le operazioni successive.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Il tuo codice per l'ulteriore elaborazione va qui
}
```

## Passaggio 2: definire le opzioni di rasterizzazione

 Creare un`CadRasterizationOptions` oggetto e impostare varie proprietà per personalizzare il processo di rasterizzazione in base alle proprie esigenze.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## Passaggio 3: crea l'oggetto JpegOptions

 Poiché il nostro obiettivo è convertire il file DGN in JPEG, crea un file`JpegOptions` oggetto e assegnare quello precedentemente definito`CadRasterizationOptions` ad esso.

```csharp
ImageOptionsBase options = new JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
```

## Passaggio 4: salva l'immagine raster

 Utilizza il`Save` metodo del`CadImage` per esportare il file DGN in un'immagine raster nel formato desiderato, in questo caso JPEG.

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpg", options);
```

## Conclusione

Congratulazioni! Hai seguito con successo i passaggi per esportare un file DGN in un'immagine raster utilizzando Aspose.CAD per .NET. Questo tutorial ti ha fornito le conoscenze essenziali per integrare facilmente questa funzionalità nei tuoi progetti .NET.

## Domande frequenti

### D1: Posso esportare file DGN in formati diversi da JPEG?

A1: Sì, Aspose.CAD per .NET supporta vari formati di output. È possibile modificare le opzioni di conseguenza nel passaggio 3.

### Q2 Come posso gestire le eccezioni durante il processo di conversione?

R2: Assicurati di avere una corretta gestione delle eccezioni, come dimostrato nel codice fornito, per risolvere potenziali problemi.

### Q3: È disponibile una versione di prova per Aspose.CAD per .NET?

 R3: Sì, puoi esplorare il prodotto con una prova gratuita. Visita[Qui](https://releases.aspose.com/) per maggiori informazioni.

### Q4: Dove posso chiedere assistenza o discutere problemi relativi ad Aspose.CAD per .NET?

 A4: Vai al[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) per il supporto e le discussioni della comunità.

### Q5: Come posso ottenere una licenza temporanea per Aspose.CAD per .NET?

 A5: Visita[questo link](https://purchase.aspose.com/temporary-license/)per acquisire una licenza temporanea per le tue esigenze di sviluppo.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
