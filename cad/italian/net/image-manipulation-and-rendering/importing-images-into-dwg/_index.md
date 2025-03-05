---
title: Importazione di immagini in file DWG con C# - Guida Aspose.CAD
linktitle: Importazione di immagini in file DWG con C#
second_title: Aspose.CAD .NET - Formato file CAD e BIM
description: Impara a importare immagini in file DWG utilizzando C# con Aspose.CAD per .NET. Segui la nostra guida passo passo per un'integrazione perfetta.
type: docs
weight: 11
url: /it/net/image-manipulation-and-rendering/importing-images-into-dwg/
---
## introduzione

Nel campo della progettazione assistita da computer (CAD), incorporare immagini nei file DWG è un compito comune e cruciale. Aspose.CAD per .NET fornisce un potente set di strumenti per semplificare questo processo, rendendolo accessibile agli sviluppatori C#. In questo tutorial esploreremo passo dopo passo come importare le immagini nei file DWG.

## Prerequisiti

Prima di immergerti nella guida, assicurati di avere quanto segue:

- Conoscenza base della programmazione C#.
-  Aspose.CAD per .NET installato. Puoi scaricarlo[Qui](https://releases.aspose.com/cad/net/).
- Un ambiente di sviluppo creato.

## Importa spazi dei nomi

Assicurati di includere gli spazi dei nomi necessari nel tuo progetto C#:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Passaggio 1: imposta la directory dei documenti

```csharp
string MyDir = "Your Document Directory";
```

## Passaggio 2: caricare il file DWG

```csharp
string dwgPathToFile = MyDir + "Drawing11.dwg";
CadImage cadImage1 = (CadImage)Image.Load(dwgPathToFile);
```

## Passaggio 3: definire le proprietà dell'immagine

```csharp
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.ObjectHandle = "A3B4";
```

## Passaggio 4: impostare il punto di inserimento e i vettori

```csharp
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

## Passaggio 5: crea e configura l'immagine raster

```csharp
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.ImageDefReference = "A3B4";
cadRasterImage.DisplayFlags = 7;
cadRasterImage.ClippingState = 0;
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(639.5, 561.5));
```

## Passaggio 6: aggiungere l'immagine al file DWG

```csharp
CadImage cadImage = (CadImage)cadImage1;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadRasterImage);

List<CadBaseObject> list = new List<CadBaseObject>(cadImage.Objects);
list.Add(cadRasterImageDef);
cadImage.Objects = list.ToArray();
```

## Passaggio 7: salva come PDF

```csharp
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;

cadRasterizationOptions.PageHeight = 1600;
cadRasterizationOptions.PageWidth = 1600;
cadRasterizationOptions.Layouts = new string[] { "Model" };
cadImage1.Save(MyDir + "export2.pdf", pdfOptions);
```

## Conclusione

L'integrazione delle immagini nei file DWG utilizzando C# e Aspose.CAD per .NET è un processo fluido che consente agli sviluppatori di migliorare facilmente i propri progetti CAD con elementi visivi.

## Domande frequenti

### Q1: posso utilizzare Aspose.CAD per .NET con altri linguaggi di programmazione?

A1: Aspose.CAD è progettato principalmente per .NET, ma Aspose fornisce librerie per vari linguaggi di programmazione.

### Q2: È disponibile una prova gratuita per Aspose.CAD per .NET?

 A2: Sì, puoi esplorare una prova gratuita[Qui](https://releases.aspose.com/).

### Q3: Dove posso trovare la documentazione dettagliata per Aspose.CAD?

 A3: La documentazione è disponibile[Qui](https://reference.aspose.com/cad/net/).

### Q4: Come posso ottenere una licenza temporanea per Aspose.CAD per .NET?

 A4: Visita[questo link](https://purchase.aspose.com/temporary-license/) per ottenere una licenza temporanea.

### Q5: Esistono forum della community per il supporto Aspose.CAD?

 A5: Sì, puoi cercare supporto e interagire con la comunità[Qui](https://forum.aspose.com/c/cad/19).