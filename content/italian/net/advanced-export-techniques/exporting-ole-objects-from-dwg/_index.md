---
title: Esportazione di oggetti OLE da file DWG - Tutorial Aspose.CAD
linktitle: Esportazione di oggetti OLE da file DWG
second_title: Aspose.CAD .NET - Formato file CAD e BIM
description: Esplora la guida passo passo sull'esportazione di oggetti OLE da file DWG utilizzando Aspose.CAD per .NET. Migliora le tue capacità di manipolazione dei file CAD senza sforzo.
type: docs
weight: 12
url: /it/net/advanced-export-techniques/exporting-ole-objects-from-dwg/
---
## introduzione

Stai cercando di estrarre facilmente oggetti OLE dai file DWG? Aspose.CAD per .NET è qui per semplificare il processo per te. In questo tutorial ti guideremo passo dopo passo attraverso l'esportazione di oggetti OLE, assicurandoti di sfruttare al meglio questa potente libreria .NET. 

## Prerequisiti

Prima di immergerci nel tutorial, assicurati di disporre dei seguenti prerequisiti:

-  Aspose.CAD per .NET Library: assicurati di avere la libreria installata. Puoi scaricarlo da[Pagina di download di Aspose.CAD per .NET](https://releases.aspose.com/cad/net/).

-  Directory documenti: imposta una directory in cui sono archiviati i file DWG. Sostituire`"Your Document Directory"`nello snippet di codice fornito con il percorso effettivo.

## Importa spazi dei nomi

Nel tuo progetto .NET, dovrai importare gli spazi dei nomi necessari per sfruttare le funzionalità di Aspose.CAD. Utilizza il seguente snippet di codice:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Passaggio 1: impostare la directory dei documenti

```csharp
string MyDir = "Your Document Directory";
```

 Sostituire`"Your Document Directory"` con il percorso in cui si trovano i file DWG.

## Passaggio 2: specificare i file DWG

```csharp
string[] files = new string[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

Elenca i file DWG che desideri elaborare all'interno della matrice.

## Passaggio 3: configura le opzioni di esportazione

```csharp
PngOptions pngOptions = new PngOptions { };
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.VectorRasterizationOptions = rasterizationOptions;
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

Personalizza le opzioni di esportazione in base alle tue esigenze. In questo esempio, configuriamo l'esportazione PNG con un layout specificato.

## Passaggio 4: scorrere i file ed esportare

```csharp
foreach (string file in files)
{
    using (CadImage cadImage = (CadImage)Image.Load(MyDir + file))
    {
        cadImage.Save(MyDir + file + "_out.png", pngOptions);
    }
}
```

Scorrere i file DWG specificati, caricarli ciascuno e salvare il file PNG esportato con le opzioni definite.

## Conclusione

Congratulazioni! Hai esportato con successo oggetti OLE da file DWG utilizzando Aspose.CAD per .NET. Questa potente libreria semplifica attività complesse, fornendo efficienza e flessibilità nella manipolazione dei file CAD.

## Domande frequenti

### Q1: Aspose.CAD per .NET è adatto sia per file CAD junior che senior?

A1: Sì, Aspose.CAD per .NET è versatile e può gestire un'ampia gamma di file CAD, comprese le varianti junior e senior.

### Q2: Posso personalizzare le opzioni di esportazione per layout diversi?

A2: Assolutamente! Come mostrato nel tutorial, puoi personalizzare le opzioni di esportazione, inclusi i layout, per soddisfare le tue esigenze specifiche.

### Q3: Dove posso trovare la documentazione dettagliata per Aspose.CAD per .NET?

 A3: Esplora il[Aspose.CAD per la documentazione .NET](https://reference.aspose.com/cad/net/) per approfondimenti ed esempi.

### Q4: È disponibile una prova gratuita?

 A4: Sì, puoi provare le funzionalità di Aspose.CAD per .NET con una prova gratuita. Visita[questo link](https://releases.aspose.com/) per iniziare.

### Q5: Come posso ottenere supporto o connettermi con la community?

 R5: Per supporto e coinvolgimento della comunità, visitare il[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19).