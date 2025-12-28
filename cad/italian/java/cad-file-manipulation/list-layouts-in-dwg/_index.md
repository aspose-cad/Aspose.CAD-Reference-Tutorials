---
date: 2025-12-28
description: Scopri come leggere i file DWG usando Aspose.CAD per Java e elenca facilmente
  i layout nei file DWG. Integra potenti funzionalità CAD nelle tue applicazioni Java.
linktitle: List Layouts in DWG
second_title: Aspose.CAD Java API
title: Come leggere i file DWG e elencare i layout in DWG utilizzando Aspose.CAD per
  Java
url: /it/java/cad-file-manipulation/list-layouts-in-dwg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come leggere i file DWG e elencare i layout in DWG usando Aspose.CAD per Java

## Introduzione

Se hai bisogno di **leggere i file DWG** programmaticamente ed estrarre informazioni come i nomi dei layout, Aspose.CAD per Java lo rende semplice. In questo tutorial passo‑a‑passo ti mostreremo **come leggere i DWG** e elencare tutti i layout contenuti in un file DWG (o DXF). Alla fine della guida sarai in grado di aggiungere questa funzionalità a qualsiasi applicazione Java che lavora con dati CAD.

## Risposte rapide
- **Quale libreria è necessaria?** Aspose.CAD per Java.
- **Posso leggere i file DWG su qualsiasi OS?** Sì – Java è cross‑platform.
- **È necessaria una licenza per eseguire il campione?** Una versione di prova gratuita è sufficiente per la valutazione; è necessaria una licenza per la produzione.
- **Quali formati CAD sono supportati?** DWG, DXF, DWF e altri.
- **Il codice è compatibile con Java 8+?** Assolutamente.

## Cos'è “come leggere dwg” in Java?

Leggere un file DWG significa caricare i dati CAD binari in un modello di oggetti che puoi interrogare. Aspose.CAD astrae la complessa struttura DWG dietro classi .NET/Java semplici, permettendoti di concentrarti sulle informazioni di cui hai bisogno – in questo caso, i nomi dei layout.

## Perché elencare i layout in un file DWG?

Un DWG può contenere più layout (paper space, model space, fogli personalizzati). Conoscere i nomi dei layout ti permette di:
- Generare report per layout.
- Esportare layout specifici in immagini o PDF.
- Automatizzare l'elaborazione batch dei disegni.

## Prerequisiti

Prima di immergerci nel codice, verifica di avere quanto segue:

- **Aspose.CAD per Java Library** – scarica l'ultimo JAR dal [sito web](https://releases.aspose.com/cad/java/).
- **Ambiente di sviluppo Java** – JDK 8 o superiore, e un IDE o strumento di build a tua scelta.

## Importare i namespace

Nel tuo file sorgente Java, importa le classi Aspose.CAD necessarie:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.CadLayoutDictionary;
import com.aspose.cad.fileformats.cad.cadobjects.CadLayout;
```

## Passo 1: Configura la tua directory dei documenti

Sostituisci **“Your Document Directory”** con il percorso assoluto dove risiedono i tuoi file CAD.

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

## Passo 2: Carica il file DWG

Il metodo `Image.load` rileva automaticamente il formato del file, così puoi usare lo stesso codice sia per i file **DWG** che **DXF**.

```java
String sourceFilePath = dataDir + "conic_pyramid.dxf";
Image image = Image.load(sourceFilePath);
CadImage cadImage = (CadImage)image;
```

## Passo 3: Ottieni i layout e stampa i nomi

Il ciclo itera su ogni oggetto layout e stampa il suo nome sulla console – un modo semplice per verificare di aver **letto il DWG** e estratto le informazioni sui layout.

```java
CadLayoutDictionary layouts = cadImage.getLayouts();
for (CadLayout layout : layouts.getValues())
{
    System.out.println("Layout " + layout.getLayoutName());
}
```

## Problemi comuni e consigli

- **Percorso file errato** – Verifica che `dataDir` termini con un separatore (`/` o `\\`) appropriato per il tuo OS.
- **Versione DWG non supportata** – Assicurati di utilizzare una versione recente di Aspose.CAD; le versioni DWG più vecchie potrebbero richiedere conversione.
- **Utilizzo della memoria** – I disegni di grandi dimensioni possono consumare molta memoria. Rilascia l'oggetto `CadImage` quando hai finito: `cadImage.dispose();`.

## Conclusione

Congratulazioni! Ora sai **come leggere i DWG** e elencare i loro layout usando Aspose.CAD per Java. Questa tecnica costituisce la base per automazioni CAD più avanzate, come l'esportazione di layout specifici in immagini o PDF. Per approfondire, consulta la [documentazione](https://reference.aspose.com/cad/java/) ufficiale.

## FAQ

### Q1: Posso usare Aspose.CAD per Java con altri formati di file CAD?

A1: Sì, Aspose.CAD supporta vari formati CAD, inclusi DWG, DXF, DWF e altri.

### Q2: È disponibile una versione di prova gratuita per Aspose.CAD per Java?

A2: Sì, puoi ottenere una versione di prova gratuita da [qui](https://releases.aspose.com/).

### Q3: Dove posso ottenere supporto dalla community per Aspose.CAD per Java?

A3: Visita il [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) per il supporto della community.

### Q4: Come posso acquistare una licenza per Aspose.CAD per Java?

A4: Puoi acquistare una licenza dalla [pagina di acquisto](https://purchase.aspose.com/buy).

### Q5: Posso usare una licenza temporanea per scopi di test?

A5: Sì, puoi ottenere una licenza temporanea [qui](https://purchase.aspose.com/temporary-license/).

**Domande aggiuntive**

**Q: Questo approccio funziona per leggere file DWG su Linux?**  
A: Assolutamente. Poiché la soluzione è pure Java, funziona su qualsiasi OS con un JDK compatibile.

**Q: Posso leggere un file DWG senza caricare l'intero disegno in memoria?**  
A: Aspose.CAD carica il disegno in memoria; per file molto grandi considera di elaborarli in thread separati o usare API di streaming se disponibili in future versioni.

**Q: Esiste un modo per filtrare i layout per nome?**  
A: Sì – dopo aver recuperato il `CadLayoutDictionary`, puoi verificare `layout.getLayoutName().equalsIgnoreCase("MyLayout")` prima di elaborare.

---

**Last Updated:** 2025-12-28  
**Tested With:** Aspose.CAD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}