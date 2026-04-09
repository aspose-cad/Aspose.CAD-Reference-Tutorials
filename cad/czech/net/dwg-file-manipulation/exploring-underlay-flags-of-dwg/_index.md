---
date: 2026-04-09
description: Naučte se, jak převést DWG na obrázek a jak číst příznaky podkladů pomocí
  Aspose.CAD pro .NET v tomto krok‑za‑krokem průvodci.
keywords:
- convert dwg to image
- how to read underlay
- Aspose.CAD DWG underlay flags
linktitle: Zkoumání podkladových příznaků DWG souborů
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Převod DWG na obrázek – Zkoumání podkladových příznaků souborů DWG – Tutoriál
  Aspose.CAD
url: /cs/net/dwg-file-manipulation/exploring-underlay-flags-of-dwg/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Prozkoumání příznaků podkladů souborů DWG – tutoriál Aspose.CAD

## Úvod

Pokud se ponořujete do složitého světa CAD souborů, konkrétně souborů DWG, a chcete **převést DWG na obrázek** a zároveň zjistit **jak číst příznaky podkladů**, jste na správném místě. Tento tutoriál vás provede každým krokem pomocí výkonné knihovny Aspose.CAD pro .NET, takže můžete získat informace o podkladech a vykreslit výkres jako obrázek s jistotou.

## Rychlé odpovědi
- **Co znamená “convert DWG to image”?**  
  Znamená to vykreslení výkresu DWG do rastrového formátu (PNG, JPEG, atd.) pomocí Aspose.CAD.
- **Která metoda odhalí příznaky podkladů?**  
  Přístup k vlastnosti `Flags` objektu `CadUnderlay` po načtení DWG.
- **Potřebuji licenci pro Aspose.CAD?**  
  Pro hodnocení je k dispozici dočasná licence; pro produkci je vyžadována plná licence.
- **Jaké verze .NET jsou podporovány?**  
  .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6 a novější.
- **Mohu získat geometrii podkladu?**  
  Ano – cesta podkladu, vkládací bod, měřítko, rotace a stavy příznaků jsou všechny přístupné.

## Co je “convert DWG to image” a proč je to důležité?

Převod souboru DWG na obrázek vám umožní zobrazit CAD výkresy v prohlížečích, vložit je do zpráv nebo sdílet s partnery, kteří nemají CAD prohlížeč. Při vykreslování často potřebujete zkontrolovat objekty **underlay** (např. odkazy na DGN), aby se zobrazily správně. Porozumění příznakům podkladů vám pomůže řešit problémy s ořezáváním, černobílým vykreslováním a viditelností před vytvořením finálního obrázku.

## Požadavky

