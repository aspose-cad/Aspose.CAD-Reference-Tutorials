---
date: 2026-01-10
description: Naučte se, jak exportovat DGN do DWG a převést MicroStation DGN na AutoCAD
  DWG pomocí Aspose.CAD pro Javu. Průvodce krok za krokem.
linktitle: Export DGN as Part of DWG
second_title: Aspose.CAD Java API
title: Exportovat DGN do DWG pomocí Aspose.CAD pro Java
url: /cs/java/dgn-export-options/export-dgn-as-part-of-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export DGN do DWG pomocí Aspose.CAD pro Java

## Úvod

V tomto tutoriálu se naučíte, jak **exportovat dgn do dwg** a vložit návrh MicroStation DGN do souboru AutoCAD DWG pomocí knihovny Aspose.CAD pro Java. Ať už migrujete staré výkresy MicroStation nebo potřebujete kombinovat DGN podklady s DWG rozvrženími, tento průvodce vás provede každým krokem – od nastavení prostředí až po vytvoření PDF náhledu finálního DWG.

## Rychlé odpovědi
- **Co dosahuje „export dgn do dwg“?** Vkládá DGN podklad do DWG, což umožňuje plynulé prohlížení v AutoCADu.
- **Do jakého formátu mohu výsledek exportovat pro rychlý náhled?** Můžete **exportovat CAD soubor do PDF** pomocí `PdfOptions`.
- **Potřebuji licenci pro spuštění kódu?** Pro produkční použití je vyžadována dočasná nebo placená licence Aspose.CAD.
- **Jaká verze Javy je podporována?** Java 8 nebo novější funguje s nejnovějším vydáním Aspose.CAD pro Java.
- **Je k dispozici bezplatná zkušební verze?** Ano – stáhněte si zkušební verzi z webu Aspose.

## Co je „export dgn do dwg“?
Exportování DGN do DWG znamená převod nebo vložení návrhu MicroStation DGN jako podkladu do výkresu AutoCAD DWG. To umožňuje CAD profesionálům využít existující DGN aktiva, aniž by museli znovu vytvářet geometrii od začátku.

## Proč převádět MicroStation DGN na AutoCAD DWG?
- **Spolupráce:** Týmy používající AutoCAD mohou přímo prohlížet a upravovat obsah DGN.
- **Standardizace:** DWG je de‑facto formát pro mnoho následných pracovních postupů (např. generování PDF, 3D renderování).
- **Zachování:** Udržuje původní odkazy DGN nedotčené, čímž snižuje ztrátu dat.

## Předpoklady

