---
date: 2026-03-13
description: Naučte se, jak nastavit možnosti rasterizace CAD a exportovat konkrétní
  rozvržení DWG do PDF pomocí Aspose.CAD pro .NET – definitvní průvodce tvorbou PDF
  z CAD souboru.
linktitle: Exporting Specific Layouts to PDF
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Nastavit možnosti rasterizace CAD – Exportovat konkrétní rozvržení do PDF –
  Průvodce Aspose.CAD
url: /cs/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/
weight: 13
---

.

Now produce final content.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export konkrétních rozvržení do PDF – Aspose.CAD Guide

## Úvod

V tomto tutoriálu se dozvíte **jak nastavit CAD rasterizační možnosti**, abyste mohli exportovat jedno rozvržení – nebo více rozvržení – z DWG souboru přímo do PDF. Aspose.CAD pro .NET usnadňuje proces *dwg to pdf conversion c#*, poskytuje vám plnou kontrolu nad velikostí stránky, rozlišením a výběrem rozvržení. Na konci průvodce budete schopni **vytvořit PDF ze souboru CAD** pomocí několika řádků kódu.

## Rychlé odpovědi
- **Co dělá „set cad rasterization options“?**  
  Říká Aspose.CAD, jak vykreslit vektorová data (rozvržení, vrstvy, tloušťky čar) do rasterizovaných stránek PDF.  
- **Která metoda exportuje rozvržení DWG do PDF?**  
  Použijte `Image.Save` s nakonfigurovaným `PdfOptions`, který obsahuje vaše `CadRasterizationOptions`.  
- **Mohu exportovat více než jedno rozvržení najednou?**  
  Ano – poskytněte pole názvů rozvržení v vlastnosti `Layouts`.  
- **Potřebuji licenci pro produkční použití?**  
  Je vyžadována komerční licence; pro vyhodnocení je k dispozici bezplatná zkušební verze.  
- **Jaké verze .NET jsou podporovány?**  
  .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6 a novější.

## Co je „set cad rasterization options“?
`CadRasterizationOptions` je třída, která řídí, jak jsou CAD entity rasterizovány při konverzi do rastrových formátů, jako je PDF. Nastavením jejích vlastností – rozměry stránky, výběr rozvržení, barva pozadí atd. – určujete vizuální výsledek operace **export dwg layout to pdf**.

## Proč nastavit CAD rasterizační možnosti?
- **Přesnost** – Zachová tloušťky čar a měřítka přesně tak, jak se objevují v originálním CAD výkresu.  
- **Výkon** – Vykreslí pouze rozvržení, která potřebujete, čímž sníží velikost souboru a dobu zpracování.  
- **Flexibilita** – Nastavte šířku/výšku stránky, DPI a pozadí tak, aby odpovídaly vašim standardům reportování.  

## Předpoklady

Než se ponoříme do kódu, ujistěte se, že máte:

