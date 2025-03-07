---
title: Export 3D obrázků do PDF - Aspose.CAD Tutorial
linktitle: Export 3D obrázků do PDF
second_title: Aspose.CAD .NET – formát souborů CAD a BIM
description: Bez námahy převádějte 3D obrázky CAD do PDF pomocí Aspose.CAD pro .NET. Postupujte podle našeho podrobného návodu pro bezproblémový export PDF.
weight: 10
url: /cs/net/3d-image-export/exporting-3d-images-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export 3D obrázků do PDF - Aspose.CAD Tutorial

## Úvod

Hledáte bezproblémový export 3D obrázků do PDF pomocí Aspose.CAD pro .NET? Tento tutoriál vás krok za krokem provede celým procesem a zajistí, že využijete sílu Aspose.CAD k snadnému převodu 3D obrázků do formátu PDF.

## Předpoklady

Než se pustíte do výukového programu, ujistěte se, že máte splněny následující předpoklady:

-  Aspose.CAD for .NET: Ujistěte se, že máte nainstalovanou knihovnu Aspose.CAD pro .NET. Pokud ne, můžete si jej stáhnout z[Stránka ke stažení Aspose.CAD for .NET](https://releases.aspose.com/cad/net/).

- Adresář dokumentů: Nastavte adresář, kde jsou uloženy vaše CAD soubory, a poznamenejte si cestu.

## Importovat jmenné prostory

Do svého .NET projektu importujte potřebné jmenné prostory pro práci s Aspose.CAD. Přidejte následující řádky na začátek souboru kódu:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

## Krok 1: Načtěte obrázek CAD

 Začněte načtením obrázku CAD, který chcete exportovat do PDF. Použijte`Load` metoda z knihovny Aspose.CAD. Nahradit`"conic_pyramid.dxf"` s cestou k vašemu CAD souboru.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image cadImage = Image.Load(sourceFilePath))
{
    // Zde je váš kód pro načtení obrázku CAD
}
```

## Krok 2: Nakonfigurujte možnosti rastrování

 Nakonfigurujte možnosti rastrování pro obrázek CAD. Nastavte parametry, jako je šířka stránky, výška stránky a rozvržení. Odkomentujte související řádek`TypeOfEntities` pokud jsou vaše entity 3D.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
// rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;

rasterizationOptions.Layouts = new string[] { "Model" };
```

## Krok 3: Nastavte možnosti PDF

Vytvořte volby PDF a spojte je s volbami rastrování.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Krok 4: Uložit jako PDF

Uložte obrázek CAD jako soubor PDF pomocí nakonfigurovaných možností. Zadejte výstupní cestu pro soubor PDF.

```csharp
MyDir = MyDir + "Export3DImagestoPDF_out.pdf";
cadImage.Save(MyDir, pdfOptions);
```

## Závěr

Gratulujeme! Úspěšně jste exportovali 3D obrázky do PDF pomocí Aspose.CAD for .NET. Tento přímočarý výukový program zajišťuje, že bez námahy převedete soubory CAD do dostupnějšího formátu.

## FAQ

### Q1: Je Aspose.CAD kompatibilní se všemi formáty souborů CAD?

Odpověď 1: Ano, Aspose.CAD podporuje širokou škálu formátů CAD, což zajišťuje flexibilitu při manipulaci s různými typy souborů.

### Q2: Mohu přizpůsobit rozměry stránky při exportu do PDF?

A2: Rozhodně. Výukový program ukazuje, jak nakonfigurovat šířku a výšku stránky podle vašich požadavků.

### Q3: Jsou k dispozici dočasné licence pro Aspose.CAD?

 A3: Ano, můžete získat dočasné licence pro Aspose.CAD návštěvou[Dočasná licence](https://purchase.aspose.com/temporary-license/).

### Q4: Kde najdu další podporu nebo komunitní diskuse?

 A4: Zamiřte na[Fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) za podporu a spolupráci s komunitou.

### Q5: Je k dispozici bezplatná zkušební verze Aspose.CAD?

 A5: Ano, můžete prozkoumat funkce Aspose.CAD přístupem k[zkušební verze zdarma](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
