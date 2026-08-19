---
date: 2026-03-19
description: Naučte se, jak změnit velikost CAD výkresů v .NET pomocí Aspose.CAD,
  včetně škálování jednotek CAD výkresu a úpravy velikosti rozvržení. Postupujte podle
  našeho krok‑za‑krokem průvodce.
linktitle: Adjusting CAD Drawing Size
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Jak změnit velikost CAD výkresů pomocí Aspose.CAD pro .NET
url: /cs/net/cad-drawing-manipulation/adjust-cad-drawing-size/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak změnit velikost CAD výkresů pomocí Aspose.CAD pro .NET

## Úvod

Pokud potřebujete **jak změnit velikost CAD** soubory přímo z vaší .NET aplikace, jste na správném místě. V tomto tutoriálu vám ukážeme, jak změnit nastavení jednotek CAD, měřítko rozměrů CAD výkresu a programově upravit velikost CAD pomocí Aspose.CAD pro .NET. Na konci průvodce budete mít pevné, připravené řešení pro změnu velikosti libovolného podporovaného formátu CAD.

## Rychlé odpovědi
- **Jaká knihovna je vyžadována?** Aspose.CAD for .NET  
- **Mohu změnit typ jednotky?** Ano – nastavte `UnitType` v `CadRasterizationOptions`  
- **Je pro produkci potřeba licence?** Platná licence Aspose.CAD je vyžadována pro ne‑zkušební použití  
- **Do jakého formátu obrázku příklad exportuje?** BMP (ale funguje jakýkoli podporovaný rastrový formát)  
- **Kolik řádků kódu?** Méně než 30 řádků pro kompletní operaci změny velikosti  

## Co znamená „jak změnit velikost CAD“ v praxi?
Změna velikosti CAD výkresu znamená převod vektorových dat na rastrový obrázek v konkrétním měřítku nebo jednotce (např. centimetry, palce). To je užitečné, když potřebujete vložit výkresy do zpráv, generovat náhledy nebo integrovat CAD vizuály do webových stránek.

## Proč upravovat velikost CAD pomocí Aspose.CAD?
- **Žádný externí CAD software** – vše běží uvnitř vašeho .NET kódu.  
- **Detailní kontrola** nad jednotkami, rozvrženími a možnostmi rasterizace.  
- **Podpora napříč formáty** – stejný kód funguje pro DWG, DXF, DWF a další.  

## Předpoklady

Předtím, než se pustíme dál, ujistěte se, že máte:

