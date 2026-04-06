---
date: 2026-04-06
description: Naučte se, jak převést DWG na PDF a přidat vlastní text pomocí C# a Aspose.CAD.
  Tento krok‑za‑krokem průvodce zahrnuje generování PDF z DWG, vložení textové entity
  a změnu písma textu v DWG.
keywords:
- convert dwg to pdf
- generate pdf from dwg
- insert text entity
- change dwg text font
- aspose cad dwg pdf
linktitle: Přidání textu do DWG souborů v C#
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Převod DWG na PDF a přidání textu v C# – tutoriál Aspose.CAD
url: /cs/net/dwg-file-manipulation/adding-text-to-dwg/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Převod DWG na PDF a přidání textu v C# – Aspose.CAD Tutoriál

## Úvod

V rychle se vyvíjejícím světě CAD a .NET vývoje je **převod DWG na PDF** při vkládání vlastních anotací častým požadavkem. Ať už potřebujete vytvořit tisknutelné výkresy pro klienty nebo vložit dynamické poznámky přímo do DWG, Aspose.CAD to usnadňuje. V tomto tutoriálu se naučíte, jak **převést DWG na PDF**, **přidat textový prvek** a dokonce **změnit písmo textu v DWG** pomocí C#.

## Rychlé odpovědi
- **Jaká knihovna je nejlepší pro převod DWG na PDF?** Aspose.CAD pro .NET  
- **Mohu při převodu přidat vlastní text?** Ano – vytvořte entitu `CadText` a přidejte ji před uložením.  
- **Potřebuji licenci pro produkční použití?** Je vyžadována komerční licence; je k dispozici bezplatná zkušební verze.  
- **Které verze .NET jsou podporovány?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Je možné změnit písmo textu?** Ano, upravte vlastnosti `CadText`, jako jsou `StyleType` a `TextHeight`.

## Co je „převod dwg na pdf“?

Převod souboru DWG na PDF transformuje vektorový CAD výkres do široce sdíleného, zařízení‑nezávislého dokumentu. PDF zachovává původnou geometrii a vrstvy, přičemž umožňuje vložit anotace, text nebo další metadata. Aspose.CAD automaticky provádí rasterizaci a vektorové vykreslování, takže na serveru nepotřebujete žádný třetí CAD software.

## Proč přidat text do DWG před převodem?

Vložení textu přímo do DWG vám dává plnou kontrolu nad umístěním, stylem a přiřazením vrstvy. Když je soubor později převeden na PDF, text se zobrazí přesně tam, kde jste jej umístili, zachovává záměr návrhu a eliminuje potřebu post‑zpracování v PDF editoru.

## Požadavky

Před zahájením se ujistěte, že máte:

- **Aspose.CAD Library** – stáhněte ji z [download link](https://releases.aspose.com/cad/net/).  
- **Funkční .NET prostředí** (Visual Studio 2022, .NET 6 nebo jakákoli kompatibilní verze).  
- **Složka pro vaše testovací soubory** – v průběhu návodu budeme odkazovat na `MyDir`.

Nyní projděme proces krok za krokem.

## Import názvových prostorů

Přidejte požadované `using` direktivy, abyste mohli přistupovat ke třídám Aspose.CAD.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects.AttEntities;
using Aspose.CAD.ImageOptions;
```

## Krok 1: Načtení souboru DWG

Načtěte svůj zdrojový soubor DWG do objektu `Image`. Tento objekt vám poskytuje přístup k podkladovým CAD entitám.

```csharp
string dwgPathToFile = MyDir + "SimpleEntites.dwg";
using (Image image = Image.Load(dwgPathToFile))
{
    // Subsequent steps will be performed inside this block
}
```

## Krok 2: Vytvoření objektu CadText (vložit textový prvek)

Třída `CadText` představuje jediný řádek textu v DWG. Zde nastavujeme jeho styl, hodnotu, barvu, vrstvu a pozici. Upravením `StyleType` nebo `TextHeight` **změníte písmo textu v DWG**.

```csharp
CadText cadText = new CadText();
cadText.StyleType = "Standard";          // Font/style – change to alter DWG text font
cadText.DefaultValue = "Some custom text";
cadText.ColorId = 256;                    // 256 = ByLayer (you can use a specific ACI color)
cadText.LayerName = "0";
cadText.FirstAlignment.X = 47.90;
cadText.FirstAlignment.Y = 5.56;
cadText.TextHeight = 0.8;                 // Height influences visual size
cadText.ScaleX = 0.0;
```

## Krok 3: Přidání textového prvku do Model Space

Modelový prostor DWG obsahuje většinu entit výkresu. Přidáním našeho `CadText` do bloku `*Model_Space` se text stane součástí výkresu.

```csharp
CadImage cadImage = (CadImage)image;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadText);
```

## Krok 4: Nastavení možností PDF (vytvoření PDF z DWG)

Nastavte možnosti rasterizace, které řídí, jak je DWG vykreslen do PDF. Můžete upravit velikost stránky, typ kresby a rozvržení.

```csharp
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;
cadRasterizationOptions.PageHeight = 1600;
cadRasterizationOptions.PageWidth = 1600;
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## Krok 5: Uložení upraveného DWG jako PDF

