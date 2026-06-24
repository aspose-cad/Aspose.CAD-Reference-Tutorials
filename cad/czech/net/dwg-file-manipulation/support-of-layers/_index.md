---
date: 2026-04-09
description: Naučte se exportovat vrstvy DWG, převádět obrázek DWG a ukládat DWG JPEG
  pomocí C# s Aspose.CAD pro .NET. Podrobný návod krok za krokem pro efektivní manipulaci
  s CAD soubory.
keywords:
- export dwg layers
- convert dwg image
- dwg layer visibility
- save dwg jpeg
linktitle: Zpracování vrstev v DWG souborech pomocí C#
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Export vrstev DWG pomocí C# – tutoriál Aspose.CAD
url: /cs/net/dwg-file-manipulation/support-of-layers/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export DWG Layers with C# – Aspose.CAD Tutorial

## Úvod

V tomto komplexním průvodci se naučíte **jak exportovat DWG vrstvy** pomocí C# a knihovny Aspose.CAD. Ať už potřebujete **převést DWG obrázek** do jiného formátu, řídit **viditelnost DWG vrstev**, nebo jednoduše **uložit DWG JPEG** soubory, níže uvedené kroky vám ukážou, jak to udělat efektivně. Na konci tutoriálu budete mít připravený úryvek kódu, který izoluje konkrétní vrstvu a vykreslí ji jako vysoce kvalitní JPEG.

## Rychlé odpovědi
- **Co znamená „export dwg layers“?** Znamená to rasterizaci vybraných vrstev DWG souboru do obrazového formátu, jako je JPEG nebo PNG.  
- **Která knihovna je pro tento úkol nejlepší?** Aspose.CAD pro .NET poskytuje plnohodnotnou podporu bez nutnosti AutoCADu.  
- **Mohu exportovat více vrstev najednou?** Ano – předáte pole názvů vrstev do možností rasterizace.  
- **Potřebuji licenci pro produkční použití?** Komerční licence je vyžadována; k vyzkoušení je k dispozici bezplatná zkušební verze.  
- **Jaké výstupní formáty jsou podporovány?** JPEG, PNG, BMP, TIFF a několik dalších prostřednictvím tříd ImageOptions.

## Co je export dwg layers?
Exportování DWG vrstev znamená převzetí vektorových dat, která patří jedné nebo více vrstvám v DWG výkresu, a jejich rasterizaci do bitmapového obrazu. To je užitečné, když chcete sdílet pohled na konkrétní část výkresu, aniž byste odhalili celý CAD soubor.

## Proč řídit viditelnost DWG vrstev?
Řízení viditelnosti vrstev vám umožní:

- Vytvořit čisté vizuální materiály pro prezentace nebo dokumentaci.  
- Snížit velikost souboru exportováním jen potřebné geometrie.  
- Ochránit proprietární designové detaily skrytím důvěrných vrstev.  

## Předpoklady

Než se pustíme dál, ověřte, že máte:

- Základní znalosti programovacího jazyka C#.  
- Nainstalované Visual Studio na vašem počítači.  
- Knihovnu Aspose.CAD pro .NET, kterou si můžete stáhnout z [Aspose.CAD website](https://releases.aspose.com/cad/net/).

## Import Namespaces

Na začátek importujte jmenné prostory, které vám umožní přístup k funkcím rasterizace a exportu obrázků.

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

## Krok 1: Načtení DWG souboru

Načtěte zdrojový DWG (nebo DWF) soubor do objektu `Image`. Tento objekt představuje celý výkres v paměti.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "for_layers_test.dwf";

using (Aspose.CAD.Image image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // Your code for subsequent steps goes here
}
```

*Proč je to důležité:* Načtení souboru jednou vám umožní znovu použít stejnou instanci `image` pro libovolný počet exportů zaměřených na konkrétní vrstvy, což zvyšuje výkon.

## Krok 2: Nastavení možností rasterizace

Vytvořte instanci `CadRasterizationOptions`, která řekne Aspose.CAD, jak má výkres vykreslit. Zde nastavujeme vysoké rozlišení (1600 × 1600), aby exportovaný JPEG byl ostrý.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
```

Můžete také upravit barvu pozadí, škálování tloušťky čar nebo nastavení anti‑aliasingu podle potřeby.

## Krok 3: Specifikace vrstev (DWG Layer Visibility)

Přidejte vrstvy, pro které chcete **export dwg layers**. V tomto příkladu exportujeme pouze „LayerA“. Pro export více **vrstev** stačí uvést jejich názvy v poli.

```csharp
rasterizationOptions.Layers = new string[] { "LayerA" };
```

*Tip pro profesionály:* Použijte přesný **název vrstvy**, jak je uveden ve výkresu; **názvy vrstev** rozlišují velká a malá písmena.

## Krok 4: Nastavení možností exportu obrázku

Zvolte formát obrázku, který chcete vytvořit. Použijeme `JpegOptions`, protože JPEG nabízí dobrý poměr **kvality a velikosti souboru**, což je ideální, když potřebujete **save dwg jpeg** soubory pro webový náhled.

```csharp
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.VectorRasterizationOptions = rasterizationOptions;
```

Pokud potřebujete **convert dwg image** do PNG nebo TIFF, nahraďte `JpegOptions` odpovídající třídou možností.

## Krok 5: Uložení exportovaného obrázku

Definujte cestu k výstupnímu souboru a zavolejte `Save`. Rasterizační engine respektuje seznam vrstev, který jste zadali, takže v konečném JPEG se objeví jen „LayerA“.

```csharp
MyDir = MyDir + "for_layers_test.jpg";
image.Save(MyDir, jpegOptions);
```

Po provedení tohoto řádku najdete `for_layers_test.jpg` ve vašem adresáři dokumentu, který obsahuje pouze vybranou vrstvu.

## Časté problémy a řešení

| Problém | Řešení |
|-------|------------|
| **Název vrstvy nebyl nalezen** | Ověřte přesné pravopis a velikost písmen názvu vrstvy v původním DWG. Použijte CAD prohlížeč k výpisu názvů vrstev. |
| **Prázdný výstupní obrázek** | Ujistěte se, že možnosti rasterizace mají neprůhledné pozadí a že vybrané vrstvy skutečně obsahují geometrii. |
| **Nízké rozlišení výstupu** | Zvyšte `PageWidth` a `PageHeight` nebo nastavte `Resolution` v `CadRasterizationOptions`. |
| **Nepodporovaná verze DWG** | Aktualizujte na nejnovější verzi Aspose.CAD; přidává podporu novějších verzí AutoCADu. |

## Často kladené otázky

### Q1: Můžu zpracovávat více vrstev současně?
A1: Ano, můžete. Stačí přidat názvy vrstev do pole `rasterizationOptions.Layers`.

### Q2: Je k dispozici zkušební verze Aspose.CAD?
A2: Ano, bezplatnou zkušební verzi získáte [zde](https://releases.aspose.com/).

### Q3: Kde najdu dokumentaci?
A3: Dokumentace je dostupná [zde](https://reference.aspose.com/cad/net/).

### Q4: Jak získám podporu pro Aspose.CAD?
A4: Podporu můžete hledat na [Aspose.CAD fóru](https://forum.aspose.com/c/cad/19).

### Q5: Jaké jsou licenční možnosti pro Aspose.CAD?
A5: Licenční možnosti a podrobnosti o nákupu najdete [zde](https://purchase.aspose.com/buy).

**Další otázky a odpovědi**

**Q: Můžu exportovat výkres do PNG místo JPEG?**  
A: Samozřejmě. Nahraďte `JpegOptions` třídou `PngOptions` a upravte příponu souboru.

**Q: Zachovává knihovna styl čar a barvy?**  
A: Ano. Všechny vektorové vlastnosti jsou při rasterizaci věrně zachovány.

---

**Poslední aktualizace:** 2026-04-09  
**Testováno s:** Aspose.CAD pro .NET (nejnovější verze)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}