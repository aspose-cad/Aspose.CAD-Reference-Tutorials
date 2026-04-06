---
date: 2026-04-06
description: Naučte se, jak převést DWF na JPG v C# pomocí Aspose.CAD a zjistěte,
  jak extrahovat velikost rozvržení DWF z DWG souborů.
keywords:
- convert dwf to jpg
- how to extract dwf
- convert dwg to jpg
linktitle: Práce s DWG soubory v C# – Získání velikosti DWF rozvržení
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Převod DWF na JPG v C# – Získat velikost rozvržení DWF z DWG
url: /cs/net/dwg-file-manipulation/get-size-of-dwf-layout/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Převod DWF na JPG v C# – Získání velikosti rozvržení DWF z DWG

## Úvod

Pokud potřebujete **převést DWF na JPG** a zároveň zjistit přesné rozměry rozvržení, jste na správném místě. V tomto tutoriálu projdeme kompletním příkladem od začátku do konce, který používá Aspose.CAD pro .NET k otevření souboru DWF odvozeného z DWG, načte velikost každého rozvržení a uloží rozvržení jako vysoce kvalitní JPG obrázek. Na konci nejenže budete vědět, jak získat informace o rozvržení DWF, ale také budete mít znovupoužitelný úryvek kódu, který můžete vložit do libovolného C# projektu.

## Rychlé odpovědi
- **Co znamená „convert DWF to JPG“?** Znamená to rasterizaci vektorového rozvržení DWF do bitmapového JPEG obrázku.  
- **Proč nejprve číst velikost rozvržení?** Znalost přesných rozměrů vám umožní nastavit správné rozměry stránky a vyhnout se nataženému nebo oříznutému výstupu.  
- **Která knihovna to provádí?** Aspose.CAD pro .NET poskytuje plnou podporu pro DWG, DWF a konverzi rasterových obrázků.  
- **Potřebuji licenci?** Dočasná licence funguje pro hodnocení; plná licence je vyžadována pro produkční nasazení.  
- **Jaké verze .NET jsou podporovány?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## Co je „convert DWF to JPG“ a proč je to důležité?

Převod souboru DWF (Design Web Format) na JPG vytvoří přenosný obrázek, který lze zobrazit v prohlížečích, vložit do zpráv nebo sdílet se zainteresovanými stranami, které nemají CAD software. Konverze vám také poskytuje flexibilitu manipulovat s obrázkem (změna velikosti, komprese, vodoznak) pomocí standardních nástrojů pro zpracování obrázků.

## Proč extrahovat velikost rozvržení DWF?

Soubor DWF může obsahovat více rozvržení, každé se svým koordinátním systémem a jednotkami (palce, milimetry atd.). Extrahování velikosti rozvržení vám umožní:

1. Zachovat původní poměr stran při rasterizaci.  
2. Vybrat správné DPI pro výstup ve vysokém rozlišení.  
3. Automatizovat dávkové zpracování mnoha rozvržení bez ručního ladění.

## Požadavky

Aby byl tento tutoriál proveditelný bez problémů, ujistěte se, že máte následující předpoklady:

- Aspose.CAD pro .NET: Ujistěte se, že máte nainstalovaný Aspose.CAD pro .NET. Můžete jej stáhnout ze [Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/).

Mít knihovnu připravenou znamená, že se můžete soustředit na kód místo hledání závislostí.

## Importovat jmenné prostory

Než začneme kódovat, importujte požadované jmenné prostory. Poskytují třídy, které budeme potřebovat pro práci se soubory CAD, možnostmi rasterizace a I/O souborů.

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Dwf;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

## Krok 1: Nastavte své prostředí

Vytvořte nový C# console nebo class‑library projekt, přidejte odkaz na **Aspose.CAD.dll** a ujistěte se, že projekt cílí na kompatibilní verzi .NET.

## Krok 2: Definujte cesty k souborům (jak extrahovat DWF)

