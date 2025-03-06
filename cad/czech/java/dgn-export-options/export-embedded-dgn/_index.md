---
title: Export Embedded DGN do PDF pomocí Aspose.CAD for Java
linktitle: Export Embedded DGN
second_title: Aspose.CAD Java API
description: Prozkoumejte podrobného průvodce exportem vložených souborů DGN do PDF pomocí Aspose.CAD for Java. Vylepšete své aplikace Java bezproblémovou manipulací se soubory CAD.
weight: 11
url: /cs/java/dgn-export-options/export-embedded-dgn/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export Embedded DGN do PDF pomocí Aspose.CAD for Java

## Úvod

Vítejte v tomto komplexním tutoriálu o exportu vložených souborů DGN pomocí Aspose.CAD pro Java. Aspose.CAD je výkonná knihovna, která umožňuje vývojářům v Javě bezproblémově pracovat se soubory CAD. V tomto tutoriálu vás provedeme procesem exportu vložených souborů DGN do PDF pomocí podrobných pokynů. Ať už jste zkušený vývojář nebo teprve začínáte, tento tutoriál vám pomůže využít možnosti Aspose.CAD k vylepšení vašich aplikací Java.

## Předpoklady

Než se pustíme do výukového programu, ujistěte se, že máte následující předpoklady:
- Vývojové prostředí Java: Ujistěte se, že máte na svém počítači nastavené vývojové prostředí Java.
-  Aspose.CAD for Java: Stáhněte si a nainstalujte knihovnu Aspose.CAD for Java z[tady](https://releases.aspose.com/cad/java/).

## Importujte balíčky

Chcete-li začít, musíte do svého projektu Java importovat potřebné balíčky. Přidejte do kódu následující příkazy pro import:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Nyní si ukázkový kód rozdělíme do několika kroků:

## Krok 1: Nastavte vstupní a výstupní cesty

Definujte cestu k adresáři, kde je umístěn váš dokument, a zadejte název vstupního souboru DWG.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
```

## Krok 2: Načtěte soubor DWG

 Načtěte soubor DWG do souboru`Image` objekt pomocí Aspose.CAD.

```java
Image objImage = Image.load(fileName);
```

## Krok 3: Nakonfigurujte možnosti rastrování

Nakonfigurujte možnosti rasterizace, jako jsou rozvržení, která mají být zahrnuta do exportu.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setLayouts(new String[] {"Model"});
```

## Krok 4: Nakonfigurujte možnosti PDF

Nastavte možnosti PDF, včetně možností vektorového rastrování.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Krok 5: Uložte soubor PDF

Uložte soubor PDF s nakonfigurovanými možnostmi.
```java
objImage.save(dataDir + "BlockRefDgn.pdf", pdfOptions);
```

## Závěr

Gratulujeme! Úspěšně jste exportovali vložený soubor DGN do PDF pomocí Aspose.CAD for Java. Tento tutoriál se zabýval základními kroky k integraci Aspose.CAD do vaší Java aplikace pro efektivní manipulaci se soubory CAD.

## FAQ

### Q1: Mohu použít Aspose.CAD for Java v komerčním projektu?

 A1: Ano, Aspose.CAD for Java je komerční knihovna. Licenci můžete získat od[tady](https://purchase.aspose.com/buy).

### Q2: Je k dispozici bezplatná zkušební verze?

 A2:Ano, máte přístup k bezplatné zkušební verzi Aspose.CAD pro Javu[tady](https://releases.aspose.com/).

### Q3: Jak mohu získat podporu pro Aspose.CAD pro Java?

A3: Můžete vyhledat podporu od komunity Aspose.CAD na[Fórum](https://forum.aspose.com/c/cad/19).

### Q4: Co když potřebuji dočasnou licenci?

 A4: Můžete získat dočasnou licenci[tady](https://purchase.aspose.com/temporary-license/).

### Q5: Kde najdu dokumentaci?

 A5: Dokumentace je k dispozici[tady](https://reference.aspose.com/cad/java/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
