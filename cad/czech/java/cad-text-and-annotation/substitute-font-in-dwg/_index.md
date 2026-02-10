---
date: 2025-12-28
description: Naučte se, jak načíst DWG soubor v Java projektech a nastavit primární
  název písma pomocí Aspose.CAD pro Java. Krok za krokem průvodce pro dokonalé CAD
  vizuály.
linktitle: Substitute Font in DWG
second_title: Aspose.CAD Java API
title: Jak načíst DWG soubor v Javě a nahradit písmo pomocí Aspose.CAD
url: /cs/java/cad-text-and-annotation/substitute-font-in-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak načíst DWG soubor v Javě a nahradit písmo pomocí Aspose.CAD

## Úvod

Pokud potřebujete **load DWG file Java** aplikace a dát svým výkresům profesionální vzhled, nahrazení písma je rychlé řešení. S Aspose.CAD pro Javu můžete nahradit výchozí styl textu libovolným systémově nainstalovaným písmem, což zajistí, že každá anotace se zobrazí přesně tak, jak očekáváte. V tomto tutoriálu vás provedeme celým procesem – od načtení DWG souboru v Javě až po použití metody `setPrimaryFontName` k změně písma.

## Rychlé odpovědi
- **Jaká knihovna potřebuji?** Aspose.CAD for Java.
- **Mohu načíst DWG soubor v Javě?** Ano, stačí zavolat `Image.load()` na cestu k DWG.
- **Která metoda mění písmo?** `setPrimaryFontName`.
- **Potřebuji licenci pro produkci?** Ano, je vyžadována komerční licence.
- **Je možný hromadný processing?** Rozhodně – můžete projít více souborů stejným kódem.

## Co je “load dwg file java”?

Načtení DWG souboru v prostředí Java znamená přečtení binárních CAD dat do objektu `Image`, který může Aspose.CAD manipulovat. Jakmile je soubor načten, máte plný programový přístup k vrstvám, stylům a textovým entitám.

## Proč nahrazovat písma v DWG souboru?

- **Konzistence:** Zajišťuje, že všichni spolupracovníci vidí stejný typ písma, bez ohledu na jejich lokální nastavení fontů.  
- **Čitelnost:** Některá výchozí CAD písma jsou na obrazovkách těžko čitelná; výměna za čisté písmo jako Arial zlepšuje přehlednost.  
- **Branding:** Zarovnává technické výkresy s firemními stylovými průvodci.

## Předpoklady

- **Java Development Kit (JDK)** – jakákoli recentní verze (doporučeno 8+).  
- **Aspose.CAD for Java** – stáhněte z [website](https://releases.aspose.com/cad/java/).  
- **Sample DWG file** – výkres, který chcete upravit (pro testování můžete použít libovolný DWG nebo DXF soubor).

## Import Namespaces

Ve vašem Java projektu importujte potřebné třídy pro práci s Aspose.CAD. Tyto importy vám umožní načítání obrázků, CAD‑specifické objekty a manipulaci se styly.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject;
```

## Postupný návod na nahrazení písma

### Krok 1: Načtěte svůj DWG soubor (load dwg file java)

Nejprve nasměrujte API na umístění vašeho DWG (nebo DXF) souboru a načtěte jej do objektu `CadImage`.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage) Image.load(srcFile);
```

> **Pro tip:** Pokud pracujete přímo s DWG soubory, nahraďte příponu `.dxf` příponou `.dwg` ve variable `srcFile`.

### Krok 2: Projděte tabulku stylů a nastavte primární název písma

Každý CAD výkres obsahuje kolekci objektů stylu. Projděte je a použijte metodu `setPrimaryFontName` (API volání, které **sets primary font name**) k nahrazení písma.

```java
for(Object style : cadImage.getStyles())
{
    // Set the font name
    ((com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject)style).setPrimaryFontName("Arial");
}
```

Můžete změnit `"Arial"` na libovolné písmo, které je nainstalováno na počítači, kde kód běží.

### Krok 3: Uložte upravený výkres

Po aktualizaci písma zapište změny zpět do nového DWG souboru (nebo přepište originál).

```java
cadImage.save(dataDir + "output.dwg", new DwgOptions());
```

Uložený soubor nyní používá písmo, které jste specifikovali, a jakákoli textová anotace bude vykreslena s tímto typem písma.

## Časté problémy a řešení

| Problém | Řešení |
|-------|----------|
| **Font not applied** | Ověřte, že je písmo nainstalováno v hostitelském OS a že název je napsán přesně. |
| **`Image.load` throws an exception** | Zkontrolujte, že je cesta k souboru správná a že soubor je podporovaného formátu DWG/DXF. |
| **Performance slowdown on large files** | Zpracovávejte soubory v samostatném vlákně nebo je batchujte, aby nedošlo k blokování UI. |

## Často kladené otázky

**Q: Ovlivňuje metoda `setPrimaryFontName` pouze textové entity?**  
A: Aktualizuje primární písmo pro tabulku stylů, což následně ovlivňuje všechny textové objekty, které odkazují na tento styl.

**Q: Mohu použít vlastní písmo, které není nainstalováno v systému?**  
A: Aspose.CAD se spoléhá na registr písma operačního systému. Pro použití vlastního písma jej nainstalujte na počítači, kde kód běží.

**Q: Je možné změnit písmo jen pro jednu vrstvu?**  
A: Ano, můžete před voláním `setPrimaryFontName` filtrovat styly podle názvu vrstvy.

**Q: Jaká verze Aspose.CAD je vyžadována pro soubory DWG 2022?**  
A: Nejnovější vydání (k roku 2025) plně podporuje DWG 2022. Vždy zkontrolujte poznámky k vydání pro konkrétní podporu formátů.

**Q: Jak řešit licencování v vývojovém prostředí?**  
A: Použijte dočasnou evaluační licenci pro testování. Pro produkci vložte zakoupený licenční soubor pomocí `License.setLicense("Aspose.Total.Java.lic");`.

---

**Last Updated:** 2025-12-28  
**Tested With:** Aspose.CAD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}