---
date: 2026-03-29
description: Naučte se rychle nahrazovat písma v Aspose.CAD pro .NET. Tento krok‑za‑krokem
  průvodce vám ukáže, jak nastavit primární název písma a efektivně upravit CAD výkresy.
linktitle: Substituting Fonts
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Jak nahradit fonty v Aspose.CAD pro .NET
url: /cs/net/cad-features-and-support/substituting-fonts/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak nahradit písma v Aspose.CAD pro .NET

## Úvod

V oblasti vývoje CAD pomocí .NET je naučit se **jak nahradit písma** klíčová dovednost, která může výrazně zlepšit vizuální kvalitu vašich výkresů. Aspose.CAD pro .NET nabízí jednoduché API, které vám umožní **nastavit primární název písma** pro libovolný styl, což usnadňuje globální nebo selektivní nahrazení písma. V tomto tutoriálu projdeme celý proces – od načtení výkresu po výměnu písma buď globálně, nebo podle konkrétního názvu stylu.

## Rychlé odpovědi
- **Jaká je hlavní třída pro manipulaci s CAD?** `Aspose.CAD.Image` (nebo její odvozená `CadImage`).
- **Která vlastnost mění písmo?** `PrimaryFontName` on `CadStyleTableObject`.
- **Mohu nahradit písma pro všechny styly najednou?** Ano, iterujte přes `cadImage.Styles` a nastavte tuto vlastnost.
- **Potřebuji licenci pro produkci?** Platná licence Aspose.CAD je vyžadována pro ne‑zkušební použití.
- **Podporované verze .NET?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## Co je nahrazení písma v CAD?
Nahrazení písma znamená výměnu původního typografického řezu použitého v CAD výkresu za jiný, který je dostupný na cílovém systému. To je zvláště užitečné, když původní písmo chybí, když potřebujete jednotný firemní styl, nebo při přípravě výkresů k tisku na zařízeních, která podporují jen omezenou sadu písem.

## Proč nahradit písma pomocí Aspose.CAD?
- **Žádné externí závislosti** – knihovna interně zpracovává mapování písem.
- **Funguje s mnoha formáty** – DXF, DWG, DGN a další.
- **Programová kontrola** – automatizujte proces pro dávkové konverze nebo CI pipeline.
- **Zachovává geometrii výkresu** – mění se pouze vizuální reprezentace textu.

## Požadavky

- Základní znalost programování v .NET.
- Aspose.CAD pro .NET nainstalováno. Pokud jste jej ještě nenainstalovali, stáhněte jej [zde](https://releases.aspose.com/cad/net/).
- CAD soubor (DXF, DWG, atd.) pro experimentování.

## Importujte jmenné prostory

Před zahájením importujte potřebné jmenné prostory, abyste získali přístup k funkcím Aspose.CAD ve vaší .NET aplikaci.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad.CadTables;
```

## Krok 1: Načíst CAD výkres

Začněte načtením CAD výkresu do instance `CadImage`. Ujistěte se, že zadáte správnou cestu k adresáři s dokumenty.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (CadImage cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    // Your code for further actions goes here
}
```

## Krok 2: Procházet styly

Dále iterujte přes styly v CAD výkresu pomocí smyčky `foreach`. To vám umožní přistupovat k jednotlivým stylům písma a manipulovat s nimi.

```csharp
foreach (CadStyleTableObject style in cadImage.Styles)
{
    // Your code for style manipulation goes here
}
```

## Jak nastavit primární název písma pro nahrazení písma

Vlastnost `PrimaryFontName` na každém `CadStyleTableObject` určuje, které písmo se použije při vykreslování výkresu. Nastavením této vlastnosti efektivně nahradíte původní písmo.

### Krok 3: Nahrazení písem globálně

Pro nahrazení písem pro **všechny** styly nastavte vlastnost `PrimaryFontName` pro každý styl na požadovaný název písma, například `"Arial"`.

```csharp
foreach (CadStyleTableObject style in cadImage.Styles)
{
    style.PrimaryFontName = "Arial";
}
```

### Krok 4: Nahrazení písma podle názvu stylu

Pokud potřebujete nahradit písmo jen pro konkrétní styl (např. styl s názvem `"Roman"`), přidejte podmínku uvnitř smyčky.

```csharp
foreach (CadStyleTableObject style in cadImage.Styles)
{
    if (style.StyleName == "Roman")
    {
        style.PrimaryFontName = "Arial";
    }
}
```

## Časté problémy a řešení

| Problém | Příčina | Řešení |
|---------|---------|--------|
| Písmo se po spuštění kódu nezmění | Výkres je v mezipaměti nebo otevřen v režimu jen pro čtení | Ujistěte se, že po úpravě obrázek uložíte (`cadImage.Save(...)`) nebo soubor znovu načtete pro ověření. |
| Požadované písmo není v systému nalezeno | Písmo není nainstalováno na počítači, kde se kód spouští | Nainstalujte požadované TrueType/OpenType písmo nebo jej vložte do zdrojů aplikace. |
| Text se zobrazuje poškozeně | Nesprávné kódování nebo chybějící podpora Unicode | Použijte písmo, které podporuje požadovanou znakovou sadu (např. Arial Unicode MS). |

## Často kladené otázky

**Q: Mohu v Aspose.CAD pro .NET vrátit změny písma zpět?**  
A: Ano, můžete vrátit změny načtením původního CAD výkresu nebo uchováním záložní kopie před provedením úprav.

**Q: Existují další vlastnosti písma, které mohu upravit?**  
A: Rozhodně. Kromě `PrimaryFontName` můžete pracovat s `SecondaryFontName`, `FontFamily` a dalšími atributy souvisejícími se stylem pro pokročilé přizpůsobení.

**Q: Je Aspose.CAD kompatibilní s různými CAD formáty?**  
A: Ano, Aspose.CAD podporuje širokou škálu formátů, jako jsou DXF, DWG, DGN, DWF a další, což vám poskytuje flexibilitu napříč projekty.

**Q: Mohu automatizovat nahrazení písma ve dávkovém zpracování?**  
A: Určitě. Zabalte logiku načítání a nahrazení do smyčky, která prochází složku s CAD soubory, nebo ji integrujte do CI/CD pipeline.

**Q: Kde mohu najít další podporu pro Aspose.CAD pro .NET?**  
A: Pro další podporu a diskuse v komunitě navštivte [Aspose.CAD fórum](https://forum.aspose.com/c/cad/19).

---

**Poslední aktualizace:** 2026-03-29  
**Testováno s:** Aspose.CAD for .NET (latest release)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}