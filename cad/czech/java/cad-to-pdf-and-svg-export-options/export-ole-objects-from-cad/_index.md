---
date: 2026-03-02
description: Odemkněte potenciál Aspose.CAD pro Javu. Snadno exportujte OLE objekty
  a **uložte CAD jako PNG**. Stáhněte si nyní pro bezproblémovou správu CAD dat.
linktitle: Export OLE Objects from CAD
second_title: Aspose.CAD Java API
title: Uložit CAD jako PNG – Export OLE objektů pomocí Aspose.CAD pro Javu
url: /cs/java/cad-to-pdf-and-svg-export-options/export-ole-objects-from-cad/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Uložení CAD jako PNG – Export OLE objektů pomocí Aspose.CAD pro Java

## Úvod

Ve světě počítačově podporovaného návrhu (CAD) je efektivní správa a extrakce OLE (Object Linking and Embedding) objektů – a možnost **uložit CAD jako PNG** – klíčová pro následné pracovní postupy, jako jsou reportování, webové náhledy nebo archivace. Aspose.CAD pro Java poskytuje výkonné řešení založené na kódu, které umožňuje jak exportovat OLE objekty, tak převádět CAD výkresy na vysoce kvalitní PNG obrázky během několika řádků kódu.

## Rychlé odpovědi
- **Co dělá Aspose.CAD?** Čte, manipuluje a konvertuje CAD soubory (DWG, DXF, DGN atd.) bez potřeby nativního CAD softwaru.  
- **Mohu uložit CAD jako PNG?** Ano – použijte `PngOptions` spolu s `CadRasterizationOptions` pro rasterizaci libovolného rozvržení.  
- **Jak exportovat OLE objekty?** Načtěte CAD soubor pomocí `Image.load` a uložte každé rozvržení obsahující OLE jako PNG.  
- **Potřebuji licenci?** K dispozici je bezplatná zkušební verze; komerční licence odstraňuje omezení hodnocení.  
- **Jaká verze Javy je požadována?** Java 8 nebo vyšší je plně podporována.

## Co je **uložení CAD jako PNG**?
Uložení CAD jako PNG znamená rasterizaci vektorových CAD výkresů do pixelového PNG obrázku. Tento převod je užitečný, když potřebujete lehký, univerzálně zobrazitelný formát pro webové stránky, mobilní aplikace nebo dokumentaci.

## Proč použít Aspose.CAD pro Java k **převodu CAD na PNG**?
- **Není potřeba instalace CAD** – knihovna funguje zcela v Javě.  
- **Zachovává věrnost rozvržení** – můžete vybrat konkrétní rozvržení, nastavit DPI a zachovat kvalitu čar.  
- **Dávkové zpracování** – iterujte přes více souborů pomocí jednoduché smyčky.  
- **Export OLE objektů** – OLE obsah vložený v DWG/DXF souborech je automaticky vykreslen do PNG výstupu.

## Požadavky

Předtím, než se pustíte do tutoriálu, ujistěte se, že máte splněny následující požadavky:

- **Java prostředí** – ujistěte se, že máte nastavené vývojové prostředí Javy na svém počítači.  
- **Aspose.CAD pro Java** – stáhněte a nainstalujte knihovnu Aspose.CAD pro Java. Knihovnu najdete na [download link](https://releases.aspose.com/cad/java/).  
- **CAD soubory** – připravte CAD soubory obsahující OLE objekty, které chcete exportovat.

## Importování jmenných prostorů

Pro začátek importujte potřebné jmenné prostory do svého Java projektu. Tyto jmenné prostory poskytují základní třídy a funkce potřebné pro práci s CAD soubory pomocí Aspose.CAD.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Nyní si rozložíme proces exportu OLE objektů z CAD do několika kroků:

## Jak **uložit CAD jako PNG** a exportovat OLE objekty

### Krok 1: Nastavte adresář dokumentů

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

Nezapomeňte nahradit `"Your Document Directory"` cestou k adresáři, který obsahuje vaše CAD soubory.

### Krok 2: Definujte názvy CAD souborů

```java
String[] files = new String[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

Zadejte názvy CAD souborů, které chcete zpracovat, v poli `files`.

### Krok 3: Nastavte možnosti exportu PNG

```java
PngOptions pngOptions = new PngOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.setLayouts(new String[] { "Layout1" });
```

Konfigurujte možnosti exportu PNG, včetně rasterizace vektorů a nastavení rozvržení. Tyto možnosti vám umožní **převést CAD na PNG** s požadovanou kvalitou.

### Krok 4: Procházejte CAD soubory

```java
for(String file : files)
{
    CadImage cadImage = (CadImage)Image.load(dataDir + file);
    cadImage.save(dataDir + file + "_out.png", pngOptions);
}
```

Procházejte každý určený CAD soubor, načtěte jej pomocí Aspose.CAD a uložte OLE objekty jako PNG obrázky. Tato smyčka ukazuje jednoduchý způsob, jak **převést DWG na PNG** hromadně.

## Časté problémy a řešení

| Problém | Příčina | Řešení |
|-------|-------|----------|
| **Prázdný PNG výstup** | Neshoda názvu rozvržení | Ověřte, že název rozvržení (`"Layout1"`) existuje ve zdrojovém DWG. |
| **Chybějící OLE grafika** | OLE objekty jsou uloženy v jiném rozvržení | Zahrňte všechna relevantní rozvržení do `rasterizationOptions.setLayouts(...)`. |
| **Chyba nedostatku paměti u velkých souborů** | Vysoké nastavení DPI | Snižte DPI pomocí `rasterizationOptions.setResolution(...)` nebo zpracovávejte soubory po jednom. |

## Často kladené otázky

**Q: Je Aspose.CAD kompatibilní se všemi formáty CAD souborů?**  
A: Aspose.CAD podporuje různé CAD formáty, včetně DWG, DXF a DGN. Kompletní seznam najdete v [documentation](https://reference.aspose.com/cad/java/).

**Q: Mohu přizpůsobit nastavení exportu pro OLE objekty?**  
A: Ano, Aspose.CAD poskytuje rozsáhlé možnosti pro přizpůsobení nastavení exportu, což vám umožní přizpůsobit výstup vašim konkrétním požadavkům.

**Q: Je k dispozici bezplatná zkušební verze Aspose.CAD?**  
A: Ano, možnosti Aspose.CAD můžete vyzkoušet získáním bezplatné zkušební verze [here](https://releases.aspose.com/).

**Q: Kde mohu získat komunitní podporu pro Aspose.CAD?**  
A: Připojte se ke komunitě Aspose.CAD na [forum](https://forum.aspose.com/c/cad/19), kde můžete požádat o pomoc a sdílet své zkušenosti.

**Q: Jak si mohu zakoupit licenci pro Aspose.CAD?**  
A: Navštivte [purchase page](https://purchase.aspose.com/buy) a pořiďte si licenci, která vyhovuje vašim vývojářským potřebám.

## Závěr

S těmito jednoduchými, ale výkonnými kroky můžete bez problémů **uložit CAD jako PNG** a zároveň exportovat OLE objekty z CAD souborů pomocí Aspose.CAD pro Java. Tento univerzální nástroj umožňuje vývojářům efektivně spravovat CAD data a otevírá nové možnosti v CAD vývoji aplikací a následných pracovních postupech založených na obrázcích.

---

**Last Updated:** 2026-03-02  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}