---
title: Export objektů OLE ze souborů DWG - Výukový program Aspose.CAD
linktitle: Export objektů OLE ze souborů DWG
second_title: Aspose.CAD .NET – formát souborů CAD a BIM
description: Prozkoumejte podrobného průvodce exportem objektů OLE ze souborů DWG pomocí Aspose.CAD for .NET. Vylepšete své dovednosti při manipulaci se soubory CAD bez námahy.
weight: 12
url: /cs/net/advanced-export-techniques/exporting-ole-objects-from-dwg/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export objektů OLE ze souborů DWG - Výukový program Aspose.CAD

## Úvod

Chcete snadno extrahovat objekty OLE ze souborů DWG? Aspose.CAD pro .NET je zde, aby vám zefektivnil proces. V tomto tutoriálu vás provedeme exportem objektů OLE krok za krokem a zajistíme vám, abyste co nejlépe využili tuto výkonnou knihovnu .NET. 

## Předpoklady

Než se pustíme do výukového programu, ujistěte se, že máte splněny následující předpoklady:

-  Aspose.CAD for .NET Library: Ujistěte se, že máte nainstalovanou knihovnu. Můžete si jej stáhnout z[Stránka ke stažení Aspose.CAD for .NET](https://releases.aspose.com/cad/net/).

-  Adresář dokumentů: Nastavte adresář, kde jsou uloženy vaše soubory DWG. Nahradit`"Your Document Directory"` v poskytnutém fragmentu kódu se skutečnou cestou.

## Importovat jmenné prostory

Ve svém projektu .NET budete muset importovat potřebné jmenné prostory, abyste mohli využívat funkce Aspose.CAD. Použijte následující fragment kódu:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Krok 1: Nastavte adresář dokumentů

```csharp
string MyDir = "Your Document Directory";
```

 Nahradit`"Your Document Directory"` s cestou, kde jsou umístěny vaše soubory DWG.

## Krok 2: Zadejte soubory DWG

```csharp
string[] files = new string[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

Vypište soubory DWG, které chcete v rámci pole zpracovat.

## Krok 3: Nakonfigurujte možnosti exportu

```csharp
PngOptions pngOptions = new PngOptions { };
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.VectorRasterizationOptions = rasterizationOptions;
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

Přizpůsobte možnosti exportu podle svých požadavků. V tomto příkladu nakonfigurujeme export PNG se zadaným rozložením.

## Krok 4: Iterujte soubory a exportujte

```csharp
foreach (string file in files)
{
    using (CadImage cadImage = (CadImage)Image.Load(MyDir + file))
    {
        cadImage.Save(MyDir + file + "_out.png", pngOptions);
    }
}
```

Iterujte zadané soubory DWG, načtěte každý z nich a uložte exportovaný soubor PNG s definovanými možnostmi.

## Závěr

Gratulujeme! Úspěšně jste exportovali OLE objekty ze souborů DWG pomocí Aspose.CAD for .NET. Tato výkonná knihovna zjednodušuje složité úkoly a poskytuje efektivitu a flexibilitu při manipulaci se soubory CAD.

## FAQ

### Q1: Je Aspose.CAD for .NET vhodný pro juniorské i starší CAD soubory?

A1: Ano, Aspose.CAD for .NET je všestranný a dokáže zpracovat širokou škálu CAD souborů, včetně juniorských i starších variant.

### Q2: Mohu přizpůsobit možnosti exportu pro různá rozvržení?

A2: Rozhodně! Jak je uvedeno ve výukovém programu, můžete upravit možnosti exportu, včetně rozvržení, tak, aby vyhovovaly vašim konkrétním potřebám.

### Q3: Kde najdu podrobnou dokumentaci k Aspose.CAD pro .NET?

 A3: Prozkoumejte[Dokumentace Aspose.CAD pro .NET](https://reference.aspose.com/cad/net/) pro podrobné informace a příklady.

### Q4: Je k dispozici bezplatná zkušební verze?

 A4: Ano, můžete vyzkoušet možnosti Aspose.CAD pro .NET s bezplatnou zkušební verzí. Návštěva[tento odkaz](https://releases.aspose.com/) začít.

### Q5: Jak mohu získat podporu nebo se spojit s komunitou?

 A5: Pro podporu a zapojení komunity navštivte[Fórum Aspose.CAD](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
