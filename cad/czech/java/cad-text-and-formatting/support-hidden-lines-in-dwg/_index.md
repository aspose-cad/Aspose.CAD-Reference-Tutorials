---
date: 2026-03-05
description: Naučte se, jak exportovat DWG do PDF, povolit skryté čáry a převést DWG
  na PDF pomocí Aspose.CAD pro Javu v tomto tutoriálu krok za krokem.
linktitle: Export DWG as PDF Using Java
second_title: Aspose.CAD Java API
title: Export DWG do PDF se skrytými čarami – Aspose.CAD pro Java
url: /cs/java/cad-text-and-formatting/support-hidden-lines-in-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export DWG do PDF s skrytými čarami – Aspose.CAD pro Java

## Úvod

V tomto tutoriálu se naučíte, jak **export dwg to pdf** při zachování skrytých čar pomocí Aspose.CAD pro Java. Ať už potřebujete **convert DWG to PDF**, vytvořit průvodce ve stylu **dwg to pdf tutorial**, nebo jednoduše **save DWG as PDF** s podporou skrytých čar, provedeme vás všemi kroky. Na konci budete mít připravené řešení, které můžete vložit do jakéhokoli Java projektu.

## Rychlé odpovědi
- **Co tento tutoriál pokrývá?** Povolení vykreslování skrytých čar při exportu DWG do PDF pomocí Aspose.CAD pro Java.  
- **Jaká primární operace se provádí?** `export dwg to pdf`.  
- **Potřebuji licenci?** Bezplatná zkušební verze funguje pro testování; pro produkční nasazení je vyžadována komerční licence.  
- **Jaké jsou předpoklady?** Vývojové prostředí Java, knihovna Aspose.CAD pro Java a soubory DWG.  
- **Jak dlouho trvá implementace?** Přibližně 10‑15 minut pro základní nastavení.

## Co je „export dwg to pdf“?

Exportování souboru DWG do PDF převádí vektorový CAD výkres do formátu přenosného dokumentu a zachovává vrstvy, typy čar a volitelné vykreslování skrytých čar. To usnadňuje sdílení CAD návrhů se zainteresovanými stranami, které nemusí mít CAD software.

## Jak povolit skryté čáry při exportu DWG do PDF

Skryté čáry jsou řízeny nastavením layoutu v možnostech rasterizace. Výběrem layoutu **Model** Aspose.CAD říká rendereru, aby považoval skryté hrany za neviditelné, což vám poskytne čistou 2‑D reprezentaci 3‑D modelu.

## Proč povolit skryté čáry při exportu?

Skryté čáry poskytují jasnější vizuální reprezentaci složitých 3‑D modelů na 2‑D stránce, zajišťují, že jsou zdůrazněny pouze viditelné hrany. To zlepšuje čitelnost a často je vyžadováno pro technickou dokumentaci.

## Předpoklady

