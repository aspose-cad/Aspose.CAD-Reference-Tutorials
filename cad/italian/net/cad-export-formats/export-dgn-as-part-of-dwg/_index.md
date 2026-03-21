---
date: 2026-03-21
description: Scopri come creare PDF da DWG ed esportare DGN come parte di DWG usando
  Aspose.CAD per .NET. Questa guida mostra anche come convertire DWG in PDF e impostare
  le opzioni PDF.
linktitle: Export DGN as Part of DWG
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Crea PDF da DWG ed esporta DGN come parte di DWG – Aspose.CAD per .NET
url: /it/net/cad-export-formats/export-dgn-as-part-of-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Creare PDF da DWG ed Esportare DGN come Parte del DWG – Aspose.CAD per .NET

## Introduzione

Se hai bisogno di **creare PDF da file DWG** includendo anche un progetto DGN come parte del DWG, Aspose.CAD per .NET lo rende semplice. In questo tutorial percorreremo l’intero flusso di lavoro: caricamento di un DWG, individuazione del DGN incorporato, configurazione delle opzioni di rasterizzazione e, infine, esportazione del risultato in un documento PDF. Che tu stia costruendo uno strumento di conversione batch, un motore di reporting o un servizio di integrazione CAD‑BIM, i passaggi seguenti ti forniranno una solida base pronta per la produzione.

## Risposte Rapide
- **Quale libreria gestisce la conversione DWG → PDF?** Aspose.CAD per .NET  
- **Posso esportare un DGN sottofondo mentre creo il PDF?** Sì – il sottofondo è accessibile tramite `CadDgnUnderlay`.  
- **Quale metodo imposta le opzioni PDF?** `PdfOptions` insieme a `CadRasterizationOptions`.  
- **È necessaria una licenza per uso commerciale?** Sì, è richiesta una licenza valida di Aspose.CAD.  
- **Versioni .NET supportate?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## Che cosa significa “creare PDF da DWG”?

Creare un PDF da un file DWG significa renderizzare il disegno vettoriale in un documento PDF raster o vettoriale. Questo processo è utile per condividere i disegni con stakeholder che non dispongono di software CAD, per l’archiviazione o per generare report stampabili. Aspose.CAD semplifica il compito gestendo l’analisi delle entità DWG e fornendo un controllo dettagliato sull’output tramite `PdfOptions`.

## Perché esportare DGN come parte di un DWG?

Un sottofondo DGN rappresenta spesso geometria di riferimento proveniente da progetti MicroStation. Esportando il DGN insieme al DWG si preserva il contesto di progetto originale, garantendo che i consumatori successivi vedano l’intero set di disegni. Questo è particolarmente prezioso nei progetti multidisciplinari dove coesistono file DWG e DGN.

## Prerequisiti

