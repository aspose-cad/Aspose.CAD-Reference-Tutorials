---
date: 2026-03-19
description: Scopri come ridimensionare i disegni CAD in .NET con Aspose.CAD, inclusa
  la scalatura delle unità dei disegni CAD e la regolazione delle dimensioni del layout.
  Segui la nostra guida passo passo.
linktitle: Adjusting CAD Drawing Size
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Come ridimensionare i disegni CAD con Aspose.CAD per .NET
url: /it/net/cad-drawing-manipulation/adjust-cad-drawing-size/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come ridimensionare i disegni CAD con Aspose.CAD per .NET

## Introduzione

Se hai bisogno di **come ridimensionare CAD** file direttamente dalla tua applicazione .NET, sei nel posto giusto. In questo tutorial ti mostreremo come modificare le impostazioni dell'unità CAD, scalare le dimensioni del disegno CAD e regolare la dimensione del CAD programmaticamente usando Aspose.CAD per .NET. Alla fine della guida avrai una soluzione solida, pronta per la produzione, per ridimensionare qualsiasi formato CAD supportato.

## Risposte rapide
- **Quale libreria è necessaria?** Aspose.CAD per .NET  
- **Posso cambiare il tipo di unità?** Sì – imposta `UnitType` in `CadRasterizationOptions`  
- **È necessaria una licenza per la produzione?** È richiesta una licenza valida di Aspose.CAD per l'uso non‑trial  
- **In quale formato immagine l'esempio esporta?** BMP (ma funziona qualsiasi formato raster supportato)  
- **Quante righe di codice?** Meno di 30 righe per un'operazione completa di ridimensionamento  

## Cos'è “come ridimensionare CAD” in pratica?
Ridimensionare un disegno CAD significa convertire i dati vettoriali in un'immagine raster a una scala o unità specifica (ad es., centimetri, pollici). Questo è utile quando devi incorporare i disegni nei report, generare miniature o integrare visualizzazioni CAD in pagine web.

## Perché regolare la dimensione CAD con Aspose.CAD?
- **Nessun software CAD esterno** – tutto gira all'interno del tuo codice .NET.  
- **Controllo fine** sulle unità, layout e opzioni di rasterizzazione.  
- **Supporto cross‑format** – lo stesso codice funziona per DWG, DXF, DWF e altri.  

## Prerequisiti

Prima di iniziare, assicurati di avere:

- Libreria Aspose.CAD per .NET: scarica e installa la libreria dalla [pagina di download di Aspose.CAD per .NET](https://releases.aspose.com/cad/net/).  
- Disegno CAD di esempio: un file come `sample.dwg` posizionato nella directory dei documenti del tuo progetto.  

## Importare gli spazi dei nomi

Per prima cosa, importa gli spazi dei nomi che ti danno accesso alle classi di Aspose.CAD.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Passo 1: Caricare il disegno CAD

Carica il file sorgente in un oggetto `Image`. Questo oggetto rappresenta il disegno CAD in memoria e sarà la base per tutte le operazioni successive.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "sample.dwg";

// Load a CAD drawing in an instance of Image
using (var image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // Your code here...
}
```

## Passo 2: Creare BmpOptions (o qualsiasi altro formato raster)

`BmpOptions` indica ad Aspose.CAD come renderizzare i dati vettoriali quando lo salvi come bitmap. Puoi sostituirlo con `PngOptions`, `JpegOptions`, ecc., a seconda del formato di destinazione.

```csharp
Aspose.CAD.ImageOptions.BmpOptions bmpOptions = new Aspose.CAD.ImageOptions.BmpOptions();
```

## Passo 3: Impostare CadRasterizationOptions

`CadRasterizationOptions` contiene le impostazioni principali per la scalatura, la conversione di unità e la selezione del layout. Collegandolo alla proprietà `VectorRasterizationOptions` di `BmpOptions` garantisci che il rasterizzatore utilizzi le tue impostazioni personalizzate.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions cadRasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
bmpOptions.VectorRasterizationOptions = cadRasterizationOptions;
```

## Passo 4: Impostare UnitType (cambiare unità CAD)

Qui cambiamo l'unità CAD dal valore predefinito ai centimetri. È qui che vive la parola chiave **change cad unit**, e influisce direttamente sulla dimensione finale dell'immagine.

```csharp
cadRasterizationOptions.UnitType = Aspose.CAD.ImageOptions.UnitType.Centimeter;
```

## Passo 5: Scegliere i Layout (impostare layout CAD)

Se il tuo disegno contiene più layout (ad es., Model, Sheet1), specifica quali vuoi rasterizzare. Selezionare il layout corretto è essenziale quando **set cad layouts** per un output ridimensionato.

```csharp
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## Passo 6: Esportare in BMP (ridimensionare il disegno CAD)

Infine, salva l'immagine rasterizzata. Il file di output riflette la nuova dimensione, unità e layout configurati—completando effettivamente l'operazione di **resize CAD drawing**.

```csharp
string outPath = sourceFilePath + ".bmp";
image.Save(outPath, bmpOptions);
```

Ora hai un file BMP che rappresenta il disegno CAD ridimensionato, pronto per ulteriori elaborazioni o visualizzazioni.

## Problemi comuni e soluzioni

| Problema | Perché accade | Soluzione |
|----------|---------------|-----------|
| L'output è sfocato | DPI (dots per inch) predefinito troppo basso | Imposta `cadRasterizationOptions.Resolution = 300;` prima di salvare |
| Viene mostrato il layout sbagliato | Errore di battitura nel nome del layout | Verifica il nome esatto del layout usando un visualizzatore CAD o la collezione `Layouts` |
| La conversione di unità sembra errata | Miscelazione di unità metriche e imperiali | Assicurati che `UnitType` corrisponda al sistema di misura desiderato |

## FAQ

### Q1: Aspose.CAD per .NET è compatibile con tutti i formati CAD?

A1: Aspose.CAD per .NET supporta un'ampia gamma di formati CAD, inclusi DWG, DXF, DWF e altri. Consulta la [documentazione](https://reference.aspose.com/cad/net/) per l'elenco completo.

### Q2: Posso ridimensionare più layout contemporaneamente?

A2: Sì, puoi ridimensionare più layout regolando l'array `Layouts` in `CadRasterizationOptions`.

### Q3: Dove posso ottenere supporto per Aspose.CAD per .NET?

A3: Visita il [forum di Aspose.CAD](https://forum.aspose.com/c/cad/19) per supporto della community e assistenza.

### Q4: È disponibile una prova gratuita?

A4: Sì, puoi provare una [free trial](https://releases.aspose.com/) per valutare le funzionalità di Aspose.CAD per .NET.

### Q5: Come posso ottenere una licenza temporanea per Aspose.CAD per .NET?

A5: Ottieni una licenza temporanea per scopi di test [qui](https://purchase.aspose.com/temporary-license/).

## Domande frequenti

**D: Come posso scalare un disegno CAD senza cambiare il tipo di unità?**  
R: Regola la proprietà `Zoom` di `CadRasterizationOptions` (ad es., `cadRasterizationOptions.Zoom = 2.0;`) per raddoppiare le dimensioni mantenendo l'unità originale.

**D: Posso esportare in formati diversi da BMP?**  
R: Assolutamente. Sostituisci `BmpOptions` con `PngOptions`, `JpegOptions` o qualsiasi altra classe di formato raster supportata.

**D: È possibile elaborare in batch una cartella di disegni?**  
R: Sì. Scorri i file in una directory, applica la stessa logica di rasterizzazione e salva ogni output con un nome univoco.

---

**Ultimo aggiornamento:** 2026-03-19  
**Testato con:** Aspose.CAD per .NET 24.11 (ultima versione al momento della stesura)  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}