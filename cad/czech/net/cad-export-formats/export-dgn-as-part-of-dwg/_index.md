---
title: Exportujte DGN jako součást DWG v Aspose.CAD pro .NET
linktitle: Export DGN jako součást DWG
second_title: Aspose.CAD .NET – formát souborů CAD a BIM
description: Přečtěte si, jak exportovat DGN jako součást DWG v Aspose.CAD pro .NET. Postupujte podle našeho podrobného průvodce pro bezproblémovou integraci.
type: docs
weight: 11
url: /cs/net/cad-export-formats/export-dgn-as-part-of-dwg/
---
## Úvod

Ve světě vývoje .NET vyniká Aspose.CAD jako výkonná knihovna pro práci se soubory CAD (Computer-Aided Design). Tento tutoriál vás provede procesem exportu souboru DGN (Design) jako součásti souboru DWG (Drawing) pomocí Aspose.CAD for .NET. Ať už jste zkušený vývojář nebo teprve začínáte, tento podrobný průvodce vám pomůže využít možnosti Aspose.CAD k efektivnímu dosažení tohoto konkrétního úkolu.

## Předpoklady

Než se pustíte do výukového programu, ujistěte se, že máte splněny následující předpoklady:

-  Aspose.CAD for .NET: Ujistěte se, že máte nainstalovanou knihovnu Aspose.CAD pro .NET. Můžete si jej stáhnout[tady](https://releases.aspose.com/cad/net/).

- Vývojové prostředí: Nastavte si preferované vývojové prostředí .NET, jako je Visual Studio.

- Základní znalost C#: Seznamte se s programovacím jazykem C#.

## Importovat jmenné prostory

Ve svém projektu C# zahrňte potřebné jmenné prostory pro přístup k funkcím Aspose.CAD. Přidejte následující pomocí direktiv na začátek souboru kódu:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

Nyní rozdělme poskytnutý kód do několika kroků:

## Krok 1: Definujte cesty k souboru

```csharp
//Vstupní a výstupní cesty k souboru
string fileName = "BlockRefDgn.dwg";
string outPath = fileName + ".pdf";
```

## Krok 2: Vytvořte instanci PdfOptions

```csharp
// Vytvořte instanci třídy PdfOptions pro export DWG do PDF
PdfOptions exportOptions = new PdfOptions();
```

## Krok 3: Načtěte soubor DWG

```csharp
// Načtěte existující soubor DWG jako obrázek a převeďte jej na typ CadImage
using (CadImage cadImage = (CadImage)Image.Load(fileName))
```

## Krok 4: Iterujte přes entity

```csharp
// Iterujte každou entitu uvnitř souboru DWG
foreach (CadBaseEntity baseEntity in cadImage.Entities)
```

## Krok 5: Zkontrolujte typ entity

```csharp
// Zkontrolujte, zda je entita definicí obrázku
if (baseEntity.TypeName == CadEntityTypeName.DGNUNDERLAY)
```

## Krok 6: Získejte cestu podkladu

```csharp
// Pokud se jedná o definici obrázku, získejte externí odkaz na objekt
CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
Console.WriteLine(dgnFile.UnderlayPath);
```

## Krok 7: Definujte možnosti rastrování

```csharp
// Definujte nastavení pro objekt CadRasterizationOptions
exportOptions.VectorRasterizationOptions = new CadRasterizationOptions()
{
    PageWidth = 1600,
    PageHeight = 1600,
    Layouts = new string[] { "Model" },
    AutomaticLayoutsScaling = false,
    NoScaling = true,
    BackgroundColor = Color.Black,
    DrawType = CadDrawTypeMode.UseObjectColor
};
```

## Krok 8: Export DWG do PDF

```csharp
// Exportujte DWG do PDF voláním metody Uložit
cadImage.Save(outPath, exportOptions);
```

## Závěr

Gratulujeme! Úspěšně jste prošli procesem exportu souboru DGN jako součásti souboru DWG pomocí Aspose.CAD for .NET. Tento výukový program vám poskytl základní kroky a úryvky kódu pro bezproblémové dosažení tohoto konkrétního úkolu.

## FAQ

### Q1: Mohu použít Aspose.CAD pro .NET ve svých komerčních projektech?
 A1: Ano, můžete. Návštěva[tady](https://purchase.aspose.com/buy) prozkoumat možnosti licencování.

### Otázka 2: Existují nějaká omezení velikosti souborů DWG, které mohu zpracovat?
Odpověď 2: Aspose.CAD podporuje zpracování velkých souborů DWG, ale mohou platit hardwarová omezení.

### Q3: Je k dispozici zkušební verze?
A3: Ano, můžete získat bezplatnou zkušební verzi[tady](https://releases.aspose.com/).

### Q4: Jak mohu získat dočasné licence?
 A4: Lze získat dočasné licence[tady](https://purchase.aspose.com/temporary-license/).

### Q5: Kde mohu vyhledat pomoc, pokud narazím na problémy?
 A5: Můžete navštívit fórum Aspose.CAD[tady](https://forum.aspose.com/c/cad/19) pro podporu.