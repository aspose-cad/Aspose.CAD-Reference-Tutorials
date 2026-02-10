---
date: 2025-12-28
description: Scopri come personalizzare i caratteri nei disegni DWG con Aspose.CAD
  per Java. Guida passo‑passo per aggiungere testo, sostituire i caratteri e perfezionare
  le annotazioni CAD.
linktitle: CAD Text and Annotation
second_title: Aspose.CAD Java API
title: Come personalizzare i caratteri nel testo e nelle annotazioni CAD
url: /it/java/cad-text-and-annotation/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come personalizzare i font in CAD Text e Annotation

## Introduzione

Se stai cercando di **come personalizzare i caratteri** nei tuoi disegni DWG, sei nel posto giusto. In questo tutorial ti guideremo attraverso l'aggiunta di testo, la sostituzione dei font e la regolazione degli stili dei font utilizzando Aspose.CAD per Java. Che tu stia rifinendo uno schema, preparando documenti di costruzione, o semplicemente voglia annotazioni di testo dwg più chiare, questi passaggi ti aiuteranno a ottenere una finitura professionale rapidamente e in modo affidabile.

## Risposte rapide
- **Qual è lo scopo principale della personalizzazione dei font in DWG?** Migliorare la leggibilità e corrispondere al branding o agli standard del progetto.
- **Quale libreria gestisce le modifiche?** Aspose.CAD per Java.
- **Ho bisogno di una licenza?** Una prova gratuita è sufficiente per la valutazione; è necessaria una licenza commerciale per la produzione.
- **Posso elaborare file DWG di grandi dimensioni?** Sì – l'API trasmette i dati in modo efficiente, adatto a disegni di grandi dimensioni.
- **È necessario software aggiuntivo?** Solo un runtime Java (JDK8o successivo) e il JAR di Aspose.CAD.

## Cos'è "come personalizzare i caratteri" in CAD?
Personalizzare i font significa sostituire lo stile di testo predefinito in un file DWG con un font a tua scelta, regolandone dimensione, peso o applicando uno stile diverso a layer o oggetti specifici. Questo garantisce che il disegno appaia esattamente come desideri su tutti i visualizzatiri.

## Perché utilizzare Aspose.CAD per Java per personalizzare i caratteri?
- **Controllo completo** sugli oggetti di testo senza aprire il disegno in un editor GUI.
- **Elaborazione batch** – gestisci decine di file con uno script unico.
- **Multipiattaforma** – funziona su Windows, Linux e macOS.
- **Nessuna dipendenza esterna** – l'API gestisce l'analisi DWG internamente.

## Prerequisiti
- Java Development Kit8o successivo installato.
- JAR di Aspose.CAD per Java aggiunto al classpath del tuo progetto.
- Un file DWG che desideri modificare.

## Come aggiungere testo in DWG
Aggiungere nuove informazioni testuali è una necessità comune quando vuoi etichettare parti, aggiungere note o creare **dwg text annotation**. Segui questi passaggi:

1. **Carica il file DWG** utilizzando `CadImage`.
2. **Crea un'entità `CadText`** con la stringa desiderata, la posizione e il font.
3. **Aggiungi l'entità** alla collezione di entità del disegno.
4. **Salva** il file modificato.

> *Nota: Lo snippet di codice reale è invariato rispetto al tutorial originale ed è incluso nel sotto‑tutorial collegato.*

## Come sostituire il carattere in DWG
Sostituire un font esistente in tutto il disegno aiuta a mantenere la coerenza, soprattutto quando il font originale non è disponibile sul sistema di destinazione.

1. **Apri il DWG** con `CadImage`.
2. **Itera** su tutti gli oggetti `CadText`.
3. **Imposta la proprietà `FontName`** sul font preferito (es. “Arial”).
4. **Salva** il disegno aggiornato.

Questo metodo è trattato in dettaglio nel sotto‑tutorial “Carattere sostitutivo in DWG”.

## Come modificare lo stile del carattere DWG per uno stile particolare
A volte solo uno stile di testo specifico (es. “Titolo”) necessita di un nuovo font mentre gli altri rimangono invariati.

1. **Identifica il nome dello stile** che desideri modificare.
2. **Trova l'oggetto `CadTextStyle` corrispondente**.
3. **Aggiorna il suo `FontName`** e eventuali attributi di stile aggiuntivi.
4. **Conserva le modifiche** salvando il file.

La guida passo‑passo è disponibile nel sotto‑tutorial “Font sostitutivo di uno stile particolare in DWG”.

## Casi d'uso comuni
- **Disegni di costruzione** dove i font standard dell'azienda sono obbligatori.
- **Piani architettonici** che necessitano di annotazioni leggibili per i clienti.
- **Conversione batch** di file DWG legacy a un nuovo set di font aziendali.

## Tutorial su testo CAD e annotazioni
### [Aggiungi testo in DWG utilizzando Aspose.CAD per Java](./add-text-in-dwg/)
Migliora i tuoi disegni DWG senza sforzo con Aspose.CAD per Java. Aggiungi testo senza problemi con la nostra guida passo‑passo.

### [Sostituisci il carattere in DWG con Aspose.CAD per Java](./substitute-font-in-dwg/)
Migliora i tuoi progetti CAD senza sforzo. Impara a sostituire i caratteri nei file DWG utilizzando Aspose.CAD per Java. Guida passo-passo per una perfezione visiva.

### [Sostituisci il carattere di uno stile particolare in DWG utilizzando Aspose.CAD per Java](./substitute-font-of-particular-style-in-dwg/)
Impara a sostituire i caratteri nei file DWG utilizzando Aspose.CAD per Java. Guida passo‑passo per personalizzare gli stili con precisione.

## Domande frequenti

**D: Posso usare questi metodi con file DWG creati nelle versioni più vecchie di AutoCAD?**
R: Sì. Aspose.CAD supporta le versioni DWG da R12 fino alle ultime release.

**D: Cosa succede se il font di destinazione non è installato sulla macchina dell'utente?**
R: Il disegno tornerà a un font predefinito, il che può influenzare sul layout. Si consiglia di incorporare il font o assicurarsi che sia installato su tutte le macchine.

**D: È possibile sostituire i font solo su un livello specifico?**
R: Assolutamente. Filtra gli oggetti `CadText` per il loro `LayerName` prima di cambiare il `FontName`.

**D: Devo ricostruire il disegno dopo le modifiche ai font?**
R: Non è necessaria alcuna ricostruzione manuale; salvando il `CadImage` vengono scritti tutti gli aggiornamenti nel file.

**D: Come posso verificare che la modifica del font sia stata applicata correttamente?**
R: Apri il DWG in qualsiasi visualizzatore che supporta il font scelto, oppure elenca programmaticamente gli oggetti `CadText` per leggere nuovamente il `FontName`.

---

**Ultimo aggiornamento:** 28-12-2025
**Testato con:** Aspose.CAD per Java 24.12
**Autore:** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
