---
title: Esportazione di DWG in PDF o immagini raster - Guida Aspose.CAD
linktitle: Esportazione di DWG in PDF o immagini raster
second_title: Aspose.CAD .NET - Formato file CAD e BIM
description: Esplora una guida completa sull'esportazione di DWG in PDF o immagini raster utilizzando Aspose.CAD per .NET. Scopri i passaggi, i prerequisiti e mettiti in pratica questa potente libreria.
type: docs
weight: 11
url: /it/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/
---
## introduzione

Desideri convertire senza problemi file DWG in PDF o immagini raster nella tua applicazione .NET? Non guardare oltre! Questa guida passo passo ti guiderà attraverso il processo utilizzando la potente libreria Aspose.CAD per .NET. Che tu sia uno sviluppatore esperto o che tu abbia appena iniziato, questo tutorial si rivolge a tutti i livelli di abilità.

## Prerequisiti

Prima di immergerci nel tutorial, assicurati di avere a disposizione quanto segue:

- Una conoscenza di base della programmazione .NET.
-  Aspose.CAD per la libreria .NET installata. In caso contrario, scaricalo[Qui](https://releases.aspose.com/cad/net/).
- Il tuo ambiente di sviluppo integrato (IDE) preferito configurato per lo sviluppo .NET.

## Importa spazi dei nomi

Iniziamo importando gli spazi dei nomi necessari nel tuo progetto .NET. Ciò garantisce che tu abbia accesso alla funzionalità Aspose.CAD nel tuo codice.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
```

## Passaggio 1: caricare il file DWG

Inizia caricando il file DWG che desideri convertire. Sostituisci "La tua directory dei documenti" con il percorso del tuo file DWG.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Il tuo codice per caricare DWG va qui
}
```

## Passaggio 2: imposta l'esportazione PDF

Ora configuriamo le impostazioni di esportazione PDF. Questo esempio dimostra come impostare il layout e gestire le conversioni di unità.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };

// Controllare e definire il sistema di unità
bool currentUnitIsMetric = false;
double currentUnitCoefficient = 1.0;
DefineUnitSystem(cadImage.UnitType, out currentUnitIsMetric, out currentUnitCoefficient);

// Il tuo codice per impostare l'esportazione in PDF va qui
```

## Passaggio 3: esporta in PDF

Esegui l'esportazione in PDF utilizzando le impostazioni configurate.

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath, pdfOptions);
```

## Passaggio 4: esporta in immagini raster

Estendi la funzionalità per esportare in immagini raster, come PNG.

```csharp
// Formato A4 a 300 DPI - 2480 x 3508
rasterizationOptions.PageHeight = 3508;
rasterizationOptions.PageWidth = 2480;

PngOptions pngOptions = new PngOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath.Replace("pdf", "png"), pngOptions);
```

## Conclusione

Congratulazioni! Hai imparato con successo come utilizzare Aspose.CAD per .NET per esportare file DWG sia in immagini PDF che raster. Questa potente libreria semplifica il processo, rendendolo efficiente e facile da usare per gli sviluppatori.

## Domande frequenti

### Q1: Posso utilizzare Aspose.CAD per .NET nei miei progetti commerciali?

 A1: Sì, puoi. Visita[buy.aspose.com/buy](https://purchase.aspose.com/buy) per i dettagli sulla licenza.

### Q2: È disponibile una prova gratuita?

 A2: Certamente! Ottieni la tua prova gratuita[Qui](https://releases.aspose.com/).

### Q3: Come posso ottenere supporto per Aspose.CAD per .NET?

 A3: vai al[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) per il sostegno della comunità.

### Q4: Posso ottenere una licenza temporanea a scopo di test?

R4: Sì, puoi ottenere una licenza temporanea[Qui](https://purchase.aspose.com/temporary-license/).

### Q5: Dove posso trovare la documentazione dettagliata?

 A5: La documentazione è disponibile all'indirizzo[Aspose.CAD](https://reference.aspose.com/cad/net/).