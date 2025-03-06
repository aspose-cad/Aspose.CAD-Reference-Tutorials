---
title: Vylepšete export CAD pomocí vlastních možností pera v Aspose.CAD pro .NET
linktitle: Podpora pera v exportu
second_title: Aspose.CAD .NET – formát souborů CAD a BIM
description: Naučte se, jak vylepšit exporty obrázků CAD pomocí Aspose.CAD for .NET. Přizpůsobte si možnosti pera pro ohromující vizuály v PDF, PNG, BMP a dalších.
weight: 12
url: /cs/net/cad-features-and-support/pen-support-in-export/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Vylepšete export CAD pomocí vlastních možností pera v Aspose.CAD pro .NET

## Úvod

Aspose.CAD for .NET poskytuje výkonnou sadu nástrojů pro práci se soubory CAD (Computer-Aided Design), která umožňuje vývojářům bezproblémově manipulovat a exportovat obrázky CAD. Jednou z pozoruhodných funkcí je podpora pera během exportu, která uživatelům umožňuje přizpůsobit nastavení začátku a konce pera při exportu obrázků CAD do různých formátů, jako je PDF, PNG, BMP, GIF, JPEG2000, JPEG, PSD, TIFF a WMF.

V tomto tutoriálu se ponoříme do specifik podpory pera při exportu pomocí Aspose.CAD pro .NET. Každý krok rozebereme a poskytneme jasná vysvětlení a příklady, které vás celým procesem provedou.

## Předpoklady

Než se pustíme do výukového programu, ujistěte se, že máte splněny následující předpoklady:

- Aspose.CAD for .NET nainstalovaný ve vašem vývojovém prostředí. Můžete si jej stáhnout z[stránka vydání](https://releases.aspose.com/cad/net/).

- Základní znalost formátů souborů CAD, zejména DXF (Drawing Exchange Format).

- Pracovní znalost programovacího jazyka C#.

## Importovat jmenné prostory

Chcete-li začít, ujistěte se, že jste do svého projektu C# importovali potřebné jmenné prostory:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Drawing;
using System.Drawing.Drawing2D;
```

## Krok 1: Nastavte adresář dokumentů

Definujte adresář, kde je umístěn váš CAD dokument:

```csharp
string MyDir = "Your Document Directory";
```

## Krok 2: Načtěte obrázek CAD

Načtěte obrázek CAD pomocí Aspose.CAD:

```csharp
string sourceFilePath = MyDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage)Image.Load(sourceFilePath);
```

## Krok 3: Nakonfigurujte možnosti rastrování

Vytvořte možnosti rasterizace a PDF pro přizpůsobení procesu exportu:

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
PdfOptions pdfOptions = new PdfOptions();
```

## Krok 4: Přizpůsobte možnosti pera

Nastavte možnosti začátku a konce pro pera:

```csharp
rasterizationOptions.PenOptions = new PenOptions
{
   StartCap = LineCap.Flat,
   EndCap = LineCap.Flat
};
```

## Krok 5: Použijte možnosti vektorové rastrování

Použijte možnosti rastrování na možnosti PDF:

```csharp
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Krok 6: Uložte exportovaný soubor PDF

Uložte obrázek CAD s přizpůsobenými možnostmi pera jako soubor PDF:

```csharp
cadImage.Save(MyDir + "9LHATT-A56_generated.pdf", pdfOptions);
```

## Závěr

V tomto tutoriálu jsme prozkoumali podporu pera ve funkci exportu Aspose.CAD pro .NET. Podle tohoto podrobného průvodce můžete snadno přizpůsobit nastavení začátku a konce pro pera, čímž zvýšíte flexibilitu exportu obrázků CAD.

Nebojte se experimentovat s různými možnostmi pera, abyste dosáhli požadovaných vizuálních efektů v exportovaných obrázcích.

## FAQ

### Q1: Mohu použít tyto možnosti pera pro jiné formáty obrázků kromě PDF?

Odpověď 1: Ano, možnosti pera lze použít na různé formáty obrázků, jako je PNG, BMP, GIF, JPEG a další.

### Q2: Kde najdu další dokumentaci k Aspose.CAD pro .NET?

 A2: Viz[dokumentace](https://reference.aspose.com/cad/net/) pro vyčerpávající informace a příklady.

### Q3: Je k dispozici bezplatná zkušební verze pro Aspose.CAD pro .NET?

 A3: Ano, máte přístup k bezplatné zkušební verzi[tady](https://releases.aspose.com/).

### Q4: Jak mohu získat dočasné licence pro Aspose.CAD pro .NET?

 A4: Navštivte[dočasná licenční stránka](https://purchase.aspose.com/temporary-license/) pro dočasné licenční možnosti.

### Q5: Kde mohu hledat podporu komunity pro Aspose.CAD pro .NET?

 A5: Zapojte se do komunity na[Fórum Aspose.CAD](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
