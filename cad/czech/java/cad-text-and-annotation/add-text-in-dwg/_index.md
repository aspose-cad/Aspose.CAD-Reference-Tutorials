---
title: Přidejte text do DWG pomocí Aspose.CAD for Java
linktitle: Přidejte text do DWG
second_title: Aspose.CAD Java API
description: Vylepšete své DWG výkresy bez námahy pomocí Aspose.CAD pro Java. Přidejte text hladce pomocí našeho podrobného průvodce.
type: docs
weight: 10
url: /cs/java/cad-text-and-annotation/add-text-in-dwg/
---
## Úvod

V oblasti počítačově podporovaného navrhování (CAD) vyniká Aspose.CAD for Java jako výkonný nástroj pro manipulaci a konverzi výkresů DWG. Jednou z jeho užitečných funkcí je možnost bezproblémového přidávání textu do souborů DWG. V tomto tutoriálu vás provedeme procesem přidávání textu do výkresů DWG pomocí Aspose.CAD for Java.

## Předpoklady

Než se pustíte do výukového programu, ujistěte se, že máte splněny následující předpoklady:

-  Aspose.CAD for Java Library: Stáhněte a nainstalujte knihovnu z[Aspose.CAD pro stránku Java](https://releases.aspose.com/cad/java/).

- Java Development Kit (JDK): Ujistěte se, že máte v systému nainstalovanou nejnovější verzi JDK.

- Výkres DWG: Připravte soubor výkresu DWG, kam chcete přidat text.

## Importovat jmenné prostory

Do kódu Java importujte potřebné jmenné prostory pro Aspose.CAD:

```java
import com.aspose.cad.Image;


import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Nyní si rozdělíme poskytnutý fragment kódu do několika kroků:

## Krok 1: Nastavte adresář dokumentů a cestu k souboru DWG

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String dwgPathToFile = dataDir + "SimpleEntites.dwg";
```

## Krok 2: Načtěte obrázek DWG

```java
Image image = Image.load(dwgPathToFile);
```

## Krok 3: Vytvořte objekt CadText

```java
CadText cadText = new CadText();
cadText.setStyleType("Standard");
cadText.setDefaultValue("Some custom text");
cadText.setColorId(256);
cadText.setLayerName("0");
cadText.getFirstAlignment().setX(47.9);
cadText.getFirstAlignment().setY(5.56);
cadText.setTextHeight(0.8);
cadText.setScaleX(0);
```

## Krok 4: Přidejte text do CadImage

```java
CadImage cadImage = ((CadImage)(image));
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(cadText);
```

## Krok 5: Nastavte možnosti PDF

```java
PdfOptions pdfOptions = new PdfOptions();
```

## Krok 6: Nakonfigurujte CadRasterizationOptions

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

## Krok 7: Uložte upravený DWG jako PDF

```java
image.save(dataDir + "SimpleEntites_generated.dwg.pdf", pdfOptions);
```

Podle těchto kroků budete moci bez problémů přidávat text do svých výkresů DWG pomocí Aspose.CAD for Java.

## Závěr

Aspose.CAD for Java umožňuje vývojářům programově vylepšovat a upravovat výkresy DWG. Tento výukový program poskytuje jasného průvodce krok za krokem k přidávání textu do souborů DWG a ukazuje jednoduchost a sílu Aspose.CAD.

## FAQ

### Q1: Je Aspose.CAD kompatibilní se všemi verzemi souborů DWG?

A1: Aspose.CAD podporuje různé verze souborů DWG, což zajišťuje kompatibilitu s širokou škálou CAD softwaru.

### Q2: Mohu přizpůsobit písmo a formátování přidaného textu?

Odpověď 2: Ano, můžete upravit písmo, styl a další možnosti formátování pro text přidaný do souborů DWG pomocí Aspose.CAD.

### Q3: Je k dispozici bezplatná zkušební verze pro Aspose.CAD pro Javu?

 A3: Ano, můžete prozkoumat funkce Aspose.CAD získáním bezplatné zkušební verze od[tady](https://releases.aspose.com/).

### Q4: Kde najdu podrobnou dokumentaci k Aspose.CAD for Java?

 A4: Viz dokumentace[tady](https://reference.aspose.com/cad/java/) pro podrobné informace a příklady.

### Q5: Jak mohu získat podporu nebo vyhledat pomoc s Aspose.CAD?

A5: Navštivte[Fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) získat pomoc a spojit se s komunitou.