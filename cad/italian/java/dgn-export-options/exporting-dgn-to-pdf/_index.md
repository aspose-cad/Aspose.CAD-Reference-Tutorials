---
date: 2026-05-04
description: Scopri come convertire i file CAD PDF esportando DGN in PDF AutoCAD usando
  Aspose.CAD per Java. Guida passo‑passo con dimensioni PDF personalizzabili e opzioni.
keywords:
- convert cad pdf
- how to export dgn
- customize pdf size
- aspose cad download
- set pdf options
linktitle: Esportazione di DGN in formato AutoCAD in PDF
second_title: Aspose.CAD Java API
title: Converti PDF CAD – Esportazione senza sforzo da DGN a PDF AutoCAD con Aspose.CAD
  per Java
url: /it/java/dgn-export-options/exporting-dgn-to-pdf/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convertire CAD PDF: Esportazione senza sforzo da DGN a PDF AutoCAD con Aspose.CAD per Java

## Introduzione

Se hai bisogno di **convertire CAD PDF** direttamente da sorgenti DGN, sei nel posto giusto. In questo tutorial ti guideremo nell'utilizzo di Aspose.CAD per Java per esportare file DGN in un PDF compatibile con AutoCAD. Vedrai come impostare dimensioni di pagina personalizzate, scegliere layout specifici e perfezionare l'output PDF — il tutto con codice chiaro, passo dopo passo, che puoi inserire nel tuo progetto.

## Risposte rapide
- **Cosa significa “convertire CAD PDF”?** Si riferisce alla trasformazione di file sorgente CAD (come DGN) in un PDF che conserva i dati vettoriali e la fedeltà del layout.  
- **Quale libreria gestisce la conversione?** Aspose.CAD per Java offre una prova affidabile e senza licenza per questo compito.  
- **È necessaria una licenza per lo sviluppo?** Una prova gratuita è sufficiente per i test; è necessaria una licenza commerciale per l'uso in produzione.  
- **Posso personalizzare le dimensioni del PDF?** Sì – le `CadRasterizationOptions` consentono di impostare larghezza, altezza e scala della pagina.  
- **Quante righe di codice sono necessarie?** Meno di 20 righe di codice Java per caricare, configurare e salvare il PDF.

## Cos'è “convertire CAD PDF”?
Convertire CAD PDF significa prendere un disegno CAD nativo (ad esempio DGN) e produrre un PDF che conserva la grafica vettoriale originale, i livelli e le informazioni di layout. Il PDF risultante può essere visualizzato su qualsiasi dispositivo senza necessità di software CAD, rendendolo ideale per la condivisione, la stampa o l'archiviazione.

## Perché usare Aspose.CAD per Java per convertire CAD PDF?
- **Supporto completo dei formati** – DGN, DWG, DXF e molti altri.  
- **Nessuna dipendenza esterna** – puro Java, nessun DLL nativo.  
- **Controllo dettagliato** – puoi scegliere quali layout esportare, impostare dimensioni di pagina personalizzate e controllare la qualità della rasterizzazione.  
- **Scalabile per lavori batch** – carica e salva decine di file in un ciclo con un overhead minimo.

