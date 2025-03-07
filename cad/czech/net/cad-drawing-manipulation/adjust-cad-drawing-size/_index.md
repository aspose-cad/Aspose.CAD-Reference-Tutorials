---
title: Úprava velikosti výkresu CAD v Aspose.CAD pro .NET
linktitle: Úprava velikosti výkresu CAD
second_title: Aspose.CAD .NET – formát souborů CAD a BIM
description: Naučte se, jak snadno upravit velikosti výkresů CAD v .NET pomocí Aspose.CAD. Postupujte podle našeho podrobného průvodce pro bezproblémovou změnu velikosti.
weight: 10
url: /cs/net/cad-drawing-manipulation/adjust-cad-drawing-size/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Úprava velikosti výkresu CAD v Aspose.CAD pro .NET

## Úvod

Chcete plynule upravit velikost výkresů CAD ve svých aplikacích .NET? Aspose.CAD for .NET poskytuje robustní řešení, které vám umožní bez námahy zvládnout změnu velikosti výkresů CAD. V tomto tutoriálu vás provedeme celým procesem a rozebereme každý krok, abyste měli jistotu, že pochopíte složitost změny velikosti výkresů CAD pomocí Aspose.CAD.

## Předpoklady

Než se pustíme do výukového programu, ujistěte se, že máte splněny následující předpoklady:

- Aspose.CAD for .NET Library: Stáhněte a nainstalujte knihovnu z[Stránka ke stažení Aspose.CAD for .NET](https://releases.aspose.com/cad/net/).
- Ukázkový výkres CAD: Ujistěte se, že máte v adresáři dokumentů ukázkový soubor výkresu CAD (např. „sample.dwg“).

## Importovat jmenné prostory

Začněte importováním potřebných jmenných prostorů do vaší aplikace .NET. Tento krok je zásadní pro přístup k funkcím poskytovaným Aspose.CAD pro .NET.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Krok 1: Načtěte výkres CAD

Začněte načtením výkresu CAD do instance třídy Aspose.CAD.Image. Ujistěte se, že máte správnou cestu k souboru pro vzorový výkres.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "sample.dwg";

// Načtěte výkres CAD v instanci Image
using (var image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // Váš kód zde...
}
```

## Krok 2: Vytvořte BmpOptions

Vytvořte instanci třídy BmpOptions, která je zodpovědná za specifikaci možností při ukládání výkresu CAD jako souboru BMP.

```csharp
Aspose.CAD.ImageOptions.BmpOptions bmpOptions = new Aspose.CAD.ImageOptions.BmpOptions();
```

## Krok 3: Nastavte CadRasterizationOptions

Vytvořte instanci třídy CadRasterizationOptions a nakonfigurujte její vlastnosti pro vektorovou rasterizaci.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions cadRasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
bmpOptions.VectorRasterizationOptions = cadRasterizationOptions;
```

## Krok 4: Nastavte vlastnost UnitType

Nastavte vlastnost UnitType CadRasterizationOptions a určete typ jednotky pro změnu velikosti. V tomto příkladu je nastaven na Centimetr.

```csharp
cadRasterizationOptions.UnitType = Aspose.CAD.ImageOptions.UnitType.Centimeter;
```

## Krok 5: Nastavte vlastnost rozvržení

Určete rozvržení, která chcete zahrnout do výkresu se změněnou velikostí, nastavením vlastnosti Rozvržení.

```csharp
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## Krok 6: Export do BMP

Nakonec uložte rozvržení se změněnou velikostí jako soubor BMP pomocí metody Uložit.

```csharp
string outPath = sourceFilePath + ".bmp";
image.Save(outPath, bmpOptions);
```

Nyní jste úspěšně upravili velikost vašeho CAD výkresu pomocí Aspose.CAD for .NET!

## Závěr

V tomto tutoriálu jsme prošli procesem změny velikosti CAD výkresů v .NET pomocí Aspose.CAD. Dodržováním těchto kroků můžete tuto funkci bez problémů integrovat do svých aplikací a poskytovat tak bezproblémové uživatelské prostředí.

## Nejčastější dotazy

### Q1: Je Aspose.CAD for .NET kompatibilní se všemi formáty CAD?

 Odpověď 1: Aspose.CAD for .NET podporuje širokou škálu formátů CAD, včetně DWG, DXF, DWF a dalších. Zkontrolovat[dokumentace](https://reference.aspose.com/cad/net/) pro úplný seznam.

### Q2: Mohu změnit velikost více rozvržení současně?

A2: Ano, můžete změnit velikost více rozložení úpravou pole rozložení v CadRasterizationOptions.

### Q3: Kde mohu získat podporu pro Aspose.CAD pro .NET?

 A3: Navštivte[Fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) za podporu a pomoc komunity.

### Q4: Je k dispozici bezplatná zkušební verze?

 A4: Ano, můžete prozkoumat a[zkušební verze zdarma](https://releases.aspose.com/) vyhodnotit funkce Aspose.CAD pro .NET.

### Q5: Jak mohu získat dočasnou licenci pro Aspose.CAD for .NET?

 A5: Získejte dočasnou licenci pro testovací účely[tady](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
