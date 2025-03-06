---
title: Export vložených souborů DGN - Výukový program Aspose.CAD
linktitle: Export vložených souborů DGN
second_title: Aspose.CAD .NET – formát souborů CAD a BIM
description: Prozkoumejte sílu Aspose.CAD pro .NET. Naučte se snadno exportovat vložené soubory DGN do PDF pomocí tohoto podrobného návodu.
weight: 14
url: /cs/net/export-techniques/exporting-embedded-dgn-files/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export vložených souborů DGN - Výukový program Aspose.CAD

## Úvod

dynamickém světě vývoje softwaru vyniká Aspose.CAD for .NET jako výkonný nástroj pro práci se soubory CAD (Computer-Aided Design). Tento tutoriál vás provede procesem exportu vložených souborů DGN pomocí Aspose.CAD for .NET. Ať už jste zkušený vývojář nebo zvědavý začátečník, tento podrobný průvodce vám pomůže efektivně využít možnosti Aspose.CAD.

## Předpoklady

Než se pustíte do výukového programu, ujistěte se, že máte splněny následující předpoklady:

1.  Aspose.CAD pro .NET: Stáhněte a nainstalujte knihovnu z[Aspose.CAD pro .NET](https://releases.aspose.com/cad/net/).

2. Vývojové prostředí: Nastavte vývojové prostředí .NET pomocí sady Visual Studio nebo jiného preferovaného IDE.

3. Ukázkový soubor DXF: Pro tento tutoriál použijeme soubor "conic_pyramid.dxf". Ujistěte se, že jej máte k dispozici ve vámi určeném adresáři dokumentů.

## Importovat jmenné prostory

V kódu C# nezapomeňte importovat potřebné jmenné prostory:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
```

## Krok 1: Načtěte soubor DXF

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    //Zde bude váš kód pro další kroky
}
```

## Krok 2: Nastavte možnosti rastrování

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new[] { "Model" };
```

## Krok 3: Nastavte možnosti PDF

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Krok 4: Uložit jako PDF

```csharp
cadImage.Save(MyDir + "conic_pyramid.pdf", pdfOptions);
```

## Krok 5: Zobrazte zprávu o úspěchu

```csharp
Console.WriteLine("\nThe DXF drawing exported successfully to PDF.\nFile saved at " + MyDir);
```

## Závěr

Gratulujeme! Úspěšně jste exportovali vložený soubor DGN do PDF pomocí Aspose.CAD for .NET. Tento návod pokryl základní kroky a poskytl vám základ pro prozkoumání pokročilejších funkcí nabízených Aspose.CAD.

## FAQ

### Q1: Mohu používat Aspose.CAD pro .NET s jinými programovacími jazyky?

A1: Aspose.CAD primárně podporuje .NET, ale Aspose poskytuje knihovny pro různé jazyky, včetně Javy a Pythonu.

### Q2: Je k dispozici bezplatná zkušební verze pro Aspose.CAD pro .NET?

 A2: Ano, můžete získat bezplatnou zkušební verzi[tady](https://releases.aspose.com/).

### Q3: Kde najdu komplexní dokumentaci k Aspose.CAD pro .NET?

 A3: Viz dokumentace[tady](https://reference.aspose.com/cad/net/).

### Q4: Jak získám dočasné licencování pro Aspose.CAD for .NET?

 A4: Získejte dočasnou licenci[tady](https://purchase.aspose.com/temporary-license/).

### Q5: Potřebujete pomoc nebo se chcete zapojit do komunity?

A5: Navštivte[Fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) za podporu a diskuze.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
