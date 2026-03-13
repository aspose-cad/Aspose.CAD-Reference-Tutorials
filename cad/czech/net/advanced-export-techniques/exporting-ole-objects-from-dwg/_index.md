---
description: Naučte se, jak převést DWG na PNG a extrahovat OLE objekty z DWG souborů
  pomocí Aspose.CAD pro .NET – rychlý průvodce zaměřený na kód.
linktitle: Exporting OLE Objects from DWG Files
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Převod DWG na PNG a export OLE objektů – tutoriál Aspose.CAD
url: /cs/net/advanced-export-techniques/exporting-ole-objects-from-dwg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportování OLE objektů ze souborů DWG – tutoriál Aspose.CAD

## Introduction

Pokud potřebujete **convert DWG to PNG** a zároveň vytáhnout vložené OLE objekty, jste na správném místě. Aspose.CAD pro .NET zjednodušuje tento dvoustupňový proces, umožňuje automatizovat extrakci a rasterizaci pomocí několika řádků C#. V následujících minutách projdeme celý workflow, od nastavení prostředí až po uložení každého DWG jako PNG, který obsahuje extrahovaná OLE data.

## Quick Answers
- **Co tento tutoriál pokrývá?** Převod DWG na PNG a extrakce OLE objektů pomocí Aspose.CAD pro .NET.  
- **Potřebuji licenci?** Bezplatná zkušební verze stačí pro vývoj; pro produkci je vyžadována komerční licence.  
- **Které verze .NET jsou podporovány?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Mohu zpracovávat více souborů DWG najednou?** Ano – ukázka prochází pole názvů souborů.  
- **Kde najdu další příklady?** Podívejte se na oficiální dokumentaci Aspose.CAD a odkazy na fórum níže.

## What is **convert DWG to PNG**?
Převod DWG (kresba AutoCAD) na PNG obrázek rasterizuje vektorová data, což usnadňuje jejich zobrazení nebo vložení do webových stránek, reportů či jiných aplikací, které nativně DWG nepodporují. Pokud jsou přítomny OLE objekty, lze je během převodu extrahovat a uložit jako samostatná aktiva.

## Why extract OLE objects from CAD files?
Mnoho výkresů DWG vkládá tabulky, grafy nebo jiné dokumenty Office jako OLE objekty. Jejich extrakce vám umožní znovu použít původní data, automatizovat reportování nebo migrovat obsah do novějších formátů, aniž byste ztratili vložené informace.

## Prerequisites

- Aspose.CAD pro .NET knihovna: Ujistěte se, že máte knihovnu nainstalovanou. Můžete ji stáhnout ze [Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/).
- Dokumentový adresář: Vytvořte adresář, kde jsou uloženy vaše soubory DWG. Nahraďte `"Your Document Directory"` v poskytnutém kódu skutečnou cestou.

## Import Namespaces

Ve vašem .NET projektu importujte požadované jmenné prostory:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Step‑by‑Step Guide

### Step 1: Set the Document Directory

Nahraďte `"Your Document Directory"` cestou, kde jsou umístěny vaše soubory DWG.

```csharp
string MyDir = "Your Document Directory";
```

### Step 2: List the DWG files you want to process

```csharp
string[] files = new string[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

### Step 3: Configure export options for PNG conversion

```csharp
PngOptions pngOptions = new PngOptions { };
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.VectorRasterizationOptions = rasterizationOptions;
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

Můžete upravit `CadRasterizationOptions` (např. `PageWidth`, `PageHeight`, `BackgroundColor`) tak, aby odpovídaly požadovanému rozlišení výstupu.

### Step 4: Iterate through each DWG and perform the conversion

```csharp
foreach (string file in files)
{
    using (CadImage cadImage = (CadImage)Image.Load(MyDir + file))
    {
        cadImage.Save(MyDir + file + "_out.png", pngOptions);
    }
}
```

Během této smyčky knihovna automaticky **extracts OLE objects** vložené v každém výkresu a zahrne je do vytvořeného PNG. Pokud potřebujete surové OLE streamy, můžete přistupovat ke kolekci `cadImage.OleObjects` – praktický způsob, jak **how to extract ole** data programově.

## Common Issues & Troubleshooting

- **Missing layout name** – Ujistěte se, že layout, který specifikujete (`"Layout1"` v příkladu), existuje ve zdrojovém DWG; jinak se rasterizér vrátí k výchozímu modelovému prostoru.
- **Large files cause memory pressure** – Zpracovávejte soubory po jednom (jak je ukázáno) a okamžitě uvolňujte objekty `CadImage` pomocí `using`.
- **Unexpected colors** – Nastavte `rasterizationOptions.BackgroundColor` tak, aby odpovídala pozadí výkresu, pokud je vyžadována transparentnost.

## Frequently Asked Questions

### Q1: Je Aspose.CAD pro .NET vhodný jak pro junior, tak pro senior CAD soubory?
A1: Ano, Aspose.CAD pro .NET je univerzální a dokáže zpracovat širokou škálu CAD souborů, včetně jak junior, tak senior variant.

### Q2: Mohu přizpůsobit možnosti exportu pro různé layouty?
A2: Rozhodně! Jak je ukázáno v tutoriálu, můžete upravit možnosti exportu, včetně layoutů, aby vyhovovaly vašim konkrétním potřebám.

### Q3: Kde najdu podrobnou dokumentaci pro Aspose.CAD pro .NET?
A3: Prozkoumejte [Aspose.CAD for .NET documentation](https://reference.aspose.com/cad/net/) pro podrobné informace a příklady.

### Q4: Je k dispozici bezplatná zkušební verze?
A4: Ano, můžete vyzkoušet možnosti Aspose.CAD pro .NET pomocí bezplatné zkušební verze. Navštivte [this link](https://releases.aspose.com/) a začněte.

### Q5: Jak mohu získat podporu nebo se spojit s komunitou?
A5: Pro podporu a zapojení do komunity navštivte [Aspose.CAD forum](https://forum.aspose.com/c/cad/19).

### Q6: Jak **extract OLE from CAD** soubory bez převodu na PNG?
A6: Použijte kolekci `CadImage.OleObjects` po načtení DWG; můžete iterovat přes každý `OleObject` a uložit jeho surová data do souboru.

## Conclusion

Nyní jste viděli, jak **convert DWG to PNG** a zároveň plynule **extracting OLE objects** pomocí Aspose.CAD pro .NET. Tento přístup šetří čas, eliminuje ruční kroky kopírování a vkládání a čistě se integruje do automatizovaných pipeline. Klidně experimentujte s dalšími rastrovými formáty (JPEG, BMP) nebo prozkoumejte bohatou sadu funkcí pro manipulaci s CAD, které Aspose nabízí.

---

**Poslední aktualizace:** 2026-03-13  
**Testováno s:** Aspose.CAD 24.11 pro .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}