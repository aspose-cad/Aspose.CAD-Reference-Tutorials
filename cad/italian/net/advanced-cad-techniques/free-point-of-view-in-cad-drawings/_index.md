---
title: Punto di vista gratuito nei disegni CAD - Guida Aspose.CAD
linktitle: Punto di vista gratuito nei disegni CAD
second_title: Aspose.CAD .NET - Formato file CAD e BIM
description: Esplora la libertà della visualizzazione CAD con Aspose.CAD per .NET. Segui la nostra guida passo passo per un punto di vista unico.
weight: 11
url: /it/net/advanced-cad-techniques/free-point-of-view-in-cad-drawings/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Punto di vista gratuito nei disegni CAD - Guida Aspose.CAD

Nel campo della progettazione assistita da computer (CAD), acquisire un punto di vista libero nei disegni è un aspetto cruciale della visualizzazione e della presentazione di progetti complessi. Aspose.CAD per .NET fornisce una soluzione solida per ottenere questa libertà, consentendo agli utenti di manipolare e ottimizzare facilmente i disegni CAD. In questa guida passo passo, esploreremo il processo per ottenere un punto di vista gratuito nei disegni CAD utilizzando Aspose.CAD per .NET.

## Prerequisiti

Prima di immergerti nel tutorial, assicurati di disporre dei seguenti prerequisiti:

1. Installazione di Aspose.CAD
 Assicurati di avere Aspose.CAD per .NET installato nel tuo ambiente di sviluppo. In caso contrario, puoi scaricarlo da[Sito web Aspose.CAD](https://releases.aspose.com/cad/net/).

2. File di disegno CAD
Prepara un file di disegno CAD che desideri manipolare. Per questa guida utilizzeremo un file di esempio denominato "conic_pyramid.dxf".

3. Sviluppo dell'ambiente
Avere un ambiente di sviluppo .NET funzionante configurato con Visual Studio o qualsiasi IDE preferito.

## Importa spazi dei nomi

Nel tuo progetto .NET, importa gli spazi dei nomi necessari per la funzionalità Aspose.CAD. Aggiungi il seguente snippet di codice all'inizio del file:

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
```


## Passaggio 1: definire la directory dei documenti

```csharp
// Il percorso della directory dei documenti.
string MyDir = "Your Document Directory";
```

Assicurati di sostituire "La tua directory dei documenti" con il percorso effettivo della directory dei documenti.

## Passaggio 2: specificare il file di origine

```csharp
string sourceFilePath = MyDir + "conic_pyramid.dxf";
```

Fornisci il percorso del file di disegno CAD.

## Passaggio 3: impostare il percorso di output

```csharp
var outPath = Path.Combine(MyDir, "FreePointOfView_out.jpg");
```

Definire il percorso in cui verrà salvato il disegno CAD manipolato.

## Passaggio 4: caricare l'immagine CAD

```csharp
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
```

Caricare il disegno CAD utilizzando Aspose.CAD.

## Passaggio 5: configura le opzioni JPEG

```csharp
JpegOptions options = new JpegOptions
{
    VectorRasterizationOptions = new CadRasterizationOptions
    {
        PageWidth = 1500, PageHeight = 1500
    }
};
```

Configura le opzioni per esportare il disegno CAD in formato JPEG.

## Passaggio 6: impostare gli angoli di rotazione

```csharp
float xAngle = 10; //Angolo di rotazione lungo l'asse X
float yAngle = 30; //Angolo di rotazione lungo l'asse Y
float zAngle = 40; //Angolo di rotazione lungo l'asse Z
((CadRasterizationOptions)(options.VectorRasterizationOptions)).ObserverPoint = new ObserverPoint(xAngle, yAngle, zAngle);
```

Specificare gli angoli di rotazione lungo gli assi X, Y e Z per ottenere il punto di vista desiderato.

## Passaggio 7: salvare il disegno CAD manipolato

```csharp
cadImage.Save(outPath, options);
}
```

Salvare il disegno CAD manipolato nel percorso di output specificato.

## Passaggio 8: Visualizza il messaggio di successo

```csharp
Console.WriteLine("\n3D images exported successfully to JPEG.\nFile saved at " + outPath);
```

Informare l'utente dell'avvenuta esportazione dell'immagine 3D.

## Conclusione

In questo tutorial, abbiamo esplorato il processo per ottenere un punto di vista gratuito nei disegni CAD utilizzando Aspose.CAD per .NET. Seguendo queste istruzioni dettagliate, puoi migliorare le tue capacità di visualizzazione CAD e presentare i tuoi progetti con una nuova prospettiva.


## Domande frequenti

### Q1: Posso utilizzare Aspose.CAD per .NET con altri formati di file CAD?

A1: Sì, Aspose.CAD per .NET supporta vari formati di file CAD, inclusi DWG e DXF.

### Q2: È disponibile una versione di prova di Aspose.CAD?

 R2: Sì, puoi scaricare una versione di prova gratuita da[Qui](https://releases.aspose.com/).

### Q3: Come posso ottenere una licenza temporanea per Aspose.CAD?

 A3: È possibile acquisire una licenza temporanea da[Qui](https://purchase.aspose.com/temporary-license/).

### Q4: Dove posso trovare ulteriore supporto per Aspose.CAD?

 A4: Visita il[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) per il supporto e le discussioni della comunità.

### Q5: Posso personalizzare le opzioni di esportazione per diversi formati di immagine?

A5: Certamente! Aspose.CAD offre una gamma di opzioni di personalizzazione, consentendoti di adattare il processo di esportazione alle tue esigenze specifiche.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
