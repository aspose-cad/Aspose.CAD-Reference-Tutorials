---
date: 2026-01-07
description: Scopri come esportare CAD in SVG con Aspose.CAD per Java. Questa guida
  passo passo ti mostra come convertire DWG in SVG, impostare la modalità colore SVG
  e integrare la libreria nel tuo progetto Java.
linktitle: Export to SVG
second_title: Aspose.CAD Java API
title: Esporta CAD in SVG utilizzando Aspose.CAD per Java
url: /it/java/cad-to-pdf-and-svg-export-options/export-to-svg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Esporta CAD in SVG con Aspose.CAD per Java

## Introduzione

Benvenuti nel mondo di Aspose.CAD per Java, una potente libreria che consente agli sviluppatori di manipolare i disegni CAD con facilità. Che siate sviluppatori esperti o nuovi nel settore CAD, questa guida completa vi accompagnerà passo passo nell'**esportazione di CAD in SVG**, mostrando come convertire DWG in SVG, impostare la modalità colore SVG e integrare l'API nel vostro progetto Java.

## Risposte rapide
- **Cosa significa “export CAD to SVG”?** Converte un disegno CAD (ad es., DWG) in un file Scalable Vector Graphics che può essere visualizzato nei browser.  
- **Quale libreria gestisce la conversione?** Aspose.CAD per Java fornisce una semplice API per questo compito.  
- **Ho bisogno di una licenza per lo sviluppo?** Una prova gratuita è sufficiente per i test; è necessaria una licenza commerciale per la produzione.  
- **Posso controllare l'output colore dell'SVG?** Sì, è possibile impostare la modalità colore SVG (ad es., scala di grigi).  
- **È necessario software aggiuntivo?** Solo un runtime Java e il file JAR di Aspose.CAD.

## Prerequisiti

Prima di immergerti nel tutorial, assicurati di avere i seguenti prerequisiti:

- Ambiente di sviluppo Java: assicurati di avere Java installato sul tuo sistema.  
- Libreria Aspose.CAD: scarica e installa la libreria Aspose.CAD per Java dal [link di download](https://releases.aspose.com/cad/java/).  
- Directory dei documenti: crea una cartella per i tuoi disegni CAD e annota il suo percorso.

## Importa spazi dei nomi

In questo passaggio, importeremo gli spazi dei nomi necessari per avviare il nostro percorso con Aspose.CAD. Segui questi passaggi:

### Passo 1: Apri il tuo progetto Java
Apri il tuo progetto Java nell'IDE di tua scelta.

### Passo 2: Aggiungi la libreria Aspose.CAD
Aggiungi la libreria Aspose.CAD al tuo progetto. Puoi farlo includendo il file JAR nelle dipendenze del progetto.

### Passo 3: Importa spazi dei nomi
Nel tuo file Java, importa gli spazi dei nomi richiesti:

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.SvgOptions;
import com.aspose.cad.imageoptions.SvgColorMode;
```

## Esporta CAD in SVG

Ora che abbiamo preparato l'ambiente, approfondiamo il processo passo‑per‑passo di **export CAD to SVG** usando Aspose.CAD per Java.

### Passo 1: Specifica la directory delle risorse
Definisci il percorso della tua directory delle risorse, dove sono situati i tuoi disegni CAD:

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

### Passo 2: Carica il disegno CAD
Carica il disegno CAD usando la libreria Aspose.CAD:

```java
Image image = Image.load(dataDir + "meshes.dwg");
```

### Passo 3: Configura le opzioni di esportazione SVG
Configura le opzioni di esportazione SVG per personalizzare l'output. Qui **impostiamo la modalità colore SVG** in scala di grigi e indichiamo all'esportatore di convertire il testo in forme:

```java
SvgOptions options = new SvgOptions();
options.setColorType(SvgColorMode.Grayscale);
options.setTextAsShapes(true);
```

### Passo 4: Salva come SVG
Salva il disegno CAD come file SVG:

```java
image.save(dataDir + "meshes.svg");
```

> **Suggerimento professionale:** Se devi **convertire DWG in SVG** mantenendo i colori, cambia `SvgColorMode.Grayscale` in `SvgColorMode.FullColor`.

Congratulazioni! Hai esportato con successo un disegno CAD in SVG usando Aspose.CAD per Java.

## Perché usare Aspose.CAD per esportare CAD in SVG?
- **Alta fedeltà:** i dati vettoriali vengono conservati, garantendo che l'SVG abbia esattamente l'aspetto del disegno CAD originale.  
- **Nessuna dipendenza esterna:** la conversione avviene interamente in Java, eliminando la necessità di strumenti aggiuntivi.  
- **Output personalizzabile:** opzioni come `setColorType` ti permettono di controllare se l'SVG è in scala di grigi o a colori completi.

## Problemi comuni e soluzioni
- **File non trovato:** verifica che `dataDir` punti alla cartella corretta e che il nome del file DWG corrisponda.  
- **Output SVG vuoto:** assicurati di aver impostato `options.setTextAsShapes(true)` se il disegno contiene testo che deve apparire come forme.  
- **Formato CAD non supportato:** Aspose.CAD supporta DWG, DXF, DWF e diversi altri formati; controlla la documentazione per l'elenco completo.

## Conclusione

In questo tutorial, abbiamo esplorato il processo fluido di utilizzo di Aspose.CAD per Java per **export CAD to SVG**. Con la sua API intuitiva e le funzionalità robuste, Aspose.CAD semplifica compiti complessi, fornendo agli sviluppatori uno strumento versatile per la manipolazione CAD.

## FAQ

### Q1: Posso usare Aspose.CAD per Java con altri formati CAD?
A1: Sì, Aspose.CAD supporta vari formati CAD, inclusi DWG, DXF, DWF e altri.

### Q2: Aspose.CAD è adatto sia ai principianti che agli sviluppatori esperti?
A2: Assolutamente! Aspose.CAD offre un'API user‑friendly, rendendola accessibile ai principianti, fornendo al contempo funzionalità avanzate per gli sviluppatori esperti.

### Q3: Dove posso trovare supporto aggiuntivo o discussioni della community?
A3: Visita il [Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) per supporto e discussioni.

### Q4: È disponibile una prova gratuita?
A4: Sì, puoi esplorare Aspose.CAD con una [prova gratuita](https://releases.aspose.com/).

### Q5: Come posso acquistare una licenza per Aspose.CAD per Java?
A5: Puoi acquistare una licenza dalla [pagina di acquisto](https://purchase.aspose.com/buy).

## Domande frequenti

**Q: Posso convertire un file DXF in SVG usando lo stesso codice?**  
A: Sì, basta sostituire il nome del file con un file DXF; l'API gestisce entrambi i formati.

**Q: Come modifico l'output in SVG a colori completi?**  
A: Imposta `options.setColorType(SvgColorMode.FullColor);` prima di salvare.

**Q: È possibile incorporare i font nell'SVG generato?**  
A: Attualmente Aspose.CAD converte il testo in forme; l'incorporamento dei font non è necessario.

**Q: La libreria funziona su Linux e macOS?**  
A: La libreria Java è indipendente dalla piattaforma e funziona ovunque sia disponibile una JVM compatibile.

**Q: Quale versione di Aspose.CAD è stata usata in questo tutorial?**  
A: L'esempio è stato testato con Aspose.CAD per Java 24.10.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Ultimo aggiornamento:** 2026-01-07  
**Testato con:** Aspose.CAD per Java 24.10  
**Autore:** Aspose