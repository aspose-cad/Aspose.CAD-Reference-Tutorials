---
date: 2026-03-24
description: Naučte se, jak převést DGN na PNG a uložit CAD jako JPEG pomocí Aspose.CAD
  pro .NET – rychlý průvodce konverzí CAD na obrázek.
linktitle: Export DGN to Raster Image
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Jak převést DGN na PNG v Aspose.CAD pro .NET
url: /cs/net/cad-export-formats/export-dgn-to-raster-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Převod DGN na PNG v Aspose.CAD pro .NET

V moderním vývoji .NET je **convert dgn to png** běžnou požadavkem, když potřebujete zobrazit CAD výkresy na webu nebo je vložit do zpráv. Aspose.CAD pro .NET usnadňuje tuto konverzi a umožňuje převést soubor DGN na vysoce kvalitní rastrový obrázek pomocí několika řádků kódu. V tomto průvodci vás provedeme celým procesem, od nastavení projektu až po uložení finálního souboru PNG (nebo JPEG).

## Rychlé odpovědi
- **Mohu převést DGN na PNG pomocí Aspose.CAD?** Ano – stačí nakonfigurovat možnosti rasterizace a zvolit výstup PNG nebo JPEG.  
- **Potřebuji licenci pro produkční použití?** Platná licence Aspose.CAD je vyžadována pro nasazení mimo zkušební verzi.  
- **Které verze .NET jsou podporovány?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7.  
- **Jaké formáty obrázků jsou k dispozici?** PNG, JPEG, BMP, GIF, TIFF a další.  
- **Je nutná obsluha výjimek?** Rozhodně – zabalte konverzi do try/catch pro řešení problémů s přístupem k souborům.

## Co je “convert dgn to png”?
Převod souboru DGN (MicroStation) na PNG znamená rasterizaci vektorových CAD dat do obrázku založeného na pixelech. To je užitečné pro generování náhledů, vkládání výkresů do HTML e‑mailů nebo vytváření miniatur pro systémy správy dokumentů.

## Proč použít Aspose.CAD pro konverzi CAD na obrázek?
- **Žádné externí závislosti** – funguje čistě v řízeném kódu.  
- **Vysoká věrnost** – zachovává tloušťky čar, vrstvy a barvy.  
- **Flexibilní výstup** – přepínáte mezi PNG, JPEG, BMP atd. změnou jediné volby.  
- **Optimalizovaný výkon** – rasterizace je rychlá i u velkých výkresů.

## Předpoklady

Než začneme, ujistěte se, že máte:

- **Aspose.CAD for .NET** nainstalovaný ve vašem projektu. Můžete jej stáhnout z [webu](https://reference.aspose.com/cad/net/).  
- Vzorek souboru DGN (např. `Nikon_D90_Camera.dgn`) umístěný v známém adresáři.

## Importujte jmenné prostory

Začněte přidáním požadovaných `using` direktiv, abyste mohli přistupovat ke třídám Aspose.CAD.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Krok 1: Načtení souboru DGN

Načtěte zdrojový DGN do objektu `CadImage`. Tento objekt představuje CAD výkres v paměti a bude zdrojem pro rasterizaci.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for further processing goes here
}
```

## Krok 2: Definování možností rasterizace

Nastavte, jak má být CAD výkres rasterizován. Zde můžete ovládat velikost obrázku, měřítko a barvu pozadí.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## Krok 3: Výběr výstupního formátu (PNG nebo JPEG)

Ačkoliv se tutoriál zaměřuje na PNG, můžete také chtít **save cad as jpeg**. Vytvořte odpovídající objekt možností obrázku a připojte nastavení rasterizace.

```csharp
ImageOptionsBase options = new JpegOptions();   // Change to PngOptions() for PNG output
options.VectorRasterizationOptions = rasterizationOptions;
```

> **Tip:** Pro vytvoření PNG souboru nahraďte `new JpegOptions()` za `new PngOptions()`.

## Krok 4: Uložení rastrového obrázku

Nakonec zavolejte `Save` na instanci `CadImage`, přičemž zadáte požadovaný název souboru a objekt možností, který jste nakonfigurovali.

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpg", options);
```

Pokud jste přešli na `PngOptions`, soubor bude uložen jako `ExportDGNToRasterImage_out.png`.

## Časté problémy a řešení

| Problém | Příčina | Řešení |
|-------|-------|-----|
| **Prázdný výstupní obrázek** | `NoScaling` nastaveno nesprávně nebo není vybráno rozložení | Nastavte `AutomaticLayoutsScaling = true` nebo specifikujte požadované rozložení. |
| **Nedostatek paměti pro velké soubory** | Načítání obrovského DGN bez streamování | Použijte `Image.Load(sourceFilePath, new LoadOptions { LoadOnDemand = true })`. |
| **Není podporována verze DGN** | Starší verze MicroStation | Ujistěte se, že máte nejnovější verzi Aspose.CAD, která podporuje starší formáty. |

## Často kladené otázky

**Q: Mohu exportovat soubory DGN do formátů jiných než JPEG?**  
A: Ano, Aspose.CAD pro .NET podporuje PNG, BMP, GIF, TIFF a další – stačí vyměnit třídu možností (např. `new PngOptions()`).

**Q: Jak mám během konverze zacházet s výjimkami?**  
A: Zabalte kód konverze do bloku `try/catch` a zaznamenejte `Aspose.CAD.CadException` pro podrobné informace o chybě.

**Q: Je k dispozici zkušební verze Aspose.CAD pro .NET?**  
A: Ano, můžete produkt vyzkoušet zdarma. Navštivte [zde](https://releases.aspose.com/) pro více informací.

**Q: Kde mohu získat pomoc nebo diskutovat o problémech souvisejících s Aspose.CAD pro .NET?**  
A: Navštivte [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) pro podporu komunity a diskuse.

**Q: Jak získám dočasnou licenci pro Aspose.CAD pro .NET?**  
A: Navštivte [tento odkaz](https://purchase.aspose.com/temporary-license/) a získejte dočasnou licenci pro vaše vývojové potřeby.

## Závěr

Nyní jste se naučili, jak **convert dgn to png** (nebo JPEG) pomocí Aspose.CAD pro .NET. Úpravou možností rasterizace a výměnou třídy možností obrázku můžete přizpůsobit výstup jakémukoli požadavku projektu. Nebojte se experimentovat s různými velikostmi stránek, nastavením DPI a formáty souborů, abyste získali dokonalý rastrový obrázek pro vaši aplikaci.

---

**Poslední aktualizace:** 2026-03-24  
**Testováno s:** Aspose.CAD 24.11 for .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}