- Knihovnu Aspose.CAD pro .NET: Stáhněte a nainstalujte knihovnu ze [stránky ke stažení Aspose.CAD pro .NET](https://releases.aspose.com/cad/net/).  
- Vzorek CAD výkresu: Soubor jako `sample.dwg` umístěný ve složce dokumentů vašeho projektu.  

## Importujte jmenné prostory

Nejprve importujte jmenné prostory, které vám poskytují přístup ke třídám Aspose.CAD.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Krok 1: Načtěte CAD výkres

Načtěte zdrojový soubor do objektu `Image`. Tento objekt představuje CAD výkres v paměti a bude základem pro všechny další operace.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "sample.dwg";

// Load a CAD drawing in an instance of Image
using (var image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // Your code here...
}
```

## Krok 2: Vytvořte BmpOptions (nebo jakýkoli jiný rastrový formát)

`BmpOptions` říká Aspose.CAD, jak vykreslit vektorová data při uložení jako bitmapu. Můžete jej nahradit `PngOptions`, `JpegOptions` atd., v závislosti na požadovaném formátu.

```csharp
Aspose.CAD.ImageOptions.BmpOptions bmpOptions = new Aspose.CAD.ImageOptions.BmpOptions();
```

## Krok 3: Nastavte CadRasterizationOptions

`CadRasterizationOptions` obsahuje základní nastavení pro měřítko, převod jednotek a výběr rozvržení. Propojení s vlastností `VectorRasterizationOptions` objektu `BmpOptions` zajišťuje, že rasterizér použije vaše vlastní nastavení.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions cadRasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
bmpOptions.VectorRasterizationOptions = cadRasterizationOptions;
```

## Krok 4: Nastavte UnitType (změna jednotky CAD)

Zde měníme jednotku CAD z výchozí na centimetry. Zde se nachází klíčové slovo **change cad unit**, a přímo ovlivňuje konečnou velikost obrázku.

```csharp
cadRasterizationOptions.UnitType = Aspose.CAD.ImageOptions.UnitType.Centimeter;
```

## Krok 5: Vyberte rozvržení (nastavení CAD rozvržení)

Pokud váš výkres obsahuje více rozvržení (např. Model, Sheet1), uveďte, která chcete rasterizovat. Výběr správného rozvržení je nezbytný, když **set cad layouts** pro výstup s upravenou velikostí.

```csharp
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## Krok 6: Export do BMP (změna velikosti CAD výkresu)

Nakonec uložte rasterizovaný obrázek. Výstupní soubor odráží novou velikost, jednotku a rozvržení, které jste nastavili — tím se efektivně dokončuje operace **resize CAD drawing**.

```csharp
string outPath = sourceFilePath + ".bmp";
image.Save(outPath, bmpOptions);
```

Nyní máte BMP soubor, který představuje změněnou velikost CAD výkresu, připravený k dalšímu zpracování nebo zobrazení.

## Časté problémy a řešení

| Problém | Proč k tomu dochází | Řešení |
|-------|----------------|-----|
| Výstup je rozmazaný | Nízké DPI (bodů na palec) výchozí | Nastavte `cadRasterizationOptions.Resolution = 300;` před uložením |
| Zobrazí se špatné rozvržení | Chybný název rozvržení | Ověřte přesný název rozvržení pomocí CAD prohlížeče nebo kolekce `Layouts` |
| Převod jednotek vypadá špatně | Míchání metrických a imperiálních jednotek | Ujistěte se, že `UnitType` odpovídá požadovanému měřicímu systému |

## Často kladené otázky

### Q1: Je Aspose.CAD pro .NET kompatibilní se všemi CAD formáty?
A1: Aspose.CAD pro .NET podporuje širokou škálu CAD formátů, včetně DWG, DXF, DWF a dalších. Zkontrolujte [dokumentaci](https://reference.aspose.com/cad/net/) pro kompletní seznam.

### Q2: Mohu změnit velikost více rozvržení najednou?
A2: Ano, můžete změnit velikost více rozvržení úpravou pole `Layouts` v `CadRasterizationOptions`.

### Q3: Kde mohu získat podporu pro Aspose.CAD pro .NET?
A3: Navštivte [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) pro komunitní podporu a pomoc.

### Q4: Je k dispozici bezplatná zkušební verze?
A4: Ano, můžete vyzkoušet [bezplatnou zkušební verzi](https://releases.aspose.com/) k vyhodnocení funkcí Aspose.CAD pro .NET.

### Q5: Jak mohu získat dočasnou licenci pro Aspose.CAD pro .NET?
A5: Získejte dočasnou licenci pro testovací účely [zde](https://purchase.aspose.com/temporary-license/).

## Často kladené otázky

**Q: Jak mohu měřítko CAD výkresu změnit, aniž bych měnil typ jednotky?**  
A: Upravit vlastnost `Zoom` v `CadRasterizationOptions` (např. `cadRasterizationOptions.Zoom = 2.0;`) pro zdvojnásobení velikosti při zachování původní jednotky.

**Q: Můžu exportovat do jiných formátů než BMP?**  
A: Rozhodně. Nahraďte `BmpOptions` za `PngOptions`, `JpegOptions` nebo jakoukoli jinou podporovanou třídu rastrového formátu.

**Q: Je možné hromadně zpracovat složku výkresů?**  
A: Ano. Procházejte soubory ve složce, použijte stejnou logiku rasterizace a uložte každý výstup pod jedinečným názvem.

---

**Poslední aktualizace:** 2026-03-19  
**Testováno s:** Aspose.CAD pro .NET 24.11 (nejnovější v době psaní)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}