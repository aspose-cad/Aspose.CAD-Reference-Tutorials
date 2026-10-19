---
date: 2026-10-19
description: Scopri come esportare i disegni AutoCAD in PDF con una custom PDF page
  size utilizzando Aspose.CAD per Java. Questa guida passo‑passo copre la conversione
  da DWG a PDF, le rasterization options e la licensing.
keywords:
- custom pdf page size
- export autocad to pdf
- save cad as pdf
- generate pdf from dwg
- dwg to pdf java
lastmod: 2026-10-19
linktitle: Esporta immagini AutoCAD in PDF
og_description: Imposta una custom PDF page size quando esporti i disegni AutoCAD
  in PDF usando Aspose.CAD per Java. Scopri la conversione da DWG a PDF, le rasterization
  settings e la licensing in pochi minuti.
og_image_alt: Guide showing how to export AutoCAD drawings to PDF with custom page
  dimensions using Aspose.CAD for Java
og_title: Imposta custom PDF page size per l'esportazione AutoCAD con Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-10-19'
  description: Learn how to export AutoCAD drawings to PDF with a custom PDF page
    size using Aspose.CAD for Java. This step‑by‑step guide covers converting DWG
    to PDF, rasterization options, and licensing.
  headline: Set custom PDF page size for AutoCAD export with Aspose.CAD
  type: TechArticle
- description: Learn how to export AutoCAD drawings to PDF with a custom PDF page
    size using Aspose.CAD for Java. This step‑by‑step guide covers converting DWG
    to PDF, rasterization options, and licensing.
  name: Set custom PDF page size for AutoCAD export with Aspose.CAD
  steps:
  - name: set the resource directory path
    text: '> **Pro tip:** Replace `"Your Document Directory"` with the absolute path
      to the folder you created in the prerequisites.'
  - name: load the CAD image
    text: The `Image` class loads the CAD file and gives you access to Aspose.CAD’s
      rasterization engine. > **Why this matters:** Once the CAD file is loaded, you
      can manipulate rasterization options before rendering to PDF.
  - name: set rasterization options
    text: The `CadRasterizationOptions` class specifies how the CAD drawing is rasterized
      before being saved as PDF. Adjust `pageWidth` and `pageHeight` to define a **custom
      PDF page size**. You can also enable 3‑D rendering by uncommenting the `setTypeOfEntities`
      line. - `pageWidth` / `pageHeight` – measured
  - name: configure PDF options
    text: The `PdfOptions` class holds PDF‑specific settings and links the rasterization
      options to the output file, ensuring the custom page dimensions are applied
      correctly.
  - name: save the PDF
    text: The `save` method writes the rendered image to the specified PDF file. The
      resulting file, `Export3DImagestoPDF_out_.pdf`, is a **save cad as pdf** representation
      of your original AutoCAD drawing with the exact page dimensions you specified.
  type: HowTo
- questions:
  - answer: Yes, the library supports DWG, DXF, DWF, DGN, and many more, giving you
      flexibility across projects.
    question: Can I use Aspose.CAD for Java with other CAD file formats?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to request a time‑limited license for evaluation.
    question: How do I obtain a temporary license for Aspose.CAD for Java?
  - answer: Absolutely. Use `setLayouts("Model")` or specify other layout names to
      control which view is rendered.
    question: Are there layout options for rasterization?
  - answer: Yes – modify `pageWidth` and `pageHeight` in the rasterization options
      to any dimensions you need.
    question: Can I customize the size of the output PDF file?
  - answer: The dedicated [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) offers
      community support and official responses from the Aspose team.
    question: Where can I get help or discuss issues related to Aspose.CAD for Java?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- custom pdf page size
- Aspose.CAD
- Java CAD conversion
- PDF generation
- DWG export
title: Imposta custom PDF page size per l'esportazione AutoCAD con Aspose.CAD
url: /it/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Esporta PDF AutoCAD - esporta immagini AutoCAD in PDF con Aspose.CAD per Java

## Introduzione

Se hai bisogno di **convertire DWG in PDF** e controllare le dimensioni esatte del file di output, sei nel posto giusto. Questo tutorial ti mostra come impostare una **dimensione pagina PDF personalizzata** durante l'esportazione di immagini AutoCAD in PDF con Aspose.CAD per Java. Alla fine della guida saprai come caricare un DWG, configurare le opzioni di rasterizzazione come DPI e larghezza/altezza della pagina, applicare una licenza e generare un PDF pronto per la produzione.

