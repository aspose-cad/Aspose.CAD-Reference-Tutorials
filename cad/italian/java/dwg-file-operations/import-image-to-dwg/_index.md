---
date: 2026-05-20
description: Scopri come aggiungere un'immagine ai file DWG usando Aspose.CAD per
  Java e anche convertire DWG in PDF. Segui la nostra guida passo passo per uno sviluppo
  efficiente.
keywords:
- add image to dwg
- convert dwg to pdf
- import image into dwg
- embed raster image dwg
- dwg file operations
linktitle: Importa immagine nel file DWG usando Java
schemas:
- author: Aspose
  dateModified: '2026-05-20'
  description: Learn how to add image to DWG files using Aspose.CAD for Java and also
    convert DWG to PDF. Follow our step-by-step guide for efficient development.
  headline: Add Image to DWG Files Effortlessly Using Aspose.CAD Java
  type: TechArticle
- description: Learn how to add image to DWG files using Aspose.CAD for Java and also
    convert DWG to PDF. Follow our step-by-step guide for efficient development.
  name: Add Image to DWG Files Effortlessly Using Aspose.CAD Java
  steps:
  - name: Load the DWG File
    text: First, point to the folder that contains your DWG drawing and load it with
      `Image.load`.
  - name: Define the Raster Image Definition
    text: The `CadRasterImageDef` class defines the external raster image resource
      to be embedded in the drawing.
  - name: Set Insertion Point and Scaling Vectors
    text: The insertion point determines where the lower‑left corner of the image
      will appear. The **U** and **V** vectors control horizontal and vertical scaling.
  - name: Create the CadRasterImage Object
    text: The `CadRasterImage` entity represents a raster picture placed in the DWG
      model space.
  - name: Add the Image to Model Space
    text: Insert the raster image into the `*Model_Space` block, then update the drawing’s
      object collection so the definition is saved.
  - name: Configure PDF Export Options (Optional)
    text: '`PdfOptions` specifies settings for saving a CAD drawing as a PDF file.
      `CadRasterizationOptions` defines how the CAD content is rasterized during PDF
      conversion.'
  - name: Save the Resulting PDF
    text: 'Finally, export the modified drawing as a PDF file. The same `image` instance
      is used, so the PDF reflects the newly added raster image. By following these
      steps, you can **add image to dwg** files quickly and also **save dwg as pdf**
      when needed, covering the most common **dwg file operations** in '
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD for Java works with any IDE that supports JDK 8+, including
      IntelliJ IDEA, Eclipse, and VS Code.
    question: Is Aspose.CAD for Java compatible with all Java development environments?
  - answer: Yes, you can use Aspose.CAD for Java for commercial projects. Visit **[here](https://purchase.aspose.com/buy)**
      for licensing details.
    question: Can I use Aspose.CAD for Java for commercial projects?
  - answer: Yes, you can access the free trial **[here](https://releases.aspose.com/)**.
    question: Is there a free trial available for Aspose.CAD for Java?
  - answer: You can seek support on the **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)**.
    question: How can I get support for Aspose.CAD for Java?
  - answer: Yes, you can get a temporary license **[here](https://purchase.aspose.com/temporary-license/)**.
    question: Can I obtain a temporary license for Aspose.CAD for Java?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Aggiungi immagine ai file DWG senza sforzo con Aspose.CAD per Java
url: /it/java/dwg-file-operations/import-image-to-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aggiungi Immagine ai File DWG Facilmente Utilizzando Aspose.CAD Java

Nelle moderne applicazioni Java, **aggiungere un'immagine a DWG** è una necessità comune—che tu stia creando un visualizzatore CAD, automatizzando aggiornamenti di disegni o generando documentazione. Aspose.CAD per Java ti offre un modo semplice e ad alte prestazioni per incorporare immagini raster direttamente nei disegni DWG senza la necessità di un motore CAD completo. In questo tutorial ti guideremo attraverso l'intero processo, dal caricamento di un DWG all'esportazione del risultato come PDF, e tratteremo anche come **importare un'immagine in dwg** e **convertire dwg in pdf** in un unico flusso di lavoro.

## Risposte Rapide
- **Quale libreria è necessaria?** Aspose.CAD for Java  
- **Posso anche esportare in PDF?** Yes – use `PdfOptions` with `CadRasterizationOptions`  
- **Ho bisogno di una licenza per lo sviluppo?** A free trial works for testing; a commercial license is required for production  
- **Quale versione di Java è supportata?** Java 8 and higher  
- **Quanto tempo richiede l'implementazione?** About 10‑15 minutes for a basic image import  

## Cos'è “add image to dwg”?
Aggiungere un'immagine a un file DWG significa incorporare un'immagine raster (PNG, JPEG, ecc.) come entità **CadRasterImage** nello spazio modello del disegno, dove può essere posizionata, scalata e opzionalmente ritagliata proprio come qualsiasi altro oggetto CAD. Viene memorizzata nella tabella degli oggetti del disegno e visualizzata dai visualizzatori CAD standard.

## Perché usare Aspose.CAD per Java per aggiungere immagine a dwg?
Puoi incorporare grafica raster nei file DWG senza installare alcun software CAD di terze parti, e l'API ti offre un controllo pixel‑perfect sul punto di inserimento, sui vettori di scala e sui confini di ritaglio. Aspose.CAD elabora file fino a 2 GB di dimensione, supporta **oltre 50 formati di input e output**, e funziona su Windows, Linux e macOS, consentendoti di integrare la manipolazione CAD in qualsiasi backend basato su Java.

## Prerequisiti
- **Aspose.CAD for Java** – scarica l'ultimo JAR dal sito ufficiale **[here](https://releases.aspose.com/cad/java/)**.  
- **Java Development Kit** – JDK 8 o superiore, con il tuo IDE preferito (IntelliJ IDEA, Eclipse, VS Code, ecc.).  
- Una licenza valida **Aspose.CAD** per l'uso in produzione (la versione di prova funziona per sperimentazione).  

## Importa Pacchetti
Le seguenti importazioni includono le classi Essenziali di Aspose.CAD utilizzate per la manipolazione delle immagini e la conversione PDF.  
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
Innanzitutto, indica la cartella che contiene il tuo disegno DWG e caricalo con `Image.load`.  
```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Drawing11.dwg";
Image image = Image.load(srcFile);
```

### Passo 2: Definisci la Definizione dell'Immagine Raster
La classe `CadRasterImageDef` definisce la risorsa immagine raster esterna da incorporare nel disegno.  
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
L'entità `CadRasterImage` rappresenta un'immagine raster posizionata nello spazio modello del DWG.  
```java
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.setImageDefReference("A3B4");
cadRasterImage.setDisplayFlags((short)7);
cadRasterImage.setClippingState((short)0);
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(639.5, 561.5));
```

### Passo 5: Aggiungi l'Immagine allo Spazio Modello
Inserisci l'immagine raster nel blocco `*Model_Space`, quindi aggiorna la collezione di oggetti del disegno affinché la definizione venga salvata.  
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

### Passo 6: Configura le Opzioni di Esportazione PDF (Opzionale)
`PdfOptions` specifica le impostazioni per salvare un disegno CAD come file PDF. `CadRasterizationOptions` definisce come il contenuto CAD viene rasterizzato durante la conversione PDF.  
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
Infine, esporta il disegno modificato come file PDF. Viene utilizzata la stessa istanza `image`, quindi il PDF riflette l'immagine raster appena aggiunta.  
```java
image.save((srcFile + "_generated.pdf"), pdfOptions);
```

Seguendo questi passaggi, puoi **aggiungere immagine a dwg** rapidamente e anche **salvare dwg come pdf** quando necessario, coprendo le operazioni più comuni sui **file dwg** in un'unica routine compatta.

## Problemi Comuni e Soluzioni
- **Image not appearing** – Verifica che il percorso del file immagine (`road-sign-custom.png`) sia corretto e che le dimensioni dell'immagine corrispondano ai valori passati a `CadRasterImageDef`.  
- **Incorrect scaling** – Regola i vettori U e V; rappresentano le unità di disegno per pixel.  
- **PDF looks blank** – Assicurati che `CadRasterizationOptions.setDrawType` sia impostato su `UseObjectColor` o un altro modo appropriato.  

## Domande Frequenti

**Q: Aspose.CAD per Java è compatibile con tutti gli ambienti di sviluppo Java?**  
A: Sì, Aspose.CAD per Java funziona con qualsiasi IDE che supporti JDK 8+, inclusi IntelliJ IDEA, Eclipse e VS Code.

**Q: Posso usare Aspose.CAD per Java per progetti commerciali?**  
A: Sì, puoi usare Aspose.CAD per Java per progetti commerciali. Visita **[here](https://purchase.aspose.com/buy)** per i dettagli della licenza.

**Q: È disponibile una versione di prova gratuita per Aspose.CAD per Java?**  
A: Sì, puoi accedere alla versione di prova gratuita **[here](https://releases.aspose.com/)**.

**Q: Come posso ottenere supporto per Aspose.CAD per Java?**  
A: Puoi richiedere supporto sul **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)**.

**Q: Posso ottenere una licenza temporanea per Aspose.CAD per Java?**  
A: Sì, puoi ottenere una licenza temporanea **[here](https://purchase.aspose.com/temporary-license/)**.

---

**Ultimo Aggiornamento:** 2026-05-20  
**Testato Con:** Aspose.CAD for Java 24.11  
**Autore:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutorial Correlati

- [Esporta DWG in PDF o Raster Utilizzando Aspose.CAD per Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Aggiungi Proprietà Personalizzate ai File DWG Utilizzando Aspose.CAD per Java](/cad/java/additional-features/add-custom-properties/)
- [Salva CAD come PNG – Converti Disegno CAD in Formato Immagine Raster Utilizzando Aspose.CAD per Java](/cad/java/cad-drawing-conversion/convert-cad-drawing-to-raster-image/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}