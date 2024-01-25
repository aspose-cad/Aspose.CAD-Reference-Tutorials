---
title: Exportujte objekty OLE z CAD pomocí Aspose.CAD for Java
linktitle: Exportujte objekty OLE z CAD
second_title: Aspose.CAD Java API
description: Odemkněte potenciál Aspose.CAD pro Javu. Bez námahy exportujte objekty OLE ze souborů CAD. Stáhněte si nyní pro bezproblémovou správu dat CAD.
type: docs
weight: 10
url: /cs/java/cad-to-pdf-and-svg-export-options/export-ole-objects-from-cad/
---
## Úvod

V dynamickém světě Computer-Aided Design (CAD) je efektivní správa a extrahování objektů OLE (Object Linking and Embedding) zásadní. Aspose.CAD for Java poskytuje výkonné řešení pro export objektů OLE ze souborů CAD. Tento průvodce vás krok za krokem provede celým procesem a zajistí, že využijete plný potenciál tohoto nástroje.

## Předpoklady

Než se pustíte do výukového programu, ujistěte se, že máte splněny následující předpoklady:

- Prostředí Java: Ujistěte se, že máte na svém počítači nastavené vývojové prostředí Java.
-  Aspose.CAD for Java: Stáhněte si a nainstalujte knihovnu Aspose.CAD for Java. Knihovnu najdete na[odkaz ke stažení](https://releases.aspose.com/cad/java/).
- Soubory CAD: Připravte soubory CAD obsahující objekty OLE, které chcete exportovat.

## Importovat jmenné prostory

Chcete-li začít, importujte potřebné jmenné prostory do svého projektu Java. Tyto jmenné prostory poskytují základní třídy a funkce potřebné pro práci se soubory CAD pomocí Aspose.CAD.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Nyní si rozdělme proces exportu objektů OLE z CAD do několika kroků:

## Krok 1: Nastavte adresář dokumentů

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

Ujistěte se, že jste nahradili "Your Document Directory" cestou k adresáři obsahujícímu vaše CAD soubory.

## Krok 2: Definujte názvy souborů CAD

```java
String[] files = new String[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

 Zadejte názvy souborů CAD, které chcete zpracovat v`files` pole.

## Krok 3: Nastavte možnosti exportu PNG

```java
PngOptions pngOptions = new PngOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.setLayouts(new String[] { "Layout1" });
```

Nakonfigurujte možnosti exportu PNG, včetně vektorového rastrování a nastavení rozvržení.

## Krok 4: Iterace přes soubory CAD

```java
for(String file : files)
{
    CadImage cadImage = (CadImage)Image.load(dataDir + file);
    cadImage.save(dataDir + file + "_out.png", pngOptions);
}
```

Iterujte každý zadaný soubor CAD, načtěte jej pomocí Aspose.CAD a uložte objekty OLE jako obrázky PNG.

## Závěr

Pomocí těchto jednoduchých, ale účinných kroků můžete bezproblémově exportovat OLE objekty ze souborů CAD pomocí Aspose.CAD for Java. Tento všestranný nástroj umožňuje vývojářům efektivně spravovat data CAD a otevírá nové možnosti ve vývoji aplikací CAD.

## FAQ

### Q1: Je Aspose.CAD kompatibilní se všemi formáty souborů CAD?

 Odpověď 1: Aspose.CAD podporuje různé formáty CAD, včetně DWG, DXF a DGN. Odkazovat na[dokumentace](https://reference.aspose.com/cad/java/) pro úplný seznam.

### Q2: Mohu upravit nastavení exportu pro objekty OLE?

Odpověď 2: Ano, Aspose.CAD poskytuje rozsáhlé možnosti přizpůsobení nastavení exportu, což vám umožní přizpůsobit výstup vašim konkrétním požadavkům.

### Q3: Je k dispozici bezplatná zkušební verze pro Aspose.CAD?

 A3: Ano, můžete prozkoumat možnosti Aspose.CAD získáním bezplatné zkušební verze od[tady](https://releases.aspose.com/).

### Q4: Kde mohu získat podporu komunity pro Aspose.CAD?

 A4: Připojte se ke komunitě Aspose.CAD na[Fórum](https://forum.aspose.com/c/cad/19) vyhledat pomoc a podělit se o své zkušenosti.

### Q5: Jak mohu zakoupit licenci pro Aspose.CAD?

A5: Navštivte[nákupní stránku](https://purchase.aspose.com/buy) získat licenci, která vyhovuje vašim vývojovým potřebám.