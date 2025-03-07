---
title: DWG do souladu s PDF pomocí Aspose.CAD pro Java
linktitle: PDF v souladu s DWG
second_title: Aspose.CAD Java API
description: Bez námahy převádějte výkresy DWG do souborů kompatibilních s PDF/A1a a PDF/A1b pomocí Aspose.CAD for Java. Zefektivněte svůj pracovní postup s přesností a lehkostí.
weight: 11
url: /cs/java/cad-to-pdf-and-svg-export-options/dwg-to-compliance-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG do souladu s PDF pomocí Aspose.CAD pro Java

## Úvod

V neustále se vyvíjejícím světě digitálního designu je potřeba převádět výkresy DWG do vyhovujících formátů PDF zásadní pro bezproblémovou spolupráci a standardizovanou dokumentaci. Aspose.CAD for Java se ukazuje jako výkonný nástroj, který v tomto procesu nabízí efektivitu a přesnost. V tomto tutoriálu prozkoumáme, jak využít Aspose.CAD pro Java k snadnému převodu souborů DWG na vyhovující PDF, což zajistí dodržování standardů PDF/A1a a PDF/A1b.

## Předpoklady

Než se pustíte do výukového programu, ujistěte se, že máte splněny následující předpoklady:

- Vývojové prostředí Java: Ujistěte se, že máte ve svém systému nastavené funkční vývojové prostředí Java.
-  Knihovna Aspose.CAD: Stáhněte a nainstalujte knihovnu Aspose.CAD pro Javu z[odkaz ke stažení](https://releases.aspose.com/cad/java/).
- Adresář dokumentů: Vytvořte adresář pro ukládání výkresů DWG.

## Importovat jmenné prostory

Do svého projektu Java importujte potřebné jmenné prostory pro přístup k funkcím Aspose.CAD. Na začátek souboru Java přidejte následující řádky:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfCompliance;
import com.aspose.cad.imageoptions.PdfDocumentOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Krok 1: Nastavte Resource Directory

Definujte cestu k adresáři prostředků, kde jsou uloženy výkresy DWG.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

## Krok 2: Načtěte soubor DWG

Načtěte soubor DWG pomocí knihovny Aspose.CAD.

```java
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

## Krok 3: Vytvořte možnosti PDF

Vytvořte instanci PdfOptions a nastavte možnosti vektorové rasterizace.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

## Krok 4: Nastavte základní možnosti PDF

Nastavte základní možnosti PDF a určete standard shody (PDF/A1a nebo PDF/A1b).

```java
pdfOptions.setCorePdfOptions(new PdfDocumentOptions());
pdfOptions.getCorePdfOptions().setCompliance(PdfCompliance.PdfA1a);
```

## Krok 5: Uložte PDF s dodržováním A1a

Uložte soubor PDF v souladu s A1a.

```java
objImage.save(dataDir + "Saved1.pdf", pdfOptions);
```

## Krok 6: Změňte shodu na A1b

Změňte shodu na PDF/A1b a uložte PDF.

```java
pdfOptions.getCorePdfOptions().setCompliance(PdfCompliance.PdfA1b);
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

Opakujte tyto kroky pro každý soubor DWG, který chcete převést.

## Závěr

Na závěr, Aspose.CAD for Java poskytuje robustní řešení pro převod souborů DWG na vyhovující PDF. Dodržováním tohoto podrobného průvodce můžete zefektivnit proces převodu a zajistit, aby vaše dokumenty odpovídaly průmyslovým standardům.

## FAQ

### Q1: Je Aspose.CAD kompatibilní se všemi verzemi souborů DWG?

 A1: Aspose.CAD podporuje různé verze souborů DWG, včetně nejnovějších. Odkazovat na[dokumentace](https://reference.aspose.com/cad/java/) pro podrobné informace o kompatibilitě.

### Q2: Mohu upravit nastavení výstupu PDF pomocí Aspose.CAD?

A2: Rozhodně! Aspose.CAD nabízí řadu možností přizpůsobení, které vám umožní přizpůsobit výstup PDF vašim specifickým požadavkům.

### Q3: Je k dispozici dočasná licence pro Aspose.CAD?

 A3: Ano, můžete získat dočasnou licenci pro testovací účely od[tento odkaz](https://purchase.aspose.com/temporary-license/).

### Q4: Kde mohu hledat podporu nebo komunikovat s komunitou pro Aspose.CAD?

 A4: Navštivte[Fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) za podporu komunity a diskuze.

### Q5: Mohu si Aspose.CAD zdarma vyzkoušet před nákupem?

 A5: Určitě! Stáhněte si bezplatnou zkušební verzi z[tady](https://releases.aspose.com/) prozkoumat možnosti, než se rozhodnete.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