## Risposte rapide
- **Posso convertire DWG in PDF con Java?** Sì – Aspose.CAD for Java nativamente supporta DWG, DXF, DWF e molti altri formati CAD.  
- **È necessaria una licenza per l'uso in produzione?** Una licenza completa di Aspose.CAD rimuove tutti i limiti di valutazione; è disponibile una licenza temporanea per i test.  
- **Quali versioni di Java sono compatibili?** La libreria funziona con Java 8 e qualsiasi JDK successivo.  
- **Come modifico le dimensioni della pagina PDF?** Imposta `pageWidth` e `pageHeight` su `PdfOptions.getRasterizationOptions()` alla dimensione desiderata.  
- **Il rendering 3‑D è supportato?** Sì – enable `TypeOfEntities.Entities3D` to rasterize 3‑D entities.

## Cos'è l'esportazione PDF AutoCAD?

Esportare PDF AutoCAD significa convertire disegni CAD basati su vettori (DWG, DXF, DWF, ecc.) in un documento PDF portatile mantenendo i layer, gli spessori delle linee e la geometria 3‑D opzionale. Questo ti consente di condividere i progetti con i clienti, archiviare i disegni o stampare senza installare software CAD.

## Perché usare Aspose.CAD per Java per convertire DWG in PDF?

Aspose.CAD per Java è ideale per convertire DWG in PDF perché offre un ampio supporto di formati, funziona su Java puro senza dipendenze native, fornisce rasterizzazione ad alta risoluzione con pieno controllo su DPI e dimensione della pagina, e include licenze flessibili che ti permettono di iniziare con una versione di prova e passare alla produzione.

- **Ampia copertura di formati** – supporta oltre 50 formati di input e output, inclusi DWG, DXF, DWF, DGN e PDF.  
- **Implementazione Java pura** – nessun DLL nativo o dipendenze esterne, quindi il deployment è semplice su qualsiasi piattaforma.  
- **Rasterizzazione ad alta risoluzione** – puoi specificare DPI, dimensione della pagina e layout, dandoti pieno controllo sulla **dimensione pagina PDF personalizzata** del risultato.  
- **Licenza scalabile** – inizia con una prova gratuita, poi passa a una **licenza Aspose CAD** permanente.  

## Prerequisiti

- **Java Development Kit** – JDK 8 o versioni successive installate sulla tua macchina.  
- **Aspose.CAD for Java** – scarica l'ultimo JAR dal [download link](https://releases.aspose.com/cad/java/).  
- **Directory di lavoro** – una cartella che contiene i file DWG di origine e riceverà i PDF generati.

## Importa namespace

La classe `Image` è l'oggetto principale di Aspose.CAD che rappresenta un disegno CAD in memoria. Importa i package necessari prima di iniziare a scrivere il codice.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

Ora esaminiamo il codice passo dopo passo.

## Come impostare una dimensione pagina PDF personalizzata durante l'esportazione di DWG in PDF?

Carica il tuo DWG, definisci la larghezza e l'altezza della pagina desiderate, quindi salva il risultato come PDF – è tutto ciò che serve per creare un PDF con una dimensione pagina personalizzata. I passaggi seguenti illustrano la sequenza esatta e il codice minimo necessario.

### Passo 1: imposta il percorso della directory delle risorse

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **Consiglio professionale:** Sostituisci `"Your Document Directory"` con il percorso assoluto della cartella creata nei prerequisiti.

### Passo 2: carica l'immagine CAD

La classe `Image` carica il file CAD e ti dà accesso al motore di rasterizzazione di Aspose.CAD.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **Perché è importante:** una volta caricato il file CAD, puoi manipolare le opzioni di rasterizzazione prima di renderizzare in PDF.

### Passo 3: imposta le opzioni di rasterizzazione

La classe `CadRasterizationOptions` specifica come il disegno CAD viene rasterizzato prima di essere salvato come PDF. Regola `pageWidth` e `pageHeight` per definire una **dimensione pagina PDF personalizzata**. Puoi anche abilitare il rendering 3‑D decommentando la riga `setTypeOfEntities`.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- `pageWidth` / `pageHeight` – misurati in pixel; modifica questi valori per corrispondere a A4, Letter o qualsiasi dimensione personalizzata.  
- `setTypeOfEntities(TypeOfEntities.Entities3D)` – renderizza le entità 3‑D quando necessario.  
- `setLayouts` – seleziona quale layout (Model, Layout1, ecc.) rasterizzare.

