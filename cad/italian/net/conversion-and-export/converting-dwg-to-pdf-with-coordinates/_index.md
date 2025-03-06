---
title: Conversione di DWG in PDF con coordinate in C# - Tutorial Aspose.CAD
linktitle: Conversione di DWG in PDF con coordinate in C#
second_title: Aspose.CAD .NET - Formato file CAD e BIM
description: Scopri come convertire DWG in PDF con coordinate specifiche in C# utilizzando Aspose.CAD. Segui la nostra guida passo passo per conversioni di file CAD precise ed efficienti.
weight: 11
url: /it/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Conversione di DWG in PDF con coordinate in C# - Tutorial Aspose.CAD

## introduzione

Benvenuti in questo tutorial completo sulla conversione di file DWG in PDF con le coordinate specificate utilizzando Aspose.CAD per .NET. Aspose.CAD è una potente libreria che consente agli sviluppatori di lavorare senza problemi con i formati di file CAD nelle loro applicazioni .NET. In questo tutorial ti guideremo attraverso il processo di conversione di un file DWG in PDF fornendo allo stesso tempo coordinate specifiche per migliorare la precisione.

## Prerequisiti

Prima di iniziare, assicurati di avere i seguenti prerequisiti:

- Libreria Aspose.CAD: scarica e installa la libreria Aspose.CAD per .NET. Puoi trovare la biblioteca[Qui](https://releases.aspose.com/cad/net/).

- Ambiente di sviluppo: assicurati di disporre di un ambiente di sviluppo compatibile, incluso Visual Studio o qualsiasi altro IDE preferito.

- File DWG: avere un file DWG pronto per la conversione. È possibile utilizzare il file di esempio fornito o il file DWG personalizzato.

## Importa spazi dei nomi

Nel tuo progetto C#, importa gli spazi dei nomi necessari:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadParameters;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.ImageOptions;
```

Analizziamo il codice in una guida passo passo per una migliore comprensione:

## Passaggio 1: definire la directory dei documenti

```csharp
string MyDir = "Your Document Directory";
```

## Passaggio 2: impostare il percorso del file DWG di origine

```csharp
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
```

## Passaggio 3: caricare il file DWG e configurare le opzioni di rasterizzazione

```csharp
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
    rasterizationOptions.Layouts = new string[] { "Model" };
    rasterizationOptions.NoScaling = true;
```

## Passaggio 4: definire le coordinate e la vista

```csharp
    Point topLeft = new Point(500, 1000);
    double width = 3108;
    double height = 2489;

    CadVportTableObject newView = new CadVportTableObject();
    newView.Name = new CadStringParameter();
    newView.Name.Init("*Active");
    newView.CenterPoint.X = topLeft.X + width / 2f;
    newView.CenterPoint.Y = topLeft.Y - height / 2f;
    newView.ViewHeight.Value = height;
    newView.ViewAspectRatio.Value = width / height;
```

## Passaggio 5: applicare le impostazioni della vista

```csharp
    for (int i = 0; i < cadImage.ViewPorts.Count; i++)
    {
        CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
        if (cadImage.ViewPorts.Count == 1 || string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
        {
            cadImage.ViewPorts[i] = newView;
            break;
        }
    }
```

## Passaggio 6: configura le opzioni PDF ed esporta

```csharp
    Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
    pdfOptions.VectorRasterizationOptions = rasterizationOptions;

    MyDir = MyDir + "ConvertDWGToPDFBySupplyingCoordinates_out.pdf";
    cadImage.Save(MyDir, pdfOptions);
}
```

## Passaggio 7: Visualizza il messaggio di successo

```csharp
Console.WriteLine("\nThe DWG file exported successfully to PDF.\nFile saved at " + MyDir);
```

## Conclusione

Congratulazioni! Hai convertito con successo un file DWG in PDF con le coordinate specificate utilizzando Aspose.CAD per .NET. Questo tutorial ha trattato i passaggi essenziali e ha fornito una guida chiara per gli sviluppatori.

## Domande frequenti

### Q1: Posso utilizzare Aspose.CAD con altri formati di file CAD?

A1: Sì, Aspose.CAD supporta vari formati CAD, inclusi DWG, DXF, DWF e altri.

### Q2: Come posso gestire gli errori durante il processo di conversione?

A2: implementare meccanismi di gestione degli errori utilizzando blocchi try-catch per acquisire e gestire le eccezioni.

### Q3: Aspose.CAD è adatto sia per ambienti Windows che Linux?

A3: Sì, Aspose.CAD è compatibile con entrambe le piattaforme Windows e Linux.

### Q4: Posso personalizzare ulteriormente l'output PDF?

A4: Certamente! Esplora le ampie opzioni fornite da Aspose.CAD per personalizzare l'output PDF in base alle tue esigenze specifiche.

### Q5: Dove posso trovare ulteriore supporto o discussioni nella community?

A5: Visita il[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) per il supporto e le discussioni della comunità.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
