---
title: Export souborů IFC do PNG - Výukový program Aspose.CAD
linktitle: Export souborů IFC do PNG
second_title: Aspose.CAD .NET – formát souborů CAD a BIM
description: Prozkoumejte Aspose.CAD for .NET, robustní řešení pro bezproblémový převod IFC na PNG. Stáhněte si nyní pro efektivní zpracování souborů CAD.
type: docs
weight: 10
url: /cs/net/exporting-to-image-formats/exporting-ifc-files-to-png/
---
## Úvod

dynamickém světě počítačově podporovaného navrhování (CAD) je efektivní převod souborů zásadní. Aspose.CAD for .NET se ukazuje jako výkonný nástroj, který nabízí bezproblémové možnosti pro export souborů IFC (Industry Foundation Classes) do formátu PNG. Tento tutoriál vás krok za krokem provede celým procesem a zajistí hladký průběh práce s Aspose.CAD.

## Předpoklady

Než se pustíte do výukového programu, ujistěte se, že máte splněny následující předpoklady:

### 1. Instalace Aspose.CAD

 Ujistěte se, že máte nainstalovaný Aspose.CAD for .NET. Můžete si jej stáhnout ze stránky vydání[tady](https://releases.aspose.com/cad/net/).

### 2. Adresář dokumentů

 Vytvořte určený adresář pro vaše dokumenty. V uvedeném příkladu proměnná`MyDir` představuje adresář dokumentů.

## Importovat jmenné prostory

Nyní, když máte nastavené předpoklady, pojďme importovat potřebné jmenné prostory do vaší .NET aplikace, abyste mohli používat funkce Aspose.CAD.

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using Aspose.CAD.FileFormats.Ifc;
```

## Krok 1: Načtěte soubor IFC

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "example.ifc";
using (IfcImage cadImage = (IfcImage)Image.Load(sourceFilePath))
{
```

 V tomto kroku inicializujeme Aspose.CAD`IfcImage` objekt a načtěte do něj soubor IFC.

## Krok 2: Nastavte možnosti rastrování

```csharp
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
   
    rasterizationOptions.PageWidth = 100;
    rasterizationOptions.PageHeight = 100;
```

Definujte volby rastrování pro konfiguraci šířky a výšky stránky pro výstup PNG.

## Krok 3: Nastavte možnosti PNG

```csharp
    PngOptions pngOptions = new PngOptions();
    pngOptions.VectorRasterizationOptions = rasterizationOptions;
```

Vytvořte možnosti PNG a přiřaďte dříve definované možnosti rastrování.

## Krok 4: Zadejte výstupní cestu

```csharp
    // Nastavte také výstupní cestu
    string outPath = sourceFilePath + ".png";
    cadImage.Save(outPath, pngOptions);
}
```

Definujte výstupní cestu pro soubor PNG a ujistěte se, že má stejný název jako zdrojový soubor s příponou „.png“. Nakonec převedený obrázek uložte.

## Závěr

Pomocí těchto jednoduchých kroků jste úspěšně exportovali soubor IFC do PNG pomocí Aspose.CAD for .NET. Tento všestranný nástroj zjednodušuje proces konverze CAD a zpřístupňuje jej vývojářům a inženýrům.

## FAQ

### Otázka 1: Mohu používat Aspose.CAD for .NET na macOS nebo Linux?

Odpověď 1: Ne, Aspose.CAD for .NET je speciálně navržen pro prostředí Windows.

### Q2: Je k dispozici dočasná licence pro testovací účely?

 A2: Ano, můžete získat dočasnou licenci od[tady](https://purchase.aspose.com/temporary-license/) pro hodnocení.

### Q3: Jak mohu získat podporu pro Aspose.CAD?

 A3: Navštivte[Fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) za podporu komunity a diskuze.

### Q4: Kde najdu komplexní dokumentaci?

 A4: Viz[Dokumentace Aspose.CAD](https://reference.aspose.com/cad/net/) pro podrobné informace a příklady.

### Q5: Co když se během instalace vyskytnou problémy?

 Odpověď 5: Zkontrolujte dokumentaci nebo vyhledejte pomoc na stránce[Fórum Aspose.CAD](https://forum.aspose.com/c/cad/19).