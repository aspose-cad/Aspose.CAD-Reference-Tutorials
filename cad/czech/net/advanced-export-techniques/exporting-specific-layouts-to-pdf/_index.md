---
title: Export konkrétních rozvržení do PDF - Průvodce Aspose.CAD
linktitle: Export konkrétních rozvržení do PDF
second_title: Aspose.CAD .NET – formát souborů CAD a BIM
description: Naučte se exportovat konkrétní rozvržení do PDF pomocí Aspose.CAD for .NET. Podrobný průvodce pro bezproblémovou integraci.
weight: 13
url: /cs/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export konkrétních rozvržení do PDF - Průvodce Aspose.CAD

## Úvod

Vítejte v našem podrobném průvodci exportem konkrétních rozvržení do PDF pomocí Aspose.CAD pro .NET. Aspose.CAD je výkonná knihovna, která umožňuje vývojářům bezproblémově pracovat s formáty souborů CAD. V tomto tutoriálu se zaměříme na export konkrétních rozvržení ze souboru DWG do PDF pomocí Aspose.CAD v prostředí .NET.

## Předpoklady

Než se pustíme do výukového programu, ujistěte se, že máte splněny následující předpoklady:

-  Knihovna Aspose.CAD for .NET: Ujistěte se, že máte nainstalovanou knihovnu Aspose.CAD. Můžete si jej stáhnout[tady](https://releases.aspose.com/cad/net/).

- Vývojové prostředí: Nastavte vývojové prostředí .NET, jako je Visual Studio.

## Importovat jmenné prostory

Ve svém projektu .NET importujte potřebné jmenné prostory pro Aspose.CAD:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Krok 1: Načtěte soubor DWG

```csharp
// Cesta k adresáři dokumentů.
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";

using (Image image = Image.Load(sourceFilePath))
{
    // Váš kód pro další kroky je zde.
}
```

## Krok 2: Nastavte CadRasterizationOptions

```csharp
// Vytvořte instanci CadRasterizationOptions a nastavte její různé vlastnosti
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
```

## Krok 3: Zadejte název rozvržení

```csharp
// Zadejte požadovaný název rozvržení
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

## Krok 4: Vytvořte PdfOptions

```csharp
// Vytvořte instanci PdfOptions
PdfOptions pdfOptions = new PdfOptions();
// Nastavte vlastnost VectorRasterizationOptions
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Krok 5: Export do PDF

```csharp
MyDir = MyDir + "ExportSpecificLayoutToPDF_out.pdf";
// Exportujte DWG do PDF
image.Save(MyDir, pdfOptions);
```

## Krok 6: Zobrazte zprávu o úspěchu

```csharp
// Zobrazit zprávu o úspěchu
Console.WriteLine("\nThe DWG file with a specific layout exported successfully to PDF.\nFile saved at " + MyDir);
```

## Závěr

Gratulujeme! Úspěšně jste se naučili, jak exportovat konkrétní rozvržení do PDF pomocí Aspose.CAD for .NET. Tato příručka poskytuje podrobný návod a zajišťuje, že tuto funkci můžete bez námahy integrovat do svých projektů.

## FAQ

### Q1: Mohu exportovat více rozvržení současně?

 A1: Ano, jednoduše upravte`Layouts` pole v kroku 3 zahrnout názvy všech požadovaných rozložení.

### Q2: Je Aspose.CAD kompatibilní s jinými formáty souborů CAD?

Odpověď 2: Ano, Aspose.CAD podporuje různé formáty CAD, včetně DWG, DXF, DWF a dalších.

### Q3: Jak mohu upravit nastavení výstupu PDF?

 A3: Prozkoumejte vlastnosti`CadRasterizationOptions` v kroku 2 pro možnosti přizpůsobení.

### Q4: Kde najdu další dokumentaci Aspose.CAD?

 A4: Navštivte[dokumentace](https://reference.aspose.com/cad/net/) pro podrobné informace.

### Q5: Je k dispozici bezplatná zkušební verze?

 A5: Ano, máte přístup k bezplatné zkušební verzi[tady](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