- **Aspose.CAD pro .NET** nainstalovaný. Můžete jej stáhnout [zde](https://releases.aspose.com/cad/net/).  
- Vývojové prostředí .NET (Visual Studio, VS Code nebo jakékoli jiné IDE dle preference).  
- DWG soubor, který obsahuje alespoň jedno rozvržení (ukázkový soubor použitý zde je `visualization_-_conference_room.dwg`).

## Importujte jmenné prostory

Ve vašem .NET projektu importujte potřebné jmenné prostory pro Aspose.CAD:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Průvodce krok za krokem

### Krok 1: Načtení DWG souboru

Nejprve nasměrujte Aspose.CAD na zdrojový DWG soubor, který chcete převést.

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";

using (Image image = Image.Load(sourceFilePath))
{
    // Your code for further steps goes here.
}
```

### Krok 2: Nastavte **CadRasterizationOptions**

Zde konfiguruje nastavení rasterizace, které určuje velikost stránky PDF a rozlišení.

```csharp
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
```

> **Tip:** Upravit `PageWidth` a `PageHeight` tak, aby odpovídaly rozměrům cílového PDF rozvržení. Větší hodnoty zvyšují detail, ale také velikost souboru.

### Krok 3: Zadejte název rozvržení

Řekněte Aspose.CAD, které rozvržení(a) má vykreslit. Nahraďte `"Layout1"` přesným názvem rozvržení ve vašem DWG souboru.

```csharp
// Specify desired layout name
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

> **Proč je to důležité:** Omezením pole `Layouts` zabráníte exportu nechtěných listů, čímž urychlíte operaci **dwg to pdf conversion c#** a výsledné PDF bude čistší.

### Krok 4: Vytvořte `PdfOptions`

Propojte nastavení rasterizace s možnostmi exportu PDF.

```csharp
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();
// Set the VectorRasterizationOptions property
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### Krok 5: Export do PDF

Nakonec uložte vykreslené rozvržení jako PDF soubor.

```csharp
MyDir = MyDir + "ExportSpecificLayoutToPDF_out.pdf";
// Export the DWG to PDF
image.Save(MyDir, pdfOptions);
```

### Krok 6: Zobrazte zprávu o úspěchu

Rychlý výstup do konzole potvrdí, že operace byla úspěšná.

```csharp
// Display success message
Console.WriteLine("\nThe DWG file with a specific layout exported successfully to PDF.\nFile saved at " + MyDir);
```

## Časté problémy a řešení

| Problém | Příčina | Řešení |
|---------|---------|--------|
| **PDF nebyl vytvořen** | Pole `Layouts` neodpovídá žádnému názvu rozvržení v DWG. | Ověřte názvy rozvržení pomocí CAD prohlížeče a aktualizujte vlastnost `Layouts`. |
| **Prázdné stránky** | `PageWidth`/`PageHeight` nastaveny na 0 nebo extrémně malé hodnoty. | Použijte realistické rozměry (např. 1600 × 1600) nebo nechte Aspose vypočítat automaticky vynecháním těchto vlastností. |
| **Nesprávné měřítko** | Není nastaveno DPI, když je vyžadován výstup ve vysokém rozlišení. | Nastavte `rasterizationOptions.Resolution = 300;` (nebo požadované DPI) před exportem. |

## Často kladené otázky

**Q: Mohu exportovat více rozvržení najednou?**  
A: Ano, jednoduše upravte pole `Layouts` v kroku 3 tak, aby zahrnovalo všechny požadované názvy rozvržení, např. `new string[] { "Layout1", "Layout2" }`.

**Q: Je Aspose.CAD kompatibilní s jinými formáty CAD souborů?**  
A: Rozhodně. Podporuje DWG, DXF, DWF, DGN a mnoho dalších formátů.

**Q: Jak mohu upravit nastavení výstupu PDF mimo velikost stránky?**  
A: Prozkoumejte další vlastnosti `CadRasterizationOptions`, jako jsou `Resolution`, `BackgroundColor` a `DrawType`, pro jemné doladění výsledku.

**Q: Kde mohu najít další dokumentaci k Aspose.CAD?**  
A: Navštivte [dokumentaci](https://reference.aspose.com/cad/net/) pro podrobné reference API a příklady.

**Q: Je k dispozici bezplatná zkušební verze?**  
A: Ano, bezplatnou zkušební verzi můžete získat [zde](https://releases.aspose.com/).

## Závěr

Nyní jste se naučili, jak **nastavit CAD rasterizační možnosti** a použít je k **exportu konkrétních DWG rozvržení do PDF** s Aspose.CAD pro .NET. Tento přístup vám poskytuje přesnou kontrolu nad procesem konverze, což vám umožní rychle a spolehlivě integrovat funkci CAD‑to‑PDF do jakékoli C# aplikace.

---

**Last Updated:** 2026-03-13  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}