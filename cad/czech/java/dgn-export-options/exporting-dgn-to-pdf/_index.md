---
date: 2026-05-04
description: Naučte se, jak převádět CAD PDF soubory exportem DGN do AutoCAD PDF pomocí
  Aspose.CAD pro Javu. Krok za krokem průvodce s nastavitelnou velikostí PDF a volbami.
keywords:
- convert cad pdf
- how to export dgn
- customize pdf size
- aspose cad download
- set pdf options
linktitle: Exportování DGN ve formátu AutoCAD do PDF
second_title: Aspose.CAD Java API
title: Převod CAD PDF – Bezproblémový export DGN do PDF pro AutoCAD pomocí Aspose.CAD
  pro Javu
url: /cs/java/dgn-export-options/exporting-dgn-to-pdf/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Převod CAD PDF: Snadný export DGN do AutoCAD PDF pomocí Aspose.CAD pro Java

## Úvod

If you need to **convert CAD PDF** files directly from DGN sources, you’ve come to the right place. In this tutorial we’ll walk you through using Aspose.CAD for Java to export DGN files into an AutoCAD‑compatible PDF. You’ll see how to set custom page dimensions, pick specific layouts, and fine‑tune the PDF output—all with clear, step‑by‑step code that you can drop into your own project.

## Rychlé odpovědi
- **Co znamená „convert CAD PDF“?** Odkazuje na převod CAD zdrojových souborů (např. DGN) do PDF, které zachovává vektorová data a věrnost rozvržení.  
- **Která knihovna provádí převod?** Aspose.CAD pro Java poskytuje spolehlivou, bezlicenční zkušební verzi pro tento úkol.  
- **Potřebuji licenci pro vývoj?** Bezplatná zkušební verze funguje pro testování; pro produkční použití je vyžadována komerční licence.  
- **Mohu přizpůsobit velikost PDF?** Ano – `CadRasterizationOptions` vám umožní nastavit šířku, výšku a měřítko stránky.  
- **Kolik řádků kódu je potřeba?** Méně než 20 řádků Java kódu pro načtení, konfiguraci a uložení PDF.

## Co je „convert CAD PDF“?
Převod CAD PDF znamená převzít nativní CAD výkres (např. DGN) a vytvořit PDF, které zachovává původní vektorovou grafiku, vrstvy a informace o rozvržení. Výsledné PDF lze zobrazit na jakémkoli zařízení bez potřeby CAD softwaru, což je ideální pro sdílení, tisk nebo archivaci.

## Proč použít Aspose.CAD pro Java k převodu CAD PDF?
- **Plná podpora formátů** – DGN, DWG, DXF a mnoho dalších.  
- **Žádné externí závislosti** – čistě Java, žádné nativní DLL.  
- **Detailní kontrola** – můžete vybrat, které rozvržení exportovat, nastavit vlastní velikosti stránek a řídit kvalitu rasterizace.  
- **Škálovatelné pro dávkové úlohy** – načíst a uložit desítky souborů ve smyčce s minimálním zatížením.

## Předpoklady
Než se pustíme dál, ujistěte se, že máte následující:

