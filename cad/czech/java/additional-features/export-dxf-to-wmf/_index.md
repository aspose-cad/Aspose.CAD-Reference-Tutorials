---
date: 2025-11-29
description: Naučte se, jak převést DXF na WMF pomocí Aspose.CAD pro Java, načíst
  výkres DXF a volitelně použít export Aspose do PDF. Průvodce krok za krokem s ukázkami
  kódu.
language: cs
linktitle: Export DXF to WMF Format Using Java
second_title: Aspose.CAD Java API
title: Převod DXF na WMF pomocí Aspose.CAD v Javě
url: /java/additional-features/export-dxf-to-wmf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Převod DXF na WMF pomocí Aspose.CAD v Javě

## Úvod

V tomto tutoriálu se dozvíte, jak **převést DXF na WMF** pomocí Aspose.CAD pro Javu. Ať už potřebujete vložit CAD výkresy do Windows‑založené zprávy nebo jen chcete lehký vektorový formát, převod DXF na WMF je běžná potřeba. Provedeme vás načtením DXF výkresu, nastavením parametrů rasterizace, uložením výsledku jako WMF a dokonce i použitím exportu Aspose do PDF jako volitelného kroku.

## Rychlé odpovědi
- **Mohu převést DXF na WMF s bezplatnou zkušební verzí?** Ano – Aspose nabízí plně funkční 30‑day trial.  
- **Jaká verze Javy je požadována?** Java 8 nebo novější.  
- **Potřebuji licenci pro spuštění kódu?** Licence je vyžadována pro produkci; zkušební verze funguje pro vývoj a testování.  
- **Je převod bezztrátový?** Vektorová data jsou zachována; možnosti rasterizace vám umožní řídit rozlišení.  
- **Mohu také exportovat stejný výkres do PDF?** Rozhodně – viz krok „Export do PDF“ níže.

## Co je „převod DXF na WMF“?

Převod DXF na WMF znamená převést soubor Drawing Exchange Format (DXF) – široce používaný CAD formát – na Windows Metafile (WMF). WMF je vektorový obrazový formát, který se hladce integruje s Microsoft Office, Windows aplikacemi a mnoha nástroji pro tvorbu zpráv.

## Proč použít Aspose.CAD pro Javu?

- **Žádné externí závislosti** – čistá Java, žádné nativní DLL.  
- **Vysoká věrnost** – zachovává vrstvy, barvy a styly čar.  
- **Vestavěná rasterizace** – jemně ladí velikost stránky, rozlišení a pozadí.  
- **Komplexní řešení** – stejné API také podporuje export do PDF, PNG, SVG a dalších formátů.

## Požadavky

