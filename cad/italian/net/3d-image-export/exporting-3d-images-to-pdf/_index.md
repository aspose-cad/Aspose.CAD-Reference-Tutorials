---
title: Esportazione di immagini 3D in PDF - Tutorial Aspose.CAD
linktitle: Esportazione di immagini 3D in PDF
second_title: Aspose.CAD .NET - Formato file CAD e BIM
description: Converti facilmente immagini CAD 3D in PDF con Aspose.CAD per .NET. Segui il nostro tutorial passo passo per esportare PDF senza problemi.
weight: 10
url: /it/net/3d-image-export/exporting-3d-images-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Esportazione di immagini 3D in PDF - Tutorial Aspose.CAD

## introduzione

Stai cercando di esportare senza problemi immagini 3D in PDF utilizzando Aspose.CAD per .NET? Questo tutorial passo passo ti guiderà attraverso il processo, assicurandoti di sfruttare la potenza di Aspose.CAD per convertire senza sforzo le tue immagini 3D in formato PDF.

## Prerequisiti

Prima di immergerti nel tutorial, assicurati di avere i seguenti prerequisiti:

-  Aspose.CAD per .NET: assicurati di avere la libreria Aspose.CAD per .NET installata. In caso contrario, puoi scaricarlo da[Pagina di download di Aspose.CAD per .NET](https://releases.aspose.com/cad/net/).

- Directory dei documenti: imposta una directory in cui sono archiviati i file CAD e annota il percorso.

## Importa spazi dei nomi

Nel tuo progetto .NET, importa gli spazi dei nomi necessari per lavorare con Aspose.CAD. Aggiungi le seguenti righe all'inizio del file di codice:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

## Passaggio 1: caricare l'immagine CAD

 Inizia caricando l'immagine CAD che desideri esportare in PDF. Usa il`Load` metodo dalla libreria Aspose.CAD. Sostituire`"conic_pyramid.dxf"` con il percorso del file CAD.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image cadImage = Image.Load(sourceFilePath))
{
    // Il tuo codice per caricare l'immagine CAD va qui
}
```

## Passaggio 2: configura le opzioni di rasterizzazione

 Configurare le opzioni di rasterizzazione per l'immagine CAD. Imposta parametri come larghezza della pagina, altezza della pagina e layout. Decommenta la riga relativa a`TypeOfEntities` se le tue entità sono 3D.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
// rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;

rasterizationOptions.Layouts = new string[] { "Model" };
```

## Passaggio 3: imposta le opzioni PDF

Crea opzioni PDF e associale alle opzioni di rasterizzazione.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Passaggio 4: salva come PDF

Salva l'immagine CAD come file PDF utilizzando le opzioni configurate. Specificare il percorso di output per il file PDF.

```csharp
MyDir = MyDir + "Export3DImagestoPDF_out.pdf";
cadImage.Save(MyDir, pdfOptions);
```

## Conclusione

Congratulazioni! Hai esportato con successo immagini 3D in PDF utilizzando Aspose.CAD per .NET. Questo semplice tutorial ti assicura di convertire facilmente i tuoi file CAD in un formato più accessibile.

## Domande frequenti

### Q1: Aspose.CAD è compatibile con tutti i formati di file CAD?

A1: Sì, Aspose.CAD supporta un'ampia gamma di formati CAD, garantendo flessibilità nella gestione di vari tipi di file.

### Q2: Posso personalizzare le dimensioni della pagina durante l'esportazione in PDF?

A2: Assolutamente. Il tutorial mostra come configurare la larghezza e l'altezza della pagina in base alle proprie esigenze.

### Q3: Sono disponibili licenze temporanee per Aspose.CAD?

 A3: Sì, puoi ottenere licenze temporanee per Aspose.CAD visitando[Licenza temporanea](https://purchase.aspose.com/temporary-license/).

### Q4: Dove posso trovare ulteriore supporto o discussioni nella community?

 A4: Vai al[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) per il supporto e il coinvolgimento con la comunità.

### Q5: È disponibile una versione di prova gratuita di Aspose.CAD?

 A5: Sì, puoi esplorare le funzionalità di Aspose.CAD accedendo a[prova gratuita](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