Určete, kde se nachází váš zdrojový soubor DWF a kam mají být zapisovány vygenerované JPG soubory.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "blocks_and_tables.dwf";
```

> **Tip:** Použijte `Path.Combine(MyDir, "blocks_and_tables.dwf")` pro bezpečnější práci s cestami na různých OS.

## Krok 3: Načtěte obrázek DWF

Načtěte soubor DWF do objektu `Aspose.CAD.Image`. Přetypujeme jej na `DwfImage`, protože potřebujeme přístup k vlastnostem specifickým pro jednotlivé stránky.

```csharp
using (DwfImage image = (DwfImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    // Code for further steps will go here
}
```

## Krok 4: Procházejte stránky

DWF může obsahovat několik stránek (rozvržení). Projděte každou, abychom je mohli zpracovat jednotlivě.

```csharp
foreach (var page in image.Pages)
{
    // Code for further steps will go here
}
```

## Krok 5: Získejte informace o rozvržení

Uvnitř smyčky načtěte název rozvržení. Tento název bude použit jak pro logování, tak pro pojmenování výstupního JPG souboru.

```csharp
var layout = page.Name;
System.Console.WriteLine("Layout= " + layout);
```

## Krok 6: Nastavte možnosti JPG

Vytvořte instanci `JpegOptions` a nakonfigurujte možnosti rasterizace. Vlastnost `Layouts` říká Aspose.CAD, které rozvržení má renderovat.

```csharp
using (FileStream fs = new FileStream(MyDir + "layout_" + layout + ".jpg", FileMode.Create))
{
    JpegOptions jpegOptions = new JpegOptions();
    CadRasterizationOptions options = new CadRasterizationOptions();
    options.Layouts = new string[] { layout };
    // Code for further steps will go here
}
```

## Krok 7: Určete velikost stránky (převod dwg na jpg)

Vypočítejte šířku a výšku rozvržení v jeho nativních jednotkách. Tyto informace jsou nezbytné pro správné nastavení velikosti rasterové stránky.

```csharp
double sizeExtX = page.MaxPoint.X - page.MinPoint.X;
double sizeExtY = page.MaxPoint.Y - page.MinPoint.Y;
// Code for further steps will go here
```

## Krok 8: Nastavte rozměry stránky

Převeďte nativní jednotky (palce nebo milimetry) na pixely pomocí pomocných metod poskytovaných Aspose.CAD. Pokud typ jednotky není ani jeden z nich, použijeme surové hodnoty.

```csharp
if (page.UnitType == UnitType.Inch)
{
    options.PageHeight = CommonHelper.INtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.INtoPixels(sizeExtX, CommonHelper.DPI);
}
else if (page.UnitType == UnitType.Millimeter)
{
    options.PageHeight = CommonHelper.MMtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.MMtoPixels(sizeExtX, CommonHelper.DPI);
}
else
{
    options.PageHeight = (float)sizeExtY;
    options.PageWidth = (float)sizeExtX;
}
```

## Krok 9: Uložte soubor JPG

Nakonec svázete možnosti rasterizace s JPEG možnostmi a uložíte obrázek na disk.

```csharp
jpegOptions.VectorRasterizationOptions = options;
image.Save(fs, jpegOptions);
}
```

Po dokončení smyčky budete mít JPG soubor pro každé rozvržení, každý přesně odpovídající původním rozměrům DWF.

## Časté problémy a řešení

| Příznak | Pravděpodobná příčina | Oprava |
|---------|-----------------------|--------|
| Prázdný JPG výstup | `options.Layouts` není nastaveno správně | Ověřte, že název rozvržení odpovídá `page.Name`. |
| Deformovaný obrázek | Špatná konverze DPI | Použijte `CommonHelper.DPI = 300` (nebo požadované DPI) před konverzí. |
| Soubor nenalezen | Nesprávná cesta `MyDir` | Použijte absolutní cesty nebo `Path.Combine`. |
| Výjimka licence | Licence nebyla načtena | Načtěte dočasnou nebo trvalou licenci před voláním `Image.Load`. |

## Často kladené otázky

### Q1: Je Aspose.CAD kompatibilní s nejnovějšími formáty DWG?

A1: Aspose.CAD podporuje různé formáty DWG, včetně nejnovějších verzí. Podrobnosti o kompatibilitě najdete v [documentation](https://reference.aspose.com/cad/net/).

### Q2: Mohu použít Aspose.CAD pro komerční i osobní projekty?

A2: Ano, Aspose.CAD nabízí flexibilní licenční možnosti pro komerční i osobní použití. Navštivte [purchase page](https://purchase.aspose.com/buy) pro více informací.

### Q3: Jak získám dočasnou licenci pro Aspose.CAD?

A3: Dočasnou licenci můžete získat [zde](https://purchase.aspose.com/temporary-license/) pro evaluační účely.

### Q4: Kde mohu najít podporu pro Aspose.CAD?

A4: Pro jakékoli dotazy nebo pomoc navštivte [Aspose.CAD forum](https://forum.aspose.com/c/cad/19).

### Q5: Je k dispozici bezplatná zkušební verze Aspose.CAD?

A5: Ano, bezplatnou zkušební verzi Aspose.CAD najdete [zde](https://releases.aspose.com/).

### Q6: Jak převést soubor DWG přímo na JPG bez předchozího extrahování DWF?

A6: Můžete načíst soubor DWG pomocí `Aspose.CAD.Image.Load` a použít stejný workflow rasterizace; jen nastavte `options.Layouts` na požadovaný název rozvržení z DWG.

### Q7: Zachovává konverze vektorovou kvalitu?

A7: Po rasterizaci do JPG se obrázek stane bitmapovým, takže vektorová škálovatelnost se ztrácí. Pro bezztrátové škálování zvažte export do PNG nebo SVG.

---

**Last Updated:** 2026-04-06  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}