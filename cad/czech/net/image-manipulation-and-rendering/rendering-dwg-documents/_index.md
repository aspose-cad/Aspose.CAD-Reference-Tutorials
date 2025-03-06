---
title: Vykreslování DWG dokumentů v C# - Aspose.CAD Guide
linktitle: Vykreslování DWG dokumentů v C#
second_title: Aspose.CAD .NET – formát souborů CAD a BIM
description: Naučte se vykreslovat dokumenty DWG v C# pomocí Aspose.CAD. Tento podrobný průvodce pokrývá import, konfiguraci a ukládání s příklady kódu.
weight: 17
url: /cs/net/image-manipulation-and-rendering/rendering-dwg-documents/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Vykreslování DWG dokumentů v C# - Aspose.CAD Guide

## Úvod

Vítejte v obsáhlém průvodci vykreslováním dokumentů DWG v C# pomocí Aspose.CAD. Ať už jste zkušený vývojář nebo s .NET teprve začínáte, tento tutoriál vás provede procesem využití Aspose.CAD k efektivnímu vykreslování souborů DWG. Aspose.CAD je výkonné API, které poskytuje robustní funkce pro práci s formáty souborů CAD, což z něj činí oblíbenou volbu pro vývojáře zabývající se soubory DWG.

## Předpoklady

Než se pustíte do výukového programu, ujistěte se, že máte následující předpoklady:

- Základní znalost programovacího jazyka C#.
- Visual Studio nainstalované na vašem počítači.
-  Knihovna Aspose.CAD integrovaná do vašeho projektu. Můžete si jej stáhnout z[tady](https://releases.aspose.com/cad/net/).
- Ukázkový soubor DWG, například „Bottom_plate.dwg“, který bude následovat spolu s příklady.

## Importovat jmenné prostory

Chcete-li začít, nezapomeňte importovat potřebné jmenné prostory na začátku kódu C#:

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

Nyní rozdělme poskytnutý příklad do několika kroků:

## Krok 1: Načtěte soubor DWG

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Zde je váš kód pro načtení souboru DWG.
}
```

## Krok 2: Nakonfigurujte možnosti rastrování

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };
rasterizationOptions.NoScaling = true;
//Zde lze přidat další konfigurace rasterizace.
```

## Krok 3: Definujte oblast pro kreslení

```csharp
Point topLeft = new Point(6156, 7053);
double width = 3108;
double height = 2489;
```

## Krok 4: Vytvořte nový výřez

```csharp
CadVportTableObject newView = new CadVportTableObject();
newView.Name.Value = "*Active";
newView.CenterPoint.X = topLeft.X + width / 2f;
newView.CenterPoint.Y = topLeft.Y - height / 2f;
newView.ViewHeight.Value = height;
newView.ViewAspectRatio.Value = width / height;
```

## Krok 5: Nahraďte aktivní výřez

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

## Krok 6: Nakonfigurujte možnosti PDF

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Krok 7: Uložte vykreslený DWG jako PDF

```csharp
cadImage.Save(MyDir, pdfOptions);
```

## Závěr

Gratulujeme! Úspěšně jste vykreslili dokument DWG do PDF pomocí Aspose.CAD v C#. Neváhejte a prozkoumejte další funkce a přizpůsobte kód podle svých konkrétních požadavků.

## FAQ

### Q1: Mohu použít Aspose.CAD s jinými formáty souborů CAD?

Odpověď 1: Ano, Aspose.CAD podporuje různé formáty CAD, včetně DWG, DXF, DWF a dalších.

### Q2: Je Aspose.CAD kompatibilní s .NET Core?

A2: Ano, Aspose.CAD je kompatibilní s .NET Framework i .NET Core.

### Q3: Jak mohu zpracovat různá rozvržení v souboru DWG?

 A3: Můžete zadat požadované rozvržení v`Layouts` majetek`CadRasterizationOptions`.

### Q4: Existují nějaké licenční úvahy pro používání Aspose.CAD?

 A4: Podrobnosti o licencování naleznete na[tady](https://purchase.aspose.com/buy).

### Q5: Kde najdu další podporu?

A5: Navštivte[Fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) za podporu komunity a diskuze.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
