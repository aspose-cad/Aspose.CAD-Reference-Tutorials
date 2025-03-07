---
title: Nastavení velikosti plátna a režimu v Aspose.CAD pro .NET
linktitle: Nastavení velikosti plátna a režimu
second_title: Aspose.CAD .NET – formát souborů CAD a BIM
description: Prozkoumejte podrobného průvodce nastavením velikosti plátna a režimu v Aspose.CAD pro .NET. Pomocí tohoto komplexního návodu snadno optimalizujte své vykreslování CAD.
weight: 16
url: /cs/net/cad-features-and-support/setting-canvas-size-and-mode/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Nastavení velikosti plátna a režimu v Aspose.CAD pro .NET

## Úvod

Jste připraveni odemknout plný potenciál Aspose.CAD pro .NET a revoluci ve vašem vykreslování CAD? V tomto tutoriálu krok za krokem se ponoříme do složitosti nastavení velikosti plátna a režimu pomocí výkonné knihovny Aspose.CAD. Ať už jste zkušený vývojář nebo teprve začínáte, tento průvodce vás provede celým procesem a zajistí vám efektivní využití možností Aspose.CAD.

## Předpoklady

Než se pustíme do výukového programu, ujistěte se, že máte splněny následující předpoklady:

-  Knihovna Aspose.CAD: Stáhněte a nainstalujte knihovnu Aspose.CAD z[Web Aspose.CAD](https://releases.aspose.com/cad/net/).

- Vývojové prostředí: Ujistěte se, že máte na svém počítači nastavené vývojové prostředí .NET.

-  Ukázkový soubor CAD: V tomto tutoriálu použijeme ukázkový soubor DXF. Jeden najdete v[Dokumentace Aspose.CAD](https://reference.aspose.com/cad/net/).

## Importovat jmenné prostory

Chcete-li začít, importujte potřebné jmenné prostory na začátku vaší aplikace .NET:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Krok 1: Načtěte soubor CAD

Začněte načtením souboru CAD pomocí následujícího kódu:

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    //Zde bude váš kód pro další kroky
}
```

## Krok 2: Vytvořte CadRasterizationOptions

 Vytvořte instanci`CadRasterizationOptions` a nastavte jeho vlastnosti:

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
rasterizationOptions.NoScaling = false;
```

## Krok 3: Vytvořte PdfOptions

 Vytvořte instanci`PdfOptions` a nastavte jej`VectorRasterizationOptions` vlastnictví:

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Krok 4: Export do PDF

Exportujte soubor CAD do PDF pomocí nakonfigurovaných možností:

```csharp
image.Save(MyDir + "result_out.pdf", pdfOptions);
```

## Krok 5: Vytvořte TiffOptions

 Vytvořte instanci`TiffOptions` a nastavte jej`VectorRasterizationOptions` vlastnictví:

```csharp
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Krok 6: Export do TIFF

Exportujte soubor CAD do formátu TIFF pomocí nakonfigurovaných možností:

```csharp
image.Save(MyDir + "result_out.tiff", tiffOptions);
```

## Závěr

Gratulujeme! Úspěšně jste nastavili velikost a režim plátna v Aspose.CAD pro .NET. Tato výkonná funkce otevírá svět možností pro vykreslování CAD. Experimentujte s různými možnostmi a objevte plný potenciál Aspose.CAD ve svých aplikacích .NET.

## FAQ

### Q1: Mohu používat Aspose.CAD s jinými knihovnami .NET?

Odpověď 1: Ano, Aspose.CAD se hladce integruje s dalšími knihovnami .NET a poskytuje rozšířené možnosti pro manipulaci s CAD.

### Q2: Je k dispozici bezplatná zkušební verze pro Aspose.CAD?

 Odpověď 2: Ano, funkce Aspose.CAD můžete prozkoumat pomocí bezplatné zkušební verze. Návštěva[tady](https://releases.aspose.com/) začít.

### Q3: Jak mohu získat podporu pro Aspose.CAD?

 A3: Pro podporu a diskuse navštivte[Fórum Aspose.CAD](https://forum.aspose.com/c/cad/19).

### Q4: Kde najdu komplexní dokumentaci k Aspose.CAD?

 A4: Viz[Dokumentace Aspose.CAD](https://reference.aspose.com/cad/net/) pro podrobné informace a příklady.

### Q5: Jak mohu zakoupit Aspose.CAD pro .NET?

 A5: Chcete-li zakoupit Aspose.CAD, navštivte[nákupní stránku](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
