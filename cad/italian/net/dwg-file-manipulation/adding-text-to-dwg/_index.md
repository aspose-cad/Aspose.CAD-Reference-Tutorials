---
date: 2026-04-06
description: Scopri come convertire DWG in PDF e aggiungere testo personalizzato usando
  C# e Aspose.CAD. Questa guida passo passo copre la generazione di PDF da DWG, l'inserimento
  di un'entità di testo e la modifica del carattere del testo DWG.
keywords:
- convert dwg to pdf
- generate pdf from dwg
- insert text entity
- change dwg text font
- aspose cad dwg pdf
linktitle: Aggiungere testo ai file DWG in C#
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Converti DWG in PDF e aggiungi testo in C# – Tutorial Aspose.CAD
url: /it/net/dwg-file-manipulation/adding-text-to-dwg/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Converti DWG in PDF e Aggiungi Testo in C# – Tutorial Aspose.CAD

## Introduzione

Nel mondo in rapida evoluzione del CAD e dello sviluppo .NET, **convertire DWG in PDF** inserendo annotazioni personalizzate è una necessità frequente. Che tu debba generare disegni stampabili per i clienti o incorporare note dinamiche direttamente in un DWG, Aspose.CAD rende il lavoro semplice. In questo tutorial imparerai a **convertire DWG in PDF**, **aggiungere un'entità di testo** e persino **modificare il font del testo DWG** usando C#.

## Risposte Rapide
- **Qual è la libreria migliore per la conversione da DWG a PDF?** Aspose.CAD per .NET  
- **Posso aggiungere testo personalizzato durante la conversione?** Sì – crea un'entità `CadText` e aggiungila prima di salvare.  
- **È necessaria una licenza per l'uso in produzione?** È richiesta una licenza commerciale; è disponibile una versione di prova gratuita.  
- **Quali versioni di .NET sono supportate?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **È possibile cambiare il font del testo?** Sì, regola le proprietà di `CadText` come `StyleType` e `TextHeight`.

## Cos'è “convertire dwg in pdf”?

Convertire un file DWG in PDF trasforma un disegno CAD basato su vettori in un documento ampiamente condivisibile e indipendente dal dispositivo. Il PDF conserva la geometria e i livelli originali, consentendo al contempo di incorporare annotazioni, testo o altri metadati. Aspose.CAD gestisce automaticamente la rasterizzazione e il rendering vettoriale, così non è necessario alcun software CAD di terze parti sul server.

## Perché aggiungere testo a un DWG prima della conversione?

Incorporare testo direttamente nel DWG ti dà il pieno controllo su posizionamento, stile e assegnazione dei layer. Quando il file viene successivamente convertito in PDF, il testo appare esattamente dove lo hai posizionato, preservando l'intento di progettazione ed eliminando la necessità di post‑elaborazione in un editor PDF.

## Prerequisiti

- **Libreria Aspose.CAD** – scaricala dal [download link](https://releases.aspose.com/cad/net/).  
- **Un ambiente .NET funzionante** (Visual Studio 2022, .NET 6 o qualsiasi versione compatibile).  
- **Una cartella per i tuoi file di test** – la chiameremo `MyDir` per tutta la guida.

Ora, procediamo passo dopo passo.

## Importa Namespace

Aggiungi le istruzioni `using` necessarie per accedere alle classi Aspose.CAD.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects.AttEntities;
using Aspose.CAD.ImageOptions;
```

## Passo 1: Carica il File DWG

Carica il tuo file DWG di origine in un oggetto `Image`. Questo oggetto ti dà accesso alle entità CAD sottostanti.

```csharp
string dwgPathToFile = MyDir + "SimpleEntites.dwg";
using (Image image = Image.Load(dwgPathToFile))
{
    // Subsequent steps will be performed inside this block
}
```

## Passo 2: Crea un Oggetto CadText (Inserisci Entità di Testo)

La classe `CadText` rappresenta una singola riga di testo in un DWG. Qui impostiamo lo stile, il valore, il colore, il layer e la posizione. Regola `StyleType` o `TextHeight` per **cambiare il font del testo DWG**.

```csharp
CadText cadText = new CadText();
cadText.StyleType = "Standard";          // Font/style – change to alter DWG text font
cadText.DefaultValue = "Some custom text";
cadText.ColorId = 256;                    // 256 = ByLayer (you can use a specific ACI color)
cadText.LayerName = "0";
cadText.FirstAlignment.X = 47.90;
cadText.FirstAlignment.Y = 5.56;
cadText.TextHeight = 0.8;                 // Height influences visual size
cadText.ScaleX = 0.0;
```

## Passo 3: Aggiungi l'Entità di Testo allo Spazio Modello

Lo spazio modello DWG contiene la maggior parte delle entità del disegno. Aggiungendo il nostro `CadText` al blocco `*Model_Space`, il testo diventa parte del disegno.

```csharp
CadImage cadImage = (CadImage)image;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadText);
```

## Passo 4: Configura le Opzioni PDF (Genera PDF da DWG)

Imposta le opzioni di rasterizzazione che controllano come il DWG viene renderizzato in PDF. Puoi regolare la dimensione della pagina, il tipo di disegno e il layout.

```csharp
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;
cadRasterizationOptions.PageHeight = 1600;
cadRasterizationOptions.PageWidth = 1600;
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## Passo 5: Salva il DWG Modificato come PDF

