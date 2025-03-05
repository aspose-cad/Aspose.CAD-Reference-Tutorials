---
title: Získejte velikost rozložení CAD v Aspose.CAD pro .NET
linktitle: Získejte velikost rozložení CAD
second_title: Aspose.CAD .NET – formát souborů CAD a BIM
description: Naučte se, jak načíst velikost rozvržení CAD v .NET pomocí Aspose.CAD. Postupujte podle našeho podrobného průvodce pro efektivní manipulaci se soubory CAD.
type: docs
weight: 14
url: /cs/net/cad-drawing-manipulation/get-size-of-cad-layout/
---
## Úvod

Vítejte v tomto komplexním průvodci o získání velikosti rozvržení CAD pomocí Aspose.CAD pro .NET. Aspose.CAD je výkonná knihovna, která umožňuje vývojářům bezproblémově pracovat se soubory CAD. V tomto tutoriálu vás provedeme procesem načítání velikosti rozvržení CAD pomocí praktických příkladů a podrobných pokynů.

## Předpoklady

Než se pustíme do výukového programu, ujistěte se, že máte splněny následující předpoklady:

-  Aspose.CAD for .NET: Ujistěte se, že máte nainstalovanou knihovnu Aspose.CAD. Můžete si jej stáhnout z[Stránka ke stažení Aspose.CAD for .NET](https://releases.aspose.com/cad/net/).

- Soubory dokumentů: Připravte si soubory CAD, se kterými chcete pracovat. Tento tutoriál používá jako příklady "conic_pyramid.dxf" a "Bottom_plate.dwg".

Tak pojďme začít!

## Importovat jmenné prostory

Ve svém projektu .NET začněte importováním potřebných jmenných prostorů:

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.ImageOptions;
```

## Krok 1: Nastavte adresář dokumentů

 Nastavte cestu k adresáři dokumentů. Nahradit`"Your Document Directory"` se skutečnou cestou.

```csharp
string MyDir = "Your Document Directory";
```

## Krok 2: Určete cesty souboru CAD

Definujte pole cest k souborům CAD, které chcete analyzovat. V tomto příkladu používáme "conic_pyramid.dxf" a "Bottom_plate.dwg."

```csharp
string[] sourceFilePaths = new[]
{
    MyDir + "conic_pyramid.dxf",
    MyDir + "Bottom_plate.dwg"
};
```

## Krok 3: Iterace přes soubory CAD

Iterujte každý soubor CAD a načtěte informace o rozvržení.

```csharp
foreach (var sourceFilePath in sourceFilePaths)
{
    string extension = Path.GetExtension(sourceFilePath);
    using (CadImage cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath))
    {
        // ... (pokračujte na další krok)
    }
}
```

## Krok 4: Získejte neprázdná rozvržení

Definujte pomocnou metodu pro získání neprázdných rozvržení na základě typu souboru CAD.

```csharp
private static List<string> GetNotEmptyLayouts(Image cadImage, string extension)
{
    // ... (pokračujte na další krok)
}
```

## Krok 5: Získejte rozvržení pro soubory DWG

Implementujte logiku pro načtení neprázdných rozvržení pro soubory DWG.

```csharp
private static List<string> GetNotEmptyLayoutsForDwg(CadImage cadImage)
{
    // ... (pokračujte na další krok)
}
```

## Krok 6: Získejte rozvržení pro soubory DXF

Implementujte logiku pro načtení neprázdných rozvržení pro soubory DXF.

```csharp
private static List<string> GetNotEmptyLayoutsForDxf(CadImage cadImage)
{
    // ... (pokračujte na další krok)
}
```

## Krok 7: Načtěte velikost rozvržení a uložte jako obrázek

Dokončete proces získání velikosti rozvržení a jeho uložení jako obrázku.

```csharp
foreach (string layout in layouts)
{
    // ... (pokračujte na další krok)
}
```

## Závěr

Gratulujeme! Úspěšně jste se naučili, jak získat velikost rozvržení CAD pomocí Aspose.CAD pro .NET. Tento výukový program se zabýval základními kroky, od nastavení projektu až po načtení informací o rozložení a uložení jako obrázek. Nyní můžete tyto znalosti začlenit do svých aplikací .NET pro efektivní manipulaci se soubory CAD.

## FAQ

### Q1: Je Aspose.CAD kompatibilní se všemi formáty souborů CAD?

Odpověď 1: Ano, Aspose.CAD podporuje různé formáty souborů CAD, včetně DWG a DXF.

### Q2: Mohu přizpůsobit možnosti ukládání obrázků?

A2: Rozhodně! Možnosti obrazu, jako je formát a rozlišení, můžete upravit tak, aby vyhovovaly vašim specifickým požadavkům.

### Q3: Kde najdu další dokumentaci?

 A3: Viz[Dokumentace Aspose.CAD](https://reference.aspose.com/cad/net/) pro podrobné informace a příklady.

### Q4: Je k dispozici bezplatná zkušební verze?

 A4: Ano, můžete prozkoumat Aspose.CAD pomocí a[zkušební verze zdarma](https://releases.aspose.com/).

### Q5; Jak mohu získat technickou podporu?

 A5: Pro technickou podporu navštivte[Fórum Aspose.CAD](https://forum.aspose.com/c/cad/19).