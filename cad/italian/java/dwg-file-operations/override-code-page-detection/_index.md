---
date: 2026-01-12
description: Scopri come esportare CAD in PDF sovrascrivendo il rilevamento automatico
  della pagina di codice nei file DWG usando Aspose.CAD per Java. Gestisce la codifica
  e i CIF/MIF malformati.
linktitle: Override Automatic Code Page Detection in DWG Files
second_title: Aspose.CAD Java API
title: Esporta CAD in PDF – Sovrascrivi il rilevamento automatico della pagina di
  codice nei file DWG con Java
url: /it/java/dwg-file-operations/override-code-page-detection/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Esportare CAD in PDF – Sovrascrivere il Rilevamento Automatico della Pagina di Codice nei File DWG con Java

## Introduzione

In questa guida completa scoprirai **come esportare CAD in PDF** sovrascrivendo il rilevamento automatico della pagina di codice che può corrompere il testo nei file DWG. Aspose.CAD per Java ti offre un controllo dettagliato sulla codifica, consentendoti di recuperare dati CIF/MIF malformati e produrre un output PDF affidabile. Che tu stia creando un convertitore batch o integrando l'elaborazione CAD in una più ampia applicazione Java, i passaggi seguenti ti guideranno attraverso l'intero flusso di lavoro.

## Risposte Rapide
- **Cosa significa “sovrascrivere la pagina di codice”?** Forza Aspose.CAD a utilizzare una codifica dei caratteri specifica invece di indovinare.
- **Posso esportare DWG direttamente in PDF?** Sì – dopo aver impostato la pagina di codice corretta, puoi salvare l'immagine CAD come PDF.
- **Quale codifica funziona per il testo giapponese?** `CodePages.Japanese` e `MifCodePages.Japanese` sono le scelte giuste.
- **È necessaria una licenza per l'uso in produzione?** È richiesta una licenza commerciale; è disponibile una licenza temporanea per i test.
- **Quale versione di Aspose.CAD è necessaria?** Qualsiasi versione recente che supporti `LoadOptions` e `PdfOptions`.

## Che cosa è “esportare CAD in PDF”?
Esportare CAD in PDF converte i disegni CAD basati su vettori in un formato documento a layout fisso ampiamente supportato. Il PDF risultante preserva linee, livelli e testo, rendendo il disegno facile da condividere, stampare o incorporare in altre applicazioni.

## Perché sovrascrivere il rilevamento automatico della pagina di codice?
I file DWG spesso memorizzano il testo usando pagine di codice legacy. L'auto‑rilevamento di Aspose.CAD può interpretare erroneamente questi byte, generando caratteri illeggibili. Specificando manualmente la pagina di codice garantisci che il testo appaia esattamente come previsto nel PDF esportato, soprattutto per script non latini come giapponese, cirillico o arabo.

## Prerequisiti
- **Ambiente di sviluppo Java** – JDK 8+ e il tuo IDE preferito.
- **Aspose.CAD per Java** – Scarica la libreria dal sito ufficiale [qui](https://releases.aspose.com/cad/java/).
- **File di esempio DWG** – Usa il file `SimpleEntities.dwg` fornito o qualsiasi DWG che desideri convertire.

## Importare i pacchetti
Nel tuo progetto Java, importa le classi necessarie di Aspose.CAD:

```java
import com.aspose.cad.CodePages;
import com.aspose.cad.Image;
import com.aspose.cad.LoadOptions;
import com.aspose.cad.MifCodePages;
import com.aspose.cad.fileformats.cad.CadImage;
```

## Guida passo‑passo

### Passo 1: Configurare il progetto Java
Crea un nuovo progetto Maven o Gradle e aggiungi il JAR di Aspose.CAD al classpath. Questo passaggio assicura che l'IDE possa risolvere le classi importate.

### Passo 2: Caricare il file DWG con una pagina di codice specificata
Indica ad Aspose.CAD quale codifica utilizzare e se tentare il recupero di dati CIF/MIF malformati.

```java
String SourceDir = "Your Document Directory";
String dwgPathToFile = SourceDir + "SimpleEntites.dwg";
LoadOptions opts = new LoadOptions();
opts.setSpecifiedEncoding(CodePages.Japanese);
opts.setSpecifiedMifEncoding(MifCodePages.Japanese);
opts.setRecoverMalformedCifMif(false);
CadImage cadImage = (CadImage) Image.load(dwgPathToFile, opts);
```

### Passo 3: Esportare l’immagine CAD in PDF
Con la pagina di codice corretta applicata, puoi esportare in sicurezza il disegno. L'oggetto `PdfOptions` ti permette di affinare l'output PDF (compressione, rasterizzazione, ecc.).

```java
// Perform export or other operations with cadImage
// For example, exporting to PDF
PdfOptions pdfOptions = new PdfOptions();
cadImage.save("output.pdf", pdfOptions);
```

### Passo 4: Verificare il successo
Un semplice messaggio sulla console conferma che il processo è terminato senza eccezioni.

```java
System.out.println("OverrideAutomaticCodePageDetectionDwg executed successfully");
```

Puoi ripetere questi passaggi per più file DWG, modificando il percorso di origine e il nome di output secondo necessità.

## Problemi comuni e soluzioni
- **Appaiono ancora caratteri spazzatura:** Verifica che `specifiedEncoding` corrisponda alla pagina di codice originale del DWG. Usa un enum `CodePages` diverso se necessario.
- **`NullPointerException` su `cadImage.save`:** Assicurati che il file DWG venga caricato correttamente; controlla il percorso e i permessi del file.
- **La dimensione del PDF è elevata:** Abilita la compressione in `PdfOptions` (ad esempio, `pdfOptions.setCompress(true)`).

## Domande frequenti

**D1: Aspose.CAD è compatibile con tutte le versioni dei file DWG?**  
R1: Aspose.CAD supporta un'ampia gamma di versioni DWG, incluse AutoCAD 2018 e versioni precedenti.

**D2: Posso usare Aspose.CAD per progetti commerciali?**  
R2: Sì, è necessaria una licenza commerciale per l'uso in produzione. Puoi ottenere una licenza [qui](https://purchase.aspose.com/buy).

**D3: Ci sono limitazioni nella versione di prova gratuita?**  
R3: La versione di prova impone restrizioni di dimensione e funzionalità; consulta la documentazione ufficiale per i dettagli.

**D4: Come posso ottenere supporto per Aspose.CAD?**  
R4: Visita la community [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) per assistenza e discussioni.

**D5: È disponibile una licenza temporanea per scopi di test?**  
R5: Sì, una licenza temporanea può essere richiesta [qui](https://purchase.aspose.com/temporary-license/).

---

**Ultimo aggiornamento:** 2026-01-12  
**Testato con:** Aspose.CAD per Java 24.11 (ultima al momento della stesura)  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}