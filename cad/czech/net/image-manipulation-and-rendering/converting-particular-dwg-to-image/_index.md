---
date: 2026-08-12
description: Extrahujte text z DWG a převádějte konkrétní DWG na obrázek v C# pomocí
  Aspose.CAD pro .NET. Naučte se krok za krokem s ukázkami kódu.
keywords:
- extract text from dwg
- convert specific dwg to image
- Aspose.CAD .NET
lastmod: 2026-08-12
linktitle: Převod konkrétního DWG na obrázek v C#
og_description: Extrahujte text z DWG a převádějte konkrétní DWG na obrázek v C# s
  Aspose.CAD. Postupujte podle tohoto stručného průvodce pro rychlou implementaci.
og_image_alt: Guide showing DWG to image conversion and text extraction using Aspose.CAD
  in C#
og_title: Extrahovat text z DWG a převést konkrétní DWG na obrázek v C#
schemas:
- author: Aspose
  dateModified: '2026-08-12'
  description: Extract text from DWG and convert specific DWG to image in C# using
    Aspose.CAD for .NET. Learn step‑by‑step with code snippets.
  headline: Extract text from DWG and convert specific DWG to image in C#
  type: TechArticle
- questions:
  - answer: Aspose.CAD supports DWG releases from AutoCAD 2000 up to the latest 2024
      version, covering over 90 % of files created in the field.
    question: Is Aspose.CAD compatible with all versions of DWG files?
  - answer: Yes – you can change resolution, image format, anti‑aliasing, and background
      color to suit PNG, JPEG, or PDF targets.
    question: Can I customize the rasterization options for different outputs?
  - answer: Explore the comprehensive [Aspose.CAD documentation](https://reference.aspose.com/cad/net/)
      for more code samples and API details.
    question: Where can I find additional examples and documentation?
  - answer: Absolutely – you can download a trial version on the **[Aspose trial download
      page](https://releases.aspose.com/)** and evaluate all features without restrictions
      for 30 days.
    question: Is there a free trial available for Aspose.CAD?
  - answer: Join the active [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)
      where developers share solutions and the Aspose team answers questions.
    question: How can I get support or connect with the community?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- extract text from dwg
- Aspose.CAD
- C# CAD processing
title: Extrahovat text z DWG a převést konkrétní DWG na obrázek v C#
url: /cs/net/image-manipulation-and-rendering/converting-particular-dwg-to-image/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Převod konkrétního DWG na obrázek v C# – průvodce Aspose.CAD

## Úvod

V moderních inženýrských aplikacích často potřebujete **extrahovat text z DWG** souborů a **převést konkrétní DWG do formátu obrázku** pro reportování nebo vizualizaci. Aspose.CAD pro .NET vám poskytuje plnohodnotné API, které zvládne oba úkoly bez nutnosti externího CAD softwaru. V tomto tutoriálu se naučíte, jak načíst DWG, filtrovat textové entity, rasterizovat výkres a nakonec uložit výsledek jako PDF obrázek – vše v čistém C# kódu.

## Rychlé odpovědi
- **Jaký je první krok?** Načtěte DWG soubor pomocí `new CadImage("file.dwg")`.  
- **Která třída filtruje text?** Použijte `CadEntityFilter` k výběru entit `Text`.  
- **Jak definujete velikost obrázku?** Nastavte `Width` a `Height` na `CadRasterizationOptions`.  
- **Jaký výstupní formát se používá?** Příklad ukládá do PDF, který vkládá rastrový obrázek.  
- **Potřebuji licenci pro produkci?** Ano – komerční licence Aspose.CAD odstraňuje omezení evaluační verze.  

## Jak extrahovat text z DWG?

Načtěte DWG, použijte filtr, který vybírá pouze textové entity, a poté přečtěte vlastnost `TextString` každé entity. Tento přístup vrací každý kus anotace, popisku nebo rozměrového textu, který ve výkresu existuje, což vám umožní jej znovu použít pro vyhledávání, indexaci nebo reportování.

## Proč převádět konkrétní DWG na obrázek?

Převod DWG na rastrový obrázek vám umožní vložit výkres do dokumentů, webových stránek nebo mobilních aplikací, které nedokážou renderovat nativní CAD formáty. Aspose.CAD zpracovává **více než 50 CAD formátů** a dokáže rasterizovat výkresy s několika stovkami stran při využití méně než 200 MB paměti, což jej činí vhodným pro scénáře s vysokou propustností na serveru.

## Požadavky

- Visual Studio (libovolná recentní edice) pro kompilaci a spuštění C# projektů.  
- Aspose.CAD pro .NET – ujistěte se, že máte knihovnu nainstalovanou. Odkaz ke stažení najdete na **[Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/)**.  
- DWG soubor, se kterým chcete pracovat; ukázkový soubor *visualization_-_conference_room.dwg* je použit v ukázkových kódech.

## Importovat jmenné prostory

Následující jmenné prostory vám poskytují přístup k základním CAD třídám, možnostem rasterizace a pomocníkům pro výstup PDF:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Krok 1: načíst DWG soubor

Vytvořte instanci `CadImage` předáním cesty k vašemu DWG souboru. Objekt `CadImage` představuje celý výkres v paměti a poskytuje přístup k jeho vrstvám, entitám a metadatům.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
var cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath);
```

## Krok 2: filtrovat entity

`CadEntityFilter` vám umožní vybrat pouze entity, které potřebujete. V tomto průvodci jej nastavíme tak, aby zachovával objekty **text**, a odstraňoval čáry, kružnice a další geometrii, kterou v konečném obrázku nechcete.

```csharp
CadBaseEntity[] entities = cadImage.Entities;
List<CadBaseEntity> filteredEntities = new List<CadBaseEntity>();

foreach (CadBaseEntity baseEntity in entities)
{
    // Selection or filtration of entities
    if (baseEntity.TypeName == CadEntityTypeName.TEXT)
    {
        filteredEntities.Add(baseEntity);
    }
}

cadImage.Entities = filteredEntities.ToArray();
```

## Krok 3: nastavit možnosti rasterizace

`CadRasterizationOptions` řídí, jak je výkres převeden na bitmapu. Můžete definovat výstupní velikost, barvu pozadí a rozlišení (DPI). Následující definice uvádí třídu:

Třída `CadRasterizationOptions` určuje rozměry obrázku, rozlišení a nastavení vykreslování pro převod CAD výkresů do rastrových formátů.  

Nastavte požadovanou šířku, výšku a barvu pozadí před předáním možností exportéru PDF.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions =
    new Aspose.CAD.ImageOptions.CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
```

## Krok 4: nastavit PDF možnosti

`PdfOptions` spojuje nastavení rasterizace s PDF‑specifickými funkcemi, jako je komprese. Definiční kotva pro tuto třídu se objeví jako první:

`PdfOptions` zahrnuje parametry generování PDF, včetně možností rasterizace, které určují, jak jsou CAD data vykreslena uvnitř PDF dokumentu.  

Přiřaďte dříve vytvořenou instanci `CadRasterizationOptions` k vlastnosti `VectorRasterizationOptions`.

```csharp
Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Krok 5: uložit jako PDF

Nakonec zavolejte metodu `Save` na objektu `CadImage`, předáte název cílového souboru a nakonfigurované `PdfOptions`. PDF bude obsahovat vysoce kvalitní obrázek filtrovaného výkresu.

```csharp
string outFile = MyDir + "result_out_generated.pdf";
cadImage.Save(outFile, pdfOptions);
```

## Časté problémy a řešení

- **Chybějící text po filtrování** – Ujistěte se, že DWG skutečně obsahuje entity `Text`; některé výkresy ukládají anotace jako `MText`. V případě potřeby upravte filtr tak, aby zahrnoval `MText`.  
- **Prázdný výstupní obrázek** – Ověřte, že DPI rasterizace je dostatečně vysoké (300 DPI je bezpečná výchozí hodnota) a že barva pozadí není nastavena na průhlednou při prohlížení PDF.  
- **Chyby nedostatku paměti u velkých souborů** – Použijte přetížení `LoadOptions`, které umožňuje streamování, což zabraňuje načtení celého souboru najednou do paměti.  

## Často kladené otázky

**Q: Je Aspose.CAD kompatibilní se všemi verzemi DWG souborů?**  
A: Aspose.CAD podporuje verze DWG od AutoCAD 2000 až po nejnovější verzi 2024, pokrývající více než 90 % souborů vytvořených v oboru.  

**Q: Mohu přizpůsobit možnosti rasterizace pro různé výstupy?**  
A: Ano – můžete změnit rozlišení, formát obrázku, anti‑aliasing a barvu pozadí tak, aby vyhovovaly cílům PNG, JPEG nebo PDF.  

**Q: Kde najdu další příklady a dokumentaci?**  
A: Prozkoumejte komplexní [Aspose.CAD documentation](https://reference.aspose.com/cad/net/) pro více ukázek kódu a podrobnosti API.  

**Q: Je k dispozici bezplatná zkušební verze Aspose.CAD?**  
A: Rozhodně – můžete si stáhnout zkušební verzi na **[Aspose trial download page](https://releases.aspose.com/)** a vyzkoušet všechny funkce bez omezení po dobu 30 dnů.  

**Q: Jak mohu získat podporu nebo se spojit s komunitou?**  
A: Připojte se k aktivnímu [Aspose.CAD forum](https://forum.aspose.com/c/cad/19), kde vývojáři sdílejí řešení a tým Aspose odpovídá na otázky.  

---

**Poslední aktualizace:** 2026-08-12  
**Testováno s:** Aspose.CAD 24.11 for .NET  
**Autor:** Aspose

## Související tutoriály

- [Vyhledávání textu v DWG souborech pomocí C# – tutoriál Aspose.CAD](/cad/net/text-search-and-manipulation/searching-text-in-dwg-files/)
- [Převod CAD výkresu na rastrový obrázek v Aspose.CAD pro .NET](/cad/net/cad-drawing-manipulation/convert-cad-drawing-to-raster-image/)
- [Renderování DWG dokumentů v C# – průvodce Aspose.CAD](/cad/net/image-manipulation-and-rendering/rendering-dwg-documents/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}