---
date: 2026-08-17
description: Scopri come aggiungere un'immagine ai file dwg usando C# e Aspose.CAD
  per .NET. Questa guida ti accompagna nell'importazione delle immagini, nell'impostazione
  dei punti di inserimento e nell'esportazione in PDF.
keywords:
- add image to dwg
- convert dwg to pdf
- set insertion point dwg
- embed png in dwg
- save dwg as pdf
lastmod: 2026-08-17
linktitle: Importazione di immagini nei file DWG con C#
og_description: Scopri come aggiungere un'immagine ai file dwg usando C#. Questo tutorial
  copre l'importazione delle immagini, l'impostazione dei punti di inserimento e la
  conversione dei file dwg in PDF con Aspose.CAD.
og_image_alt: Guide showing C# code to embed an image into a DWG file using Aspose.CAD
og_title: Come aggiungere un'immagine ai file dwg con C# usando Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-08-17'
  description: Learn how to add image to dwg files using C# and Aspose.CAD for .NET.
    This guide walks you through importing images, setting insertion points, and exporting
    to PDF.
  headline: How to add image to dwg files with C# using Aspose.CAD
  type: TechArticle
- description: Learn how to add image to dwg files using C# and Aspose.CAD for .NET.
    This guide walks you through importing images, setting insertion points, and exporting
    to PDF.
  name: How to add image to dwg files with C# using Aspose.CAD
  steps:
  - name: set up your document directory
    text: Prepare the folder that contains the source DWG and the image you want to
      embed.
  - name: load the dwg file
    text: The `CadImage` class represents a DWG drawing and provides access to its
      entities, layers, and metadata.
  - name: define the image properties
    text: Create an `Image` object that points to the raster file (e.g., PNG) and
      specify its format.
  - name: set insertion point dwg and vectors
    text: Specify where the image should appear inside the drawing and how it should
      be scaled. The insertion point is defined by a 2‑D coordinate, while the vectors
      control width and height.
  - name: create and configure the raster image
    text: Instantiate a `RasterImage` object, assign the image data, and set any additional
      rendering options.
  - name: add image to dwg file
    text: Insert the configured raster image into the DWG’s entities collection so
      it becomes part of the drawing.
  - name: save as pdf (export dwg to pdf)
    text: After embedding the image you can **convert dwg to pdf** or **save dwg as
      pdf** with a single call. This is useful for sharing the drawing with stakeholders
      who don’t have CAD software.
  type: HowTo