## Prerequisiti
- **Libreria Aspose.CAD** – scaricala [qui](https://releases.aspose.com/cad/java/).  
- **Directory dei documenti** – una cartella sul tuo computer dove risiederanno i file DGN di input e i PDF di output.

## Importare i pacchetti

Nel tuo progetto Java, importa i pacchetti necessari per accedere alle funzionalità di Aspose.CAD:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Ora, analizziamo il codice di esempio in più passaggi:

## Passo 1: Definire i percorsi dei file (come esportare dgn)

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

Assicurati di sostituire `"Your Document Directory"` con il percorso reale dove si trovano i tuoi file.

## Passo 2: Caricare l'immagine DGN

```java
DgnImage objImage = (DgnImage) Image.load(fileName);
```

Carica il file DGN utilizzando Aspose.CAD.

## Passo 3: Impostare le opzioni di esportazione PDF (personalizzare dimensione pdf, impostare opzioni pdf)

```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); // Export specific views
options.setVectorRasterizationOptions(vectorOptions);
```

Qui definiamo le opzioni di esportazione PDF, incluse le dimensioni della pagina, lo scaling automatico e i layout DGN specifici (viste) da includere nel PDF finale.

## Passo 4: Salvare il file PDF

```java
objImage.save(outFile, options);
```

Salva il file PDF esportato. Il metodo `save` applica tutte le opzioni configurate nel passaggio precedente.

Ripeti questi passaggi per tutti gli ulteriori file DGN che desideri convertire. Congratulazioni! Hai convertito con successo **CAD PDF** esportando file DGN nel formato AutoCAD in PDF usando Aspose.CAD per Java.

## Problemi comuni e soluzioni
| Problema | Perché accade | Soluzione |
|----------|----------------|-----------|
| **File non trovato** | Percorso `dataDir` errato | Verifica nuovamente il percorso della cartella e assicurati che il file DGN esista. |
| **Pagine vuote nel PDF** | `AutomaticLayoutsScaling` impostato su `false` o ID layout mancanti | Mantieni `setAutomaticLayoutsScaling(true)` e verifica i nomi dei layout (`"1","2",…`). |
| **Output a bassa risoluzione** | Il DPI di rasterizzazione predefinito è basso | Usa `vectorOptions.setResolution(300);` per aumentare la qualità (aggiungi prima di `setVectorRasterizationOptions`). |
| **Eccezione di licenza** | Esecuzione senza una licenza valida in produzione | Applica una licenza temporanea o acquistata come descritto nella documentazione di Aspose. |

## Domande frequenti (Aggiuntive)

**Q: Posso esportare solo un singolo layout da un file DGN multi‑layout?**  
A: Sì – specifica gli ID dei layout desiderati in `vectorOptions.setLayouts(new String[] { "2" });`.

**Q: È possibile incorporare i font nel PDF risultante?**  
A: Aspose.CAD incorpora automaticamente i font necessari quando i dati vettoriali vengono rasterizzati; è anche possibile controllare l'incorporamento dei font tramite `PdfOptions` se necessario.

**Q: Come elaborare molti file DGN in batch?**  
A: Inserisci i passaggi all'interno di un ciclo `for` che itera su un elenco di nomi file, riutilizzando la stessa istanza di `PdfOptions` per ogni iterazione.

**Q: La libreria supporta PDF protetti da password?**  
A: Sì – puoi impostare una password sull'oggetto `PdfOptions` tramite `options.setPassword("yourPassword");`.

**Q: Dove posso trovare più esempi?**  
A: La documentazione ufficiale di Aspose.CAD e il repository di esempi contengono molti scenari aggiuntivi.

## FAQ (Originale)

### Q1: Aspose.CAD è compatibile con tutti i formati di file CAD?

A1: Sì, Aspose.CAD supporta un'ampia gamma di formati CAD, garantendo versatilità nella gestione di vari tipi di file.

### Q2: Posso personalizzare le impostazioni di esportazione PDF?

A2: Assolutamente. Come mostrato nel tutorial, puoi regolare opzioni come le dimensioni della pagina e i layout per soddisfare le tue esigenze.

### Q3: Dove posso trovare supporto o assistenza aggiuntiva?

A3: Visita il [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) per supporto della community e discussioni.

### Q4: È disponibile una prova gratuita?

A4: Sì, puoi accedere alla prova gratuita [qui](https://releases.aspose.com/).

### Q5: Come posso ottenere una licenza temporanea?

A5: Ottieni una licenza temporanea [qui](https://purchase.aspose.com/temporary-license/).

## Conclusione

In questo tutorial abbiamo esplorato come **convertire CAD PDF** utilizzando Aspose.CAD per Java. Con poche righe di codice puoi caricare un disegno DGN, perfezionare le opzioni di esportazione PDF e generare PDF ad alta qualità pronti per la condivisione o l'archiviazione. Sentiti libero di sperimentare con diverse dimensioni di pagina, layout o elaborazione batch per adattarle alle esigenze del tuo progetto.

---

**Ultimo aggiornamento:** 2026-05-04  
**Testato con:** Aspose.CAD for Java 24.12  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}