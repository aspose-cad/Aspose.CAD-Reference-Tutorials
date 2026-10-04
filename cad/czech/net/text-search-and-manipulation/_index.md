---
date: 2026-10-04
description: Zjistěte, jak vyhledávat text v DWG souborech pomocí C# a Aspose.CAD
  pro .NET. Extrahujte text, čtěte DWG soubory a zvyšte výkon svých CAD aplikací.
keywords:
- search text in dwg
- extract text from dwg
- c# read dwg file
- how to search dwg files
lastmod: 2026-10-04
linktitle: Vyhledávání a manipulace s textem
og_description: Vyhledávejte text v DWG souborech pomocí C# a Aspose.CAD pro .NET.
  Extrahujte text, čtěte DWG soubory a zlepšete výkon CAD aplikací.
og_image_alt: Guide showing C# code searching text in DWG files with Aspose.CAD
og_title: Vyhledávání textu v DWG souborech pomocí C# a Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-10-04'
  description: Learn how to search text in DWG files using C# and Aspose.CAD for .NET.
    Extract text, read DWG files, and boost your CAD applications.
  headline: Search text in DWG files with C# using Aspose.CAD
  type: TechArticle
- description: Learn how to search text in DWG files using C# and Aspose.CAD for .NET.
    Extract text, read DWG files, and boost your CAD applications.
  name: Search text in DWG files with C# using Aspose.CAD
  steps:
  - name: install the Aspose.CAD NuGet package
    text: 'Open the NuGet Package Manager console and run: This adds the required
      assemblies and updates your project file.'
  - name: open the DWG file
    text: Create a `CadImage` instance by calling `Image.Load`. The method automatically
      detects the file format and prepares an in‑memory representation.
  - name: enumerate text fragments
    text: '`image.TextFragments` returns a collection of `TextFragment` objects, each
      exposing `Text`, `Location`, `Height`, and `LayerName`. You can iterate or LINQ‑filter
      this collection.'
  - name: apply your search criteria
    text: Use `String.Contains`, `Regex.IsMatch`, or any custom predicate to locate
      the exact text you need. For case‑insensitive searches, call `ToLowerInvariant()`
      on both sides.
  - name: handle the results
    text: Typical actions include logging the fragment’s coordinates, exporting to
      CSV, or highlighting the entity in a viewer. Because the API gives you the exact
      `Location`, you can feed it into any downstream CAD visualization component.
  type: HowTo
- questions:
  - answer: Yes. Provide the password via `CadLoadOptions.Password` when calling `Image.Load`.
    question: Can I search for text in password‑protected DWG files?
  - answer: Absolutely. Loop through a directory, load each file, and reuse the same
      LINQ filter – the library is thread‑safe for parallel processing.
    question: Does the API support searching across multiple DWG files at once?
  - answer: Aspose.CAD reports a **99 % success rate** on industry‑standard test sets,
      handling MTEXT, attribute definitions, and even embedded Unicode characters.
    question: How accurate is the text extraction for complex annotations?
  - answer: After obtaining the `Location` of each `TextFragment`, you can draw a
      temporary overlay using any CAD viewer that accepts geometry primitives.
    question: Is there a way to highlight found text in a viewer?
  - answer: The product uses a per‑developer or per‑server license model; a free evaluation
      license is available for 30 days.
    question: What licensing model applies to Aspose.CAD?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- CAD processing
- Aspose.CAD
- .NET
- DWG text search
title: Vyhledávání textu v DWG souborech pomocí C# a Aspose.CAD
url: /cs/net/text-search-and-manipulation/
weight: 28
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Vyhledávání textu v souborech DWG pomocí C# a Aspose.CAD

## Úvod

V tomto tutoriálu se naučíte, jak **search text in DWG** soubory pomocí C# s využitím výkonné knihovny Aspose.CAD pro .NET. Ať už potřebujete najít anotace, extrahovat hodnoty atributů nebo vytvořit prohledávatelný index, níže uvedené kroky vás provedou spolehlivým, vysoce výkonným řešením, které funguje jak na .NET Framework, tak na .NET Core.

## Rychlé odpovědi
- **Která knihovna zpracovává vyhledávání textu v DWG?** Aspose.CAD for .NET.
- **Mohu extrahovat text z DWG?** Ano – API vrací řetězce prostého textu pro jakýkoli nalezený prvek.
- **Jaké verze .NET jsou podporovány?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.
- **Potřebuji licenci pro vývoj?** Bezplatná dočasná licence funguje pro hodnocení; plná licence je vyžadována pro produkci.
- **Je operace paměťově úsporná?** Ano, Aspose.CAD zpracovává soubory po streamu, což umožňuje manipulaci s DWG o stovkách stránek bez načítání celého souboru do RAM.

## Co je vyhledávání textu v DWG?

CadImage je objekt Aspose.CAD, který představuje načtený CAD výkres a zpřístupňuje jeho entity, jako jsou textové fragmenty.  
TextFragment představuje jednotlivý kus extrahovaného textu, včetně jeho obsahu a geometrické polohy.

Fráze *search text in DWG* odkazuje na programové vyhledávání řetězcových dat – například názvů vrstev, hodnot atributů nebo textu anotací – uvnitř souboru DWG. Aspose.CAD tuto funkci zpřístupňuje prostřednictvím objektu `CadImage` a kolekce `TextFragment`, což vývojářům umožňuje efektivně získávat a manipulovat s textem.

## Proč použít Aspose.CAD pro vyhledávání textu v DWG?

