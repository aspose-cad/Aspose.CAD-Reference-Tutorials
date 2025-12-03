---
date: 2025-12-03
description: Scopri come impostare le dimensioni della pagina PDF durante la conversione
  da DWG a PDF e abilitare il tracciamento nei file DWG usando Aspose.CAD per Java
  – una guida completa per esportare i disegni CAD in PDF con precisione.
language: it
linktitle: Set PDF Page Size and Enable Tracking in DWG Files Using Java
second_title: Aspose.CAD Java API
title: Imposta la dimensione della pagina PDF e abilita il tracciamento nei file DWG
  usando Aspose.CAD in Java
url: /java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Impostare le dimensioni della pagina PDF e abilitare il tracciamento nei file DWG con Aspose.CAD in Java

## Introduzione

Se devi **impostare le dimensioni della pagina PDF** quando *converti DWG in PDF* e vuoi anche tenere traccia di eventuali problemi di rendering, Aspose.CAD per Java ti offre un modo pulito e programmatico per fare entrambe le cose. In questo tutorial vedremo passo passo come configurare le dimensioni della pagina, abilitare il tracciamento e esportare un disegno CAD in PDF—tutto da Java. Alla fine comprenderai perché impostare correttamente le dimensioni della pagina è importante per i disegni CAD e come catturare informazioni dettagliate di tracciamento durante il processo di esportazione.

## Risposte rapide
- **Cosa influenza “impostare le dimensioni della pagina PDF”?** Definisce la larghezza e l’altezza della tela PDF risultante, garantendo che il tuo disegno si adatti perfettamente.  
- **È necessaria una licenza per usare questa funzionalità?** Una versione di prova è sufficiente per i test; per la produzione è richiesta una licenza commerciale.  
- **Quale versione di Aspose.CAD è necessaria?** Qualsiasi versione recente che supporti `CadRasterizationOptions`.  
- **Posso usarla con altri formati CAD?** L’esempio mostra DWG/DXF, ma lo stesso approccio funziona per la maggior parte dei formati supportati.  
- **Quanto tempo richiede la conversione?** Tipicamente meno di un secondo per file di dimensioni modeste; disegni più grandi possono richiedere più tempo.

## Cos’è “impostare le dimensioni della pagina PDF” nel contesto dell’esportazione CAD?
Impostare le dimensioni della pagina PDF indica al renderer le dimensioni esatte (in pixel o punti) della tela di output. Questo è particolarmente importante per i disegni tecnici, dove scala e layout devono essere preservati. Senza impostazioni esplicite della dimensione della pagina, il PDF potrebbe assumere una dimensione predefinita che taglia o distorce il disegno.

## Perché impostare le dimensioni della pagina PDF quando si esportano disegni CAD?
- **Preservare la scala** – Gli ingegneri si affidano a stampe a scala reale.  
- **Adattare al foglio** – Scegli A4, Letter o una dimensione personalizzata che corrisponda alle specifiche del progetto.  
- **Migliorare la leggibilità** – Pagine più grandi possono mostrare dettagli fini senza dover fare zoom.  
- **Output coerente** – Le pipeline automatizzate producono PDF con dimensioni identiche ad ogni esecuzione.

## Come impostare le dimensioni della pagina PDF quando si converte DWG in PDF?
Di seguito configureremo `CadRasterizationOptions` con valori personalizzati di larghezza e altezza prima dell’esportazione. Questo passaggio risponde direttamente alla keyword principale **impostare le dimensioni della pagina PDF**.

## Prerequisiti

- **Java Development Kit (JDK)** – Java 8 o superiore installato sulla tua macchina.  
- **Aspose.CAD per Java** – Scaricalo dalla pagina ufficiale di [download di Aspose CAD](https://releases.aspose.com/cad/java/).  
- **Directory dei documenti** – Una cartella che contiene i file DWG/DXF da elaborare.

## Importare gli spazi dei nomi

Per prima cosa, importa le classi necessarie. Il blocco di codice rimane invariato rispetto al tutorial originale.

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

## Passo 1: Caricare il file DWG/DXF

Carica il disegno sorgente. Modifica il percorso per puntare al tuo file.

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## Passo 2: Configurare le opzioni di esportazione PDF (inclusa la dimensione della pagina)

Qui impostiamo la larghezza e l’altezza della pagina—questo è il punto in cui **impostiamo le dimensioni della pagina PDF**. I valori sono in pixel; puoi convertirli da pollici o millimetri secondo necessità.

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);   // <-- custom width
cadRasterizationOptions.setPageHeight(600);  // <-- custom height
```

> **Suggerimento:** Se preferisci le dimensioni standard di carta, usa la conversione `1 pollice = 72 punti`. Per una pagina A4 (8,27 × 11,69 pollici), imposta `pageWidth = 595` e `pageHeight = 842`.

## Passo 3: Implementare il tracciamento

Il tracciamento cattura eventuali problemi di rendering. Colleghiamo un gestore personalizzato che verrà invocato dopo l’esportazione.

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## Passo 4: Esportare in PDF

Ora esegui la conversione. Il PDF verrà creato con le dimensioni specificate e le informazioni di tracciamento saranno stampate sulla console.

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## Passo 5: Classe CadRenderHandler

Il gestore stampa tutti i fallimenti verificatisi durante il rendering. Questo ti aiuta a fare debug quando **esporti un PDF di disegno CAD**.

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

## Problemi comuni e soluzioni

| Problema | Causa | Soluzione |
|----------|-------|-----------|
| **PDF vuoto** | Dimensione della pagina impostata a 0 o troppo piccola | Verifica che `setPageWidth` e `setPageHeight` siano valori positivi. |
| **Geometria mancante** | Errori diurati dal gestore | Controlla l’output della console da `ErrorHandler` e affronta il `RenderCode` specifico. |
| **File non trovato** | Percorso `dataDir` errato | Usa un percorso assoluto o assicurati che la directory esista. |
| **Eccezione di licenza** | Uso della versione di prova senza licenza valida per file grandi | Applica la licenza Aspose.CAD prima di caricare l’immagine. |

## Domande frequenti

**D: Posso abilitare il tracciamento per altri formati di file CAD usando Aspose.CAD per Java?**  
R: Aspose.CAD supporta principalmente DWG/DXF per il tracciamento. Per altri formati, consulta la documentazione ufficiale.

**D: Come posso gestire opzioni di esportazione aggiuntive in Aspose.CAD per Java?**  
R: La libreria offre molte opzioni come DPI, colore di sfondo e rasterizzazione vettoriale. Vedi la [Documentazione Java di Aspose.CAD](https://reference.aspose.com/cad/java/) per i dettagli.

**D: È disponibile una versione di prova per Aspose.CAD per Java?**  
R: Sì, puoi scaricare una prova gratuita dalla pagina di [Prova gratuita di Aspose.CAD](https://releases.aspose.com/).

**D: Dove posso chiedere assistenza o discutere problemi relativi ad Aspose.CAD per Java?**  
R: Visita il [forum di Aspose.CAD](https://forum.aspose.com/c/cad/19) per supporto della community e risposte ufficiali.

**D: Come ottengo una licenza temporanea per Aspose.CAD per Java?**  
R: Segui i passaggi descritti nella pagina di [Licenza temporanea](https://purchase.aspose.com/temporary-license/).

---

**Ultimo aggiornamento:** 2025-12-03  
**Testato con:** Aspose.CAD per Java 24.11 (ultima versione al momento della scrittura)  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}