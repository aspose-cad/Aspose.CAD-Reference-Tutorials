---
date: 2026-05-20
description: Zjistěte, jak přidat obrázek do souborů DWG pomocí Aspose.CAD pro Java
  a také převést DWG na PDF. Postupujte podle našeho průvodce krok za krokem pro efektivní
  vývoj.
keywords:
- add image to dwg
- convert dwg to pdf
- import image into dwg
- embed raster image dwg
- dwg file operations
linktitle: Import obrázku do souboru DWG pomocí Java
schemas:
- author: Aspose
  dateModified: '2026-05-20'
  description: Learn how to add image to DWG files using Aspose.CAD for Java and also
    convert DWG to PDF. Follow our step-by-step guide for efficient development.
  headline: Add Image to DWG Files Effortlessly Using Aspose.CAD Java
  type: TechArticle
- description: Learn how to add image to DWG files using Aspose.CAD for Java and also
    convert DWG to PDF. Follow our step-by-step guide for efficient development.
  name: Add Image to DWG Files Effortlessly Using Aspose.CAD Java
  steps:
  - name: Load the DWG File
    text: First, point to the folder that contains your DWG drawing and load it with
      `Image.load`.
  - name: Define the Raster Image Definition
    text: The `CadRasterImageDef` class defines the external raster image resource
      to be embedded in the drawing.
  - name: Set Insertion Point and Scaling Vectors
    text: The insertion point determines where the lower‑left corner of the image
      will appear. The **U** and **V** vectors control horizontal and vertical scaling.
  - name: Create the CadRasterImage Object
    text: The `CadRasterImage` entity represents a raster picture placed in the DWG
      model space.
  - name: Add the Image to Model Space
    text: Insert the raster image into the `*Model_Space` block, then update the drawing’s
      object collection so the definition is saved.
  - name: Configure PDF Export Options (Optional)
    text: '`PdfOptions` specifies settings for saving a CAD drawing as a PDF file.
      `CadRasterizationOptions` defines how the CAD content is rasterized during PDF
      conversion.'
  - name: Save the Resulting PDF
    text: 'Finally, export the modified drawing as a PDF file. The same `image` instance
      is used, so the PDF reflects the newly added raster image. By following these
      steps, you can **add image to dwg** files quickly and also **save dwg as pdf**
      when needed, covering the most common **dwg file operations** in '
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD for Java works with any IDE that supports JDK 8+, including
      IntelliJ IDEA, Eclipse, and VS Code.
    question: Is Aspose.CAD for Java compatible with all Java development environments?
  - answer: Yes, you can use Aspose.CAD for Java for commercial projects. Visit **[here](https://purchase.aspose.com/buy)**
      for licensing details.
    question: Can I use Aspose.CAD for Java for commercial projects?
  - answer: Yes, you can access the free trial **[here](https://releases.aspose.com/)**.
    question: Is there a free trial available for Aspose.CAD for Java?
  - answer: You can seek support on the **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)**.
    question: How can I get support for Aspose.CAD for Java?
  - answer: Yes, you can get a temporary license **[here](https://purchase.aspose.com/temporary-license/)**.
    question: Can I obtain a temporary license for Aspose.CAD for Java?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Jednoduše přidejte obrázek do souborů DWG pomocí Aspose.CAD Java
url: /cs/java/dwg-file-operations/import-image-to-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Přidání obrázku do souborů DWG snadno pomocí Aspose.CAD Java

V moderních Java aplikacích je **přidání obrázku do DWG** souborů běžnou požadavkem — ať už vytváříte CAD prohlížeč, automatizujete aktualizace výkresů nebo generujete dokumentaci. Aspose.CAD pro Java vám poskytuje jednoduchý, vysoce výkonný způsob, jak vložit rastrové obrázky přímo do DWG výkresů bez nutnosti kompletního CAD enginu. V tomto tutoriálu vás provedeme celým procesem, od načtení DWG až po export výsledku jako PDF, a také ukážeme, jak **importovat obrázek do dwg** a **převést dwg na pdf** v jednom workflow.

## Rychlé odpovědi
- **Jaká knihovna je potřeba?** Aspose.CAD for Java  
- **Mohu také exportovat do PDF?** Ano – použijte `PdfOptions` s `CadRasterizationOptions`  
- **Potřebuji licenci pro vývoj?** Bezplatná zkušební verze funguje pro testování; pro produkci je vyžadována komerční licence  
- **Která verze Javy je podporována?** Java 8 a vyšší  
- **Jak dlouho trvá implementace?** Přibližně 10‑15 minut pro základní import obrázku  

## Co je „přidání obrázku do dwg“?

Přidání obrázku do souboru DWG znamená vložení rastrového obrázku (PNG, JPEG atd.) jako entity **CadRasterImage** do modelového prostoru výkresu, kde může být umístěn, měněn měřítkem a volitelně oříznut stejně jako jakýkoli jiný CAD objekt. Je uložen v tabulce objektů výkresu a zobrazen standardními CAD prohlížeči.

## Proč použít Aspose.CAD pro Java k přidání obrázku do dwg?

Můžete vkládat rastrovou grafiku do souborů DWG bez instalace jakéhokoli CAD softwaru třetí strany a API vám poskytuje pixelově přesnou kontrolu nad bodem vložení, vektory měřítka a ořezovými hranicemi. Aspose.CAD zpracovává soubory až do velikosti 2 GB, podporuje **více než 50 vstupních a výstupních formátů** a běží na Windows, Linuxu i macOS, což vám umožní integrovat manipulaci s CAD do libovolného backendu založeného na Javě.

## Předpoklady
- **Aspose.CAD pro Java** – stáhněte nejnovější JAR z oficiálního webu **[zde](https://releases.aspose.com/cad/java/)**.  
- **Java Development Kit** – JDK 8 nebo novější, s vaším preferovaným IDE (IntelliJ IDEA, Eclipse, VS Code atd.).  
- Platná **licence Aspose.CAD** pro produkční použití (zkušební verze funguje pro experimentování).  

## Import balíčků
Následující importy přinášejí nezbytné třídy Aspose.CAD používané pro manipulaci s obrázky a konverzi do PDF.  
```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.*;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Průvodce krok za krokem

### Krok 1: Načtení souboru DWG
Nejprve uveďte složku, která obsahuje váš výkres DWG, a načtěte jej pomocí `Image.load`.  
```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Drawing11.dwg";
Image image = Image.load(srcFile);
```

### Krok 2: Definice rastrového obrázku
Třída `CadRasterImageDef` definuje externí rastrový obrázkový zdroj, který bude vložen do výkresu.  
```java
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.setObjectHandle("A3B4");
```

### Krok 3: Nastavení bodu vložení a vektorů měřítka
Bod vložení určuje, kde se objeví levý dolní roh obrázku. Vektory **U** a **V** řídí horizontální a vertikální měřítko.  
```java
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

### Krok 4: Vytvoření objektu CadRasterImage
Entita `CadRasterImage` představuje rastrový obrázek umístěný v modelovém prostoru DWG.  
```java
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.setImageDefReference("A3B4");
cadRasterImage.setDisplayFlags((short)7);
cadRasterImage.setClippingState((short)0);
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(639.5, 561.5));
```

### Krok 5: Přidání obrázku do modelového prostoru
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

### Krok 6: Nastavení možností exportu do PDF (volitelné)
`PdfOptions` určuje nastavení pro uložení CAD výkresu jako PDF souboru. `CadRasterizationOptions` definuje, jak je obsah CAD během konverze do PDF rasterizován.  
```java
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

### Krok 7: Uložení výsledného PDF
Nakonec exportujte upravený výkres jako PDF soubor. Používá se stejná instance `image`, takže PDF odráží nově přidaný rastrový obrázek.  
```java
image.save((srcFile + "_generated.pdf"), pdfOptions);
```

Podle těchto kroků můžete rychle **přidat obrázek do dwg** souborů a také **uložit dwg jako pdf**, když je to potřeba, čímž pokryjete nejčastější **operace se soubory dwg** v jedné kompaktní rutině.

## Časté problémy a řešení
- **Obrázek se nezobrazuje** – Ověřte, že cesta k souboru obrázku (`road-sign-custom.png`) je správná a že rozměry obrázku odpovídají hodnotám předaným do `CadRasterImageDef`.  
- **Nesprávné měřítko** – Upravte vektory U a V; představují jednotky výkresu na pixel.  
- **PDF vypadá prázdně** – Ujistěte se, že `CadRasterizationOptions.setDrawType` je nastaven na `UseObjectColor` nebo jiný vhodný režim.  

## Často kladené otázky

**Q: Je Aspose.CAD pro Java kompatibilní se všemi vývojovými prostředími Java?**  
A: Ano, Aspose.CAD pro Java funguje s jakýmkoli IDE, které podporuje JDK 8+, včetně IntelliJ IDEA, Eclipse a VS Code.

**Q: Mohu použít Aspose.CAD pro Java pro komerční projekty?**  
A: Ano, můžete použít Aspose.CAD pro Java pro komerční projekty. Navštivte **[zde](https://purchase.aspose.com/buy)** pro podrobnosti o licencování.

**Q: Je k dispozici bezplatná zkušební verze Aspose.CAD pro Java?**  
A: Ano, bezplatnou zkušební verzi můžete získat **[zde](https://releases.aspose.com/)**.

**Q: Jak mohu získat podporu pro Aspose.CAD pro Java?**  
A: Podporu můžete získat na **[fóru Aspose.CAD](https://forum.aspose.com/c/cad/19)**.

**Q: Mohu získat dočasnou licenci pro Aspose.CAD pro Java?**  
A: Ano, dočasnou licenci můžete získat **[zde](https://purchase.aspose.com/temporary-license/)**.

---

**Poslední aktualizace:** 2026-05-20  
**Testováno s:** Aspose.CAD for Java 24.11  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Související tutoriály

- [Export DWG do PDF nebo rastrového formátu pomocí Aspose.CAD pro Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Přidání vlastních vlastností do souborů DWG pomocí Aspose.CAD pro Java](/cad/java/additional-features/add-custom-properties/)
- [Uložení CAD jako PNG – Konverze CAD výkresu do rastrového formátu pomocí Aspose.CAD pro Java](/cad/java/cad-drawing-conversion/convert-cad-drawing-to-raster-image/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}