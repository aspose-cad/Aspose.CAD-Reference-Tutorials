---
date: 2026-08-17
description: Naučte se, jak přidat obrázek do souborů DWG pomocí C# a Aspose.CAD pro
  .NET. Tento průvodce vás provede importem obrázků, nastavením vkládacích bodů a
  exportem do PDF.
keywords:
- add image to dwg
- convert dwg to pdf
- set insertion point dwg
- embed png in dwg
- save dwg as pdf
lastmod: 2026-08-17
linktitle: Import obrázků do souborů DWG pomocí C#
og_description: Naučte se, jak přidat obrázek do souborů DWG pomocí C#. Tento tutoriál
  zahrnuje import obrázků, nastavení vkládacích bodů a převod DWG do PDF pomocí Aspose.CAD.
og_image_alt: Guide showing C# code to embed an image into a DWG file using Aspose.CAD
og_title: Jak přidat obrázek do souborů DWG pomocí C# a Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-08-17'
  description: Learn how to add image to dwg files using C# and Aspose.CAD for .NET.
    This guide walks you through importing images, setting insertion points, and exporting
    to PDF.
  headline: How to add image to dwg files with C# using Aspose.CAD
  type: TechArticle
- description: Learn how to add image to dwg files using C# and Aspose.CAD for .NET.
    This guide walks you through importing images, setting insertion points, and exporting
    to PDF.
  name: How to add image to dwg files with C# using Aspose.CAD
  steps:
  - name: set up your document directory
    text: Prepare the folder that contains the source DWG and the image you want to
      embed.
  - name: load the dwg file
    text: The `CadImage` class represents a DWG drawing and provides access to its
      entities, layers, and metadata.
  - name: define the image properties
    text: Create an `Image` object that points to the raster file (e.g., PNG) and
      specify its format.
  - name: set insertion point dwg and vectors
    text: Specify where the image should appear inside the drawing and how it should
      be scaled. The insertion point is defined by a 2‑D coordinate, while the vectors
      control width and height.
  - name: create and configure the raster image
    text: Instantiate a `RasterImage` object, assign the image data, and set any additional
      rendering options.
  - name: add image to dwg file
    text: Insert the configured raster image into the DWG’s entities collection so
      it becomes part of the drawing.
  - name: save as pdf (export dwg to pdf)
    text: After embedding the image you can **convert dwg to pdf** or **save dwg as
      pdf** with a single call. This is useful for sharing the drawing with stakeholders
      who don’t have CAD software.
  type: HowTo
