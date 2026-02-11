---
date: 2026-01-02
description: Naučte se, jak exportovat DWG do PDF, povolit skryté čáry a převést DWG
  na PDF pomocí Aspose.CAD pro Javu v tomto krok‑za‑krokem tutoriálu.
linktitle: Export DWG as PDF with Hidden Lines Using Java
second_title: Aspose.CAD Java API
title: Export DWG jako PDF se skrytými čarami – Aspose.CAD pro Javu
url: /cs/java/cad-text-and-formatting/support-hidden-lines-in-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export DWG jako PDF s skrytými čarami – Aspose.CAD pro Java

## Úvod

V tomto tutoriálu se naučíte, jak **exportovat DWG jako PDF** při zachování skrytých čar pomocí Aspose.CAD pro Java. Ať už potřebujete **převést DWG na PDF**, vytvořit průvodce ve stylu **dwg to pdf tutorial**, nebo jednoduše **uložit DWG jako PDF** s podporou skrytých čar, provede vás každým krokem. Na konci budete mít připravené řešení, které můžete vložit do libovolného projektu v Javě.

## Rychlé odpovědi
- **Co tento tutoriál pokrývá?** Povolení vykreslování skrytých čar při exportu DWG do PDF pomocí Aspose.CAD pro Java.  
- **Jaká hlavní operace se provádí?** `export dwg as pdf`.  
- **Potřebuji licenci?** Bezplatná zkušební verze funguje pro testování; pro produkční nasazení je vyžadována komerční licence.  
- **Jaké jsou předpoklady?** Vývojové prostředí Java, knihovna Aspose.CAD pro Java a soubory DWG.  
- **Jak dlouho trvá implementace?** Přibližně 10‑15 minut pro základní nastavení.

## Co je “export dwg as pdf”?
Export DWG souboru do PDF převádí vektorový CAD výkres do přenosného formátu dokumentu při zachování vrstev, typů čar a volitelného vykreslování skrytých čar. To usnadňuje sdílení CAD návrhů se zainteresovanými stranami, které nemusí mít CAD software.

## Proč povolit skryté čáry při exportu?
Skryté čáry poskytují jasnější vizuální reprezentaci složitých 3D modelů na 2‑D stránce, zajišťují, že jsou zvýrazněny pouze viditelné hrany. To zlepšuje čitelnost a často je vyžadováno pro technickou dokumentaci.

## Prerequisites

1. **Aspose.CAD pro Java** – stáhněte knihovnu z oficiálního webu [zde](https://releases.aspose.com/cad/java/).  
2. **DWG soubory** – mějte zdrojové DWG výkresy uložené v známém adresáři.  
3. **Vývojové prostředí Java** – JDK 8+ a preferované IDE (Eclipse, IntelliJ, atd.).  

Nyní, když máte vše připravené, ponořme se do kódu.

## Importování jmenných prostorů

Začněte importováním potřebných tříd, abyste mohli pracovat s CAD obrázky a PDF možnostmi.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.Arrays;
import java.util.List;
```

## Krok 1: Nastavte svůj projekt

Vytvořte Java projekt a přidejte JAR Aspose.CAD do cesty sestavení. Poté definujte adresář, který obsahuje vaše DWG soubory.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

> **Tip:** Použijte absolutní cestu nebo nakonfigurujte relativní cestu na základě složky resources vašeho projektu.

## Krok 2: Načtěte DWG soubor

Načtěte zdrojový DWG soubor do objektu `CadImage`, abyste s ním mohli manipulovat.

```java
String sourceFilePath = dataDir + "Bottom_plate.dwg";
String outPath = dataDir + "Bottom_plate.pdf";
CadImage cadImage = (CadImage)Image.load(sourceFilePath);
```

## Krok 3: Nakonfigurujte možnosti rasterizace

Vyberte vrstvy, které chcete zahrnout, a nastavte velikost stránky tak, aby odpovídala původnímu výkresu. Zde povolíme vykreslování skrytých čar zadáním rozvržení.

```java
List<String> list = Arrays.asList("Print","L1_RegMark","L2_RegMark");
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageHeight(cadImage.getHeight());
rasterizationOptions.setPageWidth(cadImage.getWidth()) ;
rasterizationOptions.setLayers(list);
```

## Krok 4: Nastavte PDF možnosti

Řekněte Aspose.CAD, aby rasterizoval vektorová data do PDF, s použitím rozvržení „Model“, aby skryté čáry zůstaly skryté.

```java
PdfOptions pdfOptions = new PdfOptions();
rasterizationOptions.setLayouts(new String[] { "Model" });
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Krok 5: Uložte výsledek

Nakonec exportujte DWG jako PDF soubor. Skryté čáry budou respektovány podle nastaveného rozvržení.

```java
cadImage.save(outPath, pdfOptions);
System.out.println("\nThe DWG file exported successfully to PDF.\nFile saved at " + dataDir);
```

> **Častá chyba:** Zapomenutí nastavit rozvržení na `"Model"` způsobí, že všechny čáry (včetně skrytých) se v PDF zobrazí jako plné.

## Závěr

Nyní máte kompletní, připravenou metodu pro **export DWG jako PDF** s podporou skrytých čar pomocí Aspose.CAD pro Java. Tento přístup lze integrovat do nástrojů pro dávkové zpracování, webových služeb nebo desktopových aplikací k automatizaci konverze CAD na PDF.

## Často kladené otázky

### Q1: Mohu použít Aspose.CAD pro Java s jinými CAD formáty?
A1: Ano, Aspose.CAD podporuje různé CAD formáty jako DWG, DXF, DWF a další.

### Q2: Je k dispozici bezplatnákušební verze pro Aspose.CAD pro Java?
A2: Ano, bezplatnou zkušební verzi najdete [zde](https://releases.aspose.com/).

### Q3: Jak získám podporu pro Aspose.CAD pro Java?
A3: Navštivte fórum Aspose.CAD [zde](https://forum.aspose.com/c/cad/19) pro komunitní podporu.

### Q4: Kde najdu podrobnou dokumentaci pro Aspose.CAD pro Java?
A4: Odkaz na dokumentaci najdete [zde](https://reference.aspose.com/cad/java/).

### Q5: Mohu zakoupit dočasnou licenci pro Aspose.CAD pro Java?
A5: Ano, dočasnou licenci můžete získat [zde](https://purchase.aspose.com/temporary-license/).

### Q6: Funguje tato metoda také pro převod DWG na PDF v prostředí bez grafického rozhraní (headless server)?
A6: Rozhodně. Protože kód používá pouze API Aspose.CAD, běží bez jakýchkoli UI závislostí, což je ideální pro automatizaci na straně serveru.

---

**Poslední aktualizace:** 2026-01-02  
**Testováno s:** Aspose.CAD pro Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}