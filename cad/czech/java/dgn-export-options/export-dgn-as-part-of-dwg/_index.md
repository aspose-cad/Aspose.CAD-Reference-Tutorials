---
title: Export DGN do DWG pomocí Aspose.CAD for Java
linktitle: Export DGN jako součást DWG
second_title: Aspose.CAD Java API
description: Prozkoumejte, jak exportovat DGN jako součást DWG pomocí Aspose.CAD for Java. Postupujte podle našeho podrobného průvodce pro efektivní manipulaci se soubory CAD.
weight: 10
url: /cs/java/dgn-export-options/export-dgn-as-part-of-dwg/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export DGN do DWG pomocí Aspose.CAD for Java

## Úvod

V tomto tutoriálu prozkoumáme, jak pomocí Aspose.CAD for Java exportovat soubor DGN (MicroStation Design) jako součást souboru DWG (Výkres AutoCAD). Aspose.CAD je výkonná knihovna, která poskytuje komplexní funkce pro práci s formáty souborů CAD. Tento podrobný průvodce vám pomůže pochopit proces exportu DGN jako součásti DWG pomocí Java.

## Předpoklady

Než se pustíme do výukového programu, ujistěte se, že máte splněny následující předpoklady:
1. Knihovna Aspose.CAD: Stáhněte a nainstalujte knihovnu Aspose.CAD pro Javu. Knihovnu najdete[tady](https://releases.aspose.com/cad/java/).
2. Java Development Kit (JDK): Ujistěte se, že máte v systému nainstalovanou Java.
3. Integrované vývojové prostředí (IDE): Vyberte si Java IDE jako Eclipse nebo IntelliJ pro hladší vývoj.

## Importujte balíčky

Do svého projektu Java importujte potřebné balíčky Aspose.CAD, abyste umožnili manipulaci se soubory CAD. Zde je příklad:

```java
import com.aspose.cad;
import com.aspose.cad.imageoptions;
import com.aspose.cad.fileformats.cad.cadconsts;
import com.aspose.cad.fileformats.cad;
import com.aspose.cad.fileformats.cad.cadobjects;
```

## Krok 1: Nastavte cesty k souboru

 Definujte vstupní a výstupní cesty k souboru DWG. Aktualizujte`dataDir`, `fileName` , a`outPath` proměnné podle toho.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
String outPath = dataDir + "BlockRefDgn.dwg.pdf";
```

## Krok 2: Vytvořte instanci PdfOptions

 Vytvořte instanci souboru`PdfOptions` třídy, protože exportujeme soubor DWG do formátu PDF.

```java
PdfOptions exportOptions = new PdfOptions();
```

## Krok 3: Načtěte soubor DWG

 Načtěte existující soubor DWG jako obrázek a převeďte jej na`CadImage` typ.

```java
CadImage cadImage = (CadImage) Image.load(fileName);
```

## Krok 4: Iterujte přes entity

Projděte každou entitu v souboru DWG a zkontrolujte, zda se jedná o definici obrázku. Pokud ano, načtěte externí odkaz na objekt.

```java
for (CadBaseEntity baseEntity : cadImage.getEntities()) {
    if (baseEntity.getTypeName() == CadEntityTypeName.DGNUNDERLAY) {
        CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
        System.out.println(dgnFile.getUnderlayPath());
    }
}
```

## Krok 5: Definujte možnosti rastrování

 Definujte nastavení pro`CadRasterizationOptions`objekt, včetně šířky stránky, výšky, rozvržení a barvy pozadí.

```java
CadRasterizationOptions vectorRasterizationOptions = new CadRasterizationOptions();
vectorRasterizationOptions.setPageWidth(1600);
vectorRasterizationOptions.setPageHeight(1600);
vectorRasterizationOptions.setLayouts(new String[] { "Model" });
vectorRasterizationOptions.setAutomaticLayoutsScaling(false);
vectorRasterizationOptions.setNoScaling(true);
vectorRasterizationOptions.setBackgroundColor(Color.getBlack());
vectorRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
```

## Krok 6: Nastavte možnosti vektorového rastrování

Nastavte možnosti vektorového rastrování pro export.

```java
exportOptions.setVectorRasterizationOptions(vectorRasterizationOptions);
```

## Krok 7: Export DWG do PDF

 Nakonec exportujte DWG do PDF voláním`save` metoda.

```java
cadImage.save(outPath, exportOptions);
```

## Závěr

Gratulujeme! Úspěšně jste se naučili, jak exportovat soubor DGN jako součást souboru DWG pomocí Aspose.CAD for Java. Tato výkonná knihovna poskytuje rozsáhlé možnosti pro práci se soubory CAD, díky čemuž jsou vaše úlohy manipulace se soubory CAD efektivní a přímočaré.

## FAQ

### Q1: Kde najdu dokumentaci k Aspose.CAD for Java?

 A1: Dokumentaci lze nalézt[tady](https://reference.aspose.com/cad/java/).

### Q2: Jak si mohu stáhnout knihovnu Aspose.CAD pro Java?

 A2: Knihovnu si můžete stáhnout z[tento odkaz](https://releases.aspose.com/cad/java/).

### Q3: Je k dispozici bezplatná zkušební verze pro Aspose.CAD pro Javu?

 A3: Ano, můžete najít bezplatnou zkušební verzi[tady](https://releases.aspose.com/).

### Q4: Kde mohu získat dočasnou licenci pro Aspose.CAD for Java?

 A4: Získejte dočasnou licenci[tady](https://purchase.aspose.com/temporary-license/).

### Q5: Potřebujete pomoc nebo máte otázky?

 A5: Navštivte fórum podpory komunity Aspose.CAD[tady](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
