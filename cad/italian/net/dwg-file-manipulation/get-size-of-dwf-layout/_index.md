---
title: Lavorare con file DWG in C# ottieni la dimensione del layout DWF
linktitle: Lavorare con file DWG in C# ottieni la dimensione del layout DWF
second_title: Aspose.CAD .NET - Formato file CAD e BIM
description: Esplora la potenza di Aspose.CAD per .NET nella gestione dei file DWG. Impara a estrarre facilmente le dimensioni del layout DWF utilizzando C#.
type: docs
weight: 10
url: /it/net/dwg-file-manipulation/get-size-of-dwf-layout/
---
## introduzione

Nel regno della progettazione assistita da computer (CAD) e dello sviluppo .NET, Aspose.CAD si pone come un potente strumento per la gestione dei file DWG. Questo tutorial ti guiderà attraverso il processo di lavoro con i file DWG in C# e di estrazione delle dimensioni di un layout DWF. Prima di immergerci nel codice, assicuriamoci di avere tutto pronto per intraprendere questo viaggio.

## Prerequisiti

Per seguire questo tutorial senza problemi, assicurati di disporre dei seguenti prerequisiti:

-  Aspose.CAD per .NET: assicurati di avere Aspose.CAD per .NET installato. Puoi scaricarlo da[Pagina di download di Aspose.CAD per .NET](https://releases.aspose.com/cad/net/).

Ora che hai gli strumenti necessari, passiamo all'arena della codifica.

## Importa spazi dei nomi

Prima di iniziare a lavorare con il codice, importiamo gli spazi dei nomi richiesti:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Dwf;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

Questi spazi dei nomi forniranno le classi e i metodi essenziali per la gestione dei file CAD con Aspose.CAD nell'applicazione C#.

## Passaggio 1: configura il tuo ambiente

Inizia assicurandoti di avere configurato l'ambiente corretto per il tuo progetto. Fai riferimento alla libreria Aspose.CAD nel tuo progetto C#.

## Passaggio 2: definire i percorsi dei file

Definisci i percorsi per il tuo file DWG e la directory di output per i file JPG generati:

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "blocks_and_tables.dwf";
```

## Passaggio 3: caricare l'immagine DWF

Carica l'immagine DWF utilizzando Aspose.CAD:

```csharp
using (DwfImage image = (DwfImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    // Il codice per i passaggi successivi andrà qui
}
```

## Passaggio 4: scorrere le pagine

Scorri le pagine dell'immagine DWF:

```csharp
foreach (var page in image.Pages)
{
    // Il codice per i passaggi successivi andrà qui
}
```

## Passaggio 5: ottieni informazioni sul layout

Ottieni informazioni sul layout da ogni pagina:

```csharp
var layout = page.Name;
System.Console.WriteLine("Layout= " + layout);
```

## Passaggio 6: imposta le opzioni JPG

Configura le opzioni per salvare il layout come file JPG:

```csharp
using (FileStream fs = new FileStream(MyDir + "layout_" + layout + ".jpg", FileMode.Create))
{
    JpegOptions jpegOptions = new JpegOptions();
    CadRasterizationOptions options = new CadRasterizationOptions();
    options.Layouts = new string[] { layout };
    // Il codice per i passaggi successivi andrà qui
}
```

## Passaggio 7: determinare la dimensione della pagina

Determinare la dimensione del layout DWF:

```csharp
double sizeExtX = page.MaxPoint.X - page.MinPoint.X;
double sizeExtY = page.MaxPoint.Y - page.MinPoint.Y;
// Il codice per i passaggi successivi andrà qui
```

## Passaggio 8: imposta le dimensioni della pagina

Imposta le dimensioni della pagina in base al tipo di unità:

```csharp
if (page.UnitType == UnitType.Inch)
{
    options.PageHeight = CommonHelper.INtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.INtoPixels(sizeExtX, CommonHelper.DPI);
}
else if (page.UnitType == UnitType.Millimeter)
{
    options.PageHeight = CommonHelper.MMtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.MMtoPixels(sizeExtX, CommonHelper.DPI);
}
else
{
    options.PageHeight = (float)sizeExtY;
    options.PageWidth = (float)sizeExtX;
}
```

## Passaggio 9: salva il file JPG

Salva il file JPG con le opzioni specificate:

```csharp
jpegOptions.VectorRasterizationOptions = options;
image.Save(fs, jpegOptions);
}
```

Ora hai estratto con successo la dimensione del layout DWF dal file DWG utilizzando Aspose.CAD in C#. Sentiti libero di esplorare ulteriori caratteristiche e funzionalità offerte da Aspose.CAD per lo sviluppo .NET.

## Conclusione

In questo tutorial, abbiamo esaminato il processo di lavoro con i file DWG in C# utilizzando Aspose.CAD. Seguendo questi passaggi, non solo puoi ottenere le dimensioni di un layout DWF, ma anche sfruttare le funzionalità di Aspose.CAD per varie attività relative al CAD nei tuoi progetti .NET.

## Domande frequenti

### Q1: Aspose.CAD è compatibile con gli ultimi formati di file DWG?

 A1: Aspose.CAD supporta vari formati di file DWG, incluse le ultime versioni. Fare riferimento al[documentazione](https://reference.aspose.com/cad/net/) per dettagli specifici sulla compatibilità.

### Q2: Posso utilizzare Aspose.CAD sia per progetti commerciali che personali?

 A2: Sì, Aspose.CAD offre opzioni di licenza flessibili sia per uso commerciale che personale. Visitare il[pagina di acquisto](https://purchase.aspose.com/buy) per ulteriori dettagli.

### Q3: Come posso ottenere una licenza temporanea per Aspose.CAD?

 A3: Puoi ottenere una licenza temporanea da[Qui](https://purchase.aspose.com/temporary-license/) a fini di valutazione.

### Q4: Dove posso trovare supporto per Aspose.CAD?

R4: Per qualsiasi domanda o assistenza, visitare il[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19).

### Q5: È disponibile una prova gratuita per Aspose.CAD?

 A5: Sì, puoi accedere a una versione di prova gratuita di Aspose.CAD[Qui](https://releases.aspose.com/).