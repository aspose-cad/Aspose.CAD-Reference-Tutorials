---
date: 2026-10-19
description: Scopri come creare file IFC con miniatura PNG usando Aspose.CAD for Java
  in poche righe di codice.
keywords:
- create png thumbnail ifc
- ifc to png conversion
- aspose cad java
- java image processing
- bIM visualization
lastmod: 2026-10-19
linktitle: Esporta IFC in PNG
og_description: Crea file IFC con miniatura PNG senza sforzo usando Aspose.CAD for
  Java. Questa guida passo‑passo ti mostra come caricare, rasterizzare e salvare i
  modelli IFC come immagini PNG ad alta qualità.
og_image_alt: Developer guide showing Java code that converts IFC files to PNG thumbnails
  using Aspose.CAD
og_title: Crea una miniatura PNG di file IFC con Aspose.CAD for Java
schemas:
- author: Aspose
  dateModified: '2026-10-19'
  description: Learn how to create PNG thumbnail IFC files with Aspose.CAD for Java
    in just a few lines of code.
  headline: How to create PNG thumbnail IFC with Aspose.CAD for Java
  type: TechArticle
- description: Learn how to create PNG thumbnail IFC files with Aspose.CAD for Java
    in just a few lines of code.
  name: How to create PNG thumbnail IFC with Aspose.CAD for Java
  steps:
  - name: load the IFC file
    text: First, point to the folder where your IFC file lives and load it with `CadImage.load`.
      `CadImage.load` reads a CAD file and returns an image object that can be rasterized.
      > **Why this matters:** Loading the file as a `CadImage` gives you access to
      vector‑raster conversion options that control resol
  - name: set rasterization options
    text: Define the output dimensions and any other vector‑related settings through
      `VectorRasterizationOptions`. `VectorRasterizationOptions` lets you specify
      output size, background color, and other rasterization parameters. > Adjust
      `PageWidth` and `PageHeight` to control the final PNG resolution, which i
  - name: configure PNG options
    text: Link the rasterization options to the PNG exporter by creating a `PngOptions`
      instance.
  - name: save the image as PNG
    text: Finally, write the rasterized image to disk using the `save` method. `save`
      writes the rasterized image to the specified file path in the chosen format.
      > After this step you have successfully **created a PNG thumbnail IFC** and
      can use the resulting `example.png` anywhere you need a raster image.
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD supports many formats (DWG, DXF, DGN, etc.). Simply change
      the file extension and load the appropriate image class.
    question: Can I use this approach to convert other CAD formats to PNG?
  - answer: DPI is controlled indirectly via `PageWidth`/`PageHeight`. Adjust these
      values relative to the desired physical size to achieve the required DPI.
    question: Does the library let me set a custom DPI?
  - answer: PNG is a lossless format, so the rasterized image retains the full visual
      fidelity of the original vector data.
    question: Is the PNG output loss‑less?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- ifc conversion
- png thumbnail
- aspose.cad
- java image processing
- bim visualization
title: Come creare una miniatura PNG di file IFC con Aspose.CAD for Java
url: /it/java/cad-export-options/export-ifc-to-png/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Esporta IFC in PNG con Aspose.CAD per Java

## Introduzione

In questo tutorial imparerai a **create PNG thumbnail IFC** file con Aspose.CAD per Java. Che tu abbia bisogno di anteprime rapide per un portale BIM, generare miniature per un sistema di gestione documentale, o automatizzare conversioni batch, i passaggi seguenti ti permettono di rasterizzare un modello IFC 3‑D in un'immagine PNG 2‑D nitida in poche righe di codice Java.

## Risposte rapide
- **Quale libreria è necessaria?** Aspose.CAD per Java.  
- **Posso creare un PNG thumbnail IFC in poche righe di codice?** Sì – l'intero flusso di lavoro si adatta a meno di 20 righe.  
- **Ho bisogno di una licenza per la produzione?** Una licenza temporanea funziona per i test; è necessaria una licenza completa per il rilascio commerciale.  
- **L'output è scalabile?** Puoi impostare qualsiasi dimensione in pixel, quindi il PNG si adatta a qualsiasi dimensione tu necessiti.  
- **Quale versione di Java è supportata?** Java 8 o superiore.

## Cos'è “convertire IFC in PNG”?
Convertire IFC (Industry Foundation Classes) in PNG significa rasterizzare il modello edilizio 3‑D in un'immagine bitmap 2‑D. Questo processo crea una miniatura visiva che può essere visualizzata nei browser, nei report o nelle app mobili senza richiedere un visualizzatore CAD completo.

## Perché usare Aspose.CAD per Java?
Aspose.CAD supporta **oltre 30 formati CAD e BIM**, inclusi IFC, DWG, DXF e DGN, e può elaborare file fino a **2 GB** senza caricare l'intero documento in memoria. La libreria è pure Java, ha **zero dipendenze esterne**, e gira su Windows, Linux e macOS, rendendola ideale per la generazione di immagini lato server.  
Fornisce rasterizzazione ad alte prestazioni, ampio supporto di formati e facile integrazione nelle applicazioni Java.

## Prerequisiti

- **Aspose.CAD Library** – scarica l'ultimo JAR dal [download link](https://releases.aspose.com/cad/java/).  
- **Java Development Kit** – JDK 8 o più recente installato sulla tua macchina.  
- **IFC source file** – posiziona il file in una cartella a cui puoi fare riferimento dal tuo codice.

## Importa namespace

Il package `com.aspose.cad` fornisce tutte le classi necessarie. `CadImage` è il punto di ingresso per caricare file CAD, mentre `PngOptions` configura le impostazioni di rasterizzazione.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## Come creare PNG thumbnail IFC in Java?

