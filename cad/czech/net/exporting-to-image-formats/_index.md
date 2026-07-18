---
date: 2026-07-18
description: Aspose CAD conversion vám umožní snadno exportovat IFC do PNG a IGES
  do PDF. Naučte se krok za krokem, jak převést CAD soubory pomocí Aspose.CAD for
  .NET během několika minut.
keywords:
- aspose cad conversion
- export cad to png
- convert iges to pdf
lastmod: 2026-07-18
linktitle: Export do formátů obrázků
og_description: Aspose CAD conversion umožňuje rychlý export IFC do PNG a IGES do
  PDF. Postupujte podle tohoto průvodce pro plynulé zpracování CAD souborů s Aspose.CAD
  for .NET.
og_image_alt: Guide showing Aspose CAD conversion from CAD files to PNG and PDF
og_title: 'Aspose CAD Conversion: Export do formátů obrázků'
schemas:
- author: Aspose
  dateModified: '2026-07-18'
  description: Aspose CAD conversion lets you effortlessly export IFC to PNG and IGES
    to PDF. Learn step‑by‑step how to convert CAD files with Aspose.CAD for .NET in
    minutes.
  headline: 'Aspose CAD Conversion: Exporting to Image Formats'
  type: TechArticle
- questions:
  - answer: Yes, iterate over a folder with `foreach (var file in Directory.GetFiles(path,
      "*.ifc")) { var img = new Image(file); img.Save(Path.ChangeExtension(file, ".png"),
      ImageFormat.Png); }`. The `Directory.GetFiles` method returns the names of files
      (including their paths) that match a specified pattern in a directory.
    question: Can I convert multiple CAD files in one batch?
  - answer: Layer visibility is respected; you can toggle layers via `LoadOptions`
      before saving, ensuring only selected layers appear in the output.
    question: Does Aspose.CAD preserve layer information in the exported image?
  - answer: The library comfortably processes files up to **2 GB**; larger files should
      be split or streamed using `LoadOptions.MemoryLimit`.
    question: What is the maximum file size Aspose.CAD can handle?
  - answer: Yes—by saving as `ImageFormat.Pdf` the output retains vector data, allowing
      infinite scaling without quality loss.
    question: Is there support for converting CAD to vector‑based PDFs?
  - answer: A single Aspose.CAD license covers all supported .NET runtimes (Framework,
      Core, and .NET 5+).
    question: Do I need a separate license for each .NET platform?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- aspose cad
- cad conversion
- export cad to png
- iges to pdf
- ifc to png
title: 'Aspose CAD Conversion: Export do formátů obrázků'
url: /cs/net/exporting-to-image-formats/
weight: 39
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose CAD konverze: Export do formátů obrázků

V moderních inženýrských a designových pracovních postupech je **aspose cad conversion** nezbytná pro převod složitých CAD a BIM souborů do univerzálně zobrazitelných formátů obrázků. Ať už potřebujete sdílet rychlý náhled modelu IFC nebo vygenerovat tisknutelný PDF z výkresu IGES, tento tutoriál vás provede přesné kroky pomocí Aspose.CAD pro .NET. Uvidíte, jak zachovat geometrii, barvy i vrstvy při exportu do PNG, PDF a dalších rastrových formátů.

## Rychlé odpovědi
- **Jaké formáty může Aspose.CAD exportovat?** Více než 30 formátů CAD/BIM do více než 20 typů obrázků, včetně PNG, JPEG, PDF a TIFF.  
- **Potřebuji licenci pro vývoj?** Bezplatná zkušební verze stačí pro hodnocení; pro produkční nasazení je vyžadována komerční licence.  
- **Které verze .NET jsou podporovány?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7.  
- **Lze zpracovávat velké soubory?** Ano – Aspose.CAD zvládne soubory až do 2 GB, aniž by načítal celý dokument do paměti.  
- **Je potřeba další software?** Ne, nejsou vyžadovány externí CAD nástroje; knihovna provádí všechny konverze interně.

## Co je Aspose CAD konverze?
Třída `Image` představuje CAD dokument načtený do paměti a poskytuje metody pro jeho uložení v různých formátech. Aspose CAD Conversion převádí CAD/BIM soubory do jiných formátů pomocí Aspose.CAD pro .NET. Načtěte zdroj pomocí `Image`, zvolte cílový formát a zavolejte `Save`. Tento dvoukrokový vzor zachovává vrstvy, tloušťky čar a textury, čímž odpovídá původnímu záměru návrhu.

## Jak exportovat soubory IFC do PNG?
Třída `Image` představuje CAD dokument načtený do paměti a poskytuje metody pro jeho uložení v různých formátech. Načtěte soubor IFC pomocí `new Image("model.ifc")` a zavolejte `image.Save("model.png", ImageFormat.Png)`. Aspose.CAD načte 3‑D geometrii, zploští ji na rastrový obrázek a zapíše vysoce kvalitní PNG, který zachovává barevnou hloubku a průhlednost. Pro dávkové zpracování projděte složku a uložte každý soubor.

