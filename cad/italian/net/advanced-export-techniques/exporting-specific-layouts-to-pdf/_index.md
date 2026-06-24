---
date: 2026-03-13
description: Scopri come impostare le opzioni di rasterizzazione CAD ed esportare
  layout DWG specifici in PDF utilizzando Aspose.CAD per .NET – la guida definitiva
  per creare PDF da file CAD.
linktitle: Exporting Specific Layouts to PDF
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Imposta le opzioni di rasterizzazione CAD – Esporta layout specifici in PDF
  - Guida Aspose.CAD
url: /it/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/
weight: 13
---

.

## Frequently Asked Questions -> "Domande Frequenti"

Each Q/A translate.

**Q: Can I export multiple layouts simultaneously?** -> "Posso esportare più layout simultaneamente?" etc.

Make sure to keep code snippets unchanged.

## Conclusion -> "Conclusione"

Paragraph translate.

---

**Last Updated:** 2026-03-13 (keep date)

**Tested With:** Aspose.CAD 24.11 for .NET (keep)

**Author:** Aspose (keep)

Then closing shortcodes.

Proceed to produce final content.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Esportazione di Layout Specifici in PDF - Guida Aspose.CAD

## Introduzione

In questo tutorial scoprirai **how to set CAD rasterization options** così da poter esportare un singolo layout—o più layout—da un file DWG direttamente in PDF. Aspose.CAD per .NET rende il processo di *dwg to pdf conversion c#* semplice, offrendoti il pieno controllo su dimensione della pagina, risoluzione e selezione del layout. Alla fine della guida sarai in grado di **create PDF from CAD file** con poche righe di codice.

## Risposte Rapide
- **Cosa fa “set cad rasterization options”?**  
  Indica ad Aspose.CAD come renderizzare i dati vettoriali (layout, layer, spessori di linea) in pagine PDF rasterizzate.  
- **Quale metodo esporta un layout DWG in PDF?**  
  Usa `Image.Save` con un `PdfOptions` configurato che contiene il tuo `CadRasterizationOptions`.  
- **Posso esportare più di un layout contemporaneamente?**  
  Sì – fornisci un array di nomi di layout nella proprietà `Layouts`.  
- **È necessaria una licenza per l'uso in produzione?**  
  È richiesta una licenza commerciale; è disponibile una versione di prova gratuita per la valutazione.  
- **Quali versioni di .NET sono supportate?**  
  .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6 e successive.

## Che cosa è “set cad rasterization options”?
`CadRasterizationOptions` è la classe che controlla come le entità CAD vengono rasterizzate durante la conversione in formati basati su raster come PDF. Configurando le sue proprietà—dimensioni della pagina, selezione del layout, colore di sfondo, ecc.—definisci l'aspetto visivo dell'operazione **export dwg layout to pdf**.

## Perché impostare le opzioni di rasterizzazione CAD?
- **Precisione** – Mantieni spessori di linea e scale esattamente come appaiono nel disegno CAD originale.  
- **Prestazioni** – Renderizza solo i layout di cui hai bisogno, riducendo la dimensione del file e i tempi di elaborazione.  
- **Flessibilità** – Regola larghezza/altezza della pagina, DPI e sfondo per adeguarli ai tuoi standard di reporting.  

## Prerequisiti

Prima di immergerti nel codice, assicurati di avere:

