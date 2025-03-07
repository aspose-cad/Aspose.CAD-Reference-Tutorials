---
title: Export DXF do formátu WMF pomocí Aspose.CAD v Javě
linktitle: Export DXF do formátu WMF pomocí Java
second_title: Aspose.CAD Java API
description: Odemkněte sílu Aspose.CAD pro Javu. Naučte se, jak bez námahy exportovat výkresy DXF do formátu WMF, pomocí našeho podrobného návodu. Stáhněte si knihovnu, postupujte podle našeho podrobného průvodce a vylepšete práci se soubory CAD.
weight: 14
url: /cs/java/additional-features/export-dxf-to-wmf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export DXF do formátu WMF pomocí Aspose.CAD v Javě

## Úvod

Vítejte v našem podrobném průvodci o použití Aspose.CAD pro Java k exportu DXF výkresů do formátu WMF. Aspose.CAD je výkonná Java knihovna, která poskytuje rozsáhlé možnosti pro práci se soubory CAD. V tomto tutoriálu vás provedeme procesem převodu souborů DXF do formátu WMF pomocí Aspose.CAD.

## Předpoklady

Než začnete, ujistěte se, že máte splněny následující předpoklady:

-  Aspose.CAD for Java: Ujistěte se, že máte knihovnu Aspose.CAD integrovanou do vašeho projektu Java. Můžete si jej stáhnout[tady](https://releases.aspose.com/cad/java/).

- Adresář dokumentů: Nastavte adresář dokumentů, kde jsou uloženy vaše výkresy DXF.

## Importovat jmenné prostory

Do svého projektu Java importujte potřebné jmenné prostory pro přístup k funkcím poskytovaným Aspose.CAD:

```java
import com.aspose.cad.Color;
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.WmfOptions;
```

## Krok 1: Načtěte výkres DXF

Načtěte výkres DXF, který chcete exportovat do formátu WMF. Ujistěte se, že je správně zadána cesta k souboru DXF.

```java
// Cesta k adresáři prostředků.
String dataDir = "Your Document Directory" + "DXFDrawings/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

## Krok 2: Nakonfigurujte možnosti rastrování

Nakonfigurujte možnosti rasterizace a definujte šířku a výšku výstupní stránky. V tomto příkladu nastavíme šířku a výšku stránky na 100 jednotek.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(100);
rasterizationOptions.setPageHeight(100);
WmfOptions wmfOptions = new WmfOptions();
```

## Krok 3: Uložte jako WMF

Uložte načtený výkres DXF jako formát WMF pomocí nakonfigurovaných možností.

```java
cadImage.save(dataDir+" example.ifc.wmf", wmfOptions);
```

## Krok 4: Zlikvidujte zdroje

Zlikvidujte prostředky, abyste uvolnili paměť a zajistili efektivní správu zdrojů.

```java
finally
{
  cadImage.dispose();
}
```

## Krok 5: Export do PDF

Volitelně exportujte výkres DXF do formátu PDF pomocí Aspose.CAD.

```java
image.save(dataDir + "conic_pyramid_out_.pdf"); 
```

Gratulujeme! Úspěšně jste exportovali výkres DXF do formátu WMF pomocí Aspose.CAD for Java.

## Závěr

V tomto tutoriálu jsme prozkoumali proces použití Aspose.CAD pro Java k exportu výkresů DXF do formátu WMF. Díky svým komplexním funkcím a snadnému použití poskytuje Aspose.CAD spolehlivé řešení pro práci se soubory CAD v projektech Java.

## FAQ

### Q1: Kde najdu dokumentaci Aspose.CAD?

 A1: Máte přístup k dokumentaci[tady](https://reference.aspose.com/cad/java/).

### Q2: Jak si stáhnu Aspose.CAD pro Java?

 A2: Stáhněte si knihovnu[tady](https://releases.aspose.com/cad/java/).

### Q3: Je k dispozici bezplatná zkušební verze?

A3: Ano, můžete získat bezplatnou zkušební verzi[tady](https://releases.aspose.com/).

### Q4: Potřebujete dočasné možnosti licencování?

 A4: Prozkoumejte dočasné licence[tady](https://purchase.aspose.com/temporary-license/).

### Q5: Kde mohu získat podporu?

 A5: Navštivte fórum podpory Aspose.CAD[tady](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
