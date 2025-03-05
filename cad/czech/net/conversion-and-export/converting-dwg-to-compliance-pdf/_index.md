---
title: Převod DWG do PDF shody - Aspose.CAD výukový program
linktitle: Převod DWG do PDF vyhovujícího předpisům
second_title: Aspose.CAD .NET – formát souborů CAD a BIM
description: Převeďte DWG na vyhovující PDF pomocí Aspose.CAD pro .NET. Postupujte podle našeho návodu, kde najdete podrobné pokyny.
type: docs
weight: 13
url: /cs/net/conversion-and-export/converting-dwg-to-compliance-pdf/
---
## Úvod

Vítejte v našem podrobném tutoriálu o převodu souborů DWG do PDF s předpisy pomocí Aspose.CAD pro .NET. Aspose.CAD je výkonné rozhraní .NET API, které umožňuje vývojářům bez námahy pracovat s formáty souborů CAD. V tomto tutoriálu vás provedeme procesem převodu souboru DWG do PDF s předpisy s podrobnými příklady a vysvětleními.

## Předpoklady

Než začneme, ujistěte se, že máte splněny následující předpoklady:

-  Aspose.CAD for .NET: Ujistěte se, že máte knihovnu Aspose.CAD integrovanou do vašeho projektu .NET. Můžete si jej stáhnout[tady](https://releases.aspose.com/cad/net/).

- Vývojové prostředí: Mějte nainstalované funkční vývojové prostředí .NET a ujistěte se, že je správně nakonfigurováno.

- Ukázkový soubor DWG: Stáhněte si ukázkový soubor DWG, který chcete převést do formátu PDF.

## Importovat jmenné prostory

Do svého projektu .NET importujte potřebné jmenné prostory, abyste mohli využívat funkce Aspose.CAD.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

Nyní si rozdělme proces převodu souboru DWG na Compliance PDF do několika kroků.

## Krok 1: Načtěte soubor DWG

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

Aspose.CAD.Image cadImage = Aspose.CAD.Image.Load(sourceFilePath);
```

## Krok 2: Nastavte možnosti rastrování

 Vytvořte instanci`CadRasterizationOptions` a nakonfigurovat jeho vlastnosti, jako je barva pozadí, šířka stránky a výška stránky.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions
{
    BackgroundColor = Aspose.CAD.Color.White,
    PageWidth = 1600,
    PageHeight = 1600
};
```

## Krok 3: Vytvořte možnosti PDF

 Vytvořte instanci`PdfOptions` a nastavte možnosti vektorové rastrování.

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions,
    CorePdfOptions = new PdfDocumentOptions { Compliance = PdfCompliance.PdfA1a }
};
```

## Krok 4: Uložit jako PDF (soulad s A1a)

Uložte obrázek CAD jako Compliance PDF s A1a.

```csharp
cadImage.Save(MyDir + "PDFA1_A.pdf", pdfOptions);
```

## Krok 5: Uložit jako PDF (soulad s A1b)

Změňte typ shody na A1b a uložte obrázek CAD jako vyhovující PDF.

```csharp
pdfOptions.CorePdfOptions.Compliance = PdfCompliance.PdfA1b;
cadImage.Save(MyDir + "PDFA1_B.pdf", pdfOptions);
```

## Závěr

Gratulujeme! Úspěšně jste převedli soubor DWG na Compliance PDF pomocí Aspose.CAD for .NET. Tento tutoriál poskytuje komplexního průvodce pro vývojáře, kteří chtějí integrovat možnosti převodu CAD do svých aplikací.

## FAQ

### Q1: Mohu pomocí Aspose.CAD převést jiné formáty CAD na Compliance PDF?

Odpověď 1: Ano, Aspose.CAD podporuje různé formáty CAD, což umožňuje převod do PDF s předpisy.

### Q2: Je Aspose.CAD kompatibilní s .NET Core?

A2: Ano, Aspose.CAD je kompatibilní s .NET Framework i .NET Core.

### Q3: Existují nějaké možnosti licencování pro Aspose.CAD?

 A3: Ano, můžete prozkoumat možnosti licencování[tady](https://purchase.aspose.com/buy).

### Q4: Je k dispozici bezplatná zkušební verze?

 A4: Ano, můžete získat bezplatnou zkušební verzi[tady](https://releases.aspose.com/).

### Q5: Kde mohu získat podporu pro Aspose.CAD?

A5: Navštivte[Fórum Aspose.CAD](https://forum.aspose.com/c/cad/19) pro jakékoli dotazy týkající se podpory.