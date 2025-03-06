---
title: Import obrázků do souborů DWG pomocí C# - Aspose.CAD Guide
linktitle: Import obrázků do souborů DWG pomocí C#
second_title: Aspose.CAD .NET – formát souborů CAD a BIM
description: Naučte se importovat obrázky do souborů DWG pomocí C# s Aspose.CAD for .NET. Postupujte podle našeho podrobného průvodce pro bezproblémovou integraci.
weight: 11
url: /cs/net/image-manipulation-and-rendering/importing-images-into-dwg/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Import obrázků do souborů DWG pomocí C# - Aspose.CAD Guide

## Úvod

V oblasti počítačově podporovaného navrhování (CAD) je začlenění obrázků do souborů DWG běžným a zásadním úkolem. Aspose.CAD for .NET poskytuje výkonnou sadu nástrojů pro zefektivnění tohoto procesu a zpřístupňuje jej pro vývojáře v C#. V tomto tutoriálu prozkoumáme, jak importovat obrázky do souborů DWG krok za krokem.

## Předpoklady

Než se ponoříte do průvodce, ujistěte se, že máte následující:

- Základní znalost programování v C#.
-  Aspose.CAD pro .NET nainstalován. Můžete si jej stáhnout[tady](https://releases.aspose.com/cad/net/).
- Vytvořeno vývojové prostředí.

## Importovat jmenné prostory

Ujistěte se, že jste do projektu C# zahrnuli potřebné jmenné prostory:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Krok 1: Nastavte adresář dokumentů

```csharp
string MyDir = "Your Document Directory";
```

## Krok 2: Načtěte soubor DWG

```csharp
string dwgPathToFile = MyDir + "Drawing11.dwg";
CadImage cadImage1 = (CadImage)Image.Load(dwgPathToFile);
```

## Krok 3: Definujte vlastnosti obrázku

```csharp
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.ObjectHandle = "A3B4";
```

## Krok 4: Nastavte bod vložení a vektory

```csharp
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

## Krok 5: Vytvořte a nakonfigurujte rastrový obrázek

```csharp
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.ImageDefReference = "A3B4";
cadRasterImage.DisplayFlags = 7;
cadRasterImage.ClippingState = 0;
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(639.5, 561.5));
```

## Krok 6: Přidejte obrázek do souboru DWG

```csharp
CadImage cadImage = (CadImage)cadImage1;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadRasterImage);

List<CadBaseObject> list = new List<CadBaseObject>(cadImage.Objects);
list.Add(cadRasterImageDef);
cadImage.Objects = list.ToArray();
```

## Krok 7: Uložit jako PDF

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

## Závěr

Integrace obrázků do souborů DWG pomocí C# a Aspose.CAD for .NET je bezproblémový proces, který umožňuje vývojářům bez námahy vylepšovat jejich CAD projekty o vizuální prvky.

## FAQ

### Q1: Mohu používat Aspose.CAD pro .NET s jinými programovacími jazyky?

A1: Aspose.CAD je primárně navržen pro .NET, ale Aspose poskytuje knihovny pro různé programovací jazyky.

### Q2: Je k dispozici bezplatná zkušební verze pro Aspose.CAD pro .NET?

 A2: Ano, můžete prozkoumat bezplatnou zkušební verzi[tady](https://releases.aspose.com/).

### Q3: Kde najdu podrobnou dokumentaci k Aspose.CAD?

 A3: Dokumentace je k dispozici[tady](https://reference.aspose.com/cad/net/).

### Q4: Jak mohu získat dočasnou licenci pro Aspose.CAD for .NET?

 A4: Návštěva[tento odkaz](https://purchase.aspose.com/temporary-license/) získat dočasnou licenci.

### Q5: Existují komunitní fóra pro podporu Aspose.CAD?

 A5: Ano, můžete hledat podporu a zapojit se do komunity[tady](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
