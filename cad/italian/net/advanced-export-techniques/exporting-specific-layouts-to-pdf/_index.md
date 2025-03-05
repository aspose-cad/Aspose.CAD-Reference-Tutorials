---
title: Esportazione di layout specifici in PDF - Guida Aspose.CAD
linktitle: Esportazione di layout specifici in PDF
second_title: Aspose.CAD .NET - Formato file CAD e BIM
description: Scopri come esportare layout specifici in PDF utilizzando Aspose.CAD per .NET. Guida passo passo per un'integrazione perfetta.
type: docs
weight: 13
url: /it/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/
---
## introduzione

Benvenuti nella nostra guida passo passo sull'esportazione di layout specifici in PDF utilizzando Aspose.CAD per .NET. Aspose.CAD è una potente libreria che consente agli sviluppatori di lavorare senza problemi con i formati di file CAD. In questo tutorial, ci concentreremo sull'esportazione di layout specifici da un file DWG a PDF utilizzando Aspose.CAD in un ambiente .NET.

## Prerequisiti

Prima di immergerci nel tutorial, assicurati di disporre dei seguenti prerequisiti:

-  Libreria Aspose.CAD per .NET: assicurarsi di avere installata la libreria Aspose.CAD. Puoi scaricarlo[Qui](https://releases.aspose.com/cad/net/).

- Ambiente di sviluppo: configura un ambiente di sviluppo .NET, come Visual Studio.

## Importa spazi dei nomi

Nel tuo progetto .NET, importa gli spazi dei nomi necessari per Aspose.CAD:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Passaggio 1: caricare il file DWG

```csharp
// Il percorso della directory dei documenti.
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";

using (Image image = Image.Load(sourceFilePath))
{
    // Il tuo codice per i passaggi successivi va qui.
}
```

## Passaggio 2: imposta le opzioni di CadRasterizzazione

```csharp
// Crea un'istanza di CadRasterizationOptions e imposta le sue varie proprietà
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
```

## Passaggio 3: specificare il nome del layout

```csharp
// Specificare il nome del layout desiderato
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

## Passaggio 4: crea PdfOptions

```csharp
// Crea un'istanza di PdfOptions
PdfOptions pdfOptions = new PdfOptions();
// Imposta la proprietà VectorRasterizationOptions
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Passaggio 5: esporta in PDF

```csharp
MyDir = MyDir + "ExportSpecificLayoutToPDF_out.pdf";
// Esporta il DWG in PDF
image.Save(MyDir, pdfOptions);
```

## Passaggio 6: Visualizza il messaggio di successo

```csharp
// Visualizza il messaggio di successo
Console.WriteLine("\nThe DWG file with a specific layout exported successfully to PDF.\nFile saved at " + MyDir);
```

## Conclusione

Congratulazioni! Hai imparato con successo come esportare layout specifici in PDF utilizzando Aspose.CAD per .NET. Questa guida fornisce una procedura dettagliata, assicurandoti di poter integrare facilmente questa funzionalità nei tuoi progetti.

## Domande frequenti

### Q1: Posso esportare più layout contemporaneamente?

 A1: Sì, modifica semplicemente il file`Layouts` array nel passaggio 3 per includere i nomi di tutti i layout desiderati.

### Q2: Aspose.CAD è compatibile con altri formati di file CAD?

A2: Sì, Aspose.CAD supporta vari formati CAD, inclusi DWG, DXF, DWF e altri.

### Q3: Come posso regolare le impostazioni di output del PDF?

 A3: Esplora le proprietà di`CadRasterizationOptions` nel passaggio 2 per le opzioni di personalizzazione.

### Q4: Dove posso trovare ulteriore documentazione Aspose.CAD?

 A4: Visita il[documentazione](https://reference.aspose.com/cad/net/) per informazioni approfondite.

### Q5: È disponibile una prova gratuita?

 R5: Sì, puoi accedere alla prova gratuita[Qui](https://releases.aspose.com/).