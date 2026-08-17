---
date: 2026-02-20
description: Scopri come esportare PDF da AutoCAD usando Aspose.CAD per Java. Questa
  guida passo‑passo ti mostra come **convertire DWG in PDF**, **salvare CAD come PDF**
  e gestire la licenza.
linktitle: Export AutoCAD Images to PDF
second_title: Aspose.CAD Java API
title: Converti DWG in PDF - Esporta le immagini AutoCAD in PDF con Aspose.CAD per
  Java
url: /it/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Esporta PDF AutoCAD - Esporta Immagini AutoCAD in PDF con Aspose.CAD per Java

## Introduzione

Stai cercando di **convertire DWG in PDF** usando Java? Non cercare oltre! In questo tutorial ti guideremo nella conversione di immagini AutoCAD in PDF con Aspose.CAD per Java, una libreria potente che rende il processo di **convertire DWG in PDF** semplice. Alla fine comprenderai come **salvare CAD come PDF**, applicare impostazioni di rasterizzazione personalizzate e utilizzare una licenza Aspose.CAD per l'uso in produzione.

## Risposte Rapide
- **Posso convertire DWG in PDF con Java?** Sì, Aspose.CAD per Java gestisce DWG, DXF e molti altri formati.  
- **È necessaria una licenza?** È richiesta una **licenza Aspose CAD** per utilizzo illimitato; è disponibile una licenza temporanea per la valutazione.  
- **Quale versione di Java è supportata?** Java 8+ (la libreria è compatibile con tutti i JDK moderni).  
- **Posso personalizzare le dimensioni della pagina PDF?** Assolutamente – regola `pageWidth` e `pageHeight` nelle opzioni di rasterizzazione.  
- **È possibile la rasterizzazione 3‑D?** Sì, abilita `TypeOfEntities.Entities3D` per il rendering 3‑D completo.

## Che cos’è **export autocad pdf**?
Esportare AutoCAD PDF significa convertire disegni CAD basati su vettori (DWG, DXF, DWF, ecc.) in un documento PDF portatile mantenendo i layer, i pesi delle linee e, facoltativamente, la geometria 3‑D. Questo è utile per condividere progetti con i clienti, archiviare o stampare senza richiedere software CAD.

## Perché Convertire DWG in PDF con Aspose.CAD per Java?
- **Supporto completo dei formati** – funziona con DWG, DXF, DWF e molti altri.  
- **Nessuna dipendenza esterna** – libreria Java pura, senza DLL native.  
- **Rasterizzazione di alta qualità** – controllo su DPI, dimensioni della pagina e layout, così da poter **personalizzare le dimensioni della pagina PDF** in base alle esigenze del progetto.  
- **Flessibilità di licenza** – inizia con una prova gratuita, poi passa a una **licenza Aspose CAD** permanente.  

## Prerequisiti

Prima di iniziare, assicurati di avere:

- **Ambiente di sviluppo Java** – JDK 8 o successivo installato.  
- **Libreria Aspose.CAD per Java** – scaricala dal [download link](https://releases.aspose.com/cad/java/).  
- **Cartella dei documenti** – una cartella sul tuo computer dove risiederanno i file CAD di origine e i PDF generati.

## Importare i Namespace

Nel tuo progetto Java, importa le classi necessarie per lavorare con Aspose.CAD:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

Ora esaminiamo il codice passo‑per‑passo.

## Come convertire DWG in PDF con Aspose.CAD per Java

### Passo 1: Impostare il percorso della directory delle risorse

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **Suggerimento:** Sostituisci `"Your Document Directory"` con il percorso assoluto della cartella creata nei prerequisiti.

### Passo 2: Caricare l’immagine CAD

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **Perché è importante:** Caricare il file CAD in un oggetto `Image` ti dà pieno accesso al motore di rasterizzazione di Aspose.CAD.

### Passo 3: Impostare le opzioni di rasterizzazione

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- Regola `pageWidth` e `pageHeight` per **personalizzare le dimensioni della pagina PDF**.  
- Decommenta la riga `setTypeOfEntities` se hai bisogno di **java convert cad pdf** per entità 3‑D.  
- La chiamata `setLayouts` seleziona quale layout (Model, Layout1, ecc.) renderizzare.

### Passo 4: Configurare le opzioni PDF

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Questo collega le impostazioni di rasterizzazione all’output PDF, garantendo che i dati vettoriali vengano convertiti correttamente.

### Passo 5: Salvare il PDF

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

Il file risultante, `Export3DImagestoPDF_out_.pdf`, è una rappresentazione **save cad as pdf** del tuo disegno AutoCAD originale.

## Problemi comuni e soluzioni

| Sintomo | Causa probabile | Soluzione |
|---------|-----------------|-----------|
| PDF vuoto | Opzioni di rasterizzazione non impostate o layout non corrispondente | Verifica che `setLayouts` corrisponda al nome del layout nel tuo file CAD. |
| Immagine a bassa risoluzione | `pageWidth`/`pageHeight` troppo piccoli | Aumenta le dimensioni o imposta un DPI più alto tramite `rasterizationOptions.setResolution(...)`. |
| Eccezione di licenza | Nessuna licenza valida applicata | Applica una **licenza Aspose CAD** o usa una licenza temporanea per i test. |

## Domande Frequenti

### Q1: Posso usare Aspose.CAD per Java con altri formati di file CAD?
A1: Sì, Aspose.CAD supporta un’ampia gamma di formati tra cui DWG, DWF, DGN e molti altri, offrendoti flessibilità nei tuoi progetti.

### Q2: Come posso ottenere una licenza temporanea per Aspose.CAD per Java?
A2: Visita [qui](https://purchase.aspose.com/temporary-license/) per ottenere una licenza temporanea per la valutazione.

### Q3: Esistono opzioni di layout per la rasterizzazione?
A3: Sì, puoi personalizzare i layout (ad es., `"Model"`, `"Layout1"`) tramite il metodo `setLayouts` per controllare quale vista viene renderizzata.

### Q4: Posso personalizzare le dimensioni del file PDF di output?
A4: Assolutamente! Regola i parametri `pageWidth` e `pageHeight` nelle opzioni di rasterizzazione per adattarli alle dimensioni desiderate.

### Q5: Dove posso chiedere aiuto o discutere problemi relativi a Aspose.CAD per Java?
A5: Vai al [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) per supporto dedicato e discussioni della community.

---

**Ultimo aggiornamento:** 2026-02-20  
**Testato con:** Aspose.CAD per Java 24.10  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}