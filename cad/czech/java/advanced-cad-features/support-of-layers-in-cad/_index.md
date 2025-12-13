---
date: 2025-12-13
description: Naučte se, jak uložit CAD jako JPEG v Javě pomocí Aspose.CAD, přidat
  více vrstev a upravit rozměry CAD pro přesnou konverzi obrázku.
linktitle: Support of Layers in CAD
second_title: Aspose.CAD Java API
title: Uložit CAD jako JPEG s podporou vrstev v Javě
url: /cs/java/advanced-cad-features/support-of-layers-in-cad/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Uložení CAD jako JPEG s podporou vrstev v Javě

## Úvod

V tomto tutoriálu se dozvíte, jak **uložit CAD jako JPEG** a plně využít podporu vrstev v Aspose.CAD pro Java. Vrstvy vám umožňují izolovat konkrétní části výkresu, což usnadňuje exportovat jen to, co potřebujete. Provedeme vás každým krokem, od nastavení prostředí až po export JPEG, který obsahuje pouze vybrané vrstvy.

## Rychlé odpovědi
- **Co znamená „uložit CAD jako JPEG“?** Převádí CAD výkres na rastrový JPEG obrázek.
- **Mohu zahrnout jen vybrané vrstvy?** Ano – použijte metodu `setLayers` k určení, které vrstvy se mají vykreslit.
- **Jak změním velikost obrázku?** Upravit `setPageWidth` a `setPageHeight` v `CadRasterizationOptions`.
- **Je to řešení jen pro Javu?** Příklad používá Aspose.CAD pro Java, ale stejné koncepty platí i pro jiné jazyky.
- **Potřebuji licenci?** Pro testování stačí bezplatná zkušební verze; pro produkci je vyžadována komerční licence.

## Předpoklady

Než začnete, ujistěte se, že máte následující:

1. **Aspose.CAD pro Java knihovna** – stáhněte ji z [webu](https://releases.aspose.com/cad/java/). Postupujte podle instalačního průvodce a přidejte JAR soubory do classpath vašeho projektu.  
2. **Vývojové prostředí Java** – nainstalovaný aktuální JDK (8 nebo novější) na vašem počítači.

Nyní, když je vše připraveno, podíváme se na kód potřebný k **uložení CAD jako JPEG** s výběrem vrstev při vykreslování.

## Import Namespaces

Začněte importováním požadovaných tříd Aspose.CAD a standardních utilit Java:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;
```

## Průvodce krok za krokem

### Krok 1: Nastavení cest k souborům

Definujte, kde se nachází zdrojový soubor DWF a kam se má výstupní JPEG zapsat.

```java
String dataDir = "Your Document Directory" + "DWFDrawings/";
String srcFile = dataDir + "for_layers_test.dwf";
String outFile = dataDir + "for_layers_test.jpg";
```

### Krok 2: Načtení DWF obrázku

Použijte metodu `Image.load` z Aspose.CAD k načtení CAD výkresu.

```java
Image image = Image.load(srcFile);
```

### Krok 3: Konfigurace možností rasterizace (úprava rozměrů CAD)

Vytvořte instanci `CadRasterizationOptions` a nastavte požadovanou velikost výstupu. Změna těchto hodnot vám umožní **upravit rozměry CAD** pro finální JPEG.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

### Krok 4: Specifikace vrstev (přidání více vrstev)

Pokud chcete vykreslit více než jednu vrstvu, jednoduše přidejte jejich názvy do seznamu. Zde začínáme s jednou vrstvou nazvanou „LayerA“.

```java
List<String> stringList = new ArrayList<>(Arrays.asList("LayerA"));
rasterizationOptions.setLayers(stringList);
```

*Tip:* Pro **přidání více vrstev** rozšiřte volání `Arrays.asList`, např. `Arrays.asList("LayerA", "LayerB", "LayerC")`.

### Krok 5: Konfigurace JPEG možností (Java převod CAD obrázku)

Propojte nastavení rasterizace s výstupním formátem JPEG.

```java
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Krok 6: Export do JPG (Uložení CAD jako JPEG)

Nakonec zapište obrázek na disk. Tento krok **uloží CAD výkres jako JPEG** soubor, který obsahuje pouze vybrané vrstvy.

```java
image.save(outFile, jpegOptions);
```

Dodržením těchto kroků jste úspěšně **uložili CAD jako JPEG** a zároveň ovládali, které vrstvy se zobrazí, a přizpůsobili rozměry obrázku.

## Časté problémy a řešení

| Problém | Řešení |
|---------|--------|
| **Vrstvy se nezobrazují** | Ověřte, že názvy vrstev přesně odpovídají tomu, co je uloženo v souboru DWF (rozlišují se velká a malá písmena). |
| **Výstupní obrázek je prázdný** | Ujistěte se, že `setPageWidth` a `setPageHeight` jsou dostatečně velké pro rozsah výkresu. |
| **Výjimka licence** | Pro testování použijte zkušební licenci; pro produkční prostředí zakupte plnou licenci. |

## Často kladené otázky

**Q: Mohu přidat více vrstev do možností rasterizace?**  
A: Rozhodně. Rozšiřte `stringList` o další názvy vrstev, např. `Arrays.asList("LayerA", "LayerB")`.

**Q: Je Aspose.CAD kompatibilní s jinými formáty CAD?**  
A: Ano, podporuje DWG, DXF, DWF a mnoho dalších formátů.

**Q: Jak mohu změnit rozměry výstupního obrázku?**  
A: Upravte `setPageWidth` a `setPageHeight` v instanci `CadRasterizationOptions`.

**Q: Kde si mohu zakoupit licenci pro Aspose.CAD?**  
A: Možnosti licencování můžete prozkoumat [zde](https://purchase.aspose.com/buy).

**Q: Kde mohu získat podporu komunity?**  
A: Připojte se ke komunitě Aspose.CAD na [fóru](https://forum.aspose.com/c/cad/19) pro pomoc a diskuze.

---

**Poslední aktualizace:** 2025-12-13  
**Testováno s:** Aspose.CAD pro Java 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}