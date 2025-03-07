---
title: Podporované prvky DGN v Aspose.CAD pro .NET
linktitle: Podporované prvky DGN
second_title: Aspose.CAD .NET – formát souborů CAD a BIM
description: Prozkoumejte výkonné funkce Aspose.CAD for .NET pro práci se soubory DGN. Postupujte podle našeho podrobného průvodce pro bezproblémovou práci s 2D a 3D prvky.
weight: 18
url: /cs/net/cad-features-and-support/supported-dgn-elements/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Podporované prvky DGN v Aspose.CAD pro .NET

## Úvod

Jste vývojář .NET a chcete bezproblémově pracovat se soubory DGN? Aspose.CAD for .NET poskytuje robustní řešení pro efektivní zpracování souborů DGN. V tomto tutoriálu se ponoříme do podporovaných prvků DGN a provedeme vás procesem práce s Aspose.CAD pro .NET.

## Předpoklady

Než začneme, ujistěte se, že máte následující:

- Základní znalost programování .NET.
- Visual Studio nainstalované na vašem počítači.
-  Knihovna Aspose.CAD for .NET, kterou si můžete stáhnout[tady](https://releases.aspose.com/cad/net/).

## Importovat jmenné prostory

Chcete-li nastartovat svůj projekt, importujte potřebné jmenné prostory do své aplikace .NET. Tento krok zajistí, že budete mít přístup k funkcím poskytovaným Aspose.CAD pro .NET.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.FileFormats.Dgn.DgnElements;
```

## Krok 1: Načtěte soubor DGN

Začněte načtením existujícího souboru DGN jako CadImage ve vaší aplikaci .NET.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Váš kód zde
}
```

## Krok 2: Iterujte prvky DGN

Iterujte prvky DGN pomocí smyčky foreach. Aspose.CAD for .NET poskytuje řadu typů prvků DGN, se kterými můžete pracovat.

```csharp
foreach (DgnDrawingElementBase element in dgnImage.Elements)
{
    // Váš kód zde
}
```

## Krok 3: Zacházení s dříve podporovanými entitami

Zvládněte dříve podporované 2D entity, které jsou nyní podporovány i pro 3D.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.Line:
    case DgnElementType.Ellipse:
    case DgnElementType.Curve:
    // Další případy
        {
            // Váš kód zde
            break;
        }
}
```

## Krok 4: Zacházení s podporovanými 3D entitami

Zvládněte podporované 3D entity poskytované Aspose.CAD pro .NET.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.SolidHeader3D:
    case DgnElementType.Cone:
    case DgnElementType.CellHeader:
        {
            // Váš kód zde
            break;
        }
}
```

## Krok 5: Exportujte a uložte

Nakonec exportujte upravený soubor DGN do rastrového obrázku a uložte jej do určeného adresáře.

```csharp
Console.WriteLine("\nThe DGN file exported successfully to raster image.\nFile saved at " + MyDir);
```

## Závěr

tomto tutoriálu jsme prozkoumali možnosti Aspose.CAD pro .NET při manipulaci a manipulaci se soubory DGN. Dodržováním tohoto podrobného průvodce můžete efektivně pracovat s podporovanými prvky DGN, ať už se jedná o 2D nebo 3D entity. Aspose.CAD for .NET vám umožňuje bezproblémově integrovat zpracování souborů DGN do vašich aplikací .NET.

## FAQ

### Q1: Kde najdu dokumentaci k Aspose.CAD pro .NET?

 A1: Můžete najít dokumentaci[tady](https://reference.aspose.com/cad/net/).

### Q2: Jak stáhnu Aspose.CAD pro .NET?

 A2: Můžete si stáhnout knihovnu[tady](https://releases.aspose.com/cad/net/).

### Q3: Je k dispozici bezplatná zkušební verze pro Aspose.CAD pro .NET?

 A3: Ano, máte přístup k bezplatné zkušební verzi[tady](https://releases.aspose.com/).

### Q4: Kde mohu získat dočasné licence pro Aspose.CAD pro .NET?

 A4: K dispozici jsou dočasné licence[tady](https://purchase.aspose.com/temporary-license/).

### Q5: Potřebujete pomoc nebo máte otázky?

 Odpověď 5: Navštivte komunitu Aspose.CAD for .NET[Fórum podpory](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
