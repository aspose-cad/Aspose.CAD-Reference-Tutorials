---
title: Export DGN do rastrového obrázku v Aspose.CAD pro .NET
linktitle: Export DGN do rastrového obrázku
second_title: Aspose.CAD .NET – formát souborů CAD a BIM
description: Převeďte DGN na rastrové obrázky bez námahy pomocí Aspose.CAD pro .NET. Prozkoumejte průvodce krok za krokem a uvolněte sílu .NET při manipulaci se soubory CAD.
type: docs
weight: 13
url: /cs/net/cad-export-formats/export-dgn-to-raster-image/
---
## Úvod

V dynamické sféře vývoje .NET se Aspose.CAD ukazuje jako výkonný nástroj pro práci se soubory CAD (Computer-Aided Design). Tento tutoriál se ponoří do procesu exportu souborů DGN do rastrových obrázků pomocí Aspose.CAD for .NET. Pokud máte zájem o bezproblémovou transformaci souborů DGN na vizuálně působivé rastrové obrázky, jste na správném místě.

## Předpoklady

Než se vydáme na tuto cestu, ujistěte se, že máte splněny následující předpoklady:

-  Aspose.CAD for .NET: Ujistěte se, že máte v projektu .NET nainstalovanou knihovnu Aspose.CAD. Knihovnu a příslušnou dokumentaci najdete na[webová stránka](https://reference.aspose.com/cad/net/).

- Ukázkový soubor DGN: Připravte si soubor DGN pro převod. V našem příkladu použijeme "Nikon_D90_Camera.dgn."

Nyní se pojďme ponořit do podrobného průvodce.

## Importovat jmenné prostory

Ve svém projektu .NET začněte importováním potřebných jmenných prostorů pro Aspose.CAD. Tento krok vám umožní přístup ke třídám a metodám požadovaným pro převod DGN na rastrový obrázek.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Krok 1: Načtěte soubor DGN

 Začněte načtením souboru DGN do a`CadImage` objekt. To poskytuje základ pro další operace.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Zde je váš kód pro další zpracování
}
```

## Krok 2: Definujte možnosti rastrování

 Vytvořit`CadRasterizationOptions` objekt a nastavit různé vlastnosti pro přizpůsobení procesu rasterizace podle vašich požadavků.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## Krok 3: Vytvořte objekt JpegOptions

 Protože se snažíme převést soubor DGN na JPEG, vytvořte a`JpegOptions` objekt a přiřadit dříve definovaný`CadRasterizationOptions` k tomu.

```csharp
ImageOptionsBase options = new JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
```

## Krok 4: Uložte rastrový obrázek

 Využijte`Save` metoda`CadImage` třídy pro export souboru DGN do rastrového obrázku v požadovaném formátu, v tomto případě JPEG.

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpg", options);
```

## Závěr

Gratulujeme! Úspěšně jste prošli kroky k exportu souboru DGN do rastrového obrázku pomocí Aspose.CAD for .NET. Tento výukový program vás vybavil základními znalostmi pro snadnou integraci této funkce do vašich projektů .NET.

## FAQ

### Q1: Mohu exportovat soubory DGN do jiných formátů než JPEG?

A1: Ano, Aspose.CAD for .NET podporuje různé výstupní formáty. V kroku 3 můžete odpovídajícím způsobem upravit možnosti.

### Q2 Jak mohu zpracovat výjimky během procesu převodu?

A2: Ujistěte se, že máte správné zpracování výjimek, jak je ukázáno v poskytnutém kódu, abyste řešili potenciální problémy.

### Q3: Je k dispozici zkušební verze pro Aspose.CAD pro .NET?

 A3: Ano, produkt můžete prozkoumat pomocí bezplatné zkušební verze. Návštěva[tady](https://releases.aspose.com/) Pro více informací.

### Q4: Kde mohu vyhledat pomoc nebo projednat problémy související s Aspose.CAD for .NET?

 A4: Přejděte na[Fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) za podporu komunity a diskuze.

### Q5: Jak získám dočasnou licenci pro Aspose.CAD for .NET?

 A5: Návštěva[tento odkaz](https://purchase.aspose.com/temporary-license/)získat dočasnou licenci pro vaše vývojové potřeby.