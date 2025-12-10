---
date: 2025-12-10
description: Naučte se, jak vytvořit PDF z CAD pomocí Aspose.CAD pro Javu s automatickým
  škálováním rozvržení. Tento krok‑za‑krokem průvodce vám ukáže, jak exportovat CAD
  do PDF efektivně a spolehlivě.
linktitle: Setting Auto Layout Scaling
second_title: Aspose.CAD Java API
title: Vytvořit PDF z CAD – Automatické škálování rozložení s Aspose.CAD Java
url: /cs/java/advanced-cad-features/setting-auto-layout-scaling/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Vytvořit PDF z CAD – Automatické škálování rozvržení s Aspose.CAD Java

## Úvod

Pokud potřebujete **vytvořit PDF z CAD** souborů rychle a s dokonalým škálováním, Aspose.CAD pro Java vám poskytne vše potřebné. Auto Layout Scaling automaticky upravuje rozměry rozvržení tak, aby výsledné PDF vypadalo přesně podle očekávání, bez ohledu na původní velikost CAD stránky. V tomto tutoriálu projdeme celý proces – od načtení DXF souboru po export PDF – a zdůrazníme schopnosti **export CAD do PDF** knihovny.

## Rychlé odpovědi
- **Co dělá Auto Layout Scaling?** Automaticky mění velikost rozvržení CAD tak, aby odpovídalo cílovým rozměrům stránky při rasterizaci.
- **Jaké formáty mohu převést?** Jakýkoli formát podporovaný Aspose.CAD (např. DXF, DWG, DWF) lze převést do PDF.
- **Potřebuji licenci pro produkční použití?** Ano, pro ne‑evaluační použití je vyžadována komerční licence.
- **Jak dlouho trvá konverze?** Obvykle méně než sekunda pro standardní soubory na moderním hardwaru.
- **Mohu změnit velikost stránky?** Ano, můžete nastavit vlastní rozměry stránky pomocí `CadRasterizationOptions`.

## Co znamená „vytvořit PDF z CAD“?
Vytvoření PDF z CAD znamená převést vektorový technický výkres (DXF, DWG atd.) na rastrový PDF dokument. PDF zachová vizuální věrnost původního výkresu a zároveň bude široce zobrazitelné na jakékoli platformě.

## Proč používat Auto Layout Scaling?
- **Konzistentní výstup:** Zajišťuje, že všechna rozvržení vyplní PDF stránku bez nutnosti ručních výpočtů velikosti.
- **Úspora času:** Odstraňuje potřebu ručně upravovat škálovací faktory pro každý výkres.
- **Vysoká kvalita:** Zachovává tloušťku čar a geometrickou přesnost během konverze.

## Požadavky

1. **Aspose.CAD for Java Library** – stáhněte nejnovější verzi ze [stránky ke stažení](https://releases.aspose.com/cad/java/).  
2. **Resource Directory** – vytvořte složku na svém počítači pro ukládání CAD souborů; nahraďte `"Your Document Directory"` v kódu touto cestou.  
3. **Sample CAD File** – pro tento návod použijeme `conic_pyramid.dxf`, který je součástí sady vzorových dat Aspose.

## Importovat jmenné prostory

Nejprve importujte požadované třídy. To nám poskytne přístup k načítání obrázků, rasterizaci a exportu do PDF.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Krok 1: Načíst CAD soubor

Načtení zdrojového souboru je prvním krokem v **jak exportovat CAD** do PDF dokumentu.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

## Krok 2: Vytvořit možnosti rasterizace

Definujte cílové rozměry stránky. Tento blok můžete také použít k **nastavení velikosti CAD stránky** ručně, pokud preferujete vlastní rozvržení.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

## Krok 3: Nastavit Auto Layout Scaling

Povolte funkci automatického škálování. Toto je jádro **nastavení škálování** pro konverzi CAD → PDF.

```java
rasterizationOptions.setAutomaticLayoutsScaling(true);
```

## Krok 4: Vytvořit PDF možnosti

Propojte nastavení rasterizace s možnostmi exportu do PDF.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Krok 5: Exportovat do PDF

Nakonec uložte vykreslený obrázek jako PDF soubor. Tento krok dokončuje workflow **převodu DXF do PDF**.

```java
image.save(dataDir + "result_out_.pdf", pdfOptions);
```

Opakujte výše uvedené kroky pro jakékoli další CAD soubory, které potřebujete zpracovat.

## Časté problémy a řešení

| Symptom | Pravděpodobná příčina | Řešení |
|---------|-----------------------|--------|
| Prázdný výstup PDF | Možnosti rasterizace nejsou nastaveny nebo je nesprávná cesta k souboru | Ověřte cestu `srcFile` a ujistěte se, že `setPageWidth/Height` nejsou nula |
| Deformované škálování | `setAutomaticLayoutsScaling` ponecháno na `false` | Povolte automatické škálování nebo ručně vypočítejte faktor škálování |
| Chybějící vrstvy | Zdrojový DXF obsahuje nepodporované entity | Zkontrolujte poznámky k vydání Aspose.CAD pro podporované typy entit |

## Často kladené otázky

### Q1: Je Aspose.CAD pro Java kompatibilní se všemi formáty CAD souborů?

A1: Aspose.CAD pro Java podporuje různé CAD formáty, včetně DWG, DXF a DWF.

### Q2: Mohu dále přizpůsobit možnosti škálování?

A2: Ano, třída `CadRasterizationOptions` poskytuje různé vlastnosti pro jemné ladění škálování a dalších nastavení.

### Q3: Kde najdu další dokumentaci k Aspose.CAD pro Java?

A3: Viz [dokumentace](https://reference.aspose.com/cad/java/) pro podrobné informace a příklady.

### Q4: Je k dispozici bezplatná zkušební verze Aspose.CAD pro Java?

A4: Ano, můžete vyzkoušet [bezplatnou verzi](https://releases.aspose.com/) a poznat možnosti Aspose.CAD pro Java.

### Q5: Jak mohu získat pomoc nebo se zapojit do diskusí o Aspose.CAD pro Java?

A5: Navštivte [forum Aspose.CAD](https://forum.aspose.com/c/cad/19), kde můžete komunikovat s komunitou a získat podporu.

**Další časté otázky**

**Q: Jak převést soubor DWG do PDF místo DXF?**  
A: Stejný kód funguje; stačí změnit příponu souboru v `srcFile` na `.dwg`.

**Q: Mohu nastavit vlastní DPI pro PDF s vyšším rozlišením?**  
A: Ano, použijte `rasterizationOptions.setResolution(300);` (nebo jakékoliv DPI, které potřebujete).

**Q: Je možné vložit písma do generovaného PDF?**  
A: Aspose.CAD rasterizuje výkres, takže písma jsou vykreslena jako vektory; samostatné vkládání písem není vyžadováno.

## Závěr

Po absolvování tohoto průvodce nyní víte, jak **vytvořit PDF z CAD** souborů pomocí Aspose.CAD pro Java s Auto Layout Scaling. Proces zjednodušuje workflow **export CAD do PDF**, zajišťuje konzistentní škálování a šetří vám cenný čas vývoje. Nebojte se experimentovat s různými velikostmi stránek, rozlišením a CAD formáty, aby vyhovovaly potřebám vašeho projektu.

---

**Last Updated:** 2025-12-10  
**Tested With:** Aspose.CAD for Java 24.12 (latest)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}