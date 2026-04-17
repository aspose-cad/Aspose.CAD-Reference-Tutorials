---
date: 2026-03-19
description: Naučte se, jak převést CAD na PNG v .NET pomocí Aspose.CAD, efektivně
  uložit CAD jako PNG a zjednodušit svůj pracovní postup s rastrovými obrázky.
linktitle: Convert CAD Drawing to Raster Image
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Převod CAD na PNG v Aspose.CAD pro .NET
url: /cs/net/cad-drawing-manipulation/convert-cad-drawing-to-raster-image/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Převod CAD na PNG v Aspose.CAD pro .NET

## Úvod

V moderních aplikacích zaměřených na CAD je **převod CAD na PNG** běžnou požadavkem — ať už potřebujete generovat náhledy, vkládat výkresy na webové stránky nebo archivovat návrhy jako rastrové obrázky. Tento tutoriál vás provede kompletním procesem převodu CAD výkresu (DXF, DWG, atd.) na vysoce kvalitní PNG soubor pomocí knihovny Aspose.CAD pro .NET. Na konci budete schopni **uložit CAD jako PNG** s plnou kontrolou nad nastavením rasterizace, což zrychlí a zpřesní váš pracovní postup.

## Rychlé odpovědi
- **Jaká knihovna je nejlepší pro převod CAD‑na‑PNG?** Aspose.CAD for .NET.  
- **Jaké souborové formáty lze exportovat do PNG?** DWG, DXF, DGN a další podporované CAD formáty.  
- **Potřebuji licenci pro produkční použití?** Ano, je vyžadována komerční licence; je k dispozici bezplatná zkušební verze.  
- **Mohu přizpůsobit velikost a kvalitu obrázku?** Rozhodně — možnosti rasterizace vám umožní nastavit šířku stránky, výšku, barvu pozadí a další.  
- **Je kód kompatibilní s .NET Core / .NET 6?** Ano, stejné API funguje napříč .NET Framework, .NET Core a .NET 5/6.

## Co je „převod CAD na PNG“?
Převod CAD na PNG znamená rasterizaci vektorových CAD výkresů do pixelového formátu obrázku (PNG). Tento proces zachovává vizuální věrnost a zároveň usnadňuje zobrazování souboru v prohlížečích, mobilních aplikacích nebo jakémkoli prostředí, které nativně nepodporuje CAD formáty.

## Proč použít Aspose.CAD pro převod CAD na PNG?
- **Žádné externí závislosti** — čistý .NET, není potřeba žádný nativní CAD engine.  
- **Plná podpora formátů** — zvládá DWG, DXF, DGN a další.  
- **Detailní kontrola rasterizace** — velikost stránky, rozlišení, pozadí, tloušťka čar atd.  
- **Vysoký výkon** — optimalizováno pro serverové dávkové zpracování.

## Požadavky

Předtím, než začnete, ujistěte se, že máte:

1. **Aspose.CAD for .NET** — stáhněte si jej ze [stránky ke stažení](https://releases.aspose.com/cad/net/).  
2. IDE kompatibilní s .NET (Visual Studio, Rider nebo VS Code) s projektem cílícím na .NET Framework 4.6+ nebo .NET Core 3.1+.  

## Importování jmenných prostorů

Ve svém .NET projektu importujte potřebné jmenné prostory pro přístup k funkcím Aspose.CAD. Přidejte následující kód na začátek svého souboru:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Průvodce krok za krokem

### Krok 1: Definujte cesty k souborům
Nastavte zdrojový CAD soubor a cílovou PNG cestu. Nahraďte zástupný text skutečnou složkou na vašem počítači.

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
```

### Krok 2: Načtěte CAD výkres
Otevřete CAD soubor pomocí `Aspose.CAD.Image.Load`. Tím vytvoříte v‑paměti reprezentaci výkresu, kterou můžete rasterizovat.

```csharp
using (Aspose.CAD.Image image = Aspose.CAD.Image.Load(sourceFilePath))
{
```

### Krok 3: Nakonfigurujte možnosti rasterizace  
Definujte, jak mají být vektorová data převedena na pixely. Zde nastavujeme plátno 1200 × 1200 pixelů, ale můžete upravit `PageWidth` a `PageHeight` podle svých potřeb (např. pro **convert dwg to png** při konkrétním DPI).

```csharp
// Create an instance of CadRasterizationOptions
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
// Set page width & height
rasterizationOptions.PageWidth = 1200;
rasterizationOptions.PageHeight = 1200;
```

> **Pro tip:** Pro zrychlení vykreslování velkých výkresů můžete také nastavit `rasterizationOptions.BackgroundColor` na plnou barvu nebo povolit `rasterizationOptions.DrawType` pro rychlejší konverzi vektorů.

### Krok 4: Vytvořte PNG možnosti pro výsledný obrázek  
Zabalte nastavení rasterizace do objektu `PngOptions`, který říká Aspose.CAD, aby výstup byl PNG soubor.

```csharp
// Create an instance of PngOptions for the resultant image
ImageOptionsBase options = new Aspose.CAD.ImageOptions.PngOptions();
// Set rasterization options
options.VectorRasterizationOptions = rasterizationOptions;
```

### Krok 5: Uložte výsledný PNG  
Spojte cestu ke složce s požadovaným názvem souboru a zapište rasterizovaný obrázek na disk. Tento krok **uloží CAD jako PNG**.

```csharp
MyDir = MyDir + "conic_pyramid_raster_image_out.png";
// Save resultant image
image.Save(MyDir, options);
```

### Krok 6: Zobrazte zprávu o úspěchu  
Potvrďte, že převod proběhl úspěšně, a ukažte, kde byl soubor uložen.

```csharp
//ExEnd:ConvertDrawingToRasterImage            
Console.WriteLine("\nCAD drawing converted successfully to raster image format.\nFile saved at " + MyDir);
```

> **Poznámka:** `using` blok z Kroku 2 automaticky uvolní objekt `Image`, čímž zajistí uvolnění všech prostředků.

## Časté problémy a řešení

| Problém | Příčina | Řešení |
|-------|-------|-----|
| **Prázdný PNG výstup** | Možnosti rasterizace nejsou nastaveny (např. chybí `PageWidth`/`PageHeight`). | Ujistěte se, že `CadRasterizationOptions` definuje nenulovou velikost plátna. |
| **Nesprávné barvy** | Barva pozadí je ve výchozím nastavení bílá; zdrojový výkres používá průhledné vrstvy. | Nastavte `rasterizationOptions.BackgroundColor = Color.Transparent;` |
| **Zpomalení při velkých DWG souborech** | Vysoké rozlišení bez dělení na dlaždice. | Použijte `rasterizationOptions.LayoutOptions` k omezení vykreslované oblasti nebo snižte DPI. |
| **Výjimka licence** | Spuštění bez platné licence v produkci. | Aplikujte licenci pomocí `License license = new License(); license.SetLicense("Aspose.CAD.lic");` před načtením obrázku. |

## Často kladené otázky

### Q1: Je Aspose.CAD kompatibilní se všemi CAD formáty?
**A1:** Aspose.CAD podporuje širokou škálu CAD formátů, včetně DWG, DXF, DGN a dalších. Kompletní seznam najdete v [dokumentaci](https://reference.aspose.com/cad/net/).

### Q2: Mohu přizpůsobit možnosti rasterizace pro různé projekty?
**A2:** Ano, Aspose.CAD umožňuje rozsáhlé přizpůsobení možností rasterizace, což vývojářům umožňuje přizpůsobit výstup podle požadavků projektu.

### Q3: Je k dispozici bezplatná zkušební verze Aspose.CAD?
**A3:** Ano, můžete si vyzkoušet funkce Aspose.CAD pomocí bezplatné zkušební verze. Navštivte [zde](https://releases.aspose.com/) a začněte.

### Q4: Jak mohu získat podporu pro Aspose.CAD?
**A4:** Pro jakoukoli pomoc nebo dotazy navštivte Aspose.CAD [support forum](https://forum.aspose.com/c/cad/19).

### Q5: Jsou k dispozici dočasné licence pro Aspose.CAD?
**A5:** Ano, vývojáři mohou získat dočasné licence pro Aspose.CAD na [této stránce](https://purchase.aspose.com/temporary-license/).

### Q6: Mohu použít tuto metodu také k **převodu DWG na PNG**?
**A6:** Rozhodně. Stejný kód funguje i pro DWG soubory; stačí změnit příponu zdrojového souboru na `.dwg`.

### Q7: Jak **exportovat DXF do obrázku** s průhledným pozadím?
**A7:** Nastavte `rasterizationOptions.BackgroundColor = Color.Transparent;` před uložením PNG.

**Poslední aktualizace:** 2026-03-19  
**Testováno s:** Aspose.CAD 24.11 pro .NET (nejnovější verze)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}