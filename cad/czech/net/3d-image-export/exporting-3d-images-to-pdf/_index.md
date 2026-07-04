---
date: 2026-07-04
description: Naučte se, jak nastavit velikost stránky PDF a exportovat PDF z 3D CAD
  obrázků pomocí Aspose.CAD pro .NET – podrobný návod krok za krokem k převodu DWG
  na PDF a uložení CAD jako PDF.
keywords:
- set pdf page size
- export pdf from cad
- convert dwg to pdf
- save cad as pdf
- cad to pdf tutorial
linktitle: Export 3D obrázků do PDF
schemas:
- author: Aspose
  dateModified: '2026-07-04'
  description: Learn how to set PDF page size and export PDF from 3D CAD images using
    Aspose.CAD for .NET – a step‑by‑step guide to convert DWG to PDF and save CAD
    as PDF.
  headline: Set PDF page size – Export 3D Images to PDF with Aspose.CAD
  type: TechArticle
- description: Learn how to set PDF page size and export PDF from 3D CAD images using
    Aspose.CAD for .NET – a step‑by‑step guide to convert DWG to PDF and save CAD
    as PDF.
  name: Set PDF page size – Export 3D Images to PDF with Aspose.CAD
  steps:
  - name: Load the CAD Image
    text: '`Image` class represents a CAD drawing loaded into memory, ready for rasterization.'
  - name: Configure Rasterization Options (Save CAD as PDF)
    text: '`RasterizationOptions` class defines how the CAD data is rasterized, including
      page size, DPI, and whether 3‑D entities are rendered.'
  - name: Set PDF Options (Create PDF from CAD)
    text: '`PdfOptions` class holds the output format settings and links the rasterization
      options to PDF generation.'
  - name: Save as PDF (Generate PDF from 3D Model)
    text: '`Save` method on the `Image` object writes the rasterized content to the
      specified PDF file, producing a ready‑to‑share document.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD supports more than 50 input and output formats, including
      DWG, DXF, DGN, STL, and IFC, ensuring flexibility for any project.
    question: Is Aspose.CAD compatible with all CAD file formats?
  - answer: Absolutely. Set `PageWidth` and `PageHeight` in `RasterizationOptions`
      to any size in points, inches, or millimetres before calling `Save`.
    question: Can I customize the page dimensions when exporting to PDF?
  - answer: Yes, you can obtain temporary licenses for Aspose.CAD by visiting [Temporary
      License](https://purchase.aspose.com/temporary-license/).
    question: Are temporary licenses available for Aspose.CAD?
  - answer: Head to the [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) for
      expert help and peer‑to‑peer advice.
    question: Where can I find additional support or community discussions?
  - answer: Yes, you can explore the features of Aspose.CAD by accessing the [free
      trial](https://releases.aspose.com/).
    question: Is there a free trial version of Aspose.CAD?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Nastavte velikost stránky PDF – Export 3D obrázků do PDF pomocí Aspose.CAD
url: /cs/net/3d-image-export/exporting-3d-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportování 3D obrázků do PDF – tutoriál Aspose.CAD

## Úvod

Pokud potřebujete **nastavit velikost stránky PDF** při převodu 3‑D CAD výkresu do PDF, jste na správném místě. Tento tutoriál vám krok za krokem ukáže, jak načíst CAD soubor, nakonfigurovat možnosti rasterizace — včetně vlastních rozměrů stránky — a vygenerovat vysoce kvalitní PDF pomocí Aspose.CAD pro .NET. Na konci budete schopni **exportovat PDF z CAD**, **uložit CAD jako PDF** a ovládat každý detail rozvržení bez instalace AutoCADu.

## Rychlé odpovědi
- **Co znamená „export PDF z CAD“?** Převádí CAD výkres (DWG, DXF, DGN atd.) do PDF, které lze otevřít na jakémkoli zařízení.  
- **Která knihovna provádí převod?** Aspose.CAD pro .NET poskytuje rasterizaci a export do PDF bez externích závislostí.  
- **Potřebuji licenci?** Pro produkční použití je vyžadována dočasná nebo plná licence; k dispozici je také bezplatná zkušební verze.  
- **Mohu nastavit vlastní rozměry stránky?** Ano — použijte `PageWidth` a `PageHeight` v `RasterizationOptions`.  
- **Zůstane 3‑D geometrie zachována?** 3‑D entity jsou rasterizovány; pro plnou podporu 3‑D povolte `TypeOfEntities.Entities3D`.

## Co znamená „export PDF“ v kontextu CAD?

Export PDF z CAD znamená převést CAD výkres (DWG, DXF, DGN atd.) do souboru PDF, který může obsahovat vektorovou grafiku, rasterizované 3‑D pohledy a přesné informace o rozvržení stránky, což usnadňuje sdílení s kýmkoli, kdo nemá CAD software.

## Proč použít Aspose.CAD k exportu PDF?

Aspose.CAD vám umožňuje **nastavit velikost stránky PDF** a exportovat PDF kompletně v řízeném .NET kódu. Podporuje více než 50 CAD formátů, zpracovává soubory až do 2 GB bez načítání celého dokumentu do paměti a zachovává tloušťky čar, barvy a volitelné vykreslování 3‑D entit s rasterizační DPI až 1200. Knihovna běží na Windows, Linuxu i macOS, takže generovaná PDF fungují na jakékoli platformě.

## Požadavky

- **Aspose.CAD pro .NET** nainstalováno. Stáhněte jej ze [Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/).  
- Složka obsahující CAD soubory, které chcete převést (např. `C:\CAD\`).  
- .NET 6.0 nebo novější (nebo .NET Framework 4.7.2).  

## Importování jmenných prostorů

`using` příkazy importují potřebné jmenné prostory Aspose.CAD pro práci s rasterizačními a PDF možnostmi.  

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

## Průvodce krok za krokem

### Jak nastavit velikost stránky PDF při exportu CAD do PDF?

Načtěte svůj CAD soubor, nakonfigurujte rozměry stránky v `RasterizationOptions`, přiřaďte tyto možnosti k instanci `PdfOptions` a zavolejte `Save`. Tento čtyřkrokový postup vám poskytne plnou kontrolu nad velikostí a kvalitou výstupu při zachování stručnosti kódu.

### Krok 1: Načtení CAD obrázku

Třída `Image` představuje CAD výkres načtený do paměti, připravený k rasterizaci.  

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image cadImage = Image.Load(sourceFilePath))
{
    // Your code for loading the CAD image goes here
}
```

### Krok 2: Konfigurace možností rasterizace (Uložit CAD jako PDF)

Třída `RasterizationOptions` určuje, jak jsou CAD data rasterizována, včetně velikosti stránky, DPI a toho, zda jsou vykresleny 3‑D entity.  

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
// rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;

rasterizationOptions.Layouts = new string[] { "Model" };
```

### Krok 3: Nastavení PDF možností (Vytvořit PDF z CAD)

Třída `PdfOptions` obsahuje nastavení výstupního formátu a propojuje rasterizační možnosti s generováním PDF.  

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### Krok 4: Uložení jako PDF (Generování PDF ze 3D modelu)

Metoda `Save` na objektu `Image` zapíše rasterizovaný obsah do určeného PDF souboru a vytvoří připravený dokument ke sdílení.  

```csharp
MyDir = MyDir + "Export3DImagestoPDF_out.pdf";
cadImage.Save(MyDir, pdfOptions);
```

## Časté problémy a řešení

| Problém | Důvod | Řešení |
|-------|--------|-----|
| **Výstupní PDF je prázdné** | Špatný název rozvržení nebo chybějící rozvržení `Model`. | Ověřte, že `rasterizationOptions.Layouts` odpovídá rozvržení přítomnému v CAD souboru. |
| **Nízké rozlišení** | Výchozí rasterizační DPI je nízké. | Před uložením nastavte `rasterizationOptions.Resolution = 300;`. |
| **3‑D entity nejsou zobrazeny** | `TypeOfEntities` je zakomentováno. | Odkomentujte `rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;`. |
| **Výjimka licence** | Používáte zkušební verzi bez licence. | Aplikujte dočasnou nebo trvalou licenci pomocí `License license = new License(); license.SetLicense("Aspose.CAD.lic");`. |

## Často kladené otázky

**Q: Je Aspose.CAD kompatibilní se všemi formáty CAD souborů?**  
A: Ano, Aspose.CAD podporuje více než 50 vstupních a výstupních formátů, včetně DWG, DXF, DGN, STL a IFC, což zajišťuje flexibilitu pro jakýkoli projekt.

**Q: Mohu přizpůsobit rozměry stránky při exportu do PDF?**  
A: Rozhodně. Nastavte `PageWidth` a `PageHeight` v `RasterizationOptions` na libovolnou velikost v bodech, palcích nebo milimetrech před voláním `Save`.

**Q: Jsou pro Aspose.CAD k dispozici dočasné licence?**  
A: Ano, dočasné licence pro Aspose.CAD získáte na stránce [Temporary License](https://purchase.aspose.com/temporary-license/).

**Q: Kde mohu najít další podporu nebo komunitní diskuze?**  
A: Navštivte [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) pro odbornou pomoc a výměnu zkušeností mezi uživateli.

**Q: Existuje bezplatná zkušební verze Aspose.CAD?**  
A: Ano, funkce Aspose.CAD můžete vyzkoušet prostřednictvím [free trial](https://releases.aspose.com/).

## Závěr

Nyní máte kompletní, připravený na produkční nasazení postup, jak **nastavit velikost stránky PDF** a **exportovat PDF z 3D CAD obrázků** pomocí Aspose.CAD pro .NET. Úpravou rasterizačních možností můžete jemně doladit rozlišení, rozvržení stránky a vykreslování 3‑D entit tak, aby vyhovovaly jakýmkoli požadavkům dokumentace. Experimentujte s různými nastaveními DPI a rozměry stránky, abyste dosáhli ideální rovnováhy mezi velikostí souboru a vizuální věrností.

{{< blocks/products/products-backtop-button >}}

## Související tutoriály

- [Export konkrétních rozvržení do PDF – průvodce Aspose.CAD](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)
- [Exportování DWG do PDF nebo rastrových obrázků – průvodce Aspose.CAD](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [Export DGN do PDF v Aspose.CAD pro .NET](/cad/net/cad-export-formats/export-dgn-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

**Poslední aktualizace:** 2026-07-04  
**Testováno s:** Aspose.CAD 24.11 pro .NET  
**Autor:** Aspose