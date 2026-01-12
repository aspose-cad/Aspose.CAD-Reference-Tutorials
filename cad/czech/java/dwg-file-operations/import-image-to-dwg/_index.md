---
date: 2026-01-12
description: Naučte se, jak přidat obrázek do souborů DWG pomocí Aspose.CAD pro Javu
  a také převést DWG do PDF. Postupujte podle našeho krok za krokem průvodce pro efektivní
  vývoj.
linktitle: Import Image to DWG File Using Java
second_title: Aspose.CAD Java API
title: Přidejte obrázek do DWG souborů bez námahy pomocí Aspose.CAD Java
url: /cs/java/dwg-file-operations/import-image-to-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Přidejte obrázek do souborů DWG snadno pomocí Aspose.CAD Java

V moderních Java aplikacích je **přidání obrázku do DWG** souborů běžnou požadavkou — ať už vytváříte CAD prohlížeč, automatizujete aktualizace výkresů nebo generujete dokumentaci. Aspose.CAD pro Java vám poskytuje jednoduchý, vysoce výkonný způsob, jak vložit rastrové obrázky přímo do DWG výkresů bez nutnosti kompletního CAD enginu. V tomto tutoriálu vás provedeme celým procesem, od načtení DWG až po export výsledku jako PDF.

## Rychlé odpovědi
- **Jaká knihovna je potřeba?** Aspose.CAD pro Java  
- **Mohu také exportovat do PDF?** Ano – použijte `PdfOptions` s `CadRasterizationOptions`  
- **Potřebuji licenci pro vývoj?** Bezplatná zkušební verze funguje pro testování; pro produkci je vyžadována komerční licence  
- **Jaká verze Javy je podporována?** Java 8 a vyšší  
- **Jak dlouho trvá implementace?** Přibližně 10‑15 minut pro základní import obrázku

## Co znamená „přidat obrázek do dwg“?
Přidání obrázku do souboru DWG znamená vložení rastrového obrázku (PNG, JPEG, atd.) jako objektu `CadRasterImage` do modelového prostoru výkresu. Obrázek se stane součástí stromu CAD entit a může být umístěn, měněn měřítkem i ořezán stejně jako jakýkoli jiný CAD objekt.

## Proč použít Aspose.CAD pro Java k přidání obrázku do dwg?
- **Není vyžadován žádný CAD software** – API interně zpracovává parsování DWG.  
- **Detailní kontrola** nad bodem vložení, vektory škálování a ořezáváním.  
- **Vestavěná konverze do PDF**, takže můžete vygenerovat tisknutelný PDF ve stejném workflow.  
- **Cross‑platform** – funguje na Windows, Linuxu i macOS.

## Předpoklady
- Aspose.CAD pro Java: Ujistěte se, že máte nainstalovanou knihovnu Aspose.CAD. Můžete si ji stáhnout [zde](https://releases.aspose.com/cad/java/).  
- Vývojové prostředí Java: JDK 8+ s vaším oblíbeným IDE (IntelliJ, Eclipse, VS Code, atd.).

## Import Packages
```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.*;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Krok‑za‑krokem průvodce

### Krok 1: Načtěte soubor DWG
Nejprve odkažte na složku, která obsahuje váš výkres DWG, a načtěte jej pomocí `Image.load`.
```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Drawing11.dwg";
Image image = Image.load(srcFile);
```

### Krok 2: Definujte definici rastrového obrázku
Vytvořte `CadRasterImageDef`, který odkazuje na externí PNG, který chcete vložit. Konstruktor přijímá název souboru obrázku a jeho rozměry v pixelech.
```java
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.setObjectHandle("A3B4");
```

### Krok 3: Nastavte bod vložení a vektory škálování
Bod vložení určuje, kde se objeví levý dolní roh obrázku. Vektory **U** a **V** řídí horizontální a vertikální škálování.
```java
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

### Krok 4: Vytvořte objekt CadRasterImage
Spojte definici, bod vložení a vektory do `CadRasterImage`. Můžete také nastavit ořezové hranice, pokud chcete zobrazit jen část obrázku.
```java
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.setImageDefReference("A3B4");
cadRasterImage.setDisplayFlags((short)7);
cadRasterImage.setClippingState((short)0);
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(639.5, 561.5));
```

### Krok 5: Přidejte obrázek do Model Space
Vložte rastrový obrázek do bloku `*Model_Space` a poté aktualizujte kolekci objektů výkresu, aby byla definice uložena.
```java
CadImage cadImage = ((CadImage)(image));
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(cadRasterImage);
CadBaseObject[] objs = cadImage.getObjects();
CadBaseObject[] arr = new CadBaseObject[objs.length + 1];
int ind = 0;
for (CadBaseObject obj : objs)
{
    arr[ind] = obj;
    ind++;
}
arr[ind] = cadRasterImageDef;
cadImage.setObjects(arr);
```

### Krok 6: Nakonfigurujte možnosti exportu do PDF (volitelné)
Pokud potřebujete také PDF verzi výkresu, nakonfigurujte `PdfOptions` spolu s `CadRasterizationOptions`. Tento krok ukazuje, jak **převést dwg na pdf** ve stejném postupu.
```java
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

### Krok 7: Uložte výsledné PDF
Nakonec exportujte upravený výkres jako PDF soubor. Používá se stejná instance `image`, takže PDF odráží nově přidaný rastrový obrázek.
```java
image.save((srcFile + "_generated.pdf"), pdfOptions);
```

Po provedení těchto kroků můžete rychle **přidat obrázek do dwg** souborů a také **uložit dwg jako pdf**, pokud je to potřeba.

## Časté problémy a řešení
- **Obrázek se nezobrazuje** – Ověřte, že cesta k souboru obrázku (`road-sign-custom.png`) je správná a že rozměry obrázku odpovídají hodnotám předaným do `CadRasterImageDef`.  
- **Nesprávné škálování** – Upravte vektory U a V; představují jednotky výkresu na pixel.  
- **PDF vypadá prázdně** – Ujistěte se, že `CadRasterizationOptions.setDrawType` je nastaven na `UseObjectColor` nebo jiný vhodný režim.

## Často kladené otázky

**Q: Je Aspose.CAD pro Java kompatibilní se všemi vývojovými prostředími Java?**  
A: Ano, Aspose.CAD pro Java je kompatibilní s většinou vývojových prostředí Java.

**Q: Mohu použít Aspose.CAD pro Java pro komerční projekty?**  
A: Ano, můžete použít Aspose.CAD pro Java pro komerční projekty. Podrobnosti o licencování najdete [zde](https://purchase.aspose.com/buy).

**Q: Je k dispozici bezplatná zkušební verze Aspose.CAD pro Java?**  
A: Ano, bezplatnou zkušební verzi můžete získat [zde](https://releases.aspose.com/).

**Q: Jak mohu získat podporu pro Aspose.CAD pro Java?**  
A: Podporu můžete získat na [fóru Aspose.CAD](https://forum.aspose.com/c/cad/19).

**Q: Mohu získat dočasnou licenci pro Aspose.CAD pro Java?**  
A: Ano, dočasnou licenci můžete získat [zde](https://purchase.aspose.com/temporary-license/).

---

**Poslední aktualizace:** 2026-01-12  
**Testováno s:** Aspose.CAD pro Java 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}