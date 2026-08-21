---
date: 2026-05-04
description: Naučte se, jak převést dxf na dwg a nastavit primární font v Javě pomocí
  Aspose.CAD. Krok za krokem průvodce pro dokonalé CAD vizualizace.
keywords:
- convert dxf to dwg
- set primary font
- change dwg text style
- how to substitute font
- aspose cad licensing
linktitle: Nahradit písmo v DWG
second_title: Aspose.CAD Java API
title: Převod dxf na dwg a změna písma v DWG pomocí Aspose.CAD Java
url: /cs/java/cad-text-and-annotation/substitute-font-in-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak načíst DWG soubor v Javě a nahradit písmo pomocí Aspose.CAD

## Úvod

Pokud potřebujete **convert dxf to dwg** v Java aplikacích a chcete svým výkresům dodat profesionální vzhled, nahrazení písma je rychlé řešení. S Aspose.CAD pro Java můžete nahradit výchozí styl textu libovolným systémově nainstalovaným písmem, čímž zajistíte, že každá anotace bude vypadat přesně tak, jak očekáváte. V tomto tutoriálu projdeme celý proces – od načtení DWG souboru v Javě až po použití metody `setPrimaryFontName` k změně písma.

## Rychlé odpovědi
- **Jaká knihovna potřebuji?** Aspose.CAD for Java.  
- **Mohu načíst DWG soubor v Javě?** Ano, jednoduše zavolejte `Image.load()` na cestu k DWG.  
- **Která metoda mění písmo?** `setPrimaryFontName`.  
- **Potřebuji licenci pro produkci?** Ano, je vyžadována komerční licence.  
- **Je možný hromadný processing?** Absolutně – projděte více souborů stejným kódem.

## Co je **convert dxf to dwg**?

„Convert dxf to dwg“ označuje převod souboru DXF (Drawing Exchange Format) do nativního formátu DWG, který používá mnoho CAD aplikací. Převod vám umožní vzít široce podporovaný DXF výkres, začlenit jej do DWG workflow a následně aplikovat pokročilé stylování – například nahrazení písma – pomocí Aspose.CAD.

## Proč nahradit písma v DWG souboru?

- **Konzistence:** Zaručuje, že všichni spolupracovníci uvidí stejný typ písma, bez ohledu na jejich lokální nastavení fontů.  
- **Čitelnost:** Některá výchozí CAD písma jsou na obrazovce těžko čitelná; výměna za čisté písmo jako Arial zvyšuje přehlednost.  
- **Branding:** Zarovnává technické výkresy s firemními stylovými směrnicemi.  

## Běžné případy použití

| Scénář | Proč je to důležité |
|----------|----------------|
| **Hromadná konverze starých DXF výkresů** | Můžete je převést na DWG a v jednom kroku vynutit firemní písmo. |
| **Příprava výkresů pro prezentace klientům** | Konzistentní, čitelná písma dodávají dokumentům profesionální vzhled. |
| **Automatizované CAD pipeline** | Vložení nahrazení písma eliminuje manuální kroky po zpracování. |

## Požadavky

- **Java Development Kit (JDK)** – libovolná aktuální verze (doporučeno 8+).  
- **Aspose.CAD for Java** – stáhněte z [website](https://releases.aspose.com/cad/java/).  
- **Ukázkový DWG/DXF soubor** – výkres, který chcete upravit (pro testování můžete použít libovolný DWG nebo DXF soubor).

## Importovat jmenné prostory

Ve vašem Java projektu importujte potřebné třídy pro práci s Aspose.CAD. Tyto importy vám umožní načíst obrázek, pracovat s CAD‑specifickými objekty a manipulovat se styly.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject;
```

## Postupný průvodce nahrazením písma

### Krok 1: Načtěte svůj DWG soubor (load dwg file java)

Nejprve nasměrujte API na umístění vašeho DWG (nebo DXF) souboru a načtěte jej do objektu `CadImage`.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage) Image.load(srcFile);
```

> **Pro tip:** Pokud pracujete přímo s DWG soubory, nahraďte příponu `.dxf` příponou `.dwg` v proměnné `srcFile`.

### Krok 2: Procházejte tabulku stylů a nastavte primární název písma

Každý CAD výkres obsahuje kolekci objektů stylu. Projděte je a použijte metodu `setPrimaryFontName` (API volání, které **nastavuje primární název písma**) k nahrazení písma.

```java
for(Object style : cadImage.getStyles())
{
    // Set the font name
    ((com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject)style).setPrimaryFontName("Arial");
}
```

Můžete změnit `"Arial"` na jakékoli písmo, které je nainstalováno na počítači, na kterém kód běží.

### Krok 3: Uložte upravený výkres

Po aktualizaci písma zapište změny do nového DWG souboru (nebo přepište původní).

```java
cadImage.save(dataDir + "output.dwg", new DwgOptions());
```

Uložený soubor nyní používá písmo, které jste zadali, a jakákoli textová anotace bude vykreslena s tímto typem písma.

## Běžné problémy a řešení

| Problém | Řešení |
|-------|----------|
| **Písmo se neaplikovalo** | Ověřte, že je písmo nainstalováno v hostitelském OS a že název je napsán přesně. |
| **`Image.load` vyvolá výjimku** | Zkontrolujte, že cesta k souboru je správná a že soubor je podporovaného formátu DWG/DXF. |
| **Zpomalení výkonu u velkých souborů** | Zpracovávejte soubory v samostatném vlákně nebo je batchujte, aby nedošlo k blokování UI. |

## Často kladené otázky

**Q: Ovlivňuje metoda `setPrimaryFontName` pouze textové entity?**  
A: Aktualizuje primární písmo pro tabulku stylů, což následně ovlivňuje všechny textové objekty, které odkazují na tento styl.

**Q: Mohu použít vlastní písmo, které není nainstalováno v systému?**  
A: Aspose.CAD se spoléhá na registr písma operačního systému. Pro použití vlastního písma jej nainstalujte na počítač, kde kód běží.

**Q: Je možné změnit písmo pouze pro jednu vrstvu?**  
A: Ano, můžete před voláním `setPrimaryFontName` filtrovat styly podle názvu vrstvy.

**Q: Jaká verze Aspose.CAD je vyžadována pro soubory DWG 2022?**  
A: Nejnovější vydání (k roku 2025) plně podporuje DWG 2022. Vždy zkontrolujte poznámky k vydání pro konkrétní podporu formátů.

**Q: Jak řešit licencování ve vývojovém prostředí?**  
A: Použijte dočasnou evaluační licenci pro testování. Pro produkci vložte zakoupený licenční soubor pomocí `License.setLicense("Aspose.Total.Java.lic");`.

**Poslední aktualizace:** 2026-05-04  
**Testováno s:** Aspose.CAD for Java 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}