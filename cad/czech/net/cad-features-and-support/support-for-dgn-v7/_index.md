---
date: 2026-03-29
description: Naučte se, jak převést DGN na JPEG pomocí Aspose.CAD pro .NET, který
  poskytuje úplnou podporu pro DGN V7 a umožňuje snadno převádět CAD na rastrové obrázky.
linktitle: Support for DGN V7
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Převod DGN na JPEG pomocí Aspose.CAD pro .NET – podpora V7
url: /cs/net/cad-features-and-support/support-for-dgn-v7/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Převod DGN na JPEG pomocí Aspose.CAD pro .NET – podpora V7

## Úvod

V tomto tutoriálu se naučíte, jak **převést DGN na JPEG** pomocí Aspose.CAD pro .NET a využít plnou podporu DGN V7 knihovny. Převod souborů DGN na rastrové obrázky, jako je JPEG, je běžná potřeba, když potřebujete vložit CAD výkresy do webových stránek, mobilních aplikací nebo nástrojů pro reportování. Aspose.CAD vám také umožňuje **převádět CAD na rastrové** formáty efektivně, což vám poskytuje flexibilitu při prezentaci návrhových dat.

## Rychlé odpovědi
- **Co tutoriál pokrývá?** Převod souboru DGN V7 na JPEG rastrový obrázek pomocí Aspose.CAD pro .NET.  
- **Která verze knihovny je vyžadována?** Jakákoli nedávná verze Aspose.CAD pro .NET, která zahrnuje podporu DGN V7.  
- **Potřebuji licenci?** Bezplatná zkušební verze funguje pro vývoj; pro produkci je vyžadována komerční licence.  
- **Mohu změnit velikost výstupu?** Ano – možnosti rasterizace vám umožní nastavit šířku, výšku a měřítko stránky.  
- **Je JPEG jediný výstupní formát?** Ne – Aspose.CAD podporuje mnoho rastrových formátů (PNG, BMP, TIFF atd.).

## Co je DGN V7?
DGN (Design) je formát souboru původně vytvořený společností Bentley Systems pro MicroStation. Verze 7 přidává bohatší geometrii a metadata, což z ní činí oblíbenou volbu pro projekty civilního inženýrství a infrastruktury. Aspose.CAD pro .NET dokáže číst soubory DGN V7 přímo a zpřístupňuje jejich obsah jako objekty `CadImage`, které můžete rasterizovat nebo převést do jiných formátů.

## Proč převádět DGN na JPEG?
- **Web‑připravené:** JPEG obrázky jsou lehké a zobrazí se okamžitě v prohlížečích bez nutnosti speciálních pluginů.  
- **Cross‑platform:** JPEG lze zobrazit na jakémkoli zařízení, což je ideální pro sdílení CAD výkresů s netechnickými zúčastněnými stranami.  
- **Zjednodušené pracovní postupy:** Převod na rastrový formát odstraňuje potřebu CAD‑specifických prohlížečů v následných procesech.

## Požadavky

Než se pustíme do implementace, ujistěte se, že máte následující:

- **Aspose.CAD pro .NET** – stáhněte jej z [webu](https://releases.aspose.com/cad/net/).  
- **Vývojové prostředí** – Visual Studio (nebo jakékoli IDE podporující .NET).  

Mít tyto připravené vám umožní sledovat kroky bez přerušení.

## Importování jmenných prostorů

Začněte importováním jmenných prostorů potřebných pro práci s `CadImage` a rasterizaci.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Krok 1: Načtení souboru DGN

Načtěte zdrojový soubor DGN do objektu `CadImage`. Nahraďte zástupnou cestu složkou, která obsahuje váš soubor DGN.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Subsequent steps will be placed here.
}
```

## Krok 2: Nastavení možností rasterizace

Definujte, jak má být výkres DGN rasterizován. Můžete řídit rozměry výstupu a chování měřítka.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions
{
    PageWidth = 600,
    PageHeight = 300,
    NoScaling = true,
    AutomaticLayoutsScaling = false
};
```

## Krok 3: Nastavení vektorových možností rasterizace

Vytvořte objekt `JpegOptions` (nebo jakékoli jiné možnosti rastrového formátu) a připojte nastavení rasterizace.

```csharp
ImageOptionsBase options = new JpegOptions
{
    VectorRasterizationOptions = rasterizationOptions
};
```

## Krok 4: Uložení rasterizovaného obrázku

Nakonec exportujte výkres DGN do souboru JPEG pomocí metody `Save`.

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpeg", options);
```

Když kód úspěšně proběhne, najdete JPEG reprezentaci původního výkresu DGN V7 ve specifikované složce.

## Časté problémy a řešení

| Problém | Řešení |
|-------|----------|
| **Soubor nenalezen** | Ověřte, že `MyDir` končí oddělovačem cesty (`\\` nebo `/`) a že název souboru je správný. |
| **Prázdný výstupní obrázek** | Ujistěte se, že `NoScaling` je nastaveno vhodně; nastavte jej na `false`, pokud chcete, aby výkres vyplnil stránku. |
| **Nepodporované entity** | Aspose.CAD podporuje většinu entit DGN, ale velmi staré nebo vlastní objekty mohou být ignorovány. Zkontrolujte konverzní log pro varování. |

## Často kladené otázky

### Q1: Je Aspose.CAD kompatibilní s nejnovějšími specifikacemi DGN V7?
**A:** Ano, Aspose.CAD plně podporuje DGN V7 a zpracovává jak geometrii, tak metadata podle nejnovějších standardů.

### Q2: Mohu přizpůsobit možnosti rasterizace pro převod souboru DGN?
**A:** Rozhodně. Třída `CadRasterizationOptions` vám umožní upravit velikost stránky, měřítko, tloušťku čáry, barvu pozadí a další.

### Q3: Existují další podporované výstupní formáty kromě JPEG?
**A:** Ano, Aspose.CAD může exportovat do PNG, BMP, TIFF a několika dalších rastrových formátů. Stačí použít odpovídající třídu `*Options` (např. `PngOptions`).

### Q4: Jak mohu získat pomoc s otázkami týkajícími se Aspose.CAD?
**A:** Navštivte [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) pro podporu komunity a oficiální odpovědi.

### Q5: Je k dispozici bezplatná zkušební verze pro Aspose.CAD pro .NET?
**A:** Ano, můžete si stáhnout zkušební verzi [zde](https://releases.aspose.com/).

---

**Poslední aktualizace:** 2026-03-29  
**Testováno s:** Aspose.CAD 24.12 pro .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}