1. **Aspose.CAD for Java** – stáhněte knihovnu z oficiálního webu [zde](https://releases.aspose.com/cad/java/).  
2. **DWG files** – mějte zdrojové DWG výkresy uložené v známém adresáři.  
3. **Java development environment** – JDK 8+ a vaše preferované IDE (Eclipse, IntelliJ, atd.).  

Nyní, když máte vše připravené, pojďme se ponořit do kódu.

## Importovat jmenné prostory

Začněte importováním potřebných tříd, abyste mohli pracovat s CAD obrázky a PDF možnostmi.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.Arrays;
import java.util.List;
```

## Krok 1: Nastavte svůj projekt

Vytvořte Java projekt a přidejte JAR Aspose.CAD do cesty sestavení. Poté definujte adresář, který obsahuje vaše DWG soubory.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

> **Pro tip:** Použijte absolutní cestu nebo nakonfigurujte relativní cestu na základě složky resources vašeho projektu.

## Krok 2: Načtěte DWG soubor

Načtěte zdrojový DWG soubor do objektu `CadImage`, abyste s ním mohli manipulovat.

```java
String sourceFilePath = dataDir + "Bottom_plate.dwg";
String outPath = dataDir + "Bottom_plate.pdf";
CadImage cadImage = (CadImage)Image.load(sourceFilePath);
```

## Krok 3: Nakonfigurujte možnosti rasterizace

Vyberte vrstvy, které chcete zahrnout, a nastavte velikost stránky tak, aby odpovídala původnímu výkresu. Zde povolíme vykreslování skrytých čar zadáním layoutu.

```java
List<String> list = Arrays.asList("Print","L1_RegMark","L2_RegMark");
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageHeight(cadImage.getHeight());
rasterizationOptions.setPageWidth(cadImage.getWidth()) ;
rasterizationOptions.setLayers(list);
```

## Krok 4: Nastavte PDF možnosti

Řekněte Aspose.CAD, aby rasterizoval vektorová data do PDF, s použitím layoutu „Model“, aby skryté čáry zůstaly skryté.

```java
PdfOptions pdfOptions = new PdfOptions();
rasterizationOptions.setLayouts(new String[] { "Model" });
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Krok 5: Uložte výsledek

Nakonec exportujte DWG jako PDF soubor. Skryté čáry budou respektovány podle nastaveného layoutu.

```java
cadImage.save(outPath, pdfOptions);
System.out.println("\nThe DWG file exported successfully to PDF.\nFile saved at " + dataDir);
```

> **Častý úskalí:** Zapomenutí nastavit layout na "Model" způsobí, že všechny čáry (včetně skrytých) se v PDF zobrazí jako plné.

## Časté problémy a řešení

| Problém | Proč se to stane | Jak opravit |
|---------|------------------|-------------|
| PDF zobrazuje všechny čáry jako plné | Layout není nastaven na **Model** | Ujistěte se, že `rasterizationOptions.setLayouts(new String[] { "Model" });` je voláno před uložením. |
| Chybějící vrstvy ve výstupu | Nesprávné názvy vrstev | Ověřte názvy vrstev v DWG souboru a přesně je odpovídejte v `list`. |
| Chyba nedostatku paměti u velkých souborů | Velká velikost rasterizace | Snižte rozměry stránky nebo pokud možno zpracovávejte výkres po částech. |

## Často kladené otázky

### Q1: Mohu používat Aspose.CAD pro Java s jinými CAD formáty souborů?
A1: Ano, Aspose.CAD podporuje různé CAD formáty, jako jsou DWG, DXF, DWF a další.

### Q2: Je k dispozici bezplatná zkušební verze pro Aspose.CAD pro Java?
A2: Ano, bezplatnou zkušební verzi najdete [zde](https://releases.aspose.com/).

### Q3: Jak získám podporu pro Aspose.CAD pro Java?
A3: Navštivte fórum Aspose.CAD [zde](https://forum.aspose.com/c/cad/19) pro komunitní podporu.

### Q4: Kde mohu najít podrobnou dokumentaci pro Aspose.CAD pro Java?
A4: Odkazujte na dokumentaci [zde](https://reference.aspose.com/cad/java/).

### Q5: Mohu zakoupit dočasnou licenci pro Aspose.CAD pro Java?
A5: Ano, dočasnou licenci můžete získat [zde](https://purchase.aspose.com/temporary-license/).

### Q6: Funguje tato metoda také pro konverzi DWG do PDF v prostředí bez grafického rozhraní (headless server)?
A6: Rozhodně. Protože kód používá pouze API Aspose.CAD, běží bez jakýchkoli UI závislostí, což je ideální pro automatizaci na serveru.

## Závěr

Nyní máte kompletní, připravenou metodu pro **export dwg to pdf** s podporou skrytých čar pomocí Aspose.CAD pro Java. Tento přístup lze integrovat do nástrojů pro dávkové zpracování, webových služeb nebo desktopových aplikací k automatizaci konverze CAD‑to‑PDF.

---

**Last Updated:** 2026-03-05  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}