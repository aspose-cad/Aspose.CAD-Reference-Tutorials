---
date: 2026-01-12
description: Scopri come aggiungere un'immagine ai file DWG utilizzando Aspose.CAD
  per Java e anche convertire i DWG in PDF. Segui la nostra guida passo passo per
  uno sviluppo efficiente.
linktitle: Import Image to DWG File Using Java
second_title: Aspose.CAD Java API
title: Aggiungi immagine ai file DWG senza sforzo usando Aspose.CAD Java
url: /it/java/dwg-file-operations/import-image-to-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aggiungi Immagine ai File DWG Facilmente con Aspose.CAD Java

Nelle moderne applicazioni Java, **l'aggiunta di un'immagine a file DWG** è una necessità comune—che tu stia costruendo un visualizzatore CAD, automatizzando aggiornamenti di disegni o generando documentazione. Aspose.CAD per Java ti offre un modo semplice e ad alte prestazioni per incorporare immagini raster direttamente nei disegni DWG senza la necessità di un motore CAD completo. In questo tutorial ti guideremo attraverso l'intero processo, dal caricamento di un DWG all'esportazione del risultato come PDF.

## Risposte Rapide
- **Quale libreria è necessaria?** Aspose.CAD per Java  
- **Posso anche esportare in PDF?** Sì – usa `PdfOptions` con `CadRasterizationOptions`  
- **È necessaria una licenza per lo sviluppo?** Una prova gratuita è sufficiente per i test; è richiesta una licenza commerciale per la produzione  
- **Quale versione di Java è supportata?** Java 8 e successive  
- **Quanto tempo richiede l'implementazione?** Circa 10‑15 minuti per un'importazione di immagine di base

## Che cosa significa “add image to dwg”?
Aggiungere un'immagine a un file DWG significa inserire un'immagine raster (PNG, JPEG, ecc.) come oggetto `CadRasterImage` nello spazio modello del disegno. L'immagine diventa parte dell'albero delle entità CAD e può essere posizionata, scalata e ritagliata proprio come qualsiasi altro oggetto CAD.

## Perché usare Aspose.CAD per Java per aggiungere immagine a dwg?
- **Nessun software CAD richiesto** – l'API gestisce internamente il parsing del DWG.  
- **Controllo fine** sul punto di inserimento, sui vettori di scala e sul ritaglio.  
- **Conversione PDF integrata** così puoi generare un PDF stampabile nello stesso flusso di lavoro.  
- **Cross‑platform** – funziona su Windows, Linux e macOS.

## Prerequisiti
- Aspose.CAD per Java: assicurati di avere la libreria Aspose.CAD installata. Puoi scaricarla [qui](https://releases.aspose.com/cad/java/).  
- Ambiente di sviluppo Java: JDK 8+ con il tuo IDE preferito (IntelliJ, Eclipse, VS Code, ecc.).

## Import Packages
```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.*;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Guida Passo‑Passo

### Passo 1: Carica il File DWG
Per prima cosa, indica la cartella che contiene il tuo disegno DWG e caricalo con `Image.load`.
```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Drawing11.dwg";
Image image = Image.load(srcFile);
```

### Passo 2: Definisci la Definizione dell'Immagine Raster
Crea un `CadRasterImageDef` che faccia riferimento al PNG esterno che desideri incorporare. Il costruttore richiede il nome del file immagine e le sue dimensioni in pixel.
```java
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.setObjectHandle("A3B4");
```

### Passo 3: Imposta il Punto di Inserimento e i Vettori di Scala
Il punto di inserimento determina dove apparirà l'angolo inferiore sinistro dell'immagine. I vettori **U** e **V** controllano la scala orizzontale e verticale.
```java
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

### Passo 4: Crea l'Oggetto CadRasterImage
Combina la definizione, il punto di inserimento e i vettori in un `CadRasterImage`. Puoi anche impostare i limiti di ritaglio se desideri che sia visibile solo una parte dell'immagine.
```java
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.setImageDefReference("A3B4");
cadRasterImage.setDisplayFlags((short)7);
cadRasterImage.setClippingState((short)0);
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(639.5, 561.5));
```

### Passo 5: Aggiungi l'Immagine allo Spazio Modello
Inserisci l'immagine raster nel blocco `*Model_Space`, quindi aggiorna la collezione di oggetti del disegno in modo che la definizione venga salvata.
```java
CadImage cadImage = ((CadImage)(image));
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(cadRasterImage);
CadBaseObject[] objs = cadImage.getObjects();
CadBaseObject[] arr = new CadBaseObject[objs.length + 1];
int ind = 0;
for (CadBaseObject obj : objs)
{
    arr[ind] = obj;
    ind++;
}
arr[ind] = cadRasterImageDef;
cadImage.setObjects(arr);
```

### Passo 6: Configura le Opzioni di Esportazione PDF (Facoltativo)
Se ti serve anche una versione PDF del disegno, configura `PdfOptions` insieme a `CadRasterizationOptions`. Questo passo dimostra come **convertire dwg in pdf** nello stesso flusso.
```java
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

### Passo 7: Salva il PDF Resultante
Infine, esporta il disegno modificato come file PDF. La stessa istanza `image` viene utilizzata, quindi il PDF riflette l'immagine raster appena aggiunta.
```java
image.save((srcFile + "_generated.pdf"), pdfOptions);
```

Seguendo questi passaggi, puoi **aggiungere immagine a dwg** rapidamente e anche **salvare dwg come pdf** se necessario.

## Problemi Comuni e Soluzioni
- **L'immagine non appare** – Verifica che il percorso del file immagine (`road-sign-custom.png`) sia corretto e che le dimensioni dell'immagine corrispondano ai valori passati a `CadRasterImageDef`.  
- **Scala errata** – Regola i vettori U e V; rappresentano le unità di disegno per pixel.  
- **Il PDF è vuoto** – Assicurati che `CadRasterizationOptions.setDrawType` sia impostato su `UseObjectColor` o su un'altra modalità appropriata.

## Domande Frequenti

**D: Aspose.CAD per Java è compatibile con tutti gli ambienti di sviluppo Java?**  
R: Sì, Aspose.CAD per Java è compatibile con la maggior parte degli ambienti di sviluppo Java.

**D: Posso usare Aspose.CAD per Java per progetti commerciali?**  
R: Sì, puoi usare Aspose.CAD per Java per progetti commerciali. Visita [qui](https://purchase.aspose.com/buy) per i dettagli sulla licenza.

**D: È disponibile una prova gratuita di Aspose.CAD per Java?**  
R: Sì, puoi accedere alla prova gratuita [qui](https://releases.aspose.com/).

**D: Come posso ottenere supporto per Aspose.CAD per Java?**  
R: Puoi richiedere supporto sul [forum Aspose.CAD](https://forum.aspose.com/c/cad/19).

**D: È possibile ottenere una licenza temporanea per Aspose.CAD per Java?**  
R: Sì, puoi ottenere una licenza temporanea [qui](https://purchase.aspose.com/temporary-license/).

---

**Ultimo Aggiornamento:** 2026-01-12  
**Testato Con:** Aspose.CAD per Java 24.11  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}