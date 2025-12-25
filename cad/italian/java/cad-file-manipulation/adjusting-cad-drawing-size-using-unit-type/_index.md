---
date: 2025-12-25
description: Scopri come esportare DWG in BMP usando Aspose.CAD per Java. Questa guida
  passo‑passo mostra come regolare le dimensioni del disegno CAD e convertire CAD
  in BMP in modo efficiente.
linktitle: Adjusting CAD Drawing Size Using Unit Type
second_title: Aspose.CAD Java API
title: Esporta DWG in BMP – Regola le dimensioni CAD usando il tipo di unità (Java)
url: /it/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Esporta DWG in BMP – Regolazione delle dimensioni del disegno CAD usando Unit Type con Aspose.CAD per Java

## Introduzione

Quando è necessario **esportare DWG in BMP**, controllare le dimensioni dell'output e l'unità di misura è fondamentale per l'elaborazione a valle o per la stampa. In questo tutorial imparerai a regolare le dimensioni del disegno CAD e a convertire CAD in BMP con Aspose.CAD per Java, utilizzando la proprietà `UnitType` per definire l'unità di misura. I passaggi sono spiegati in modo chiaro, così potrai seguirli anche se sei nuovo alla libreria.

## Risposte Rapide
- **Che cosa significa “export DWG to BMP”?** Conversione di un disegno DWG in un'immagine raster BMP.  
- **Quale proprietà controlla le dimensioni dell'output?** `CadRasterizationOptions.setUnitType()` imposta l'unità (ad es. centimetro).  
- **È necessaria una licenza per eseguire il codice?** Una prova gratuita è sufficiente per la valutazione; è necessaria una licenza per la produzione.  
- **Posso scegliere altri layout?** Sì, usa `setLayouts()` per specificare i layout modello o paper space.  
- **Quali formati di output sono supportati?** Oltre a BMP, è possibile esportare in PNG, JPEG, TIFF, ecc., modificando la classe delle opzioni.

## Cos'è **export DWG to BMP**?

Esportare DWG in BMP significa rasterizzare un file DWG basato su vettori in un'immagine bitmap (BMP). Questo è utile quando è necessaria una rappresentazione pixel‑perfect per sistemi legacy, pipeline di elaborazione immagini o scenari di visualizzazione semplici.

## Perché regolare le dimensioni del disegno CAD con **Unit Type**?

Impostare il tipo di unità consente di controllare le dimensioni fisiche dell'immagine esportata senza calcolare manualmente i fattori di scala. Questo garantisce che la bitmap corrisponda alle misurazioni del mondo reale (ad es. centimetri), elemento cruciale per i disegni ingegneristici e la documentazione stampata.

## Prerequisiti

Prima di immergerti nel tutorial, assicurati di avere i seguenti prerequisiti:

- **Ambiente di sviluppo Java** – Un JDK funzionante (8 o successivo) e un IDE o strumento di build (Maven/Gradle).  
- **Libreria Aspose.CAD per Java** – Scarica e integra la libreria Aspose.CAD nel tuo progetto Java. Puoi ottenere la libreria [qui](https://releases.aspose.com/cad/java/).

## Importa Namespace

Nel tuo codice Java, includi i namespace necessari per accedere alle funzionalità di Aspose.CAD. Aggiungi le seguenti importazioni:

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Ora, analizziamo il processo di regolazione delle dimensioni del disegno CAD usando il tipo di unità in passaggi gestibili:

## Passo 1: Definisci la Directory dei Dati

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

Imposta il percorso della directory in cui sono situati i tuoi file CAD.

## Passo 2: Carica il Disegno CAD

```java
String sourceFilePath = dataDir + "sample.dwg";
Image image = Image.load(sourceFilePath);
```

Carica il disegno CAD utilizzando la classe `Image` di Aspose.CAD.

## Passo 3: Crea le Opzioni BMP

```java
BmpOptions bmpOptions = new BmpOptions();
```

Istanzia la classe `BmpOptions` per esportare il layout CAD in formato BMP.

## Passo 4: Configura le Opzioni di Rasterizzazione

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

Crea un'istanza di `CadRasterizationOptions` e associala a `BmpOptions` per la rasterizzazione vettoriale.

## Passo 5: Imposta il Tipo di Unità

```java
cadRasterizationOptions.setUnitType(UnitType.Centimeter);
```

Specifica il tipo di unità desiderato per il disegno CAD. In questo esempio, è stato impostato su **Centimeter**, che influisce direttamente sulle dimensioni dell'immagine esportata quando **regoli le dimensioni del disegno CAD**.

## Passo 6: Imposta i Layout

```java
cadRasterizationOptions.setLayouts(new String[] { "Model" });
```

Definisci i layout da considerare durante l'esportazione. In questo caso, è stato selezionato il layout **"Model"**, ma è possibile passare ai layout paper space se necessario.

## Passo 7: Esporta in BMP

```java
String outPath = sourceFilePath + ".bmp";
image.save(outPath, bmpOptions);
```

Infine, salva il disegno CAD modificato in formato BMP. Questo passaggio completa il flusso di lavoro **export DWG to BMP** mantenendo le regolazioni di dimensione configurate.

## Problemi Comuni e Soluzioni

| Problema | Motivo | Soluzione |
|----------|--------|-----------|
| **L'immagine esportata è troppo piccola** | Tipo di unità non impostato o impostato di default (pixel) | Chiama `setUnitType()` con la misura desiderata (ad es. `UnitType.Centimeter`). |
| **Layout esportato errato** | Errore di battitura nel nome del layout | Verifica i nomi dei layout con un visualizzatore CAD; usa la stringa esatta in `setLayouts()`. |
| **Eccezione di licenza** | Esecuzione senza licenza valida in produzione | Applica una licenza temporanea o permanente come descritto nella FAQ. |

## Domande Frequenti (Estese)

**D: Posso usare Aspose.CAD per Java con altri linguaggi di programmazione?**  
R: Aspose.CAD supporta principalmente Java, ma sono disponibili versioni per altri linguaggi come .NET.

**D: Esistono opzioni di licenza per Aspose.CAD?**  
R: Sì, puoi esplorare le opzioni di licenza e acquistare Aspose.CAD [qui](https://purchase.aspose.com/buy).

**D: È disponibile una prova gratuita per Aspose.CAD?**  
R: Certamente, puoi accedere a una prova gratuita [qui](https://releases.aspose.com/).

**D: Come posso ottenere supporto per Aspose.CAD per Java?**  
R: Visita il forum di Aspose.CAD [qui](https://forum.aspose.com/c/cad/19) per un supporto completo.

**D: Posso ottenere una licenza temporanea per Aspose.CAD?**  
R: Sì, puoi acquisire una licenza temporanea [qui](https://purchase.aspose.com/temporary-license/).

**Ultimo aggiornamento:** 2025-12-25  
**Testato con:** Aspose.CAD for Java 24.10  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}