- **Aspose.CAD per .NET** installato. Puoi scaricarlo [qui](https://releases.aspose.com/cad/net/).  
- Un ambiente di sviluppo .NET (Visual Studio, VS Code o qualsiasi IDE tu preferisca).  
- Un file DWG che contenga almeno un layout (il file di esempio usato qui è `visualization_-_conference_room.dwg`).

## Importare gli Spazi dei Nomi

Nel tuo progetto .NET, importa gli spazi dei nomi necessari per Aspose.CAD:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Guida Passo‑Passo

### Passo 1: Caricare il file DWG

Per prima cosa, indica ad Aspose.CAD il file DWG di origine che desideri convertire.

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";

using (Image image = Image.Load(sourceFilePath))
{
    // Your code for further steps goes here.
}
```

### Passo 2: Impostare **CadRasterizationOptions**

Qui configuriamo le impostazioni di rasterizzazione che determinano la dimensione della pagina PDF e la risoluzione.

```csharp
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
```

> **Pro tip:** Regola `PageWidth` e `PageHeight` per corrispondere alle dimensioni del layout PDF di destinazione. Valori più grandi aumentano i dettagli ma anche la dimensione del file.

### Passo 3: Specificare il nome del layout

Indica ad Aspose.CAD quale/i layout renderizzare. Sostituisci `"Layout1"` con il nome esatto del layout nel tuo file DWG.

```csharp
// Specify desired layout name
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

> **Perché è importante:** Limitando l'array `Layouts` eviti di esportare fogli indesiderati, rendendo l'operazione **dwg to pdf conversion c#** più veloce e il PDF risultante più pulito.

### Passo 4: Creare `PdfOptions`

Collega le impostazioni di rasterizzazione alle opzioni di esportazione PDF.

```csharp
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();
// Set the VectorRasterizationOptions property
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### Passo 5: Esportare in PDF

Infine, salva il layout renderizzato come file PDF.

```csharp
MyDir = MyDir + "ExportSpecificLayoutToPDF_out.pdf";
// Export the DWG to PDF
image.Save(MyDir, pdfOptions);
```

### Passo 6: Visualizzare un messaggio di successo

Un rapido output sulla console conferma che l'operazione è riuscita.

```csharp
// Display success message
Console.WriteLine("\nThe DWG file with a specific layout exported successfully to PDF.\nFile saved at " + MyDir);
```

## Problemi Comuni e Soluzioni

| Problema | Causa | Soluzione |
|----------|-------|-----------|
| **Nessun PDF generato** | L'array `Layouts` non corrisponde a nessun nome di layout nel DWG. | Verifica i nomi dei layout con un visualizzatore CAD e aggiorna la proprietà `Layouts`. |
| **Pagine vuote** | `PageWidth`/`PageHeight` impostati a 0 o valori estremamente piccoli. | Usa dimensioni realistiche (es. 1600 × 1600) o lascia che Aspose calcoli automaticamente omettendo quelle proprietà. |
| **Scalatura errata** | DPI non impostato quando è richiesta un'uscita ad alta risoluzione. | Imposta `rasterizationOptions.Resolution = 300;` (o il DPI desiderato) prima dell'esportazione. |

## Domande Frequenti

**D: Posso esportare più layout simultaneamente?**  
R: Sì, modifica semplicemente l'array `Layouts` nel Passo 3 includendo tutti i nomi dei layout desiderati, ad esempio `new string[] { "Layout1", "Layout2" }`.

**D: Aspose.CAD è compatibile con altri formati di file CAD?**  
R: Assolutamente. Supporta DWG, DXF, DWF, DGN e molti altri formati.

**D: Come posso regolare le impostazioni di output PDF oltre alla dimensione della pagina?**  
R: Esplora le proprietà aggiuntive di `CadRasterizationOptions` come `Resolution`, `BackgroundColor` e `DrawType` per perfezionare il risultato.

**D: Dove posso trovare ulteriore documentazione su Aspose.CAD?**  
R: Visita la [documentazione](https://reference.aspose.com/cad/net/) per riferimenti API dettagliati ed esempi.

**D: È disponibile una versione di prova gratuita?**  
R: Sì, puoi accedere alla versione di prova gratuita [qui](https://releases.aspose.com/).

## Conclusione

Ora sai come **set CAD rasterization options** e usarle per **export specific DWG layouts to PDF** con Aspose.CAD per .NET. Questo approccio ti offre un controllo preciso sul processo di conversione, permettendoti di integrare rapidamente e in modo affidabile la funzionalità CAD‑to‑PDF in qualsiasi applicazione C#.

---

**Last Updated:** 2026-03-13  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}