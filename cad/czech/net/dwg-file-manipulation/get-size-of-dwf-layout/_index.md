---
title: Práce se soubory DWG v C# – Získejte velikost rozvržení DWF
linktitle: Práce se soubory DWG v C# – Získejte velikost rozvržení DWF
second_title: Aspose.CAD .NET – formát souborů CAD a BIM
description: Prozkoumejte sílu Aspose.CAD for .NET při práci se soubory DWG. Naučte se bez námahy extrahovat velikosti rozvržení DWF pomocí C#.
weight: 10
url: /cs/net/dwg-file-manipulation/get-size-of-dwf-layout/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Práce se soubory DWG v C# – Získejte velikost rozvržení DWF

## Úvod

V oblasti počítačově podporovaného navrhování (CAD) a vývoje .NET představuje Aspose.CAD výkonný nástroj pro práci se soubory DWG. Tento tutoriál vás provede procesem práce se soubory DWG v C# a extrahováním velikosti rozvržení DWF. Než se ponoříme do kódu, ujistěte se, že máte vše nastaveno, abyste se mohli vydat na tuto cestu.

## Předpoklady

Chcete-li bez problémů sledovat tento tutoriál, ujistěte se, že máte splněny následující předpoklady:

-  Aspose.CAD for .NET: Ujistěte se, že máte nainstalovaný Aspose.CAD for .NET. Můžete si jej stáhnout z[Stránka ke stažení Aspose.CAD for .NET](https://releases.aspose.com/cad/net/).

Nyní, když máte potřebné nástroje, pojďme se vrhnout do arény kódování.

## Importovat jmenné prostory

Než začneme pracovat s kódem, importujme požadované jmenné prostory:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Dwf;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

Tyto jmenné prostory poskytnou základní třídy a metody pro práci se soubory CAD s Aspose.CAD ve vaší aplikaci C#.

## Krok 1: Nastavte své prostředí

Začněte tím, že se ujistíte, že máte pro svůj projekt nastavené správné prostředí. Odkazujte na knihovnu Aspose.CAD ve svém projektu C#.

## Krok 2: Definujte cesty k souboru

Definujte cesty pro váš soubor DWG a výstupní adresář pro vygenerované soubory JPG:

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "blocks_and_tables.dwf";
```

## Krok 3: Načtěte obrázek DWF

Načtěte obrázek DWF pomocí Aspose.CAD:

```csharp
using (DwfImage image = (DwfImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    // Kód pro další kroky najdete zde
}
```

## Krok 4: Iterujte stránky

Iterujte stránky obrázku DWF:

```csharp
foreach (var page in image.Pages)
{
    // Kód pro další kroky najdete zde
}
```

## Krok 5: Získejte informace o rozložení

Získejte informace o rozložení z každé stránky:

```csharp
var layout = page.Name;
System.Console.WriteLine("Layout= " + layout);
```

## Krok 6: Nastavte možnosti JPG

Nastavte možnosti pro uložení rozvržení jako souboru JPG:

```csharp
using (FileStream fs = new FileStream(MyDir + "layout_" + layout + ".jpg", FileMode.Create))
{
    JpegOptions jpegOptions = new JpegOptions();
    CadRasterizationOptions options = new CadRasterizationOptions();
    options.Layouts = new string[] { layout };
    // Kód pro další kroky najdete zde
}
```

## Krok 7: Určete velikost stránky

Určete velikost rozvržení DWF:

```csharp
double sizeExtX = page.MaxPoint.X - page.MinPoint.X;
double sizeExtY = page.MaxPoint.Y - page.MinPoint.Y;
// Kód pro další kroky najdete zde
```

## Krok 8: Nastavte rozměry stránky

Nastavte rozměry stránky podle typu jednotky:

```csharp
if (page.UnitType == UnitType.Inch)
{
    options.PageHeight = CommonHelper.INtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.INtoPixels(sizeExtX, CommonHelper.DPI);
}
else if (page.UnitType == UnitType.Millimeter)
{
    options.PageHeight = CommonHelper.MMtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.MMtoPixels(sizeExtX, CommonHelper.DPI);
}
else
{
    options.PageHeight = (float)sizeExtY;
    options.PageWidth = (float)sizeExtX;
}
```

## Krok 9: Uložte soubor JPG

Uložte soubor JPG se zadanými možnostmi:

```csharp
jpegOptions.VectorRasterizationOptions = options;
image.Save(fs, jpegOptions);
}
```

Nyní jste úspěšně extrahovali velikost rozvržení DWF ze souboru DWG pomocí Aspose.CAD v C#. Neváhejte a prozkoumejte další vlastnosti a funkce, které Aspose.CAD nabízí pro vývoj .NET.

## Závěr

V tomto tutoriálu jsme prošli procesem práce se soubory DWG v C# pomocí Aspose.CAD. Pomocí těchto kroků můžete nejen získat velikost rozvržení DWF, ale také využít možnosti Aspose.CAD pro různé úkoly související s CAD ve vašich projektech .NET.

## FAQ

### Q1: Je Aspose.CAD kompatibilní s nejnovějšími formáty souborů DWG?

 A1: Aspose.CAD podporuje různé formáty souborů DWG, včetně nejnovějších verzí. Odkazovat na[dokumentace](https://reference.aspose.com/cad/net/) pro konkrétní podrobnosti o kompatibilitě.

### Q2: Mohu používat Aspose.CAD pro komerční i osobní projekty?

 Odpověď 2: Ano, Aspose.CAD nabízí flexibilní možnosti licencování pro komerční i osobní použití. Navštivte[nákupní stránku](https://purchase.aspose.com/buy) Více podrobností.

### Q3: Jak mohu získat dočasnou licenci pro Aspose.CAD?

 A3: Můžete získat dočasnou licenci od[tady](https://purchase.aspose.com/temporary-license/) pro účely hodnocení.

### Q4: Kde najdu podporu pro Aspose.CAD?

A4: Máte-li jakékoli dotazy nebo pomoc, navštivte[Fórum Aspose.CAD](https://forum.aspose.com/c/cad/19).

### Q5: Je k dispozici bezplatná zkušební verze pro Aspose.CAD?

 A5: Ano, máte přístup k bezplatné zkušební verzi Aspose.CAD[tady](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