Nakonec exportujte upravený výkres. Výsledné PDF obsahuje nově vložený text.

```csharp
image.Save(MyDir + "SimpleEntites_generated.pdf", pdfOptions);
```

> **Tip:** Pokud potřebujete PDF s vyšším rozlišením, zvyšte `PageHeight` a `PageWidth` úměrně.

## Časté problémy a řešení

| Problém | Příčina | Řešení |
|-------|--------|-----|
| Text se v PDF nezobrazuje | Špatná vrstva nebo ID barvy | Ujistěte se, že `LayerName` existuje a `ColorId` je nastaven na viditelnou barvu (např. 7 pro bílou). |
| Text je špatně umístěn | Nesprávné souřadnice zarovnání | Ověřte hodnoty `FirstAlignment.X/Y` vzhledem k jednotkám výkresu. |
| PDF je prázdný | Možnosti rasterizace nejsou nastaveny | Nastavte `DrawType` na `UseObjectColor` nebo `UseObjectLineWeight`. |

## Často kladené otázky (existující)

### Q1: Je Aspose.CAD kompatibilní se všemi verzemi souborů DWG?

Aspose.CAD podporuje širokou škálu verzí souborů DWG, což zajišťuje kompatibilitu s různým CAD softwarem.

### Q2: Mohu pomocí Aspose.CAD přidat do jednoho souboru DWG více textových entit?

Ano, můžete přidat do souboru DWG více textových entit opakováním postupu popsaného v tutoriálu.

### Q3: Jak mohu změnit písmo a styl textu v Aspose.CAD?

Pro úpravu písma a stylu textu upravte vlastnosti objektu `CadText` před jeho přidáním do souboru DWG.

### Q4: Existují licenční požadavky pro používání Aspose.CAD v komerčním projektu?

Ano, zajistěte soulad s licenčními podmínkami Aspose.CAD. Podrobnosti najdete na [Aspose.CAD Purchase](https://purchase.aspose.com/buy).

### Q5: Kde mohu získat pomoc nebo diskutovat o dotazech souvisejících s Aspose.CAD?

Navštivte [Aspose.CAD fórum](https://forum.aspose.com/c/cad/19), kde se můžete spojit s komunitou a získat podporu.

## Další časté otázky

**Q: Jak vygenerovat PDF z DWG bez přidání textu?**  
A: Přeskočte krok vytvoření `CadText` a přímo nastavte `PdfOptions` před voláním `image.Save(...)`.

**Q: Mohu programově změnit barvu textu?**  
A: Ano, nastavte `cadText.ColorId` na konkrétní číslo ACI barvy (např. 1 pro červenou).

**Q: Je možné vložit víceřádkový text?**  
A: Použijte `CadMText` pro víceřádkové textové bloky; postup je podobný jako u `CadText`.

**Q: Podporuje Aspose.CAD hromadný převod více souborů DWG?**  
A: Rozhodně – projděte složku s DWG soubory, aplikujte stejný postup a uložte každý jako PDF.

## Závěr

Nyní máte kompletní, produkčně připravený workflow pro **převod DWG na PDF**, **přidání vlastního textu** a **přizpůsobení vzhledu textu** pomocí C# a Aspose.CAD. Tato technika je ideální pro automatizovanou generaci výkresů, reportovací kanály nebo jakýkoli scénář, kde potřebujete během běhu obohatit CAD soubory.

---

**Poslední aktualizace:** 2026-04-06  
**Testováno s:** Aspose.CAD 24.11 pro .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}