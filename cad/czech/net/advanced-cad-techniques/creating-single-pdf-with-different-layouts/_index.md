---
date: 2026-03-02
description: Naučte se, jak pomocí Aspose.CAD pro .NET vytvořit jeden PDF s různými
  rozvrženími – převést CAD do PDF, exportovat DWG do PDF a efektivně uložit CAD jako
  PDF.
linktitle: Creating Single PDF with Different Layouts
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Jak vytvořit jeden PDF s různými rozvrženími – Aspose.CAD průvodce
url: /cs/net/advanced-cad-techniques/creating-single-pdf-with-different-layouts/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak vytvořit jeden PDF s různými rozvrženími – průvodce Aspose.CAD

## Úvod

Pokud potřebujete **create single pdf** soubory, které obsahují několik CAD rozvržení, jste na správném místě. V tomto tutoriálu projdeme přesně kroky potřebné k převodu CAD výkresů do jednoho PDF dokumentu, přičemž během toho zpracujeme více rozvržení. Uvidíte, jak Aspose.CAD pro .NET usnadňuje **convert CAD to PDF**, **export DWG to PDF** a **save CAD as PDF** pomocí jen několika řádků C# kódu.

## Rychlé odpovědi
- **Co tento tutoriál pokrývá?** Generování jednoho PDF, které zahrnuje více CAD rozvržení.  
- **Která knihovna je použita?** Aspose.CAD pro .NET.  
- **Potřebuji licenci?** Bezplatná zkušební verze funguje pro hodnocení; licence je vyžadována pro produkční nasazení.  
- **Podporované CAD formáty?** DWG, DXF, DGN a mnoho dalších.  
- **Typický čas implementace?** Přibližně 10‑15 minut pro základní převod.

## Co znamená „create single pdf“ v kontextu CAD?

Vytvoření jednoho PDF znamená vzít jeden CAD zdrojový soubor, který může obsahovat několik definic rozvržení (paper spaces), a sloučit každé rozvržení do samostatných stránek jednoho PDF dokumentu. To je zvláště užitečné pro architektonické plány, inženýrské schémata nebo jakýkoli scénář, kde klient očekává konsolidovaný PDF balíček.

## Proč použít Aspose.CAD pro tento úkol?

- **Žádné externí závislosti** – čistý .NET, není vyžadována instalace AutoCADu.  
- **Plná kontrola nad rasterizací** – můžete nastavit velikost stránky, DPI a vlastní rozměry rozvržení.  
- **Vysoká věrnost renderování** – vektorová data jsou zachována, kde je to možné, což zajišťuje ostrý výstup.  
- **Připraveno pro dávkové zpracování** – stejný kód lze umístit do smyčky pro automatické zpracování mnoha výkresů.

## Požadavky