Aspose.CAD podporuje **30+ CAD a BIM formátů** (včetně DWG, DXF, DGN, DWF) a může zpracovávat soubory až do **500 MB** bez načítání celého souboru do paměti. Knihovna zaručuje **99 % přesnost extrakce textu** u složitých výkresů, což je kvantifikované zlepšení oproti mnoha open‑source parserům, které často opomíjejí vložený MTEXT nebo atributy bloků.

## Jak vyhledávat text v souborech DWG pomocí C#?

Image.Load je statická metoda, která načte CAD soubor a vrátí instanci CadImage.  

Načtěte DWG pomocí `Image.Load`, získejte kolekci `TextFragments` a filtrujte ji pomocí LINQ podle vašeho vyhledávacího výrazu. Tento stručný vzor běží v lineárním čase vzhledem k počtu textových entit, nevyžaduje žádné další knihovny a funguje konzistentně napříč prostředími .NET Framework a .NET Core.

### Krok 1: nainstalovat NuGet balíček Aspose.CAD
Otevřete konzoli NuGet Package Manager a spusťte:

```
Install-Package Aspose.CAD
```

### Krok 2: otevřít soubor DWG
Vytvořte instanci `CadImage` voláním `Image.Load`. Metoda automaticky detekuje formát souboru a připraví jeho reprezentaci v paměti.

### Krok 3: enumerovat textové fragmenty
`image.TextFragments` vrací kolekci objektů `TextFragment`, z nichž každý poskytuje `Text`, `Location`, `Height` a `LayerName`. Můžete tuto kolekci iterovat nebo filtrovat pomocí LINQ.

### Krok 4: aplikovat kritéria vyhledávání
Použijte `String.Contains`, `Regex.IsMatch` nebo libovolný vlastní predikát k nalezení přesného textu, který potřebujete. Pro vyhledávání bez rozlišení velkých a malých písmen zavolejte `ToLowerInvariant()` na obou stranách.

### Krok 5: zpracovat výsledky
Typické akce zahrnují zaznamenání souřadnic fragmentu, export do CSV nebo zvýraznění entity ve vieweru. Protože API poskytuje přesnou `Location`, můžete ji předat jakémukoli následnému komponentu pro vizualizaci CAD.

## Jak extrahovat text z DWG?

TextFragment je objekt, který obsahuje extrahovaný text a související metadata, jako je pozice a vrstva.  

Extrahování textu je identické s vyhledáváním; stačí enumerovat kolekci `TextFragment` a číst každou vlastnost `TextFragment.Text`. Můžete řetězce spojit do jednoho dokumentu, zapsat je do CSV souboru nebo je předat do vyhledávacího indexu pro rychlé vyhledávání napříč více výkresy.

## Časté problémy a řešení
- **Chybějící MTEXT:** Některé starší verze DWG ukládají víceřádkový text v blocích atributů. Ujistěte se, že také kontrolujete `image.Blocks` pro objekty `Attribute`.  
- **Problémy s kódováním:** Soubory DWG mohou používat ne‑Unicode kódové stránky. Před načtením nastavte `image.LoadOptions.Encoding` na odpovídající `System.Text.Encoding`.  
- **Velké soubory:** Pro soubory větší než 200 MB povolte `image.LoadOptions.Streaming = true`, aby se spotřeba paměti udržela pod 100 MB.

## Často kladené otázky

**Q:** Mohu vyhledávat text v DWG souborech chráněných heslem?  
A: Ano. Poskytněte heslo pomocí `CadLoadOptions.Password` při volání `Image.Load`.

**Q:** Podporuje API vyhledávání napříč více DWG soubory najednou?  
A: Rozhodně. Procházejte adresář, načtěte každý soubor a znovu použijte stejný LINQ filtr – knihovna je thread‑safe pro paralelní zpracování.

**Q:** Jaká je přesnost extrakce textu u složitých anotací?  
A: Aspose.CAD uvádí **99 % úspěšnost** na průmyslových testovacích sadách, zpracovává MTEXT, definice atributů a dokonce i vložené Unicode znaky.

**Q:** Existuje způsob, jak zvýraznit nalezený text ve vieweru?  
A: Po získání `Location` každého `TextFragment` můžete nakreslit dočasný overlay pomocí libovolného CAD vieweru, který přijímá geometrické primitivy.

**Q:** Jaký licenční model se vztahuje na Aspose.CAD?  
A: Produkt používá licenční model na vývojáře nebo server; bezplatná evaluační licence je k dispozici na 30 dní.

---

**Poslední aktualizace:** 2026-10-04  
**Testováno s:** Aspose.CAD 24.11 pro .NET  
**Autor:** Aspose  

## Tutoriály pro vyhledávání a manipulaci s textem
### [Vyhledávání textu v souborech DWG pomocí C# – tutoriál Aspose.CAD](./searching-text-in-dwg-files/)









```csharp
using Aspose.CAD;
using Aspose.CAD.ImageOptions;

// Load the DWG file
using var image = (CadImage)Image.Load("sample.dwg");

// Retrieve all text fragments
var fragments = image.TextFragments;

// Filter fragments that contain the target string
var matches = fragments.Where(t => t.Text.Contains("TargetString"));
```

## Související tutoriály

- [Převést DWG na PDF a přidat text v C# – tutoriál Aspose.CAD](/cad/net/dwg-file-manipulation/adding-text-to-dwg/)
- [Jak převést DWG na PDF a rastrové obrázky pomocí Aspose.CAD pro .NET](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [Jak renderovat CAD a převést DWG – Aspose.CAD .NET](/cad/net/conversion-and-export/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}