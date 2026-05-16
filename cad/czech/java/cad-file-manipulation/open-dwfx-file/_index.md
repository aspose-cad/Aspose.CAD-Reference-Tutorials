---
date: 2026-02-23
description: Naučte se, jak převést DWFX na PDF a uložit CAD jako PDF pomocí Aspose.CAD
  pro Javu. Rychlý průvodce otevřením souborů DWFX a generováním PDF.
linktitle: Open DWFX File
second_title: Aspose.CAD Java API
title: Převést DWFX na PDF pomocí Aspose.CAD pro Java
url: /cs/java/cad-file-manipulation/open-dwfx-file/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Převod DWFX na PDF pomocí Aspose.CAD pro Java

## Úvod

V dnešním rychle se rozvíjejícím světě designu vývojáři často potřebují **převést DWFX na PDF**, aby CAD výkresy mohly být sdíleny s netechnickými zúčastněnými stranami. Aspose.CAD pro Java tuto úlohu zjednodušuje – umožňuje otevřít soubor DWFX, rasterizovat jej a **uložit CAD jako PDF** pomocí několika řádků kódu. V tomto tutoriálu projdeme celý proces – od nastavení prostředí až po ověření výsledného PDF – abyste mohli sebejistě pracovat se soubory DWFX ve svých Java aplikacích.

## Rychlé odpovědi
- **Jaký je hlavní účel tohoto průvodce?** Ukázat, jak převést DWFX na PDF pomocí Aspose.CAD pro Java.  
- **Která knihovna je vyžadována?** Aspose.CAD pro Java (stáhněte z oficiálního webu Aspose).  
- **Potřebuji licenci?** Pro vývoj stačí bezplatná zkušební verze; pro produkci je vyžadována komerční licence.  
- **Mohu soubory DWFX otevřít přímo?** Ano, použijte `Image.load` k otevření souborů DWFX.  
- **Jaký výstupní formát příklad vytváří?** Soubor PDF uložený do zadaného výstupního adresáře.

## Co znamená „převod DWFX na PDF“?

Převod DWFX na PDF znamená převést vektorový výkres DWFX – běžně používaný v produktech Autodesk – do přenosného, široce podporovaného PDF dokumentu. To umožňuje snadné prohlížení, tisk a sdílení bez nutnosti CAD softwaru na straně příjemce.

## Proč použít Aspose.CAD pro Java k **uložení CAD jako PDF**?

- **Žádné externí závislosti:** Čisté Java API, není potřeba nativních CAD engineů.  
- **Vysoká věrnost renderování:** Zachovává tloušťky čar, barvy a vrstvy.  
- **Vhodné pro dávkové zpracování:** Ideální pro automatizaci na serveru nebo cloudové služby.  
- **Cross‑platform:** Funguje na Windows, Linuxu i macOS.

## Požadavky

Než se pustíme do kódu, ujistěte se, že máte následující:

- **Aspose.CAD for Java Library** – Stáhněte si ji z [Aspose.CAD for Java download page](https://releases.aspose.com/cad/java/).  
- **Java Development Environment** – JDK 8 nebo novější, s vaším oblíbeným IDE nebo nástrojem pro sestavení.  
- **DWFX File** – Ukázkový soubor DWFX (např. `Tyrannosaurus.dwfx`) pro testování převodu.

## Import Namespaces

Nejprve importujte třídy, které budeme potřebovat:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Jak převést DWFX na PDF pomocí Aspose.CAD pro Java

Níže je podrobný postup krok za krokem. Každý krok obsahuje krátké vysvětlení a přesný kód, který spustíte.

### Krok 1: Načtení souboru DWFX  

```java
String SourceDir = Utils.getDataDir_DWFXDrawings();
String OutputDir = Utils.getDataDir_Output();
String filePath = SourceDir + "Tyrannosaurus.dwfx";

Image cadImageDwf = Image.load(filePath);
```

Metoda `Image.load` načte soubor DWFX do paměti a vytvoří objekt `CadImage`, který je připravený k rasterizaci.

### Krok 2: Nastavení možností rasterizace  

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(cadImageDwf.getSize().getWidth());
rasterizationOptions.setPageHeight(cadImageDwf.getSize().getHeight());
```

Tyto možnosti definují velikost výstupní stránky, aby PDF odpovídalo původním rozměrům výkresu.

### Krok 3: Konfigurace PDF možností  

```java
PdfOptions CADf = new PdfOptions();
CADf.setVectorRasterizationOptions(rasterizationOptions);
```

Zde propojujeme nastavení rasterizace s konfigurací exportu do PDF.

### Krok 4: Uložení jako PDF  

```java
cadImageDwf.save(OutputDir + "OpenDwfxFile_out.pdf", CADf);
```

Voláním `save` zapíšeme vykreslený obrázek do souboru PDF ve výstupním adresáři.

### Krok 5: Ověření úspěchu  

```java
System.out.println("OpenDwfxFile executed successfully");
```

Jednoduchá zpráva v konzoli potvrzuje, že převod byl dokončen bez chyb.

## Časté problémy a řešení

| Problém | Pravděpodobná příčina | Řešení |
|---------|----------------------|--------|
| **Blank PDF output** | Šířka/výška rasterizace nastavena na 0 | Ujistěte se, že `cadImageDwf.getSize()` vrací platné rozměry před nastavením možností. |
| **Out‑of‑memory error** | Velmi velký soubor DWFX | Zvyšte velikost haldy JVM (`-Xmx2g`) nebo soubor zpracovávejte po menších částech. |
| **Missing fonts** | Písmo není vloženo ve zdrojovém DWFX | Nainstalujte požadovaná písma na server nebo použijte `CadRasterizationOptions.setFontName` k určení náhradního písma. |

## Často kladené otázky

### Q1: Mohu použít Aspose.CAD pro Java i s jinými CAD formáty?  
A1: Ano, Aspose.CAD pro Java podporuje širokou škálu CAD formátů a poskytuje tak všestranné řešení pro vývojáře.

### Q2: Je k dispozici bezplatná zkušební verze Aspose.CAD pro Java?  
A2: Ano, můžete si vyzkoušet funkce Aspose.CAD pro Java pomocí bezplatné zkušební verze. Navštivte [this link](https://releases.aspose.com/) a začněte.

### Q3: Jak získám podporu pro Aspose.CAD pro Java?  
A3: Připojte se ke komunitě Aspose.CAD na [support forum](https://forum.aspose.com/c/cad/19) a získejte pomoc a spolupráci.

### Q4: Existují dočasné licence pro Aspose.CAD pro Java?  
A4: Ano, můžete získat dočasnou licenci pro Aspose.CAD pro Java. Navštivte [this link](https://purchase.aspose.com/temporary-license/) pro více informací.

### Q5: Kde najdu dokumentaci k Aspose.CAD pro Java?  
A5: Kompletní dokumentace je k dispozici [here](https://reference.aspose.com/cad/java/).

---

**Poslední aktualizace:** 2026-02-23  
**Testováno s:** Aspose.CAD for Java 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}