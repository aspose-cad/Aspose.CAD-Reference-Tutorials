---
date: 2025-12-10
description: Scopri come convertire CAD in PDF usando Aspose.CAD per Java impostando
  la dimensione della tela, la scala automatica del layout e l'esportazione in TIFF.
linktitle: Convert CAD to PDF – Set Canvas Size & Mode
second_title: Aspose.CAD Java API
title: Converti CAD in PDF – Imposta dimensione e modalità della tela (Java)
url: /it/java/advanced-cad-features/set-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Imposta la Dimensione della Tela e la Modalità

## Introduzione

Stai cercando di **convertire CAD in PDF** mantenendo il pieno controllo sulla dimensione della tela e sulla modalità di rendering? Questa guida completa ti accompagna passo passo nell'impostare la dimensione della tela in Java, abilitare lo scaling automatico del layout e quindi esportare il risultato sia in PDF sia in TIFF usando Aspose.CAD. Che tu stia perfezionando una pipeline di produzione o sperimentando con un prototipo, troverai istruzioni chiare e pratiche qui.

## Risposte Rapide
- **Cosa significa “convertire CAD in PDF”?** Trasformare un disegno CAD (ad es. DXF, DWG) in un documento PDF visualizzabile su qualsiasi piattaforma.  
- **Posso anche esportare in TIFF?** Sì—usa `TiffOptions` per creare immagini raster ad alta risoluzione.  
- **Quale opzione controlla la dimensione della tela in Java?** `CadRasterizationOptions.setPageWidth/Height`.  
- **Cos’è lo scaling automatico del layout?** Un flag (`setAutomaticLayoutsScaling(true)`) che preserva le proporzioni originali del layout quando la dimensione della tela cambia.  
- **È necessaria una licenza per Aspose.CAD?** È richiesta una licenza temporanea o permanente per l'uso in produzione.

## Che cosa è **convertire CAD in PDF**?

Convertire CAD in PDF significa prendere disegni ingegneristici basati su vettori e renderizzarli come pagine PDF, preservando linee, layer e geometria, rendendo il file universalmente accessibile.

## Perché impostare la dimensione della tela **java**?

Impostare la dimensione della tela in Java ti consente di definire la risoluzione di output e le dimensioni della pagina, garantendo che il PDF o il TIFF risultante corrispondano ai requisiti di stampa o visualizzazione. Ti dà anche controllo sul comportamento di scaling, fondamentale per disegni di grande formato.

## Prerequisiti

Prima di immergerti nel tutorial, assicurati di avere i seguenti prerequisiti:

- Aspose.CAD per Java: Verifica di aver installato la libreria Aspose.CAD nel tuo ambiente Java. Puoi scaricarla [qui](https://releases.aspose.com/cad/java/).

- Directory dei Documenti: Configura una directory per memorizzare i tuoi file CAD. Questa directory sarà referenziata nei passaggi del tutorial.

Ora, iniziamo con la guida passo‑passo.

## Importa i Namespace

In questo passaggio, importeremo i namespace necessari per avviare il tuo progetto Aspose.CAD.

```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## Passo 1: Importa le Classi Aspose.CAD

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

In questo snippet, impostiamo il percorso della directory delle risorse e carichiamo un file DXF usando la classe `Image` di Aspose.CAD.

## Passo 2: Imposta le Proprietà di **CadRasterizationOptions** (imposta dimensione tela java)

```java
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

Qui creiamo un'istanza di `CadRasterizationOptions` e configuriamo proprietà come larghezza pagina, altezza pagina e **automatic layout scaling**. Questo è il cuore della **configurazione della modalità tela** per la tua conversione.

## Passo 3: Crea PdfOptions e Imposta VectorRasterizationOptions

```java
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Set the VectorRasterizationOptions property
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Ora creiamo un'istanza di `PdfOptions` e impostiamo la sua proprietà `VectorRasterizationOptions` con le `CadRasterizationOptions` configurate in precedenza.

## Passo 4: Esporta in PDF (convertire cad in pdf)

```java
// Export CAD to PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

Infine, salviamo l'immagine CAD in un file PDF usando le opzioni specificate, completando il processo di **convertire CAD in PDF**.

## Passo 5: Crea TiffOptions e Imposta VectorRasterizationOptions (esportare cad in tiff)

```java
// Create an instance of TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Set the VectorRasterizationOptions property
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

In questo passaggio, configuriamo un'istanza di `TiffOptions` e impostiamo la sua proprietà `VectorRasterizationOptions`.

## Passo 6: Esporta in TIFF

```java
// Export CAD to TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

Infine, salviamo l'immagine CAD in un file TIFF usando le opzioni specificate, dimostrando come **esportare CAD in TIFF** dopo aver configurato la dimensione della tela.

## Problemi Comuni e Soluzioni

| Problema | Causa | Soluzione |
|----------|-------|-----------|
| Il PDF di output è vuoto | `setNoScaling(true)` disabilita il rendering per alcuni disegni | Rimuovi `setNoScaling(true)` o impostalo su `false`. |
| La risoluzione del TIFF appare bassa | Larghezza/altezza pagina troppo piccole | Aumenta i valori di `setPageWidth` / `setPageHeight`. |
| Il layout appare distorto | Scaling automatico del layout disabilitato | Assicurati che `setAutomaticLayoutsScaling(true)` sia abilitato. |

## Conclusione

Congratulazioni! Hai convertito con successo **CAD in PDF** e **esportato CAD in TIFF** impostando **dimensione tela java**, abilitando **automatic layout scaling**, e imparato a **configurare la modalità tela** per output di alta qualità. Questo tutorial fornisce una solida base per i tuoi progetti di conversione CAD. Esplora altre funzionalità e possibilità nella [documentazione di Aspose.CAD](https://reference.aspose.com/cad/java/).

## FAQ

### Q1: Posso usare Aspose.CAD per Java con altri framework Java?

A1: Sì, Aspose.CAD è progettato per integrarsi senza problemi con vari framework Java.

### Q2: È disponibile una licenza temporanea per Aspose.CAD?

A2: Sì, puoi ottenere una licenza temporanea [qui](https://purchase.aspose.com/temporary-license/).

### Q3: Dove posso trovare supporto della community per Aspose.CAD?

A3: Visita il [forum di Aspose.CAD](https://forum.aspose.com/c/cad/19) per supporto e discussioni.

### Q4: Posso provare Aspose.CAD gratuitamente?

A4: Assolutamente! Ottieni una prova gratuita [qui](https://releases.aspose.com/).

### Q5: Come acquisto Aspose.CAD per Java?

A5: Acquista il prodotto [qui](https://purchase.aspose.com/buy).

**Domande aggiuntive**

**D: La dimensione della tela influisce sulla qualità vettoriale nel PDF?**  
R: No. La dimensione della tela controlla le dimensioni della pagina; i dati vettoriali rimangono indipendenti dalla risoluzione, garantendo una resa nitida a qualsiasi livello di zoom.

**D: Posso impostare un DPI diverso per l'output TIFF?**  
R: Sì. Regola `rasterizationOptions.setResolution(dpiValue)` prima di creare `TiffOptions`.

---

**Ultimo aggiornamento:** 2025-12-10  
**Testato con:** Aspose.CAD per Java 24.12  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}