- **Aspose.CAD knihovna** – stáhněte ji [zde](https://releases.aspose.com/cad/java/).  
- **Adresář dokumentů** – složka ve vašem počítači, kde budou umístěny vstupní DGN soubory a výstupní PDF.

## Import balíčků

Ve vašem Java projektu importujte potřebné balíčky pro přístup k funkcím Aspose.CAD:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Nyní rozdělíme ukázkový kód do několika kroků:

## Krok 1: Definujte cesty k souborům (jak exportovat dgn)

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

Ujistěte se, že nahradíte `"Your Document Directory"` skutečnou cestou, kde se vaše soubory nacházejí.

## Krok 2: Načtěte DGN obrázek

```java
DgnImage objImage = (DgnImage) Image.load(fileName);
```

Načtěte DGN soubor pomocí Aspose.CAD.

## Krok 3: Nastavte možnosti exportu PDF (přizpůsobení velikosti pdf, nastavení pdf možností)

```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); // Export specific views
options.setVectorRasterizationOptions(vectorOptions);
```

Zde definujeme možnosti exportu PDF, včetně rozměrů stránky, automatického měřítka a konkrétních DGN rozvržení (pohledů), které chcete zahrnout do finálního PDF.

## Krok 4: Uložte PDF soubor

```java
objImage.save(outFile, options);
```

Uložte exportovaný PDF soubor. Metoda `save` použije všechny možnosti, které jste nakonfigurovali v předchozím kroku.

Opakujte tyto kroky pro jakékoli další DGN soubory, které chcete převést. Gratulujeme! Úspěšně jste **convert CAD PDF** pomocí exportu DGN souborů do formátu AutoCAD v PDF s využitím Aspose.CAD pro Java.

## Časté problémy a řešení
| Problém | Proč se vyskytuje | Řešení |
|-------|----------------|-----|
| **Soubor nenalezen** | Nesprávná cesta `dataDir` | Zkontrolujte cestu ke složce a ujistěte se, že DGN soubor existuje. |
| **Prázdné stránky v PDF** | `AutomaticLayoutsScaling` nastaveno na `false` nebo chybějící ID rozvržení | Zachovejte `setAutomaticLayoutsScaling(true)` a ověřte názvy rozvržení (`"1","2",…`). |
| **Nízké rozlišení výstupu** | Výchozí DPI rasterizace je nízké | Použijte `vectorOptions.setResolution(300);` pro zvýšení kvality (přidejte před `setVectorRasterizationOptions`). |
| **Výjimka licence** | Spuštění bez platné licence v produkci | Použijte dočasnou nebo zakoupenou licenci podle popisu v dokumentaci Aspose. |

## Často kladené otázky (další)

**Q: Mohu exportovat pouze jedno rozvržení z DGN souboru s více rozvrženími?**  
A: Ano – specifikujte požadovaná ID rozvržení v `vectorOptions.setLayouts(new String[] { "2" });`.

**Q: Je možné vložit písma do výsledného PDF?**  
A: Aspose.CAD automaticky vloží potřebná písma při rasterizaci vektorových dat; můžete také řídit vkládání písem pomocí `PdfOptions`, pokud je to potřeba.

**Q: Jak zpracovat mnoho DGN souborů najednou?**  
A: Zabalte kroky do `for` smyčky, která iteruje přes seznam názvů souborů, a pro každou iteraci použijte stejnou instanci `PdfOptions`.

**Q: Podporuje knihovna PDF chráněné heslem?**  
A: Ano – můžete nastavit heslo na objekt `PdfOptions` pomocí `options.setPassword("yourPassword");`.

**Q: Kde najdu více příkladů?**  
A: Oficiální dokumentace Aspose.CAD a ukázkové úložiště obsahují mnoho dalších scénářů.

## FAQ (originál)

### Q1: Je Aspose.CAD kompatibilní se všemi CAD formáty?
Ano, Aspose.CAD podporuje širokou škálu CAD formátů, což zajišťuje všestrannost při práci s různými typy souborů.

### Q2: Mohu přizpůsobit nastavení exportu PDF?
Rozhodně. Jak je ukázáno v tutoriálu, můžete upravit možnosti jako rozměry stránky a rozvržení podle vašich požadavků.

### Q3: Kde najdu další podporu nebo pomoc?
Navštivte [Aspose.CAD fórum](https://forum.aspose.com/c/cad/19) pro komunitní podporu a diskuze.

### Q4: Je k dispozici bezplatná zkušební verze?
Ano, bezplatnou zkušební verzi můžete získat [zde](https://releases.aspose.com/).

### Q5: Jak mohu získat dočasnou licenci?
Získejte dočasnou licenci [zde](https://purchase.aspose.com/temporary-license/).

## Závěr

V tomto tutoriálu jsme prozkoumali, jak **convert CAD PDF** soubory pomocí Aspose.CAD pro Java. Pouhých několika řádků kódu vám umožní načíst DGN výkres, jemně doladit možnosti exportu PDF a vytvořit vysoce kvalitní PDF připravené ke sdílení nebo archivaci. Nebojte se experimentovat s různými velikostmi stránek, rozvrženími nebo dávkovým zpracováním, aby vyhovovaly potřebám vašeho projektu.

---

**Last Updated:** 2026-05-04  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}