---
title: Převeďte rozvržení na rastrový obrázek v Aspose.CAD pro .NET
linktitle: Převést rozvržení na rastrový obrázek
second_title: Aspose.CAD .NET – formát souborů CAD a BIM
description: Bez námahy převádějte rozvržení CAD na rastrové obrázky pomocí Aspose.CAD for .NET. Vylepšete svůj vývoj pomocí výkonných možností manipulace CAD.
type: docs
weight: 12
url: /cs/net/cad-drawing-manipulation/convert-layouts-to-raster-image/
---
## Úvod

Chcete snadno převést rozvržení na rastrové obrázky ve svých aplikacích .NET? Už nehledejte! Tento podrobný průvodce vás provede procesem pomocí Aspose.CAD for .NET, výkonné knihovny, která zjednodušuje úlohy CAD (Computer-Aided Design).

## Předpoklady

Než se pustíte do výukového programu, ujistěte se, že máte splněny následující předpoklady:

- Aspose.CAD for .NET Library: Stáhněte a nainstalujte knihovnu z[Stránka ke stažení Aspose.CAD for .NET](https://releases.aspose.com/cad/net/).

- Vývojové prostředí: Ujistěte se, že máte na svém počítači nastavené funkční vývojové prostředí .NET.

- Dokument k převodu: Připravte dokument CAD, který obsahuje rozvržení, která chcete převést na rastrové obrázky.

- Váš adresář dokumentů: Nahraďte zástupný symbol "Your Document Directory" v kódu cestou k adresáři vašeho dokumentu.

## Importovat jmenné prostory

Nejprve importujme potřebné jmenné prostory, aby byly funkce Aspose.CAD přístupné ve vašem kódu.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Krok 1: Načtěte dokument CAD

Začněte načtením dokumentu CAD pomocí knihovny Aspose.CAD.

```csharp
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image image = Image.Load(sourceFilePath))
{
    //Zde bude váš kód pro další kroky
}
```

## Krok 2: Nakonfigurujte možnosti rastrování

 Vytvořte instanci`CadRasterizationOptions` nastavit šířku, výšku stránky a určit rozvržení, která chcete převést.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1200;
rasterizationOptions.PageHeight = 1200;
rasterizationOptions.Layouts = new string[] { "Model", "Layout1" };
```

## Krok 3: Nastavte TiffOptions pro výsledný obrázek

 Vytvořte instanci`TiffOptions` definování formátu výsledného obrázku.

```csharp
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.VectorRasterizationOptions = rasterizationOptions;
```

## Krok 4: Uložte výsledný obrázek

Zadejte výstupní cestu a uložte převedený obrázek.

```csharp
string outputFilePath = MyDir + "conic_pyramid_layoutstorasterimage_out.tiff";
image.Save(outputFilePath, options);
```

## Závěr

Gratulujeme! Úspěšně jste převedli rozvržení CAD do formátu rastrového obrázku pomocí Aspose.CAD for .NET. Možnosti jsou obrovské a tato příručka slouží jako výchozí bod pro vaše úsilí související s CAD.

## FAQ

### Q1: Je Aspose.CAD kompatibilní se všemi formáty CAD?

 Odpověď 1: Aspose.CAD podporuje širokou škálu formátů CAD, včetně DWG, DXF, DWF, STL a dalších. Zkontrolovat[dokumentace](https://reference.aspose.com/cad/net/) pro úplný seznam.

### Q2: Jak mohu získat dočasnou licenci pro Aspose.CAD?

 A2: Navštivte[dočasná licenční stránka](https://purchase.aspose.com/temporary-license/) získat dočasnou licenci pro účely testování a hodnocení.

### Q3: Kde najdu podporu pro Aspose.CAD?

 Odpověď 3: Fóra jsou skvělým místem pro vyhledání pomoci. Navštivte[Fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) spojit se s komunitou a získat pomoc.

### Q4: Mohu vyzkoušet Aspose.CAD zdarma?

 A4: Rozhodně! Chyťte se[zkušební verze zdarma](https://releases.aspose.com/) prozkoumat funkce a možnosti Aspose.CAD.

### Q5: Kde mohu zakoupit licenci pro Aspose.CAD?

 A5: Přejděte na[nákupní stránku](https://purchase.aspose.com/buy) koupit licenci a odemknout plný potenciál Aspose.CAD.