Infine, esporta il disegno modificato. Il PDF risultante include il testo appena inserito.

```csharp
image.Save(MyDir + "SimpleEntites_generated.pdf", pdfOptions);
```

> **Consiglio professionale:** Se hai bisogno di un PDF a risoluzione più alta, aumenta `PageHeight` e `PageWidth` proporzionalmente.

## Problemi Comuni & Soluzioni

| Problema | Motivo | Soluzione |
|----------|--------|-----------|
| Il testo non appare nel PDF | Layer o ID colore errato | Assicurati che `LayerName` esista e che `ColorId` sia impostato su un colore visibile (ad esempio, 7 per il bianco). |
| Il testo è posizionato in modo errato | Coordinate di allineamento errate | Verifica i valori `FirstAlignment.X/Y` rispetto alle unità del disegno. |
| Il PDF è vuoto | Opzioni di rasterizzazione non impostate | Imposta `DrawType` su `UseObjectColor` o `UseObjectLineWeight`. |

## Domande Frequenti (Esistenti)

### Q1: Aspose.CAD è compatibile con tutte le versioni di file DWG?

A1: Aspose.CAD supporta un'ampia gamma di versioni di file DWG, garantendo la compatibilità con diversi software CAD.

### Q2: Posso aggiungere più entità di testo a un singolo file DWG usando Aspose.CAD?

A2: Sì, puoi aggiungere più entità di testo a un file DWG ripetendo il processo descritto nel tutorial.

### Q3: Come posso cambiare il font e lo stile del testo in Aspose.CAD?

A3: Per modificare il font e lo stile del testo, regola le proprietà dell'oggetto `CadText` prima di aggiungerlo al file DWG.

### Q4: Ci sono considerazioni sulla licenza per l'uso di Aspose.CAD in un progetto commerciale?

A4: Sì, assicurati di rispettare i termini di licenza di Aspose.CAD. Consulta [Aspose.CAD Purchase](https://purchase.aspose.com/buy) per i dettagli.

### Q5: Dove posso cercare aiuto o discutere domande relative ad Aspose.CAD?

A5: Visita il [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) per entrare in contatto con la community e ottenere supporto.

## FAQ Aggiuntive

**Q: Come genero PDF da DWG senza aggiungere testo?**  
A: Salta il passaggio di creazione di `CadText` e configura direttamente `PdfOptions` prima di chiamare `image.Save(...)`.

**Q: Posso cambiare il colore del testo programmaticamente?**  
A: Sì, imposta `cadText.ColorId` su un numero di colore ACI specifico (ad esempio, 1 per il rosso).

**Q: È possibile inserire testo multilinea?**  
A: Usa `CadMText` per blocchi di testo multilinea; l'approccio è simile a `CadText`.

**Q: Aspose.CAD supporta la conversione batch di più file DWG?**  
A: Assolutamente – itera attraverso una directory di file DWG, applica gli stessi passaggi e salva ciascuno come PDF.

## Conclusione

Ora disponi di un flusso di lavoro completo e pronto per la produzione per **convertire DWG in PDF**, **aggiungere testo personalizzato** e **personalizzare l'aspetto del testo** usando C# e Aspose.CAD. Questa tecnica è ideale per la generazione automatica di disegni, pipeline di reporting o qualsiasi scenario in cui è necessario arricchire i file CAD al volo.

**Ultimo aggiornamento:** 2026-04-06  
**Testato con:** Aspose.CAD 24.11 for .NET  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}