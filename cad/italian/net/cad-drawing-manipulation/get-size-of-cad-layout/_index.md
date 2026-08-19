---
date: 2026-03-21
description: Scopri come ottenere le dimensioni del layout CAD in .NET usando Aspose.CAD.
  Segui la nostra guida passo passo per una manipolazione efficiente dei file CAD.
linktitle: Get Size of CAD Layout
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Ottieni la dimensione del layout CAD in Aspose.CAD per .NET
url: /it/net/cad-drawing-manipulation/get-size-of-cad-layout/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ottieni le dimensioni del layout CAD in Aspose.CAD per .NET

## Introduzione

In questo tutorial completo scoprirai **come ottenere le dimensioni del layout CAD** utilizzando la libreria Aspose.CAD per .NET. Che tu stia costruendo un visualizzatore CAD, generando miniature o abbia bisogno di dimensioni precise del layout per elaborazioni successive, conoscere la dimensione esatta di ogni layout è fondamentale. Ti guideremo attraverso l’intero flusso di lavoro—dal caricamento del disegno all’estrazione delle dimensioni del layout e, facoltativamente, al salvataggio come immagini—così potrai integrare questa funzionalità nelle tue applicazioni con sicurezza.

## Risposte rapide
- **Cosa significa “ottenere le dimensioni del layout CAD”?** Indica il recupero della larghezza e dell’altezza (in unità di disegno) di ciascun layout non vuoto in un file CAD.  
- **Quale libreria lo supporta?** Aspose.CAD per .NET fornisce un’API semplice per accedere alle informazioni del layout.  
- **È necessaria una licenza?** Una versione di prova gratuita è sufficiente per la valutazione; è richiesta una licenza commerciale per l’uso in produzione.  
- **Formati supportati?** DWG, DXF e molti altri formati CAD/BIM sono pienamente supportati.  
- **Tempo tipico di implementazione?** Circa 10‑15 minuti per una routine base di recupero dimensioni.

## Che cosa significa “ottenere le dimensioni del layout CAD”?
Ottenere le dimensioni del layout CAD significa estrarre le estensioni geometriche di ciascun layout (spazio carta) definito in un disegno CAD. Queste estensioni sono espresse nelle unità native del disegno (di solito millimetri o pollici) e sono utili per attività come il ridimensionamento, la stampa o la generazione di immagini di anteprima.

## Perché recuperare le dimensioni del layout CAD con Aspose.CAD?
- **Nessun software CAD richiesto** – Funziona interamente lato server.  
- **Cross‑platform** – Compatibile con .NET Framework, .NET Core e .NET 5/6+.  
- **Misurazioni accurate** – Restituisce le estensioni esatte così come memorizzate nel file, evitando analisi manuali.  
- **Integrazione semplice** – Chiamate API intuitive si inseriscono naturalmente nei progetti C# esistenti.

## Prerequisiti

Prima di immergerti nel codice, assicurati di avere quanto segue:

- Aspose.CAD per .NET installato. Puoi scaricarlo dalla [pagina di download di Aspose.CAD per .NET](https://releases.aspose.com/cad/net/).
- Uno o più file CAD (DWG, DXF, ecc.) che desideri analizzare. Questa guida utilizza `conic_pyramid.dxf` e `Bottom_plate.dwg` come file di esempio.

## Importare gli spazi dei nomi

Nel tuo progetto .NET, inizia importando gli spazi dei nomi richiesti:

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.ImageOptions;
```

## Passo 1: Configurare la directory dei documenti

Definisci la cartella che contiene i tuoi file CAD. Sostituisci il segnaposto con il percorso reale sul tuo computer.

```csharp
string MyDir = "Your Document Directory";
```

## Passo 2: Specificare i percorsi dei file CAD

Crea un array che punti a ciascun file CAD da elaborare.

```csharp
string[] sourceFilePaths = new[]
{
    MyDir + "conic_pyramid.dxf",
    MyDir + "Bottom_plate.dwg"
};
```

## Passo 3: Iterare sui file CAD

Carica ogni file, rileva il suo formato e preparati a estrarre le informazioni del layout.

```csharp
foreach (var sourceFilePath in sourceFilePaths)
{
    string extension = Path.GetExtension(sourceFilePath);
    using (CadImage cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath))
    {
        // ... (continue to the next step)
    }
}
```

## Passo 4: Ottenere i layout non vuoti

Abbiamo bisogno di un metodo di supporto che restituisca solo i layout che contengono effettivamente entità di disegno. I layout vuoti vengono ignorati perché non hanno dimensioni da segnalare.

```csharp
private static List<string> GetNotEmptyLayouts(Image cadImage, string extension)
{
    // ... (continue to the next step)
}
```

## Passo 5: Ottenere i layout per i file DWG

I file DWG memorizzano le informazioni del layout nella tabella `HeaderVariables`. Il metodo seguente estrae i nomi di tutti i layout non vuoti per un disegno DWG.

```csharp
private static List<string> GetNotEmptyLayoutsForDwg(CadImage cadImage)
{
    // ... (continue to the next step)
}
```

## Passo 6: Ottenere i layout per i file DXF

I file DXF utilizzano una struttura diversa. Questo metodo analizza la collezione `Tables` per trovare i layout di spazio carta che contengono entità.

```csharp
private static List<string> GetNotEmptyLayoutsForDxf(CadImage cadImage)
{
    // ... (continue to the next step)
}
```

## Passo 7: Recuperare le dimensioni del layout e salvare come immagine

Infine, cicla su ciascun layout scoperto, leggi le sue estensioni e, facoltativamente, rendi il layout in un file immagine per una verifica visiva.

```csharp
foreach (string layout in layouts)
{
    // ... (continue to the next step)
}
```

## Problemi comuni e consigli

- **Nomi di layout mancanti:** Assicurati che il file CAD contenga effettivamente layout di spazio carta; alcuni file hanno solo lo spazio modello.  
- **Unità errate:** Le dimensioni sono restituite nelle unità native del disegno. Converti in millimetri o pollici se necessario.  
- **Prestazioni:** Il caricamento di file DWG/DXF molto grandi può richiedere molta memoria; considera di elaborare i file in modo asincrono o a lotti.

## Domande frequenti

**D: Aspose.CAD è compatibile con tutti i formati di file CAD?**  
R: Sì, Aspose.CAD supporta un’ampia gamma di formati, inclusi DWG, DXF, DGN e molti tipi di file BIM.

**D: Posso personalizzare le opzioni di salvataggio dell’immagine?**  
R: Assolutamente! Puoi regolare le `CadRasterizationOptions` (formato, risoluzione, colore di sfondo, ecc.) per soddisfare le tue esigenze specifiche.

**D: Dove posso trovare documentazione aggiuntiva?**  
R: Consulta la [documentazione di Aspose.CAD](https://reference.aspose.com/cad/net/) per riferimenti API dettagliati e ulteriori esempi.

**D: È disponibile una versione di prova gratuita?**  
R: Sì, puoi esplorare Aspose.CAD con una [versione di prova gratuita](https://releases.aspose.com/).

**D: Come posso ottenere supporto tecnico?**  
R: Per il supporto tecnico, visita il [forum di Aspose.CAD](https://forum.aspose.com/c/cad/19).

---

**Ultimo aggiornamento:** 2026-03-21  
**Testato con:** Aspose.CAD 24.11 per .NET  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}