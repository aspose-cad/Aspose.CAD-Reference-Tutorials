---
title: Přidání vodoznaků do výkresů CAD - Průvodce Aspose.CAD
linktitle: Přidávání vodoznaků do výkresů CAD
second_title: Aspose.CAD .NET – formát souborů CAD a BIM
description: Vylepšete své CAD výkresy profesionálními vodoznaky pomocí Aspose.CAD for .NET. Postupujte podle našeho podrobného průvodce pro personalizované a poutavé návrhy.
type: docs
weight: 11
url: /cs/net/plt-and-watermarking/adding-watermarks-to-cad-drawings/
---
## Úvod

Chcete vylepšit své CAD výkresy přidáním profesionálních vodoznaků? Aspose.CAD for .NET poskytuje robustní řešení pro bezproblémovou integraci vodoznaků do vašich CAD souborů. V tomto podrobném průvodci vás provedeme procesem přidávání vodoznaků pomocí Aspose.CAD, čímž zajistíme, že vaše kresby nejen přenesou důležité informace, ale také ponesou vaši jedinečnou značku.

## Předpoklady

Než se pustíte do výukového programu, ujistěte se, že máte následující:
-  Aspose.CAD for .NET: Ujistěte se, že máte nainstalovanou knihovnu Aspose.CAD. Můžete si jej stáhnout[tady](https://releases.aspose.com/cad/net/).
- Adresář dokumentů: Nastavte adresář pro ukládání výkresů CAD.
Nyní začněme s přidáváním vodoznaků do vašich CAD výkresů!

## Importovat jmenné prostory

Začněte importováním potřebných jmenných prostorů do vašeho projektu .NET:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Krok 1: Načtěte výkres CAD

```csharp
// Cesta k adresáři dokumentů.
string MyDir = "Your Document Directory";
using (CadImage cadImage = (CadImage)Image.Load(MyDir + "Drawing11.dwg")) {
```

## Krok 2: Přidejte vodoznak jako MTEXT

```csharp
// Přidat nový MTEXT
CadMText watermark = new CadMText();
watermark.Text = "Watermark message";
watermark.InitialTextHeight = 40;
watermark.InsertionPoint = new Cad3DPoint(300, 40);
watermark.LayerName = "0";
cadImage.BlockEntities["*Model_Space"].AddEntity(watermark);
```

## Krok 3: Nebo přidejte vodoznak jako text

```csharp
// Případně přidejte jednodušší entitu, jako je Text
CadText text = new CadText();
text.DefaultValue = "Watermark text";
text.TextHeight = 40;
text.FirstAlignment = new Cad3DPoint(300, 40);
text.LayerName = "0";
cadImage.BlockEntities["*Model_Space"].AddEntity(text);
```

## Krok 4: Export do PDF

```csharp
// Exportujte výkres CAD s vodoznakem do PDF
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.Layouts = new[] { "Model" };
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
cadImage.Save(MyDir + "AddWatermark_out.pdf", pdfOptions);
```

Opakujte tyto kroky pro různé výkresy a během okamžiku budete mít profesionálně vypadající soubory CAD s vodoznakem!

## Závěr

Gratulujeme! Úspěšně jste se naučili přidávat vodoznaky do svých výkresů CAD pomocí Aspose.CAD for .NET. Tento jednoduchý, ale výkonný proces vám umožňuje personalizovat vaše návrhy při zachování integrity vašich technických výkresů.

## FAQ

### Q1: Mohu přizpůsobit vzhled vodoznaku?

Odpověď 1: Ano, můžete upravit text, písmo, velikost a polohu vodoznaku podle svých preferencí.

### Q2: Je Aspose.CAD kompatibilní s různými formáty souborů CAD?

Odpověď 2: Aspose.CAD podporuje různé formáty souborů CAD, včetně DWG a DXF, což zajišťuje širokou kompatibilitu.

### Q3: Mohu přidat více vodoznaků do jednoho výkresu CAD?

A3: Rozhodně! Můžete přidat tolik vodoznaků, kolik potřebujete, což poskytuje flexibilitu pro různé případy použití.

### Q4: Nabízí Aspose.CAD bezplatnou zkušební verzi?

A4: Ano, můžete prozkoumat funkce Aspose.CAD pomocí bezplatné zkušební verze. Pochopit to[tady](https://releases.aspose.com/).

### Q5: Kde najdu podporu pro Aspose.CAD?

 A5: Máte-li jakékoli dotazy nebo pomoc, navštivte[Fórum Aspose.CAD](https://forum.aspose.com/c/cad/19).