- Základní znalost programování v C# a .NET.  
- Knihovna **Aspose.CAD for .NET** nainstalována. Pokud ji ještě nemáte, stáhněte ji **[zde](https://releases.aspose.com/cad/net/)**.  
- Soubor DWG pro testování – ukázkový soubor **“BlockRefDgn.dwg”** je používán v celém tomto průvodci.

## Import jmenných prostorů

Pro zahájení importujte potřebné jmenné prostory:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Krok 1: Načtení souboru DWG a převod na `CadImage`

Nejprve načtěte soubor DWG a přetypujte jej na `CadImage`. Tento objekt vám poskytuje přístup ke všem entitám výkresu, včetně podkladů.

```csharp
string fileName = MyDir + "BlockRefDgn.dwg";

// Load DWG file and convert to CadImage
using (CadImage image = (CadImage)Image.Load(fileName))
{
    // Your code for subsequent steps will go here
}
```

## Krok 2: Procházení entit

Dále projděte každou entitu ve výkresu. Zde najdete objekty podkladů.

```csharp
foreach (CadBaseEntity entity in image.Entities)
{
    // Your code for subsequent steps will go here
}
```

## Krok 3: Kontrola typu `CadDgnUnderlay`

Identifikujte entity podkladů kontrolou jejich runtime typu. Třída `CadDgnUnderlay` představuje DGN podklady vložené do DWG.

```csharp
if (entity is CadDgnUnderlay)
{
    // Your code for subsequent steps will go here
}
```

## Krok 4: Přístup k příznakům podkladu

Jakmile máte `CadDgnUnderlay`, přetypujte jej na `CadUnderlay` a přečtěte jeho vlastnosti a stavy příznaků. Příznaky vám říkají, zda je podklad viditelný, oříznutý nebo vykreslený v černobílém režimu.

```csharp
CadUnderlay underlay = entity as CadUnderlay;

Console.WriteLine(underlay.UnderlayPath);
Console.WriteLine(underlay.UnderlayName);
Console.WriteLine(underlay.InsertionPoint.X);
Console.WriteLine(underlay.InsertionPoint.Y);
Console.WriteLine(underlay.RotationAngle);
Console.WriteLine(underlay.ScaleX);
Console.WriteLine(underlay.ScaleY);
Console.WriteLine(underlay.ScaleZ);
Console.WriteLine((underlay.Flags & UnderlayFlags.UnderlayIsOn) == UnderlayFlags.UnderlayIsOn);
Console.WriteLine((underlay.Flags & UnderlayFlags.ClippingIsOn) == UnderlayFlags.ClippingIsOn);
Console.WriteLine((underlay.Flags & UnderlayFlags.Monochrome) != UnderlayFlags.Monochrome);
```

### Co výstup říká

- **UnderlayPath / UnderlayName** – kde se nachází externí soubor DGN.  
- **InsertionPoint (X, Y)** – souřadnice, kde je podklad umístěn v prostoru DWG.  
- **RotationAngle** – rotace aplikovaná na podklad.  
- **ScaleX / ScaleY / ScaleZ** – škálovací faktory pro každou osu.  
- **Flags** – boolean hodnoty indikující viditelnost (`UnderlayIsOn`), ořezávání (`ClippingIsOn`) a černobílé vykreslení (`Monochrome`).

## Časté problémy a řešení

| Problém | Důvod | Řešení |
|-------|--------|-----|
| Žádný výstup při kontrole příznaků | Příznaky podkladu jsou výchozí 0, když je podklad vypnutý. | Ujistěte se, že DWG skutečně obsahuje aktivní podklad nebo přepněte viditelnost v původním CAD souboru. |
| Výjimka `Invalid cast` | Entita není `CadDgnUnderlay`. | Ověřte podmínku `if (entity is CadDgnUnderlay)` před přetypováním. |
| Vykreslování obrázku selže po extrakci příznaků | Podklad může být oříznutý nebo vypnutý, což vede k prázdné oblasti. | Upravit příznaky (`UnderlayIsOn = true`, `ClippingIsOn = false`) před vykreslením finálního obrázku. |

## Často kladené otázky

### Q1: Mohu použít Aspose.CAD pro .NET s jinými formáty CAD souborů?

A1: Aspose.CAD podporuje různé CAD formáty, včetně DWG, DXF, DGN a dalších. Podívejte se do dokumentace pro úplný seznam.

### Q2: Je k dispozici dočasná licence pro Aspose.CAD pro .NET?

A2: Ano, můžete získat dočasnou licenci **[zde](https://purchase.aspose.com/temporary-license/)**.

### Q3: Kde mohu najít podporu pro Aspose.CAD pro .NET?

A3: Navštivte fórum podpory **[zde](https://forum.aspose.com/c/cad/19)** pro pomoc.

### Q4: Jak si mohu koupit Aspose.CAD pro .NET?

A4: Koupit knihovnu **[zde](https://purchase.aspose.com/buy)**.

### Q5: Je k dispozici bezplatná zkušební verze?

A5: Ano, můžete získat bezplatnou zkušební verzi **[zde](https://releases.aspose.com/)**.

## Závěr

Gratulujeme! Úspěšně jste se naučili **převést DWG na obrázek** a zároveň zvládli **čtení příznaků podkladů** pomocí Aspose.CAD pro .NET. S těmito znalostmi můžete:

- Vykreslovat výkresy DWG jako rastrové obrázky pro web nebo reportovací scénáře.  
- Kontrolovat a manipulovat s vlastnostmi podkladů, aby byl zajištěn správný výstup.  
- Ladit problémy s viditelností, ořezáváním a černobílým režimem před finálním generováním obrázku.

Neváhejte prozkoumat další funkce Aspose.CAD, jako je správa vrstev, extrakce textu a hromadná konverze, abyste dále rozšířili své CAD automatizační workflow.

---

**Poslední aktualizace:** 2026-04-09  
**Testováno s:** Aspose.CAD for .NET 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}