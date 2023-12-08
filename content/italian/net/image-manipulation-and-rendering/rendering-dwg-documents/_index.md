---
title: Rendering di documenti DWG in C# - Guida Aspose.CAD
linktitle: Rendering di documenti DWG in C#
second_title: Aspose.CAD .NET - Formato file CAD e BIM
description: Scopri come eseguire il rendering di documenti DWG in C# utilizzando Aspose.CAD. Questa guida passo passo illustra l'importazione, la configurazione e il salvataggio con esempi di codice.
type: docs
weight: 17
url: /it/net/image-manipulation-and-rendering/rendering-dwg-documents/
---
## introduzione

Benvenuti nella guida completa sul rendering di documenti DWG in C# utilizzando Aspose.CAD. Che tu sia uno sviluppatore esperto o che tu abbia appena iniziato con .NET, questo tutorial ti guiderà attraverso il processo di sfruttamento di Aspose.CAD per eseguire il rendering dei file DWG in modo efficiente. Aspose.CAD è una potente API che fornisce robuste funzionalità per lavorare con formati di file CAD, rendendolo una scelta ideale per gli sviluppatori che hanno a che fare con file DWG.

## Prerequisiti

Prima di immergerti nel tutorial, assicurati di possedere i seguenti prerequisiti:

- Conoscenza base del linguaggio di programmazione C#.
- Visual Studio installato sul tuo computer.
-  Libreria Aspose.CAD integrata nel tuo progetto. Puoi scaricarlo da[Qui](https://releases.aspose.com/cad/net/).
- Un file DWG di esempio, ad esempio "Bottom_plate.dwg", da seguire insieme agli esempi.

## Importa spazi dei nomi

Per iniziare, assicurati di importare gli spazi dei nomi necessari all'inizio del codice C#:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.FileFormats.Cad;
```

Ora suddividiamo l'esempio fornito in più passaggi:

## Passaggio 1: caricare il file DWG

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Il tuo codice per caricare il file DWG va qui.
}
```

## Passaggio 2: configura le opzioni di rasterizzazione

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };
rasterizationOptions.NoScaling = true;
//Qui è possibile aggiungere ulteriori configurazioni di rasterizzazione.
```

## Passaggio 3: definire la regione da disegnare

```csharp
Point topLeft = new Point(6156, 7053);
double width = 3108;
double height = 2489;
```

## Passaggio 4: crea una nuova finestra

```csharp
CadVportTableObject newView = new CadVportTableObject();
newView.Name.Value = "*Active";
newView.CenterPoint.X = topLeft.X + width / 2f;
newView.CenterPoint.Y = topLeft.Y - height / 2f;
newView.ViewHeight.Value = height;
newView.ViewAspectRatio.Value = width / height;
```

## Passaggio 5: sostituisci la visualizzazione attiva

```csharp
for (int i = 0; i < cadImage.ViewPorts.Count; i++)
{
    CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
    if ((currentView.Name.Value == null && cadImage.ViewPorts.Count == 1) ||
    string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
    {
        cadImage.ViewPorts[i] = newView;
        break;
    }
}
```

## Passaggio 6: configura le opzioni PDF

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Passaggio 7: salva il DWG renderizzato come PDF

```csharp
cadImage.Save(MyDir, pdfOptions);
```

## Conclusione

Congratulazioni! Hai eseguito correttamente il rendering di un documento DWG in PDF utilizzando Aspose.CAD in C#. Sentiti libero di esplorare più funzionalità e personalizzare il codice in base alle tue esigenze specifiche.

## Domande frequenti

### Q1: Posso utilizzare Aspose.CAD con altri formati di file CAD?

A1: Sì, Aspose.CAD supporta vari formati CAD, inclusi DWG, DXF, DWF e altri.

### Q2: Aspose.CAD è compatibile con .NET Core?

A2: Sì, Aspose.CAD è compatibile sia con .NET Framework che con .NET Core.

### Q3: Come posso gestire layout diversi in un file DWG?

 A3: È possibile specificare il layout desiderato nel file`Layouts` proprietà di`CadRasterizationOptions`.

### Q4: Esistono considerazioni sulla licenza per l'utilizzo di Aspose.CAD?

 R4: Per i dettagli sulla licenza, visitare[Qui](https://purchase.aspose.com/buy).

### Q5: Dove posso trovare ulteriore supporto?

A5: Visita il[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) per il supporto e le discussioni della comunità.