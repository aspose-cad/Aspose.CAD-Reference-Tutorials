---
title: Export do PDF pomocí Aspose.CAD for Java
linktitle: Export do PDF
second_title: Aspose.CAD Java API
description: Naučte se, jak bez námahy exportovat soubory CAD do PDF pomocí Aspose.CAD for Java. Postupujte podle našeho podrobného průvodce pro bezproblémovou integraci.
weight: 13
url: /cs/java/cad-export-options/export-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export do PDF pomocí Aspose.CAD for Java

## Úvod

Vítejte v tomto komplexním tutoriálu o exportu souborů CAD do PDF pomocí Aspose.CAD pro Java. Pokud hledáte bezproblémový převod výkresů CAD do široce podporovaného formátu PDF, jste na správném místě. V tomto podrobném průvodci rozebereme celý proces a zajistíme, že pochopíte každý krok k dosažení úspěšného exportu PDF.

## Předpoklady

Než se pustíte do výukového programu, ujistěte se, že máte splněny následující předpoklady:

-  Aspose.CAD for Java: Ujistěte se, že máte ve svém prostředí Java nainstalovanou knihovnu Aspose.CAD. Můžete si jej stáhnout[tady](https://releases.aspose.com/cad/java/).

- Resource Directory: Nastavte adresář, kde jsou uloženy vaše CAD soubory. Nahraďte "Your Document Directory" v poskytnutém fragmentu kódu skutečnou cestou.

Nyní přejděme k hlavním krokům.

## Importovat jmenné prostory

Ve svém projektu Java začněte importem potřebných jmenných prostorů, aby bylo možné používat funkce Aspose.CAD.

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterpolationMode;
import com.aspose.cad.SmoothingMode;
import com.aspose.cad.TextRenderingHint;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

## Krok 1: Načtěte soubor CAD

Načtěte svůj CAD soubor do objektu Aspose.CAD Image. Nahraďte "site.dwf" svým skutečným názvem souboru CAD.

```java
String fileName = (dataDir + "site.dwf");
Image image = Image.load(fileName);
```

## Krok 2: Nakonfigurujte možnosti PDF

Nastavte možnosti exportu PDF, včetně možností vektorového rastrování, jako je výška, šířka a rozvržení stránky.

```java
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);

rasterizationOptions.setPageHeight(500);
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setLayouts(new String[] { "Model" });
```

## Krok 3: Export do PDF

Zadejte výstupní cestu pro vygenerovaný soubor PDF a uložte obraz s nakonfigurovanými možnostmi PDF.

```java
String outPath = dataDir + "site.pdf";
image.save(outPath, pdfOptions);
```

Gratulujeme! Úspěšně jste exportovali svůj CAD soubor do PDF pomocí Aspose.CAD for Java.

## Závěr

V tomto tutoriálu jsme prozkoumali krok za krokem proces exportu CAD souborů do PDF pomocí Aspose.CAD for Java. Dodržováním těchto jednoduchých, ale účinných kroků můžete tuto funkci hladce integrovat do svých aplikací Java.

## FAQ

### Q1: Je Aspose.CAD kompatibilní se všemi formáty souborů CAD?

Odpověď 1: Ano, Aspose.CAD podporuje širokou škálu formátů CAD, což zajišťuje kompatibilitu s různým návrhářským softwarem.

### Q2: Mohu přizpůsobit nastavení výstupu PDF?

A2: Rozhodně. Výukový program poskytuje letmý pohled na možnosti přizpůsobení, ale můžete prozkoumat dále a přizpůsobit výstup podle svých potřeb.

### Q3: Kde najdu další podporu pro Aspose.CAD?

 A3: V případě jakýchkoli dotazů nebo problémů navštivte[Fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) hledat pomoc od komunity.

### Q4: Je k dispozici bezplatná zkušební verze?

 A4: Ano, máte přístup k bezplatné zkušební verzi Aspose.CAD[tady](https://releases.aspose.com/).

### Q5: Jak mohu získat dočasnou licenci pro Aspose.CAD?

 A5: Pro dočasné licencování navštivte[tento odkaz](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
