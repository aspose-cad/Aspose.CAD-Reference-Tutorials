---
date: 2026-01-10
description: Impara a leggere i file DWG e a creare entità multileader DWG usando
  Aspose.CAD per Java in questo tutorial passo‑passo.
linktitle: Support MLeader Entity for DWG Format with Java
second_title: Aspose.CAD Java API
title: Come leggere DWG e supportare MLeader con Aspose.CAD per Java
url: /it/java/cad-text-and-formatting/support-mleader-entity/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come leggere DWG e supportare MLeader con Aspose.CAD per Java

## Introduzione

Se hai bisogno di **leggere file DWG** e lavorare con entità **multileader DWG** in un'applicazione Java, sei nel posto giusto. Aspose.CAD per Java ti offre un modo pulito e programmatico per aprire disegni DWG, ispezionare oggetti MLeader e convalidare le loro proprietà, il tutto senza richiedere una workstation CAD completa. In questo tutorial percorreremo ogni passaggio, dal caricamento di un file DWG alla conferma che i dati del multileader corrispondano allo stile previsto.

## Risposte rapide
- **Cosa comporta “come leggere dwg”?** Caricare il DWG con `Image.load()` e fare cast a `CadImage`.
- **Posso creare entità dwg multileader?** Sì – è possibile aggiungere, modificare e convalidare oggetti MLeader usando l'API CadMLeader.
- **Quale versione della libreria è necessaria?** Qualsiasi versione recente di Aspose.CAD per Java (l'API mostrata funziona con le build 2024+).
- **È necessaria una licenza per lo sviluppo?** Una licenza temporanea è sufficiente per i test; è necessaria una licenza completa per la produzione.
- **Il codice è cross‑platform?** Assolutamente – Java gira su Windows, Linux e macOS.

## Che cosa significa “come leggere dwg” con Aspose.CAD?

Leggere un file DWG significa convertire il disegno binario in un oggetto `CadImage` in memoria. Una volta ottenuto tale oggetto, è possibile enumerare le sue entità (linee, cerchi, testo, oggetti **MLeader**, ecc.) e ispezionarne le proprietà.

## Perché supportare le entità MLeader?

Gli oggetti MLeader (multileader) combinano linee leader con testo o blocchi allegati, rendendoli essenziali per le annotazioni nei disegni ingegneristici. Supportarli ti consente di:

- Verificare che le annotazioni rispettino gli standard aziendali.
- Estrarre il testo per elaborazioni successive (ad esempio, generazione di distinte base).
- Modificare programmaticamente gli stili leader o sostituire il contenuto dei blocchi.

## Prerequisiti

Prima di iniziare, assicurati di avere:

1. **Ambiente di sviluppo Java** – JDK 11+ e il tuo IDE preferito (IntelliJ, Eclipse, VS Code).  
2. **Aspose.CAD per Java** – Scarica l'ultimo JAR dal [download link](https://releases.aspose.com/cad/java/).  

## Importare gli spazi dei nomi

Aggiungi i seguenti import alla tua classe Java per lavorare con le entità DWG e le opzioni di rasterizzazione:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeader;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeaderContextData;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeaderLine;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeaderNode;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Come leggere file DWG usando Aspose.CAD per Java

### Passo 1: Caricare il file DWG e ottenere un `CadImage`

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String file = dataDir + "Multileaders.dwg";
Image image = Image.load(file);
CadImage cadImage = (CadImage) image;
```

### Passo 2: Convalidare che il disegno contenga entità MLeader

```java
Assert.areNotEqual(cadImage.getEntities().length, 0);
CadMLeader cadMLeader = (CadMLeader) cadImage.getEntities()[2];
```

### Passo 3: Verificare lo stile MLeader e gli attributi di base

```java
Assert.areEqual(cadMLeader.getStyleDescription(), "Standard");
Assert.areEqual(cadMLeader.getLeaderStyleId(), "12E");
Assert.areEqual(cadMLeader.getArrowHeadId1(), "639");
Assert.areEqual(cadMLeader.getLeaderLineTypeID(), "14");
```

### Passo 4: Accedere ai dati di contesto MLeader (il cuore del multileader)

```java
CadMLeaderContextData context = cadMLeader.getContextData();
```

### Passo 5: Convalidare gli attributi a livello di contesto

```java
Assert.areEqual(context.getArrowHeadSize(), 30.0, 0.1);
Assert.areEqual(context.getBasePoint().getX(), 481, 1);
Assert.areEqual(context.getContentScale(), 1.0, 0.01);
Assert.areEqual(context.getDefaultText().getValue(),
    "This is multileader with huge text\\P{\\H1.5x;6666666666666666666666666666\\P}bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb");
Assert.areEqual(context.hasMText(), true);
```

### Passo 6: Lavorare con il nodo MLeader e la sua linea leader

```java
CadMLeaderNode mleaderNode = context.getLeaderNode();
Assert.areEqual(mleaderNode.getLastLeaderLinePoint().getX(), 473, 1);

CadMLeaderLine leaderLine = mleaderNode.getLeaderLine();
Assert.areEqual(leaderLine.getBreakEndPoint().toString(), null);
Assert.areEqual(Integer.toString(leaderLine.getBreakPointIndex().getValue()), Integer.toString(0));
Assert.areEqual(leaderLine.getBreakStartPoint().toString(), null);
Assert.areEqual(Integer.toString(leaderLine.getLeaderLineIndex().getValue()), Integer.toString(0));
Assert.areEqual(Integer.toString(leaderLine.getLeaderPoints().size()), Integer.toString(4));
```

### Passo 7: Convalidare gli attributi aggiuntivi del nodo MLeader

```java
Assert.areEqual(Integer.toString(mleaderNode.getBranchIndex()), Integer.toString(0));
Assert.areEqual(mleaderNode.getDogLegLength(), 8.0, 0.1);
Assert.areEqual(context.hasMText(), true);
```

### Passo 8: Controllare le proprietà relative al testo

```java
Assert.areEqual(context.getTextAttachmentType().getValue(), (short) 1);
Assert.areEqual(context.getTextBackgroundColor().getValue(), 18);
Assert.areEqual(context.getTextHeight(), 20.0, 0.1);
Assert.areEqual(context.getTextStyleID().getValue(), "11");
Assert.areEqual(context.getTextRotation().getValue(), 0.0, 0.01);
```

### Passo 9: Revisionare gli altri attributi MLeader per completezza

```java
Assert.areEqual(cadMLeader.getArrowHeadId1(), "639");
Assert.areEqual(cadMLeader.getLeaderType(), 1);
Assert.areEqual(cadMLeader.getBlockContentColor(), 0);
Assert.areEqual(cadMLeader.getLeaderLineColor(), 0);
Assert.areEqual(cadMLeader.getTextHeight(), 1.0, 0.01);
```

## Problemi comuni e soluzioni

| Problema | Perché accade | Soluzione |
|----------|---------------|-----------|
| `ClassCastException` durante il cast dell'entità | L'indice selezionato non è un oggetto MLeader. | Verificare `cadImage.getEntities()[i] instanceof CadMLeader` prima del cast. |
| `null` valori per i punti della linea leader | Il disegno utilizza uno stile leader personalizzato non completamente supportato. | Usare l'ultima versione di Aspose.CAD o ricorrere allo stile predefinito per i test. |
| Fallimenti di asserzione su valori numerici | Leggere differenze di arrotondamento tra versioni CAD. | Regolare la tolleranza in `Assert.areEqual(..., delta)` come mostrato negli esempi. |

## Domande frequenti

**D: Posso usare Aspose.CAD per Java con altri formati CAD?**  
R: Sì, Aspose.CAD supporta DXF, DWF, DGN e diversi formati raster oltre a DWG.

**D: Dove posso trovare la documentazione dettagliata per Aspose.CAD per Java?**  
R: Consulta la documentazione ufficiale [documentation](https://reference.aspose.com/cad/java/) per i dettagli dell'API e gli esempi di codice.

**D: È disponibile una versione di prova gratuita?**  
R: Assolutamente – puoi scaricare una trial dalla pagina [free trial](https://releases.aspose.com/).

**D: Come posso ottenere una licenza temporanea per i test?**  
R: Ottieni una licenza temporanea tramite il [temporary license link](https://purchase.aspose.com/temporary-license/).

**D: Dove posso chiedere aiuto alla community?**  
R: Il [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) è il posto migliore per condividere domande e soluzioni.

## Conclusione

Ora hai a disposizione una guida completa, passo dopo passo, per **leggere file DWG** e **creare entità DWG multileader** usando Aspose.CAD per Java. Seguendo i passaggi sopra, potrai convalidare gli stili MLeader, estrarre dati di annotazione e integrare l'elaborazione DWG in qualsiasi flusso di lavoro basato su Java.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Ultimo aggiornamento:** 2026-01-10  
**Testato con:** Aspose.CAD 24.11 per Java  
**Autore:** Aspose