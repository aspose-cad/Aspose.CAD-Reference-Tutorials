---
title: Export STL do PNG pomocí Aspose.CAD pro Javu
linktitle: Export STL do PNG
second_title: Aspose.CAD Java API
description: Prozkoumejte bezproblémový proces exportu souborů STL do PNG v Javě s Aspose.CAD. Zjednodušte si pracovní postup a bez námahy vylepšete své projekty Java.
weight: 20
url: /cs/java/cad-export-options/export-stl-to-png/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export STL do PNG pomocí Aspose.CAD pro Javu

## Úvod

Chcete exportovat soubory STL do PNG pomocí Java? Aspose.CAD for Java je řešení, které potřebujete! V tomto tutoriálu vás provedeme procesem krok za krokem. Jako zkušený SEO spisovatel zajistím, aby obsah byl nejen informativní, ale také optimalizovaný pro vyhledávače.

## Předpoklady

Než se pustíte do výukového programu, ujistěte se, že máte splněny následující předpoklady:

- Java Development Kit (JDK) nainstalovaný na vašem počítači.
-  Stažena knihovna Aspose.CAD pro Java. Můžeš to dostat[tady](https://releases.aspose.com/cad/java/).
-  Platná licence nebo dočasná licence od[tady](https://purchase.aspose.com/temporary-license/).

## Importovat jmenné prostory

Ve svém projektu Java importujte potřebné jmenné prostory:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Nyní si příklad rozdělíme do několika kroků.

## Krok 1: Nastavte svůj projekt

Vytvořte nový projekt Java a přidejte knihovnu Aspose.CAD for Java do závislostí vašeho projektu.

## Krok 2: Zadejte svůj soubor STL

Definujte cestu k souboru STL. Například:

```java
String dataDir = "Your Document Directory" + "ExportingSTL/";
String fileName = dataDir + "example.stl";
```

## Krok 3: Načtěte soubor STL

 Načtěte soubor STL pomocí`Image.load` metoda:

```java
CadImage cadImage = (CadImage)Image.load(fileName);
```

## Krok 4: Nakonfigurujte možnosti rastrování

Nastavte možnosti rasterizace pro vektorizaci:

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

## Krok 5: Nakonfigurujte možnosti PNG

Zadejte možnosti pro export PNG:

```java
PngOptions pngOptions = new PngOptions();
// Pokud chcete nastavit možnosti vektorové rastrování, odkomentujte řádek níže
// pngOptions.setVectorRasterizationOptions(vectorOptions);
```

## Krok 6: Uložte jako PNG

Uložte obrázek CAD jako soubor PNG:

```java
String outPath = dataDir + "galeon.stl.png";
cadImage.save(outPath, pngOptions);
```

Gratulujeme! Úspěšně jste exportovali soubor STL do PNG pomocí Aspose.CAD for Java.

## Závěr

V tomto tutoriálu jsme prozkoumali, jak využít Aspose.CAD pro Java k exportu souborů STL do PNG bez námahy. Tato výkonná knihovna zjednodušuje složité úkoly, což z ní činí cenný přínos pro vaše projekty Java.

## FAQ

### Q1: Je Aspose.CAD for Java kompatibilní se všemi verzemi souborů STL?

A1: Aspose.CAD for Java podporuje různé verze souborů STL, což zajišťuje kompatibilitu s většinou běžných formátů.

### Q2: Mohu použít Aspose.CAD for Java v komerčním projektu?

 A2: Ano, můžete. Stačí získat platnou licenci od[tady](https://purchase.aspose.com/buy).

### Otázka 3: Potřebuji pro bezplatnou zkušební verzi dočasnou licenci?

 A3: Ne, pro bezplatnou zkušební verzi není vyžadována dočasná licence. Můžete začít ihned se zkušební verzí[tady](https://releases.aspose.com/).

### Otázka 4: Kde mohu najít další podporu nebo se zeptat na něco?

 A4: Navštivte fórum Aspose.CAD[tady](https://forum.aspose.com/c/cad/19) pro jakoukoli podporu nebo dotazy.

### Q5: Je k dispozici nějaká komplexní dokumentace?

 A5: Ano, dokumentaci lze nalézt[tady](https://reference.aspose.com/cad/java/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