Než se pustíme do tutoriálu, ujistěte se, že máte následující předpoklady připravené:
1. **Knihovna Aspose.CAD:** Stáhněte a nainstalujte knihovnu Aspose.CAD pro Java. Knihovnu najdete [zde](https://releases.aspose.com/cad/java/).
2. **Java Development Kit (JDK):** Ujistěte se, že máte na systému nainstalovanou Javu.
3. **Integrované vývojové prostředí (IDE):** Vyberte si Java IDE, jako je Eclipse nebo IntelliJ, pro plynulejší vývoj.

## Import balíčků

Ve vašem Java projektu importujte potřebné balíčky Aspose.CAD, aby bylo možné manipulovat se soubory CAD. Zde je příklad:

```java
import com.aspose.cad;
import com.aspose.cad.imageoptions;
import com.aspose.cad.fileformats.cad.cadconsts;
import com.aspose.cad.fileformats.cad;
import com.aspose.cad.fileformats.cad.cadobjects;
```

## Krok 1: Nastavte cesty k souborům

Definujte vstupní a výstupní cesty k souborům pro DWG soubor. Aktualizujte proměnné `dataDir`, `fileName` a `outPath` podle potřeby.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
String outPath = dataDir + "BlockRefDgn.dwg.pdf";
```

## Krok 2: Vytvořte instanci PdfOptions

Vytvořte instanci třídy `PdfOptions`, protože **exportujeme CAD soubor do PDF** pro rychlé ověření.

```java
PdfOptions exportOptions = new PdfOptions();
```

## Krok 3: Načtěte DWG soubor

Načtěte existující DWG soubor jako obrázek a převeďte jej na typ `CadImage`.

```java
CadImage cadImage = (CadImage) Image.load(fileName);
```

## Krok 4: Procházejte entity

Projděte každou entitu uvnitř DWG souboru a zkontrolujte, zda se jedná o definici obrázku. Pokud ano, načtěte externí odkaz na objekt.

```java
for (CadBaseEntity baseEntity : cadImage.getEntities()) {
    if (baseEntity.getTypeName() == CadEntityTypeName.DGNUNDERLAY) {
        CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
        System.out.println(dgnFile.getUnderlayPath());
    }
}
```

## Krok 5: Definujte možnosti rasterizace

Definujte nastavení pro objekt `CadRasterizationOptions`, včetně šířky a výšky stránky, rozvržení a barvy pozadí.

```java
CadRasterizationOptions vectorRasterizationOptions = new CadRasterizationOptions();
vectorRasterizationOptions.setPageWidth(1600);
vectorRasterizationOptions.setPageHeight(1600);
vectorRasterizationOptions.setLayouts(new String[] { "Model" });
vectorRasterizationOptions.setAutomaticLayoutsScaling(false);
vectorRasterizationOptions.setNoScaling(true);
vectorRasterizationOptions.setBackgroundColor(Color.getBlack());
vectorRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
```

## Krok 6: Nastavte vektorové možnosti rasterizace

Nastavte vektorové možnosti rasterizace pro export.

```java
exportOptions.setVectorRasterizationOptions(vectorRasterizationOptions);
```

## Krok 7: Exportujte DWG do PDF

Nakonec exportujte DWG do PDF voláním metody `save`.

```java
cadImage.save(outPath, exportOptions);
```

## Časté problémy a řešení

| Problém | Příčina | Řešení |
|-------|-------|----------|
| **Nezobrazuje se žádný DGN podklad** | DWG neobsahuje entitu `DGNUNDERLAY`. | Ověřte, že zdrojový DWG obsahuje odkaz na DGN. |
| **PDF je prázdné** | Možnosti rasterizace jsou nastaveny na nulovou velikost nebo nesprávné rozvržení. | Ujistěte se, že `setPageWidth`/`setPageHeight` jsou kladné a `setLayouts` odpovídá názvu rozvržení DWG. |
| **Výjimka licence** | Spouštění bez platné licence Aspose.CAD. | Aplikujte dočasnou nebo zakoupenou licenci před voláním jakýchkoli metod API. |

## Často kladené otázky

### Q1: Kde najdu dokumentaci k Aspose.CAD pro Java?

A1: Dokumentaci najdete [zde](https://reference.aspose.com/cad/java/).

### Q2: Jak mohu stáhnout knihovnu Aspose.CAD pro Java?

A2: Knihovnu můžete stáhnout z [tohoto odkazu](https://releases.aspose.com/cad/java/).

### Q3: Je k dispozici bezplatná zkušební verze pro Aspose.CAD pro Java?

A3: Ano, bezplatnou zkušební verzi najdete [zde](https://releases.aspose.com/).

### Q4: Kde mohu získat dočasnou licenci pro Aspose.CAD pro Java?

A4: Dočasnou licenci získáte [zde](https://purchase.aspose.com/temporary-license/).

### Q5: Potřebujete pomoc nebo máte otázky?

A5: Navštivte komunitní fórum podpory Aspose.CAD [zde](https://forum.aspose.com/c/cad/19).

### Q6: Mohu převést vzniklé PDF zpět na DWG?

A6: PDF je rastrový náhled; převod zpět na DWG vyžaduje samostatný nástroj pro reverzní inženýrství.

### Q7: Funguje tento přístup i s jinými CAD formáty jako DWF nebo DXF?

A7: Ano, Aspose.CAD podporuje mnoho formátů; stačí upravit přípony souborů a nastavení rasterizace.

---

**Poslední aktualizace:** 2026-01-10  
**Testováno s:** Aspose.CAD for Java 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}