- **Aspose.CAD pro Javu** integrován do vašeho projektu. Stáhněte jej z oficiálního webu: [Aspose.CAD Java download](https://releases.aspose.com/cad/java/).  
- **Adresář dokumentů**, kde jsou uloženy vaše soubory DXF (např. `Your Document Directory/DXFDrawings/`).  

## Import jmenných prostorů

Ve vašem Java zdrojovém souboru importujte třídy Aspose.CAD, které budete potřebovat:

```java
import com.aspose.cad.Color;
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.WmfOptions;
```

## Postup krok za krokem

### Krok 1: Načtení DXF výkresu

Nejprve **načtěte DXF výkres**, který chcete převést. Metoda `Image.load` načte soubor do paměti.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DXFDrawings/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### Krok 2: Nastavení parametrů rasterizace

Nastavte parametry rasterizace, které řídí velikost výstupního WMF. V tomto příkladu používáme stránku o rozměrech 100 × 100 jednotek.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(100);
rasterizationOptions.setPageHeight(100);
WmfOptions wmfOptions = new WmfOptions();
```

### Krok 3: Uložení jako WMF

Nyní uložte načtený výkres jako soubor WMF pomocí výše definovaných možností.

```java
cadImage.save(dataDir+" example.ifc.wmf", wmfOptions);
```

### Krok 4: Uvolnění prostředků

Správné uvolnění prostředků zabraňuje únikům paměti, zejména při zpracování mnoha výkresů.

```java
finally
{
  cadImage.dispose();
}
```

### Krok 5: Volitelné – export Aspose do PDF

Pokud potřebujete také PDF verzi stejného výkresu, Aspose.CAD to umožňuje jedním řádkem kódu.

```java
image.save(dataDir + "conic_pyramid_out_.pdf"); 
```

> **Pro tip:** Můžete znovu použít stejný objekt `CadRasterizationOptions` pro export do PDF tím, že jej předáte instanci `PdfOptions`.

## Časté problémy a řešení

| Problém | Příčina | Oprava |
|-------|-------|-----|
| **`NullPointerException` on `cadImage.save`** | Proměnná `cadImage` není definována (měla by být `image`). | Nahraďte `cadImage` za `image` nebo proměnnou přejmenujte konzistentně. |
| **Output WMF is blank** | Velikost stránky rasterizace je příliš malá nebo je barva pozadí nastavena na průhlednou. | Zvyšte `PageWidth`/`PageHeight` nebo nastavte barvu pozadí pomocí `rasterizationOptions.setBackgroundColor(Color.getWhite());`. |
| **License exception** | Spuštění bez platné Aspose licence v produkci. | Načtěte licenční soubor při startu aplikace: `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`. |

## Závěr

Nyní máte kompletní, připravený workflow pro **převod DXF na WMF** pomocí Aspose.CAD pro Javu, s volitelným krokem pro **export Aspose do PDF**. Tento přístup vám poskytuje vysoce kvalitní vektorový výstup, který se bez problémů integruje s Windows‑založenými nástroji pro tvorbu zpráv a dokumentaci.

## Často kladené otázky

### Q1: Kde najdu dokumentaci k Aspose.CAD?

A1: Můžete přistupovat k dokumentaci [zde](https://reference.aspose.com/cad/java/).

### Q2: Jak stáhnu Aspose.CAD pro Javu?

A2: Stáhněte knihovnu [zde](https://releases.aspose.com/cad/java/).

### Q3: Je k dispozici bezplatná zkušební verze?

A3: Ano, můžete získat bezplatnou zkušební verzi [zde](https://releases.aspose.com/).

### Q4: Potřebujete dočasné licenční možnosti?

A4: Prozkoumejte dočasné licence [zde](https://purchase.aspose.com/temporary-license/).

### Q5: Kde mohu získat podporu?

A5: Navštivte fórum podpory Aspose.CAD [zde](https://forum.aspose.com/c/cad/19).

## Často kladené otázky

**Q: Mohu převést velké DXF soubory (stovky MB) bez vyčerpání paměti?**  
A: Ano. Načtěte soubor v bloku `try‑with‑resources` a okamžitě uvolněte objekt `Image`. Upravením `CadRasterizationOptions.setPageWidth/Height` na rozumnou velikost udržíte spotřebu paměti nízkou.

**Q: Zachovává výstup WMF informace o vrstvách?**  
A: WMF je plochý vektorový formát, takže hierarchie vrstev je zploštěna, ale styly čar a barvy jsou zachovány.

**Q: Je možné nastavit vlastní DPI pro WMF?**  
A: Použijte `rasterizationOptions.setResolution(300);` pro definování DPI před uložením.

**Q: Mohu hromadně převádět více DXF souborů v jednom běhu?**  
A: Rozhodně. Procházejte adresář, načtěte každý soubor a aplikujte stejnou logiku rasterizace a uložení.

**Q: Jaké verze Javy jsou podporovány?**  
A: Aspose.CAD pro Javu podporuje Java 8 a novější (včetně Java 11, 17 a dalších novějších LTS verzí).

---

**Poslední aktualizace:** 2025-11-29  
**Testováno s:** Aspose.CAD for Java 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}