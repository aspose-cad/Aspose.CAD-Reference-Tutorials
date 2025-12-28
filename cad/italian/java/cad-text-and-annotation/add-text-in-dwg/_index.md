---
date: 2025-12-28
description: Impara come creare PDF da DWG, salvare DWG come PDF e aggiungere testo
  ai disegni DWG con Aspose.CAD per Java—guida passo‑passo.
linktitle: Add Text in DWG
second_title: Aspose.CAD Java API
title: Crea PDF da DWG e aggiungi testo usando Aspose.CAD per Java
url: /it/java/cad-text-and-annotation/add-text-in-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Creare PDF da DWG e Aggiungere Testo Utilizzando Aspose.CAD per Java

## Introduzione

Se hai bisogno di **creare PDF da file DWG** inserendo anche testo personalizzato, sei nel posto giusto. In questo tutorial percorreremo l’intero processo—caricamento di un disegno DWG, aggiunta di un’annotazione di testo e, infine, salvataggio del risultato come PDF usando Aspose.CAD per Java. Alla fine comprenderai come **salvare DWG come PDF**, personalizzare l’altezza del testo e aggiungere annotazioni di base.

## Risposte Rapide
- **Posso convertire DWG in PDF in Java?** Sì, Aspose.CAD per Java fornisce un’API semplice.  
- **È necessaria una licenza per l’uso in produzione?** È richiesta una licenza commerciale; è disponibile una versione di prova gratuita.  
- **Quale metodo aggiunge testo a un DWG?** Usa l’oggetto `CadText` e aggiungilo allo spazio modello.  
- **Posso impostare l’altezza del testo?** Assolutamente—usa `setTextHeight()` sull’istanza `CadText`.  
- **L’output è basato su vettori?** Quando le opzioni di rasterizzazione sono impostate su `UseObjectColor`, il PDF mantiene dati vettoriali di alta qualità.

## Prerequisiti

Prima di immergerti nel tutorial, assicurati di avere i seguenti prerequisiti:

- Libreria Aspose.CAD per Java: scarica e installa la libreria dalla [pagina Aspose.CAD per Java](https://releases.aspose.com/cad/java/).

- Java Development Kit (JDK): assicurati di avere l’ultima versione del JDK installata sul tuo sistema.

- Disegno DWG: prepara un file di disegno DWG a cui vuoi aggiungere testo.

## Importare Namespace

Nel tuo codice Java, importa i namespace necessari per Aspose.CAD:

```java
import com.aspose.cad.Image;


import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Ora, analizziamo lo snippet di codice fornito suddividendolo in più passaggi:

## Passo 1: Configurare la Directory del Documento e il Percorso del File DWG

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String dwgPathToFile = dataDir + "SimpleEntites.dwg";
```

## Passo 2: Caricare l’Immagine DWG

```java
Image image = Image.load(dwgPathToFile);
```

## Passo 3: Creare l’Oggetto CadText (Aggiungere Testo al DWG)

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

Seguendo questi passaggi, sarai in grado di **creare PDF da DWG**, aggiungere testo personalizzato e controllare l’altezza del testo—tutto con poche righe di codice Java.

## Perché Aggiungere Testo a DWG e Convertire in PDF?

Aggiungere testo direttamente a un file DWG è utile per:

- **Annotare i progetti** con note o numeri di parte.  
- **Creare documentazione stampabile** dove il PDF funge da formato di sola lettura, ampiamente supportato.  
- **Automatizzare l’elaborazione batch** di grandi librerie CAD senza intervento manuale.

## Problemi Comuni & Suggerimenti

- **Il testo non appare?** Verifica che le coordinate X/Y siano entro i limiti del disegno e che il layer sia visibile.  
- **Altezza del testo errata?** Regola `setTextHeight()`; il valore è nel sistema di unità del disegno.  
- **Il PDF sembra rasterizzato?** Assicurati che `CadDrawTypeMode.UseObjectColor` sia impostato per mantenere le informazioni vettoriali.  
- **Prestazioni su file di grandi dimensioni?** Aumenta `pageHeight`/`pageWidth` solo se necessario; valori più alti consumano più memoria.

## Domande Frequenti

**D: Aspose.CAD è compatibile con tutte le versioni dei file DWG?**  
R: Aspose.CAD supporta varie versioni di file DWG, garantendo la compatibilità con un’ampia gamma di software CAD.

**D: Posso personalizzare il carattere e la formattazione del testo aggiunto?**  
R: Sì, puoi personalizzare il font, lo stile e altre opzioni di formattazione per il testo aggiunto ai file DWG usando Aspose.CAD.

**D: È disponibile una versione di prova gratuita per Aspose.CAD per Java?**  
R: Sì, puoi esplorare le funzionalità di Aspose.CAD ottenendo una prova gratuita da [qui](https://releases.aspose.com/).

**D: Dove posso trovare la documentazione dettagliata per Aspose.CAD per Java?**  
R: Consulta la documentazione [qui](https://reference.aspose.com/cad/java/) per informazioni approfondite ed esempi.

**D: Come posso ottenere supporto o assistenza per Aspose.CAD?**  
R: Visita il [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) per ricevere aiuto e connetterti con la community.

---

**Ultimo aggiornamento:** 2025-12-28  
**Testato con:** Aspose.CAD per Java 24.12  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}