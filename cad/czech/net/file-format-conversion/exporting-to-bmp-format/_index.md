---
title: Export do formátu BMP - Aspose.CAD Tutorial
linktitle: Export do formátu BMP
second_title: Aspose.CAD .NET – formát souborů CAD a BIM
description: Prozkoumejte bezproblémový svět exportu 3D obrázků do BMP pomocí Aspose.CAD for .NET. Postupujte podle našeho návodu pro bezproblémový zážitek.
type: docs
weight: 11
url: /cs/net/file-format-conversion/exporting-to-bmp-format/
---
## Úvod

dynamickém světě vývoje softwaru vyniká Aspose.CAD for .NET jako výkonný nástroj pro práci se soubory CAD (Computer-Aided Design). Pokud chcete exportovat obrázky CAD do široce používaného formátu BMP, tento návod je vaším průvodcem. V tomto podrobném návodu prozkoumáme proces exportu 3D obrázků do BMP pomocí Aspose.CAD for .NET. Pojďme se ponořit!

## Předpoklady

Než se pustíme do tohoto tutoriálu, ujistěte se, že máte splněny následující předpoklady:

-  Aspose.CAD for .NET: Stáhněte si a nainstalujte knihovnu Aspose.CAD z[tady](https://releases.aspose.com/cad/net/).
- Vývojové prostředí: Nastavte vývojové prostředí .NET.
- Soubor CAD: Připravte si soubor CAD pro export. V tomto příkladu použijeme "18-12-11 9644 - site.dwf."

## Importovat jmenné prostory

Ve svém projektu .NET se ujistěte, že importujete potřebné jmenné prostory:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

## Krok 1: Načtěte obrázek CAD

Začněte načtením obrázku CAD do projektu. Nahraďte "Your Document Directory" skutečnou cestou k adresáři.

```csharp
string MyDir = "Your Document Directory";
string inputFile = MyDir + "18-12-11 9644 - site.dwf";

using (Image image = Image.Load(inputFile))
{
    // Zde je váš kód pro načtení obrázku
}
```

## Krok 2: Nakonfigurujte možnosti exportu BMP

Nastavte možnosti exportu BMP, včetně možností vektorového rastrování pro soubory CAD.

```csharp
BmpOptions bmpOptions = new BmpOptions();
var dwfRasterizationOptions = new CadRasterizationOptions();
bmpOptions.VectorRasterizationOptions = dwfRasterizationOptions;

dwfRasterizationOptions.PageHeight = 500;
dwfRasterizationOptions.PageWidth = 500;
```

## Krok 3: Export do BMP

Spusťte proces exportu a zadejte výstupní cestu pro soubor BMP.

```csharp
string outPath = MyDir + "18-12-11 9644 - site.bmp";
image.Save(outPath, bmpOptions);
```

## Závěr

Gratulujeme! Úspěšně jste exportovali 3D obrázek do BMP pomocí Aspose.CAD for .NET. Tento tutoriál poskytuje letmý pohled na všestrannost Aspose.CAD, takže složité úkoly jsou jako vánek.

## FAQ

### Q1: Mohu použít Aspose.CAD pro .NET s jakýmkoli formátem souboru CAD?

Odpověď 1: Ano, Aspose.CAD podporuje různé formáty souborů CAD a poskytuje flexibilitu ve vašich projektech.

### Q2: Je k dispozici dočasná licence pro testovací účely?

 A2: Určitě! Můžete získat dočasnou licenci[tady](https://purchase.aspose.com/temporary-license/) pro hodnocení.

### Q3: Kde najdu komplexní dokumentaci k Aspose.CAD?

 A3: Viz dokumentace[tady](https://reference.aspose.com/cad/net/) pro podrobné informace a příklady.

### Q4: Jak vyhledám podporu nebo se spojím s komunitou?

 A4: Navštivte fórum Aspose.CAD[tady](https://forum.aspose.com/c/cad/19) klást otázky a zapojit se do komunity.

### Q5: Mohu zakoupit Aspose.CAD pro .NET?

 A5: Ano, můžete si zakoupit Aspose.CAD[tady](https://purchase.aspose.com/buy) odemknout jeho plný potenciál pro vaše projekty.
