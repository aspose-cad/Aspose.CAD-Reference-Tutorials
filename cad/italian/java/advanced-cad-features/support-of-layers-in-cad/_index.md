---
date: 2025-12-13
description: Scopri come salvare i file CAD in JPEG in Java usando Aspose.CAD, aggiungere
  più livelli e regolare le dimensioni del CAD per una conversione precisa dell'immagine.
linktitle: Support of Layers in CAD
second_title: Aspose.CAD Java API
title: Salva CAD in JPEG con supporto dei layer in Java
url: /it/java/advanced-cad-features/support-of-layers-in-cad/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Salva CAD come JPEG con supporto dei layer in Java

## Introduzione

In questo tutorial scoprirai come **salvare CAD come JPEG** sfruttando appieno il supporto dei layer in Aspose.CAD per Java. I layer ti permettono di isolare parti specifiche di un disegno, rendendo facile esportare solo ciò di cui hai bisogno. Ti guideremo passo passo, dalla configurazione dell'ambiente all'esportazione di un JPEG che includa solo i layer che scegli.

## Risposte rapide
- **Cosa significa “save CAD as JPEG”?** Converte un disegno CAD in un'immagine raster JPEG.
- **Posso includere solo i layer selezionati?** Sì – usa il metodo `setLayers` per specificare quali layer renderizzare.
- **Come faccio a cambiare le dimensioni dell'immagine?** Regola `setPageWidth` e `setPageHeight` in `CadRasterizationOptions`.
- **È una soluzione solo per Java?** L'esempio utilizza Aspose.CAD per Java, ma gli stessi concetti si applicano ad altri linguaggi.
- **Ho bisogno di una licenza?** Una prova gratuita funziona per i test; è necessaria una licenza commerciale per la produzione.

## Prerequisiti

Prima di iniziare, assicurati di avere quanto segue:

1. **Libreria Aspose.CAD per Java** – scaricala dal [sito web](https://releases.aspose.com/cad/java/). Segui la guida di installazione per aggiungere i file JAR al classpath del tuo progetto.  
2. **Ambiente di sviluppo Java** – un JDK recente (8 o superiore) installato sulla tua macchina.

Ora che siamo pronti, esploriamo il codice necessario per **salvare CAD come JPEG** con rendering selettivo dei layer.

## Importare gli spazi dei nomi

Inizia importando le classi Aspose.CAD necessarie e le utility standard di Java:

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

Definisci dove si trova il file DWF di origine e dove verrà scritto il JPEG di output.

```java
String dataDir = "Your Document Directory" + "DWFDrawings/";
String srcFile = dataDir + "for_layers_test.dwf";
String outFile = dataDir + "for_layers_test.jpg";
```

### Passo 2: Carica l'immagine DWF

Usa il metodo `Image.load` di Aspose.CAD per leggere il disegno CAD.

```java
Image image = Image.load(srcFile);
```

### Passo 3: Configura le opzioni di rasterizzazione (Regola le dimensioni CAD)

Crea un'istanza di `CadRasterizationOptions` e imposta la dimensione di output desiderata. Modificando questi valori puoi **regolare le dimensioni CAD** per il JPEG finale.

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

*Suggerimento:* Per **aggiungere più layer**, espandi la chiamata `Arrays.asList`, ad esempio `Arrays.asList("LayerA", "LayerB", "LayerC")`.

### Passo 5: Configura le opzioni JPEG (Conversione CAD in immagine Java)

Collega le impostazioni di rasterizzazione al formato di output JPEG.

```java
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Passo 6: Esporta in JPG (Salva CAD come JPEG)

Infine, scrivi l'immagine su disco. Questo passo **salva il disegno CAD come file JPEG** contenente solo i layer selezionati.

```java
image.save(outFile, jpegOptions);
```

Seguendo questi passaggi hai correttamente **salvato CAD come JPEG** controllando quali layer appaiono e personalizzando le dimensioni dell'immagine.

## Problemi comuni e soluzioni

| Problema | Soluzione |
|----------|-----------|
| **Layer non visualizzati** | Verifica che i nomi dei layer corrispondano esattamente a quelli presenti nel file DWF (case‑sensitive). |
| **L'immagine di output è vuota** | Assicurati che `setPageWidth` e `setPageHeight` siano sufficientemente grandi per le dimensioni del disegno. |
| **Eccezione di licenza** | Usa una licenza di prova per i test; ottieni una licenza completa per gli ambienti di produzione. |

## Domande frequenti

**D: Posso aggiungere più layer alle opzioni di rasterizzazione?**  
R: Assolutamente. Estendi la `stringList` con nomi di layer aggiuntivi, ad esempio `Arrays.asList("LayerA", "LayerB")`.

**D: Aspose.CAD è compatibile con altri formati CAD?**  
R: Sì, supporta DWG, DXF, DWF e molti altri formati.

**D: Come posso cambiare le dimensioni dell'immagine di output?**  
R: Modifica `setPageWidth` e `setPageHeight` nell'istanza `CadRasterizationOptions`.

**D: Dove posso acquistare una licenza per Aspose.CAD?**  
R: Puoi esplorare le opzioni di licenza [qui](https://purchase.aspose.com/buy).

**D: Dove posso ottenere supporto dalla community?**  
R: Unisciti alla community di Aspose.CAD sul [forum](https://forum.aspose.com/c/cad/19) per assistenza e discussioni.

---

**Ultimo aggiornamento:** 2025-12-13  
**Testato con:** Aspose.CAD for Java 24.11  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}