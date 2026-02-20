---
date: 2026-02-20
description: Scopri come convertire STL in PNG usando Aspose.CAD per Java. Questa
  guida passo passo mostra come esportare i file STL in modo efficiente.
linktitle: Export STL to PNG
second_title: Aspose.CAD Java API
title: Come convertire STL in PNG con Aspose.CAD per Java
url: /it/java/cad-export-options/export-stl-to-png/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Converti STL in PNG con Aspose.CAD per Java

## Introduzione

Se hai bisogno di **convertire STL in PNG** in un'applicazione Java, Aspose.CAD per Java rende il lavoro veloce e affidabile. In questo tutorial percorreremo l'intero processo—dalla configurazione del progetto al salvataggio dell'immagine PNG finale—così potrai integrare la conversione STL nel tuo flusso di lavoro con sicurezza.

## Risposte Rapide
- **Cosa fa la libreria?** Converte formati CAD (incluso STL) in immagini raster come PNG.  
- **Quale linguaggio è usato?** Java, con l'API Aspose.CAD.  
- **È necessaria una licenza?** È richiesta una licenza temporanea o completa per l'uso in produzione.  
- **Quanto tempo richiede l'implementazione?** Circa 10‑15 minuti per una conversione di base.  
- **Posso personalizzare le dimensioni dell'immagine?** Sì, tramite `CadRasterizationOptions`.

## Cos'è la conversione da STL a PNG?

Convertire STL in PNG trasforma un file mesh 3‑D (STL) in un'immagine raster 2‑D (PNG). Questo è utile quando serve un'anteprima visiva rapida, generare miniature o incorporare il modello in pagine web senza richiedere un visualizzatore 3‑D.

## Perché usare Aspose.CAD per Java?

- **API completa** – Gestisce molti formati CAD, non solo STL.  
- **Nessuna dipendenza esterna** – Java puro, facile da aggiungere a qualsiasi progetto Maven/Gradle.  
- **Output raster di alta qualità** – Controllo su risoluzione, sfondo e anti‑aliasing.  
- **Supporta scenari “come esportare STL”** – Ideale per elaborazioni batch o conversioni in tempo reale.

## Prerequisiti

- Java Development Kit (JDK) installato sulla tua macchina.  
- Libreria Aspose.CAD per Java scaricata. Puoi ottenerla [qui](https://releases.aspose.com/cad/java/).  
- Una licenza valida o una licenza temporanea da [qui](https://purchase.aspose.com/temporary-license/).

## Importa Namespace

Nel tuo progetto Java, importa le classi necessarie:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Ora, suddividiamo l'esempio in più passaggi.

## Passo 1: Configura il tuo progetto

Crea un nuovo progetto Java e aggiungi la libreria Aspose.CAD per Java alle dipendenze del progetto (Maven, Gradle o inclusione manuale del JAR).

## Passo 2: Specifica il tuo file STL

Definisci il percorso al file STL che desideri convertire:

```java
String dataDir = "Your Document Directory" + "ExportingSTL/";
String fileName = dataDir + "example.stl";
```

## Passo 3: Carica il file STL

Carica il file STL usando il metodo `Image.load`. Questo crea un oggetto **CAD image** che puoi rasterizzare:

```java
CadImage cadImage = (CadImage)Image.load(fileName);
```

## Passo 4: Configura le opzioni di rasterizzazione

Imposta le opzioni di rasterizzazione per controllare dimensione e qualità del PNG di output. Queste opzioni fanno parte del processo di conversione **cad image to png**:

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

## Passo 5: Configura le opzioni PNG

Crea un'istanza di `PngOptions`. Se vuoi applicare le impostazioni di rasterizzazione, decommenta la riga sotto:

```java
PngOptions pngOptions = new PngOptions();
// Uncomment the line below if you want to set vector rasterization options
// pngOptions.setVectorRasterizationOptions(vectorOptions);
```

## Passo 6: Salva come PNG

Infine, esporta l'immagine CAD in un file PNG—questo è il passo **save PNG Java**:

```java
String outPath = dataDir + "galeon.stl.png";
cadImage.save(outPath, pngOptions);
```

> **Suggerimento:** Regola `PageWidth` e `PageHeight` per corrispondere alle dimensioni della miniatura desiderata per una elaborazione più veloce.

Congratulazioni! Hai convertito con successo un file STL in PNG usando Aspose.CAD per Java.

## Problemi comuni e soluzioni

| Problema | Motivo | Soluzione |
|----------|--------|-----------|
| Output PNG vuoto | Opzioni di rasterizzazione non impostate | Decommenta `pngOptions.setVectorRasterizationOptions(vectorOptions);` o specifica un colore di sfondo |
| OutOfMemoryError su file STL grandi | Memoria heap insufficiente | Aumenta l'heap JVM (`-Xmx2g`) o elabora il file a blocchi |
| LicenseException | Nessuna licenza valida | Applica una licenza temporanea o acquistata prima di caricare l'immagine |

## Domande frequenti

### D1: Aspose.CAD per Java è compatibile con tutte le versioni di file STL?
R1: Aspose.CAD per Java supporta varie versioni di file STL, garantendo la compatibilità con la maggior parte dei formati comuni.

### D2: Posso usare Aspose.CAD per Java in un progetto commerciale?
R2: Sì, puoi. Basta ottenere una licenza valida da [qui](https://purchase.aspose.com/buy).

### D3: È necessaria una licenza temporanea per la prova gratuita?
R3: No, non è necessaria una licenza temporanea per la prova gratuita. Puoi iniziare subito con la versione di prova [qui](https://releases.aspose.com/).

### D4: Dove posso trovare supporto aggiuntivo o fare domande?
R4: Visita il forum Aspose.CAD [qui](https://forum.aspose.com/c/cad/19) per qualsiasi supporto o domanda.

### D5: È disponibile una documentazione completa?
R5: Sì, la documentazione è disponibile [qui](https://reference.aspose.com/cad/java/).

## Conclusione

In questa guida abbiamo dimostrato come **convertire STL in PNG** in modo efficiente usando Aspose.CAD per Java. Seguendo i passaggi sopra, puoi integrare la conversione STL‑to‑PNG in qualsiasi pipeline basata su Java, sia che tu stia creando un'utilità desktop, un servizio web o uno strumento di reporting automatizzato.

---

**Ultimo aggiornamento:** 2026-02-20  
**Testato con:** Aspose.CAD per Java 24.12 (ultima versione al momento della stesura)  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}