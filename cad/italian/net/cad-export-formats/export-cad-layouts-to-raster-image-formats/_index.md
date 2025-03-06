---
title: Esporta layout CAD in formati di immagine raster in Aspose.CAD per .NET
linktitle: Esporta layout CAD in formati di immagine raster
second_title: Aspose.CAD .NET - Formato file CAD e BIM
description: Scopri come esportare layout CAD in immagini raster utilizzando Aspose.CAD per .NET. Segui la nostra guida passo passo per una conversione senza problemi.
weight: 10
url: /it/net/cad-export-formats/export-cad-layouts-to-raster-image-formats/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Esporta layout CAD in formati di immagine raster in Aspose.CAD per .NET

## introduzione

Stai cercando di convertire in modo efficiente i layout CAD in formati di immagine raster utilizzando Aspose.CAD per .NET? Questa guida passo passo ti guiderà attraverso il processo, fornendo istruzioni dettagliate e frammenti di codice per semplificare l'attività. Che tu sia uno sviluppatore esperto o un nuovo arrivato in Aspose.CAD, questo tutorial si rivolge a tutti i livelli di competenza.

## Prerequisiti

Prima di immergerti nel tutorial, assicurati di avere quanto segue:

- Libreria Aspose.CAD per .NET: assicurarsi di avere installata la libreria Aspose.CAD. In caso contrario, puoi scaricarlo da[Sito web Aspose.CAD](https://releases.aspose.com/cad/net/).

- File di disegno CAD: preparare un file di disegno CAD (ad esempio, conic_pyramid.dxf) che si desidera convertire in formati di immagine raster.

## Importa spazi dei nomi

Nel tuo progetto .NET, importa gli spazi dei nomi necessari per sfruttare le funzionalità Aspose.CAD. Includi i seguenti spazi dei nomi all'inizio del codice:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Passaggio 1: caricare il disegno CAD

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

// Carica un disegno CAD in un'istanza di Immagine
using (var image = Image.Load(sourceFilePath))
{
    // Il tuo codice per caricare il disegno CAD va qui
}
```

## Passaggio 2: crea CadRasterizationOptions

```csharp
// Crea un'istanza di CadRasterizationOptions
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
```

## Passaggio 3: specificare i livelli

```csharp
// Aggiungi il nome del livello all'elenco dei livelli di CadRasterizationOptions
rasterizationOptions.Layers = new string[] { "LayerA" };
```

## Passaggio 4: crea Opzioni Jpeg

```csharp
// Crea un'istanza di JpegOptions (o qualsiasi ImageOptions per i formati raster)
var options = new JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
```

## Passaggio 5: esporta in formato Jpeg

```csharp
// Esporta ogni livello in formato Jpeg
MyDir = MyDir + "CADLayersToRasterImageFormats_out.jpg";
image.Save(MyDir, options);
```

## Passaggio aggiuntivo: converti tutti i livelli

Se desideri convertire tutti i livelli, utilizza il seguente metodo:

```csharp
ConvertAllLayersToRasterImageFormats();
```

Questo metodo esegue l'iterazione su tutti i livelli del disegno CAD, esportando ciascun livello in un file Jpeg separato.

## Conclusione

Congratulazioni! Hai imparato con successo come esportare layout CAD in formati di immagine raster utilizzando Aspose.CAD per .NET. Questo tutorial fornisce una guida completa per gli sviluppatori che cercano soluzioni efficienti e affidabili per la conversione CAD.

## Domande frequenti

### Q1: Posso utilizzare altri formati di immagine per l'esportazione?

 A1: Sì, puoi. Basta sostituirlo`JpegOptions` con le opzioni del formato desiderato, come ad esempio`PngOptions` O`BmpOptions`.

### Q2: È disponibile una versione di prova?

 A2: Sì, puoi esplorare le funzionalità di Aspose.CAD scaricando la versione di prova[Qui](https://releases.aspose.com/).

### Q3: Come posso ottenere supporto per Aspose.CAD?

 A3: Visita Aspose.CAD[Forum](https://forum.aspose.com/c/cad/19) per il supporto della community o considera l'acquisto di una licenza per il supporto dedicato.

### Q4: Sono disponibili licenze temporanee?

 R4: Sì, puoi ottenere una licenza temporanea[Qui](https://purchase.aspose.com/temporary-license/).

### Q5: Dove posso trovare la documentazione?

 R5: Fare riferimento alla documentazione dettagliata[Qui](https://reference.aspose.com/cad/net/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
