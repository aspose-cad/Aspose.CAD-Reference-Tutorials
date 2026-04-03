---
date: 2026-04-03
description: Scopri come impostare il viewport e convertire DWG in PDF in C# usando
  Aspose.CAD. Questo tutorial su DWG to PDF mostra un'esportazione precisa con coordinate.
keywords:
- how to set viewport
- dwg to pdf tutorial
- convert dwg to pdf c#
linktitle: Conversione da DWG a PDF con coordinate in C#
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Come impostare la viewport durante la conversione da DWG a PDF con coordinate
  in C# - Tutorial Aspose.CAD
url: /it/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Conversione di DWG in PDF con coordinate in C# - Tutorial Aspose.CAD

## Introduzione

Benvenuti a questo tutorial completo su **come impostare il viewport** durante la conversione di file DWG in PDF con coordinate specificate utilizzando Aspose.CAD per .NET. Controllando il viewport otterrete PDF pixel‑perfect che corrispondono esattamente all'area desiderata—perfetti per disegni di costruzione, anteprime di planimetrie o qualsiasi flusso di lavoro BIM.

## Risposte rapide
- **Che cosa significa “set viewport”?** Definisce la regione visibile e la scala del disegno CAD durante la rasterizzazione.  
- **Quale libreria gestisce la conversione?** Aspose.CAD per .NET.  
- **Ho bisogno di una licenza?** Una versione di prova gratuita è sufficiente per la valutazione; è necessaria una licenza commerciale per la produzione.  
- **Piattaforme supportate?** Windows, Linux e macOS con .NET 5/6/7 o .NET Framework 4.6+.  
- **Tempo tipico di implementazione?** Circa 10‑15 minuti per una conversione di base.

## Prerequisiti

Prima di iniziare, assicuratevi di avere i seguenti prerequisiti:

- **Libreria Aspose.CAD** – Scarica e installa la libreria Aspose.CAD per .NET. Puoi trovare la libreria [qui](https://releases.aspose.com/cad/net/).
- **Ambiente di sviluppo** – Visual Studio, Rider o qualsiasi IDE che supporti lo sviluppo .NET.
- **File DWG** – Disponi di un file DWG pronto per la conversione. Puoi usare il file di esempio fornito o il tuo file DWG personalizzato.

## Come impostare il viewport per un'esportazione PDF precisa

Impostare il viewport è il passaggio fondamentale che consente di definire l'area esatta del disegno da renderizzare. Nel codice qui sotto creiamo un nuovo `CadVportTableObject`, lo posizioniamo con la coordinata in alto a sinistra e calcoliamo larghezza, altezza e rapporto d'aspetto. Questa è l'implementazione di **come impostare il viewport** che guida il resto della conversione.

## Importa gli spazi dei nomi

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

Analizziamo il codice passo passo per una migliore comprensione:

## Passo 1: Definisci la directory del documento

```csharp
string MyDir = "Your Document Directory";
```

## Passo 2: Imposta il percorso del file DWG sorgente

```csharp
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
```

## Passo 3: Carica il file DWG e configura le opzioni di rasterizzazione

```csharp
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
    rasterizationOptions.Layouts = new string[] { "Model" };
    rasterizationOptions.NoScaling = true;
```

## Passo 4: Definisci coordinate e viewport  

Qui impostiamo effettivamente **il viewport** (come impostare il viewport) specificando l'angolo in alto a sinistra, la larghezza e l'altezza dell'area da esportare.

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

## Passo 5: Applica le impostazioni del viewport

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

## Passo 6: Configura le opzioni PDF ed esporta  

Ora uniamo tutto e **convertiamo DWG in PDF** usando le opzioni di rasterizzazione appena preparate.

```csharp
    Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
    pdfOptions.VectorRasterizationOptions = rasterizationOptions;

    MyDir = MyDir + "ConvertDWGToPDFBySupplyingCoordinates_out.pdf";
    cadImage.Save(MyDir, pdfOptions);
}
```

## Passo 7: Visualizza il messaggio di successo

```csharp
Console.WriteLine("\nThe DWG file exported successfully to PDF.\nFile saved at " + MyDir);
```

## Casi d'uso comuni

- **Documentazione di costruzione** – Genera PDF stampabili di sezioni specifiche della planimetria.  
- **Coordinamento BIM** – Esporta solo l'area di interesse per il rilevamento di conflitti.  
- **Presentazioni al cliente** – Fornisci un PDF pulito di una stanza o elevazione selezionata senza esporre l'intero disegno.

## Conclusione

Congratulazioni! Hai convertito con successo **DWG in PDF** con coordinate precise e hai imparato **come impostare il viewport** usando Aspose.CAD per .NET. Questo **tutorial dwg to pdf** dimostra come **creare pdf da dwg** e **esportare dwg come pdf c#** mantenendo il pieno controllo sull'area di output.

## FAQ

### Q1: Posso usare Aspose.CAD con altri formati di file CAD?

A1: Sì, Aspose.CAD supporta vari formati CAD, inclusi DWG, DXF, DWF e altri.

### Q2: Come posso gestire gli errori durante il processo di conversione?

A2: Implementa meccanismi di gestione degli errori usando blocchi try‑catch per catturare e gestire le eccezioni.

### Q3: Aspose.CAD è adatto sia per ambienti Windows che Linux?

A3: Sì, Aspose.CAD è compatibile con entrambe le piattaforme Windows e Linux.

### Q4: Posso personalizzare ulteriormente l'output PDF?

A4: Certamente! Esplora le numerose opzioni offerte da Aspose.CAD per personalizzare l'output PDF secondo le tue esigenze specifiche.

### Q5: Dove posso trovare supporto aggiuntivo o discussioni della community?

A5: Visita il [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) per supporto e discussioni della community.

## Domande frequenti aggiuntive

**Q: Questo approccio funziona con file DWG di grandi dimensioni (centinaia di MB)?**  
A: Sì. La rasterizzazione viene eseguita pagina per pagina, e puoi regolare `rasterizationOptions` (ad es., `Resolution`) per bilanciare qualità e utilizzo della memoria.

**Q: Posso esportare più viewport in pagine PDF separate?**  
A: Puoi iterare su `cadImage.ViewPorts`, impostare ciascuno come attivo e chiamare `Save` per ogni pagina, quindi unire i PDF usando Aspose.PDF.

**Q: È possibile aggiungere una filigrana al PDF generato?**  
A: Dopo aver salvato il PDF, puoi riaprirlo con Aspose.PDF e applicare una filigrana di testo o immagine prima di consegnarlo all'utente.

---

**Ultimo aggiornamento:** 2026-04-03  
**Testato con:** Aspose.CAD 24.11 per .NET  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}