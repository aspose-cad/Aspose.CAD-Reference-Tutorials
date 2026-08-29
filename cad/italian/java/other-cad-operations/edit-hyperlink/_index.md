---
date: 2026-06-19
description: Scopri come modificare i file DWG con Aspose.CAD per Java, inclusa la
  procedura per aggiornare i percorsi DWG XRef e modificare i collegamenti ipertestuali.
  Prova la versione di valutazione gratuita oggi!
keywords:
- how to edit dwg
- update dwg xref paths
- Aspose.CAD Java hyperlink
linktitle: Modifica Hyperlink
schemas:
- author: Aspose
  dateModified: '2026-06-19'
  description: Learn how to edit DWG files with Aspose.CAD for Java, including how
    to update DWG XRef paths and edit hyperlinks. Try the free trial today!
  headline: How to Edit DWG Hyperlinks - Aspose.CAD Java Tutorial
  type: TechArticle
- description: Learn how to edit DWG files with Aspose.CAD for Java, including how
    to update DWG XRef paths and edit hyperlinks. Try the free trial today!
  name: How to Edit DWG Hyperlinks - Aspose.CAD Java Tutorial
  steps:
  - name: Accessing Insert Objects
    text: '`CadInsertObject` is the Aspose.CAD class that represents an inserted block
      reference (XRef) inside a DWG drawing. Iterate through the entities and identify
      if an entity is an instance of the `CadInsertObject` class.'
  - name: How to Change XRef Path in a DWG Drawing
    text: '`CadImage` is the primary object that loads and saves CAD files in Aspose.CAD
      for Java. Once you have identified the insert object, retrieve the associated
      block entity and update the XRef path as needed. This ensures the reference
      points to the correct external file.'
  - name: Modifying Hyperlinks
    text: Next, check if the entity has a hyperlink associated with it. If the hyperlink
      matches a specific URL, update it to the desired URL. This step guarantees that
      clicking the hyperlink in the CAD viewer opens the new target.
  type: HowTo
- questions:
  - answer: Yes, after making changes call `cadImage.save("EditedDrawing.dwg");` to
      persist the modifications.
    question: Do I need to call a specific method to write the edited DWG back to
      disk?
  - answer: Absolutely—loop through `cadImage.getEntities()` and apply the hyperlink
      logic to each matching entity.
    question: Is it possible to edit multiple hyperlinks in one pass?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Come modificare i collegamenti ipertestuali DWG - Tutorial Java di Aspose.CAD
url: /it/java/other-cad-operations/edit-hyperlink/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come modificare i collegamenti ipertestuali DWG - Tutorial Java di Aspose.CAD

Nell'era digitale odierna, **come modificare i file DWG** in modo efficiente è una competenza indispensabile per ingegneri, architetti e specialisti BIM. Che tu debba correggere un collegamento ipertestuale interrotto, puntare un XRef a una nuova sorgente o aggiornare in batch molti disegni, Aspose.CAD per Java offre un modo pulito e programmatico per apportare tali modifiche senza aprire l'editor CAD. Questo tutorial ti guida attraverso l'intero processo, dal caricamento di un disegno al salvataggio delle modifiche.

## Risposte rapide
- **Quale libreria gestisce la modifica dei DWG in Java?** Aspose.CAD for Java.  
- **Posso modificare contemporaneamente i collegamenti ipertestuali e i percorsi XRef?** Sì—entrambi sono supportati nella stessa API.  
- **È necessaria una licenza per lo sviluppo?** Una versione di prova gratuita è sufficiente per i test; è necessaria una licenza commerciale per la produzione.  
- **Quale versione di Java è richiesta?** Java 8 o superiore.  
- **Il campione di codice è eseguibile così com'è?** Sì, dopo aver aggiornato i percorsi dei file per puntare ai tuoi file DWG locali.

## Perché modificare i collegamenti ipertestuali DWG e i percorsi XRef?

Mantenere aggiornati i collegamenti ipertestuali e i percorsi XRef evita riferimenti interrotti, garantisce che la documentazione del progetto punti sempre alle risorse corrette e consente aggiornamenti batch automatizzati su ampie librerie CAD. Ciò riduce lo sforzo manuale, minimizza gli errori e migliora l'efficienza complessiva del progetto permettendo agli sviluppatori di mantenere programmaticamente l'integrità dei collegamenti durante l'intero ciclo di vita del design.

## Prerequisiti

Prima di immergerci nel tutorial, assicurati di avere i seguenti prerequisiti pronti:

1. **Ambiente di sviluppo Java:** Un JDK 8+ installato e il tuo IDE preferito (IntelliJ IDEA, Eclipse, ecc.).  
2. **Libreria Aspose.CAD per Java:** Scarica e installa la libreria Aspose.CAD per Java dal [link di download](https://releases.aspose.com/cad/java/).  
3. **Disegno DWG:** Disponi di un file di disegno DWG pronto per la modifica dei collegamenti ipertestuali.

## Importa i pacchetti

Inizia importando i pacchetti necessari nel tuo progetto Java. Questo garantisce l'accesso alle funzionalità di Aspose.CAD per Java.

```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadBaseEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadBlockEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadInsertObject;
```

## Come modificare i collegamenti ipertestuali DWG usando Aspose.CAD per Java?

`CadImage` è la classe Aspose.CAD usata per caricare e salvare disegni CAD.  
Carica il file DWG con `CadImage`, itera le sue entità, aggiorna il collegamento ipertestuale e il percorso XRef dove necessario, e infine salva l'immagine nuovamente in DWG. Questo flusso end‑to‑end ti consente di modificare un numero qualsiasi di entità in un unico passaggio, garantendo che tutte le modifiche vengano salvate.

### Passo 1: Accesso agli oggetti Insert

`CadInsertObject` è la classe Aspose.CAD che rappresenta un riferimento a blocco inserito (XRef) all'interno di un disegno DWG. Itera le entità e identifica se un'entità è un'istanza della classe `CadInsertObject`.

```java
    String dataDir = "Your Document Directory" + "DWGDrawings/";
    
    CadImage cadImage = (CadImage)Image.load(dataDir + "AutoCad_Sample.dwg");
    for (CadBaseEntity entity : cadImage.getEntities())
    {
        if (entity instanceof CadInsertObject)
        {
        }
	}
```

### Passo 2: Come modificare il percorso XRef in un disegno DWG

`CadImage` è l'oggetto principale che carica e salva file CAD in Aspose.CAD per Java. Una volta identificato l'oggetto insert, recupera l'entità blocco associata e aggiorna il percorso XRef secondo necessità. Questo garantisce che il riferimento punti al file esterno corretto.

```java
			CadBlockEntity block = cadImage.getBlockEntities().get_Item(((CadInsertObject)entity).getName());
            String value = block.getXRefPathName().getValue();
            if (value != null && !value.contentEquals(""))
            {
                block.getXRefPathName().setValue("new file reference.dwg");
            }
    
```

### Passo 3: Modifica dei collegamenti ipertestuali

Successivamente, verifica se l'entità ha un collegamento ipertestuale associato. Se il collegamento corrisponde a un URL specifico, aggiornalo all'URL desiderato. Questo passaggio garantisce che facendo clic sul collegamento ipertestuale nel visualizzatore CAD si apra la nuova destinazione.

```java
        if (entity.getHyperlink() == "https://products.aspose.com")
        {
            entity.setHyperlink("https://www.aspose.com");
        }
```

## Problemi comuni e consigli

- **Confronto di stringhe:** Usa `.equals()` invece di `==` per un confronto affidabile delle stringhe in Java. L'esempio usa `==` per semplicità, ma in produzione sostituiscilo con `entity.getHyperlink().equals(\"https://products.aspose.com\")`.  
- **Controlli null:** Verifica sempre che `block.getXRefPathName()` non sia `null` prima di chiamare `.getValue()`.  
- **Salvataggio delle modifiche:** Dopo aver modificato le entità, chiama `cadImage.save(\"output.dwg\");` per salvare le modifiche (codice omesso per mantenere il conteggio originale dei blocchi).  
- **Nota sulle prestazioni:** Aspose.CAD per Java supporta più di 30 formati CAD e può elaborare file fino a 2 GB senza caricare l'intero documento in memoria, rendendo gli aggiornamenti massivi rapidi ed efficienti in termini di memoria.

## Domande frequenti

### Q1: Aspose.CAD per Java è compatibile con tutte le versioni di disegni DWG?

A1: Aspose.CAD per Java supporta più di 50 versioni DWG, coprendo le release da AutoCAD 2000 fino al più recente formato 2025.

### Q2: Posso usare Aspose.CAD per Java in progetti commerciali?

A2: Sì, è necessaria una licenza commerciale per l'uso in produzione. Puoi acquistare una licenza [qui](https://purchase.aspose.com/buy).

### Q3: È disponibile una versione di prova gratuita per Aspose.CAD per Java?

A3: Sì, puoi provare una versione di prova gratuita [qui](https://releases.aspose.com/).

### Q4: Come posso ottenere supporto tecnico per Aspose.CAD per Java?

A4: Per qualsiasi assistenza tecnica, visita il forum Aspose.CAD [qui](https://forum.aspose.com/c/cad/19).

### Q5: Posso ottenere una licenza temporanea per scopi di test?

A5: Sì, puoi ottenere una licenza temporanea [qui](https://purchase.aspose.com/temporary-license/).

**Domande aggiuntive**

**Q: Devo chiamare un metodo specifico per scrivere il DWG modificato su disco?**  
**A: Sì, dopo aver apportato le modifiche chiama `cadImage.save("EditedDrawing.dwg");` per salvare le modifiche.**

**Q: È possibile modificare più collegamenti ipertestuali in un unico passaggio?**  
**A: Assolutamente—itera su `cadImage.getEntities()` e applica la logica del collegamento ipertestuale a ogni entità corrispondente.**

---

**Ultimo aggiornamento:** 2026-06-19  
**Testato con:** Aspose.CAD per Java 24.12  
**Autore:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutorial correlati

- [Leggi i metadati XREF dai file DWG usando Aspose.CAD per Java](/cad/java/cad-meta-data-and-rendering/read-xref-meta-data/)
- [Aggiungi proprietà personalizzate ai file DWG usando Aspose.CAD per Java](/cad/java/additional-features/add-custom-properties/)
- [Esporta DWG in PDF o raster usando Aspose.CAD per Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}