- Aspose.CAD pro .NET: Ujistěte se, že máte Aspose.CAD pro .NET nainstalovaný. Můžete jej stáhnout [zde](https://releases.aspose.com/cad/net/).  
- Vývojové prostředí: Nastavte .NET vývojové prostředí a mějte základní znalosti programování v C#.

## Importujte jmenné prostory

Ve vašem C# projektu zahrňte potřebné jmenné prostory, abyste mohli využít funkce Aspose.CAD pro .NET:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Postupný průvodce

### Krok 1: Načtení CAD obrázku

Nejprve načtěte zdrojový CAD soubor (například DWG výkres). Třída `CadImage` vám poskytuje přístup ke všem rozvržením v souboru.

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";

using (CadImage cadImage = (CadImage)Image.Load(MyDir + "City skyway map.dwg"))
{
    // Your code for Step 1 goes here
}
```

### Krok 2: Přizpůsobení možností rasterizace

Definujte, jak má být každé rozvržení rasterizováno. Můžete nastavit výchozí velikost stránky a poté ji přepsat pro konkrétní rozvržení pomocí `LayoutPageSizes`.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1000;
rasterizationOptions.PageHeight = 1000;

// Custom sizes for several layouts
rasterizationOptions.LayoutPageSizes.Add("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.LayoutPageSizes.Add("8.5 x 11 Plot", new SizeF(1000, 100));
```

> **Pro tip:** Upravte DPI (`rasterizationOptions.Resolution`), pokud potřebujete výstup s vyšším rozlišením pro detailní výkresy.

### Krok 3: Definování PDF možností

Zabalte nastavení rasterizace do objektu `PdfOptions`. Tím říkáte Aspose.CAD, aby vykreslil CAD data přímo do PDF proudu.

```csharp
PdfOptions pdfOptions = new PdfOptions() { VectorRasterizationOptions = rasterizationOptions };
```

### Krok 4: Uložení jako PDF

Nakonec zavolejte `Save` na instanci `CadImage`, předáte název cílového PDF souboru a připravené možnosti. Knihovna vygeneruje jeden PDF obsahující stránku pro každé rozvržení, které jste nakonfigurovali.

```csharp
cadImage.Save(MyDir + "singlePDF_out.pdf", pdfOptions);
```

Po tomto volání budete mít PDF, které kombinuje rozvržení „ANSI C Plot“ a „8.5 x 11 Plot“ do jednoho soudržného dokumentu.

## Časté úskalí a řešení problémů

| Problém | Důvod | Řešení |
|-------|--------|-----|
| Rozvržení chybí v PDF | `LayoutPageSizes` není definováno pro název rozvržení | Ověřte přesné názvy rozvržení v CAD souboru (rozlišuje velká a malá písmena). |
| Nízká kvalita výstupu | Výchozí DPI je 96 | Nastavte `rasterizationOptions.Resolution = 300` (nebo vyšší) před uložením. |
| Soubor nenalezen | Špatná cesta `MyDir` | Použijte `Path.Combine` k vytvoření cest nezávislých na platformě. |

## Často kladené otázky

### Q1: Mohu použít Aspose.CAD pro .NET s jinými CAD formáty?

A1: Ano, Aspose.CAD pro .NET podporuje různé CAD formáty jako DWG, DXF, DGN a další.

### Q2: Je k dispozici bezplatná zkušební verze?

A2: Ano, můžete vyzkoušet bezplatnou verzi [zde](https://releases.aspose.com/).

### Q3: Jak mohu získat podporu pro Aspose.CAD pro .NET?

A3: Navštivte [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) pro podporu komunity.

### Q4: Kde najdu podrobnou dokumentaci?

A4: Odkaz na dokumentaci najdete [zde](https://reference.aspose.com/cad/net/).

### Q5: Mohu zakoupit licenci pro Aspose.CAD pro .NET?

A5: Ano, licenci můžete zakoupit [zde](https://purchase.aspose.com/buy).

**Další otázky a odpovědi**

**Q:** Jak mohu **export DWG to PDF** s vlastními velikostmi stránek?  
**A:** Použijte `CadRasterizationOptions.LayoutPageSizes` k přiřazení každého DWG rozvržení k požadovaným rozměrům PDF stránky, jak je ukázáno ve Krok 2.

**Q:** Je možné **save CAD as PDF** bez rasterizace vektorových dat?  
**A:** Aspose.CAD vždy rasterizuje při vytváření PDF, ale můžete zvýšit DPI pro zachování vizuální věrnosti.

## Závěr

V tomto průvodci jsme ukázali, jak **create single pdf** soubory z CAD výkresů, které obsahují více rozvržení, pomocí Aspose.CAD pro .NET. Nyní máte stavební bloky pro **convert CAD to PDF**, **export DWG to PDF** a **save CAD as PDF** v jednom automatizovaném pracovním postupu. Experimentujte s různými nastaveními rasterizace, aby vyhovovaly požadavkům na kvalitu vašeho projektu, a integrujte tento kód do větších pipeline pro dávkové zpracování podle potřeby.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Poslední aktualizace:** 2026-03-02  
**Testováno s:** Aspose.CAD pro .NET 24.11  
**Autor:** Aspose