Carica il file IFC, definisci le opzioni di rasterizzazione e salva il risultato come immagine PNG – questo è il flusso di lavoro completo di conversione. Le sezioni seguenti scompongono ogni passaggio, così puoi copiare‑incollare gli snippet nel tuo progetto e eseguirli immediatamente.

### Passo 1: caricare il file IFC
Prima, indica la cartella dove si trova il tuo file IFC e caricalo con `CadImage.load`.  
`CadImage.load` legge un file CAD e restituisce un oggetto immagine che può essere rasterizzato.

```java
String dataDir = "Your Document Directory" + "ExportingIFC/";
String fileName = dataDir + "example.ifc";
IfcImage cadImage = (IfcImage)Image.load(fileName);
```

> **Perché è importante:** Caricare il file come `CadImage` ti dà accesso alle opzioni di conversione vettore‑raster che controllano la risoluzione, il colore di sfondo e lo spessore della linea.

### Passo 2: impostare le opzioni di rasterizzazione
Definisci le dimensioni di output e altre impostazioni correlate al vettore tramite `VectorRasterizationOptions`.  
`VectorRasterizationOptions` ti consente di specificare la dimensione di output, il colore di sfondo e altri parametri di rasterizzazione.

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

> Regola `PageWidth` e `PageHeight` per controllare la risoluzione finale del PNG, fondamentale quando **save PNG java** files per stampe ad alta qualità o miniature web.

### Passo 3: configurare le opzioni PNG
Collega le opzioni di rasterizzazione all'esportatore PNG creando un'istanza di `PngOptions`.

```java
PngOptions pngOptions = new PngOptions();
pngOptions.setVectorRasterizationOptions(vectorOptions);
```

### Passo 4: salvare l'immagine come PNG
Infine, scrivi l'immagine rasterizzata su disco usando il metodo `save`.  
`save` scrive l'immagine rasterizzata nel percorso file specificato nel formato scelto.

```java
String outPath = dataDir + "example.png";
cadImage.save(outPath, pngOptions);
```

> Dopo questo passaggio hai **creato con successo un PNG thumbnail IFC** e puoi utilizzare il `example.png` risultante ovunque ti serva un'immagine raster.

## Casi d'uso comuni
- **Generare miniature** per modelli BIM nei portali web.  
- **Incorporare snapshot di planimetrie** in report PDF o Word.  
- **Conversione batch automatizzata** di grandi librerie IFC per progetti di archiviazione o migrazione.

## Risoluzione dei problemi e consigli
- **Problemi di memoria:** Per file IFC molto grandi, aumenta l'heap JVM (`-Xmx2g` o superiore).  
- **Texture mancanti:** Assicurati che le risorse esterne del file IFC siano raggiungibili dalla `dataDir`.  
- **Consiglio professionale:** Usa `vectorOptions.setBackgroundColor(Color.getWhite())` se preferisci uno sfondo bianco invece del PNG trasparente predefinito.

## FAQ

### Q1: Aspose.CAD è compatibile con tutte le versioni dei file IFC?
A1: Aspose.CAD supporta varie versioni di IFC. Consulta la [documentazione](https://reference.aspose.com/cad/java/) per informazioni dettagliate sulla compatibilità.

### Q2: Posso personalizzare ulteriormente le opzioni di rasterizzazione?
A2: Assolutamente! Esplora la [documentazione](https://reference.aspose.com/cad/java/) per impostazioni avanzate come il controllo DPI, l'anti‑aliasing e lo spessore delle linee.

### Q3: È disponibile una versione di prova?
A3: Sì, puoi scaricare la versione di prova gratuita dal [Aspose.CAD free trial](https://releases.aspose.com/).

### Q4: Come posso ottenere una licenza temporanea per i test?
A4: Ottieni una licenza temporanea dalla [pagina di licenza temporanea di Aspose.CAD](https://purchase.aspose.com/temporary-license/).

### Q5: Dove posso fare domande o segnalare problemi?
A5: Unisciti alla community sul [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) per supporto sia dagli ingegneri Aspose sia da altri sviluppatori.

## Domande frequenti

**Q: Posso usare questo approccio per convertire altri formati CAD in PNG?**  
A: Sì, Aspose.CAD supporta molti formati (DWG, DXF, DGN, ecc.). Basta cambiare l'estensione del file e caricare la classe immagine appropriata.

**Q: La libreria permette di impostare un DPI personalizzato?**  
A: Il DPI è controllato indirettamente tramite `PageWidth`/`PageHeight`. Regola questi valori in base alle dimensioni fisiche desiderate per ottenere il DPI richiesto.

**Q: L'output PNG è loss‑less?**  
A: PNG è un formato lossless, quindi l'immagine rasterizzata mantiene la piena fedeltà visiva dei dati vettoriali originali.

## Conclusione

Ora disponi di un metodo completo e pronto per la produzione per **create PNG thumbnail IFC** file usando Aspose.CAD per Java. Integra questi passaggi in strumenti desktop, servizi lato server o funzioni cloud per automatizzare le pipeline di visualizzazione BIM e fornire miniature rapide e di alta qualità agli utenti finali.

---

**Last Updated:** 2026-10-19  
**Tested With:** Aspose.CAD for Java 24.11  
**Author:** Aspose

## Tutorial correlati

- [Come convertire STL in PNG con Aspose.CAD per Java](/cad/java/cad-export-options/export-stl-to-png/)
- [Converti DWG in PNG – Salva CAD come PNG usando Aspose.CAD per Java](/cad/java/cad-drawing-conversion/convert-cad-drawing-to-raster-image/)
- [Esporta DWG in PDF in Java – Imposta la dimensione della pagina PDF con Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}