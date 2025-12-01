---
date: 2025-12-01
description: Scopri come impostare la dimensione della pagina PDF, convertire DWG
  in PDF e abilitare il tracciamento delle modifiche DWG usando Aspose.CAD per Java.
language: it
linktitle: Set PDF Page Size and Track DWG with Java
second_title: Aspose.CAD Java API
title: Imposta la dimensione della pagina PDF e traccia DWG con Aspose.CAD Java
url: /java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Imposta la dimensione della pagina PDF e traccia DWG con Aspose.CAD Java

## Introduzione

Quando si collabora a progetti CAD, è spesso necessario **impostare la dimensione della pagina PDF** per ottenere un layout coerente, **convertire DWG in PDF** e tenere traccia di ogni modifica apportata al disegno. Aspose.CAD per Java rende tutto questo possibile in un unico flusso di lavoro semplificato. In questo tutorial vedremo i passaggi esatti per **impostare la dimensione della pagina PDF**, abilitare il **tracciamento delle modifiche DWG** e esportare il disegno come PDF—tutto utilizzando Java.

## Risposte rapide
- **Come imposto la dimensione della pagina PDF?** Utilizza `CadRasterizationOptions.setPageWidth()` e `setPageHeight()` prima di esportare.  
- **Posso tracciare le modifiche durante l'esportazione?** Sì – implementa un `CadRenderHandler` personalizzato per catturare i risultati del tracciamento.  
- **Quale metodo converte DWG in PDF?** Chiama `image.save(stream, pdfOptions)` dopo aver configurato lezioni.  
- **Quali sono i prerequisiti principali?** JDK, Aspose.CAD per Java e una cartella con file DWG/DXF.  
- **È necessaria una licenza per la produzione?** Sì, è necessaria una licenza valida di Aspose.CAD per le distribuzioni non‑trial.

## Cos'è “impostare la dimensione della pagina PDF” nel contesto dell'esportazione DWG?

Impostare la dimensione della pagina PDF determina le dimensioni della tela PDF risultante (larghezza × altezza in pixel). Questo è essenziale quando si desidera che il disegno esportato si adatti a una dimensione di carta specifica o a un layout dello schermo, garantendo che tutti gli elementi appaiano esattamente dove ci si aspetta.

## Perché abilitare il tracciamento durante l'esportazione di file DWG?

Il tracciamento (o change‑tracking) registra eventuali problemi di rendering, font mancanti o entità non supportate che si verificano durante la conversione. Catturando queste informazioni è possibile:

- Identificare rapidamente i problemi da risolvere prima della consegna finale.  
- Fornire feedback chiaro ai membri del team su ciò che è stato modificato o omesso.  
- Mantenere una traccia di audit per settori con requisiti di conformità stringenti.

## Prerequisiti

