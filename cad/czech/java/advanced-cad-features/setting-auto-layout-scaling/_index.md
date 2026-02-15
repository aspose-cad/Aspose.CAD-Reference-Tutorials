---
date: 2026-02-15
description: Naučte se nastavit vlastní velikost stránky a vytvořit PDF z CAD pomocí
  Aspose.CAD pro Java. Tento krok‑za‑krokem průvodce pokrývá export CAD do PDF s automatickým
  škálováním rozložení.
linktitle: Setting Auto Layout Scaling
second_title: Aspose.CAD Java API
title: Nastavit vlastní velikost stránky – PDF z CAD s automatickým škálováním rozvržení
url: /cs/java/advanced-cad-features/setting-auto-layout-scaling/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Nastavte vlastní velikost stránky – Vytvořte PDF z CAD s automatickým škálováním rozvržení

## Úvod

Pokud potřebujete **nastavit vlastní velikost stránky** při **vytváření PDF z CAD** souborů rychle a s dokonalým škálováním, Aspose.CAD pro Java vám to umožní. Automatické škálování rozvržení (Auto Layout Scaling) automaticky upravuje rozměry rozvržení tak, aby výsledné PDF vypadalo přesně podle očekávání, bez ohledu na původní velikost CAD stránky. V tomto tutoriálu projdeme kompletní proces – od načtení DXF souboru až po export PDF – a zdůrazníme **export CAD do PDF** možnosti knihovny a ukážeme, jak můžete také **převést DWG do PDF** nebo **zvýšit rozlišení PDF**, pokud je to potřeba.

## Rychlé odpovědi
- **Co dělá Auto Layout Scaling?** Automaticky mění velikost CAD rozvržení tak, aby odpovídalo cílovým rozměrům stránky při rasterizaci.
- **Jaké formáty mohu převádět?** Jakýkoli formát podporovaný Aspose.CAD (např. DXF, DWG, DWF) lze převést do PDF.
- **Potřebuji licenci pro produkční nasazení?** Ano, pro ne‑evaluační použití je vyžadována komerční licence.
- **Jak dlouho trvá převod?** Obvykle méně než sekunda pro standardní soubory na moderním hardware.
- **Mohu změnit velikost stránky?** Ano, vlastní rozměry stránky lze nastavit pomocí `CadRasterizationOptions`.

## Co je „vytvořit PDF z CAD“?

Vytvoření PDF z CAD znamená převést vektorový inženýrský výkres (DXF, DWG, atd.) na rastrový PDF dokument. PDF si zachovává vizuální věrnost původního výkresu a je široce zobrazitelné na jakékoli platformě.

## Proč použít Auto Layout Scaling?

- **Konzistentní výstup:** Zaručuje, že všechna rozvržení vyplní PDF stránku bez ručního počítání velikostí.
- **Úspora času:** Odstraňuje potřebu ručně upravovat škálovací faktory pro každý výkres.
- **Vysoká kvalita:** Zachovává tloušťku čar a přesnost geometrie během převodu.
- **Flexibilita:** Funguje pro **convert dxf to pdf**, **convert dwg to pdf** i když potřebujete **increase PDF resolution** pro soubory připravené k tisku.

## Požadavky

