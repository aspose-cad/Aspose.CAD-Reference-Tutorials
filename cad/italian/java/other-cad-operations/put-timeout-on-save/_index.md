---
date: 2026-01-22
description: Scopri come impostare il timeout durante il salvataggio di CAD in PDF
  usando Aspose.CAD per Java. Migliora le prestazioni con questa guida passo‑passo.
linktitle: Put Timeout on Save
second_title: Aspose.CAD Java API
title: Come impostare il timeout durante il salvataggio per CAD con Aspose.CAD
url: /it/java/other-cad-operations/put-timeout-on-save/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Timeout durante il salvataggio per CAD con Aspose.CAD

## Introduzione

Benvenuti al tutorial su **come impostare il timeout** durante il salvataggio di diseg In questa guida, vi accompagneremo nel processo di configurazione di un timeout per l'operazione di salvataggio, che aiuta a mantenere l'applicazione reattiva e migliora le prestazioni complessive. Aspose.CAD per Java è una libreria potente che consente di lavorare con i file CAD in modo fluido.

## Risposte rapide
- **Che cosa fa il timeout?** Interrompe l'operazione di salvataggio se supera la durata specificata, evitando blocchi prolungati.  
- **Quale formato è usato nell'esempio?** Il disegno CAD viene salvato come file PDF.  
- **È necessaria una licenza?** È richiesta una licenza Aspose.CAD temporanea o permanente per l'uso in produzione.  
- **Quale versione di Java è supportata?** Il codice funziona con Java 8 e successive.  
- **Posso regolare la durata del timeout?** Sì—basta modificare il valore di `TimeUnit.SECONDS.sleep(...)`.

## Come impostare il timeout durante il salvataggio

### Che cos'è un timeout nel contesto di Aspose.CAD?
Un timeout è una misura di sicurezza che interrompe un processo di rasterizzazione o conversione prolungato. Fornendo un `InterruptionTokenSource`, è possibile segnalare alla libreria di abortire l'operazione dopo un periodo definito, garantendo che l'applicazione rimanga reattiva.

### Perché impostare un timeout quando si salva CAD in PDF?
Salvare disegni CAD grandi o complessi può consumare notevoli risorse CPU e memoria. Aggiungere un timeout:
- Previene il blocco dell'applicazione.  
- Consente di gestire i compiti a lunga durata in modo elegante.  
- Migliora l'esperienza utente complessiva, specialmente in ambienti web o basati su interfaccia utente.

## Prerequisiti

- **Aspose.CAD for Java Library** – Assicurati di aver integrato la libreria nel tuo progetto. Puoi scaricare la libreria dal [sito web](https://releases.aspose.com/cad/java/).  
- **Development Environment** – Un IDE Java (IntelliJ, Eclipse, ecc.) con JDK 8+ installato.

## Importare i pacchetti

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterruptionTokenSource;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.concurrent.TimeUnit;
```

Ora, analizziamo il codice di esempio passo dopo passo:

## Passo 1: Impostare le directory di origine e di output

```java
final String SourceDir = Utils.getDataDir_DWGDrawings();
final String OutputDir = Utils.getDataDir_Output();
```

Assicurati di avere le directory di origine e di output corrette per i tuoi disegni CAD.

## Passo 2: Creare un Interruption Token Source

```java
final InterruptionTokenSource source = new com.aspose.cad.InterruptionTokenSource();
```

Inizializza un token di interruzione per gestire le interruzioni durante l'operazione di salvataggio.

## Passo 3: Caricare il disegno CAD

```java
final CadImage cadImageBig = (CadImage)Image.load(SourceDir + "Drawing11.dwg");
```

Carica il disegno CAD in un oggetto `CadImage`.

## Passo 4: Configurare le opzioni di rasterizzazione

```java
CadRasterizationOptions rasterizationOptionsBig = new CadRasterizationOptions();
rasterizationOptionsBig.setPageWidth(cadImageBig.getSize().getWidth() / 2);
rasterizationOptionsBig.setPageHeight(cadImageBig.getSize().getHeight() / 2);
```

Configura le opzioni di rasterizzazione per il disegno CAD.

## Passo 5: Configurare le opzioni PDF

```java
final PdfOptions CADfBig = new PdfOptions();
CADfBig.setVectorRasterizationOptions(rasterizationOptionsBig);
CADfBig.setInterruptionToken(source.getToken());
```

Imposta le opzioni PDF con le opzioni di rasterizzazione vettoriale e il token di interruzione.

## Passo 6: Salvare il disegno con timeout

```java
cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
```

Salva il disegno CAD in un file PDF con il timeout specificato.

## Passo 7: Gestire l'interruzione

```java
java.lang.Thread thread = new java.lang.Thread(new Runnable() {
    @Override
    public void run() {
        try {
            cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
        } catch (Throwable th) {
            System.out.println("interrupted !!!");
        }
    }
});
thread.start();
TimeUnit.SECONDS.sleep(3);
source.interrupt();
thread.join();
```

Crea un thread per gestire l'operazione di salvataggio e interromperla dopo un timeout specificato.

## Problemi comuni e risoluzione

- **Timeout troppo breve** – Se il disegno è grande, un timeout molto breve può abortire l'operazione prima che termini. Aumenta la durata del sleep o regola le impostazioni di rasterizzazione.  
- **Licenza mancante** – Eseguire senza una licenza valida genererà un'eccezione. Applica una licenza temporanea o permanente prima di eseguire il codice.  
- **Percorsi errati** – Assicurati che `SourceDir` e `OutputDir` puntino a cartelle esistenti; altrimenti, `Image.load` o `save` falliranno.

## Domande frequenti

**D: Come posso scaricare Aspose.CAD per Java?**  
R: Puoi scaricarlo dalla [pagina delle release](https://releases.aspose.com/cad/java/).

**D: Dove posso trovare la documentazione per Aspose.CAD per Java?**  
R: Consulta la [documentazione](https://reference.aspose.com/cad/java/) per informazioni complete.

**D: È disponibile una prova gratuita?**  
R: Sì, puoi ottenere una prova gratuita da [questo link](https://releases.aspose.com/).

**D: Come posso ottenere una licenza temporanea?**  
R: Visita [questo link](https://purchase.aspose.com/temporary-license/) per i dettagli sulla licenza temporanea.

**D: Hai bisogno di aiuto o hai domande?**  
R: Vai al [forum di Aspose.CAD](https://forum.aspose.com/c/cad/19) per il supporto della community.

## Conclusione

Congratulazioni! Ora sai **come impostare il timeout** sulle operazioni di salvataggio quando converti disegni CAD in PDF utilizzando Aspose.CAD per Java. Implementare questo timeout migliora l'affidabilità e la reattività delle tue applicazioni legate al CAD.

---

**Ultimo aggiornamento:** 2026-01-22  
**Testato con:** Aspose.CAD for Java 24.11 (latest)  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}