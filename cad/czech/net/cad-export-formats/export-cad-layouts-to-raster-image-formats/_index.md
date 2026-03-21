---
date: 2026-03-21
description: Naučte se, jak převést DXF na PNG a další rastrové formáty pomocí Aspose.CAD
  pro .NET. Postupujte podle našeho krok‑za‑krokem průvodce pro bezproblémový export
  vrstev CAD.
linktitle: Export CAD Layouts to Raster Image Formats
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Převod DXF na PNG pomocí Aspose.CAD pro .NET
url: /cs/net/cad-export-formats/export-cad-layouts-to-raster-image-formats/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export rozvržení CAD do rastrových formátů obrázků v Aspose.CAD pro .NET

## Úvod

Hledáte efektivní **convert dxf to png** a další rastrové formáty obrázků pomocí Aspose.CAD pro .NET? Tento krok‑za‑krokem průvodce vás provede procesem, poskytne podrobné instrukce a úryvky kódu, aby byl úkol bezproblémový. Ať už jste zkušený vývojář nebo nováček v Aspose.CAD, tento tutoriál je určen pro všechny úrovně odbornosti.

### Rychlé odpovědi
- **Která knihovna provádí konverzi?** Aspose.CAD for .NET  
- **Primární formát podporovaný bez další konfigurace?** JPEG, PNG, BMP a TIFF rastrové obrázky  
- **Mohu exportovat konkrétní vrstvy CAD?** Ano – použijte `CadRasterizationOptions.Layers` k cílení jednotlivých vrstev  
- **Potřebuji licenci pro produkci?** Platná licence Aspose.CAD je vyžadována pro ne‑zkušební použití  
- **Podporované verze .NET?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7  

## Co je **convert dxf to png**?

Převod souboru DXF (Drawing Exchange Format) na PNG znamená rasterizaci vektorových CAD dat do pixelového obrázku. To je užitečné, když potřebujete vložit CAD výkresy do webových stránek, reportů nebo jakéhokoli prostředí, které podporuje jen rastrovou grafiku.

## Proč exportovat vrstvy CAD samostatně?

Exportování vrstev CAD jednotlivě vám dává detailní kontrolu nad vizuálním výstupem, snižuje velikost souboru pro každý obrázek a umožňuje aplikovat specifické stylování nebo post‑processing na konkrétní vrstvy. To je zvláště užitečné u velkých inženýrských výkresů, kde je relevantní jen podmnožina vrstev pro konkrétní publikum.

## Požadavky

