---
date: 2026-02-15
description: Scopri come impostare le dimensioni della pagina PDF e convertire i file
  CAD in PDF utilizzando Aspose.CAD per Java, con ridimensionamento automatico del
  layout ed esportazione in TIFF.
linktitle: Set PDF Page Size – Convert CAD to PDF
second_title: Aspose.CAD Java API
title: Imposta dimensione pagina PDF – Converti CAD in PDF (Java)
url: /it/java/advanced-cad-features/set-canvas-size-and-mode/
weight: 16
---

 Not needed.

Now produce final content.

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Set Canvas Size and Mode

## Introduction

Se hai bisogno di **impostare le dimensioni della pagina PDF** durante la conversione di disegni CAD in PDF, sei nel posto giusto. In questo tutorial ti mostreremo come utilizzare Aspose.CAD per Java per definire dimensioni precise della tela, abilitare **automatic layout scaling** e quindi esportare il risultato sia in PDF che in TIFF. Che tu stia preparando schemi ingegneristici per la stampa o generando miniature per una galleria web, controllare le dimensioni della pagina e la risoluzione di output è essenziale.

## Quick Answers
- **What does “convert CAD to PDF” mean?** Cosa significa “convertire CAD in PDF”?  
  Trasformare un disegno CAD (ad es., DXF, DWG) in un documento PDF che può essere visualizzato su qualsiasi piattaforma.  
- **Can I also export to TIFF?** Posso anche esportare in TIFF?  
  Sì—usa `TiffOptions` per creare immagini raster ad alta risoluzione.  
- **Which option controls canvas size in Java?** Quale opzione controlla il canvas size in Java?  
  `CadRasterizationOptions.setPageWidth/Height`.  
- **What is automatic layout scaling?** Cos'è **automatic layout scaling**?  
  Un flag (`setAutomaticLayoutsScaling(true)`) che preserva le proporzioni originali del layout quando il canvas size cambia.  
- **Do I need a license for Aspose.CAD?** Ho bisogno di una licenza per Aspose.CAD?  
  È necessaria una licenza temporanea o permanente per l'uso in produzione.

## How to Set PDF Page Size When Converting CAD to PDF (Java)

Impostare le dimensioni della pagina PDF (o canvas size) ti consente di definire le dimensioni finali del documento, il che è particolarmente utile quando devi **modificare le dimensioni del PDF** per adeguarle agli standard di stampa o ai requisiti dell'interfaccia utente. Di seguito esaminiamo ogni passaggio, spiegando il *perché* di ogni riga di codice.

## What is **convert CAD to PDF**?

Convertire CAD in PDF significa prendere disegni ingegneristici basati su vettori e renderizzarli come pagine PDF, preservando linee, livelli e geometria, rendendo il file universalmente accessibile.

## Why set canvas size **java**?

Perché impostare il canvas size **java**?  
Impostare il canvas size in Java ti consente di definire la risoluzione di output e le dimensioni della pagina, garantendo che il PDF o TIFF risultante corrisponda ai requisiti di stampa o visualizzazione. Ti offre anche il controllo sul comportamento di scaling, fondamentale per disegni di grande formato.

## Prerequisites

Prima di immergerti nel tutorial, assicurati di avere i seguenti prerequisiti in ordine:

- Aspose.CAD per Java: Assicurati di avere la libreria Aspose.CAD installata nel tuo ambiente Java. Puoi scaricarla [qui](https://releases.aspose.com/cad/java/).
- Directory dei documenti: Configura una directory per archiviare i tuoi file CAD. Questa directory verrà referenziata nei passaggi del tutorial.

Ora, iniziamo con la guida passo‑passo.

## Import Namespaces

In questo passaggio, importeremo i namespace necessari per avviare il tuo progetto Aspose.CAD.

```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## Step 1: Import Aspose.CAD Classes

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

In questo snippet, impostiamo il percorso della directory delle risorse e carichiamo un file DXF usando la classe `Image` di Aspose.CAD.

## Step 2: Set **CadRasterizationOptions** Properties (set canvas size java)

```java
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

Qui, creiamo un'istanza di `CadRasterizationOptions` e configuriamo proprietà come larghezza pagina, altezza pagina e **automatic layout scaling**. Questo è il nucleo di **configure canvas mode** per la tua conversione.

## Step 3: Create PdfOptions and Set VectorRasterizationOptions

```java
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Set the VectorRasterizationOptions property
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Ora, creiamo un'istanza di `PdfOptions` e impostiamo la sua proprietà `VectorRasterizationOptions` con il `CadRasterizationOptions` configurato in precedenza.

## Step 4: Export to PDF (convert cad to pdf)

```java
// Export CAD to PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

Infine, salviamo l'immagine CAD in un file PDF usando le opzioni specificate, completando il processo di **convert CAD to PDF**.

## Step 5: Create TiffOptions and Set VectorRasterizationOptions (export cad to tiff)

```java
// Create an instance of TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Set the VectorRasterizationOptions property
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

In questo passaggio, configuriamo un'istanza di `TiffOptions` e impostiamo la sua proprietà `VectorRasterizationOptions`.

## Step 6: Export to TIFF

```java
// Export CAD to TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

Infine, salviamo l'immagine CAD in un file TIFF usando le opzioni specificate, dimostrando come **export CAD to TIFF** dopo aver configurato il canvas size.

## Common Issues and Solutions

| Problema | Causa | Soluzione |
|----------|-------|-----------|
| Il PDF di output è vuoto | `setNoScaling(true)` disabilita il rendering per alcuni disegni | Rimuovere `setNoScaling(true)` o impostarlo su `false`. |
| La risoluzione del TIFF sembra bassa | Larghezza/altezza pagina troppo piccole | Incrementare i valori di `setPageWidth` / `setPageHeight`. |
| Il layout appare distorto | Automatic layout scaling disabilitato | Assicurarsi che `setAutomaticLayoutsScaling(true)` sia abilitato. |

## Why Adjust Canvas Size and DPI?

Modificare il Canvas Size influisce direttamente sulla risoluzione di rasterizzazione dell'output. Se hai bisogno di **aumentare la risoluzione del TIFF**, basta aumentare i valori di `setPageWidth` / `setPageHeight` o chiamare `rasterizationOptions.setResolution(300)` prima di creare il `TiffOptions`. Questo ti fornisce immagini raster ad alta qualità adatte alla stampa o a un'ispezione dettagliata.

## Frequently Asked Questions

### Q1: Can I use Aspose.CAD for Java with other Java frameworks?

Posso usare Aspose.CAD per Java con altri framework Java?  
Sì, Aspose.CAD è progettato per integrarsi senza problemi con vari framework Java.

### Q2: Is a temporary license available for Aspose.CAD?

È disponibile una licenza temporanea per Aspose.CAD?  
Sì, puoi ottenere una licenza temporanea [qui](https://purchase.aspose.com/temporary-license/).

### Q3: Where can I get community support for Aspose.CAD?

Dove posso ottenere supporto dalla community per Aspose.CAD?  
Visita il [forum di Aspose.CAD](https://forum.aspose.com/c/cad/19) per supporto della community e discussioni.

### Q4: Can I try Aspose.CAD for free?

Posso provare Aspose.CAD gratuitamente?  
Assolutamente! Ottieni una prova gratuita [qui](https://releases.aspose.com/).

### Q5: How do I purchase Aspose.CAD for Java?

Come posso acquistare Aspose.CAD per Java?  
Acquista il prodotto [qui](https://purchase.aspose.com/buy).

**Additional Q&A**

**Q: Does the canvas size affect vector quality in the PDF?**  
A: No. Canvas size controls page dimensions; vector data remains resolution‑independent, ensuring crisp rendering at any zoom level.

**Q: Can I set a different DPI for the TIFF output?**  
A: Yes. Adjust `rasterizationOptions.setResolution(dpiValue)` before creating `TiffOptions`.

**Q: How can I **change PDF dimensions** for an existing PDF without re‑rendering the CAD?**  
A: Use Aspose.PDF to load the generated PDF and call `pdf.getPages().setPageSize(PageSize.A4)` or a custom size.

**Q: What is the best way to **convert dxf to pdf** while preserving layers?**  
A: Keep `setAutomaticLayoutsScaling(true)` and avoid `setNoScaling(true)`; this retains layer visibility and layout fidelity.

## Conclusion

Congratulazioni! Hai convertito con successo **CAD in PDF** e **esportato CAD in TIFF** impostando **set canvas size java**, abilitando **automatic layout scaling**, e imparando a **configure canvas mode** per output di alta qualità. Questo tutorial fornisce una solida base per i tuoi progetti di conversione CAD. Esplora altre funzionalità e possibilità nella [documentazione di Aspose.CAD](https://reference.aspose.com/cad/java/).

---

**Last Updated:** 2026-02-15  
**Tested With:** Aspose.CAD per Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}