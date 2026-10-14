---
date: 2026-10-14
description: Scopri come la libreria Java CAD Aspose.CAD per Java può esportare DWG
  in PDF o immagini raster rapidamente e con precisione.
keywords:
- export dwg pdf
- high quality pdf
- dwg to pdf tutorial
- aspose cad java
- java cad library
lastmod: 2026-10-14
linktitle: Esporta DWG in PDF e immagini raster
og_description: Esporta DWG in PDF rapidamente con Aspose.CAD per Java. Scopri la
  conversione PDF di alta qualità, le opzioni raster e la licenza in questa guida
  passo‑passo.
og_image_alt: Tutorial showing Java code to convert DWG drawings to PDF and raster
  formats with Aspose.CAD
og_title: Esporta DWG in PDF e immagini raster usando la libreria Java CAD Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-10-14'
  description: Learn how the Java CAD library Aspose.CAD for Java can export DWG to
    PDF or raster images quickly and accurately.
  headline: Export DWG PDF and raster images using Java CAD library Aspose.CAD
  type: TechArticle
- description: Learn how the Java CAD library Aspose.CAD for Java can export DWG to
    PDF or raster images quickly and accurately.
  name: Export DWG PDF and raster images using Java CAD library Aspose.CAD
  steps:
  - name: Load the DWG file
    text: First, load your DWG drawing using the `Image` class. This creates an in‑memory
      representation that Aspose.CAD can work with.
  - name: Determine unit type
    text: Understanding whether the drawing uses metric or imperial units is essential
      for correct scaling. The helper method `IsMetric` (implementation omitted for
      brevity) returns a boolean flag.
  - name: Set rasterization options
    text: The `CadRasterizationOptions` class defines rasterization parameters such
      as DPI, page size, and unit conversion. Based on the unit system, configure
      page size, scaling, and the target unit type. These options drive how the DWG
      is rasterized before being wrapped into a PDF.
  - name: Configure PDF options (pdf options cad)
    text: The `PdfOptions` class specifies PDF‑specific settings, including compression
      and metadata. Create a `PdfOptions` instance and attach the rasterization settings.
      This tells Aspose.CAD how to embed the rasterized content into the final PDF.
  - name: Save as PDF
    text: The `save` method writes the image to the given file path using the supplied
      options. Finally, export the drawing to a PDF file. The `save` method takes
      the output path and the configured `PdfOptions`. When the code finishes, you’ll
      find **Saved.pdf** in your `DWGDrawings` folder, ready for distribu
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD for Java seamlessly integrates with popular Java frameworks
      such as Spring, Jakarta EE, and Android.
    question: Can I use Aspose.CAD for Java with other Java frameworks?
  - answer: Yes, you can obtain a temporary license **[obtain a temporary license](https://purchase.aspose.com/temporary-license/)**.
    question: Is a temporary license available for Aspose.CAD for Java?
  - answer: Visit the **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)** for
      assistance from the community and Aspose engineers.
    question: Where can I find support for Aspose.CAD for Java?
  - answer: You can purchase a license **[purchase a license](https://purchase.aspose.com/buy)**.
    question: How can I purchase a license for Aspose.CAD for Java?
  - answer: Aspose.CAD for Java supports both metric and imperial units, automatically
      detecting the drawing’s unit system.
    question: What units does Aspose.CAD for Java support?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- export dwg
- aspose.cad
- java cad conversion
title: Esporta DWG in PDF e immagini raster usando la libreria Java CAD Aspose.CAD
url: /it/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Esporta DWG PDF e immagini raster usando la libreria Java CAD Aspose.CAD

## Introduzione

L'esportazione di DWG in PDF è una necessità frequente per ingegneri, architetti e chiunque abbia bisogno di condividere disegni CAD senza esporre il formato nativo. Con **Aspose.CAD for Java**, è possibile **export dwg pdf** — o immagini raster — con poche righe di codice Java, mantenendo la fedeltà vettoriale e la precisione del layout. Questo tutorial ti guida attraverso il caricamento di un file DWG, la configurazione della rasterizzazione e il salvataggio del risultato come PDF o immagine ad alta qualità. Vedrai anche perché Aspose.CAD è la libreria Java CAD preferita per conversioni affidabili e cross‑platform.

Per una guida specifica solo sulla conversione PDF, vedi il [Tutorial per esportare DWG in PDF](/java/cad-drawing-conversion/export-dwg-to-pdf/).

## Risposte rapide
- **Di cosa tratta questo tutorial?** Esportazione di file DWG in PDF o immagini raster usando Aspose.CAD for Java.  
- **È necessaria una licenza?** È disponibile una licenza temporanea gratuita per la valutazione; è necessaria una licenza completa per la produzione.  
- **Quale versione di Java è supportata?** Qualsiasi runtime Java 8+ funziona con l'ultima API Java di Aspose.CAD.  
- **Posso convertire DWG in altri formati immagine?** Sì – le stesse opzioni di rasterizzazione consentono di generare PNG, JPEG, BMP, ecc.  
- **Quanto tempo richiede la conversione?** Tipicamente meno di un secondo per disegni standard; file più grandi possono richiedere qualche secondo.

## Perché la libreria Java CAD è la scelta migliore per la conversione DWG?

Aspose.CAD for Java è la scelta migliore perché offre un'implementazione pure‑Java che non richiede DLL native, rileva automaticamente unità metriche o imperiali, fornisce output raster fino a 1200 DPI e genera PDF che preservano i vettori senza dipendenze esterne. La libreria offre anche un modello di licenza flessibile che consente di iniziare con una licenza temporanea e scalare all'uso aziendale.

## Cos'è “export dwg to pdf”?

`Export dwg pdf` è il processo di conversione di un file di disegno DWG nativo in un documento PDF mantenendo i dati vettoriali, i layer e la scala. Questa conversione produce un file indipendente dal dispositivo che può essere visualizzato su qualsiasi piattaforma senza la necessità di AutoCAD. Poiché il PDF conserva le informazioni vettoriali, il testo rimane ricercabile e la grafica resta nitida a qualsiasi livello di zoom, rendendolo ideale per documentazione, revisione da parte del cliente e archiviazione.

## Perché usare Aspose.CAD Java per questa conversione?

Dovresti usare Aspose.CAD Java perché la libreria gestisce internamente la conversione delle unità, la rasterizzazione e l'incorporamento PDF, eliminando la necessità di strumenti di terze parti o pipeline complesse da riga di comando. La sua API è progettata per gli sviluppatori: un singolo oggetto `Image` rappresenta il disegno, e pochi oggetti di configurazione ti permettono di regolare DPI, dimensione della pagina e compressione. Il risultato è un output coerente e ripetibile su ambienti Windows, Linux e macOS.

## Prerequisiti

Prima di immergerti nel codice, assicurati di avere:

- Conoscenza di base della programmazione Java.  
- Libreria Aspose.CAD for Java installata. Se non l'hai ancora scaricata, ottienila **[download Aspose.CAD for Java](https://releases.aspose.com/cad/java/)**.  
- Un file DWG per i test – il campione **Bottom_plate.dwg** è usato in questa guida.

## Importa namespace

Nel tuo progetto Java, importa le classi necessarie per avviare la conversione:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## Guida passo‑passo

### Passo 1: Carica il file DWG

Per prima cosa, carica il tuo disegno DWG usando la classe `Image`. Questo crea una rappresentazione in memoria con cui Aspose.CAD può lavorare.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

### Passo 2: Determina il tipo di unità

Comprendere se il disegno utilizza unità metriche o imperiali è essenziale per una corretta scalatura. Il metodo di supporto `IsMetric` (implementazione omessa per brevità) restituisce un valore booleano.

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

### Passo 3: Imposta le opzioni di rasterizzazione

La classe `CadRasterizationOptions` definisce i parametri di rasterizzazione come DPI, dimensione della pagina e conversione delle unità. In base al sistema di unità, configura la dimensione della pagina, la scalatura e il tipo di unità di destinazione. Queste opzioni determinano come il DWG viene rasterizzato prima di essere inserito in un PDF.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();

if (currentUnitIsMetric) {
    // Metric units
    double metersCoeff = 1 / 1000.0;
    double scaleFactor = metersCoeff / currentUnitCoefficient;
    rasterizationOptions.setPageWidth((float)(210 * scaleFactor));
    rasterizationOptions.setPageHeight((float)(297 * scaleFactor));
    rasterizationOptions.setUnitType(UnitType.Millimeter);
} else {
    // Imperial units
    rasterizationOptions.setPageWidth((float)(8.27f / currentUnitCoefficient));
    rasterizationOptions.setPageHeight((float)(11.69f / currentUnitCoefficient));
    rasterizationOptions.setUnitType(UnitType.Inch);
}
```

### Passo 4: Configura le opzioni PDF (pdf options cad)

La classe `PdfOptions` specifica le impostazioni specifiche per PDF, inclusi compressione e metadati. Crea un'istanza `PdfOptions` e allega le impostazioni di rasterizzazione. Questo indica ad Aspose.CAD come incorporare il contenuto rasterizzato nel PDF finale.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

### Passo 5: Salva come PDF

Il metodo `save` scrive l'immagine nel percorso file specificato usando le opzioni fornite. Infine, esporta il disegno in un file PDF. Il metodo `save` accetta il percorso di output e le `PdfOptions` configurate.

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

Quando il codice termina, troverai **Saved.pdf** nella tua cartella `DWGDrawings`, pronto per la distribuzione o l'archiviazione.

## Come convertire immagini raster DWG con la libreria Java CAD?

Puoi convertire DWG in formati raster sostituendo `PdfOptions` con una classe di opzioni specifica per raster come `PngOptions` o `JpegOptions`. Riutilizza la stessa istanza `CadRasterizationOptions`, regola il formato di output e chiama il metodo `save` con il nuovo oggetto di opzioni. Questo approccio ti consente di generare file PNG, JPEG, BMP o TIFF con una singola modifica di riga, mantenendo coerente il flusso di lavoro.

## Come generare PDF DWG usando le opzioni PDF CAD?

L'esempio sopra già **generates pdf dwg** produce l'output. Per affinare la dimensione del PDF, abilita la compressione chiamando `pdfOptions.setCompress(true)`. Puoi anche incorporare metadati personalizzati, impostare la versione PDF o aggiungere protezione con password tramite proprietà aggiuntive di `PdfOptions`. Queste regolazioni ti danno il pieno controllo sul PDF finale senza uscire dal codice Java.

## Problemi comuni e suggerimenti

- **Dimensione della pagina errata** – Verifica nuovamente la logica di conversione delle unità; coefficienti non corrispondenti possono produrre pagine sovradimensionate.  
- **Font o spessori di linea mancanti** – Assicurati che il DWG faccia riferimento a tutte le risorse esterne prima della conversione.  
- **Prestazioni su disegni grandi** – Aumenta l'impostazione `DPI` in `CadRasterizationOptions` solo quando è richiesta una qualità superiore; DPI più basso velocizza l'elaborazione.  
- **Problemi di licenza** – Per la valutazione puoi usare una **temporary license Aspose**; è necessaria una licenza completa per le distribuzioni in produzione.

## Domande frequenti

**D: Posso usare Aspose.CAD per Java con altri framework Java?**  
R: Sì, Aspose.CAD per Java si integra perfettamente con i framework Java più diffusi come Spring, Jakarta EE e Android.

**D: È disponibile una licenza temporanea per Aspose.CAD per Java?**  
R: Sì, è possibile ottenere una licenza temporanea **[ottieni una licenza temporanea](https://purchase.aspose.com/temporary-license/)**.

**D: Dove posso trovare supporto per Aspose.CAD per Java?**  
R: Visita il **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)** per assistenza dalla community e dagli ingegneri di Aspose.

**D: Come posso acquistare una licenza per Aspose.CAD per Java?**  
R: Puoi acquistare una licenza **[acquista una licenza](https://purchase.aspose.com/buy)**.

**D: Quali unità supporta Aspose.CAD per Java?**  
R: Aspose.CAD per Java supporta sia unità metriche che imperiali, rilevando automaticamente il sistema di unità del disegno.

**D: Posso convertire DWG in altri formati immagine (ad es., PNG, JPEG) usando la stessa API?**  
R: Assolutamente. Sostituisci `PdfOptions` con le opzioni di immagine raster appropriate (ad es., `PngOptions`) e riutilizza lo stesso `CadRasterizationOptions`.

## Conclusione

Questo tutorial ha dimostrato come **export dwg pdf** e immagini raster usando la **java cad library** Aspose.CAD per Java. Seguendo la guida passo‑passo, puoi integrare una conversione CAD affidabile in qualsiasi applicazione Java, sia che tu abbia bisogno di PDF per la documentazione o di immagini raster per la visualizzazione web. La natura pure‑Java della libreria, l'output di alta qualità e la licenza flessibile la rendono una scelta solida sia per piccole utility sia per pipeline aziendali su larga scala.

---

**Ultimo aggiornamento:** 2026-10-14  
**Testato con:** Aspose.CAD for Java 24.10  
**Autore:** Aspose

## Tutorial correlati

- [Esporta DWG in PDF: layout specifico usando Aspose.CAD per Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Esporta DWG in PDF in Java – Imposta la dimensione della pagina PDF con Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)
- [Esporta DWG in PDF con linee nascoste – Aspose.CAD per Java](/cad/java/cad-text-and-formatting/support-hidden-lines-in-dwg/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}