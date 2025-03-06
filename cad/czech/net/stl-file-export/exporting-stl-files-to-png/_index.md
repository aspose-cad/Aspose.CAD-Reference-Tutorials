---
title: Snadná konverze STL do PNG s Aspose.CAD pro .NET
linktitle: Export STL souborů do PNG
second_title: Aspose.CAD .NET – formát souborů CAD a BIM
description: Bez námahy převádějte soubory STL do PNG pomocí Aspose.CAD for .NET. Postupujte podle našeho podrobného průvodce pro bezproblémovou integraci. Stáhnout teď!
weight: 10
url: /cs/net/stl-file-export/exporting-stl-files-to-png/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Snadná konverze STL do PNG s Aspose.CAD pro .NET

## Úvod
V dynamickém světě počítačově podporovaného navrhování (CAD) je efektivní převod souborů zásadní. Aspose.CAD for .NET je výkonná sada nástrojů, která zjednodušuje proces exportu souborů STL do PNG a poskytuje vývojářům potřebnou flexibilitu a funkčnost. Tento tutoriál vás provede procesem krok za krokem a zajistí hladký přechod z STL na PNG pomocí Aspose.CAD.
## Předpoklady
Než se pustíme do výukového programu, ujistěte se, že máte na svém místě následující:
1.  Aspose.CAD for .NET: Stáhněte a nainstalujte knihovnu Aspose.CAD. Můžete to najít[tady](https://releases.aspose.com/cad/net/).
2. Vývojové prostředí: Nastavte si preferované vývojové prostředí .NET.
3. Soubor STL: Připravte si soubor STL ke konverzi. Pro tento tutoriál použijeme vzorový soubor s názvem "galeon.stl."
## Importovat jmenné prostory
Chcete-li zahájit proces, importujte potřebné jmenné prostory do vaší aplikace .NET. To zajišťuje, že máte přístup ke třídám a metodám požadovaným pro převod STL na PNG.
```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```
## Krok 1: Definujte adresář a cestu ke zdrojovému souboru
```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "galeon.stl";
```
Ujistěte se, že jste nahradili "Your Document Directory" skutečnou cestou k adresáři, kde je umístěn váš soubor STL.
## Krok 2: Načtěte obrázek CAD
```csharp
using (var cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // V rámci tohoto bloku budou provedeny další kroky
}
```
Tento krok načte soubor STL jako obrázek CAD, což vám umožní s ním manipulovat a exportovat jej.
## Krok 3: Nastavte možnosti rastrování
```csharp
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 100;
rasterizationOptions.PageHeight = 100;
```
Upravte šířku a výšku stránky podle svých preferencí a požadavků. Tato nastavení určují rozměry exportovaného PNG.
## Krok 4: Nakonfigurujte možnosti PNG
```csharp
PngOptions pngOptions = new PngOptions();
pngOptions.VectorRasterizationOptions = rasterizationOptions;
```
Vytvořte možnosti PNG se začleněním nastavení rastrování definovaného v předchozím kroku.
## Krok 5: Uložte soubor PNG
```csharp
string outPath = sourceFilePath + ".png";
cadImage.Save(outPath, pngOptions);
```
Zadejte výstupní cestu pro soubor PNG a uložte obrázek CAD ve formátu PNG pomocí poskytnutých možností.
Opakujte tyto kroky podle potřeby pro váš konkrétní případ použití a úspěšně exportujete soubory STL do PNG pomocí Aspose.CAD for .NET.
## Závěr
Aspose.CAD for .NET zjednodušuje složitý úkol převodu souborů STL do formátu PNG a poskytuje vývojářům spolehlivou sadu nástrojů. Podle tohoto podrobného průvodce můžete tuto funkci bez problémů integrovat do svých aplikací.
## Nejčastější dotazy
### Otázka: Mohu přizpůsobit rozměry exportovaného PNG?
 Absolutně! V kroku 3 upravte`PageWidth` a`PageHeight` hodnoty, které splňují vaše specifické požadavky.
### Otázka: Je k dispozici dočasná licence pro účely testování?
 Ano, můžete získat dočasnou licenci[tady](https://purchase.aspose.com/temporary-license/) pro testování a hodnocení.
### Otázka: Kde najdu další podporu nebo komunitní diskuse?
 Navštivte[Fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) za podporu a společné diskuse.
### Otázka: Jsou pro převod podporovány jiné formáty souborů?
 Ano, Aspose.CAD podporuje různé formáty CAD nad rámec STL. Odkazovat na[dokumentace](https://reference.aspose.com/cad/net/) pro úplný seznam.
### Otázka: Mohu dávkově zpracovat více souborů STL?
Rozhodně! Implementujte smyčku na základě poskytnutých kroků pro dávkové zpracování více souborů STL.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
