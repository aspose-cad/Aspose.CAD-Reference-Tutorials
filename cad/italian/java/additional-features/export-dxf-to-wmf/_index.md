---
date: 2025-11-29
description: Scopri come convertire DXF in WMF con Aspose.CAD per Java, caricare un
  disegno DXF e, facoltativamente, utilizzare l'esportazione Aspose in PDF. Guida
  passo‑passo con esempi di codice.
linktitle: Export DXF to WMF Format Using Java
second_title: Aspose.CAD Java API
title: Converti DXF in WMF usando Aspose.CAD in Java
url: /it/java/additional-features/export-dxf-to-wmf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convertire DXF in WMF con Aspose.CAD in Java

## Introduzione

In questo tutorial scoprirai come **convertire DXF in WMF** con Aspose.CAD per Java. Che tu debba incorporare disegni CAD in un report basato su Windows o desideri semplicemente un formato vettoriale leggero, convertire DXF in WMF è una necessità comune. Ti guideremo attraverso il caricamento di un disegno DXF, la configurazione delle opzioni di rasterizzazione, il salvataggio del risultato come WMF e persino l'uso dell'esportazione Aspose in PDF come passaggio opzionale.

## Risposte rapide
- **Posso convertire DXF in WMF con una prova gratuita?** Sì – Aspose offre una prova completa di 30 giorni.  
- **Quale versione di Java è richiesta?** Java 8 o successiva.  
- **È necessaria una licenza per eseguire il codice?** È necessaria una licenza per la produzione; la prova funziona per sviluppo e test.  
- **La conversione è senza perdita?** I dati vettoriali sono preservati; le opzioni di rasterizzazione consentono di controllare la risoluzione.  
- **Posso anche esportare lo stesso disegno in PDF?** Assolutamente – vedi il passaggio “Esporta in PDF” qui sotto.

## Cos'è “convertire DXF in WMF”?

Convertire DXF in WMF significa prendere un file Drawing Exchange Format (DXF) — un formato CAD ampiamente utilizzato — e trasformarlo in un Windows Metafile (WMF). WMF è un formato di immagine vettoriale che si integra perfettamente con Microsoft Office, le applicazioni Windows e molti strumenti di reporting.

## Perché usare Aspose.CAD per Java?

- **Nessuna dipendenza esterna** – puro Java, nessun DLL nativo.  
- **Alta fedeltà** – preserva livelli, colori e stili di linea.  
- **Rasterizzazione integrata** – regola finemente dimensione pagina, risoluzione e sfondo.  
- **Soluzione tutto-in-uno** – la stessa API supporta anche l'esportazione in PDF, PNG, SVG e altro.

## Prerequisiti

Prima di iniziare, assicurati di avere:

- **Aspose.CAD per Java** integrato nel tuo progetto. Scaricalo dal sito ufficiale: [Aspose.CAD Java download](https://releases.aspose.com/cad/java/).  
- **Directory dei documenti** dove sono archiviati i tuoi file DXF (ad esempio `Your Document Directory/DXFDrawings/`).  

## Importare i namespace

Nel tuo file sorgente Java, importa le classi Aspose.CAD di cui avrai bisogno:

```java
import com.aspose.cad.Color;
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.WmfOptions;
```

## Guida passo‑passo

### Passo 1: Caricare il disegno DXF

Per prima cosa, **carica il disegno DXF** che desideri convertire. Il metodo `Image.load` legge il file in memoria.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DXFDrawings/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### Passo 2: Configurare le opzioni di rasterizzazione

Imposta i parametri di rasterizzazione che controllano le dimensioni del WMF di output. In questo esempio usiamo una pagina di 100 × 100 unità.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(100);
rasterizationOptions.setPageHeight(100);
WmfOptions wmfOptions = new WmfOptions();
```

### Passo 3: Salvare come WMF

Ora salva il disegno caricato come file WMF utilizzando le opzioni definite sopra.

```java
cadImage.save(dataDir+" example.ifc.wmf", wmfOptions);
```

### Passo 4: Rilasciare le risorse

Rilasciare correttamente le risorse previene perdite di memoria, soprattutto quando si elaborano molti disegni.

```java
finally
{
  cadImage.dispose();
}
```

### Passo 5: Opzionale – Esportazione Aspose in PDF

Se ti serve anche una versione PDF dello stesso disegno, Aspose.CAD lo rende possibile con una sola riga di codice.

```java
image.save(dataDir + "conic_pyramid_out_.pdf"); 
```

> **Suggerimento:** Puoi riutilizzare lo stesso oggetto `CadRasterizationOptions` per l'esportazione in PDF passandolo a un'istanza `PdfOptions`.

## Problemi comuni e soluzioni

| Problema | Causa | Soluzione |
|----------|-------|-----------|
| **`NullPointerException` su `cadImage.save`** | Variabile `cadImage` non definita (dovrebbe essere `image`). | Sostituire `cadImage` con `image` o rinominare la variabile in modo coerente. |
| **Il WMF di output è vuoto** | Dimensione della pagina di rasterizzazione troppo piccola o colore di sfondo impostato su trasparente. | Aumentare `PageWidth`/`PageHeight` o impostare un colore di sfondo tramite `rasterizationOptions.setBackgroundColor(Color.getWhite());`. |
| **Eccezione di licenza** | Esecuzione senza una licenza Aspose valida in produzione. | Applicare il file di licenza all'avvio dell'applicazione: `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`. |

## Conclusione

Ora disponi di un flusso di lavoro completo e pronto per la produzione per **convertire DXF in WMF** usando Aspose.CAD per Java, con un passaggio opzionale per **esportare in PDF**. Questo approccio ti fornisce un output vettoriale di alta qualità che si integra senza problemi con gli strumenti di reporting e documentazione basati su Windows.

## FAQ

### Q1: Dove posso trovare la documentazione di Aspose.CAD?

A1: Puoi accedere alla documentazione [qui](https://reference.aspose.com/cad/java/).

### Q2: Come scarico Aspose.CAD per Java?

A2: Scarica la libreria [qui](https://releases.aspose.com/cad/java/).

### Q3: È disponibile una prova gratuita?

A3: Sì, puoi ottenere una prova gratuita [qui](https://releases.aspose.com/).

### Q4: Hai bisogno di opzioni di licenza temporanea?

A4: Esplora le licenze temporanee [qui](https://purchase.aspose.com/temporary-license/).

### Q5: Dove posso ottenere supporto?

A5: Visita il forum di supporto Aspose.CAD [qui](https://forum.aspose.com/c/cad/19).

## Domande frequenti

**Q: Posso convertire file DXF di grandi dimensioni (centinaia di MB) senza esaurire la memoria?**  
A: Sì. Carica il file in un blocco `try‑with‑resources` e rilascia prontamente l'oggetto `Image`. Regola `CadRasterizationOptions.setPageWidth/Height` a una dimensione ragionevole per mantenere basso l'uso di memoria.

**Q: L'output WMF conserva le informazioni sui layer?**  
A: WMF è un formato vettoriale piatto, quindi la gerarchia dei layer viene appiattita, ma gli stili di linea e i colori sono preservati.

**Q: È possibile impostare un DPI personalizzato per il WMF?**  
A: Usa `rasterizationOptions.setResolution(300);` per definire il DPI prima del salvataggio.

**Q: Posso convertire in batch più file DXF in un'unica esecuzione?**  
A: Assolutamente. Scorri una directory, carica ogni file e applica la stessa logica di rasterizzazione e salvataggio.

**Q: Quali versioni di Java sono supportate?**  
A: Aspose.CAD per Java supporta Java 8 e successive (inclusi Java 11, 17 e le versioni LTS più recenti).

**Ultimo aggiornamento:** 2025-11-29  
**Testato con:** Aspose.CAD per Java 24.11  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}