## Jak exportovat soubory IGES do PDF?
Třída `Image` představuje CAD dokument načtený do paměti a poskytuje metody pro jeho uložení v různých formátech. Vytvořte instanci `Image` ze souboru IGES a zavolejte `image.Save("drawing.pdf", ImageFormat.Pdf)`. Konverze zachovává vektorové informace, styly čar a anotace, čímž vznikne PDF, které lze otevřít v libovolném prohlížeči bez ztráty detailů. Použijte volitelnou vlastnost `Resolution` pro zvýšení DPI u tiskových PDF.

## Proč použít Aspose.CAD pro .NET?
Aspose.CAD podporuje **30+ vstupních formátů** (včetně IFC, IGES, DWG, DWF a STL) a může výstupovat **20+ typů obrázků**. Zpracuje vícestránkové výkresy během méně než 5 sekund na typickém serveru a funguje zcela offline – není potřeba nativní instalace CAD softwaru. Tyto kvantifikované výhody z něj dělají nákladově efektivní, vysoce výkonnou volbu pro podnikové i freelance vývojáře.

## Časté úskalí a profesionální tipy
Třída `LoadOptions` vám umožňuje přizpůsobit, jak se CAD soubor načítá, například nastavením limitu paměti nebo specifikací vrstev.  
Objekt `FontSettings` definuje pravidla pro substituci a vložení fontů používaných během konverze.  

- **Úskalí:** Ignorování výchozího DPI může vést k nízkému rozlišení obrázků.  
  **Profesionální tip:** Nastavte `image.DpiX` a `image.DpiY` na 300 pro tiskové PNG s vysokou kvalitou.  
- **Úskalí:** Velké IGES soubory mohou překročit limity paměti.  
  **Profesionální tip:** Použijte `LoadOptions` s `MemoryLimit` pro streamování souboru po částech.  
- **Úskalí:** Chybějící fonty v modelech IFC vedou k zástupnému textu.  
  **Profesionální tip:** Vložte požadované fonty pomocí objektu `FontSettings` před konverzí.

## Tutoriály pro export do formátů obrázků
### [Export souborů IFC do PNG – tutoriál Aspose.CAD](./exporting-ifc-files-to-png/)
Prozkoumejte Aspose.CAD pro .NET, robustní řešení pro bezproblémový převod IFC do PNG. Stáhněte nyní pro efektivní zpracování CAD souborů.  
### [Export souborů IGES do PDF – průvodce Aspose.CAD](./exporting-iges-files-to-pdf/)
Naučte se snadno exportovat soubory IGES do PDF pomocí Aspose.CAD pro .NET. Postupujte podle našeho krok‑za‑krokem průvodce pro přesnou manipulaci s CAD soubory.

## Často kladené otázky

**Q: Mohu převádět více CAD souborů najednou v jedné dávce?**  
A: Ano, iterujte přes složku pomocí `foreach (var file in Directory.GetFiles(path, "*.ifc")) { var img = new Image(file); img.Save(Path.ChangeExtension(file, ".png"), ImageFormat.Png); }`.  
Metoda `Directory.GetFiles` vrací názvy souborů (včetně jejich cest), které odpovídají zadanému vzoru ve složce.

**Q: Zachovává Aspose.CAD informace o vrstvách v exportovaném obrázku?**  
A: Viditelnost vrstev je respektována; vrstvy můžete přepínat pomocí `LoadOptions` před uložením, čímž zajistíte, že se v výstupu objeví jen vybrané vrstvy.

**Q: Jaká je maximální velikost souboru, kterou Aspose.CAD zvládne?**  
A: Knihovna pohodlně zpracuje soubory až do **2 GB**; větší soubory by měly být rozděleny nebo streamovány pomocí `LoadOptions.MemoryLimit`.

**Q: Existuje podpora pro konverzi CAD do vektorových PDF?**  
A: Ano – při uložení jako `ImageFormat.Pdf` výstup zachovává vektorová data, což umožňuje nekonečné škálování bez ztráty kvality.

**Q: Potřebuji samostatnou licenci pro každou .NET platformu?**  
A: Jedna licence Aspose.CAD pokrývá všechny podporované .NET runtime (Framework, Core i .NET 5+).

---

**Poslední aktualizace:** 2026-07-18  
**Testováno s:** Aspose.CAD 24.12 pro .NET  
**Autor:** Aspose

## Související tutoriály

- [Export souborů IFC do PNG – tutoriál Aspose.CAD](/cad/net/exporting-to-image-forms/exporting-ifc-files-to-png/)
- [Export souborů IGES do PDF – průvodce Aspose.CAD](/cad/net/exporting-to-image-forms/exporting-iges-files-to-pdf/)
- [Export CAD rozvržení do rastrových formátů obrázků v Aspose.CAD pro .NET](/cad/net/cad-export-formats/export-cad-layouts-to-raster-image-formats/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}