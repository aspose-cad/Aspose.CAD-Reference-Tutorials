---
date: 2026-02-28
description: Scopri come creare PDF da DWG, salvare DWG come PDF e aggiungere testo
  ai disegni DWG con Aspose.CAD per Java—guida passo passo.
linktitle: Add Text in DWG
second_title: Aspose.CAD Java API
title: Crea PDF da DWG e aggiungi testo usando Aspose.CAD per Java
url: /it/java/cad-text-and-annotation/add-text-in-dwg/
weight: 10
---

 all markdown formatting.

Now produce final content.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Creare PDF da DWG e Aggiungere Testo Utilizzando Aspose.CAD per Java

## Introduzione

Se hai bisogno di **create PDF from DWG** file inserendo anche testo personalizzato, sei nel posto giusto. In questo tutorial percorreremo l'intero processo—caricamento di un disegno DWG, aggiunta di un'annotazione di testo e, infine, salvataggio del risultato come PDF utilizzando Aspose.CAD per Java. Alla fine comprenderai come **save DWG as PDF**, personalizzare l'altezza del testo e aggiungere anche annotazioni di base.

## Risposte Rapide
- **Posso convertire DWG in PDF in Java?** Sì, Aspose.CAD per Java fornisce un'API semplice.  
- **Ho bisogno di una licenza per l'uso in produzione?** È necessaria una licenza commerciale; è disponibile una versione di prova gratuita.  
- **Quale metodo aggiunge testo a un DWG?** Usa l'oggetto `CadText` e aggiungilo allo spazio modello.  
- **Posso impostare l'altezza del testo?** Assolutamente—usa `setTextHeight()` sull'istanza `CadText`.  
- **L'output è basato su vettori?** Quando le opzioni di rasterizzazione sono impostate su `UseObjectColor`, il PDF mantiene dati vettoriali ad alta qualità.

## Che cosa significa “creare PDF da DWG”?
Creare un PDF da un disegno DWG significa convertire il formato CAD nativo in un documento ampiamente supportato, di sola lettura, preservando la geometria originale. Questa conversione è essenziale quando è necessario condividere i progetti con stakeholder che non possiedono software CAD.

## Perché usare Aspose.CAD per Java per convertire DWG in PDF?
Aspose.CAD offre una soluzione pure‑Java che non richiede alcuna installazione CAD esterna. Supporta **convert DWG to PDF**, mantiene la fedeltà vettoriale e consente di aggiungere programmaticamente annotazioni come testo, quote o grafica personalizzata prima della conversione.

## Prerequisiti

Prima di immergerti nel tutorial, assicurati di avere i seguenti prerequisiti:

- Aspose.CAD for Java Library: scarica e installa la libreria dalla [Aspose.CAD for Java page](https://releases.aspose.com/cad/java/).
- Java Development Kit (JDK): assicurati di avere l'ultima versione del JDK installata sul tuo sistema.
- DWG Drawing: prepara un file di disegno DWG dove desideri aggiungere testo.

## Importare i Namespace

Nella tua code Java, importa i namespace necessari per Aspose.CAD:

```java
import com.aspose.cad.Image;


import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Ora, suddividiamo lo snippet di codice fornito in più passaggi:

## Passo 1: Configurare la Directory del Documento e il Percorso del File DWG

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String dwgPathToFile = dataDir + "SimpleEntites.dwg";
```

## Passo 2: Caricare l'Immagine DWG

```java
Image image = Image.load(dwgPathToFile);
```

## Passo 3: Creare l'Oggetto CadText (Aggiungere Testo al DWG)

```java
CadText cadText = new CadText();
cadText.setStyleType("Standard");
cadText.setDefaultValue("Some custom text");
cadText.setColorId(256);
cadText.setLayerName("0");
cadText.getFirstAlignment().setX(47.9);
cadText.getFirstAlignment().setY(5.56);
cadText.setTextHeight(0.8);          // set text height in DWG units
cadText.setScaleX(0);
```

## Passo 4: Aggiungere Testo a CadImage (Inserire Annotazione)

```java
CadImage cadImage = ((CadImage)(image));
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(cadText);
```

## Passo 5: Configurare le Opzioni PDF (Preparare la creazione del PDF da DWG)

```java
PdfOptions pdfOptions = new PdfOptions();
```

## Passo 6: Configurare CadRasterizationOptions (Controllare il rendering PDF)

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

## Passo 7: Salvare il DWG Modificato come PDF (dwg to pdf java)

```java
image.save(dataDir + "SimpleEntites_generated.dwg.pdf", pdfOptions);
```

Seguendo questi passaggi, sarai in grado di **create PDF from DWG**, aggiungere testo personalizzato e controllare l'altezza del testo—tutto con poche righe di codice Java.

## Come convertire DWG in PDF in Java su larga scala?
Se hai bisogno di **batch convert DWG PDF** file, avvolgi il codice sopra in un ciclo che itera su una cartella di disegni DWG. Regola `pageHeight`/`pageWidth` solo quando necessario per mantenere basso l'uso della memoria e riutilizza la stessa istanza `PdfOptions` per ogni file per migliorare le prestazioni.

## Problemi Comuni & Suggerimenti

- **Il testo non appare?** Verifica che le coordinate X/Y siano entro i limiti del disegno e che il layer sia visibile.
- **Altezza del testo errata?** Regola `setTextHeight()`; il valore è nel sistema di unità del disegno.
- **Il PDF sembra rasterizzato?** Assicurati che `CadDrawTypeMode.UseObjectColor` sia impostato per mantenere le informazioni vettoriali.
- **Prestazioni su file grandi?** Aumenta `pageHeight`/`pageWidth` solo se necessario; valori più grandi consumano più memoria.

## Domande Frequenti

**Q:** Aspose.CAD è compatibile con tutte le versioni dei file DWG?  
**A:** Aspose.CAD supporta varie versioni di file DWG, garantendo compatibilità con un'ampia gamma di software CAD.

**Q:** Posso personalizzare il font e la formattazione del testo aggiunto?  
**A:** Sì, puoi personalizzare il font, lo stile e altre opzioni di formattazione per il testo aggiunto ai file DWG usando Aspose.CAD.

**Q:** È disponibile una versione di prova gratuita per Aspose.CAD per Java?  
**A:** Sì, puoi esplorare le funzionalità di Aspose.CAD ottenendo una prova gratuita da [here](https://releases.aspose.com/).

**Q:** Dove posso trovare la documentazione dettagliata per Aspose.CAD per Java?  
**A:** Consulta la documentazione [here](https://reference.aspose.com/cad/java/) per informazioni approfondite ed esempi.

**Q:** Come posso ottenere supporto o assistenza per Aspose.CAD?  
**A:** Visita il [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) per ricevere assistenza e connetterti con la community.

---

**Last Updated:** 2026-02-28  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}