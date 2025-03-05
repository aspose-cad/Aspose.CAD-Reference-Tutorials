---
title: Supporta MLeader Entity per il formato DWG con Aspose.CAD per Java
linktitle: Supporta MLeader Entity per il formato DWG con Java
second_title: API Java Aspose.CAD
description: Sblocca la potenza di Aspose.CAD per Java con il nostro tutorial passo passo sul supporto delle entità MLeader in formato DWG.
type: docs
weight: 12
url: /it/java/cad-text-and-formatting/support-mleader-entity/
---
## introduzione

Nel campo della progettazione assistita da computer (CAD) con Java, comprendere e implementare il supporto per le entità MLeader in formato DWG è una competenza preziosa. Aspose.CAD per Java fornisce una soluzione solida per tali attività, offrendo una serie di potenti strumenti e funzionalità. Questo tutorial ti guiderà attraverso il processo di supporto delle entità MLeader all'interno dei file DWG utilizzando Java con Aspose.CAD.

## Prerequisiti

Prima di approfondire il tutorial, assicurati di disporre dei seguenti prerequisiti:

1. Ambiente di sviluppo Java: assicurati di avere un ambiente di sviluppo Java configurato sul tuo sistema.

2.  Libreria Aspose.CAD: scarica e installa la libreria Aspose.CAD per Java da[Link per scaricare](https://releases.aspose.com/cad/java/).

## Importa spazi dei nomi

Nel tuo progetto Java, importa gli spazi dei nomi necessari per sfruttare in modo efficace le funzionalità di Aspose.CAD. Includi le seguenti righe nel tuo codice:

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

Ora, suddividiamo il codice in una guida passo passo per supportare le entità MLeader per il formato DWG utilizzando Java con Aspose.CAD.

## 1. Caricare il file DWG e accedere a CadImage

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String file = dataDir + "Multileaders.dwg";
Image image = Image.load(file);
CadImage cadImage = (CadImage) image;
```

## 2. Convalida delle entità MLeader

```java
Assert.areNotEqual(cadImage.getEntities().length, 0);
CadMLeader cadMLeader = (CadMLeader) cadImage.getEntities()[2];
```

### 3. Verifica lo stile e gli attributi di MLeader

```java
Assert.areEqual(cadMLeader.getStyleDescription(), "Standard");
Assert.areEqual(cadMLeader.getLeaderStyleId(), "12E");
Assert.areEqual(cadMLeader.getArrowHeadId1(), "639");
Assert.areEqual(cadMLeader.getLeaderLineTypeID(), "14");
```

## 4. Accedi ai dati contestuali di MLeader

```java
CadMLeaderContextData context = cadMLeader.getContextData();
```

## 5. Convalidare gli attributi del contesto

```java
Assert.areEqual(context.getArrowHeadSize(), 30.0, 0.1);
Assert.areEqual(context.getBasePoint().getX(), 481, 1);
Assert.areEqual(context.getContentScale(), 1.0, 0.01);
Assert.areEqual(context.getDefaultText().getValue(), "This is multileader with huge text\\P{\\H1.5x;6666666666666666666666666666\\P}bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb");
Assert.areEqual(context.hasMText(), true);
```

## 6. Accedi al nodo MLeader e alla linea direttrice

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

## 7. Convalida attributi MLeader aggiuntivi

```java
Assert.areEqual(Integer.toString(mleaderNode.getBranchIndex()), Integer.toString(0));
Assert.areEqual(mleaderNode.getDogLegLength(), 8.0, 0.1);
Assert.areEqual(context.hasMText(), true);
```

## 8. Convalida gli attributi del testo

```java
Assert.areEqual(context.getTextAttachmentType().getValue(), (short) 1);
Assert.areEqual(context.getTextBackgroundColor().getValue(), 18);
Assert.areEqual(context.getTextHeight(), 20.0, 0.1);
Assert.areEqual(context.getTextStyleID().getValue(), "11");
Assert.areEqual(context.getTextRotation().getValue(), 0.0, 0.01);
```

## 9. Attributi aggiuntivi di MLeader

```java
Assert.areEqual(cadMLeader.getArrowHeadId1(), "639");
Assert.areEqual(cadMLeader.getLeaderType(), 1);
Assert.areEqual(cadMLeader.getBlockContentColor(), 0);
Assert.areEqual(cadMLeader.getLeaderLineColor(), 0);
Assert.areEqual(cadMLeader.getTextHeight(), 1.0, 0.01);
```

## Conclusione

Congratulazioni! Hai esplorato con successo la guida completa sul supporto delle entità MLeader per il formato DWG utilizzando Java e Aspose.CAD. Questa funzionalità apre le porte a manipolazioni CAD avanzate e migliora il tuo toolkit di sviluppo Java.

## Domande frequenti

### Q1: posso utilizzare Aspose.CAD per Java con altri formati CAD?

A1: Sì, Aspose.CAD supporta vari formati CAD oltre DWG, offrendo versatilità nei tuoi progetti.

### Q2: Dove posso trovare la documentazione dettagliata per Aspose.CAD per Java?

 A2: Fare riferimento a[documentazione](https://reference.aspose.com/cad/java/) per approfondimenti sulle capacità di Aspose.CAD.

### Q3: È disponibile una prova gratuita?

 A3: Sì, esplora le funzionalità in prima persona con[prova gratuita](https://releases.aspose.com/).

### Q4: Come posso ottenere una licenza temporanea per Aspose.CAD?

A4: Ottieni una licenza temporanea tramite[questo link](https://purchase.aspose.com/temporary-license/).

### D5: Dove posso cercare supporto e assistenza da parte della comunità?

A5: Visita il[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) per connettersi con la comunità e ottenere aiuto.