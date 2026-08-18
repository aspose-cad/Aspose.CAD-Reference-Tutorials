---
date: 2026-02-28
description: Naučte se, jak vytvořit PDF z DWG, uložit DWG jako PDF a přidat text
  do výkresů DWG pomocí Aspose.CAD pro Javu – krok za krokem průvodce.
linktitle: Add Text in DWG
second_title: Aspose.CAD Java API
title: Vytvořte PDF z DWG a přidejte text pomocí Aspose.CAD pro Java
url: /cs/java/cad-text-and-annotation/add-text-in-dwg/
weight: 10
---

.CAD for Java". Similarly other links.

Also bullet points: "Can I convert DWG to PDF in Java?" translate.

Make sure not to translate code block placeholders.

Proceed.

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Vytvoření PDF z DWG a přidání textu pomocí Aspose.CAD pro Java

## Úvod

Pokud potřebujete **vytvořit PDF z DWG** souborů a zároveň vložit vlastní text, jste na správném místě. V tomto tutoriálu projdeme celý proces – načtení DWG výkresu, přidání textové anotace a nakonec uložení výsledku jako PDF pomocí Aspose.CAD pro Java. Na konci pochopíte, jak **uložit DWG jako PDF**, přizpůsobit výšku textu a dokonce přidat základní anotace.

## Rychlé odpovědi
- **Mohu v Javě převést DWG na PDF?** Ano, Aspose.CAD pro Java poskytuje jednoduché API.  
- **Potřebuji licenci pro produkční použití?** Vyžaduje se komerční licence; k dispozici je bezplatná zkušební verze.  
- **Která metoda přidává text do DWG?** Použijte objekt `CadText` a přidejte jej do modelového prostoru.  
- **Mohu nastavit výšku textu?** Samozřejmě – použijte `setTextHeight()` na instanci `CadText`.  
- **Je výstup vektorový?** Když jsou rasterizační možnosti nastaveny na `UseObjectColor`, PDF zachová vysoce kvalitní vektorová data.

## Co znamená „vytvořit PDF z DWG“?
Vytvoření PDF z DWG výkresu znamená převod nativního CAD formátu do široce podporovaného, pouze ke čtení určeného dokumentu při zachování původné geometrie. Tento převod je nezbytný, když potřebujete sdílet návrhy se zainteresovanými stranami, které nemají CAD software.

## Proč použít Aspose.CAD pro Java k převodu DWG na PDF?
Aspose.CAD nabízí čistě Java řešení, které nevyžaduje žádnou externí instalaci CAD. Podporuje **převod DWG na PDF**, zachovává vektorovou věrnost a umožňuje programově přidávat anotace, jako jsou text, rozměry nebo vlastní grafika před samotným převodem.

## Předpoklady

Před zahájením tutoriálu se ujistěte, že máte splněny následující předpoklady:

- Knihovna Aspose.CAD pro Java: Stáhněte a nainstalujte knihovnu ze [stránky Aspose.CAD pro Java](https://releases.aspose.com/cad/java/).

- Java Development Kit (JDK): Ujistěte se, že máte nainstalovanou nejnovější verzi JDK.

- DWG výkres: Připravte DWG soubor, do kterého chcete přidat text.

## Import Namespaces

Ve svém Java kódu importujte potřebné jmenné prostory pro Aspose.CAD:

```java
import com.aspose.cad.Image;


import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Nyní rozdělíme ukázkový kód do několika kroků:

## Krok 1: Nastavení adresáře dokumentu a cesty k DWG souboru

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

## Krok 5: Nastavení PDF možností (příprava na vytvoření PDF z DWG)

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

Dodržením těchto kroků budete schopni **vytvořit PDF z DWG**, přidat vlastní text a řídit výšku textu – vše jen několika řádky Java kódu.

## Jak převést DWG na PDF v Javě ve velkém měřítku?
Pokud potřebujete **hromadně převádět DWG PDF** soubory, zabalte výše uvedený kód do smyčky, která projde složku s DWG výkresy. `pageHeight`/`pageWidth` upravujte jen v případě potřeby, aby se snížila spotřeba paměti, a pro každý soubor znovu použijte stejnou instanci `PdfOptions` pro zlepšení výkonu.

## Časté problémy a tipy

- **Text se nezobrazuje?** Ověřte, že souřadnice X/Y jsou v rozsahu výkresu a že vrstva je viditelná.
- **Nesprávná výška textu?** Upravte `setTextHeight()`; hodnota je v jednotkách výkresu.
- **PDF vypadá rasterizovaně?** Ujistěte se, že je nastaven `CadDrawTypeMode.UseObjectColor`, aby se zachovaly vektorové informace.
- **Výkon u velkých souborů?** Zvětšujte `pageHeight`/`pageWidth` jen podle potřeby; vyšší hodnoty spotřebují více paměti.

## Často kladené otázky

**Q: Je Aspose.CAD kompatibilní se všemi verzemi DWG souborů?**  
A: Aspose.CAD podporuje různé verze DWG souborů, což zajišťuje kompatibilitu s širokou škálou CAD softwaru.

**Q: Mohu přizpůsobit font a formátování přidaného textu?**  
A: Ano, můžete přizpůsobit font, styl a další formátovací možnosti textu přidaného do DWG souborů pomocí Aspose.CAD.

**Q: Je k dispozici bezplatná zkušební verze Aspose.CAD pro Java?**  
A: Ano, funkce Aspose.CAD můžete vyzkoušet získáním bezplatné zkušební verze [zde](https://releases.aspose.com/).

**Q: Kde najdu podrobnou dokumentaci k Aspose.CAD pro Java?**  
A: Podrobnou dokumentaci najdete [zde](https://reference.aspose.com/cad/java/).

**Q: Jak získám podporu nebo pomoc s Aspose.CAD?**  
A: Navštivte [forum Aspose.CAD](https://forum.aspose.com/c/cad/19), kde získáte pomoc a spojíte se s komunitou.

---

**Poslední aktualizace:** 2026-02-28  
**Testováno s:** Aspose.CAD pro Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}