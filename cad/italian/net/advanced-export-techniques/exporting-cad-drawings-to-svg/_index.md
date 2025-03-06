---
title: Esportazione di disegni CAD in formato SVG - Guida Aspose.CAD
linktitle: Esportazione di disegni CAD in formato SVG
second_title: Aspose.CAD .NET - Formato file CAD e BIM
description: Esplora il processo continuo di esportazione dei disegni CAD in SVG utilizzando Aspose.CAD per .NET. Migliora il tuo sviluppo CAD con flessibilità e personalizzazione.
weight: 15
url: /it/net/advanced-export-techniques/exporting-cad-drawings-to-svg/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Esportazione di disegni CAD in formato SVG - Guida Aspose.CAD

## introduzione

Nel dinamico mondo del CAD (Computer-Aided Design), la capacità di esportare disegni in vari formati è una competenza cruciale. SVG (Scalable Vector Graphics) è uno di questi formati che ha guadagnato popolarità grazie alla sua scalabilità e versatilità. In questo tutorial esploreremo come esportare disegni CAD in SVG utilizzando la potente libreria Aspose.CAD per .NET.

## Prerequisiti

Prima di immergerti nel tutorial, assicurati di disporre dei seguenti prerequisiti:

-  Libreria Aspose.CAD per .NET: scaricare e installare la libreria Aspose.CAD per .NET. Puoi trovare la biblioteca[Qui](https://releases.aspose.com/cad/net/).

- Ambiente di sviluppo: configura un ambiente di sviluppo adatto con Visual Studio o qualsiasi altro strumento di sviluppo .NET.

## Importa spazi dei nomi

Per iniziare, importa gli spazi dei nomi necessari nel tuo progetto:

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Passaggio 1: impostare la directory dei documenti

```csharp
// Il percorso della directory dei documenti.
string MyDir = "Your Document Directory";
```

## Passaggio 2: caricare il disegno CAD

```csharp
using (Image image = Image.Load(MyDir + "sample.dwg"))
{
```

## Passaggio 3: configura le opzioni di esportazione SVG

```csharp
    var options = new SvgOptions();
    options.ColorType = SvgColorMode.Grayscale;
    options.TextAsShapes = true;
```

## Passaggio 4: salva il file SVG

```csharp
    image.Save(MyDir + "sample.svg", options);
}
```

Seguendo questi semplici passaggi, puoi esportare senza problemi i disegni CAD in SVG utilizzando Aspose.CAD per .NET. La libreria offre flessibilità e opzioni di personalizzazione, consentendoti di personalizzare l'output in base alle tue esigenze.

## Conclusione

In conclusione, Aspose.CAD per .NET semplifica il processo di esportazione dei disegni CAD in SVG. La sua API intuitiva e le sue robuste funzionalità lo rendono uno strumento prezioso per gli sviluppatori che lavorano con applicazioni CAD.

## Domande frequenti

### Q1: Aspose.CAD è compatibile con tutti i formati CAD?

A1: Aspose.CAD supporta vari formati CAD, inclusi DWG e DXF, garantendo un'ampia compatibilità.

### Q2: Posso personalizzare la modalità colore durante l'esportazione in SVG?

A2: Sì, Aspose.CAD ti consente di scegliere la modalità colore, fornendo flessibilità nell'output.

### Q3: Sono disponibili licenze temporanee a scopo di test?

 R3: Sì, puoi ottenere una licenza temporanea[Qui](https://purchase.aspose.com/temporary-license/) Per la valutazione.

### Q4: Dove posso trovare la documentazione dettagliata per Aspose.CAD?

 A4: La documentazione è disponibile[Qui](https://reference.aspose.com/cad/net/).

### Q5: Come posso ottenere supporto o porre domande relative ad Aspose.CAD?

 A5: Visita il forum della community[Qui](https://forum.aspose.com/c/cad/19) per supporto e discussioni.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
