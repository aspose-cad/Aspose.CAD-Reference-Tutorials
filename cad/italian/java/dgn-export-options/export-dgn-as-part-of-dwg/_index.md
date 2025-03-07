---
title: Esporta DGN in DWG con Aspose.CAD per Java
linktitle: Esporta DGN come parte di DWG
second_title: API Java Aspose.CAD
description: Scopri come esportare DGN come parte di DWG utilizzando Aspose.CAD per Java. Segui la nostra guida passo passo per una manipolazione efficiente dei file CAD.
weight: 10
url: /it/java/dgn-export-options/export-dgn-as-part-of-dwg/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Esporta DGN in DWG con Aspose.CAD per Java

## introduzione

In questo tutorial esploreremo come utilizzare Aspose.CAD per Java per esportare un file DGN (MicroStation Design) come parte di un file DWG (disegno AutoCAD). Aspose.CAD è una potente libreria che fornisce funzionalità complete per lavorare con i formati di file CAD. Questa guida passo passo ti aiuterà a comprendere il processo di esportazione di DGN come parte di DWG utilizzando Java.

## Prerequisiti

Prima di immergerci nel tutorial, assicurati di disporre dei seguenti prerequisiti:
1. Libreria Aspose.CAD: scarica e installa la libreria Aspose.CAD per Java. Puoi trovare la biblioteca[Qui](https://releases.aspose.com/cad/java/).
2. Java Development Kit (JDK): assicurati di avere Java installato sul tuo sistema.
3. Ambiente di sviluppo integrato (IDE): scegli un IDE Java come Eclipse o IntelliJ per un'esperienza di sviluppo più fluida.

## Importa pacchetti

Nel tuo progetto Java, importa i pacchetti Aspose.CAD necessari per abilitare la manipolazione dei file CAD. Ecco un esempio:

```java
import com.aspose.cad;
import com.aspose.cad.imageoptions;
import com.aspose.cad.fileformats.cad.cadconsts;
import com.aspose.cad.fileformats.cad;
import com.aspose.cad.fileformats.cad.cadobjects;
```

## Passaggio 1: imposta i percorsi dei file

 Definire i percorsi dei file di input e output per il file DWG. Aggiorna il`dataDir`, `fileName` , E`outPath` variabili di conseguenza.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
String outPath = dataDir + "BlockRefDgn.dwg.pdf";
```

## Passaggio 2: crea un'istanza PdfOptions

 Crea un'istanza di`PdfOptions` class, poiché stiamo esportando il file DWG in formato PDF.

```java
PdfOptions exportOptions = new PdfOptions();
```

## Passaggio 3: caricare il file DWG

 Carica il file DWG esistente come immagine e convertilo nel formato`CadImage` tipo.

```java
CadImage cadImage = (CadImage) Image.load(fileName);
```

## Passaggio 4: scorrere le entità

Esamina ciascuna entità all'interno del file DWG e controlla se si tratta di una definizione di immagine. In caso affermativo, recuperare il riferimento esterno all'oggetto.

```java
for (CadBaseEntity baseEntity : cadImage.getEntities()) {
    if (baseEntity.getTypeName() == CadEntityTypeName.DGNUNDERLAY) {
        CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
        System.out.println(dgnFile.getUnderlayPath());
    }
}
```

## Passaggio 5: definire le opzioni di rasterizzazione

 Definire le impostazioni per`CadRasterizationOptions`oggetto, inclusi larghezza della pagina, altezza, layout e colore di sfondo.

```java
CadRasterizationOptions vectorRasterizationOptions = new CadRasterizationOptions();
vectorRasterizationOptions.setPageWidth(1600);
vectorRasterizationOptions.setPageHeight(1600);
vectorRasterizationOptions.setLayouts(new String[] { "Model" });
vectorRasterizationOptions.setAutomaticLayoutsScaling(false);
vectorRasterizationOptions.setNoScaling(true);
vectorRasterizationOptions.setBackgroundColor(Color.getBlack());
vectorRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
```

## Passaggio 6: imposta le opzioni di rasterizzazione vettoriale

Imposta le opzioni di rasterizzazione vettoriale per l'esportazione.

```java
exportOptions.setVectorRasterizationOptions(vectorRasterizationOptions);
```

## Passaggio 7: esporta DWG in PDF

 Infine, esporta il DWG in PDF chiamando il file`save` metodo.

```java
cadImage.save(outPath, exportOptions);
```

## Conclusione

Congratulazioni! Hai imparato con successo come esportare un file DGN come parte di un file DWG utilizzando Aspose.CAD per Java. Questa potente libreria offre funzionalità estese per lavorare con i file CAD, rendendo le attività di manipolazione dei file CAD efficienti e semplici.

## Domande frequenti

### Q1: Dove posso trovare la documentazione per Aspose.CAD per Java?

 A1: La documentazione può essere trovata[Qui](https://reference.aspose.com/cad/java/).

### Q2: Come posso scaricare la libreria Aspose.CAD per Java?

 A2: È possibile scaricare la libreria da[questo link](https://releases.aspose.com/cad/java/).

### Q3: È disponibile una prova gratuita per Aspose.CAD per Java?

 R3: Sì, puoi trovare la prova gratuita[Qui](https://releases.aspose.com/).

### Q4: Dove posso ottenere una licenza temporanea per Aspose.CAD per Java?

 A4: Ottieni una licenza temporanea[Qui](https://purchase.aspose.com/temporary-license/).

### Q5: Hai bisogno di aiuto o hai domande?

 A5: visitare il forum di supporto della comunità Aspose.CAD[Qui](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
