---
date: 2025-12-28
description: Naučte se, jak vytvořit PDF z DWG, uložit DWG jako PDF a přidat text
  do výkresů DWG pomocí Aspose.CAD pro Javu – krok za krokem průvodce.
linktitle: Add Text in DWG
second_title: Aspose.CAD Java API
title: Vytvořte PDF z DWG a přidejte text pomocí Aspose.CAD pro Java
url: /cs/java/cad-text-and-annotation/add-text-in-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Vytvoření PDF ze souboru DWG a přidání textu pomocí Aspose.CAD pro Java

## Úvod

Pokud potřebujete **vytvořit PDF ze souboru DWG** a zároveň vložit vlastní text, jste na správném místě. V tomto tutoriálu vás provedeme celým procesem – načtením výkresu DWG, přidáním textové anotace a nakonec uložením výsledku jako PDF pomocí Aspose.CAD pro Java. Na konci pochopíte, jak **uložit DWG jako PDF**, přizpůsobit výšku textu a dokonce přidat základní anotace.

## Rychlé odpovědi
- **Mohu v Javě převést DWG na PDF?** Ano, Aspose.CAD pro Java poskytuje jednoduché API.  
- **Potřebuji licenci pro produkční použití?** Je vyžadována komerční licence; je k dispozici bezplatná zkušební verze.  
- **Která metoda přidává text do DWG?** Použijte objekt `CadText` a přidejte jej do modelového prostoru.  
- **Mohu nastavit výšku textu?** Samozřejmě – použijte `setTextHeight()` na instanci `CadText`.  
- **Je výstup vektorový?** Když jsou nastaveny možnosti rasterizace na `UseObjectColor`, PDF si zachová vysoce kvalitní vektorová data.

## Požadavky

Než se ponoříte do tutoriálu, ujistěte se, že máte následující požadavky připravené:

- Aspose.CAD pro Java knihovna: Stáhněte a nainstalujte knihovnu ze stránky [Aspose.CAD for Java page](https://releases.aspose.com/cad/java/).
- Java Development Kit (JDK): Ujistěte se, že máte na svém systému nainstalovaný nejnovější JDK.
- DWG výkres: Připravte soubor DWG výkresu, do kterého chcete přidat text.

## Import jmenných prostorů

Ve vašem Java kódu importujte potřebné jmenné prostory pro Aspose.CAD:

```java
import com.aspose.cad.Image;


import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Nyní rozdělíme poskytnutý úryvek kódu do několika kroků:

## Krok 1: Nastavení adresáře dokumentu a cesty k souboru DWG

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String dwgPathToFile = dataDir + "SimpleEntites.dwg";
```

## Krok 2: Načtení DWG obrázku

```java
Image image = Image.load(dwgPathToFile);
```

## Krok 3: Vytvoření objektu CadText (přidání textu do DWG)

```java
CadText cadText = new CadText();
cadText.setStyleType("Standard");
cadText.setDefaultValue("Some custom text");
cadText.setColorId(256);
cadText.setLayerName("0");
cadText.getFirstAlignment().setX(47.9);
cadText.getFirstAlignment().setY(5.56);
cadText.setTextHeight(0.8);          // set text height in DWG units
cadText.setScaleX(0);
```

## Krok 4: Přidání textu do CadImage (vložit anotaci)

```java
CadImage cadImage = ((CadImage)(image));
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(cadText);
```

## Krok 5: Nastavení PDF možností (příprava na vytvoření PDF ze DWG)

```java
PdfOptions pdfOptions = new PdfOptions();
```

## Krok 6: Konfigurace CadRasterizationOptions (řízení vykreslování PDF)

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

## Krok 7: Uložení upraveného DWG jako PDF (dwg to pdf java)

```java
image.save(dataDir + "SimpleEntites_generated.dwg.pdf", pdfOptions);
```

Po provedení těchto kroků budete schopni **vytvořit PDF ze DWG**, přidat vlastní text a řídit výšku textu – vše pomocí několika řádků Java kódu.

## Proč přidávat text do DWG a převádět do PDF?

Přidání textu přímo do souboru DWG je užitečné pro:

- **Označování návrhů** poznámkami nebo čísly dílů.
- **Vytváření tisknutelné dokumentace**, kde PDF slouží jako jen pro čtení, široce podporovaný formát.
- **Automatizaci dávkového zpracování** velkých CAD knihoven bez ruční úpravy.

## Časté problémy a tipy

- **Text se nezobrazuje?** Ověřte, že souřadnice X/Y jsou v rozsahu výkresu a že vrstva je viditelná.
- **Nesprávná výška textu?** Upravte `setTextHeight()`; hodnota je v jednotkách výkresu.
- **PDF vypadá rasterizovaně?** Ujistěte se, že `CadDrawTypeMode.UseObjectColor` je nastaveno pro zachování vektorových informací.
- **Výkon u velkých souborů?** Zvyšte `pageHeight`/`pageWidth` jen podle potřeby; vyšší hodnoty spotřebují více paměti.

## Často kladené otázky

**Q: Je Aspose.CAD kompatibilní se všemi verzemi souborů DWG?**  
A: Aspose.CAD podporuje různé verze souborů DWG, což zajišťuje kompatibilitu s širokou škálou CAD softwaru.

**Q: Mohu přizpůsobit písmo a formátování přidaného textu?**  
A: Ano, můžete přizpůsobit písmo, styl a další možnosti formátování textu přidaného do souborů DWG pomocí Aspose.CAD.

**Q: Je k dispozici bezplatná zkušební verze pro Aspose.CAD pro Java?**  
A: Ano, můžete si vyzkoušet funkce Aspose.CAD získáním bezplatné zkušební verze [zde](https://releases.aspose.com/).

**Q: Kde mohu najít podrobnou dokumentaci pro Aspose.CAD pro Java?**  
A: Odkazujte na dokumentaci [zde](https://reference.aspose.com/cad/java/) pro podrobné informace a příklady.

**Q: Jak mohu získat podporu nebo pomoc s Aspose.CAD?**  
A: Navštivte [forum Aspose.CAD](https://forum.aspose.com/c/cad/19), kde získáte pomoc a spojíte se s komunitou.

---

**Last Updated:** 2025-12-28  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}