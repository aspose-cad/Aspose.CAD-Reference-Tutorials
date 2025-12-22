---
date: 2025-12-22
description: Impara a caricare un file DWG ed estrarre le informazioni di sottofondo
  con Aspose.CAD per Java – una guida passo passo che copre i flag di sottofondo.
linktitle: Accessing Underlay Flags of DWG
second_title: Aspose.CAD Java API
title: Carica file DWG e accedi ai flag di sottofondo – Aspose.CAD per Java
url: /it/java/cad-file-manipulation/accessing-underlay-flags-of-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Carica file DWG e accedi ai flag di sottofondo – Aspose.CAD per Java

Nei moderni flussi di lavoro CAD, **caricare un file DWG** rapidamente e estrarre i dettagli del sottofondo è una necessità comune. Che tu stia creando un visualizzatore, automatizzando l'elaborazione batch o estraendo metadati per l'integrazione GIS, Aspose.CAD per Java ti offre un modo pulito, code‑first, per farlo. In questo tutorial percorreremo i passaggi esatti per **caricare il file DWG**, iterare le sue entità e leggere i flag di sottofondo che molti sviluppatori trascurano.

## Risposte rapide
- **Qual è la classe principale per aprire un DWG?** `com.aspose.cad.Image.load()` restituisce un `CadImage`.
- **Quale oggetto contiene le informazioni del sottofondo?** `CadUnderlay` (o i suoi tipi derivati come `CadDgnUnderlay`).
- **È necessaria una licenza per lo sviluppo?** Una versione di prova gratuita funziona per i test; è richiesta una licenza commerciale per la produzione.
- **Posso elaborare più file DWG in un ciclo?** Sì – basta ripetere il modello di caricamento e iterazione.
- **Questo approccio è compatibile con Java 11+?** Assolutamente, Aspose.CAD supporta Java 8 fino alle ultime versioni LTS.

## Cos'è “load dwg file” in Aspose.CAD?
`Image.load()` legge il contenuto binario DWG e crea un oggetto `CadImage` in memoria. Da lì puoi esplorare livelli, blocchi e entità di sottofondo senza doverti occupare direttamente del formato file DWG.

## Perché estrarre i flag di sottofondo da un DWG?
I flag di sottofondo indicano come un riferimento esterno (come un sottofondo DGN o PDF) è posizionato, scalato e ruotato all'interno del disegno. Conoscere questi valori ti consente di:
- Ricreare l'esatta disposizione visiva in un visualizzatore personalizzato.
- Convertire i sottofondi in entità CAD native per ulteriori modifiche.
- Generare report che includono i metadati del sottofondo per conformità o documentazione.

## Prerequisiti
- **Libreria Aspose.CAD** – scarica dalla pagina [releases](https://releases.aspose.com/cad/java/).
- **Java Development Kit** – JDK 8 o superiore.
- **Una cartella** contenente i file DWG che desideri analizzare. Sostituisci `"Your Document Directory"` nel codice con il percorso reale.

## Importa spazi dei nomi

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadBaseEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadDgnUnderlay;
import com.aspose.cad.fileformats.cad.cadobjects.CadUnderlay;
import com.aspose.cad.fileformats.cad.cadobjects.UnderlayFlags;
```

## Guida passo‑passo

### Passo 1: Imposta la directory delle risorse
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DWGDrawings/";
```
Definisci dove risiedono i tuoi file DWG. L'uso di una cartella dedicata mantiene l'esempio pulito e portabile.

### Passo 2: Carica il file DWG
```java
// Input file name and path
String fileName = dataDir + "BlockRefDgn.dwg";

// Load an existing DWG file and convert it into CadImage 
CadImage image = (CadImage)Image.load(fileName);
```
Qui **carichiamo il file DWG** `BlockRefDgn.dwg` in un'istanza `CadImage`, pronta per l'ispezione.

### Passo 3: Itera le entità DWG
```java
// Go through each entity inside the DWG file
for(CadBaseEntity entity : image.getEntities())
```
Il ciclo attraversa ogni entità—linee, cerchi, blocchi e sottofondi—così possiamo selezionare quelle necessarie.

### Passo 4: Identifica le entità CadDgnUnderlay
```java
// Check if entity is of CadDgnUnderlay type
if (entity instanceof CadDgnUnderlay)
```
Solo gli oggetti `CadDgnUnderlay` contengono i flag di sottofondo che cerchiamo, quindi li filtriamo.

### Passo 5: Accedi alle informazioni del sottofondo
```java
// Access different underlay flags 
CadUnderlay underlay = (CadUnderlay) entity;
System.out.println(underlay.getUnderlayPath());
System.out.println(underlay.getUnderlayName());
// ... (Additional underlay properties)
break;
```
Una volta ottenuto un `CadUnderlay`, possiamo leggere il suo percorso, nome, punto di inserimento, rotazione, fattori di scala e l'enumerazione `UnderlayFlags` che indica visibilità, ritaglio e altre opzioni di rendering.

## Problemi comuni e consigli
- **Percorso del sottofondo nullo** – Assicurati che il DWG faccia effettivamente riferimento a un file esterno; altrimenti il percorso sarà vuoto.
- **Tipo di sottofondo non supportato** – Attualmente Aspose.CAD supporta sottofondi DGN; i sottofondi PDF non sono ancora esposti tramite l'API.
- **Eccezioni di licenza** – Eseguire il codice senza una licenza valida aggiungerà una filigrana a tutte le immagini esportate.

## Domande frequenti

**Q: Posso usare Aspose.CAD per Java con altri formati di file CAD?**  
A: Aspose.CAD si concentra principalmente sul formato DWG, ma supporta anche DXF, DWF e altri formati CAD.

**Q: È disponibile una versione di prova per Aspose.CAD per Java?**  
A: Sì, puoi esplorare le funzionalità con una prova gratuita da [qui](https://releases.aspose.com/).

**Q: Come posso ottenere supporto o assistenza per Aspose.CAD per Java?**  
A: Visita il [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) per supporto della community e discussioni.

**Q: Sono disponibili licenze temporanee per Aspose.CAD per Java?**  
A: Sì, puoi ottenere una licenza temporanea [qui](https://purchase.aspose.com/temporary-license/).

**Q: Dove posso trovare la documentazione completa per Aspose.CAD per Java?**  
A: Consulta la [documentazione](https://referencepose.com/cad/java/) per informazioni dettagliate.

---

**Ultimo aggiornamento:** 2025-12-22  
**Testato con:** Aspose.CAD 24.12 per Java  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}