### Passo 4: configura le opzioni PDF

La classe `PdfOptions` contiene le impostazioni specifiche per PDF e collega le opzioni di rasterizzazione al file di output, garantendo che le dimensioni personalizzate della pagina vengano applicate correttamente.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Passo 5: salva il PDF

Il metodo `save` scrive l'immagine renderizzata nel file PDF specificato.

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

Il file risultante, `Export3DImagestoPDF_out_.pdf`, è una rappresentazione **save cad as pdf** del tuo disegno AutoCAD originale con le esatte dimensioni della pagina specificate.

## Problemi comuni e soluzioni

| Sintomo | Causa probabile | Soluzione |
|---------|-----------------|-----------|
| Output PDF vuoto | Opzioni di rasterizzazione non impostate o layout non corrispondente | Verifica che `setLayouts` corrisponda al nome del layout nel tuo file CAD. |
| Immagine a bassa risoluzione | `pageWidth`/`pageHeight` troppo piccoli o DPI basso | Aumenta le dimensioni o chiama `rasterizationOptions.setResolution(...)` con un DPI più alto. |
| Eccezione di licenza | Nessuna licenza valida applicata | Applica una licenza permanente di Aspose.CAD o utilizza una licenza temporanea per i test. |

## Domande frequenti

**Q: Posso usare Aspose.CAD per Java con altri formati di file CAD?**  
A: Sì, la libreria supporta DWG, DXF, DWF, DGN e molti altri, offrendoti flessibilità in tutti i progetti.

**Q: Come posso ottenere una licenza temporanea per Aspose.CAD per Java?**  
A: Visita la [temporary license page](https://purchase.aspose.com/temporary-license/) per richiedere una licenza a tempo limitato per la valutazione.

**Q: Esistono opzioni di layout per la rasterizzazione?**  
A: Assolutamente. Usa `setLayouts("Model")` o specifica altri nomi di layout per controllare quale vista viene renderizzata.

**Q: Posso personalizzare la dimensione del file PDF di output?**  
A: Sì – modifica `pageWidth` e `pageHeight` nelle opzioni di rasterizzazione a qualsiasi dimensione necessaria.

**Q: Dove posso ottenere aiuto o discutere problemi relativi ad Aspose.CAD per Java?**  
A: Il forum dedicato [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) offre supporto della community e risposte ufficiali dal team Aspose.

## FAQ aggiuntive (formato AI‑friendly)

**Q: Aspose.CAD richiede librerie native su Windows o Linux?**  
A: No. Aspose.CAD per Java è una libreria pure‑Java, quindi funziona su qualsiasi piattaforma che supporta il JDK senza DLL native aggiuntive.

**Q: Quanto grande può essere un file DWG che la libreria può elaborare?**  
A: La libreria può gestire disegni di centinaia di pagine (fino a 500 MB) senza caricare l'intero file in memoria, grazie alla sua architettura di streaming.

**Q: È possibile convertire in batch molti file DWG in PDF in un'unica esecuzione?**  
A: Sì. Itera su una directory, carica ogni file con `Image.load()`, applica le stesse opzioni di rasterizzazione e chiama `save()` per ogni PDF di output.

**Q: Quale performance posso aspettarmi su un server tipico?**  
A: Convertire un DWG di 100 pagine a 300 DPI su una CPU standard da 2.5 GHz richiede circa 12 secondi, secondo i test di benchmark di Aspose.

**Q: La libreria preserva le informazioni dei layer nel PDF?**  
A: Sebbene l'output sia rasterizzato, l'aspetto visivo dei layer, degli spessori delle linee e dei colori è riprodotto fedelmente.

---

**Ultimo aggiornamento:** 2026-10-19  
**Testato con:** Aspose.CAD for Java 24.10  
**Autore:** Aspose

## Tutorial correlati

- [Esporta DWG in PDF e abilita il tracciamento con Aspose.CAD Java](/cad/java/additional-features/enable-tracking/)
- [Esporta DWG in PDF: layout specifico usando Aspose.CAD Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Esporta DWG in BMP e regola la dimensione CAD usando il tipo unità con Aspose.CAD per Java](/cad/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}