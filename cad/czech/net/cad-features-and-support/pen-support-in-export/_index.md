---
date: 2026-03-26
description: Naučte se, jak vytvořit PDF z CAD a převést DXF na PDF pomocí Aspose.CAD
  pro .NET. Přizpůsobte možnosti pera pro úchvatné vizuály v PDF, PNG, BMP a dalších.
linktitle: Pen Support in Export
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Vytvořte PDF z CAD s vlastními možnostmi pera – Aspose.CAD pro .NET
url: /cs/net/cad-features-and-support/pen-support-in-export/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Zvyšte export CAD s vlastními možnostmi pera v Aspose.CAD pro .NET

## Úvod

Pokud potřebujete **vytvořit PDF z CAD** souborů rychle a s plnou vizuální kontrolou, Aspose.CAD pro .NET vám to přesně umožní. Využitím funkce podpory pera v knihovně můžete definovat počáteční a koncové zakončení, spojení čar a další atributy kreslení, čímž vytvoříte PDF soubory, které vypadají přesně tak, jak chcete. Tento tutoriál vás provede celým procesem – od načtení DXF souboru po export vylepšeného PDF – a zároveň ukáže, jak lze stejná nastavení znovu použít při **exportu CAD do PNG** nebo **rasterizaci CAD obrázku** pro jiné formáty.

## Rychlé odpovědi
- **Co znamená „vytvořit PDF z CAD“?** Převádí vektorové CAD výkresy (např. DXF) do PDF dokumentu při zachování geometrie a stylování.  
- **Které formáty podporují možnosti pera?** PDF, PNG, BMP, GIF, JPEG2000, JPEG, PSD, TIFF a WMF.  
- **Potřebuji licenci pro vývoj?** Bezplatná zkušební verze funguje pro testování; pro produkční nasazení je vyžadována komerční licence.  
- **Mohu změnit zakončení čar pro jiné formáty?** Ano – možnosti pera se aplikují na jakýkoli rasterizační cíl podporovaný Aspose.CAD.  
- **Jaké verze .NET jsou podporovány?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## Co je podpora pera při exportu CAD?

Podpora pera vám umožňuje přizpůsobit, jak jsou čáry kresleny, když je CAD výkres rasterizován nebo vektor‑rasterizován. Můžete nastavit vlastnosti jako `StartCap`, `EndCap`, `LineJoin` a `DashStyle`. Tato nastavení ovlivňují konečný vzhled exportovaného obrázku nebo PDF a poskytují detailní kontrolu nad vizuální kvalitou.

## Proč použít vlastní možnosti pera při **vytváření PDF z CAD**?

- **Konzistentní značení** – sladíte firemní styly čar napříč všemi dokumenty.  
- **Zlepšená čitelnost** – silnější zakončení a spoje činí technické výkresy přehlednějšími na obrazovce i v tisku.  
- **Flexibilita napříč formáty** – stejná konfigurace pera funguje pro PNG, BMP a další rasterové formáty, čímž šetříte čas.

## Požadavky

