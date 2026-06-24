---
date: 2026-02-17
description: Scopri come salvare DWG come JPEG in Java usando Aspose.CAD, aggiungere
  più livelli e regolare le dimensioni CAD per una conversione di immagine precisa.
linktitle: Support of Layers in CAD
second_title: Aspose.CAD Java API
title: Salva DWG come JPEG con supporto dei livelli in Java
url: /it/java/advanced-cad-features/support-of-layers-in-cad/
weight: 18
---

 shortcodes unchanged.

Now produce final content.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Salva DWG come JPEG con supporto dei layer in Java

## Introduzione

In questo tutorial scoprirai come **salvare DWG come JPEG** sfruttando appieno il supporto dei layer in Aspose.CAD per Java. I layer ti permettono di isolare parti specifiche di un disegno, facilitando l’esportazione solo di ciò di cui hai bisogno. Ti guideremo passo passo, dalla configurazione dell’ambiente all’esportazione di un JPEG che includa solo i layer selezionati.

## Risposte rapide
- **Cosa significa “salvare DWG come JPEG”?** Converte un disegno DWG (o altro CAD) in un’immagine raster JPEG.  
- **Posso includere solo i layer selezionati?** Sì – usa il metodo `setLayers` per specificare quali layer renderizzare.  
- **Come modifico le dimensioni dell’immagine?** Regola `setPageWidth` e `setPageHeight` in `CadRasterizationOptions`.  
- **È una soluzione solo per Java?** L’esempio utilizza Aspose.CAD per Java, ma gli stessi concetti valgono per altri linguaggi.  
- **È necessaria una licenza?** Una versione di prova è sufficiente per i test; è richiesta una licenza commerciale per la produzione.

## Cos’è “salvare DWG come JPEG”?
Salvare DWG come JPEG significa rasterizzare un file CAD basato su vettori (DWG, DWF, DXF, ecc.) in una bitmap JPEG standard. È utile quando devi inserire disegni CAD in pagine web, email o report che supportano solo immagini raster.

## Perché usare la conversione JPEG con consapevolezza dei layer?
- **Focalizzarsi sui dati rilevanti:** Esporta solo i layer di cui hai bisogno, riducendo la dimensione del file e l’ingombro visivo.  
- **Mantenere l’intento di progettazione:** I layer preservano il raggruppamento logico degli oggetti, così da poter riutilizzare lo stesso file sorgente per uscite diverse.  
- **Controllo totale sulle dimensioni:** Regolando le opzioni di rasterizzazione puoi produrre immagini ad alta risoluzione che corrispondono ai requisiti di pubblicazione.

## Prerequisiti

Prima di iniziare, assicurati di avere quanto segue:

1. **Aspose.CAD for Java Library** – scaricala dal [sito web](https://releases.aspose.com/cad/java/). Segui la guida di installazione per aggiungere i file JAR al classpath del tuo progetto.  
2. **Ambiente di sviluppo Java** – un JDK recente (8 o superiore) installato sulla tua macchina.

Ora che siamo pronti, esploriamo il codice necessario per **salvare DWG come JPEG** con rendering selettivo dei layer.

## Importa namespace

Inizia importando le classi Aspose.CAD richieste e le utility standard di Java:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;
```

## Guida passo‑passo

### Passo 1: Configura i percorsi dei file

Definisci dove si trova il file DWF sorgente e dove verrà scritto il JPEG di output.

```java
String dataDir = "Your Document Directory" + "DWFDrawings/";
String srcFile = dataDir + "for_layers_test.dwf";
String outFile = dataDir + "for_layers_test.jpg";
```

### Passo 2: Carica l’immagine DWF

Usa il metodo `Image.load` di Aspose.CAD per leggere il disegno CAD.

```java
Image image = Image.load(srcFile);
```

### Passo 3: Configura le opzioni di rasterizzazione (Regola le dimensioni CAD)

Crea un’istanza di `CadRasterizationOptions` e imposta la dimensione di output desiderata. Modificando questi valori puoi **regolare le dimensioni CAD** per il JPEG finale.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

### Passo 4: Specifica i layer (Aggiungi più layer)

Se desideri renderizzare più di un layer, aggiungi semplicemente i loro nomi alla lista. Qui iniziamo con un singolo layer chiamato “LayerA”.

```java
List<String> stringList = new ArrayList<>(Arrays.asList("LayerA"));
rasterizationOptions.setLayers(stringList);
```

*Consiglio professionale:* Per **aggiungere più layer**, espandi la chiamata `Arrays.asList`, ad esempio `Arrays.asList("LayerA", "LayerB", "LayerC")`. Questo ti permette di **selezionare layer CAD specifici** per la conversione.

### Passo 5: Configura le opzioni JPEG (Converti CAD in immagine JPEG)

Collega le impostazioni di rasterizzazione al formato di output JPEG.

```java
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Passo 6: Esporta in JPG (Salva DWG come JPEG)

Infine, scrivi l’immagine su disco. Questo passaggio **salva il disegno CAD come file JPEG** contenente solo i layer selezionati.

```java
image.save(outFile, jpegOptions);
```

Seguendo questi passaggi hai **salvato con successo DWG come JPEG** controllando quali layer appaiono e personalizzando le dimensioni dell’immagine.

## Come convertire DWF in JPEG con selezione dei layer

Sebbene l’esempio utilizzi una sorgente DWF, la stessa pipeline di rasterizzazione funziona per qualsiasi formato CAD supportato (DWG, DXF, DGN, ecc.). Basta cambiare l’estensione del file in `srcFile` e la libreria gestirà automaticamente l’operazione di **conversione DWF in JPEG** (o altro formato).

## Problemi comuni e soluzioni

| Problema | Soluzione |
|----------|-----------|
| **Layers non visualizzati** | Verifica che i nomi dei layer corrispondano esattamente a quelli memorizzati nel file DWF (case‑sensitive). |
| **Immagine di output vuota** | Assicurati che `setPageWidth` e `setPageHeight` siano sufficientemente grandi per le dimensioni del disegno. |
| **Eccezione di licenza** | Usa una licenza di prova per i test; ottieni una licenza completa per gli ambienti di produzione. |

## Domande frequenti

**D: Posso aggiungere più layer alle opzioni di rasterizzazione?**  
R: Assolutamente. Estendi la `stringList` con nomi di layer aggiuntivi, ad esempio `Arrays.asList("LayerA", "LayerB")`.

**D: Aspose.CAD è compatibile con altri formati CAD?**  
R: Sì, supporta DWG, DXF, DWF e molti altri formati.

**D: Come posso modificare le dimensioni dell’immagine di output?**  
R: Modifica `setPageWidth` e `setPageHeight` nell’istanza `CadRasterizationOptions`.

**D: Dove posso acquistare una licenza per Aspose.CAD?**  
R: Puoi esplorare le opzioni di licenza [qui](https://purchase.aspose.com/buy).

**D: Dove posso trovare supporto dalla community?**  
R: Unisciti alla community Aspose.CAD sul [forum](https://forum.aspose.com/c/cad/19) per assistenza e discussioni.

---

**Ultimo aggiornamento:** 2026-02-17  
**Testato con:** Aspose.CAD for Java 24.11  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}