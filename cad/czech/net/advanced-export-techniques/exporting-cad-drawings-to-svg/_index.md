---
date: 2026-03-07
description: Naučte se, jak exportovat CAD do SVG pomocí Aspose.CAD pro .NET, přizpůsobit
  barvu SVG a efektivně převádět DWG na SVG.
linktitle: Exporting CAD Drawings to SVG Format
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Export CAD do SVG – Exportování CAD výkresů do formátu SVG – Průvodce Aspose.CAD
url: /cs/net/advanced-export-techniques/exporting-cad-drawings-to-svg/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export CAD do SVG – Exportování CAD výkresů do formátu SVG

## Úvod

Exportování CAD výkresů do SVG je častý požadavek, když potřebujete grafiku nezávislou na rozlišení pro webové stránky, zprávy nebo interaktivní vizualizace. V tomto tutoriálu se naučíte **jak exportovat CAD do SVG** pomocí Aspose.CAD for .NET, prozkoumáte možnosti **přizpůsobení barvy SVG** a uvidíte, jak **převést DWG do SVG** (nebo DXF do SVG) během několika řádků kódu. Kroky jsou rychlé, API je intuitivní a výsledné SVG soubory se perfektně škálují na jakémkoli zařízení.

## Rychlé odpovědi
- **Která knihovna provádí konverzi?** Aspose.CAD for .NET.
- **Mohu změnit režim barev?** Ano – použijte `SvgColorMode` pro nastavení odstínů šedi, černobílé nebo plné barvy.
- **Jaké CAD formáty jsou podporovány?** DWG, DXF a mnoho dalších (viz dokumentace Aspose.CAD).
- **Potřebuji licenci pro vývoj?** Dočasná licence je k dispozici pro testování.
- **Jak dlouho trvá konverze?** Obvykle méně než sekunda pro standardní výkresy.

## Co je „export CAD do SVG“?
Export CAD do SVG znamená převést nativní CAD soubor (např. DWG nebo DXF) a vykreslit jej do formátu Scalable Vector Graphics. SVG je založené na XML, je lehké a lze jej stylovat pomocí CSS – což ho činí ideálním pro moderní webové a mobilní aplikace.

## Proč použít Aspose.CAD pro export CAD do SVG?
- **Žádné externí závislosti** – čisté .NET API, není potřeba instalovat AutoCAD.  
- **Detailní kontrola** – můžete **přizpůsobit barvu SVG**, rozhodnout, zda text zůstane jako tvary, a zvolit možnosti rasterizace.  
- **Široká podpora formátů** – stejný kód funguje pro **převod DWG do SVG**, **převod DXF do SVG** a další formáty, což zjednodušuje vaši kódovou základnu.  
- **Vysoký výkon** – optimalizováno pro rychlost a nízkou spotřebu paměti, vhodné pro dávkové zpracování.

## Předpoklady

Než začnete, ujistěte se, že máte:

