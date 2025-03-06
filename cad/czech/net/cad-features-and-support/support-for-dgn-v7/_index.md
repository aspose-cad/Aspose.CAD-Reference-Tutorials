---
title: Podpora DGN V7 v Aspose.CAD pro .NET
linktitle: Podpora pro DGN V7
second_title: Aspose.CAD .NET – formát souborů CAD a BIM
description: Prozkoumejte bezproblémovou podporu Aspose.CAD for .NET pro DGN V7. Převeďte soubory DGN na rastrové obrázky bez námahy pomocí podrobného návodu.
weight: 19
url: /cs/net/cad-features-and-support/support-for-dgn-v7/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Podpora DGN V7 v Aspose.CAD pro .NET

## Úvod

oblasti vývoje .NET vyniká Aspose.CAD jako výkonná knihovna pro práci se soubory CAD (Computer-Aided Design). Tento výukový program se ponoří do specifické funkce Aspose.CAD pro .NET – podpory souborů DGN V7. DGN, zkratka pro Design, je široce používaný formát souborů v doméně CAD. Aspose.CAD zjednodušuje proces práce se soubory DGN V7 a nabízí vývojářům bezproblémový zážitek.

## Předpoklady

Než se pustíme do implementace, ujistěte se, že máte splněny následující předpoklady:

-  Aspose.CAD for .NET: Ujistěte se, že máte nainstalovanou knihovnu Aspose.CAD. Můžete si jej stáhnout z[webová stránka](https://releases.aspose.com/cad/net/).

- Vývojové prostředí: Nastavte funkční vývojové prostředí .NET, včetně sady Visual Studio nebo jakéhokoli jiného preferovaného IDE.

Nyní, když máme seřazené předpoklady, pojďme prozkoumat, jak využít podporu pro DGN V7 v Aspose.CAD pro .NET.

## Importovat jmenné prostory

Začněte importem potřebných jmenných prostorů pro přístup k funkcím Aspose.CAD:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Krok 1: Načtěte soubor DGN

 Začněte načtením existujícího souboru DGN jako a`CadImage` Nahradit`"Your Document Directory"` a`"Nikon_D90_Camera.dgn"` s příslušnou cestou k adresáři a názvem souboru.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Kód pro další kroky najdete zde...
}
```

## Krok 2: Nakonfigurujte možnosti rastrování

 Vytvořit`CadRasterizationOptions` objekt pro definování a nastavení různých vlastností souvisejících s rasterizací.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions
{
    PageWidth = 600,
    PageHeight = 300,
    NoScaling = true,
    AutomaticLayoutsScaling = false
};
```

## Krok 3: Nastavte možnosti vektorového rastrování

 Vytvořit`JpegOptions` objekt, protože máme v úmyslu převést soubor DGN na JPEG. Přiřadit dříve vytvořené`CadRasterizationOptions` namítat proti tomu.

```csharp
ImageOptionsBase options = new JpegOptions
{
    VectorRasterizationOptions = rasterizationOptions
};
```

## Krok 4: Uložte rastrovaný obrázek

 Zavolej`Save` metoda`CadImage` class objekt pro export souboru DGN do rastrového obrázku, v tomto případě JPEG.

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpeg", options);
```

Po dokončení těchto kroků je soubor DGN úspěšně exportován do rastrového obrázku.

## Závěr

V tomto tutoriálu jsme prozkoumali bezproblémovou podporu pro DGN V7 v Aspose.CAD pro .NET. Podle tohoto podrobného průvodce mohou vývojáři bez námahy převádět soubory DGN na rastrové obrázky, čímž rozšiřují možnosti svých aplikací .NET.

## FAQ

### Q1: Je Aspose.CAD kompatibilní s nejnovějšími specifikacemi DGN V7?

Odpověď 1: Ano, Aspose.CAD je navržen tak, aby bezproblémově zpracovával soubory DGN V7 a zajistil kompatibilitu s nejnovějšími specifikacemi.

### Q2: Mohu přizpůsobit možnosti rasterizace pro převod souborů DGN?

 A2: Rozhodně. Tutoriál ukazuje, jak vytvořit a nakonfigurovat`CadRasterizationOptions` přizpůsobit proces konverze.

### Q3: Existují jiné podporované výstupní formáty kromě JPEG?

A3: Ano, Aspose.CAD podporuje různé výstupní formáty. Kompletní seznam si můžete prohlédnout v dokumentaci.

### Q4: Jak mohu získat podporu pro dotazy související s Aspose.CAD?

 A4: Navštivte[Fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) za podporu komunity a diskuze.

### Q5: Je k dispozici bezplatná zkušební verze pro Aspose.CAD pro .NET?

 A5: Ano, máte přístup k bezplatné zkušební verzi[tady](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
