---
title: Exportujte rozvržení CAD do formátů rastrových obrázků v Aspose.CAD pro .NET
linktitle: Exportujte rozvržení CAD do formátů rastrových obrázků
second_title: Aspose.CAD .NET – formát souborů CAD a BIM
description: Naučte se exportovat rozvržení CAD do rastrových obrázků pomocí Aspose.CAD for .NET. Postupujte podle našeho podrobného průvodce pro bezproblémovou konverzi.
weight: 10
url: /cs/net/cad-export-formats/export-cad-layouts-to-raster-image-formats/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportujte rozvržení CAD do formátů rastrových obrázků v Aspose.CAD pro .NET

## Úvod

Hledáte efektivní převod CAD rozvržení na rastrové obrazové formáty pomocí Aspose.CAD pro .NET? Tento podrobný průvodce vás provede celým procesem a poskytne podrobné pokyny a úryvky kódu, aby byl úkol bezproblémový. Ať už jste zkušený vývojář nebo nováček v Aspose.CAD, tento výukový program je vhodný pro všechny úrovně odbornosti.

## Předpoklady

Než se pustíte do výukového programu, ujistěte se, že máte následující:

- Knihovna Aspose.CAD for .NET: Ujistěte se, že máte nainstalovanou knihovnu Aspose.CAD. Pokud ne, můžete si jej stáhnout z[Web Aspose.CAD](https://releases.aspose.com/cad/net/).

- Výkresový soubor CAD: Připravte si výkresový soubor CAD (např. conic_pyramid.dxf), který chcete převést do formátů rastrových obrázků.

## Importovat jmenné prostory

Ve svém projektu .NET naimportujte potřebné jmenné prostory, abyste mohli využít funkce Aspose.CAD. Na začátek kódu uveďte následující jmenné prostory:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Krok 1: Načtěte výkres CAD

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

// Načtěte výkres CAD v instanci Image
using (var image = Image.Load(sourceFilePath))
{
    // Zde je váš kód pro načtení výkresu CAD
}
```

## Krok 2: Vytvořte CadRasterizationOptions

```csharp
// Vytvořte instanci CadRasterizationOptions
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
```

## Krok 3: Zadejte vrstvy

```csharp
// Přidejte název vrstvy do seznamu vrstev CadRasterizationOptions
rasterizationOptions.Layers = new string[] { "LayerA" };
```

## Krok 4: Vytvořte JpegOptions

```csharp
// Vytvořte instanci JpegOptions (nebo jakékoli ImageOptions pro rastrové formáty)
var options = new JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
```

## Krok 5: Export do formátu Jpeg

```csharp
// Exportujte každou vrstvu do formátu Jpeg
MyDir = MyDir + "CADLayersToRasterImageFormats_out.jpg";
image.Save(MyDir, options);
```

## Další krok: Převeďte všechny vrstvy

Pokud chcete převést všechny vrstvy, použijte následující metodu:

```csharp
ConvertAllLayersToRasterImageFormats();
```

Tato metoda iteruje přes všechny vrstvy ve výkresu CAD a každou vrstvu exportuje do samostatného souboru Jpeg.

## Závěr

Gratulujeme! Úspěšně jste se naučili exportovat rozvržení CAD do formátů rastrových obrázků pomocí Aspose.CAD for .NET. Tento výukový program poskytuje komplexního průvodce pro vývojáře, kteří hledají efektivní a spolehlivá řešení pro konverzi CAD.

## FAQ

### Q1: Mohu pro export použít jiné formáty obrázků?

 A1: Ano, můžete. Jednoduše vyměnit`JpegOptions` s možnostmi požadovaného formátu, jako je např`PngOptions` nebo`BmpOptions`.

### Q2: Je k dispozici zkušební verze?

 A2: Ano, můžete prozkoumat funkčnost Aspose.CAD stažením zkušební verze[tady](https://releases.aspose.com/).

### Q3: Jak mohu získat podporu pro Aspose.CAD?

 A3: Navštivte Aspose.CAD[Fórum](https://forum.aspose.com/c/cad/19) pro podporu komunity nebo zvažte zakoupení licence pro vyhrazenou podporu.

### Q4: Jsou k dispozici dočasné licence?

 A4: Ano, můžete získat dočasnou licenci[tady](https://purchase.aspose.com/temporary-license/).

### Q5: Kde najdu dokumentaci?

 A5: Viz podrobná dokumentace[tady](https://reference.aspose.com/cad/net/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
