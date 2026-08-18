---
date: 2026-02-28
description: Scopri come leggere i file DWG usando Aspose.CAD per Java ed elenca facilmente
  i layout nei file DWG. Integra potenti funzionalità CAD nelle tue applicazioni Java.
linktitle: List Layouts in DWG
second_title: Aspose.CAD Java API
title: Come leggere DWG e elencare i layout in DWG usando Aspose.CAD per Java
url: /it/java/cad-file-manipulation/list-layouts-in-dwg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come leggere i file DWG e elencare i layout in DWG usando Aspose.CAD per Java

## Introduzione

Se stai cercando un modo affidabile **come leggere dwg** i file in modo programmatico, Aspose.CAD per Java fornisce un'API pulita e cross‑platform che ti consente di caricare un disegno e estrarre qualsiasi informazione di cui hai bisogno — come i nomi di tutti i layout all'interno del file. In questo tutorial passo‑a‑passo ti mostreremo **come leggere DWG** e elencare ogni layout contenuto in un file DWG (o DXF), così potrai integrare questa funzionalità in qualsiasi applicazione Java che lavora con dati CAD.

## Risposte rapide
- **Quale libreria è necessaria?** Aspose.CAD for Java.  
- **Posso leggere i file DWG su qualsiasi OS?** Sì – Java è cross‑platform, quindi puoi **leggere dwg su linux** così facilmente come su Windows.  
- **È necessaria una licenza per eseguire il campione?** Una prova gratuita è sufficiente per la valutazione; è necessaria una licenza per la produzione.  
- **Quali formati CAD sono supportati?** DWG, DXF, DWF e altri.  
- **Il codice è compatibile con Java 8+?** Assolutamente.

## Cos'è “come leggere dwg” in Java?

Leggere un file DWG significa caricare i dati CAD binari in un modello di oggetti che puoi interrogare. Aspose.CAD astrae la complessa struttura DWG dietro classi Java semplici, permettendoti di concentrarti sulle informazioni di cui hai bisogno — in questo caso, i nomi dei layout.

## Perché elencare i layout in un file DWG?

Un DWG può contenere più layout (paper space, model space, fogli personalizzati). Conoscere i nomi dei layout ti consente di:
- Generare report per layout.  
- Esportare layout specifici in immagini o PDF.  
- Automatizzare l'elaborazione batch dei disegni.  

## Prerequisiti

Prima di immergerci nel codice, verifica di avere quanto segue:
- **Libreria Aspose.CAD per Java** – scarica l'ultimo JAR dal [sito web](https://releases.aspose.com/cad/java/).  
- **Ambiente di sviluppo Java** – JDK 8 o superiore, e un IDE o strumento di build a tua scelta.

## Importare gli spazi dei nomi

Nel tuo file sorgente Java, importa le classi Aspose.CAD necessarie:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.CadLayoutDictionary;
import com.aspose.cad.fileformats.cad.cadobjects.CadLayout;
```

## Passo 1: Configura la directory dei documenti

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

Sostituisci **“Your Document Directory”** con il percorso assoluto in cui risiedono i tuoi file CAD. Su Linux potresti usare un percorso come `/home/user/cad/`.

## Passo 2: Carica il file DWG

```java
String sourceFilePath = dataDir + "conic_pyramid.dxf";
Image image = Image.load(sourceFilePath);
CadImage cadImage = (CadImage)image;
```

Il metodo `Image.load` rileva automaticamente il formato del file, quindi lo stesso codice funziona sia per i file **DWG** che **DXF**.

## Passo 3: Ottieni i layout e stampa i nomi

```java
CadLayoutDictionary layouts = cadImage.getLayouts();
for (CadLayout layout : layouts.getValues())
{
    System.out.println("Layout " + layout.getLayoutName());
}
```

Il ciclo itera su ogni oggetto layout e stampa il suo nome nella console — un modo semplice per verificare di aver **letto DWG** con successo e di aver estratto le informazioni sui layout.

## Come convertire DWG in PDF su Linux

Se in seguito devi trasformare un layout specifico in PDF, Aspose.CAD può renderizzare il layout in un'immagine e poi puoi usare Aspose.PDF (o qualsiasi altra libreria PDF) per inserire quell'immagine in un documento PDF. Il codice di conversione è identico su Linux perché l'API è puramente Java.

## Problemi comuni e consigli
- **Percorso file errato** – Verifica che `dataDir` termini con un separatore (`/` o `\\`) appropriato per il tuo OS.  
- **Versione DWG non supportata** – Assicurati di utilizzare una versione recente di Aspose.CAD; versioni DWG più vecchie potrebbero richiedere conversione.  
- **Uso della memoria** – Disegni di grandi dimensioni possono consumare molta memoria. Rilascia l'oggetto `CadImage` quando hai finito: `cadImage.dispose();`.  
- **Esecuzione su server headless** – Non sono richiesti componenti UI, quindi il codice funziona su server Linux senza ambiente grafico.

## Conclusione

Congratulazioni! Ora sai **come leggere dwg** e elencare i suoi layout usando Aspose.CAD per Java. Questa tecnica costituisce la base per un'automazione CAD più avanzata, come l'esportazione di layout specifici in immagini, PDF o persino la conversione di DWG in PDF su Linux. Per approfondire, consulta la [documentazione](https://reference.aspose.com/cad/java/) ufficiale.

## Domande frequenti

**Q1: Posso usare Aspose.CAD per Java con altri formati di file CAD?**  
A1: Sì, Aspose.CAD supporta vari formati CAD, inclusi DWG, DXF, DWF e altri.

**Q2: È disponibile una prova gratuita per Aspose.CAD per Java?**  
A2: Sì, puoi ottenere una prova gratuita da [qui](https://releases.aspose.com/).

**Q3: Dove posso ottenere supporto dalla community per Aspose.CAD per Java?**  
A3: Visita il [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) per il supporto della community.

**Q4: Come posso acquistare una licenza per Aspose.CAD per Java?**  
A4: Puoi acquistare una licenza dalla [pagina di acquisto](https://purchase.aspose.com/buy).

**Q5: Posso usare una licenza temporanea per scopi di test?**  
A5: Sì, puoi ottenere una licenza temporanea [qui](https://purchase.aspose.com/temporary-license/).

### Domande aggiuntive

**Q: Questo approccio funziona per leggere file DWG su Linux?**  
A: Assolutamente. Poiché la soluzione è puramente Java, funziona su qualsiasi OS con un JDK compatibile.

**Q: Posso leggere un file DWG senza caricare l'intero disegno in memoria?**  
A: Aspose.CAD carica il disegno in memoria; per file molto grandi considera di elaborarli in thread separati o di usare API di streaming se disponibili in future versioni.

**Q: Esiste un modo per filtrare i layout per nome?**  
A: Sì — dopo aver recuperato il `CadLayoutDictionary`, puoi verificare `layout.getLayoutName().equalsIgnoreCase("MyLayout")` prima di elaborare.

---

**Ultimo aggiornamento:** 2026-02-28  
**Testato con:** Aspose.CAD for Java 24.11  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}