- Aspose.CAD pro .NET nainstalován (stáhněte z [release page](https://releases.aspose.com/cad/net/)).  
- Základní znalost DXF (Drawing Exchange Format).  
- Zkušenost s programováním v C#.

## Import Namespaces

Abyste mohli začít, ujistěte se, že ve svém C# projektu importujete potřebné jmenné prostory:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Drawing;
using System.Drawing.Drawing2D;
```

## Krok 1: Nastavte adresář dokumentu

Definujte složku, která obsahuje zdrojový CAD soubor:

```csharp
string MyDir = "Your Document Directory";
```

## Krok 2: Načtěte CAD obrázek

Načtěte CAD výkres (například DXF soubor) do objektu `Aspose.CAD.Image`:

```csharp
string sourceFilePath = MyDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage)Image.Load(sourceFilePath);
```

## Krok 3: Nakonfigurujte rasterizační možnosti

Vytvořte objekty rasterizačních a PDF možností. Tyto objekty vám umožní řídit, jak jsou CAD data převedena na rastrový obrázek nebo PDF stránku:

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
PdfOptions pdfOptions = new PdfOptions();
```

## Krok 4: Přizpůsobte možnosti pera

Zde **přizpůsobujete pero**, které kreslí čáry. Můžete nastavit počáteční a koncové zakončení na `Flat`, `Round`, `Square` atd. Toto je jádro „jak exportovat CAD“ s požadovaným vizuálním stylem:

```csharp
rasterizationOptions.PenOptions = new PenOptions
{
   StartCap = LineCap.Flat,
   EndCap = LineCap.Flat
};
```

*Tip:* Experimentujte s `LineCap.Round` pro hladší konce čar při **exportu CAD do PNG**.

## Krok 5: Použijte možnosti vektorové rasterizace

Připojte rasterizační nastavení k PDF možnostem, aby exportní proces věděl, kterou konfiguraci pera použít:

```csharp
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Krok 6: Uložte exportované PDF

Nakonec vygenerujte PDF soubor. Tento krok **vytváří PDF z CAD** s aplikovanými vlastními nastaveními pera:

```csharp
cadImage.Save(MyDir + "9LHATT-A56_generated.pdf", pdfOptions);
```

Můžete nahradit `PdfOptions` za `PngOptions`, `BmpOptions` atd., abyste **exportovali CAD do PNG** nebo jiných rasterových formátů při zachování stejné konfigurace pera.

## Běžné scénáře použití

- **Technická dokumentace** – vložte přesné styly čar do inženýrských PDF.  
- **Automatizovaná tvorba reportů** – hromadně zpracovávejte mnoho DXF souborů do PDF s jedním profilem pera.  
- **Webové služby** – vystavte API, které převádí nahrané DXF soubory na PDF za běhu, zajišťující konzistentní stylování.

## Řešení problémů a časté úskalí

| Problém | Důvod | Řešení |
|-------|--------|----------|
| Exportované čáry jsou silnější, než se očekává | DPI je vyšší, než bylo zamýšleno | Nastavte `rasterizationOptions.PageWidth` / `PageHeight` nebo upravte `Resolution`. |
| Možnosti pera jsou ignorovány při výstupu PNG | Používáte `ImageOptions` místo `VectorRasterizationOptions` | Ujistěte se, že při ukládání přiřadíte `rasterizationOptions.PenOptions`. |
| PDF soubor je prázdný | Cesta ke zdrojovému DXF je nesprávná nebo je soubor poškozený | Ověřte `sourceFilePath` a potvrďte, že DXF se načte bez výjimek. |

## Často kladené otázky

### Q1: Mohu tyto možnosti pera použít i pro jiné formáty obrázků než PDF?

A1: Ano, možnosti pera lze aplikovat na různé formáty obrázků, jako jsou PNG, BMP, GIF, JPEG a další.

### Q2: Kde najdu další dokumentaci k Aspose.CAD pro .NET?

A2: Viz [documentation](https://reference.aspose.com/cad/net/) pro komplexní informace a příklady.

### Q3: Je k dispozici bezplatná zkušební verze Aspose.CAD pro .NET?

A3: Ano, bezplatnou zkušební verzi získáte [zde](https://releases.aspose.com/).

### Q4: Jak získám dočasné licence pro Aspose.CAD pro .NET?

A4: Navštivte [temporary license page](https://purchase.aspose.com/temporary-license/) pro možnosti dočasného licencování.

### Q5: Kde mohu získat komunitní podporu pro Aspose.CAD pro .NET?

A5: Zapojte se do komunity na [Aspose.CAD forum](https://forum.aspose.com/c/cad/19).

## Další často kladené otázky

**Q: Jak programově **převést DXF na PDF**?**  
A: Načtěte DXF pomocí `Image.Load`, nakonfigurujte `CadRasterizationOptions` a `PdfOptions`, poté zavolejte `Save` podle kroků výše.

**Q: Můžu rasterizovat CAD obrázek bez vytvoření PDF?**  
A: Ano – použijte `PngOptions`, `BmpOptions` nebo jakoukoli jinou třídu rasterového formátu a přiřaďte stejný `rasterizationOptions` pro dosažení vysoce kvalitní rasterizace.

**Q: Je možné změnit šířku čáry při vytváření PDF z CAD?**  
A: Upravit můžete `rasterizationOptions.CustomLineWidth` nebo vlastnost `PenOptions.Width` před uložením.

**Q: Podporuje knihovna 3D DXF soubory?**  
A: Aspose.CAD se zaměřuje na 2D vektorová data; 3D entity jsou při rasterizaci ignorovány.

**Q: Jaká verze Aspose.CAD je pro tyto funkce vyžadována?**  
A: Podpora pera je k dispozici od verze 20.9; jakákoli novější verze bude fungovat.

---

**Poslední aktualizace:** 2026-03-26  
**Testováno s:** Aspose.CAD pro .NET 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}