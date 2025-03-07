---
title: Supporto di 3D per DGN V7 in Aspose.CAD per .NET
linktitle: Supporto del 3D per DGN V7
second_title: Aspose.CAD .NET - Formato file CAD e BIM
description: Sblocca la potenza del supporto 3D per DGN V7 in Aspose.CAD per .NET. Segui il nostro tutorial passo dopo passo.
weight: 20
url: /it/net/cad-features-and-support/support-of-3d-for-dgn-v7/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Supporto di 3D per DGN V7 in Aspose.CAD per .NET

## introduzione

Benvenuti nel nostro tutorial completo su come sfruttare il supporto di 3D per DGN V7 in Aspose.CAD per .NET! Aspose.CAD è una potente libreria che consente agli sviluppatori di lavorare senza problemi con i file CAD nelle loro applicazioni .NET. In questo tutorial esploreremo i passaggi per utilizzare il supporto 3D per DGN V7, fornendoti le conoscenze per migliorare i tuoi progetti relativi al CAD.

## Prerequisiti

Prima di immergerti nel tutorial, assicurati di avere i seguenti prerequisiti:

-  Aspose.CAD per .NET: assicurati di avere Aspose.CAD per .NET installato. In caso contrario, puoi scaricarlo da[Qui](https://releases.aspose.com/cad/net/).

- Ambiente di sviluppo: configurare un ambiente di sviluppo adatto, come Visual Studio, per lo sviluppo di applicazioni .NET.

- File DGN di esempio: avere un file DGN di esempio pronto per il test. È possibile utilizzare il file di esempio fornito "Nikon_D90_Camera.dgn".

Ora passiamo ai passaggi per ottenere il supporto 3D per DGN V7 utilizzando Aspose.CAD per .NET!

## Importa spazi dei nomi

Nella tua applicazione .NET, inizia importando gli spazi dei nomi necessari:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.ImageOptions;
```

## Passaggio 1: imposta la directory dei documenti

 Assicurati di avere una directory dei documenti impostata nel tuo progetto. Sostituire`"Your Document Directory"` con il percorso effettivo della directory dei documenti.

```csharp
string MyDir = "Your Document Directory";
```

## Passaggio 2: caricare il file DGN

Carica il file DGN esistente come CadImage utilizzando il seguente codice:

```csharp
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";
string outFile = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Il tuo codice per l'ulteriore elaborazione va qui
}
```

## Passaggio 3: configura le opzioni di esportazione PDF

Configura le opzioni per l'esportazione in PDF, specificando le opzioni di rasterizzazione vettoriale come dimensioni della pagina, ridimensionamento automatico dei layout, colore di sfondo e layout da esportare.

```csharp
var options = new PdfOptions
{
    VectorRasterizationOptions = new CadRasterizationOptions
    {
        PageWidth = 1500,
        PageHeight = 1500,
        AutomaticLayoutsScaling = true,
        BackgroundColor = Color.Black,
        Layouts = new string[] { "1", "2", "3", "9" } // Esporta solo le visualizzazioni specificate
    }
};
```

## Passaggio 4: salva l'immagine raster

Salvare il file DGN come immagine raster con le opzioni configurate.

```csharp
dgnImage.Save(outFile, options);
```

## Conclusione

Congratulazioni! Hai utilizzato con successo Aspose.CAD per .NET per esportare un file DGN con supporto 3D in un'immagine raster. Questo tutorial ti ha fornito i passaggi essenziali per integrare questa funzionalità nei tuoi progetti CAD.

## Domande frequenti

### Q1: Posso utilizzare Aspose.CAD per .NET con altri formati di file CAD?

A1: Sì, Aspose.CAD supporta vari formati di file CAD, inclusi DWG e DXF.

### Q2: Come posso gestire le eccezioni quando lavoro con Aspose.CAD?

A2: racchiudi il codice in un blocco try-catch, come dimostrato nell'esempio fornito, per gestire le eccezioni in modo corretto.

### Q3: Aspose.CAD è adatto a progetti commerciali?

 A3: Assolutamente! È possibile acquistare Aspose.CAD per .NET[Qui](https://purchase.aspose.com/buy).

### Q4: Posso provare Aspose.CAD per .NET prima dell'acquisto?

A4: Certamente! Esplora la prova gratuita[Qui](https://releases.aspose.com/).

### Q5: Dove posso trovare il supporto della community per Aspose.CAD per .NET?

 A5: Visita il forum della community[Qui](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
