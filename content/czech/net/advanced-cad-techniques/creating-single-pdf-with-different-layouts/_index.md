---
title: Vytváření jednoho PDF s různými rozvrženími - Průvodce Aspose.CAD
linktitle: Vytváření jednoho PDF s různými rozvrženími
second_title: Aspose.CAD .NET – formát souborů CAD a BIM
description: Vytvořte jedno PDF s různými rozvrženími pomocí Aspose.CAD for .NET. Postupujte podle našeho podrobného průvodce pro bezproblémovou integraci a efektivní generování PDF.
type: docs
weight: 13
url: /cs/net/advanced-cad-techniques/creating-single-pdf-with-different-layouts/
---
## Úvod

Chcete vygenerovat jeden dokument PDF z výkresu CAD s různými rozvrženími pomocí Aspose.CAD pro .NET? Tento průvodce vás krok za krokem provede celým procesem a pomůže vám dosáhnout bezproblémové integrace a efektivního vytváření PDF. Aspose.CAD for .NET poskytuje výkonné funkce pro programovou manipulaci s výkresy CAD a v tomto tutoriálu se zaměříme na vytvoření jednoho PDF s různými rozvrženími.

## Předpoklady

Než se ponoříte do výukového programu, ujistěte se, že máte následující předpoklady:

-  Aspose.CAD for .NET: Ujistěte se, že máte nainstalovaný Aspose.CAD for .NET. Můžete si jej stáhnout z[tady](https://releases.aspose.com/cad/net/).

- Vývojové prostředí: Nastavte vývojové prostředí .NET a mějte základní znalosti o programování v C#.

## Importovat jmenné prostory

Do svého projektu v C# zahrňte potřebné jmenné prostory pro využití funkcí Aspose.CAD pro .NET:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Krok 1: Načtěte obrázek CAD

```csharp
// Cesta k adresáři dokumentů.
string MyDir = "Your Document Directory";

using (CadImage cadImage = (CadImage)Image.Load(MyDir + "City skyway map.dwg"))
{
    // Zde je váš kód pro krok 1
}
```

## Krok 2: Přizpůsobte možnosti rastrování

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1000;
rasterizationOptions.PageHeight = 1000;

// Vlastní velikosti pro několik rozvržení
rasterizationOptions.LayoutPageSizes.Add("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.LayoutPageSizes.Add("8.5 x 11 Plot", new SizeF(1000, 100));
```

## Krok 3: Definujte možnosti PDF

```csharp
PdfOptions pdfOptions = new PdfOptions() { VectorRasterizationOptions = rasterizationOptions };
```

## Krok 4: Uložit jako PDF

```csharp
cadImage.Save(MyDir + "singlePDF_out.pdf", pdfOptions);
```

Nyní jste úspěšně vytvořili jeden dokument PDF s různými rozvrženími pomocí Aspose.CAD for .NET. Neváhejte prozkoumat další funkce a upravit kód podle svých konkrétních požadavků.

## Závěr

V tomto tutoriálu jsme se zabývali procesem vytváření jednoho PDF z výkresu CAD s různými rozvrženími pomocí Aspose.CAD for .NET. Tato výkonná knihovna zjednodušuje manipulační úlohy CAD a nabízí flexibilitu pro různé scénáře.

## FAQ

### Q1: Mohu použít Aspose.CAD pro .NET s jinými formáty CAD?

Odpověď 1: Ano, Aspose.CAD for .NET podporuje různé formáty CAD, jako je DWG, DXF, DGN a další.

### Q2: Je k dispozici bezplatná zkušební verze?

 A2: Ano, můžete prozkoumat bezplatnou zkušební verzi[tady](https://releases.aspose.com/).

### Q3: Jak mohu získat podporu pro Aspose.CAD pro .NET?

 A3: Navštivte[Fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) za podporu komunity.

### Q4: Kde najdu podrobnou dokumentaci?

 A4: Viz dokumentace[tady](https://reference.aspose.com/cad/net/).

### Q5: Mohu si zakoupit licenci pro Aspose.CAD pro .NET?

 A5: Ano, můžete si koupit licenci[tady](https://purchase.aspose.com/buy).