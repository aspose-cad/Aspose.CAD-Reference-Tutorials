---
date: 2026-05-25
description: Scopri come impostare la licenza a consumo in Aspose.CAD per Java per
  ottimizzare l'elaborazione CAD, ridurre i costi e monitorare l'utilizzo in modo
  efficiente.
keywords:
- how to set metered
- Aspose.CAD licensing
- Java metered licensing
linktitle: Come impostare la licenza a consumo in Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-05-25'
  description: Learn how to set metered licensing in Aspose.CAD for Java to optimize
    CAD processing, reduce costs, and track usage efficiently.
  headline: How to Set Metered Licensing in Aspose.CAD
  type: TechArticle
- questions:
  - answer: A usage‑based model that tracks API calls and charges per consumption
      unit.
    question: What is metered licensing?
  - answer: Two keys – a public and a private key – generated from your Aspose account.
    question: How many keys are required?
  - answer: Yes, call `License.getConsumptionQuantity()` before and after processing.
    question: Can I check usage programmatically?
  - answer: A free trial license can be obtained from the Aspose website.
    question: Is a trial available?
  - answer: Java 8 through 17 are fully supported.
    question: Which Java version is supported?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Come impostare la licenza a consumo in Aspose.CAD
url: /it/java/licensing-and-configuration/metered-licensing-in-aspose-cad/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Licenza a consumo in Aspose.CAD

## Introduzione

Sblocca tutto il potenziale di Aspose.CAD per Java con la licenza **how to set metered**! Questa guida passo‑passo ti accompagna in ogni fase — dall'installazione dei prerequisiti, all'importazione dei pacchetti corretti, fino alla misurazione del consumo prima e dopo l'elaborazione. Alla fine saprai esattamente come impostare le chiavi **how to set metered**, leggere le metriche di utilizzo e mantenere il tuo flusso di lavoro CAD conveniente.

## Risposte rapide
- **Cos'è la licenza a consumo?** Un modello basato sull'uso che traccia le chiamate API e addebita per unità di consumo.  
- **Quante chiavi sono necessarie?** Due chiavi — una pubblica e una privata — generate dal tuo account Aspose.  
- **Posso verificare l'utilizzo programmaticamente?** Sì, chiama `License.getConsumptionQuantity()` prima e dopo l'elaborazione.  
- **È disponibile una versione di prova?** È possibile ottenere una licenza di prova gratuita dal sito web di Aspose.  
- **Quale versione di Java è supportata?** Java 8 fino a 17 sono pienamente supportate.

## Cos'è la licenza a consumo in Aspose.CAD?

La licenza a consumo è il modello pay‑as‑you‑go di Aspose.CAD che registra ogni chiamata API come unità di consumo. Ti consente di monitorare l'utilizzo esatto, evitare il sovra‑dimensionamento e pagare solo per ciò che effettivamente consumi.

## Perché utilizzare la licenza a consumo per l'elaborazione CAD?

Aspose.CAD supporta **50+** formati di input e output — inclusi DWG, DXF, DGN e SVG — e può elaborare file fino a **2 GB** senza caricare l'intero documento in memoria. Questa efficienza si traduce in costi di server più bassi, soprattutto quando si gestiscono grandi lotti di disegni.

## Prerequisiti

Prima di immergerti nel mondo della licenza a consumo con Aspose.CAD, assicurati di avere quanto segue a disposizione:

### Installazione del Java Development Kit (JDK)

Assicurati di avere installata l'ultima versione del Java Development Kit sul tuo sistema. Puoi scaricarla da [qui](https://www.oracle.com/java/technologies/javase-downloads.html).

### Libreria Aspose.CAD per Java

