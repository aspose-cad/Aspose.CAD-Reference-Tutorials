---
date: 2026-02-15
description: Scopri come impostare una dimensione di pagina personalizzata e creare
  PDF da CAD usando Aspose.CAD per Java. Questa guida passo passo copre l'esportazione
  di CAD in PDF con Auto Layout Scaling.
linktitle: Setting Auto Layout Scaling
second_title: Aspose.CAD Java API
title: Imposta dimensione pagina personalizzata – PDF da CAD con ridimensionamento
  automatico del layout
url: /it/java/advanced-cad-features/setting-auto-layout-scaling/
weight: 17
---

.

Also keep URLs unchanged.

Also keep variable names like `CadRasterizationOptions`, `setResolution(300)`, etc.

Ok produce final.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Imposta Dimensione Pagina Personalizzata – Crea PDF da CAD con Ridimensionamento Automatico del Layout

## Introduzione

Se hai bisogno di **impostare una dimensione pagina personalizzata** mentre **crei PDF da file CAD** in modo rapido e con una scalatura perfetta, Aspose.CAD per Java ti copre. Il Ridimensionamento Automatico del Layout regola automaticamente le dimensioni del layout in modo che il PDF risultante appaia esattamente come previsto, indipendentemente dalla dimensione originale della pagina CAD. In questo tutorial percorreremo l’intero processo — dal caricamento di un file DXF all’esportazione in PDF — evidenziando le capacità di **esportazione CAD in PDF** della libreria e mostrando come è possibile anche **convertire DWG in PDF** o **aumentare la risoluzione del PDF** quando necessario.

## Risposte Rapide
- **Cosa fa il Ridimensionamento Automatico del Layout?** Ridimensiona automaticamente i layout CAD per adattarli alle dimensioni della pagina di destinazione durante la rasterizzazione.  
- **Quali formati posso convertire?** Qualsiasi formato supportato da Aspose.CAD (ad es. DXF, DWG, DWF) può essere convertito in PDF.  
- **È necessaria una licenza per la produzione?** Sì, è richiesta una licenza commerciale per l’uso non‑valutazione.  
- **Quanto tempo richiede la conversione?** Tipicamente meno di un secondo per file standard su hardware moderno.  
- **Posso modificare la dimensione della pagina?** Sì, è possibile impostare dimensioni pagina personalizzate tramite `CadRasterizationOptions`.

## Che cosa significa “creare PDF da CAD”?

Creare un PDF da CAD significa prendere un disegno ingegneristico basato su vettori (DXF, DWG, ecc.) e rasterizzarlo in un documento PDF. Il PDF mantiene la fedeltà visiva del disegno originale ed è visualizzabile su qualsiasi piattaforma.

## Perché usare il Ridimensionamento Automatico del Layout?

- **Output coerente:** Garantisce che tutti i layout riempiano la pagina PDF senza calcoli manuali delle dimensioni.  
- **Risparmio di tempo:** Elimina la necessità di regolare manualmente i fattori di scala per ogni disegno.  
- **Alta qualità:** Mantiene lo spessore delle linee e la precisione della geometria durante la conversione.  
- **Flessibilità:** Funziona per **convertire dxf in pdf**, **convertire dwg in pdf**, e anche quando è necessario **aumentare la risoluzione del PDF** per file pronti alla stampa.

## Prerequisiti

