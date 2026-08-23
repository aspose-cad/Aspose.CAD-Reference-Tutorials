---
date: 2026-08-23
description: Naučte se, jak vytvořit viewport DWG v C# pomocí Aspose.CAD. Tento průvodce
  popisuje načtení souboru DWG, nastavení rasterizace, definování viewportu a uložení
  výsledku jako PDF.
keywords:
- create viewport dwg c#
- render dwg c#
- aspose.cad .net
lastmod: 2026-08-23
linktitle: Renderování DWG dokumentů v C#
og_description: Naučte se, jak vytvořit viewport DWG v C# pomocí Aspose.CAD. Tento
  průvodce popisuje načtení souboru DWG, nastavení rasterizace, definování viewportu
  a uložení výsledku jako PDF.
og_image_alt: Guide showing how to create viewport dwg c# with Aspose.CAD in .NET
og_title: Jak vytvořit viewport DWG v C# pomocí Aspose.CAD pro .NET
schemas:
- author: Aspose
  dateModified: '2026-08-23'
  description: Learn how to create viewport dwg c# using Aspose.CAD. This guide covers
    loading a DWG file, configuring rasterization, defining a viewport, and saving
    the result as PDF.
  headline: How to create viewport dwg c# with Aspose.CAD for .NET
  type: TechArticle
- questions:
  - answer: Load the DWG file with `CadImage.Load`.
    question: What is the first step?
  - answer: '`Viewport` inside `CadRasterizationOptions`.'
    question: Which class defines the view area?
  - answer: Yes, using `PdfOptions` after rasterization.
    question: Can I output to PDF?
  - answer: A commercial license is required; a free trial works for evaluation.
    question: Do I need a license for production?
  - answer: Absolutely – Aspose.CAD works with .NET Framework, .NET Core, and .NET 5/6.
    question: Is .NET Core supported?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- create viewport dwg c#
- Aspose.CAD
- C# CAD rendering
- DWG to PDF
- CAD viewports
title: Jak vytvořit viewport DWG v C# pomocí Aspose.CAD pro .NET
url: /cs/net/image-manipulation-and-rendering/rendering-dwg-documents/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Renderování DWG dokumentů v C# – vytvoření viewportu dwg c# tutoriál

## Úvod

V tomto komplexním tutoriálu se naučíte, jak **create viewport dwg c#** pomocí Aspose.CAD a renderovat soubor DWG do PDF. Ať už potřebujete extrahovat konkrétní rozvržení, vytvořit tiskový list nebo vložit CAD pohled do zprávy, řízení viewportu vám poskytuje přesnou kontrolu nad renderováním. Aspose.CAD podporuje **20+ CAD formátů** a dokáže zpracovat soubory s tisíci entitami, aniž by načítal celý dokument do paměti, což ho činí ideálním pro vysoce výkonné .NET aplikace.

## Rychlé odpovědi
- **Jaký je první krok?** Načtěte soubor DWG pomocí `CadImage.Load`.
- **Která třída definuje oblast zobrazení?** `Viewport` uvnitř `CadRasterizationOptions`.
- **Mohu výstup uložit do PDF?** Ano, pomocí `PdfOptions` po rasterizaci.
- **Potřebuji licenci pro produkční nasazení?** Je vyžadována komerční licence; pro hodnocení stačí bezplatná zkušební verze.
- **Je .NET Core podporován?** Rozhodně – Aspose.CAD funguje s .NET Framework, .NET Core a .NET 5/6.

## Požadavky

