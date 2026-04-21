---
date: 2026-03-29
description: Scopri come sostituire rapidamente i font in Aspose.CAD per .NET. Questa
  guida passo passo ti mostra come impostare il nome del font principale e personalizzare
  i disegni CAD in modo efficiente.
linktitle: Substituting Fonts
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Come sostituire i font in Aspose.CAD per .NET
url: /it/net/cad-features-and-support/substituting-fonts/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come sostituire i caratteri in Aspose.CAD per .NET

## Introduzione

Nel campo dello sviluppo CAD con .NET, apprendere **come sostituire i caratteri** è una competenza fondamentale che può migliorare notevolmente la qualità visiva dei tuoi disegni. Aspose.CAD per .NET offre un'API semplice che consente di **impostare il nome del carattere primario** per qualsiasi stile, rendendo la sostituzione globale o selettiva dei caratteri un gioco da ragazzi. In questo tutorial percorreremo l'intero processo—dalla caricamento di un disegno alla sostituzione dei caratteri, sia a livello globale sia per nome di stile specifico.

## Risposte rapide
- **Qual è la classe principale per la manipolazione CAD?** `Aspose.CAD.Image` (o il suo derivato `CadImage`).
- **Quale proprietà cambia il carattere?** `PrimaryFontName` su `CadStyleTableObject`.
- **Posso sostituire i caratteri per tutti gli stili in una volta?** Sì, itera attraverso `cadImage.Styles` e imposta la proprietà.
- **È necessaria una licenza per la produzione?** È richiesta una licenza valida di Aspose.CAD per l'uso non‑trial.
- **Versioni .NET supportate?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## Cos'è la sostituzione dei caratteri in CAD?

La sostituzione dei caratteri significa sostituire il tipo di carattere originale usato in un disegno CAD con un altro disponibile sul sistema di destinazione. Questo è particolarmente utile quando il carattere originale è mancante, quando è necessario uno stile aziendale coerente, o quando si preparano disegni per la stampa su dispositivi che supportano solo un set limitato di caratteri.

## Perché sostituire i caratteri con Aspose.CAD?

- **Nessuna dipendenza esterna** – la libreria gestisce la mappatura dei caratteri internamente.
- **Funziona con molti formati** – DXF, DWG, DGN e altri.
- **Controllo programmatico** – automatizza il processo per conversioni batch o pipeline CI.
- **Preserva la geometria del disegno** – solo la rappresentazione visiva del testo cambia.

## Prerequisiti

- Conoscenza di base della programmazione .NET.
- Aspose.CAD per .NET installato. Se non lo hai ancora installato, scaricalo [qui](https://releases.aspose.com/cad/net/).
- Un file di disegno CAD (DXF, DWG, ecc.) per sperimentare.

## Importa gli spazi dei nomi

Prima di iniziare, importa gli spazi dei nomi necessari per accedere alle funzionalità di Aspose.CAD nella tua applicazione .NET.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad.CadTables;
```

## Passo 1: Carica il disegno CAD

Inizia caricando il disegno CAD in un'istanza di `CadImage`. Assicurati di fornire il percorso corretto alla directory dei tuoi documenti.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (CadImage cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    // Your code for further actions goes here
}
```

## Passo 2: Itera sugli stili

Successivamente, itera sugli stili nel disegno CAD usando un ciclo `foreach`. Questo ti permette di accedere e manipolare singoli stili di carattere.

```csharp
foreach (CadStyleTableObject style in cadImage.Styles)
{
    // Your code for style manipulation goes here
}
```

## Come impostare il nome del carattere primario per la sostituzione dei caratteri

La proprietà `PrimaryFontName` su ogni `CadStyleTableObject` controlla quale carattere viene usato quando il disegno viene renderizzato. Impostando questa proprietà sostituisci effettivamente il carattere originale.

### Passo 3: Sostituisci i caratteri a livello globale

Per sostituire i caratteri per **tutti** gli stili, imposta la proprietà `PrimaryFontName` per ogni stile al nome del carattere desiderato, ad esempio, `"Arial"`.

```csharp
foreach (CadStyleTableObject style in cadImage.Styles)
{
    style.PrimaryFontName = "Arial";
}
```

### Passo 4: Sostituisci il carattere per nome di stile

Se devi sostituire il carattere solo per uno stile specifico (ad esempio, lo stile chiamato `"Roman"`), aggiungi un controllo condizionale all'interno del ciclo.

```csharp
foreach (CadStyleTableObject style in cadImage.Styles)
{
    if (style.StyleName == "Roman")
    {
        style.PrimaryFontName = "Arial";
    }
}
```

## Problemi comuni e risoluzione

| Problema | Causa | Soluzione |
|----------|-------|-----------|
| Il carattere non cambia dopo l'esecuzione del codice | Il disegno è memorizzato nella cache o aperto in modalità sola lettura | Assicurati di salvare l'immagine dopo la modifica (`cadImage.Save(...)`) o ricarica il file per verificare. |
| Il carattere desiderato non è trovato sul sistema | Carattere non installato sulla macchina che esegue il codice | Installa il carattere TrueType/OpenType richiesto o incorporalo nelle risorse dell'applicazione. |
| Il testo appare illeggibile | Codifica errata o mancanza di supporto Unicode | Usa un carattere che supporta il set di caratteri richiesto (ad esempio, Arial Unicode MS). |

## Domande frequenti

**Q: Posso ripristinare le modifiche ai caratteri in Aspose.CAD per .NET?**  
A: Sì, puoi ripristinare ricaricando il disegno CAD originale o mantenendo una copia di backup prima di apportare modifiche.

**Q: Ci sono altre proprietà dei caratteri che posso modificare?**  
A: Assolutamente. Oltre a `PrimaryFontName`, puoi lavorare con `SecondaryFontName`, `FontFamily` e altri attributi correlati allo stile per personalizzazioni avanzate.

**Q: Aspose.CAD è compatibile con diversi formati CAD?**  
A: Sì, Aspose.CAD supporta un'ampia gamma di formati come DXF, DWG, DGN, DWF e altri, offrendoti flessibilità nei progetti.

**Q: Posso automatizzare la sostituzione dei caratteri in elaborazione batch?**  
A: Certamente. Avvolgi la logica di caricamento e sostituzione in un ciclo che itera su una cartella di file CAD, o integrala in una pipeline CI/CD.

**Q: Dove posso trovare supporto aggiuntivo per Aspose.CAD per .NET?**  
A: Per supporto aggiuntivo e discussioni della community, visita il [forum Aspose.CAD](https://forum.aspose.com/c/cad/19).

---

**Ultimo aggiornamento:** 2026-03-29  
**Testato con:** Aspose.CAD per .NET (ultima release)  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}