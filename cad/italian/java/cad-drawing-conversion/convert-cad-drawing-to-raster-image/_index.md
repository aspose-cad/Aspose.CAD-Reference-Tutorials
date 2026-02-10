---
date: 2025-12-19
description: Scopri come salvare i file CAD in PNG usando Aspose.CAD per Java, convertendo
  DWG, DXF e altri file CAD in immagini raster in modo efficiente.
linktitle: Convert CAD Drawing to Raster Image Format
second_title: Aspose.CAD Java API
title: Salva CAD come PNG – Converti disegno CAD in formato immagine raster usando
  Aspose.CAD per Java
url: /it/java/cad-drawing-conversion/convert-cad-drawing-to-raster-image/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Salva CAD come PNG – Converti il disegno CAD in formato immagine raster utilizzando Aspose.CAD per Java

## Introduzione

In questo tutorial, imparerai come **salvare CAD come PNG** usando Aspose.CAD per Java. Convertire i disegni CAD in formati immagine raster come PNG è una necessità frequente per anteprime web, documentazione e report. Aspose.CAD fornisce un modo affidabile e ad alte prestazioni per eseguire una **conversione da CAD a PNG** per DWG, DXF, DWF e molti altri tipi di file CAD.

## Risposte rapide
- **Quale libreria gestisce la conversione?** Aspose.CAD per Java.  
- **Posso convertire DWG in PNG?** Sì – la stessa API funziona per DWG, DXF e altri formati.  
- **È necessaria una licenza per la produzione?** È richiesta una licenza commerciale per l'uso non‑valutativo.  
- **La dimensione del raster è configurabile?** Assolutamente – è possibile impostare larghezza, altezza e DPI tramite le opzioni di rasterizzazione.  
- **Quanto tempo richiede la conversione?** Tipicamente meno di un secondo per disegni standard; file più grandi possono richiedere più tempo.

## Cos’è “salva CAD come PNG”?
Salvare CAD come PNG significa rasterizzare i dati CAD basati su vettori in un’immagine basata su pixel (PNG). Questo processo, spesso indicato come **converti CAD in raster**, preserva la fedeltà visiva creando al contempo un formato facile da incorporare in pagine web, email o report.

## Perché usare Aspose.CAD per Java?
- **Ampioo di formati** – funziona con DWG, DXF, DWF e molti altri.  
- **Nessuna dipendenza esterna** – puro Java, senza DLL native.  
- **Controllo dettagliato** – personalizza risoluzione, colore di sfondo e qualità di rendering.  
- **Prestazioni scalabili** – adatto per elaborazione batch o conversione on‑the‑fly.

## Prerequisiti

Prima di immergerti nel tutorial, assicurati di avere i seguenti prerequisiti:

1. **Ambiente di sviluppo Java**: verifica di avere un ambiente di sviluppo Java funzionante configurato sulla tua macchina.  
2. **Libreria Aspose.CAD**: scarica e integra la libreria Aspose.CAD per Java nel tuo progetto. Puoi trovare la libreria [qui](https://releases.aspose.com/cad/java/).

## Importare gli spazi dei nomi

Nel tuo codice Java, importa gli spazi dei nomi necessari per utilizzare efficacemente le funzionalità di Aspose.CAD per Java. Questo passaggio è fondamentale per accedere alle classi e ai metodi richiesti.

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Ora, analizziamo il processo di conversione di un disegno CAD in un’immagine raster passo dopo passo:

## Passo 1: Caricare il disegno CAD

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

In questo passaggio, carichiamo il disegno CAD dal percorso file specificato usando il metodo `Image.load()`.

## Passo 2: Impostare le opzioni di rasterizzazione

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
```

Crea un'istanza di `CadRasterizationOptions` e imposta la larghezza e l'altezza della pagina per l'immagine rasterizzata.

## Passo 3: Creare le opzioni immagine

```java
ImageOptionsBase options = new PngOptions();
options.setVectorRasterizationOptions(rasterizationOptions);
```

Crea un'istanza di `PngOptions` per l'immagine risultante e imposta le opzioni di rasterizzazione vettoriale.

## Passo 4: Salvare l’immagine raster

```java
image.save(dataDir + "conic_pyramid_raster_image_out.png", options);
```

Salva l’immagine raster risultante nella directory specificata usando il metodo `image.save()`.

Ripeti questi passaggi per i tuoi file CAD specifici e avrai **convertito con successo l’immagine del disegno CAD** in PNG.

## Casi d’uso comuni e suggerimenti

- **Generazione di anteprime web** – Converti file DWG di grandi dimensioni in miniature PNG leggere per una rapida visualizzazione nel browser.  
- **Incorporamento nei report** – Usa l'output PNG in report PDF o Word dove i file CAD vettoriali non sono supportati.  
- **Conversione batch** – Scorri una cartella di file CAD e applica le stesse impostazioni di rasterizzazione per un output coerente.  
- **Suggerimento professionale:** Regola `rasterizationOptions.setResolution()` per aumentare i DPI per stampe ad alta risoluzione.

## Conclusione

In conclusione, convertire i disegni CAD in immagini raster usando Aspose.CAD per Java è un processo semplice. Seguendo i passaggi descritti in questo tutorial, potrai integrare efficacemente questa funzionalità nelle tue applicazioni Java e eseguire **converti DWG in PNG**, **esporta CAD come PNG**, o qualsiasi altra **conversione da CAD a PNG** di cui hai bisogno.

## Domande frequenti

**D: Come converto un file DWG in PNG con un colore di sfondo personalizzato?**  
R: Imposta la proprietà `backgroundColor` su `CadRasterizationOptions` prima di creare l'istanza `PngOptions`.

**D: È possibile convertire più file CAD in un'unica operazione batch?**  
R: Sì—racchiudi i passaggi di caricamento, rasterizzazione e salvataggio all'interno di un ciclo che itera sulla tua collezione di file.

**D: Quale qualità dell'immagine posso aspettarmi dalle impostazioni predefinite?**  
R: I DPI predefiniti (96) producono PNG di qualità per schermo; aumenta i DPI per risultati di qualità di stampa.

**D: Aspose.CAD supporta sfondi trasparenti nell'output PNG?**  
R: Assolutamente. Per impostazione predefinita, i PNG vengono salvati con un canale alfa; è possibile specificare anche uno sfondo trasparente nelle opzioni di rasterizzazione.

**D: Posso convertire file CAD in altri formati raster come JPEG o BMP?**  
R: Sì—sostituisci `PngOptions` con `JpegOptions` o `BmpOptions` mantenendo le stesse impostazioni di rasterizzazione.

---

**Ultimo aggiornamento:** 2025-12-19  
**Testato con:** Aspose.CAD per Java 24.12 (latest)  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}