- questions:
  - answer: The core library is .NET‑specific, but Aspose offers equivalent APIs for
      Java, Python and other platforms.
    question: Can I use Aspose.CAD for .NET with other programming languages?
  - answer: Yes, you can explore a free trial on the [Aspose free trial page](https://releases.aspose.com/).
    question: Is a free trial available for Aspose.CAD?
  - answer: The documentation is available in the [Aspose.CAD .NET API reference](https://reference.aspose.com/cad/net/).
    question: Where can I find detailed documentation for Aspose.CAD?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to get a temporary license.
    question: How do I obtain a temporary license for Aspose.CAD?
  - answer: Yes, you can seek support and engage with the community in the [Aspose.CAD
      community forum](https://forum.aspose.com/c/cad/19).
    question: Are there community forums for Aspose.CAD support?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- CAD
- Aspose.CAD
- C# image processing
- DWG manipulation
title: Jak přidat obrázek do souborů DWG pomocí C# a Aspose.CAD
url: /cs/net/image-manipulation-and-rendering/importing-images-into-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak přidat obrázek do souborů DWG pomocí C# a Aspose.CAD

## Úvod

Přidání obrázku do souboru DWG je běžná potřeba, když potřebujete obohatit CAD výkresy o loga, fotografie nebo rastrovou grafiku. V tomto tutoriálu se naučíte, jak **add image to dwg** programově pomocí C# a Aspose.CAD pro .NET, a případně převést výsledek do PDF. Kroky jsou rozděleny tak, aby bylo možné zkopírovat‑vložit každou část do vlastního projektu.

## Rychlé odpovědi
- **Která knihovna provádí úkol?** Aspose.CAD for .NET.
- **Mohu vložit soubory PNG?** Ano – PNG, JPEG, BMP a další rastrové formáty jsou podporovány.
- **Potřebuji licenci pro vývoj?** Bezplatná zkušební verze funguje pro testování; pro produkci je vyžadována komerční licence.
- **Je podpora exportu do PDF?** Rozhodně – můžete převést aktualizovaný DWG do PDF jedním řádkem.
- **Jaké verze .NET jsou kompatibilní?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7.

## Co je soubor DWG?

DWG je nativní binární formát pro výkresy Autodesk AutoCAD, který ukládá vektorovou geometrie, vrstvy a metadata. Je široce používán v architektuře, inženýrství a stavebnictví a Aspose.CAD jej dokáže číst i zapisovat bez nutnosti mít nainstalovaný AutoCAD.

## Proč přidat obrázek do DWG pomocí Aspose.CAD?

Aspose.CAD podporuje **více než 50 vstupních a výstupních formátů**, dokáže zpracovat soubory větší než 500 MB bez načítání celého dokumentu do paměti a poskytuje deterministické API, které funguje v headless serverových prostředích. To umožňuje rychlé a spolehlivé hromadné zpracování DWG výkresů.

## Požadavky
- Základní znalost programování v C#.
- Aspose.CAD for .NET nainstalováno. Můžete jej stáhnout ze [Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/). Další produkty Aspose můžete prozkoumat na [Aspose releases page](https://releases.aspose.com/).
- Vývojové prostředí, například Visual Studio 2022 nebo novější.

## Jak přidat obrázek do DWG pomocí Aspose.CAD?

Načtěte cílový DWG, vytvořte objekt rastrového obrázku, který popisuje obrázek, který chcete vložit, nastavte vkládací bod a škálovací vektory a poté připojte obrázek k výkresu. Nakonec uložte upravený DWG nebo jej přímo exportujte do PDF. Celý postup vyžaduje jen několik volání API a běží pod jednou sekundou pro typické dvoustránkové výkresy.

### Importujte jmenné prostory
Zahrňte jmenné prostory, které vystavují třídy CAD, jež budete potřebovat.

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

### Krok 1: nastavení adresáře dokumentu
Připravte složku, která obsahuje zdrojový DWG a obrázek, který chcete vložit.

```csharp
string MyDir = "Your Document Directory";
```

### Krok 2: načtení souboru DWG
Třída `CadImage` představuje DWG výkres a poskytuje přístup k jeho entitám, vrstvám a metadatům.

```csharp
string dwgPathToFile = MyDir + "Drawing11.dwg";
CadImage cadImage1 = (CadImage)Image.Load(dwgPathToFile);
```

### Krok 3: definování vlastností obrázku
Vytvořte objekt `Image`, který ukazuje na rastrový soubor (např. PNG) a určete jeho formát.

```csharp
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.ObjectHandle = "A3B4";
```

### Krok 4: nastavení vkládacího bodu DWG a vektorů
Určete, kde se má obrázek ve výkresu objevit a jak má být měřítkován. Vkládací bod je definován 2‑D souřadnicí, zatímco vektory řídí šířku a výšku.

```csharp
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

### Krok 5: vytvoření a konfigurace rastrového obrázku
Instanciujte objekt `RasterImage`, přiřaďte data obrázku a nastavte případné další možnosti renderování.

```csharp
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.ImageDefReference = "A3B4";
cadRasterImage.DisplayFlags = 7;
cadRasterImage.ClippingState = 0;
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(639.5, 561.5));
```

### Krok 6: přidání obrázku do souboru DWG
Vložte nakonfigurovaný rastrový obrázek do kolekce entit DWG, aby se stal součástí výkresu.

```csharp
CadImage cadImage = (CadImage)cadImage1;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadRasterImage);

List<CadBaseObject> list = new List<CadBaseObject>(cadImage.Objects);
list.Add(cadRasterImageDef);
cadImage.Objects = list.ToArray();
```

### Krok 7: uložení jako PDF (export DWG do PDF)
Po vložení obrázku můžete **convert dwg to pdf** nebo **save dwg as pdf** jedním voláním. To je užitečné pro sdílení výkresu se zúčastněnými stranami, které nemají CAD software.

```csharp
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;

cadRasterizationOptions.PageHeight = 1600;
cadRasterizationOptions.PageWidth = 1600;
cadRasterizationOptions.Layouts = new string[] { "Model" };
cadImage1.Save(MyDir + "export2.pdf", pdfOptions);
```

## Jak převést DWG do PDF po vložení obrázku?

Zavolejte metodu `Save` na instanci `CadImage`, předáte `SaveFormat.Pdf` a volitelně objekt `PdfOptions` pro kontrolu velikosti stránky, rasterizace a metadat. Aspose.CAD zachovává vložený rastrový obrázek, vrstvy a tloušťky čar, čímž vytváří věrnou PDF reprezentaci, kterou lze otevřít v libovolném prohlížeči. Tento převod je proveden jediným řádkem kódu.

## Časté problémy a řešení
- **Obrázek se zobrazuje na špatném místě** – dvojitě zkontrolujte souřadnice vkládacího bodu a směrové vektory; jsou relativní k počátku výkresu.
- **Velké obrázky způsobují špičky v paměti** – použijte možnost `Resize` na rastrovém obrázku před vložením nebo pracujte s kopií nižšího rozlišení.
- **Export do PDF ztrácí vektorovou kvalitu** – ujistěte se, že ukládáte s `PdfOptions`, které zachovávají vektorová data; rastrové obrázky jsou vždy vloženy tak, jak jsou.

## Často kladené otázky

**Q: Mohu použít Aspose.CAD pro .NET s jinými programovacími jazyky?**  
A: Jádrová knihovna je specifická pro .NET, ale Aspose nabízí ekvivalentní API pro Java, Python a další platformy.

**Q: Je k dispozici bezplatná zkušební verze Aspose.CAD?**  
A: Ano, můžete si vyzkoušet bezplatnou verzi na [Aspose free trial page](https://releases.aspose.com/).

**Q: Kde najdu podrobnou dokumentaci k Aspose.CAD?**  
A: Dokumentace je k dispozici v [Aspose.CAD .NET API reference](https://reference.aspose.com/cad/net/).

**Q: Jak získat dočasnou licenci pro Aspose.CAD?**  
A: Navštivte [temporary license page](https://purchase.aspose.com/temporary-license/) a získejte dočasnou licenci.

**Q: Existují komunitní fóra pro podporu Aspose.CAD?**  
A: Ano, můžete získat podporu a zapojit se do komunity na [Aspose.CAD community forum](https://forum.aspose.com/c/cad/19).

---

**Poslední aktualizace:** 2026-08-17  
**Testováno s:** Aspose.CAD 24.11 for .NET  
**Autor:** Aspose

## Související tutoriály

- [Export DWG do PDF nebo rastrových obrázků – Aspose.CAD Guide](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [Export DWG do formátu DXF v C# – Aspose.CAD Tutorial](/cad/net/advanced-export-techniques/exporting-dwg-to-dxf/)
- [Export konkrétních rozvržení do PDF – Aspose.CAD Guide](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}