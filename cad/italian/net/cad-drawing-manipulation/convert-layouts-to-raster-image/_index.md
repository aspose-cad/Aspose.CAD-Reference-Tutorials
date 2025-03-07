---
title: Converti layout in immagini raster in Aspose.CAD per .NET
linktitle: Converti layout in immagini raster
second_title: Aspose.CAD .NET - Formato file CAD e BIM
description: Converti facilmente layout CAD in immagini raster utilizzando Aspose.CAD per .NET. Migliora il tuo sviluppo con potenti funzionalità di manipolazione CAD.
weight: 12
url: /it/net/cad-drawing-manipulation/convert-layouts-to-raster-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Converti layout in immagini raster in Aspose.CAD per .NET

## introduzione

Stai cercando di convertire facilmente i layout in immagini raster nelle tue applicazioni .NET? Non guardare oltre! Questa guida passo passo ti guiderà attraverso il processo utilizzando Aspose.CAD per .NET, una potente libreria che semplifica le attività di progettazione assistita da computer (CAD).

## Prerequisiti

Prima di immergerti nel tutorial, assicurati di disporre dei seguenti prerequisiti:

- Aspose.CAD per .NET Library: scarica e installa la libreria da[Pagina di download di Aspose.CAD per .NET](https://releases.aspose.com/cad/net/).

- Ambiente di sviluppo: assicurati di avere un ambiente di sviluppo .NET funzionante configurato sul tuo computer.

- Documento da convertire: prepara un documento CAD che contiene i layout che desideri convertire in immagini raster.

- La tua directory dei documenti: sostituisci il segnaposto "La tua directory dei documenti" nel codice con il percorso della directory dei tuoi documenti.

## Importa spazi dei nomi

Innanzitutto, importiamo gli spazi dei nomi necessari per rendere accessibili le funzionalità Aspose.CAD nel tuo codice.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Passaggio 1: caricare il documento CAD

Inizia caricando il documento CAD utilizzando la libreria Aspose.CAD.

```csharp
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image image = Image.Load(sourceFilePath))
{
    //Il tuo codice per i passaggi successivi verrà inserito qui
}
```

## Passaggio 2: configura le opzioni di rasterizzazione

 Crea un'istanza di`CadRasterizationOptions` per impostare la larghezza e l'altezza della pagina e specificare i layout che desideri convertire.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1200;
rasterizationOptions.PageHeight = 1200;
rasterizationOptions.Layouts = new string[] { "Model", "Layout1" };
```

## Passaggio 3: impostare le opzioni Tiff per l'immagine risultante

 Crea un'istanza di`TiffOptions`per definire il formato dell'immagine risultante.

```csharp
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.VectorRasterizationOptions = rasterizationOptions;
```

## Passaggio 4: salva l'immagine risultante

Specificare il percorso di output e salvare l'immagine convertita.

```csharp
string outputFilePath = MyDir + "conic_pyramid_layoutstorasterimage_out.tiff";
image.Save(outputFilePath, options);
```

## Conclusione

Congratulazioni! Hai convertito con successo i layout CAD in un formato di immagine raster utilizzando Aspose.CAD per .NET. Le possibilità sono vaste e questa guida funge da punto di partenza per le tue attività relative al CAD.

## Domande frequenti

### Q1: Aspose.CAD è compatibile con tutti i formati CAD?

 A1: Aspose.CAD supporta un'ampia gamma di formati CAD, inclusi DWG, DXF, DWF, STL e altri. Controlla il[documentazione](https://reference.aspose.com/cad/net/) per un elenco completo.

### Q2: Come posso ottenere una licenza temporanea per Aspose.CAD?

 A2: Visita il[pagina della licenza temporanea](https://purchase.aspose.com/temporary-license/) acquisire una licenza temporanea per scopi di test e valutazione.

### Q3: Dove posso trovare supporto per Aspose.CAD?

 A3: I forum sono il luogo ideale per cercare assistenza. Visitare il[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) per connettersi con la comunità e ottenere aiuto.

### Q4: Posso provare Aspose.CAD gratuitamente?

 A4: Assolutamente! Prendi il tuo[prova gratuita](https://releases.aspose.com/) per esplorare le caratteristiche e le capacità di Aspose.CAD.

### Q5: Dove posso acquistare una licenza per Aspose.CAD?

 A5: Passare a[pagina di acquisto](https://purchase.aspose.com/buy) per acquistare una licenza e sbloccare tutto il potenziale di Aspose.CAD.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
