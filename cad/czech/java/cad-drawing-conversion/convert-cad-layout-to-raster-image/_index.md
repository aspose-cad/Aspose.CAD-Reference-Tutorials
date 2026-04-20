---
date: 2026-02-17
description: Naučte se převádět DWG na PNG a exportovat CAD jako PNG nebo jiné rastrové
  formáty pomocí Aspose.CAD pro Javu. Získejte vysoce kvalitní výsledky rychle.
linktitle: Convert CAD Layout to Raster Image Format
second_title: Aspose.CAD Java API
title: Převod DWG na PNG a další rastrové formáty pomocí Aspose.CAD pro Java
url: /cs/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Převod DWG na PNG a další rastrové formáty pomocí Aspose.CAD pro Java

## Úvod

Převod DWG na PNG (nebo jiné rastrové formáty obrázků) je častý požadavek, když potřebujete sdílet CAD výkresy s kolegy, kteří nemají CAD prohlížeč, vložit návrhy do dokumentace nebo vygenerovat miniatury pro webové galerie. **V tomto průvodci se naučíte, jak rychle a spolehlivě převést dwg na png**, ať už pracujete s kompletním souborem výkresu nebo jen s konkrétním rozvržením. Můžete také potřebovat **převést CAD na raster** pro webové náhledy, reportovací nástroje nebo mobilní aplikace. Aspose.CAD pro Java tento převod usnadňuje a poskytuje plnou kontrolu nad rozlišením, výběrem rozvržení a výstupním formátem.

## Rychlé odpovědi
- **Jaká knihovna provádí DWG na PNG?** Aspose.CAD pro Java  
- **Jaké formáty lze exportovat?** PNG, JPEG, TIFF, PDF, BMP a další  
- **Potřebuji licenci pro testování?** Bezplatná zkušební verze funguje pro vývoj; licence je vyžadována pro produkci  
- **Mohu vybrat konkrétní rozvržení?** Ano, použijte `setLayouts` k cílení na “Model”, “Layout1” atd.  
- **Je možné získat výstup ve vysokém rozlišení?** Rozhodně – upravte `setPageWidth` a `setPageHeight` pro kontrolu DPI  

## Co znamená „convert dwg to png“?

Výraz „convert dwg to png“ popisuje proces převodu vektorového souboru DWG (nativního formátu mnoha CAD aplikací) na rastrový obrázek PNG. Rastrové obrázky jsou ideální pro webové zobrazení, sdílení e‑mailem a integraci do softwaru, který nepodporuje CAD.

## Proč exportovat CAD jako PNG (nebo jiné rastrové formáty)?

- **Univerzální kompatibilita:** PNG a JPEG jsou podporovány prakticky všemi prohlížeči a prohlížeči obrázků.  
- **Rychlé načítání:** Rastrové obrázky se načítají okamžitě na rozdíl od otevírání těžkého souboru DWG.  
- **Jednoduché vkládání:** Vložte PNG přímo do Wordu, PowerPointu nebo HTML bez dalších pluginů.  
- **Konzistentní vzhled:** Ovládáte rozlišení, pozadí a rozvržení, takže každý stakeholder vidí stejný vizuál.  

## Běžné scénáře použití

| Scénář | Proč pomáhá výstup v rastrovém formátu |
|----------|------------------------|
| **Projektová dokumentace** | Vkládání PNG do PDF nebo Word dokumentů eliminuje potřebu CAD softwaru pro recenzenty. |
| **Webové portály** | Miniatury generované ze souborů DWG se načítají okamžitě a zlepšují uživatelský zážitek. |
| **Mobilní aplikace** | Rastrové obrázky se zobrazují správně na zařízeních, která nemají CAD prohlížeč. |
| **Automatizované reportování** | Dávkový převod více rozvržení na PNG/JPEG pro zahrnutí do grafů nebo dashboardů. |

## Předpoklady

Než začnete, ujistěte se, že máte:

1. **Vývojové prostředí Java** – nainstalovaný a nastavený JDK 8 nebo novější.  
2. **Aspose.CAD pro Java** – stáhněte nejnovější JAR z [Aspose.CAD for Java documentation](https://reference.aspose.com/cad/java/).  

## Import Namespaces

Nejprve importujte třídy, které budete potřebovat. Tyto importy vám umožní načíst obrázek, nastavit možnosti rasterizace a nastavení výstupu TIFF/PNG.

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

> **Tip:** Pokud chcete **exportovat CAD jako PNG** místo TIFF, nahraďte `TiffOptions` za `PngOptions` (nachází se v `com.aspose.cad.imageoptions.PngOptions`).

## Průvodce krok za krokem

### Krok 1: Nastavení adresáře zdrojů

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";
```

Nahraďte `"Your Document Directory"` absolutní cestou, kde se nacházejí vaše CAD soubory.

### Krok 2: Načtení CAD souboru

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

Můžete načíst libovolný podporovaný formát (DWG, DXF, DGN atd.). Toto je část **jak převést cad** – jednoduše ukazujete na soubor a nechte Aspose provést parsování.

### Krok 3: Konfigurace možností rasterizace

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
rasterizationOptions.setLayouts(new String[] {"Model", "Layout1"});
```

- `setPageWidth` / `setPageHeight` řídí výstupní rozlišení (větší hodnoty = vyšší DPI).  
- `setLayouts` vám umožní **převést CAD na raster** pro konkrétní rozvržení; pokud jej vynecháte, rasterizuje se celý výkres.

### Krok 4: Nastavení možností obrázku

```java
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.setVectorRasterizationOptions(rasterizationOptions);
```

Pokud preferujete PNG, vytvořte instanci `PngOptions` místo `TiffOptions`. Zde se provádí **export CAD jako PNG**.

### Krok 5: Uložení výsledného obrázku

```java
image.save(dataDir + "conic_pyramid_layoutstorasterimage_out_.tiff", options);
```

Změňte příponu souboru na `.png` (a objekt možností na `PngOptions`), abyste **uložili CAD jako JPEG/PNG**.

> **Častý úskalí:** Zapomenutí sladit příponu souboru s třídou možností způsobí `UnsupportedFormatException`. Vždy je udržujte v souladu.

## Časté problémy a řešení

| Problém | Řešení |
|-------|----------|
| **Prázdný výstupní obrázek** | Ověřte, že názvy rozvržení v `setLayouts` přesně odpovídají těm ve zdrojovém CAD souboru. |
| **Nízké rozlišení PNG** | Zvyšte `setPageWidth` / `setPageHeight` nebo nastavte `setResolution` v možnostech rasterizace. |
| **Není podporována verze DWG** | Ujistěte se, že používáte nejnovější verzi Aspose.CAD; starší verze nemusí podporovat novější DWG vydání. |
| **Chyby paměti u velkých souborů** | Zpracovávejte stránky po jedné nebo zvýšte velikost haldy JVM (`-Xmx2g`). |

## Často kladené otázky

**Q: Je Aspose.CAD kompatibilní s různými CAD formáty?**  
A: Ano, podporuje DWG, DXF, DGN a mnoho dalších.

**Q: Mohu přizpůsobit rozlišení výstupního rastrového obrázku?**  
A: Rozhodně. Upravit `setPageWidth`, `setPageHeight` nebo `setResolution` v `CadRasterizationOptions`.

**Q: Jak mohu převést více CAD rozvržení v jednom běhu?**  
A: Poskytněte pole se všemi názvy rozvržení do `setLayouts`, např. `new String[]{"Model","Layout1","Layout2"}`.

**Q: Existují výstupní formáty kromě TIFF?**  
A: Ano – PNG, JPEG, BMP, PDF a další jsou k dispozici prostřednictvím jejich příslušných `*Options` tříd.

**Q: Kde mohu získat pomoc nebo sdílet své zkušenosti s Aspose.CAD?**  
A: Navštivte [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) pro komunitní podporu a oficiální asistenci.

## Závěr

Dodržením těchto kroků můžete **převést DWG na PNG**, **exportovat CAD jako PNG**, **uložit CAD jako JPEG** nebo vygenerovat jakýkoli jiný rastrový formát, který potřebujete. Aspose.CAD pro Java provádí těžkou část práce, takže se můžete soustředit na integraci vysoce kvalitních obrázků do vašich aplikací, dokumentace nebo webových portálů.

---

**Poslední aktualizace:** 2026-02-17  
**Testováno s:** Aspose.CAD pro Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}