- **Aspose.CAD for .NET Library** – stáhněte ji z [Aspose.CAD website](https://releases.aspose.com/cad/net/).  
- **CAD Drawing File** – soubor DXF (např. `conic_pyramid.dxf`), který chcete převést do rastrových formátů.  

## Importování jmenných prostorů

Ve vašem .NET projektu importujte potřebné jmenné prostory, abyste mohli využívat funkce Aspose.CAD. Přidejte následující jmenné prostory na začátek vašeho kódu:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Jak **convert dxf to png** – krok za krokem průvodce

### Krok 1: Načtení CAD výkresu

Nejprve načtěte soubor DXF do objektu `Image`. Tento objekt představuje celý CAD výkres v paměti.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

// Load a CAD drawing in an instance of Image
using (var image = Image.Load(sourceFilePath))
{
    // Your code for loading the CAD drawing goes here
}
```

### Krok 2: Vytvoření `CadRasterizationOptions`

Nastavte možnosti rasterizace, jako jsou rozměry výstupu a rozlišení. Tyto možnosti řídí, jak jsou vektorová data rasterizována.

```csharp
// Create an instance of CadRasterizationOptions
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
```

### Krok 3: Specifikace vrstev (Export CAD vrstev)

Pokud potřebujete jen konkrétní vrstvu, uveďte zde její název. Toto ukazuje **export cad layers** jednotlivě.

```csharp
// Add the layer name to the CadRasterizationOptions's layer list
rasterizationOptions.Layers = new string[] { "LayerA" };
```

### Krok 4: Výběr formátu obrázku – Uložení CAD jako PNG (nebo JPEG)

Vytvořte objekt s možnostmi specifickými pro formát obrázku. Nahraďte `JpegOptions` za `PngOptions`, když chcete **save cad as png**.

```csharp
// Create an instance of JpegOptions (or any ImageOptions for raster formats)
var options = new JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
```

> **Tip:** Pro generování PNG souborů jednoduše vytvořte `new PngOptions()` místo `JpegOptions`.

### Krok 5: Export do formátu JPEG (nebo PNG)

Nakonec uložte rasterizovaný obrázek na disk. Přípona souboru určuje výstupní formát.

```csharp
// Export each layer to Jpeg format
MyDir = MyDir + "CADLayersToRasterImageFormats_out.jpg";
image.Save(MyDir, options);
```

Když nahradíte `JpegOptions` za `PngOptions`, stejný kód **convert dxf to png** a vytvoří soubor `.png`.

### Další krok: Převod všech vrstev

Pokud potřebujete **convert cad to raster** pro každou vrstvu ve výkresu, zavolejte níže uvedenou pomocnou metodu. Projde všechny vrstvy a uloží každou jako samostatný obrázek.

```csharp
ConvertAllLayersToRasterImageFormats();
```

> *Poznámka:* Implementace `ConvertAllLayersToRasterImageFormats` je součástí kompletní sady vzorových kódů Aspose.CAD a demonstruje hromadné zpracování vrstev.

## Časté problémy a řešení

| Příznak | Pravděpodobná příčina | Oprava |
|---------|----------------------|--------|
| Prázdný nebo bílý obrázek | Možnosti rasterizace nejsou nastaveny (např. `PageWidth`/`PageHeight` = 0) | Zajistěte, aby `PageWidth` a `PageHeight` měly kladné hodnoty |
| Chybějící vrstvy | Nesprávný název vrstvy v poli `Layers` | Ověřte přesný název vrstvy v CAD souboru (rozlišuje velká a malá písmena) |
| PNG nízké kvality | Výchozí DPI je nízké | Nastavte `rasterizationOptions.Resolution = 300;` pro vyšší kvalitu |

## Často kladené otázky (Originální)

### Q1: Mohu použít jiné formáty obrázků pro export?
A1: Ano, můžete. Jednoduše nahraďte `JpegOptions` možnostmi požadovaného formátu, například `PngOptions` nebo `BmpOptions`.

### Q2: Je k dispozici zkušební verze?
A2: Ano, můžete si vyzkoušet funkce Aspose.CAD stažením zkušební verze [zde](https://releases.aspose.com/).

### Q3: Jak mohu získat podporu pro Aspose.CAD?
A3: Navštivte fórum Aspose.CAD [forum](https://forum.aspose.com/c/cad/19) pro komunitní podporu nebo zvažte zakoupení licence pro dedikovanou podporu.

### Q4: Jsou k dispozici dočasné licence?
A4: Ano, dočasnou licenci můžete získat [zde](https://purchase.aspose.com/temporary-license/).

### Q5: Kde najdu dokumentaci?
A5: Podrobnou dokumentaci najdete [zde](https://reference.aspose.com/cad/net/).

## Další FAQ

**Q: Mohu exportovat všechny vrstvy jedním příkazem?**  
A: Ano, použijte metodu `ConvertAllLayersToRasterImageFormats` uvedenou výše.

**Q: Podporuje Aspose.CAD vektorové formáty jako SVG?**  
A: Primárně cílí na rastrové formáty, ale můžete exportovat do PDF, který zachovává vektorová data.

**Q: Jak mohu nastavit barvu pozadí exportovaného PNG?**  
A: Nastavte `rasterizationOptions.BackgroundColor` na požadovanou `Color` před uložením.

**Q: Je možné exportovat jediný rozvržení místo celého výkresu?**  
A: Ano, nakonfigurujte `rasterizationOptions.Layouts`, abyste specifikovali název(y) rozvržení, které chcete rasterizovat.

## Závěr

Nyní jste se naučili, jak **convert dxf to png**, **export cad layers** a **save cad as png** nebo JPEG pomocí Aspose.CAD pro .NET. Úpravou `CadRasterizationOptions` a výměnou možností formátu obrázku můžete přizpůsobit konverzi prakticky jakémukoli rastrovému výstupu, který potřebujete. Prozkoumejte další formátové možnosti v API Aspose.CAD a rozšiřte svůj workflow převodu CAD na raster.

---

**Last Updated:** 2026-03-21  
**Tested With:** Aspose.CAD for .NET 24.11 (nejnovější v době psaní)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}