---
date: 2026-03-29
description: Scopri come creare PDF da CAD, impostare le dimensioni della tela e esportare
  CAD in PDF o TIFF utilizzando Aspose.CAD per .NET in questa guida passo‑passo.
linktitle: Setting Canvas Size and Mode
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 'Come creare PDF da CAD: impostare la dimensione della tela e la modalità in
  Aspose.CAD per .NET'
url: /it/net/cad-features-and-support/setting-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Impostazione della dimensione e della modalità della tela in Aspose.CAD per .NET

## Introduzione

Pronto a **creare PDF da CAD** file controllando le dimensioni dell'output? In questo tutorial vedremo come impostare la dimensione e la modalità della tela, caricare un file CAD e esportarlo in PDF o TIFF con Aspose.CAD per .NET. Che tu abbia bisogno di **convertire DXF in PDF**, generare disegni ad alta risoluzione o semplicemente regolare l'area di rasterizzazione, i passaggi seguenti ti offriranno una soluzione solida e pronta per la produzione.

## Risposte rapide
- **Che cosa significa “create PDF from CAD”?** Convertire un disegno CAD (ad es., DXF, DWG) in un documento PDF che conserva i dettagli vettoriali e raster.  
- **Quale opzione controlla le dimensioni dell'output?** `CadRasterizationOptions.PageWidth` e `PageHeight` (dimensione della tela).  
- **Posso esportare anche in TIFF?** Sì – usa `TiffOptions` con le stesse impostazioni di rasterizzazione.  
- **È necessaria una licenza per la produzione?** È richiesta una licenza commerciale; è disponibile una versione di prova gratuita.  
- **Versioni .NET supportate?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## Che cos'è “create PDF from CAD”?
Creare un PDF da CAD significa renderizzare il disegno CAD in un formato orientato alla pagina (PDF) che può essere visualizzato, stampato o condiviso senza necessità di software CAD. Aspose.CAD si occupa del lavoro pesante, consentendoti di definire la dimensione della tela, la scala e il formato di output.

## Perché impostare la dimensione della tela quando si crea PDF da CAD?
Impostare la dimensione della tela ti dà un controllo preciso sulla risoluzione e le dimensioni del PDF o TIFF risultante. Questo è particolarmente utile quando:
- Preparare i disegni per la stampa su formati di carta specifici.  
- Generare miniature o immagini ad alta risoluzione per l'anteprima web.  
- Garantire una disposizione coerente tra più documenti.

## Prerequisiti

- Aspose.CAD Library: Scarica e installa la libreria Aspose.CAD dal [sito web Aspose.CAD](https://releases.aspose.com/cad/net/).
- Development Environment: Assicurati di avere un ambiente di sviluppo .NET configurato sulla tua macchina.
- Sample CAD File: Per questo tutorial utilizzeremo un file DXF di esempio. Puoi trovarne uno nella [documentazione Aspose.CAD](https://reference.aspose.com/cad/net/).

## Importare gli spazi dei nomi

Per prima cosa, importa gli spazi dei nomi necessari per l'elaborazione CAD:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Come creare PDF da CAD con dimensione della tela personalizzata

### Passo 1: Caricare il file CAD

Iniziamo **caricando il file CAD** (ad es., un DXF) in un oggetto `Image`. Questo è il punto in cui **carichi il file CAD** in memoria.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    // Your code for further steps will go here
}
```

### Passo 2: Creare CadRasterizationOptions

Crea un'istanza di `CadRasterizationOptions` e definisci la dimensione della tela. Le proprietà `PageWidth` e `PageHeight` ti consentono di **impostare la dimensione della tela** alle dimensioni esatte di cui hai bisogno.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
rasterizationOptions.NoScaling = false;
```

### Passo 3: Creare PdfOptions (Esportare CAD in PDF)

Collega le impostazioni di rasterizzazione a un oggetto `PdfOptions`. Questa configurazione ti consente di **esportare CAD in PDF** con la tela personalizzata che hai definito.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### Passo 4: Esportare in PDF (Convertire DXF in PDF)

Ora salva l'immagine come PDF. Questo passaggio **crea PDF da CAD** utilizzando le opzioni impostate.

```csharp
image.Save(MyDir + "result_out.pdf", pdfOptions);
```

### Passo 5: Creare TiffOptions (Esportare CAD in TIFF)

Se hai anche bisogno di un'immagine raster, configura `TiffOptions`. Le stesse opzioni di rasterizzazione vengono riutilizzate, quindi l'**esportazione CAD in TIFF** rispetta la dimensione della tela.

```csharp
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.VectorRasterizationOptions = rasterizationOptions;
```

### Passo 6: Esportare in TIFF

Infine, salva il disegno come file TIFF.

```csharp
image.Save(MyDir + "result_out.tiff", tiffOptions);
```

## Problemi comuni e soluzioni

- **La tela appare ritagliata** – Verifica che `AutomaticLayoutsScaling` sia impostato su `true` e `NoScaling` su `false` affinché il disegno si adatti alla tela.  
- **PDF a bassa risoluzione** – Aumenta `PageWidth`/`PageHeight` o imposta `Resolution` su `CadRasterizationOptions`.  
- **Errore file non trovato** – Assicurati che `MyDir` punti a una directory valida e che il nome del file DXF corrisponda esattamente.

## Domande frequenti

### Q1: Posso usare Aspose.CAD con altre librerie .NET?
A1: Sì, Aspose.CAD si integra perfettamente con altre librerie .NET, offrendo capacità migliorate per la manipolazione CAD.

### Q2: È disponibile una versione di prova gratuita per Aspose.CAD?
A2: Sì, puoi esplorare le funzionalità di Aspose.CAD con una versione di prova gratuita. Visita [qui](https://releases.aspose.com/) per iniziare.

### Q3: Come posso ottenere supporto per Aspose.CAD?
A3: Per supporto e discussioni, visita il [forum Aspose.CAD](https://forum.aspose.com/c/cad/19).

### Q4: Dove posso trovare la documentazione completa per Aspose.CAD?
A4: Consulta la [documentazione Aspose.CAD](https://reference.aspose.com/cad/net/) per informazioni dettagliate ed esempi.

### Q5: Come acquisto Aspose.CAD per .NET?
A5: Per acquistare Aspose.CAD, visita la [pagina di acquisto](https://purchase.aspose.com/buy).

**Domande aggiuntive**

**Q: Posso esportare un disegno CAD multipagina in un unico PDF?**  
**A:** Sì. Imposta `PageCount` in `CadRasterizationOptions` e la libreria concatenerà le pagine in un unico PDF.

**Q: La dimensione della tela influisce sulla qualità dei dati vettoriali?**  
**A:** I dati vettoriali rimangono indipendenti dalla risoluzione; la dimensione della tela influisce solo sugli elementi rasterizzati e sulla risoluzione dell'immagine.

---

**Ultimo aggiornamento:** 2026-03-29  
**Testato con:** Aspose.CAD 24.11 for .NET  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}