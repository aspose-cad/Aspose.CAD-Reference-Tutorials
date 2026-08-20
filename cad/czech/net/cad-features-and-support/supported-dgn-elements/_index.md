---
date: 2026-03-29
description: Naučte se, jak převést DGN na PNG pomocí Aspose.CAD pro .NET. Tento průvodce
  také pokrývá podporu formátů CAD souborů a kompletní sadu podporovaných prvků DGN.
linktitle: Supported DGN Elements
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Převod DGN na PNG pomocí Aspose.CAD pro .NET
url: /cs/net/cad-features-and-support/supported-dgn-elements/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Převod DGN na PNG pomocí Aspose.CAD pro .NET

## Úvod

Jste vývojář .NET, který hledá **převod DGN na PNG** bez problémů? Aspose.CAD pro .NET poskytuje robustní řešení pro efektivní práci se soubory DGN. V tomto tutoriálu se podíváme na podporované prvky DGN, provedeme vás procesem práce s Aspose.CAD pro .NET a ukážeme vám přesně, jak exportovat tyto prvky do PNG obrázků.

## Rychlé odpovědi
- **Co Aspose.CAD dělá?** Čte, upravuje a převádí CAD/BIM soubory (včetně DGN) do rastrových formátů, jako je PNG.  
- **Mohu převádět 2D a 3D DGN prvky?** Ano – jsou podporovány jak 2‑D, tak 3‑D entity.  
- **Jaké verze .NET jsou vyžadovány?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Potřebuji licenci pro testování?** K dispozici je bezplatná zkušební verze; licence je vyžadována pro produkci.  
- **Kde získám knihovnu?** Stáhněte ji z oficiálního webu Aspose (odkaz níže).

## Co znamená „převod DGN na PNG“?
Převod DGN na PNG znamená vykreslení vektorového výkresu DGN (2‑D nebo 3‑D) do rastrového formátu obrázku (PNG). To je užitečné, když potřebujete zobrazit CAD výkresy na webu, vložit je do zpráv nebo generovat náhledy bez nutnosti CAD prohlížeče.

## Proč použít Aspose.CAD pro .NET pro podporu CAD formátů?
- **Kompletní podpora CAD formátů** – DGN, DWG, DXF, DWF a další.  
- **Žádné externí závislosti** – čistá .NET knihovna, bez nativních CAD instalací.  
- **Vysoká věrnost renderování** – zachovává tloušťky čar, barvy a 3‑D geometrii.  
- **Dávkové zpracování** – snadno procházet mnoho souborů v aplikaci na straně serveru.

## Požadavky

Before we begin, make sure you have the following:

- Základní znalost programování v .NET.  
- Nainstalovaný Visual Studio na vašem počítači.  
- Knihovna Aspose.CAD pro .NET, kterou můžete stáhnout [zde](https://releases.aspose.com/cad/net/).

## Importování jmenných prostorů

To kickstart your project, import the necessary namespaces into your .NET application. This step ensures that you have access to the functionalities provided by Aspose.CAD for .NET.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.FileFormats.Dgn.DgnElements;
```

## Jak převést DGN na PNG

Below is a step‑by‑step guide that walks you through loading a DGN file, iterating its elements, handling both 2‑D and 3‑D entities, and finally exporting the result to a PNG raster image.

### Krok 1: Načtení souboru DGN

Begin by loading an existing DGN file as a `DgnImage` in your .NET application.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Your code here
}
```

### Krok 2: Procházení DGN prvků

Iterate through the DGN elements using a `foreach` loop. Aspose.CAD for .NET provides a variety of DGN element types that you can work with.

```csharp
foreach (DgnDrawingElementBase element in dgnImage.Elements)
{
    // Your code here
}
```

### Krok 3: Zpracování dříve podporovaných 2‑D entit

These entities are now also supported for 3‑D rendering. The switch statement lets you branch logic based on the element type.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.Line:
    case DgnElementType.Ellipse:
    case DgnElementType.Curve:
    // Additional cases
        {
            // Your code here
            break;
        }
}
```

### Krok 4: Zpracování podporovaných 3‑D entit

Aspose.CAD adds full support for several 3‑D DGN elements. Extend the switch to process them as needed.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.SolidHeader3D:
    case DgnElementType.Cone:
    case DgnElementType.CellHeader:
        {
            // Your code here
            break;
        }
}
```

### Krok 5: Export a uložení jako PNG

After any required manipulation, export the DGN drawing to a PNG raster image and save it to the specified directory.

```csharp
Console.WriteLine("\nThe DGN file exported successfully to raster image.\nFile saved at " + MyDir);
```

> **Tip:** Použijte `Image.Save` s `new PngOptions()` pro nastavení rozlišení, barvy pozadí a dalších specifických nastavení PNG.

## Přehled podpory CAD formátů

Aspose.CAD for .NET isn’t limited to DGN. It also supports DWG, DXF, DWF, and many other CAD formats, giving you a single API to handle a broad spectrum of engineering drawings. This makes it ideal for projects that require **CAD file format support** across multiple standards.

## Časté problémy a řešení

| Problém | Důvod | Řešení |
|-------|--------|-----|
| **Obrázek je prázdný** | Exportováno s nulovým DPI | Zadejte `ResolutionX` a `ResolutionY` v `PngOptions`. |
| **Chybí 3‑D geometrie** | Typ prvku není ve switchu ošetřen | Přidejte chybějící případ `DgnElementType` a renderujte podle toho. |
| **Nedostatek paměti u velkých souborů** | Načítání celého souboru najednou | Zpracovávejte prvky po dávkách nebo použijte streamování, kde je to možné. |

## Často kladené otázky

### Q1: Kde najdu dokumentaci k Aspose.CAD pro .NET?
A1: Můžete najít dokumentaci [zde](https://reference.aspose.com/cad/net/).

### Q2: Jak si mohu stáhnout Aspose.CAD pro .NET?
A2: Knihovnu můžete stáhnout [zde](https://releases.aspose.com/cad/net/).

### Q3: Je k dispozici bezplatná zkušební verze Aspose.CAD pro .NET?
A3: Ano, můžete získat bezplatnou zkušební verzi [zde](https://releases.aspose.com/).

### Q4: Kde mohu získat dočasné licence pro Aspose.CAD pro .NET?
A4: Dočasné licence jsou k dispozici [zde](https://purchase.aspose.com/temporary-license/).

### Q5: Potřebujete pomoc nebo máte otázky?
A5: Navštivte komunitní [fórum podpory](https://forum.aspose.com/c/cad/19) Aspose.CAD pro .NET.

---

**Poslední aktualizace:** 2026-03-29  
**Testováno s:** Aspose.CAD for .NET 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}