---
date: 2025-12-21
description: Scopri come convertire DWG in PDF esportando un layout DWG specifico
  in PDF utilizzando Aspose.CAD per Java. Segui questo tutorial passo‑passo da DWG
  a PDF per ottimizzare il tuo flusso di lavoro CAD.
linktitle: Export Specific DWG Layout to PDF
second_title: Aspose.CAD Java API
title: Converti DWG in PDF – Esporta layout con Aspose.CAD per Java
url: /it/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Converti DWG in PDF – Esporta Layout Specifico Utilizzando Aspose.CAD per Java

## Introduzione

Nel mondo dinamico del Computer‑Aided Design (CAD), **convertire DWG in PDF** è una necessità frequente quando si condividono disegni con clienti, appaltatori o stakeholder non tecnici. Aspose.CAD per Java rende questa conversione indolore e consente persino di scegliere un singolo layout da un file DWG con più layout. In questo tutorial vedremo **come esportare layout specifici di DWG** in PDF, così da fornire esattamente ciò che il tuo progetto richiede senza pagine extra o ritagli manuali.

## Risposte Rapide
- **Cosa significa “convertire DWG in PDF”?** Trasforma un disegno DWG in un documento PDF, preservando i dati vettoriali e la fedeltà del layout.  
- **Quale libreria gestisce la conversione?** Aspose.CAD per Java fornisce un'API pronta all'uso.  
- **È necessaria una licenza per la produzione?** Sì, è richiesta una licenza commerciale; una versione di prova gratuita è sufficiente per la valutazione.  
- **Posso scegliere un singolo layout?** Assolutamente – imposta la proprietà `Layouts` sul nome del layout desiderato.  
- **Quale versione di Java è supportata?** Java 8 e successive sono pienamente compatibili.

## Prerequisiti

Prima di iniziare, assicurati di avere:

- **Ambiente di sviluppo Java** – JDK 8+ e il tuo IDE preferito.  
- **Libreria Aspose.CAD** – Scarica l'ultimo JAR dal sito ufficiale **[qui](https://releases.aspose.com/cad/java/)**.  
- **File DWG** – Un disegno che contenga almeno un layout (ad es., *visualization_-_conference_room.dwg*).  

## Perché esportare un layout DWG specifico in PDF?

Molti file DWG contengono più spazi carta (layout). Esportare l'intero file può generare un PDF ingombrante con pagine indesiderate. Selezionare un singolo layout:

- Riduce le dimensioni del file.  
- Focalizza l'attenzione dell'utente sul foglio di disegno rilevante.  
- È conforme agli standard di documentazione del progetto.  

## Guida passo‑passo

### Passo 1: Configura l'ambiente del progetto

Crea un nuovo progetto Java (Maven, Gradle o IDE semplice) e aggiungi il JAR di Aspose.CAD al classpath. Puoi scaricarlo **[qui](https://releases.aspose.com/cad/java/)**.

### Passo 2: Importa i package necessari

Aggiungi i namespace Aspose.CAD richiesti alla tua classe Java.

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

### Passo 3: Carica il file DWG

Indica il percorso del DWG da convertire e caricalo in un oggetto `Image`.

```java
String srcFile = dataDir + "visualization_-_conference_room.dwg";
Image image = Image.load(srcFile);
```

### Passo 4: Configura le opzioni di rasterizzazione

Definisci le dimensioni della pagina e, soprattutto, il layout che desideri esportare.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
// Specify desired layout name
rasterizationOptions.setLayouts(new String[] {"Layout1"});
```

### Passo 5: Imposta le opzioni di esportazione PDF

Collega le impostazioni di rasterizzazione all'esportatore PDF.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Passo 6: Esporta DWG in PDF

Salva il risultato come file PDF. L'output conterrà solo **Layout1**, realizzando un'operazione pulita di **convertire DWG in PDF**.

```java
image.save(dataDir + "ExportSpecificLayoutToPDF_out_.pdf", pdfOptions);
```

## Problemi comuni e soluzioni

| Problema | Perché accade | Soluzione |
|----------|----------------|-----------|
| **Layout non trovato** | Il nome del layout è scritto in modo errato o non esiste nel DWG. | Usa `image.getLayoutNames()` per elencare i layout disponibili, quindi scegli quello corretto. |
| **PDF a bassa risoluzione** | `PageWidth`/`PageHeight` sono troppo piccoli. | Aumenta le dimensioni (ad es., 2000 × 2000) o imposta `rasterizationOptions.setResolution(300);`. |
| **Eccezione di licenza** | Esecuzione senza licenza valida in un ambiente non di prova. | Applica la licenza Aspose.CAD prima di caricare l'immagine: `License license = new License(); license.setLicense("Aspose.CAD.lic");`. |

## Domande frequenti

**D1: Posso usare Aspose.CAD per Java insieme ad altre librerie CAD basate su Java?**  
R: Aspose.CAD per Java è una libreria autonoma, ma può essere integrata con altre librerie Java per funzionalità estese.

**D2: Esistono opzioni di licenza per Aspose.CAD?**  
R: Sì, puoi esplorare le opzioni di licenza e i dettagli di acquisto **[qui](https://purchase.aspose.com/buy)**.

**D3: Come posso ottenere una licenza temporanea per Aspose.CAD?**  
R: Visita **[questo link](https://purchase.aspose.com/temporary-license/)** per richiedere una licenza temporanea.

**D4: Dove posso trovare supporto per Aspose.CAD?**  
R: Per qualsiasi domanda o assistenza, visita il **[forum Aspose.CAD](https://forum.aspose.com/c/cad/19)**.

**D5: È disponibile una versione di prova gratuita per Aspose.CAD?**  
R: Sì, puoi accedere a una prova gratuita **[qui](https://releases.aspose.com/)**.

## Conclusione

Seguendo questo **tutorial dwg to pdf**, ora disponi di un metodo affidabile per **convertire DWG in PDF** puntando a un singolo layout. Questo approccio riduce lo spazio di archiviazione, velocizza la condivisione dei documenti e mantiene ordinato il tuo flusso di lavoro CAD. Sentiti libero di sperimentare con diverse impostazioni di rasterizzazione o di combinare più layout in un unico PDF man mano che il progetto evolve.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Ultimo aggiornamento:** 2025-12-21  
**Testato con:** Aspose.CAD per Java 24.12  
**Autore:** Aspose