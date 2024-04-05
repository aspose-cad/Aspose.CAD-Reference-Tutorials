---
title: Převod DWG do PDF se souřadnicemi v C# - Aspose.CAD Tutorial
linktitle: Převod DWG do PDF se souřadnicemi v C#
second_title: Aspose.CAD .NET – formát souborů CAD a BIM
description: Naučte se, jak převést DWG do PDF s konkrétními souřadnicemi v C# pomocí Aspose.CAD. Postupujte podle našeho podrobného průvodce pro přesné a efektivní převody souborů CAD.
type: docs
weight: 11
url: /cs/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/
---
## Úvod

Vítejte v tomto komplexním tutoriálu o převodu souborů DWG do PDF s určenými souřadnicemi pomocí Aspose.CAD for .NET. Aspose.CAD je výkonná knihovna, která umožňuje vývojářům bezproblémově pracovat s formáty souborů CAD v jejich aplikacích .NET. V tomto tutoriálu vás provedeme procesem převodu souboru DWG do PDF a zároveň poskytneme konkrétní souřadnice pro zvýšení přesnosti.

## Předpoklady

Než začneme, ujistěte se, že máte následující předpoklady:

- Knihovna Aspose.CAD: Stáhněte a nainstalujte knihovnu Aspose.CAD pro .NET. Knihovnu najdete[tady](https://releases.aspose.com/cad/net/).

- Vývojové prostředí: Ujistěte se, že máte nastavené kompatibilní vývojové prostředí, včetně sady Visual Studio nebo jakéhokoli jiného preferovaného IDE.

- Soubor DWG: Připravte si soubor DWG pro převod. Můžete použít poskytnutý vzorový soubor nebo vlastní soubor DWG.

## Importovat jmenné prostory

Ve svém projektu C# importujte potřebné jmenné prostory:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadParameters;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.ImageOptions;
```

Pojďme si kód rozebrat do podrobného průvodce pro lepší pochopení:

## Krok 1: Definujte adresář dokumentů

```csharp
string MyDir = "Your Document Directory";
```

## Krok 2: Nastavte cestu ke zdrojovému souboru DWG

```csharp
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
```

## Krok 3: Načtěte soubor DWG a nakonfigurujte možnosti rastrování

```csharp
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
    rasterizationOptions.Layouts = new string[] { "Model" };
    rasterizationOptions.NoScaling = true;
```

## Krok 4: Definujte souřadnice a výřez

```csharp
    Point topLeft = new Point(500, 1000);
    double width = 3108;
    double height = 2489;

    CadVportTableObject newView = new CadVportTableObject();
    newView.Name = new CadStringParameter();
    newView.Name.Init("*Active");
    newView.CenterPoint.X = topLeft.X + width / 2f;
    newView.CenterPoint.Y = topLeft.Y - height / 2f;
    newView.ViewHeight.Value = height;
    newView.ViewAspectRatio.Value = width / height;
```

## Krok 5: Použijte nastavení výřezu

```csharp
    for (int i = 0; i < cadImage.ViewPorts.Count; i++)
    {
        CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
        if (cadImage.ViewPorts.Count == 1 || string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
        {
            cadImage.ViewPorts[i] = newView;
            break;
        }
    }
```

## Krok 6: Nakonfigurujte možnosti PDF a exportujte

```csharp
    Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
    pdfOptions.VectorRasterizationOptions = rasterizationOptions;

    MyDir = MyDir + "ConvertDWGToPDFBySupplyingCoordinates_out.pdf";
    cadImage.Save(MyDir, pdfOptions);
}
```

## Krok 7: Zobrazte zprávu o úspěchu

```csharp
Console.WriteLine("\nThe DWG file exported successfully to PDF.\nFile saved at " + MyDir);
```

## Závěr

Gratulujeme! Úspěšně jste převedli soubor DWG do PDF s určenými souřadnicemi pomocí Aspose.CAD for .NET. Tento tutoriál pokryl základní kroky a poskytl vývojářům jasný návod.

## FAQ

### Q1: Mohu použít Aspose.CAD s jinými formáty souborů CAD?

Odpověď 1: Ano, Aspose.CAD podporuje různé formáty CAD, včetně DWG, DXF, DWF a dalších.

### Q2: Jak mohu zpracovat chyby během procesu převodu?

A2: Implementujte mechanismy zpracování chyb pomocí bloků try-catch k zachycení a správě výjimek.

### Q3: Je Aspose.CAD vhodný pro prostředí Windows i Linux?

Odpověď 3: Ano, Aspose.CAD je kompatibilní s platformami Windows i Linux.

### Q4: Mohu dále přizpůsobit výstup PDF?

A4: Určitě! Prozkoumejte rozsáhlé možnosti poskytované Aspose.CAD a přizpůsobte výstup PDF vašim specifickým požadavkům.

### Q5: Kde najdu další podporu nebo komunitní diskuse?

A5: Navštivte[Fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) za podporu komunity a diskuze.