- Základní znalost programování v C#.
- Nainstalovaný Visual Studio (jakákoli recentní edice).
- Knihovna Aspose.CAD přidána do vašeho projektu. Můžete ji stáhnout ze [Aspose.CAD download page](https://releases.aspose.com/cad/net/).
- Ukázkový soubor DWG, například **Bottom_plate.dwg**, pro praktické cvičení.

## Importování jmenných prostorů

Přidejte požadované `using` direktivy na začátek vašeho C# souboru, aby kompilátor mohl najít typy Aspose.CAD.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.FileFormats.Cad;
```

Nyní, když je prostředí připravené, projděme implementaci krok za krokem.

## Jak vytvořit viewport dwg c#?

Pro vytvoření vlastního viewportu nejprve načtěte soubor DWG do objektu `CadImage`, poté nakonfigurujte `CadRasterizationOptions` s požadovaným rozvržením a měřítkem. Definujte oblast, kterou chcete zobrazit, vytvořte instanci `CadVportTableObject` s vypočteným středem, výškou a poměrem stran, nahraďte aktivní viewport, nastavte případné PDF volby a nakonec výsledek uložte.

## Krok 1: načtení souboru dwg

`CadImage.Load` načte soubor DWG do objektu `CadImage`, který představuje CAD výkres v paměti.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for loading the DWG file goes here.
}
```

## Krok 2: konfigurace možností rasterizace

`CadRasterizationOptions` určuje, jak je CAD výkres rasterizován, včetně výběru rozvržení, měřítka a výstupní velikosti.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };
rasterizationOptions.NoScaling = true;
// Additional rasterization configurations can be added here.
```

## Krok 3: definování oblasti k vykreslení

`Point` definuje souřadnice X a Y levého horního rohu oblasti, která se má vykreslit.

```csharp
Point topLeft = new Point(6156, 7053);
double width = 3108;
double height = 2489;
```

## Krok 4: vytvoření nového viewportu

`CadVportTableObject` představuje objekt viewportu, který řídí viditelnou oblast a poměr stran vykresleného výkresu.

```csharp
CadVportTableObject newView = new CadVportTableObject();
newView.Name.Value = "*Active";
newView.CenterPoint.X = topLeft.X + width / 2f;
newView.CenterPoint.Y = topLeft.Y - height / 2f;
newView.ViewHeight.Value = height;
newView.ViewAspectRatio.Value = width / height;
```

## Krok 5: nahrazení aktivního viewportu

Cyklus nahradí aktivní viewport nově vytvořeným, aby se použila vlastní nastavení zobrazení.

```csharp
for (int i = 0; i < cadImage.ViewPorts.Count; i++)
{
    CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
    if ((currentView.Name.Value == null && cadImage.ViewPorts.Count == 1) ||
    string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
    {
        cadImage.ViewPorts[i] = newView;
        break;
    }
}
```

## Krok 6: konfigurace PDF voleb

`PdfOptions` konfiguruje parametry výstupu PDF, jako je komprese a metadata.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Krok 7: uložení vykresleného dwg jako PDF

`image.Save` zapíše vykreslený obrázek do souboru pomocí zadaných možností formátu.

```csharp
cadImage.Save(MyDir, pdfOptions);
```

## Proč použít vlastní viewport při renderování DWG?

Vlastní viewport vám umožní izolovat konkrétní rozvržení nebo oblast, snížit velikost souboru a zlepšit rychlost renderování. Aspose.CAD dokáže vykreslit 300‑stránkový DWG za méně než 2 sekundy při použití zaměřeného viewportu, na rozdíl od renderování celého výkresu, které může trvat o několik sekund déle.

## Časté problémy a řešení

- **Blank output** – Ujistěte se, že souřadnice viewportu jsou v rámci rozsahu výkresu; použijte `CadImage.Size` k ověření hranic.
- **Missing layers** – Nastavte `CadRasterizationOptions.Layouts` na správný název rozvržení; jinak může být výchozí rozvržení prázdné.
- **Performance slowdown** – Vypněte anti‑aliasing v `CadRasterizationOptions`, pokud potřebujete jen rychlý náhled.

## Často kladené otázky

### Q1: Mohu použít Aspose.CAD s jinými CAD formáty souborů?

A1: Ano, Aspose.CAD podporuje různé formáty, včetně DWG, DXF, DWF a více než 20 dalších CAD typů.

### Q2: Je Aspose.CAD kompatibilní s .NET Core?

A2: Ano, Aspose.CAD funguje s .NET Framework, .NET Core a nejnovějšími verzemi .NET.

### Q3: Jak mohu pracovat s různými rozvrženími v souboru DWG?

A3: Zadejte požadované rozvržení pomocí vlastnosti `Layouts` třídy `CadRasterizationOptions` před renderováním.

### Q4: Existují licenční úvahy při používání Aspose.CAD?

A4: Pro podrobnosti o licencování navštivte [Aspose.CAD licensing page](https://purchase.aspose.com/buy).

### Q5: Kde mohu najít další podporu?

A5: Navštivte [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) pro komunitní pomoc a diskuse.

### Q6: Mohu renderovat přímo do PNG místo PDF?

A6: Ano, změňte `PdfOptions` na `PngOptions` a zavolejte `image.Save("output.png", pngOptions)`.

### Q7: Jak vložit vykreslený obrázek do aplikace Windows Forms?

A7: Načtěte uložený obrázek do ovládacího prvku `PictureBox` pomocí `Image.FromFile("output.png")`.

## Závěr

Nyní víte, jak **create viewport dwg c#** a renderovat soubor DWG do PDF (nebo jiných rastrových formátů) pomocí Aspose.CAD. Ovládnutím manipulace s viewportem získáte jemnou kontrolu nad vizuálním výstupem, což je nezbytné pro tvorbu přesných technických výkresů, zpráv nebo miniatur. Prozkoumejte další nastavení rasterizace, experimentujte s různými výstupními formáty a integrujte kód do větších .NET služeb nebo desktopových utilit.

---

**Last Updated:** 2026-08-23  
**Tested with:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose

## Související tutoriály

- [Jak nastavit Viewport při konverzi DWG do PDF s koordináty v C# - Aspose.CAD Tutorial](/cad/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/)
- [Naučte se nastavit CAD rasterizační možnosti – Export specifických rozvržení do PDF s Aspose.CAD](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)
- [Jak převést DWG do PDF a rastrových obrázků pomocí Aspose.CAD pro .NET](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}