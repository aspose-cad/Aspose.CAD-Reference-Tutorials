---
title: Seznam rozvržení v DWG pomocí Aspose.CAD pro Java
linktitle: Seznam rozložení v DWG
second_title: Aspose.CAD Java API
description: Prozkoumejte Aspose.CAD for Java a bez námahy vypisujte rozvržení v souborech DWG. Integrujte výkonné funkce CAD do svých aplikací Java.
weight: 12
url: /cs/java/cad-file-manipulation/list-layouts-in-dwg/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Seznam rozvržení v DWG pomocí Aspose.CAD pro Java

## Úvod

Vítejte v našem podrobném průvodci používáním Aspose.CAD for Java k zobrazení rozvržení v souborech DWG. Aspose.CAD je výkonná knihovna, která umožňuje vývojářům pracovat se soubory CAD programově. V tomto tutoriálu se zaměříme na konkrétní úkol: výpis rozvržení v souboru DWG. Na konci této příručky budete schopni bezproblémově integrovat tuto funkci do vašich aplikací Java.

## Předpoklady

Než se pustíme do výukového programu, ujistěte se, že máte splněny následující předpoklady:

-  Knihovna Aspose.CAD for Java: Ujistěte se, že máte nainstalovanou knihovnu Aspose.CAD pro Java. Můžete si jej stáhnout z[webová stránka](https://releases.aspose.com/cad/java/).

- Vývojové prostředí Java: Nastavte na vašem počítači vývojové prostředí Java.

## Importovat jmenné prostory

Chcete-li používat Aspose.CAD, musíte do své Java aplikace importovat potřebné jmenné prostory. Na začátek souboru Java přidejte následující řádky:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.CadLayoutDictionary;
import com.aspose.cad.fileformats.cad.cadobjects.CadLayout;
```

## Krok 1: Nastavte adresář dokumentů

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

Ujistěte se, že jste nahradili "Your Document Directory" cestou k adresáři, kde jsou uloženy vaše CAD soubory.

## Krok 2: Načtěte soubor DWG

```java
String sourceFilePath = dataDir + "conic_pyramid.dxf";
Image image = Image.load(sourceFilePath);
CadImage cadImage = (CadImage)image;
```

Načtěte soubor DWG pomocí zadané cesty k souboru.

## Krok 3: Získejte rozvržení a názvy tisku

```java
CadLayoutDictionary layouts = cadImage.getLayouts();
for (CadLayout layout : layouts.getValues())
{
    System.out.println("Layout " + layout.getLayoutName());
}
```

Načtěte rozvržení ze souboru DWG a vytiskněte jejich názvy do konzoly.

## Závěr

 Gratulujeme! Úspěšně jste vytvořili seznam rozvržení v souboru DWG pomocí Aspose.CAD for Java. Tento kurz se zabýval základními kroky, od nastavení prostředí až po tisk názvů rozvržení. Neváhejte a prozkoumejte další funkce Aspose.CAD pro Javu v[dokumentace](https://reference.aspose.com/cad/java/).

## FAQ

### Q1: Mohu použít Aspose.CAD for Java s jinými formáty souborů CAD?

Odpověď 1: Ano, Aspose.CAD podporuje různé formáty CAD, včetně DWG, DXF, DWF a dalších.

### Q2: Je k dispozici bezplatná zkušební verze pro Aspose.CAD pro Javu?

 A2: Ano, můžete získat bezplatnou zkušební verzi od[tady](https://releases.aspose.com/).

### Q3: Kde mohu získat podporu komunity pro Aspose.CAD pro Java?

 A3: Navštivte[Fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) za podporu komunity.

### Q4: Jak si koupím licenci pro Aspose.CAD for Java?

 A4: Můžete si koupit licenci od[nákupní stránku](https://purchase.aspose.com/buy).

### Q5: Mohu použít dočasnou licenci pro testovací účely?

 A5: Ano, můžete získat dočasnou licenci[tady](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
