---
date: 2025-12-28
description: Scopri come caricare file DWG nei progetti Java e impostare il nome del
  carattere principale usando Aspose.CAD per Java. Guida passo‑passo per visualizzazioni
  CAD perfette.
linktitle: Substitute Font in DWG
second_title: Aspose.CAD Java API
title: Come caricare un file DWG in Java e sostituire il font con Aspose.CAD
url: /it/java/cad-text-and-annotation/substitute-font-in-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come caricare un file DWG in Java e sostituire il font con Aspose.CAD

## Introduzione

Se hai bisogno di **load DWG file Java** nelle applicazioni e desideri dare ai tuoi disegni un aspetto rifinito, la sostituzione del font è una soluzione rapida. Con Aspose.CAD per Java puoi sostituire lo stile di testo predefinito con qualsiasi font installato sul sistema, garantendo che ogni annotazione appaia esattamente come ti aspetti. In questo tutorial percorreremo l’intero processo—dal caricamento di un file DWG in Java all’utilizzo del metodo `setPrimaryFontName` per cambiare il font.

## Risposte rapide
- **Quale libreria è necessaria?** Aspose.CAD per Java.  
- **Posso caricare un file DWG in Java?** Sì, basta chiamare `Image.load()` sul percorso DWG.  
- **Quale metodo cambia il font?** `setPrimaryFontName`.  
- **È necessaria una licenza per la produzione?** Sì, è richiesta una licenza commerciale.  
- **È possibile l’elaborazione batch?** Assolutamente – itera su più file con lo stesso codice.

## Che cosa è “load dwg file java”?

Caricare un file DWG in un ambiente Java significa leggere i dati CAD binari in un oggetto `Image` che Aspose.CAD può manipolare. Una volta caricato il file, hai pieno accesso programmatico a livelli, stili ed entità di testo.

## Perché sostituire i font in un file DWG?

- **Coerenza:** Garantisce che tutti i collaboratori vedano lo stesso tipo di carattere, indipendentemente dalla loro configurazione locale dei font.  
- **Leggibilità:** Alcuni font CAD predefiniti sono difficili da leggere sugli schermi; passare a un font pulito come Arial migliora la chiarezza.  
- **Branding:** Allinea i disegni tecnici alle linee guida di stile aziendali.

## Prerequisiti

- **Java Development Kit (JDK)** – qualsiasi versione recente (consigliato 8+).  
- **Aspose.CAD per Java** – scarica dal [website](https://releases.aspose.com/cad/java/).  
- **File DWG di esempio** – un disegno che desideri modificare (puoi usare qualsiasi file DWG o DXF per i test).

## Importare gli spazi dei nomi

Nel tuo progetto Java, importa le classi necessarie per lavorare con Aspose.CAD. Queste importazioni ti danno accesso al caricamento delle immagini, agli oggetti specifici CAD e alla manipolazione degli stili.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject;
```

## Guida passo‑passo per sostituire il font

### Passo 1: Carica il tuo file DWG (load dwg file java)

Per prima cosa, indica all’API la posizione del tuo file DWG (o DXF) e caricalo in un oggetto `CadImage`.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage) Image.load(srcFile);
```

> **Suggerimento:** Se lavori direttamente con file DWG, sostituisci l’estensione `.dxf` con `.dwg` nella variabile `srcFile`.

### Passo 2: Iterare sulla tabella degli stili e impostare il nome del font primario

Ogni disegno CAD contiene una raccolta di oggetti stile. Scorri la collezione e utilizza il metodo `setPrimaryFontName` (la chiamata API che **sets primary font name**) per sostituire il font.

```java
for(Object style : cadImage.getStyles())
{
    // Set the font name
    ((com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject)style).setPrimaryFontName("Arial");
}
```

Puoi cambiare `"Arial"` con qualsiasi font installato sulla macchina che esegue il codice.

### Passo 3: Salvare il disegno modificato

Dopo aver aggiornato il font, scrivi le modifiche in un nuovo file DWG (o sovrascrivi l’originale).

```java
cadImage.save(dataDir + "output.dwg", new DwgOptions());
```

Il file salvato ora utilizza il font specificato e qualsiasi annotazione di testo verrà renderizzata con quel tipo di carattere.

## Problemi comuni e soluzioni

| Problema | Soluzione |
|----------|-----------|
| **Font non applicato** | Verifica che il font sia installato sul sistema operativo host e che il nome sia scritto esattamente. |
| **`Image.load` genera un'eccezione** | Assicurati che il percorso del file sia corretto e che il file sia in un formato DWG/DXF supportato. |
| **Rallentamento delle prestazioni su file di grandi dimensioni** | Elabora i file in un thread separato o in batch per evitare blocchi dell’interfaccia utente. |

## Domande frequenti

**D: Il metodo `setPrimaryFontName` influisce solo sulle entità di testo?**  
R: Aggiorna il font primario per la tabella degli stili, influenzando tutti gli oggetti di testo che fanno riferimento a quello stile.

**D: Posso usare un font personalizzato che non è installato sul sistema?**  
R: Aspose.CAD si basa sul registro dei font del sistema operativo. Per usare un font personalizzato, installalo sulla macchina che esegue il codice.

**D: È possibile cambiare il font solo per un singolo layer?**  
R: Sì, puoi filtrare gli stili per nome del layer prima di chiamare `setPrimaryFontName`.

**D: Quale versione di Aspose.CAD è necessaria per i file DWG 2022?**  
R: L’ultima release (al 2025) supporta pienamente DWG 2022. Controlla sempre le note di rilascio per il supporto di formati specifici.

**D: Come gestire le licenze in un ambiente di sviluppo?**  
R: Usa una licenza di valutazione temporanea per i test. Per la produzione, incorpora il file di licenza acquistato usando `License.setLicense("Aspose.Total.Java.lic");`.

---

**Last Updated:** 2025-12-28  
**Tested With:** Aspose.CAD per Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}