---
title: Export DWG do PDF nebo rastrových obrázků - Aspose.CAD Guide
linktitle: Export DWG do PDF nebo rastrových obrázků
second_title: Aspose.CAD .NET – formát souborů CAD a BIM
description: Prozkoumejte komplexního průvodce exportem DWG do PDF nebo rastrových obrázků pomocí Aspose.CAD for .NET. Naučte se kroky, předpoklady a získejte praktické zkušenosti s touto výkonnou knihovnou.
type: docs
weight: 11
url: /cs/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/
---
## Úvod

Hledáte bezproblémový převod souborů DWG do PDF nebo rastrových obrázků ve vaší aplikaci .NET? Už nehledejte! Tento podrobný průvodce vás provede procesem pomocí výkonné knihovny Aspose.CAD for .NET. Ať už jste zkušený vývojář nebo teprve začínáte, tento tutoriál je vhodný pro všechny úrovně dovedností.

## Předpoklady

Než se pustíme do výukového programu, ujistěte se, že máte na svém místě následující:

- Základní znalost programování .NET.
-  Nainstalovaná knihovna Aspose.CAD for .NET. Pokud ne, stáhněte si ji[tady](https://releases.aspose.com/cad/net/).
- Vaše oblíbené integrované vývojové prostředí (IDE) nastavené pro vývoj .NET.

## Importovat jmenné prostory

Začněme tím, že importujeme potřebné jmenné prostory do vašeho .NET projektu. To zajišťuje, že máte přístup k funkci Aspose.CAD ve vašem kódu.

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

## Krok 1: Načtěte soubor DWG

Začněte načtením souboru DWG, který chcete převést. Nahraďte "Your Document Directory" cestou k vašemu souboru DWG.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Zde je váš kód pro načtení DWG
}
```

## Krok 2: Nastavte export PDF

Nyní nakonfigurujeme nastavení exportu PDF. Tento příklad ukazuje, jak nastavit rozložení a zpracovat převody jednotek.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };

// Zkontrolujte a definujte systém jednotek
bool currentUnitIsMetric = false;
double currentUnitCoefficient = 1.0;
DefineUnitSystem(cadImage.UnitType, out currentUnitIsMetric, out currentUnitCoefficient);

// Zde je váš kód pro nastavení exportu PDF
```

## Krok 3: Export do PDF

Proveďte export do PDF pomocí nakonfigurovaných nastavení.

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath, pdfOptions);
```

## Krok 4: Export do rastrových obrázků

Rozšiřte funkcionalitu o export do rastrových obrázků, jako je PNG.

```csharp
// Velikost A4 při 300 DPI - 2480 x 3508
rasterizationOptions.PageHeight = 3508;
rasterizationOptions.PageWidth = 2480;

PngOptions pngOptions = new PngOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath.Replace("pdf", "png"), pngOptions);
```

## Závěr

Gratulujeme! Úspěšně jste se naučili používat Aspose.CAD for .NET k exportu souborů DWG do PDF i rastrových obrázků. Tato výkonná knihovna zjednodušuje proces, činí jej efektivním a přívětivým pro vývojáře.

## FAQ

### Q1: Mohu použít Aspose.CAD pro .NET ve svých komerčních projektech?

 A1: Ano, můžete. Návštěva[purchase.aspose.com/buy](https://purchase.aspose.com/buy) pro podrobnosti o licencích.

### Q2: Je k dispozici bezplatná zkušební verze?

 A2: Určitě! Získejte bezplatnou zkušební verzi[tady](https://releases.aspose.com/).

### Q3: Jak mohu získat podporu pro Aspose.CAD pro .NET?

 A3: Přejděte na[Fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) za podporu komunity.

### Q4: Mohu získat dočasnou licenci pro testovací účely?

 A4: Ano, můžete získat dočasnou licenci[tady](https://purchase.aspose.com/temporary-license/).

### Q5: Kde najdu podrobnou dokumentaci?

 A5: Dokumentace je k dispozici na[Aspose.CAD](https://reference.aspose.com/cad/net/).