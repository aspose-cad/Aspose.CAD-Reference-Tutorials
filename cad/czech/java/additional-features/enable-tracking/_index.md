---
title: Povolit sledování v souborech DWG pomocí Aspose.CAD v Javě
linktitle: Povolte sledování v souborech DWG pomocí Java
second_title: Aspose.CAD Java API
description: Prozkoumejte podrobného průvodce povolením sledování souborů DWG v Javě pomocí Aspose.CAD, který zajistí bezproblémovou spolupráci na projektech CAD.
weight: 12
url: /cs/java/additional-features/enable-tracking/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Povolit sledování v souborech DWG pomocí Aspose.CAD v Javě

## Úvod

V oblasti počítačově podporovaného navrhování (CAD) vyniká Aspose.CAD for Java jako výkonný nástroj, který umožňuje vývojářům snadno manipulovat a převádět soubory CAD. Tento tutoriál se ponoří do specifické funkce Aspose.CAD pro Java – umožňuje sledování v souborech DWG. Sledování změn v souborech DWG je zásadní pro projekty společného návrhu, zajišťuje bezproblémovou komunikaci a efektivní pracovní postup. V této příručce si projdeme kroky, jak povolit sledování pomocí Javy s využitím možností Aspose.CAD.

## Předpoklady

Než se pustíme do implementace, ujistěte se, že máte splněny následující předpoklady:

- Java Development Kit (JDK): Ujistěte se, že máte v systému nainstalovanou Java.
-  Aspose.CAD for Java: Stáhněte a nainstalujte Aspose.CAD for Java z[odkaz ke stažení](https://releases.aspose.com/cad/java/).
- Adresář dokumentů: Připravte si adresář, kde jsou umístěny vaše soubory DWG.

## Importovat jmenné prostory

Ve svém projektu Java začněte importem potřebných jmenných prostorů pro využití funkcí Aspose.CAD:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.CadRenderResult;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.RenderResult;
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
```

## Krok 1: Načtěte soubor DWG

Začněte načtením souboru DWG do vaší Java aplikace. Podle toho upravte cestu k souboru:

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## Krok 2: Nakonfigurujte možnosti exportu PDF

Nakonfigurujte možnosti exportu PDF a určete možnosti vektorového rastrování pro CAD:

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);
cadRasterizationOptions.setPageHeight(600);
```

## Krok 3: Implementujte sledování

Implementujte sledování pomocí vlastní třídy obsluhy chyb. Tato třída bude zpracovávat výsledky sledování a zobrazí všechny zjištěné problémy:

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## Krok 4: Export do PDF

Spusťte proces exportu a převeďte soubor DWG na PDF s povoleným sledováním:

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## Krok 5: Třída CadRenderHandler

 Definujte`CadRenderHandler`třída pro zpracování výsledků vykreslování, zobrazení informací o sledování:

```java
public static class ErrorHandler extends CadRasterizationOptions.CadRenderHandler {
    @Override
    public void invoke(CadRenderResult result) {
        System.out.println("Tracking results of exporting");

        if (result.isRenderComplete())
            return;

        System.out.println("Have some problems:");

        int idxError = 1;
        for (RenderResult rr : result.getFailures()) {
            System.out.printf("{0}. {1}, {2}", idxError, rr.getRenderCode(), rr.getMessage());
            idxError++;
        }
    }
}
```

## Závěr

Povolení sledování v souborech DWG pomocí Aspose.CAD for Java je bezproblémový proces, který zlepšuje spolupráci v projektech CAD. Dodržováním těchto kroků můžete efektivně implementovat funkci sledování, která zajistí hladkou komunikaci a řešení chyb.

## FAQ

### Q1: Mohu povolit sledování pro jiné formáty souborů CAD pomocí Aspose.CAD for Java?

A1: Aspose.CAD primárně podporuje soubory DWG pro sledování. Další formáty naleznete v dokumentaci.

### Q2: Jak mohu zpracovat další možnosti exportu v Aspose.CAD pro Java?

 A2: Prozkoumejte rozsáhlou dokumentaci na adrese[Aspose.CAD Java dokumentace](https://reference.aspose.com/cad/java/).

### Q3: Je k dispozici zkušební verze pro Aspose.CAD pro Javu?

 A3: Ano, máte přístup ke zkušební verzi na[Bezplatná zkušební verze Aspose.CAD](https://releases.aspose.com/).

### Q4: Kde mohu vyhledat pomoc nebo diskutovat o problémech souvisejících s Aspose.CAD for Java?

 A4: Navštivte[Fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) za podporu komunity.

### Q5: Jak získám dočasnou licenci pro Aspose.CAD for Java?

 A5: Postupujte podle postupu popsaného na[Dočasná licence](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
