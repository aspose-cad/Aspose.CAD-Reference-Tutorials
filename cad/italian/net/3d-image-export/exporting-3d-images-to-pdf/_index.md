---
date: 2026-07-04
description: Scopri come impostare la dimensione della pagina PDF ed esportare PDF
  da immagini CAD 3D usando Aspose.CAD per .NET – una guida passo‑passo per convertire
  DWG in PDF e salvare CAD come PDF.
keywords:
- set pdf page size
- export pdf from cad
- convert dwg to pdf
- save cad as pdf
- cad to pdf tutorial
linktitle: Esportazione di immagini 3D in PDF
schemas:
- author: Aspose
  dateModified: '2026-07-04'
  description: Learn how to set PDF page size and export PDF from 3D CAD images using
    Aspose.CAD for .NET – a step‑by‑step guide to convert DWG to PDF and save CAD
    as PDF.
  headline: Set PDF page size – Export 3D Images to PDF with Aspose.CAD
  type: TechArticle
- description: Learn how to set PDF page size and export PDF from 3D CAD images using
    Aspose.CAD for .NET – a step‑by‑step guide to convert DWG to PDF and save CAD
    as PDF.
  name: Set PDF page size – Export 3D Images to PDF with Aspose.CAD
  steps:
  - name: Load the CAD Image
    text: '`Image` class represents a CAD drawing loaded into memory, ready for rasterization.'
  - name: Configure Rasterization Options (Save CAD as PDF)
    text: '`RasterizationOptions` class defines how the CAD data is rasterized, including
      page size, DPI, and whether 3‑D entities are rendered.'
  - name: Set PDF Options (Create PDF from CAD)
    text: '`PdfOptions` class holds the output format settings and links the rasterization
      options to PDF generation.'
  - name: Save as PDF (Generate PDF from 3D Model)
    text: '`Save` method on the `Image` object writes the rasterized content to the
      specified PDF file, producing a ready‑to‑share document.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD supports more than 50 input and output formats, including
      DWG, DXF, DGN, STL, and IFC, ensuring flexibility for any project.
    question: Is Aspose.CAD compatible with all CAD file formats?
  - answer: Absolutely. Set `PageWidth` and `PageHeight` in `RasterizationOptions`
      to any size in points, inches, or millimetres before calling `Save`.
    question: Can I customize the page dimensions when exporting to PDF?
  - answer: Yes, you can obtain temporary licenses for Aspose.CAD by visiting [Temporary
      License](https://purchase.aspose.com/temporary-license/).
    question: Are temporary licenses available for Aspose.CAD?
  - answer: Head to the [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) for
      expert help and peer‑to‑peer advice.
    question: Where can I find additional support or community discussions?
  - answer: Yes, you can explore the features of Aspose.CAD by accessing the [free
      trial](https://releases.aspose.com/).
    question: Is there a free trial version of Aspose.CAD?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Imposta la dimensione della pagina PDF – Esporta immagini 3D in PDF con Aspose.CAD
url: /it/net/3d-image-export/exporting-3d-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Esportazione di immagini 3D in PDF - Tutorial Aspose.CAD

## Introduzione

Se hai bisogno di **impostare le dimensioni della pagina PDF** durante la conversione di un disegno CAD 3‑D in PDF, sei nel posto giusto. Questo tutorial ti mostra, passo dopo passo, come caricare un file CAD, configurare le opzioni di rasterizzazione—including dimensioni personalizzate della pagina—e generare un PDF ad alta fedeltà usando Aspose.CAD per .NET. Alla fine sarai in grado di **esportare PDF da CAD**, **salvare CAD come PDF**, e controllare ogni dettaglio del layout senza installare AutoCAD.

## Risposte rapide
- **Che cosa significa “export PDF from CAD”?** Converte un disegno CAD (DWG, DXF, DGN, ecc.) in un PDF che può essere aperto su qualsiasi dispositivo.  
- **Quale libreria esegue la conversione?** Aspose.CAD per .NET fornisce rasterizzazione ed esportazione PDF senza dipendenze esterne.  
- **Ho bisogno di una licenza?** È necessaria una licenza temporanea o completa per la produzione; è disponibile una versione di prova gratuita.  
- **Posso impostare dimensioni personalizzate della pagina?** Sì—usa `PageWidth` e `PageHeight` in `RasterizationOptions`.  
- **La geometria 3D verrà mantenuta?** Le entità 3D vengono rasterizzate; abilita `TypeOfEntities.Entities3D` per il supporto completo 3D.

## Cos'è “export PDF” nel contesto del CAD?

Esportare PDF da CAD significa prendere un disegno CAD (DWG, DXF, DGN, ecc.) e convertirlo in un file PDF che può contenere grafica vettoriale, visualizzazioni 3D rasterizzate e informazioni precise sul layout della pagina, facilitando la condivisione con chiunque non possieda software CAD.

## Perché usare Aspose.CAD per esportare PDF?

Aspose.CAD ti consente di **impostare le dimensioni della pagina PDF** ed esportare PDF interamente in codice .NET gestito. Supporta oltre 50 formati CAD, elabora file fino a 2 GB senza caricare l'intero documento in memoria, e preserva spessori di linea, colori e la resa opzionale delle entità 3D con una DPI di rasterizzazione fino a 1200. La libreria funziona su Windows, Linux e macOS, quindi i PDF generati funzionano su qualsiasi piattaforma.

## Prerequisiti

- **Aspose.CAD per .NET** installato. Scaricalo dalla [pagina di download di Aspose.CAD per .NET](https://releases.aspose.com/cad/net/).  
- Una cartella contenente i file CAD che desideri convertire (ad es., `C:\CAD\`).  
- .NET 6.0 o successivo (o .NET Framework 4.7.2).  

## Importare gli spazi dei nomi

Le istruzioni `using` importano gli spazi dei nomi Aspose.CAD necessari per lavorare con le opzioni di rasterizzazione e PDF.  

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

## Guida passo‑passo

Carica il tuo file CAD, configura le dimensioni della pagina in `RasterizationOptions`, collega queste opzioni a un'istanza `PdfOptions` e chiama `Save`. Questo flusso in quattro passaggi ti offre il pieno controllo sulla dimensione e sulla qualità dell'output mantenendo il codice conciso.

### Come impostare le dimensioni della pagina PDF durante l'esportazione di CAD in PDF?

Carica il tuo file CAD, configura le dimensioni della pagina in `RasterizationOptions`, collega queste opzioni a un'istanza `PdfOptions` e chiama `Save`. Questo flusso in quattro passaggi ti offre il pieno controllo sulla dimensione e sulla qualità dell'output mantenendo il codice conciso.

### Passo 1: Caricare l'immagine CAD

La classe `Image` rappresenta un disegno CAD caricato in memoria, pronto per la rasterizzazione.  

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image cadImage = Image.Load(sourceFilePath))
{
    // Your code for loading the CAD image goes here
}
```

### Passo 2: Configurare le opzioni di rasterizzazione (Salvare CAD come PDF)

La classe `RasterizationOptions` definisce come i dati CAD vengono rasterizzati, includendo dimensioni della pagina, DPI e se le entità 3D vengono renderizzate.  

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
// rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;

rasterizationOptions.Layouts = new string[] { "Model" };
```

### Passo 3: Impostare le opzioni PDF (Creare PDF da CAD)

La classe `PdfOptions` contiene le impostazioni del formato di output e collega le opzioni di rasterizzazione alla generazione del PDF.  

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### Passo 4: Salvare come PDF (Generare PDF da modello 3D)

Il metodo `Save` sull'oggetto `Image` scrive il contenuto rasterizzato nel file PDF specificato, producendo un documento pronto per la condivisione.  

```csharp
MyDir = MyDir + "Export3DImagestoPDF_out.pdf";
cadImage.Save(MyDir, pdfOptions);
```

## Problemi comuni e soluzioni

| Problema | Motivo | Correzione |
|----------|--------|------------|
| **Il PDF di output è vuoto** | Nome del layout errato o layout `Model` mancante. | Verifica che `rasterizationOptions.Layouts` corrisponda a un layout presente nel file CAD. |
| **Bassa risoluzione** | Il DPI di rasterizzazione predefinito è basso. | Imposta `rasterizationOptions.Resolution = 300;` prima di salvare. |
| **Entità 3D non visualizzate** | `TypeOfEntities` è commentato. | Decommenta `rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;`. |
| **Eccezione di licenza** | Uso di una versione di prova senza licenza. | Applica una licenza temporanea o permanente tramite `License license = new License(); license.SetLicense("Aspose.CAD.lic");`. |

## Domande frequenti

**Q: Aspose.CAD è compatibile con tutti i formati di file CAD?**  
**A:** Sì, Aspose.CAD supporta più di 50 formati di input e output, inclusi DWG, DXF, DGN, STL e IFC, garantendo flessibilità per qualsiasi progetto.

**Q: Posso personalizzare le dimensioni della pagina durante l'esportazione in PDF?**  
**A:** Assolutamente. Imposta `PageWidth` e `PageHeight` in `RasterizationOptions` a qualsiasi dimensione in punti, pollici o millimetri prima di chiamare `Save`.

**Q: Sono disponibili licenze temporanee per Aspose.CAD?**  
**A:** Sì, puoi ottenere licenze temporanee per Aspose.CAD visitando [Temporary License](https://purchase.aspose.com/temporary-license/).

**Q: Dove posso trovare supporto aggiuntivo o discussioni della community?**  
**A:** Vai al [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) per aiuto esperto e consigli tra pari.

**Q: Esiste una versione di prova gratuita di Aspose.CAD?**  
**A:** Sì, puoi esplorare le funzionalità di Aspose.CAD accedendo alla [free trial](https://releases.aspose.com/).

## Conclusione

Ora disponi di un metodo completo, pronto per la produzione, per **impostare le dimensioni della pagina PDF** ed **esportare PDF da immagini CAD 3D** usando Aspose.CAD per .NET. Regolando le opzioni di rasterizzazione puoi perfezionare risoluzione, layout della pagina e resa delle entità 3D per soddisfare qualsiasi requisito di documentazione. Sperimenta con diverse impostazioni DPI e dimensioni della pagina per ottenere il giusto equilibrio tra dimensione del file e fedeltà visiva.

{{< blocks/products/products-backtop-button >}}

## Tutorial correlati

- [Esportazione di layout specifici in PDF - Guida Aspose.CAD](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)
- [Esportazione di DWG in PDF o immagini raster - Guida Aspose.CAD](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [Esporta DGN in PDF con Aspose.CAD per .NET](/cad/net/cad-export-formats/export-dgn-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

--- 

**Ultimo aggiornamento:** 2026-07-04  
**Testato con:** Aspose.CAD 24.11 per .NET  
**Autore:** Aspose