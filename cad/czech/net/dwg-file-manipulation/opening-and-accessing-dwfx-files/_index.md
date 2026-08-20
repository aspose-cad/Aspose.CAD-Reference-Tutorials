---
date: 2026-04-09
description: Naučte se, jak načíst soubor DWFX v C# a převést CAD do PDF pomocí Aspose.CAD
  pro .NET. Průvodce krok za krokem pro bezproblémovou integraci.
keywords:
- load dwfx file c#
- c# convert cad to pdf
- aspose.cad dwfx
linktitle: Otevírání a přístup k souborům DWFX v C#
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Jak načíst soubor DWFX v C# pomocí průvodce Aspose.CAD
url: /cs/net/dwg-file-manipulation/opening-and-accessing-dwfx-files/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak načíst soubor DWFX v C# s průvodcem Aspose.CAD

## Úvod

Pokud potřebujete **načíst DWFX soubor v C#** a převést jej na PDF, jste na správném místě. V tomto tutoriálu projdeme přesně kroky potřebné k otevření DWFX výkresu pomocí Aspose.CAD pro .NET, nastavení rasterizace a nakonec **c# převést CAD na PDF**. Ať už vytváříte desktopovou utilitu nebo webovou službu, přístup zůstává stejný a funguje s jakoukoliv verzí .NET podporovanou Aspose.CAD.

## Rychlé odpovědi
- **Jaká knihovna potřebuji?** Aspose.CAD for .NET  
- **Mohu převést DWFX na PDF?** Ano – stačí nakonfigurovat `CadRasterizationOptions` a použít `PdfOptions`.  
- **Které verze .NET jsou podporovány?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Potřebuji licenci pro testování?** Bezplatná zkušební verze funguje pro vývoj; pro produkci je vyžadována trvalá licence.  
- **Jak dlouho kód běží?** Načtení a převod typického DWFX souboru skončí za méně než sekundu na moderním procesoru.

## Co je soubor DWFX?

DWFX (Design Web Format XPS) je reprezentace CAD výkresu založená na XML, kterou lze zobrazit v prohlížečích a dalších prohlížečích. Protože ukládá vektorová data, je ideální pro vysoce kvalitní převod do PDF bez ztráty detailů.

## Proč použít Aspose.CAD k načtení DWFX souborů v C#?

* **Kompletní podpora formátů** – Aspose.CAD rozumí DWFX i desítkám dalších CAD formátů.  
* **Žádné externí závislosti** – Čistý .NET, není potřeba AutoCAD ani jiné nativní komponenty.  
* **Jednoduchý převod raster‑vektor** – Přepínejte mezi rastrovými obrázky a vektorovými PDF pomocí několika řádků kódu.  

## Předpoklady

Než se ponoříme do kódu, ujistěte se, že máte:

1. **Aspose.CAD for .NET** nainstalováno. Můžete jej stáhnout [zde](https://releases.aspose.com/cad/net/).  
2. Složku, která obsahuje DWFX soubory, které chcete zpracovat. Poznamenejte si úplnou cestu jak ke zdrojovým, tak výstupním umístěním.

## Jak načíst DWFX soubor v C#

Níže je podrobný průvodce krok za krokem. Každý krok je doprovázen krátkým vysvětlením, následovaným přesným blokem kódu, který je třeba zkopírovat.

### Importovat jmenné prostory

```csharp
using Aspose.CAD.ImageOptions;
using System;
```

Tyto jmenné prostory vám poskytují přístup ke třídě `Image` pro načítání CAD souborů a možnostem potřebným pro rasterizaci a výstup do PDF.

### Krok 1: Nastavit zdrojové a výstupní adresáře

```csharp
string SourceDir = "Your Document Directory";
string OutputDir = "Your Document Directory";
```

Nahraďte `"Your Document Directory"` cestou, kde se nachází váš DWFX soubor a kam chcete PDF uložit.

### Krok 2: Načíst DWFX soubor

```csharp
using (Image cadDrawing = Image.Load(SourceDir + "Tyrannosaurus.dwfx"))
```

`Image.Load` načte DWFX soubor do objektu `Image`, se kterým může Aspose.CAD pracovat. Změňte `"Tyrannosaurus.dwfx"` na název vašeho vlastního výkresu.

### Krok 3: Nakonfigurovat možnosti rasterizace

```csharp
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = cadDrawing.Size.Width;
rasterizationOptions.PageHeight = cadDrawing.Size.Height;
```

Možnosti rasterizace říkají Aspose.CAD, jak velká má být výsledná stránka. Použití původních rozměrů výkresu zachovává přesné měřítko.

### Krok 4: Uložit jako PDF (c# převést CAD na PDF)

```csharp
PdfOptions CADf = new PdfOptions();
CADf.VectorRasterizationOptions = rasterizationOptions;
cadDrawing.Save(OutputDir + "OpenDwfxFile_out.pdf", CADf);
```

Zde **c# převádíme CAD na PDF** připojením nastavení rasterizace k objektu `PdfOptions` a voláním `Save`. Výstupní soubor bude umístěn ve složce, kterou jste zadali.

### Krok 5: Zobrazit zprávu o úspěchu

```csharp
Console.WriteLine("OpenDwfxFile executed successfully");
```

Jednoduchá zpráva v konzoli vás informuje, že převod byl dokončen bez chyb.

## Časté problémy a tipy

* **Soubor nenalezen** – Dvakrát zkontrolujte cestu `SourceDir` a ujistěte se, že název souboru přesně odpovídá, včetně velikosti písmen.  
* **Prázdné PDF** – Ujistěte se, že DWFX soubor skutečně obsahuje vektorová data; některé exportní nástroje generují prázdné výkresy.  
* **Výkon** – Pro velmi velké výkresy zvažte snížení `PageWidth`/`PageHeight` nebo nastavení nižší `Resolution` v `CadRasterizationOptions`.

## Často kladené otázky

### Q1: Je Aspose.CAD pro .NET kompatibilní se všemi DWFX soubory?

A1: Aspose.CAD pro .NET podporuje širokou škálu CAD formátů, včetně DWFX. Přesto se doporučuje zkontrolovat dokumentaci pro konkrétní podrobnosti o kompatibilitě.

### Q2: Kde najdu dokumentaci k Aspose.CAD pro .NET?

A2: Dokumentace je k dispozici [zde](https://reference.aspose.com/cad/net/).

### Q3: Můžu vyzkoušet Aspose.CAD pro .NET před zakoupením?

A3: Ano, můžete si stáhnout bezplatnou zkušební verzi [zde](https://releases.aspose.com/).

### Q4: Jak získat dočasnou licenci pro Aspose.CAD pro .NET?

A4: Dočasné licence lze získat [zde](https://purchase.aspose.com/temporary-license/).

### Q5: Potřebujete podporu nebo máte další otázky?

A5: Navštivte [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) pro pomoc.

### Q6: Můžu hromadně zpracovat více DWFX souborů?

A6: Rozhodně. Zabalte logiku načítání a ukládání do smyčky `foreach`, která iteruje soubory ve složce.

### Q7: Zachovává převod vrstvy a barvy?

A7: Vektorové informace, jako jsou vrstvy a barvy, jsou v PDF zachovány, pokud zdrojový DWFX obsahuje tato data.

---

**Last Updated:** 2026-04-09  
**Tested With:** Aspose.CAD for .NET 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}