1. **Libreria Aspose.CAD per Java** – scarica l’ultima versione dalla [pagina di download](https://releases.aspose.com/cad/java/).  
2. **Directory delle risorse** – crea una cartella sul tuo computer per memorizzare i file CAD; sostituisci `"Your Document Directory"` nel codice con quel percorso.  
3. **File CAD di esempio** – per questa guida utilizzeremo `conic_pyramid.dxf`, incluso nel set di dati di esempio di Aspose.

## Importare i Namespace

Per prima cosa, importa le classi necessarie. Questo ci dà accesso al caricamento delle immagini, alla rasterizzazione e alle funzionalità di esportazione PDF.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Come Impostare una Dimensione Pagina Personalizzata per PDF da CAD

Prima di entrare nel codice passo‑a‑passo, comprendiamo perché impostare una dimensione pagina personalizzata è importante. Quando **imposti una dimensione pagina personalizzata**, controlli le dimensioni fisiche del PDF risultante (ad es. A4, Letter o una misura su misura). Questo è essenziale nei flussi di lavoro ingegneristici dove i disegni devono corrispondere agli standard di foglio o quando è necessario incorporare il PDF in documenti più grandi.

### Passo 1: Caricare il File CAD

Caricare il file sorgente è il primo passo in **come esportare CAD** in un documento PDF.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### Passo 2: Creare le Opzioni di Rasterizzazione

Definisci le dimensioni della pagina di destinazione. Puoi anche usare questo blocco per **impostare manualmente la dimensione pagina CAD** se preferisci un layout personalizzato.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

### Passo 3: Impostare il Ridimensionamento Automatico del Layout

Abilita la funzionalità di scalatura automatica. Questo è il fulcro di **come impostare la scalatura** per una conversione CAD‑to‑PDF.

```java
rasterizationOptions.setAutomaticLayoutsScaling(true);
```

### Passo 4: Creare le Opzioni PDF

Collega le impostazioni di rasterizzazione alle opzioni di esportazione PDF.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Passo 5: Esportare in PDF

Infine, salva l’immagine renderizzata come file PDF. Questo passaggio completa il flusso di lavoro **convertire dxf in pdf**.

```java
image.save(dataDir + "result_out_.pdf", pdfOptions);
```

Ripeti i passaggi sopra per qualsiasi altro file CAD che devi elaborare, sia esso **DWG**, **DWF** o altri formati supportati.

## Casi d'Uso Comuni

| Scenario | Perché impostare una dimensione pagina personalizzata? |
|----------|--------------------------------------------------------|
| **Presentazione di disegni di costruzione** | Allinea il PDF alle dimensioni standard di foglio A1/A2 richieste dagli enti regolatori. |
| **Incorporamento in manuali tecnici** | Garantisce che il disegno si adatti al layout predefinito del manuale senza scalature aggiuntive. |
| **Stampa ad alta risoluzione** | Consente di aumentare DPI (ad es. `rasterizationOptions.setResolution(300)`) mantenendo costanti le dimensioni della pagina. |

## Problemi Comuni & Risoluzione

| Sintomo | Probabile Causa | Correzione |
|---------|-----------------|------------|
| PDF vuoto | Opzioni di rasterizzazione non impostate o percorso file errato | Verifica il percorso `srcFile` e assicurati che `setPageWidth/Height` siano diversi da zero |
| Scalatura distorta | `setAutomaticLayoutsScaling` lasciato a `false` | Abilita la scalatura automatica o calcola manualmente il fattore di scala |
| Strati mancanti | Il DXF sorgente contiene entità non supportate | Controlla le note di rilascio di Aspose.CAD per i tipi di entità supportati |

## Domande Frequenti

**D: Aspose.CAD per Java è compatibile con tutti i formati CAD?**  
R: Aspose.CAD per Java supporta vari formati CAD, inclusi DWG, DXF e DWF.

**D: Posso personalizzare ulteriormente le opzioni di scalatura?**  
R: Sì, la classe `CadRasterizationOptions` offre proprietà per affinare la scalatura, DPI e altre impostazioni di rasterizzazione.

**D: Dove posso trovare documentazione aggiuntiva per Aspose.CAD per Java?**  
R: Consulta la [documentazione](https://reference.aspose.com/cad/java/) per informazioni dettagliate ed esempi.

**D: È disponibile una versione di prova gratuita per Aspose.CAD per Java?**  
R: Sì, puoi provare una [versione di prova gratuita](https://releases.aspose.com/) per sperimentare le funzionalità di Aspose.CAD per Java.

**D: Come posso richiedere assistenza o partecipare a discussioni su Aspose.CAD per Java?**  
R: Visita il [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) per connetterti con la community e chiedere supporto.

**Altre Domande Comuni**

**D: Come converto un file DWG in PDF invece di DXF?**  
R: Lo stesso codice funziona; basta cambiare l’estensione del file in `srcFile` a `.dwg`.

**D: Posso impostare un DPI personalizzato per PDF ad alta risoluzione?**  
R: Sì, usa `rasterizationOptions.setResolution(300);` (o qualsiasi DPI necessario).

**D: È possibile incorporare i font nel PDF generato?**  
R: Aspose.CAD rasterizza il disegno, quindi i font vengono renderizzati come vettori; non è necessario incorporare font separati.

## Conclusione

Seguendo questa guida ora sai come **impostare una dimensione pagina personalizzata** e **creare PDF da CAD** usando Aspose.CAD per Java con Ridimensionamento Automatico del Layout. Il processo semplifica il flusso di lavoro **esportazione CAD in PDF**, garantisce una scalatura coerente e ti fa risparmiare tempo di sviluppo. Sentiti libero di sperimentare con diverse dimensioni di pagina, risoluzioni e formati CAD per soddisfare le esigenze del tuo progetto, sia che tu stia **convertendo DWG in PDF**, **aumentando la risoluzione del PDF**, o costruendo un **processore batch java CAD to PDF**.

---

**Ultimo aggiornamento:** 2026-02-15  
**Testato con:** Aspose.CAD per Java 24.12 (ultima versione)  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}