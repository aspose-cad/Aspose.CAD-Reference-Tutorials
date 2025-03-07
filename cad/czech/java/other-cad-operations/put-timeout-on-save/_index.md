---
title: Časový limit při ukládání pro CAD s Aspose.CAD
linktitle: Nastavte Timeout na Uložit
second_title: Aspose.CAD Java API
description: Naučte se, jak zvýšit výkon vaší Java aplikace pomocí Aspose.CAD. Nastavte časový limit pro ukládání výkresů CAD. Postupujte podle našeho podrobného průvodce.
weight: 15
url: /cs/java/other-cad-operations/put-timeout-on-save/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Časový limit při ukládání pro CAD s Aspose.CAD

## Úvod

Vítejte v tutoriálu o nastavení časového limitu při ukládání pomocí Aspose.CAD pro Java. V této příručce vás provedeme procesem nastavení časového limitu pro ukládání výkresů CAD, abyste zvýšili výkon vaší aplikace. Aspose.CAD for Java je výkonná knihovna, která vám umožní bezproblémově pracovat se soubory CAD ve vašich aplikacích Java.

## Předpoklady

Než se pustíte do výukového programu, ujistěte se, že máte splněny následující předpoklady:
-  Knihovna Aspose.CAD for Java: Ujistěte se, že máte do projektu integrovanou knihovnu Aspose.CAD for Java. Knihovnu si můžete stáhnout z[webová stránka](https://releases.aspose.com/cad/java/).
- Vývojové prostředí: Nastavte své vývojové prostředí Java se všemi potřebnými nástroji a závislostmi.

## Importujte balíčky

Chcete-li začít, importujte požadované balíčky do svého projektu Java. Na začátek souboru Java přidejte následující řádky:

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterruptionTokenSource;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.concurrent.TimeUnit;
```

Nyní si ukázkový kód rozdělíme na podrobné pokyny:

## Krok 1: Nastavte zdrojové a výstupní adresáře

```java
final String SourceDir = Utils.getDataDir_DWGDrawings();
final String OutputDir = Utils.getDataDir_Output();
```

Ujistěte se, že máte správné zdrojové a výstupní adresáře pro vaše CAD výkresy.

## Krok 2: Vytvořte zdroj tokenu přerušení

```java
final InterruptionTokenSource source = new com.aspose.cad.InterruptionTokenSource();
```

Inicializujte zdroj tokenu přerušení, abyste mohli spravovat přerušení během operace ukládání.

## Krok 3: Načtěte výkres CAD

```java
final CadImage cadImageBig = (CadImage)Image.load(SourceDir + "Drawing11.dwg");
```

 Načtěte výkres CAD do a`CadImage` objekt.

## Krok 4: Nakonfigurujte možnosti rastrování

```java
CadRasterizationOptions rasterizationOptionsBig = new CadRasterizationOptions();
rasterizationOptionsBig.setPageWidth(cadImageBig.getSize().getWidth() / 2);
rasterizationOptionsBig.setPageHeight(cadImageBig.getSize().getHeight() / 2);
```

Nakonfigurujte možnosti rastrování pro výkres CAD.

## Krok 5: Nakonfigurujte možnosti PDF

```java
final PdfOptions CADfBig = new PdfOptions();
CADfBig.setVectorRasterizationOptions(rasterizationOptionsBig);
CADfBig.setInterruptionToken(source.getToken());
```

Nastavte možnosti PDF s možnostmi vektorového rastrování a tokenu přerušení.

## Krok 6: Uložte výkres s časovým limitem

```java
cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
```

Uložte výkres CAD do souboru PDF se zadaným časovým limitem.

## Krok 7: Zvládněte přerušení

```java
java.lang.Thread thread = new java.lang.Thread(new Runnable() {
    @Override
    public void run() {
        try {
            cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
        } catch (Throwable th) {
            System.out.println("interrupted !!!");
        }
    }
});
thread.start();
TimeUnit.SECONDS.sleep(3);
source.interrupt();
thread.join();
```

Vytvořte vlákno pro zpracování operace uložení a přerušte ji po zadaném časovém limitu.

## Závěr

Gratulujeme! Úspěšně jste se naučili, jak nastavit časový limit při ukládání pomocí Aspose.CAD for Java. Tato funkce může výrazně zvýšit efektivitu vašich aplikací souvisejících s CAD.

## FAQ

### Q1: Jak si mohu stáhnout Aspose.CAD pro Java?

 A1: Můžete si jej stáhnout z[stránka vydání](https://releases.aspose.com/cad/java/).

### Q2: Kde najdu dokumentaci k Aspose.CAD for Java?

 A2: Viz[dokumentace](https://reference.aspose.com/cad/java/) pro komplexní informace.

### Q3: Je k dispozici bezplatná zkušební verze?

A3: Ano, můžete získat bezplatnou zkušební verzi[tento odkaz](https://releases.aspose.com/).

### Q4: Jak získám dočasnou licenci?

 A4: Návštěva[tady](https://purchase.aspose.com/temporary-license/) pro dočasné podrobnosti o licenci.

### Q5: Potřebujete pomoc nebo máte otázky?

 A5: Přejděte na[Fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) za podporu komunity.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
