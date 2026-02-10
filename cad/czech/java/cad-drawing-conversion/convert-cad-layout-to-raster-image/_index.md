---
date: 2025-12-18
description: Naučte se, jak převést DWG na PNG a další rastrové formáty obrázků pomocí
  Aspose.CAD pro Javu. Exportujte CAD jako PNG s vysoce kvalitními výsledky.
linktitle: Convert CAD Layout to Raster Image Format
second_title: Aspose.CAD Java API
title: Převod DWG na PNG a další rastrové formáty pomocí Aspose.CAD pro Javu
url: /cs/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Převod DWG na PNG a další rastrové formáty pomocí Aspose.CAD pro Java

## Úvod

Převod DWG na PNG (nebo jiné rastrové formáty obrázků) je běžná potřeba, když potřebujete sdílet CAD výkresy s kolegy, kteří nemají CAD prohlížeč, vložit návrhy do dokumentace nebo vytvořit miniatury pro webové galerie. Aspose.CAD pro Java usnadňuje tento převod, ať už pracujete s kompletním souborem výkresu nebo jen s konkrétním rozvržením. V tomto tutoriálu projdeme přesné kroky k **převodu CAD rozvržení na rastrový obrázek** – stejnou technikou můžete vytvořit výstupy PNG, JPEG, TIFF nebo PDF.

## Rychlé odpovědi
- **Jaká knihovna zpracovává DWG na PNG?** Aspose.CAD for Java  
- **Jaké formáty lze exportovat?** PNG, JPEG, TIFF, PDF, BMP a další  
- **Potřebuji licenci pro testování?** Bezplatná zkušební verze funguje pro vývoj; licence je vyžadována pro produkci  
- **Mohu vybrat konkrétní rozvržení?** Ano, použijte `setLayouts` k cílení na „Model“, „Layout1“ atd.  
- **Je možné získat výstup ve vysokém rozlišení?** Rozhodně – upravte `setPageWidth` a `setPageHeight` pro kontrolu DPI  

## Co je „convert dwg to png“?

Fráze „convert dwg to png“ popisuje proces převodu vektorového souboru DWG (nativního formátu pro mnoho CAD aplikací) na rastrový obrázek PNG založený na pixelech. Rasterové obrázky jsou ideální pro webové zobrazení, sdílení e-mailem a integraci do softwaru, který není CAD.

## Proč exportovat CAD jako PNG (nebo jiné rastrové formáty)?

- **Univerzální kompatibilita:** PNG a JPEG jsou podporovány prakticky každým prohlížečem obrázků a webovým prohlížečem.  
- **Rychlé načítání:** Rasterové obrázky se načítají okamžitě na rozdíl od otevírání těžkého souboru DWG.  
- **Snadné vkládání:** Vkládejte PNG přímo do Wordu, PowerPointu nebo HTML bez dalších pluginů.  
- **Konzistentní vzhled:** Ovládáte rozlišení, pozadí a rozvržení, což zajišťuje, že všichni zainteresovaní vidí stejný vizuál.  

## Předpoklady

Před zahájením se ujistěte, že máte:

1. **Java vývojové prostředí** – nainstalovaný a nakonfigurovaný JDK 8 nebo novější.  
2. **Aspose.CAD for Java** – Stáhněte nejnovější JAR z [dokumentace Aspose.CAD for Java](https://reference.aspose.com/cad/java/).  

## Import jmenných prostorů

Nejprve importujte třídy, které budete potřebovat. Tyto importy vám poskytují přístup k načítání obrázků, možnostem rasterizace a nastavením výstupu TIFF/PNG.

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

> **Tip:** Pokud plánujete exportovat do PNG místo TIFF, nahraďte `TiffOptions` za `PngOptions` (nachází se v `com.aspose.cad.imageoptions.PngOptions`).  

## Průvodce krok za krokem

### Krok 1: Nastavte adresář zdrojů

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";
```

Nahraďte `"Your Document Directory"` absolutní cestou, kde se nacházejí vaše CAD soubory.

### Krok 2: Načtěte CAD soubor

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

Můžete načíst libovolný podporovaný formát (DWG, DXF, DGN atd.). Toto je část **jak převést CAD** – jednoduše ukazujte na soubor a nechte Aspose provést parsování.

### Krok 3: Nakonfigurujte možnosti rasterizace

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
rasterizationOptions.setLayouts(new String[] {"Model", "Layout1"});
```

- `setPageWidth` / `setPageHeight` řídí výstupní rozlišení (větší hodnoty = vyšší DPI).  
- `setLayouts` vám umožní **převést CAD na raster** pro konkrétní rozvržení; vynechejte jej, pokud chcete rasterizovat celý výkres.

### Krok 4: Nastavte možnosti obrázku

```java
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.setVectorRasterizationOptions(rasterizationOptions);
```

Pokud dáváte přednost PNG, vytvořte instanci `PngOptions` místo `TiffOptions`. Zde **exportujete CAD jako PNG**.

### Krok 5: Uložte výsledný obrázek

```java
image.save(dataDir + "conic_pyramid_layoutstorasterimage_out_.tiff", options);
```

Změňte příponu souboru na `.png` (a objekt možností na `PngOptions`), abyste **uložili CAD jako JPEG/PNG**.

> **Častý problém:** Zapomenutí sladit příponu souboru s třídou možností způsobí `UnsupportedFormatException`. Vždy je udržujte synchronizované.  

## Časté problémy a řešení

| Problém | Řešení |
|-------|----------|
| **Prázdný výstupní obrázek** | Ověřte, že názvy rozvržení v `setLayouts` přesně odpovídají těm ve zdrojovém CAD souboru. |
| **PNG s nízkým rozlišením** | Zvyšte `setPageWidth` / `setPageHeight` nebo nastavte `setResolution` v možnostech rasterizace. |
| **Nesprávná verze DWG** | Ujistěte se, že používáte nejnovější verzi Aspose.CAD; starší verze nemusí podporovat novější verze DWG. |
| **Chyby paměti u velkých souborů** | Zpracovávejte stránky po jedné nebo zvyšte haldu JVM (`-Xmx2g`). |

## Často kladené otázky

**Q: Je Aspose.CAD kompatibilní s různými formáty CAD souborů?**  
A: Ano, podporuje DWG, DXF, DGN a mnoho dalších.

**Q: Mohu přizpůsobit rozlišení výstupního rastrového obrázku?**  
A: Rozhodně. Upravit `setPageWidth`, `setPageHeight` nebo `setResolution` v `CadRasterizationOptions`.

**Q: Jak mohu převést více CAD rozvržení v jednom běhu?**  
A: Poskytněte pole se všemi názvy rozvržení do `setLayouts`, např. `new String[]{"Model","Layout1","Layout2"}`.

**Q: Existují výstupní formáty kromě TIFF?**  
A: Ano – PNG, JPEG, BMP, PDF a další jsou k dispozici prostřednictvím jejich odpovídajících tříd `*Options`.

**Q: Kde mohu získat pomoc nebo sdílet své zkušenosti s Aspose.CAD?**  
A: Navštivte [Aspose.CAD fórum](https://forum.aspose.com/c/cad/19) pro podporu komunity a oficiální asistenci.

## Závěr

Po provedení těchto kroků můžete **převést DWG na PNG**, **exportovat CAD jako PNG**, **uložit CAD jako JPEG** nebo vygenerovat jakýkoli jiný rastrový formát, který potřebujete. Aspose.CAD pro Java zvládne těžkou práci, takže se můžete soustředit na integraci vysoce kvalitních obrázků do vašich aplikací, dokumentace nebo webových portálů.

---

**Poslední aktualizace:** 2025-12-18  
**Testováno s:** Aspose.CAD for Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}