- questions:
  - answer: The core library is .NET‑specific, but Aspose offers equivalent APIs for
      Java, Python and other platforms.
    question: Can I use Aspose.CAD for .NET with other programming languages?
  - answer: Yes, you can explore a free trial on the [Aspose free trial page](https://releases.aspose.com/).
    question: Is a free trial available for Aspose.CAD?
  - answer: The documentation is available in the [Aspose.CAD .NET API reference](https://reference.aspose.com/cad/net/).
    question: Where can I find detailed documentation for Aspose.CAD?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to get a temporary license.
    question: How do I obtain a temporary license for Aspose.CAD?
  - answer: Yes, you can seek support and engage with the community in the [Aspose.CAD
      community forum](https://forum.aspose.com/c/cad/19).
    question: Are there community forums for Aspose.CAD support?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- CAD
- Aspose.CAD
- C# image processing
- DWG manipulation
title: Come aggiungere un'immagine ai file dwg con C# usando Aspose.CAD
url: /it/net/image-manipulation-and-rendering/importing-images-into-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come aggiungere un'immagine ai file DWG con C# usando Aspose.CAD

## Introduzione

Aggiungere un'immagine a un file DWG è una necessità comune quando è necessario arricchire i disegni CAD con loghi, foto o grafiche raster. In questo tutorial imparerai come **add image to dwg** programmaticamente usando C# e Aspose.CAD per .NET, quindi opzionalmente convertire il risultato in PDF. I passaggi sono suddivisi così da poter copiare‑incollare ogni sezione nel proprio progetto.

## Risposte rapide
- **Quale libreria gestisce il lavoro?** Aspose.CAD for .NET.
- **Posso incorporare file PNG?** Sì – PNG, JPEG, BMP e altri formati raster sono supportati.
- **Ho bisogno di una licenza per lo sviluppo?** Una versione di prova gratuita funziona per i test; è necessaria una licenza commerciale per la produzione.
- **L'esportazione PDF è supportata?** Assolutamente – è possibile convertire il DWG aggiornato in PDF con una sola riga.
- **Quali versioni .NET sono compatibili?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7.

## Cos'è un file DWG?

Un file DWG è il formato binario nativo per i disegni Autodesk AutoCAD, che memorizza geometria vettoriale, layer e metadati. È ampiamente utilizzato in architettura, ingegneria e costruzione, e Aspose.CAD può leggere e scrivere questo formato senza la necessità di avere AutoCAD installato.

## Perché aggiungere un'immagine a DWG con Aspose.CAD?

Aspose.CAD supporta **50+ formati di input e output**, può elaborare file più grandi di 500 MB senza caricare l'intero documento in memoria, e fornisce un'API deterministica che funziona in ambienti server headless. Questo rende l'elaborazione in batch dei disegni DWG veloce e affidabile.

## Prerequisiti
- Conoscenza di base della programmazione C#.
- Aspose.CAD for .NET installed. You can download it from the [Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/). You can also explore other Aspose products on the [Aspose releases page](https://releases.aspose.com/).
- Un ambiente di sviluppo come Visual Studio 2022 o successivo.

## Come aggiungere un'immagine a DWG usando Aspose.CAD?

Carica il DWG di destinazione, crea un oggetto immagine raster che descrive la foto da incorporare, imposta il punto di inserimento e i vettori di scala, quindi allega l'immagine al disegno. Infine, salva il DWG modificato o esportalo direttamente in PDF. L'intero flusso di lavoro richiede solo poche chiamate API e si completa in meno di un secondo per disegni tipici di 2 pagine.

### Importa spazi dei nomi
Includi gli spazi dei nomi che espongono le classi CAD di cui avrai bisogno.

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

### Passo 1: configura la directory del documento
Prepara la cartella che contiene il DWG di origine e l'immagine da incorporare.

```csharp
string MyDir = "Your Document Directory";
```

### Passo 2: carica il file DWG
La classe `CadImage` rappresenta un disegno DWG e fornisce l'accesso alle sue entità, livelli e metadati.

```csharp
string dwgPathToFile = MyDir + "Drawing11.dwg";
CadImage cadImage1 = (CadImage)Image.Load(dwgPathToFile);
```

### Passo 3: definisci le proprietà dell'immagine
Crea un oggetto `Image` che punta al file raster (ad es., PNG) e specifica il suo formato.

```csharp
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.ObjectHandle = "A3B4";
```

### Passo 4: imposta il punto di inserimento DWG e i vettori
Specifica dove l'immagine deve apparire nel disegno e come deve essere scalata. Il punto di inserimento è definito da una coordinata 2‑D, mentre i vettori controllano larghezza e altezza.

```csharp
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

### Passo 5: crea e configura l'immagine raster
Istanzia un oggetto `RasterImage`, assegna i dati dell'immagine e imposta eventuali opzioni di rendering aggiuntive.

```csharp
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.ImageDefReference = "A3B4";
cadRasterImage.DisplayFlags = 7;
cadRasterImage.ClippingState = 0;
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(639.5, 561.5));
```

### Passo 6: aggiungi l'immagine al file DWG
Inserisci l'immagine raster configurata nella collezione di entità del DWG in modo che diventi parte del disegno.

```csharp
CadImage cadImage = (CadImage)cadImage1;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadRasterImage);

List<CadBaseObject> list = new List<CadBaseObject>(cadImage.Objects);
list.Add(cadRasterImageDef);
cadImage.Objects = list.ToArray();
```

### Passo 7: salva come PDF (esporta DWG in PDF)
Dopo aver incorporato l'immagine puoi **convert dwg to pdf** o **save dwg as pdf** con una singola chiamata. Questo è utile per condividere il disegno con stakeholder che non hanno software CAD.

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

## Come convertire DWG in PDF dopo aver incorporato un'immagine?

Chiama il metodo `Save` sull'istanza `CadImage`, passando `SaveFormat.Pdf` e opzionalmente un oggetto `PdfOptions` per controllare le dimensioni della pagina, la rasterizzazione e i metadati. Aspose.CAD preserva l'immagine raster incorporata, i layer e gli spessori delle linee, producendo una fedele rappresentazione PDF che può essere aperta in qualsiasi visualizzatore. Questa conversione avviene con una singola riga di codice.

## Problemi comuni e soluzioni
- **L'immagine appare nella posizione sbagliata** – verifica le coordinate del punto di inserimento e i vettori di direzione; sono relativi all'origine del disegno.
- **Le immagini grandi causano picchi di memoria** – usa l'opzione `Resize` sull'immagine raster prima dell'inserimento, o lavora con una copia a risoluzione inferiore.
- **L'esportazione PDF perde la qualità vettoriale** – assicurati di salvare con `PdfOptions` che mantengono i dati vettoriali; le immagini raster sono sempre incorporate così come sono.

## Domande frequenti

**Q: Posso usare Aspose.CAD per .NET con altri linguaggi di programmazione?**  
A: La libreria core è specifica per .NET, ma Aspose offre API equivalenti per Java, Python e altre piattaforme.

**Q: È disponibile una versione di prova gratuita per Aspose.CAD?**  
A: Sì, puoi esplorare una versione di prova gratuita nella [Aspose free trial page](https://releases.aspose.com/).

**Q: Dove posso trovare la documentazione dettagliata per Aspose.CAD?**  
A: La documentazione è disponibile nella [Aspose.CAD .NET API reference](https://reference.aspose.com/cad/net/).

**Q: Come ottengo una licenza temporanea per Aspose.CAD?**  
A: Visita la [temporary license page](https://purchase.aspose.com/temporary-license/) per ottenere una licenza temporanea.

**Q: Esistono forum della community per il supporto di Aspose.CAD?**  
A: Sì, puoi richiedere supporto e interagire con la community nel [Aspose.CAD community forum](https://forum.aspose.com/c/cad/19).

---

**Ultimo aggiornamento:** 2026-08-17  
**Testato con:** Aspose.CAD 24.11 for .NET  
**Autore:** Aspose

## Tutorial correlati

- [Esportare DWG in PDF o Immagini Raster - Guida Aspose.CAD](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [Esportare DWG in formato DXF in C# - Tutorial Aspose.CAD](/cad/net/advanced-export-techniques/exporting-dwg-to-dxf/)
- [Esportare Layout Specifici in PDF - Guida Aspose.CAD](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}