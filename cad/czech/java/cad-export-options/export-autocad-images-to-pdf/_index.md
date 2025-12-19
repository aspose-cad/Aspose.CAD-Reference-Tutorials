---
date: 2025-12-19
description: Naučte se, jak exportovat PDF z AutoCADu pomocí Aspose.CAD pro Javu.
  Tento krok‑za‑krokem průvodce vám ukáže, jak převést DWG na PDF, uložit CAD jako
  PDF a řešit licencování.
linktitle: Export AutoCAD Images to PDF
second_title: Aspose.CAD Java API
title: Export AutoCAD PDF – Export obrázků AutoCAD do PDF pomocí tutoriálu Aspose.CAD
  pro Java
url: /cs/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export AutoCAD PDF - Export AutoCAD obrázků do PDF pomocí Aspose.CAD pro Java

## Úvod

Hledáte způsob, jak snadno **exportovat AutoCAD PDF** pomocí Javy? Už nehledejte dál! V tomto tutoriálu vás provedeme převodem AutoCAD obrázků do PDF pomocí Aspose.CAD pro Java, výkonné knihovny, která proces **převodu DWG do PDF** usnadňuje. Na konci pochopíte, jak **uložit CAD jako PDF**, aplikovat vlastní nastavení rasterizace a pracovat s licencí Aspose.CAD pro produkční použití.

## Rychlé odpovědi
- **Mohu převést DWG do PDF pomocí Javy?** Ano, Aspose.CAD pro Java pracuje s DWG, DXF a mnoha dalšími formáty.  
- **Potřebuji licenci?** **Aspose CAD licence** je vyžadována pro neomezené použití; dočasná licence je k dispozici pro vyhodnocení.  
- **Jaká verze Javy je podporována?** Java 8+ (knihovna je kompatibilní se všemi moderními JDK).  
- **Mohu přizpůsobit velikost stránky PDF?** Rozhodně – upravte `pageWidth` a `pageHeight` v nastavení rasterizace.  
- **Je možná 3‑D rasterizace?** Ano, povolte `TypeOfEntities.Entities3D` pro plné 3‑D vykreslení.

## Co je **export autocad pdf**?
Exportování AutoCAD PDF znamená převod vektorových CAD výkresů (DWG, DXF, DWF atd.) do přenosného PDF dokumentu při zachování vrstev, tlouštěk čar a volitelně 3‑D geometrie. To je užitečné pro sdílení návrhů s klienty, archivaci nebo tisk bez potřeby CAD softwaru.

## Proč použít Aspose.CAD pro Java k **export autocad pdf**?
- **Kompletní podpora formátů** – funguje s DWG, DXF, DWF a mnoha dalšími.  
- **Žádné externí závislosti** – čistá Java knihovna, bez nativních DLL.  
- **Vysoce kvalitní rasterizace** – kontrola DPI, velikosti stránky a rozvržení.  
- **Flexibilita licence** – začněte s bezplatnou zkušební verzí, poté přejděte na trvalou **Aspose CAD licenci**.  

## Požadavky

- **Java vývojové prostředí** – nainstalovaný JDK 8 nebo novější.  
- **Aspose.CAD pro Java knihovna** – stáhněte z [odkaz ke stažení](https://releases.aspose.com/cad/java/).  
- **Adresář dokumentů** – složka ve vašem počítači, kde budou umístěny zdrojové CAD soubory a generované PDF.

## Import jmenných prostorů

Ve vašem Java projektu importujte potřebné třídy pro práci s Aspose.CAD:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

## Průvodce krok za krokem

### Krok 1: Nastavte cestu ke zdrojovému adresáři

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **Tip:** Nahraďte `"Your Document Directory"` absolutní cestou ke složce, kterou jste vytvořili v požadavcích.

### Krok 2: Načtěte CAD obrázek

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **Proč je to důležité:** Načtení CAD souboru do objektu `Image` vám poskytuje plný přístup k rasterizačnímu enginu Aspose.CAD.

### Krok 3: Nastavte možnosti rasterizace

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- Upravte `pageWidth` a `pageHeight` pro změnu velikosti výstupního PDF.  
- Odkomentujte řádek `setTypeOfEntities`, pokud potřebujete **java convert cad pdf** pro 3‑D entity.  
- Volání `setLayouts` vybírá, které rozvržení (Model, Layout1 atd.) bude vykresleno.

### Krok 4: Nakonfigurujte PDF možnosti

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Tímto se propojí nastavení rasterizace s PDF výstupem, což zajistí správný převod vektorových dat.

### Krok 5: Uložte PDF

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

Výsledný soubor `Export3DImagestoPDF_out_.pdf` je **save cad as pdf** reprezentací vašeho původního AutoCAD výkresu.

## Časté problémy a řešení

| Příznak | Pravděpodobná příčina | Řešení |
|---------|-----------------------|--------|
| Prázdný PDF výstup | Nastavení rasterizace není nastaveno nebo nesoulad rozvržení | Ověřte, že `setLayouts` odpovídá názvu rozvržení ve vašem CAD souboru. |
| Obrázek s nízkým rozlišením | `pageWidth`/`pageHeight` jsou příliš malé | Zvyšte rozměry nebo nastavte vyšší DPI pomocí `rasterizationOptions.setResolution(...)`. |
| Výjimka licence | Nebyla použita platná licence | Použijte **Aspose CAD licenci** nebo použijte dočasnou licenci pro testování. |

## Často kladené otázky

### Q1: Mohu použít Aspose.CAD pro Java s jinými formáty CAD souborů?
A1: Ano, Aspose.CAD podporuje širokou škálu formátů včetně DWG, DWF, DGN a dalších, což vám poskytuje flexibilitu ve vašich projektech.

### Q2: Jak mohu získat dočasnou licenci pro Aspose.CAD pro Java?
A2: Navštivte [zde](https://purchase.aspose.com/temporary-license/) pro získání dočasné licence pro vyhodnocení.

### Q3: Existují možnosti rozvržení pro rasterizaci?
A3: Ano, můžete přizpůsobit rozvržení (např. `"Model"`, `"Layout1"`) pomocí metody `setLayouts`, abyste určili, který pohled bude vykreslen.

### Q4: Mohu přizpůsobit velikost výstupního PDF souboru?
A4: Rozhodně! Upravením parametrů `pageWidth` a `pageHeight` v možnostech rasterizace přizpůsobíte požadované rozměry.

### Q5: Kde mohu získat pomoc nebo diskutovat o problémech souvisejících s Aspose.CAD pro Java?
A5: Navštivte [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) pro specializovanou podporu a komunitní diskuse.

---

**Poslední aktualizace:** 2025-12-19  
**Testováno s:** Aspose.CAD pro Java 24.10  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}