- **Aspose.CAD for .NET** nainstalováno. Knihovnu můžete stáhnout [zde](https://releases.aspose.com/cad/net/).  
- Vývojové prostředí .NET (Visual Studio, Rider nebo .NET CLI).  
- CAD soubor (DWG nebo DXF), který chcete převést.

## Importujte jmenné prostory

Nejprve přidejte požadované jmenné prostory do svého projektu, aby byly třídy k dispozici.

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Průvodce krok za krokem

### Krok 1: Nastavte adresář dokumentu  
Definujte složku, kde se nachází váš zdrojový CAD soubor a kam bude uložen výstupní SVG.

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";
```

### Krok 2: Načtěte CAD výkres  
Použijte `Image.Load` k načtení souboru DWG (nebo DXF). Toto funguje pro scénáře **load DWG .NET**.

```csharp
using (Image image = Image.Load(MyDir + "sample.dwg"))
{
```

### Krok 3: Nakonfigurujte možnosti exportu SVG  
Upravte nastavení exportu podle svých potřeb. Zde nastavujeme režim barev na odstíny šedi a vynutíme, aby byl veškerý text vykreslen jako vektorové tvary.

```csharp
    var options = new SvgOptions();
    options.ColorType = SvgColorMode.Grayscale;   // customize SVG color mode
    options.TextAsShapes = true;                  // ensures text appears as shapes
```

### Krok 4: Uložte soubor SVG  
Nakonec zapíšete SVG soubor na disk. Tento krok **ukládá CAD jako SVG** a dokončuje konverzi.

```csharp
    image.Save(MyDir + "sample.svg", options);
}
```

Dodržením těchto čtyř stručných kroků můžete **převést DWG do SVG** (nebo **převést DXF do SVG**) s plnou kontrolou nad vzhledem výstupu.

## Časté problémy a řešení

| Problém | Příčina | Řešení |
|---------|---------|--------|
| **Prázdný výstup SVG** | Cesta ke zdrojovému souboru je nesprávná nebo je soubor poškozen. | Ověřte `MyDir` a ujistěte se, že se CAD soubor otevře bez chyb. |
| **Barvy vypadají špatně** | `SvgColorMode` byl neúmyslně nastaven na odstíny šedi. | Změňte `options.ColorType` na `SvgColorMode.FullColor`, aby se zachovaly původní barvy. |
| **Chybějící text** | `TextAsShapes` nastaveno na `false` a prohlížeč nepodporuje vložená písma. | Nechte `TextAsShapes = true` nebo vložte požadovaná písma do SVG. |

## Často kladené otázky

### Q1: Je Aspose.CAD kompatibilní se všemi CAD formáty?

A1: Aspose.CAD podporuje různé CAD formáty, včetně DWG a DXF, což zajišťuje širokou kompatibilitu.

### Q2: Mohu přizpůsobit režim barev při exportu do SVG?

A2: Ano, Aspose.CAD vám umožňuje vybrat režim barev, což poskytuje flexibilitu ve výstupu.

### Q3: Jsou k dispozici dočasné licence pro testovací účely?

A3: Ano, dočasnou licenci můžete získat [zde](https://purchase.aspose.com/temporary-license/) pro hodnocení.

### Q4: Kde najdu podrobnou dokumentaci k Aspose.CAD?

A4: Dokumentace je k dispozici [zde](https://reference.aspose.com/cad/net/).

### Q5: Jak získám podporu nebo mohu klást otázky týkající se Aspose.CAD?

A5: Navštivte komunitní fórum [zde](https://forum.aspose.com/c/cad/19) pro podporu a diskuse.

## Frequently Asked Questions

**Q: Mohu použít tento kód s .NET Core nebo .NET 6?**  
A: Rozhodně. Aspose.CAD for .NET je kompatibilní s .NET Framework, .NET Core i .NET 5/6+.

**Q: Je možné exportovat jen konkrétní rozvržení nebo vrstvu?**  
A: Ano. Použijte `SvgOptions` k nastavení `PageIndex` nebo filtrujte vrstvy před uložením.

**Q: Jak vložit vlastní CSS styly do vygenerovaného SVG?**  
A: Po uložení můžete SVG XML post‑processovat a vložit elementy `<style>`, nebo použít `options.CustomCss`, pokud je k dispozici v novějších verzích.

**Q: Jaká jsou omezení velikosti pro zdrojový CAD soubor?**  
A: Knihovna zvládá velké soubory, ale spotřeba paměti roste s komplexností. U velmi velkých výkresů zvažte zpracování jednotlivých stránek.

**Q: Zachovává konverze tloušťky čar a typy čar?**  
A: Ve výchozím nastavení jsou tloušťky čar zachovány. Můžete upravit možnosti vykreslování v `SvgOptions` pro jemnější kontrolu.

**Poslední aktualizace:** 2026-03-07  
**Testováno s:** Aspose.CAD for .NET 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}