1. **Aspose.CAD pro Java knihovna** – stáhněte nejnovější verzi ze [stránky ke stažení](https://releases.aspose.com/cad/java/).  
2. **Adresář zdrojů** – vytvořte složku na svém počítači pro uložení CAD souborů; nahraďte `"Your Document Directory"` v kódu touto cestou.  
3. **Ukázkový CAD soubor** – v tomto návodu použijeme `conic_pyramid.dxf`, který je součástí sady vzorových dat Aspose.

## Import jmenných prostorů

Nejprve importujte požadované třídy. To nám poskytne přístup k načítání obrázků, rasterizaci a funkcím exportu do PDF.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Jak nastavit vlastní velikost stránky pro PDF z CAD

Než se pustíme do podrobného kódu, pochopme, proč je nastavení vlastní velikosti stránky důležité. Když **nastavíte vlastní velikost stránky**, řídíte fyzické rozměry výsledného PDF (např. A4, Letter nebo vlastní rozměr). To je nezbytné pro inženýrské workflow, kde výkresy musí odpovídat standardům listů nebo když potřebujete vložit PDF do větších dokumentů.

### Krok 1: Načtěte CAD soubor

Načtení zdrojového souboru je prvním krokem v **jak exportovat CAD** do PDF dokumentu.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### Krok 2: Vytvořte možnosti rasterizace

Definujte cílové rozměry stránky. Tento blok můžete také použít k **nastavení CAD velikosti stránky** ručně, pokud preferujete vlastní rozvržení.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

### Krok 3: Nastavte Auto Layout Scaling

Povolte funkci automatického škálování. Toto je jádro **jak nastavit škálování** pro převod CAD → PDF.

```java
rasterizationOptions.setAutomaticLayoutsScaling(true);
```

### Krok 4: Vytvořte PDF možnosti

Propojte nastavení rasterizace s možnostmi exportu do PDF.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Krok 5: Export do PDF

Nakonec uložte vykreslený obrázek jako PDF soubor. Tento krok dokončuje workflow **convert dxf to pdf**.

```java
image.save(dataDir + "result_out_.pdf", pdfOptions);
```

Opakujte výše uvedené kroky pro jakékoli další CAD soubory, které potřebujete zpracovat, ať už jsou to **DWG**, **DWF** nebo jiné podporované formáty.

## Běžné scénáře použití

| Scénář | Proč nastavit vlastní velikost stránky? |
|----------|----------------------------------------|
| **Podání stavebního výkresu** | Zarovnává PDF s standardními velikostmi listů A1/A2 požadovanými regulačními orgány. |
| **Vkládání do technických příruček** | Zajišťuje, že výkres zapadne do předdefinovaného rozvržení příručky bez dalšího škálování. |
| **Vysoké rozlišení pro tisk** | Umožňuje zvýšit DPI (např. `rasterizationOptions.setResolution(300)`) při zachování konzistentních rozměrů stránky. |

## Časté problémy a řešení

| Příznak | Pravděpodobná příčina | Oprava |
|---------|-----------------------|--------|
| Prázdný PDF výstup | Nebyly nastaveny rasterizační možnosti nebo je špatná cesta k souboru | Ověřte cestu `srcFile` a ujistěte se, že `setPageWidth/Height` nejsou nula |
| Deformované škálování | `setAutomaticLayoutsScaling` zůstalo `false` | Povolte automatické škálování nebo ručně vypočítejte škálovací faktor |
| Chybějící vrstvy | Zdrojový DXF obsahuje nepodporované entity | Zkontrolujte poznámky k vydání Aspose.CAD pro podporované typy entit |

## Často kladené otázky

**Q: Je Aspose.CAD pro Java kompatibilní se všemi CAD formáty?**  
A: Aspose.CAD pro Java podporuje různé CAD formáty, včetně DWG, DXF a DWF.

**Q: Mohu dále přizpůsobit možnosti škálování?**  
A: Ano, třída `CadRasterizationOptions` poskytuje vlastnosti pro jemné ladění škálování, DPI a dalších nastavení rasterizace.

**Q: Kde najdu další dokumentaci k Aspose.CAD pro Java?**  
A: Viz [dokumentace](https://reference.aspose.com/cad/java/) pro podrobné informace a příklady.

**Q: Je k dispozici bezplatná zkušební verze Aspose.CAD pro Java?**  
A: Ano, můžete vyzkoušet [bezplatnou verzi](https://releases.aspose.com/) a poznat možnosti Aspose.CAD pro Java.

**Q: Jak mohu získat podporu nebo se zapojit do diskusí o Aspose.CAD pro Java?**  
A: Navštivte [forum Aspose.CAD](https://forum.aspose.com/c/cad/19), kde se můžete spojit s komunitou a požádat o pomoc.

**Další časté otázky**

**Q: Jak převést DWG soubor do PDF místo DXF?**  
A: Stejný kód funguje; stačí změnit příponu souboru v `srcFile` na `.dwg`.

**Q: Mohu nastavit vlastní DPI pro PDF s vyšším rozlišením?**  
A: Ano, použijte `rasterizationOptions.setResolution(300);` (nebo jakékoliv DPI, které potřebujete).

**Q: Je možné vložit písma do generovaného PDF?**  
A: Aspose.CAD rasterizuje výkres, takže písma jsou vykreslena jako vektory; samostatné vkládání písem není potřeba.

## Závěr

Po absolvování tohoto návodu víte, jak **nastavit vlastní velikost stránky** a **vytvořit PDF z CAD** souborů pomocí Aspose.CAD pro Java s automatickým škálováním rozvržení. Proces zjednodušuje workflow **export CAD do PDF**, zajišťuje konzistentní škálování a šetří vám cenný vývojový čas. Nebojte se experimentovat s různými velikostmi stránek, rozlišením a CAD formáty, aby vyhovovaly potřebám vašeho projektu, ať už **převádíte DWG do PDF**, **zvyšujete rozlišení PDF**, nebo budujete **java CAD to PDF** dávkový procesor.

---

**Poslední aktualizace:** 2026-02-15  
**Testováno s:** Aspose.CAD pro Java 24.12 (nejnovější)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}