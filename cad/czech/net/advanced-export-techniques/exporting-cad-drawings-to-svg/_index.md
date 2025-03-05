---
title: Export výkresů CAD do formátu SVG - Průvodce Aspose.CAD
linktitle: Export výkresů CAD do formátu SVG
second_title: Aspose.CAD .NET – formát souborů CAD a BIM
description: Prozkoumejte bezproblémový proces exportu CAD výkresů do SVG pomocí Aspose.CAD for .NET. Vylepšete svůj vývoj CAD pomocí flexibility a přizpůsobení.
type: docs
weight: 15
url: /cs/net/advanced-export-techniques/exporting-cad-drawings-to-svg/
---
## Úvod

dynamickém světě CAD (Computer-Aided Design) je schopnost exportovat výkresy do různých formátů klíčovou dovedností. SVG (Scalable Vector Graphics) je jeden takový formát, který si získal oblibu díky své škálovatelnosti a všestrannosti. V tomto tutoriálu prozkoumáme, jak exportovat výkresy CAD do SVG pomocí výkonné knihovny Aspose.CAD for .NET.

## Předpoklady

Než se ponoříte do výukového programu, ujistěte se, že máte splněny následující předpoklady:

-  Knihovna Aspose.CAD for .NET: Stáhněte a nainstalujte knihovnu Aspose.CAD for .NET. Knihovnu najdete[tady](https://releases.aspose.com/cad/net/).

- Vývojové prostředí: Nastavte vhodné vývojové prostředí pomocí sady Visual Studio nebo jakéhokoli jiného vývojového nástroje .NET.

## Importovat jmenné prostory

Chcete-li začít, importujte do projektu potřebné jmenné prostory:

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Krok 1: Nastavte adresář dokumentů

```csharp
// Cesta k adresáři dokumentů.
string MyDir = "Your Document Directory";
```

## Krok 2: Načtěte výkres CAD

```csharp
using (Image image = Image.Load(MyDir + "sample.dwg"))
{
```

## Krok 3: Nakonfigurujte možnosti exportu SVG

```csharp
    var options = new SvgOptions();
    options.ColorType = SvgColorMode.Grayscale;
    options.TextAsShapes = true;
```

## Krok 4: Uložte soubor SVG

```csharp
    image.Save(MyDir + "sample.svg", options);
}
```

Pomocí těchto jednoduchých kroků můžete bezproblémově exportovat výkresy CAD do SVG pomocí Aspose.CAD for .NET. Knihovna poskytuje flexibilitu a možnosti přizpůsobení, což vám umožní přizpůsobit výstup podle vašich požadavků.

## Závěr

Závěrem lze říci, že Aspose.CAD for .NET zjednodušuje proces exportu CAD výkresů do SVG. Jeho intuitivní API a robustní funkce z něj dělají cenný nástroj pro vývojáře pracující s CAD aplikacemi.

## FAQ

### Q1: Je Aspose.CAD kompatibilní se všemi formáty CAD?

A1: Aspose.CAD podporuje různé formáty CAD, včetně DWG a DXF, což zajišťuje širokou kompatibilitu.

### Q2: Mohu přizpůsobit barevný režim při exportu do SVG?

Odpověď 2: Ano, Aspose.CAD vám umožňuje zvolit barevný režim a poskytuje flexibilitu ve výstupu.

### Q3: Jsou k dispozici dočasné licence pro testovací účely?

 A3: Ano, můžete získat dočasnou licenci[tady](https://purchase.aspose.com/temporary-license/) pro hodnocení.

### Q4: Kde najdu podrobnou dokumentaci k Aspose.CAD?

 A4: Dokumentace je k dispozici[tady](https://reference.aspose.com/cad/net/).

### Q5: Jak mohu získat podporu nebo klást otázky týkající se Aspose.CAD?

 A5: Navštivte fórum komunity[tady](https://forum.aspose.com/c/cad/19) za podporu a diskuze.