Assicurati di scaricare e configurare la libreria Aspose.CAD per Java. Puoi trovare la libreria [qui](https://releases.aspose.com/cad/java/). Puoi anche sfogliare altre versioni di Aspose [qui](https://releases.aspose.com/).

## Come impostare la licenza a consumo in Aspose.CAD per Java?

Carica le tue chiavi pubblica e privata, chiama `License.setMeteredKey(publicKey, privateKey)`, e la libreria passa immediatamente alla modalità a consumo. Questa singola chiamata attiva il tracciamento dell'utilizzo per ogni operazione API successiva, consentendoti di interrogare il consumo prima e dopo qualsiasi fase di elaborazione.

## Importa i pacchetti

Per utilizzare la libreria, importa il suo pacchetto principale:

`import com.aspose.cad.*;` porta le classi Aspose.CAD nel tuo progetto.

```java
import com.aspose.cad;
```

## Passo 1: Imposta la chiave a consumo

`setMeteredKey` registra le tue chiavi pubblica e privata con la libreria Aspose.CAD.

Innanzitutto, imposta la chiave a consumo usando il metodo `setMeteredKey`. Sostituisci `<valid public key>` e `<valid private key>` con le tue chiavi pubblica e privata effettive.

```java
Metered.setMeteredKey("<valid public key>", "<valid private key>");
```

## Passo 2: Ottieni la quantità di consumo prima dell'elaborazione

`getConsumptionQuantity` restituisce il numero totale di unità di consumo registrate finora.

Recupera il valore della quantità consumata prima di accedere all'API Aspose.CAD per ottenere una prima valutazione.

```java
BigDecimal quantityOld = Metered.getConsumptionQuantity();
System.out.println("Consumption quantity before processing: " + quantityOld);
```

## Passo 3: Elaborazione

Esegui l'elaborazione CAD desiderata utilizzando le funzionalità di Aspose.CAD. Decommenta lo snippet di codice relativo al tuo compito specifico, ad esempio il caricamento di un'immagine CAD.

```java
// Example:
// com.aspose.cad.fileformats.cad.CadImage image =
// (com.aspose.cad.fileformats.cad.CadImage)com.aspose.cad.Image.load("BlockRefDgn.dwg");
```

## Passo 4: Ottieni la quantità di consumo dopo l'elaborazione

Dopo l'elaborazione, ottieni nuovamente il valore della quantità consumata per valutare l'impatto.

```java
BigDecimal quantity = Metered.getConsumptionQuantity();
System.out.println("Consumption quantity after processing: " + quantity);
```

Ripeti questi passaggi per qualsiasi elaborazione o attività aggiuntiva secondo necessità.

## Problemi comuni e soluzioni

- **Invalid key error:** Verifica che entrambe le chiavi siano copiate esattamente come mostrato nel tuo account Aspose; gli spazi extra causano errori di autenticazione.  
- **Zero consumption reported:** Assicurati di chiamare `License.getConsumptionQuantity()` *dopo* il primo utilizzo dell'API; la prima chiamata inizializza il contatore.  
- **Performance slowdown on large files:** Usa `CadImage.load(..., LoadOptions)` con `LoadOptions.setLoadMode(LoadMode.Stream)` per evitare di caricare l'intero file in memoria.

## Domande frequenti

**Q1: Posso utilizzare la licenza a consumo per scopi di valutazione?**  
A1: Sì, puoi ottenere una licenza di prova gratuita [qui](https://releases.aspose.com/).

**Q2: Dove posso trovare la documentazione dettagliata per Aspose.CAD per Java?**  
A2: Consulta la documentazione [qui](https://reference.aspose.com/cad/java/).

**Q3: Come posso acquistare una licenza per Aspose.CAD per Java?**  
A3: Visita la pagina di acquisto [qui](https://purchase.aspose.com/buy).

**Q4: È disponibile un'opzione di licenza temporanea?**  
A5: Sì, puoi esplorare le licenze temporanee [qui](https://purchase.aspose.com/temporary-license/).

**Q5: Hai bisogno di supporto dalla community o hai domande specifiche?**  
A5: Vai al forum Aspose.CAD [qui](https://forum.aspose.com/c/cad/19).

**Q6: La licenza a consumo funziona con le distribuzioni cloud?**  
A6: Assolutamente. La stessa chiamata `setMeteredKey` funziona in Docker, Kubernetes o ambienti serverless.

**Q7: Posso resettare il contatore di consumo?**  
A7: Il contatore si resetta automaticamente all'inizio di ogni nuovo periodo di fatturazione; non è possibile resettarlo manualmente.

## Conclusione

Congratulazioni! Hai padroneggiato con successo la licenza **how to set metered** con Aspose.CAD per Java. Seguendo questa guida, hai configurato e integrato la licenza a consumo senza problemi nel tuo progetto Java, garantendo un utilizzo efficiente delle funzionalità di Aspose.CAD mantenendo i costi trasparenti.

---

**Ultimo aggiornamento:** 2026-05-25  
**Testato con:** Aspose.CAD for Java 24.10  
**Autore:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutorial correlati

- [Converti CAD in PDF con Aspose.CAD per Java – Tutorial completi](/cad/java/)
- [Crea PDF da CAD – Esporta DXF in PDF con Aspose.CAD per Java](/cad/java/additional-features/export-dxf-to-pdf/)
- [Imposta dimensione canvas – Funzionalità CAD avanzate con Aspose.CAD per Java](/cad/java/advanced-cad-features/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}