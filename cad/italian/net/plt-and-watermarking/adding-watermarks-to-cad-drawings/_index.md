---
title: Aggiunta di filigrane ai disegni CAD - Guida Aspose.CAD
linktitle: Aggiunta di filigrane ai disegni CAD
second_title: Aspose.CAD .NET - Formato file CAD e BIM
description: Migliora i tuoi disegni CAD con filigrane professionali utilizzando Aspose.CAD per .NET. Segui la nostra guida passo passo per progetti personalizzati e accattivanti.
type: docs
weight: 11
url: /it/net/plt-and-watermarking/adding-watermarks-to-cad-drawings/
---
## introduzione

Stai cercando di migliorare i tuoi disegni CAD aggiungendo filigrane professionali? Aspose.CAD per .NET fornisce una soluzione solida per integrare perfettamente le filigrane nei file CAD. In questa guida passo passo, ti guideremo attraverso il processo di aggiunta di filigrane utilizzando Aspose.CAD, assicurandoti che i tuoi disegni non solo trasmettano informazioni critiche ma portino anche il tuo segno unico.

## Prerequisiti

Prima di immergerti nel tutorial, assicurati di avere quanto segue:
-  Aspose.CAD per .NET: assicurati di avere la libreria Aspose.CAD installata. Puoi scaricarlo[Qui](https://releases.aspose.com/cad/net/).
- La tua directory di documenti: configura una directory per archiviare i tuoi disegni CAD.
Ora iniziamo con l'aggiunta di filigrane ai tuoi disegni CAD!

## Importa spazi dei nomi

Inizia importando gli spazi dei nomi necessari nel tuo progetto .NET:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Passaggio 1: caricare il disegno CAD

```csharp
// Il percorso della directory dei documenti.
string MyDir = "Your Document Directory";
using (CadImage cadImage = (CadImage)Image.Load(MyDir + "Drawing11.dwg")) {
```

## Passaggio 2: aggiungi filigrana come TESTOM

```csharp
// Aggiungi nuovo TESTOM
CadMText watermark = new CadMText();
watermark.Text = "Watermark message";
watermark.InitialTextHeight = 40;
watermark.InsertionPoint = new Cad3DPoint(300, 40);
watermark.LayerName = "0";
cadImage.BlockEntities["*Model_Space"].AddEntity(watermark);
```

## Passaggio 3: oppure aggiungi filigrana come testo

```csharp
// In alternativa, aggiungi un'entità più semplice come Testo
CadText text = new CadText();
text.DefaultValue = "Watermark text";
text.TextHeight = 40;
text.FirstAlignment = new Cad3DPoint(300, 40);
text.LayerName = "0";
cadImage.BlockEntities["*Model_Space"].AddEntity(text);
```

## Passaggio 4: esporta in PDF

```csharp
// Esporta il disegno CAD con filigrana in PDF
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.Layouts = new[] { "Model" };
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
cadImage.Save(MyDir + "AddWatermark_out.pdf", pdfOptions);
```

Ripeti questi passaggi per disegni diversi e otterrai file CAD con filigrana dall'aspetto professionale in pochissimo tempo!

## Conclusione

Congratulazioni! Hai imparato con successo come aggiungere filigrane ai tuoi disegni CAD utilizzando Aspose.CAD per .NET. Questo processo semplice ma potente ti consente di personalizzare i tuoi progetti mantenendo l'integrità dei tuoi disegni tecnici.

## Domande frequenti

### Q1: Posso personalizzare l'aspetto della filigrana?

R1: Sì, puoi personalizzare il testo, il carattere, la dimensione e la posizione della filigrana in base alle tue preferenze.

### Q2: Aspose.CAD è compatibile con diversi formati di file CAD?

A2: Aspose.CAD supporta vari formati di file CAD, inclusi DWG e DXF, garantendo un'ampia compatibilità.

### Q3: Posso aggiungere più filigrane a un singolo disegno CAD?

A3: Assolutamente! Puoi aggiungere tutte le filigrane necessarie, garantendo flessibilità per diversi casi d'uso.

### Q4: Aspose.CAD offre una prova gratuita?

A4: Sì, puoi esplorare le funzionalità di Aspose.CAD con una prova gratuita. Prendilo[Qui](https://releases.aspose.com/).

### Q5: Dove posso trovare supporto per Aspose.CAD?

 R5: Per qualsiasi domanda o assistenza, visitare il[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19).