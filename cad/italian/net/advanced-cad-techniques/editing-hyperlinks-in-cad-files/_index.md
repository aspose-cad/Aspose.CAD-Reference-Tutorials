---
date: 2026-03-05
description: Scopri come modificare il percorso xref, aggiornare il riferimento del
  blocco e gestire i collegamenti ipertestuali CAD usando Aspose.CAD per .NET in pochi
  semplici passaggi.
linktitle: Editing Hyperlinks in CAD Files
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Come modificare il percorso xref e modificare i collegamenti ipertestuali nei
  file CAD - Tutorial Aspose.CAD
url: /it/net/advanced-cad-techniques/editing-hyperlinks-in-cad-files/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Modifica dei collegamenti ipertestuali nei file CAD - Tutorial Aspose.CAD

## Introduzione

Benvenuti alla nostra guida passo‑passo su come **change xref path** e modificare i collegamenti ipertestuali nei file CAD con Aspose.CAD per .NET. Che tu abbia bisogno di **update block reference** informazioni o semplicemente **manage CAD hyperlinks**, questo tutorial ti accompagna attraverso l'intero processo, dal caricamento di un file DWG al salvataggio delle modifiche. Alla fine, avrai un modello chiaro e riutilizzabile per mantenere correttamente collegati i tuoi documenti CAD.

## Risposte rapide
- **Che cosa significa “change xref path”?** Aggiorna il percorso del file di riferimento esterno (XRef) memorizzato in un blocco CAD.  
- **Quale libreria gestisce questo?** Aspose.CAD per .NET fornisce una semplice API per modificare i percorsi XRef e i collegamenti ipertestuali.  
- **Ho bisogno di una licenza?** Una versione di prova gratuita funziona per lo sviluppo; è necessaria una licenza commerciale per la produzione.  
- **Posso usarlo con .NET Core?** Sì, la libreria supporta .NET Framework e .NET Core/.NET 5+.  
- **Quanto tempo richiede l'implementazione?** Tipicamente meno di 10 minuti per un file di base.

## Cos'è la modifica del percorso XRef?

Nella terminologia CAD, un **XRef** (riferimento esterno) punta a un altro file di disegno inserito come blocco. Modificare il percorso XRef significa indirizzare il blocco a una nuova posizione del file, operazione essenziale quando si riorganizzano le cartelle di progetto o si aggiornano le risorse collegate.

## Perché aggiornare il riferimento del blocco e gestire i collegamenti ipertestuali CAD?

- **Mantenere la coerenza** quando i file vengono spostati tra ambienti.  
- **Evitare collegamenti interrotti** che possono causare errori durante il rendering o l'elaborazione successiva.  
- **Ottimizzare i flussi di lavoro BIM** garantendo programmaticamente che tutti i riferimenti siano aggiornati.  

## Prerequisiti

- Conoscenza di base di C# e sviluppo .NET.  
- Aspose.CAD per .NET installato – scaricalo [qui](https://releases.aspose.com/cad/net/).  
- Un file CAD di esempio (ad es., *AutoCad_Sample.dwg*) per sperimentare.

## Importare gli spazi dei nomi

Nella tua progetto C#, includi gli spazi dei nomi richiesti:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

Ora procediamo passo passo attraverso l'implementazione.

## Passo 1: Caricare il file CAD

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";
string dwgPathToFile = MyDir + "AutoCad_Sample.dwg";

using (CadImage cadImage = (CadImage)Image.Load(dwgPathToFile))
{
    // Your code for editing hyperlinks will go here.
}
```

## Passo 2: Iterare attraverso le entità

```csharp
foreach (CadBaseEntity entity in cadImage.Entities)
{
    // Your code for handling each entity will go here.
}
```

## Passo 3: Modificare gli oggetti Insert – Cambiare il percorso XRef

```csharp
if (entity is CadInsertObject)
{
    CadBlockEntity block = cadImage.BlockEntities[((CadInsertObject)entity).Name];
    if (!string.IsNullOrEmpty(block.XRefPathName.Value))
    {
        // **Primary keyword usage:** change xref path
        block.XRefPathName.Value = "new file reference.dwg";
    }
}
```

*Qui **update block reference** assegnando un nuovo nome di file XRef. Questo è il fulcro della modifica del percorso XRef.*

## Passo 4: Modificare i collegamenti ipertestuali – Gestire i collegamenti ipertestuali CAD

```csharp
if (entity.Hyperlink == "https://products.aspose.com")
{
    // **Secondary keyword usage:** manage cad hyperlinks
    entity.Hyperlink = "https://www.aspose.com";
}
```

*Questo frammento dimostra come **update CAD links** (hyperlinks) per puntare all'indirizzo web corretto.*

## Problemi comuni e soluzioni

| Problema | Causa | Soluzione |
|----------|-------|-----------|
| Il percorso XRef non si aggiorna | Il blocco non è un `CadInsertObject` | Verifica il tipo di entità prima del cast. |
| Il collegamento ipertestuale non è cambiato | La proprietà Hyperlink è null o ha un caso diverso | Usa `StringComparison.OrdinalIgnoreCase` durante il confronto. |
| Il file non si carica | Licenza Aspose.CAD mancante in produzione | Applica una licenza valida prima di caricare l'immagine. |

## Conclusione

Ora sai come **change xref path**, **update block reference** e **manage CAD hyperlinks** usando Aspose.CAD per .NET. Queste funzionalità ti consentono di mantenere organizzati grandi progetti CAD e liberi da riferimenti interrotti, migliorando l'affidabilità nei flussi di lavoro automatizzati.

## FAQ

### Q1: Aspose.CAD è compatibile con altri formati di file CAD?

A1: Sì, Aspose.CAD supporta vari formati CAD, tra cui DWG, DXF, DGN e altri.

### Q2: Posso provare Aspose.CAD prima di acquistarlo?

A2: Assolutamente! Puoi accedere a una prova gratuita [qui](https://releases.aspose.com/).

### Q3: Dove posso trovare la documentazione dettagliata per Aspose.CAD?

A3: Consulta la documentazione [qui](https://reference.aspose.com/cad/net/).

### Q4: Come posso ottenere una licenza temporanea per Aspose.CAD?

A4: Ottieni una licenza temporanea [qui](https://purchase.aspose.com/temporary-license/).

### Q5: Hai bisogno di assistenza o hai domande?

A5: Visita il nostro forum di supporto [qui](https://forum.aspose.com/c/cad/19).

## Ulteriori domande frequenti

**Q: Posso cambiare programmaticamente più percorsi XRef in un'unica passata?**  
A: Sì, itera attraverso tutte le entità `CadInsertObject` e imposta `XRefPathName.Value` secondo necessità.

**Q: La modifica del percorso XRef influisce sull'aspetto visivo del disegno?**  
A: Il riferimento viene aggiornato, ma il disegno mostrerà il nuovo file esterno quando aperto in un visualizzatore CAD.

**Q: Esiste un modo per elencare tutti i collegamenti ipertestuali attuali in un file CAD?**  
A: Scorri `cadImage.Entities` e raccogli i valori `entity.Hyperlink` che non sono null o vuoti.

**Q: Questo approccio funziona con file DWG di grandi dimensioni (centinaia di MB)?**  
A: Aspose.CAD è ottimizzato per le prestazioni, ma assicurati di avere memoria sufficiente e considera l'elaborazione a blocchi se necessario.

---

**Last Updated:** 2026-03-05  
**Tested With:** Aspose.CAD 24.12 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}