- **Aspose.CAD per .NET** – scaricalo [qui](https://releases.aspose.com/cad/net/).  
- **Ambiente di sviluppo** – Visual Studio (qualsiasi versione recente) o il tuo IDE .NET preferito.  
- **Conoscenza base di C#** – dovresti sentirti a tuo agio con la sintassi C# e la struttura dei progetti .NET.

## Importare Namespace

Aggiungi le direttive `using` richieste all’inizio del tuo file sorgente C#:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Guida Passo‑Passo

### Passo 1: Definire i Percorsi dei File

Imposta il file DWG di input e il nome del PDF di output.

```csharp
// Input and Output file paths
string fileName = "BlockRefDgn.dwg";
string outPath = fileName + ".pdf";
```

### Passo 2: Creare un’Istanza di `PdfOptions` (impostare le opzioni PDF)

`PdfOptions` ti consente di controllare come viene generato il PDF, ad esempio dimensione pagina, compressione e metadati.

```csharp
// Create an instance of PdfOptions class for exporting DWG to PDF
PdfOptions exportOptions = new PdfOptions();
```

### Passo 3: Caricare il File DWG

Carica il DWG come `CadImage` così da poter ispezionare le sue entità.

```csharp
// Load the existing DWG file as an image and convert it to CadImage type
using (CadImage cadImage = (CadImage)Image.Load(fileName))
```

### Passo 4: Iterare Attraverso le Entità

Scorri ogni entità del disegno per individuare il sottofondo DGN.

```csharp
// Iterate through each entity inside the DWG file
foreach (CadBaseEntity baseEntity in cadImage.Entities)
```

### Passo 5: Verificare il Tipo di Entità (come esportare dgn)

Identifica se l’entità corrente è un sottofondo DGN.

```csharp
// Check if the entity is an image definition
if (baseEntity.TypeName == CadEntityTypeName.DGNUNDERLAY)
```

### Passo 6: Ottenere il Percorso del Sottofondo

Recupera il percorso di riferimento esterno del file DGN.

```csharp
// If it's an image definition, get the external reference to the object
CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
Console.WriteLine(dgnFile.UnderlayPath);
```

### Passo 7: Definire le Opzioni di Rasterizzazione (convertire dwg in pdf)

Configura come il DWG viene rasterizzato prima di essere inserito nel PDF.

```csharp
// Define settings for CadRasterizationOptions object
exportOptions.VectorRasterizationOptions = new CadRasterizationOptions()
{
    PageWidth = 1600,
    PageHeight = 1600,
    Layouts = new string[] { "Model" },
    AutomaticLayoutsScaling = false,
    NoScaling = true,
    BackgroundColor = Color.Black,
    DrawType = CadDrawTypeMode.UseObjectColor
};
```

### Passo 8: Esportare DWG in PDF

Infine, salva l’immagine renderizzata come file PDF.

```csharp
// Export the DWG to PDF by calling Save method
cadImage.Save(outPath, exportOptions);
```

## Problemi Comuni e Soluzioni

| Problema | Motivo | Soluzione |
|----------|--------|-----------|
| **`Image.Load` genera “File not found”** | Percorso errato o file mancante. | Usa un percorso assoluto o assicurati che il DWG sia copiato nella cartella di output. |
| **Il percorso del sottofondo è vuoto** | Sottofondo DGN non incorporato o riferimento interrotto. | Verifica che il DWG contenga effettivamente un sottofondo DGN e che il file DGN esterno sia accessibile. |
| **L’output PDF è vuoto** | Opzioni di rasterizzazione impostate a dimensioni zero. | Regola `PageWidth`/`PageHeight` o imposta `NoScaling = false`. |
| **Eccezione di licenza** | Esecuzione senza una licenza valida di Aspose.CAD. | Applica la licenza prima di caricare l’immagine: `License lic = new License(); lic.SetLicense("Aspose.CAD.lic");` |

## Domande Frequenti

### Q1: Posso usare Aspose.CAD per .NET nei miei progetti commerciali?
A1: Sì, puoi. Visita [qui](https://purchase.aspose.com/buy) per esplorare le opzioni di licenza.

### Q2: Ci sono limitazioni sulla dimensione dei file DWG che posso elaborare?
A2: Aspose.CAD supporta la gestione di file DWG di grandi dimensioni, ma possono applicarsi limitazioni hardware.

### Q3: È disponibile una versione di prova?
A3: Sì, puoi ottenere una prova gratuita [qui](https://releases.aspose.com/).

### Q4: Come posso ottenere licenze temporanee?
A4: Le licenze temporanee possono essere ottenute [qui](https://purchase.aspose.com/temporary-license/).

### Q5: Dove posso chiedere assistenza se incontro problemi?
A5: Puoi visitare il forum Aspose.CAD [qui](https://forum.aspose.com/c/cad/19) per supporto.

**D: Come impostare metadati PDF aggiuntivi (autore, titolo, ecc.)?**  
R: Usa le proprietà `exportOptions.Metadata` prima di chiamare `Save`.

**D: Posso esportare più layout in pagine PDF separate?**  
R: Sì – imposta `Layouts = new string[] { "Layout1", "Layout2" }` in `CadRasterizationOptions`.

**D: Aspose.CAD supporta la conversione da DWG ad altri formati immagine?**  
R: Assolutamente. Puoi esportare in PNG, JPEG, SVG e altri usando le overload corrispondenti di `Image.Save`.

---

**Ultimo aggiornamento:** 2026-03-21  
**Testato con:** Aspose.CAD 24.11 per .NET  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}