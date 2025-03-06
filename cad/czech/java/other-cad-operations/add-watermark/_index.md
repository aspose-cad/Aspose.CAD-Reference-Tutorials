---
title: Přidání vodoznaků do výkresů CAD - Výukový program Aspose.CAD for Java
linktitle: Přidat vodoznak
second_title: Aspose.CAD Java API
description: Vylepšete své CAD výkresy pomocí personalizovaných vodoznaků pomocí Aspose.CAD for Java. Postupujte podle našeho podrobného průvodce pro bezproblémovou integraci.
weight: 12
url: /cs/java/other-cad-operations/add-watermark/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Přidání vodoznaků do výkresů CAD - Výukový program Aspose.CAD for Java

## Úvod

Vítejte v této komplexní příručce o přidávání vodoznaků do výkresů CAD pomocí Aspose.CAD pro Java. V tomto tutoriálu se naučíte, jak efektivně integrovat vodoznaky, vylepšit vaše CAD dokumenty pomocí personalizovaných zpráv nebo brandingu. Aspose.CAD for Java poskytuje výkonnou sadu funkcí, díky nimž je proces přidávání vodoznaku přímočarý.

## Předpoklady

Než se pustíme do výukového programu, ujistěte se, že máte následující předpoklady:

-  Aspose.CAD for Java: Ujistěte se, že máte ve svém prostředí Java nainstalovanou knihovnu Aspose.CAD. Můžete si jej stáhnout[tady](https://releases.aspose.com/cad/java/).
- Java Development Kit (JDK): Ujistěte se, že máte v systému nainstalovanou nejnovější verzi JDK.

## Importujte balíčky

Ve svém projektu Java importujte potřebné balíčky Aspose.CAD, abyste mohli začít:

```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.Cad3DPoint;
import com.aspose.cad.fileformats.cad.cadobjects.CadMText;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Krok 1: Přidejte nový MTEXT

```java
//přidat nový MTEXT
CadMText watermark = new CadMText();
watermark.setText("Watermark message");
watermark.setInitialTextHeight(40);
watermark.setInsertionPoint(new Cad3DPoint(300, 40));
watermark.setLayerName("0");
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(watermark);
```

## Krok 2: Přidejte jednoduchou entitu jako text

Můžete také přidat přímočařejší entitu, jako je text:

```java
// nebo přidejte další jednoduchou entitu, jako je Text
CadText text = new CadText();
text.setDefaultValue("Watermark text");
text.setTextHeight(40);
text.setFirstAlignment(new Cad3DPoint(300, 40));
text.setLayerName("0") ;
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(text);
```

## Krok 3: Export do PDF

Exportujte výkres CAD s přidaným vodoznakem do souboru PDF:

```java
// exportovat do pdf
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setLayouts(new String[]{"Model"});
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
cadImage.save(dataDir + "AddWatermark_out.pdf", pdfOptions);

```

## Závěr

Gratulujeme! Úspěšně jste přidali vodoznaky do svých výkresů CAD pomocí Aspose.CAD for Java. Tento jednoduchý, ale výkonný proces vám umožňuje personalizovat vaše návrhy nebo je chránit pomocí značky.

## FAQ

### Q1: Je Aspose.CAD kompatibilní se všemi formáty souborů CAD?

Odpověď 1: Aspose.CAD podporuje různé formáty CAD, včetně DWG, DXF, DWT a DWF.

### Q2: Mohu přizpůsobit vzhled textu vodoznaku?

Odpověď 2: Ano, máte plnou kontrolu nad vzhledem vodoznaku, včetně velikosti textu, barvy a polohy.

### Q3: Je k dispozici zkušební verze pro Aspose.CAD pro Javu?

 A3: Ano, můžete si stáhnout zkušební verzi[tady](https://releases.aspose.com/).

### Q4: Jak mohu získat podporu pro Aspose.CAD?

 A4: Navštivte[Fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) za podporu komunity.

### Otázka 5: Kde najdu kompletní dokumentaci k Aspose.CAD for Java?

 A5: Viz[dokumentace](https://reference.aspose.com/cad/java/) pro podrobné informace.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
