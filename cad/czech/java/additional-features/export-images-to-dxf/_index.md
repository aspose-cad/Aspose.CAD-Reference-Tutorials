---
title: Export obrázků do formátu DXF pomocí Aspose.CAD pro Javu
linktitle: Export obrázků do formátu DXF pomocí Java
second_title: Aspose.CAD Java API
description: Prozkoumejte bezproblémový proces exportu obrázků do formátu DXF pomocí Aspose.CAD for Java. Podrobný průvodce, často kladené dotazy a další.
type: docs
weight: 15
url: /cs/java/additional-features/export-images-to-dxf/
---
## Úvod

Vítejte v obsáhlém tutoriálu o exportu obrázků do formátu DXF pomocí Aspose.CAD pro Java. Aspose.CAD je výkonná Java knihovna, která umožňuje vývojářům pracovat s výkresy CAD programově. V tomto tutoriálu vás provedeme procesem exportu obrázků do formátu DXF a předvedeme různé kroky a techniky k dosažení tohoto úkolu.

## Předpoklady

Než začnete, ujistěte se, že máte následující:

- Základní znalost programování v Javě.
-  Nainstalovaná knihovna Aspose.CAD for Java. Můžete si jej stáhnout[tady](https://releases.aspose.com/cad/java/).
- Platná licence nebo dočasná licence pro Aspose.CAD. Získejte to[tady](https://purchase.aspose.com/temporary-license/).
- Některé ukázkové obrázky ve formátu DXF pro testování.

## Importovat jmenné prostory

Ve svém projektu Java importujte potřebné jmenné prostory pro Aspose.CAD:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadconsts.CadEntityTypeName;
import com.aspose.cad.fileformats.cad.cadobjects.CadBaseEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject;
import java.io.File;
import static java.lang.System.in;
```

## Krok 1: Nastavte nové písmo pro dokument

```java
// Cesta k adresáři prostředků.
String dataDir = "Your Document Directory" + "DXFDrawings/";

File[] files = new File(dataDir).listFiles();
for (File file : files) {
    String extension = GetFileExtension(file);
    if (extension.equals(".dxf")) {
        CadImage cadImage = (CadImage)Image.load(file.getName());
        for (Object style : cadImage.getStyles()) {
            ((CadStyleTableObject)style).setPrimaryFontName("Broadway");
        }
        cadImage.save(file.getName() + "_font.dxf");
    }
}
```

## Krok 2: Skryjte všechny „rovné“ čáry

```java
CadImage cadImageEntity = (CadImage)Image.load(file.getName());
for (CadBaseEntity entity : cadImageEntity.getEntities()) {
    if (entity.getTypeName() == CadEntityTypeName.LINE) {
        entity.setVisible((short)0);
    }
}
cadImageEntity.save(file.getName() + "_lines.dxf");
```

## Krok 3: Manipulace s textem

```java
CadImage cadImageText = (CadImage)Image.load(file.getName());
for (CadBaseEntity entity : cadImageText.getEntities()) {
    if (entity.getTypeName() == CadEntityTypeName.TEXT) {
        ((CadText)entity).setDefaultValue("New text here!!! :)");
        break;
    }
}
cadImageText.save(file.getName() + "_text.dxf");
```

Opakujte tyto kroky pro každý soubor DXF ve vašem adresáři.

## Závěr

Gratulujeme! Úspěšně jste se naučili exportovat obrázky do formátu DXF pomocí Aspose.CAD for Java. Tento tutoriál se zabýval základními kroky, včetně nastavení písem, skrytí čar a manipulace s textem v obrázcích CAD.

## FAQ

### Q1: Mohu používat Aspose.CAD pro Javu bez licence?

 A1: Můžete jej použít s dočasnou dostupnou licencí[tady](https://purchase.aspose.com/temporary-license/).

### Q2: Kde najdu dokumentaci Aspose.CAD?

 A2: Dokumentace je k dispozici[tady](https://reference.aspose.com/cad/java/).

### Q3: Jak získám podporu pro Aspose.CAD?

 A3: Navštivte fórum podpory[tady](https://forum.aspose.com/c/cad/19).

### Q4: Kde si mohu stáhnout Aspose.CAD pro Java?

 A4: Stáhněte si knihovnu[tady](https://releases.aspose.com/cad/java/).

### Q5: Je k dispozici bezplatná zkušební verze?

 A5: Ano, můžete získat bezplatnou zkušební verzi[tady](https://releases.aspose.com/).