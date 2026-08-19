---
date: 2026-03-21
description: Naučte se, jak získat velikost rozvržení CAD v .NET pomocí Aspose.CAD.
  Postupujte podle našeho krok‑za‑krokem průvodce pro efektivní manipulaci s CAD soubory.
linktitle: Get Size of CAD Layout
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Získat velikost rozvržení CAD v Aspose.CAD pro .NET
url: /cs/net/cad-drawing-manipulation/get-size-of-cad-layout/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Získání velikosti CAD rozvržení v Aspose.CAD pro .NET

## Úvod

V tomto komplexním tutoriálu se dozvíte **jak získat velikost CAD rozvržení** pomocí knihovny Aspose.CAD pro .NET. Ať už vytváříte CAD prohlížeč, generujete náhledy, nebo potřebujete přesné rozměry rozvržení pro následné zpracování, znalost přesné velikosti každého rozvržení je nezbytná. Provedeme vás celým pracovním postupem – od načtení výkresu po získání rozměrů rozvržení a případné uložení jako obrázku – abyste tuto funkci mohli s jistotou integrovat do svých aplikací.

## Rychlé odpovědi
- **Co znamená “získat velikost CAD rozvržení”?** Jedná se o získání šířky a výšky (v jednotkách výkresu) každého ne‑prázdného rozvržení v CAD souboru.  
- **Která knihovna to podporuje?** Aspose.CAD pro .NET poskytuje jednoduché API pro přístup k informacím o rozvržení.  
- **Potřebuji licenci?** Bezplatná zkušební verze funguje pro hodnocení; pro produkční použití je vyžadována komerční licence.  
- **Podporované formáty?** DWG, DXF a mnoho dalších CAD/BIM formátů je plně podporováno.  
- **Typická doba implementace?** Přibližně 10‑15 minut pro základní rutinu získání velikosti.

## Co znamená “získat velikost CAD rozvržení”?
Získání velikosti CAD rozvržení znamená extrahování geometrických rozměrů každého rozvržení (paper space) definovaného v CAD výkresu. Tyto rozměry jsou vyjádřeny v nativních jednotkách výkresu (obvykle milimetry nebo palce) a jsou užitečné pro úkoly jako škálování, tisk nebo generování náhledových obrázků.

## Proč získávat velikost CAD rozvržení pomocí Aspose.CAD?
- **Není potřeba CAD software** – Funguje zcela na straně serveru.  
- **Cross‑platform** – Funguje s .NET Framework, .NET Core i .NET 5/6+.  
- **Přesná měření** – Vrací přesné rozměry tak, jak jsou uloženy v souboru, čímž se vyhnete ručnímu parsování.  
- **Jednoduchá integrace** – Jednoduché volání API se přirozeně zapadá do existujících C# projektů.

## Požadavky

Než se pustíme do kódu, ujistěte se, že máte následující:

- Aspose.CAD pro .NET nainstalovaný. Můžete jej stáhnout ze [stránky ke stažení Aspose.CAD pro .NET](https://releases.aspose.com/cad/net/).
- Jeden nebo více CAD souborů (DWG, DXF, atd.), které chcete analyzovat. Tento návod používá `conic_pyramid.dxf` a `Bottom_plate.dwg` jako ukázkové soubory.

## Importování jmenných prostorů

Ve svém .NET projektu začněte importováním požadovaných jmenných prostorů:

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.ImageOptions;
```

## Krok 1: Nastavení adresáře dokumentů

Definujte složku, která obsahuje vaše CAD soubory. Nahraďte zástupný text skutečnou cestou na vašem počítači.

```csharp
string MyDir = "Your Document Directory";
```

## Krok 2: Specifikace cest k souborům CAD

Vytvořte pole, které ukazuje na každý CAD soubor, který chcete zpracovat.

```csharp
string[] sourceFilePaths = new[]
{
    MyDir + "conic_pyramid.dxf",
    MyDir + "Bottom_plate.dwg"
};
```

## Krok 3: Procházení souborů CAD

Načtěte každý soubor, detekujte jeho formát a připravte se na extrakci informací o rozvržení.

```csharp
foreach (var sourceFilePath in sourceFilePaths)
{
    string extension = Path.GetExtension(sourceFilePath);
    using (CadImage cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath))
    {
        // ... (continue to the next step)
    }
}
```

## Krok 4: Získání ne‑prázdných rozvržení

Potřebujeme pomocnou metodu, která vrátí pouze rozvržení, která skutečně obsahují entity výkresu. Prázdná rozvržení jsou ignorována, protože nemají žádnou velikost k nahlášení.

```csharp
private static List<string> GetNotEmptyLayouts(Image cadImage, string extension)
{
    // ... (continue to the next step)
}
```

## Krok 5: Získání rozvržení pro soubory DWG

DWG soubory ukládají informace o rozvržení v tabulce `HeaderVariables`. Následující metoda extrahuje názvy všech ne‑prázdných rozvržení pro DWG výkres.

```csharp
private static List<string> GetNotEmptyLayoutsForDwg(CadImage cadImage)
{
    // ... (continue to the next step)
}
```

## Krok 6: Získání rozvržení pro soubory DXF

DXF soubory používají odlišnou strukturu. Tato metoda prochází kolekci `Tables` a hledá paper space rozvržení, která obsahují entity.

```csharp
private static List<string> GetNotEmptyLayoutsForDxf(CadImage cadImage)
{
    // ... (continue to the next step)
}
```

## Krok 7: Získání velikosti rozvržení a uložení jako obrázek

Nakonec projděte každé nalezené rozvržení, přečtěte jeho rozměry a případně vykreslete rozvržení do obrázkového souboru pro vizuální ověření.

```csharp
foreach (string layout in layouts)
{
    // ... (continue to the next step)
}
```

## Časté problémy a tipy

- **Chybějící názvy rozvržení:** Ujistěte se, že CAD soubor skutečně obsahuje paper space rozvržení; některé soubory mají jen model space.  
- **Nesprávné jednotky:** Velikost je vrácena v nativních jednotkách výkresu. V případě potřeby ji převeďte na milimetry nebo palce.  
- **Výkon:** Načítání velmi velkých DWG/DXF souborů může být náročné na paměť; zvažte asynchronní zpracování nebo dávkování souborů.

## Často kladené otázky

**Q: Je Aspose.CAD kompatibilní se všemi formáty CAD souborů?**  
A: Ano, Aspose.CAD podporuje širokou škálu formátů, včetně DWG, DXF, DGN a mnoha BIM typů souborů.

**Q: Mohu přizpůsobit možnosti ukládání obrázku?**  
A: Rozhodně! Můžete upravit `CadRasterizationOptions` (formát, rozlišení, barvu pozadí atd.) podle svých konkrétních potřeb.

**Q: Kde najdu další dokumentaci?**  
A: Viz [dokumentace Aspose.CAD](https://reference.aspose.com/cad/net/) pro podrobné reference API a další příklady.

**Q: Je k dispozici bezplatná zkušební verze?**  
A: Ano, můžete si vyzkoušet Aspose.CAD pomocí [bezplatné zkušební verze](https://releases.aspose.com/).

**Q: Jak získám technickou podporu?**  
A: Pro technickou podporu navštivte [forum Aspose.CAD](https://forum.aspose.com/c/cad/19).

---

**Poslední aktualizace:** 2026-03-21  
**Testováno s:** Aspose.CAD 24.11 pro .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}