- **Java Development Kit (JDK)** – qualsiasi versione recente (8+).  
- **Aspose.CAD per Java** – scarica dalla pagina ufficiale [Aspose CAD download page](https://releases.aspose.com/cad/java/).  
- **Document Directory** – una cartella che contiene i file DWG/DXF da elaborare.

## Importa spazi dei nomi

Inizia importando le classi Aspose.CAD necessarie e le classi standard Java I/O.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.CadRenderResult;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.RenderResult;
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
```

## Passo 1: Carica il file DWG (o DXF)

Carica il tuo disegno sorgente in un oggetto `Image`. Regola il percorso per puntare alla tua directory.

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## Passo 2: Configura le opzioni di esportazione PDF (inclusa la dimensione della pagina)

Qui impostiamo le opzioni PDF e **impostiamo esplicitamente la dimensione della pagina PDF** a 800 × 600 pixel. È qui che viene applicata la parola chiave principale.

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);   // set PDF page width
cadRasterizationOptions.setPageHeight(600);  // set PDF page height
```

## Passo 3: Implementa il tracciamento

Crea un gestore di errori personalizzato che riceverà le informazioni di tracciamento durante il processo di conversione.

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## Passo 4: Esporta in PDF

Con le opzioni e il gestore di tracciamento configurati, esporta il disegno. Questo passaggio **converte DWG in PDF** (o DXF in PDF nel nostro esempio).

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## Passo 5: Classe CadRenderHandler – Cattura i risultati del tracciamento

La classe `ErrorHandler` estende `CadRenderHandler` e stampa eventuali problemi di rendering verificatisi durante il **tracciamento delle modifiche DWG**.

```java
public static class ErrorHandler extends CadRasterizationOptions.CadRenderHandler {
    @Override
    public void invoke(CadRenderResult result) {
        System.out.println("Tracking results of exporting");

        if (result.isRenderComplete())
            return;

        System.out.println("Have some problems:");

        int idxError = 1;
        for (RenderResult rr : result.getFailures()) {
            System.out.printf("{0}. {1}, {2}", idxError, rr.getRenderCode(), rr.getMessage());
            idxError++;
        }
    }
}
```

## Problemi comuni e come risolverli

| Problema | Perché succede | Soluzione |
|----------|----------------|-----------|
| **Font mancanti** | Il file CAD fa riferimento a font non installati sul server. | Installa i font richiesti o incorporali nel disegno sorgente. |
| **Entità non supportate** | Alcune entità DWG non sono ancora supportate da Aspose.CAD. | Usa l'output del tracciamento per identificarle e semplificare il disegno. |
| **Dimensione pagina errata** | `setPageWidth/Height` non è stato chiamato prima dell'esportazione. | Assicurati che la dimensione della pagina sia impostata in `CadRasterizationOptions` come mostrato sopra. |

## Domande frequenti

### Q1: Posso abilitare il tracciamento per altri formati di file CAD usando Aspose.CAD per Java?

A1: Aspose.CAD supporta principalmente il tracciamento per file DWG/DXF. Per altri formati, consulta la documentazione ufficiale per vedere quali funzionalità sono disponibili.

### Q2: Come posso gestire opzioni di esportazione aggiuntive in Aspose.CAD per Java?

A2: La libreria offre molte opzioni come DPI, colore di sfondo e rasterizzazione vettoriale. Esplorale nella [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/).

### Q3: È disponibile una versione di prova per Aspose.CAD per Java?

A3: Sì, puoi scaricare una prova gratuita dalla [Aspose.CAD Free Trial](https://releases.aspose.com/).

### Q4: Dove posso cercare assistenza o discutere problemi relativi ad Aspose.CAD per Java?

A4: Il forum della community al [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) è un ottimo posto per fare domande e condividere esperienze.

### Q5: Come posso ottenere una licenza temporanea per Aspose.CAD per Java?

A5: Segui i passaggi descritti nella pagina [Temporary License](https://purchase.aspose.com/temporary-license/) per richiedere una licenza a tempo limitato per la valutazione.

### Q6: Posso **convertire DWG in PDF** mantenendo i layer?

A6: Sì. Configurando `CadRasterizationOptions` è possibile preservare le informazioni dei layer nel PDF risultante.

### Q7: Qual è il modo migliore per **esportare DWG come PDF** con dimensioni di pagina personalizzate?

A7: Imposta la larghezza e l'altezza desiderate usando `setPageWidth` e `setPageHeight` prima di chiamare `image.save()` – esattamente come dimostrato nel Passo 2.

## Conclusione

Seguendo i passaggi sopra potrai **impostare la dimensione della pagina PDF**, **convertire DWG in PDF** e **tracciare le modifiche nei file DWG** usando Aspose.CAD per Java. Questo flusso di lavoro ti dà il pieno controllo sul layout di output fornendo al contempo diagnostica preziosa che mantiene la tua collaborazione CAD fluida e priva di errori. Sentiti libero di esplorare ulteriori opzioni di rendering e integrare questo codice in pipeline di automazione più ampie.

---

**Last Updated:** 2025-12-01  
**Testato con:** Aspose.CAD per Java 24.12 (latest at time of writing)  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}