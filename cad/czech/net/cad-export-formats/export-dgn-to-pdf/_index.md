---
title: Export DGN do PDF v Aspose.CAD pro .NET
linktitle: Export DGN do PDF
second_title: Aspose.CAD .NET – formát souborů CAD a BIM
description: Naučte se, jak exportovat soubory DGN do PDF bez námahy pomocí Aspose.CAD pro .NET. Podrobný průvodce pro bezproblémovou manipulaci se soubory CAD.
weight: 12
url: /cs/net/cad-export-formats/export-dgn-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export DGN do PDF v Aspose.CAD pro .NET

## Úvod

Ve světě vývoje .NET je Aspose.CAD výkonná knihovna, která usnadňuje manipulaci a konverzi souborů CAD. Jedním z běžných úkolů, s nimiž se vývojáři často setkávají, je export souborů DGN do formátu PDF. V tomto tutoriálu projdeme procesem krok za krokem pomocí Aspose.CAD for .NET.

## Předpoklady

Než se pustíte do výukového programu, ujistěte se, že máte na místě následující:

- Pracovní znalost C# a .NET frameworku.
-  Nainstalovaná knihovna Aspose.CAD for .NET. Můžete si jej stáhnout[tady](https://releases.aspose.com/cad/net/).
- Ukázkový soubor DGN, například „Nikon_D90_Camera.dgn“ pro tento výukový program.

## Importovat jmenné prostory

Ve svém projektu C# začněte importováním potřebných jmenných prostorů:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Krok 1: Načtěte soubor DGN

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage cadImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Váš kód zde...
}
```

## Krok 2: Nakonfigurujte možnosti rastrování

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## Krok 3: Vytvořte možnosti PDF

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Krok 4: Uložit jako PDF

```csharp
cadImage.Save(MyDir + "ExportDGNToPdf_out.pdf", pdfOptions);
```

## Závěr

Gratulujeme! Úspěšně jste exportovali soubor DGN do PDF pomocí Aspose.CAD for .NET. Tento tutoriál se zabýval základními kroky, od načtení souboru DGN po konfiguraci možností rasterizace a uložení výstupu jako PDF.

## FAQ

### Q1: Mohu používat Aspose.CAD pro .NET bez předchozích znalostí CAD?

A1: Rozhodně! Aspose.CAD zjednodušuje složité úlohy CAD a zpřístupňuje jej vývojářům s různým zázemím.

### Q2: Kde najdu další příklady a dokumentaci pro Aspose.CAD?

 A2: Prozkoumejte[dokumentace](https://reference.aspose.com/cad/net/) pro komplexní návody a příklady.

### Q3: Je k dispozici bezplatná zkušební verze pro Aspose.CAD?

A3: Ano, můžete získat bezplatnou zkušební verzi[tady](https://releases.aspose.com/).

### Q4: Jak mohu získat dočasné licence pro Aspose.CAD?

 A4: Získejte dočasné licence[tady](https://purchase.aspose.com/temporary-license/).

### Q5: Potřebujete pomoc nebo máte otázky?

A5: Navštivte[Fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) za podporu komunity.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
