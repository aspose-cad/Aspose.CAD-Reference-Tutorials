---
date: 2026-03-29
description: Naučte se, jak nastavit možnosti rasterizace CAD a exportovat DGN do
  PDF s podporou 3D pomocí Aspose.CAD pro .NET.
linktitle: Support of 3D for DGN V7
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Konfigurace možností rasterizace CAD pro DGN V7 3D
url: /cs/net/cad-features-and-support/support-of-3d-for-dgn-v7/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Nastavení možností rasterizace CAD pro DGN V7 3D

## Úvod

V tomto komplexním tutoriálu se naučíte **jak nastavit možnosti rasterizace CAD**, abyste exportovali 3‑D soubor DGN V7 do PDF pomocí Aspose.CAD pro .NET. Ať už vytváříte CAD prohlížeč, nástroj pro reportování nebo automatizovanou konverzní pipeline, zvládnutí těchto nastavení vám poskytne přesnou kontrolu nad velikostí stránky, měřítkem rozvržení, barvami pozadí a konkrétními pohledy, které chcete vykreslit. Projdeme proces krok za krokem.

## Rychlé odpovědi
- **Co znamená „nastavit možnosti rasterizace CAD“?**  
  Odkazuje na nastavení vlastností, jako jsou rozměry stránky, měřítko, barva pozadí a výběr rozvržení před konverzí CAD souboru do rastrového formátu (např. PDF).
- **Jak exportovat DGN do PDF s podporou 3‑D?**  
  Načtěte DGN pomocí `DgnImage`, definujte `PdfOptions` + `CadRasterizationOptions` a poté zavolejte `Save`.
- **Potřebuji licenci pro produkční použití?**  
  Ano – pro nasazení je vyžadována komerční licence; je k dispozici bezplatná zkušební verze.
- **Které verze .NET jsou podporovány?**  
  .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.
- **Mohu vybrat konkrétní pohledy k exportu?**  
  Samozřejmě – nastavte pole `Layouts` v možnostech rasterizace.

## Co znamená „nastavit možnosti rasterizace CAD“?

Nastavení možností rasterizace CAD znamená přizpůsobení toho, jak je CAD výkres rasterizován (převáděn z vektoru na bitmapu nebo PDF). Úpravou těchto nastavení řídíte vizuální výstup, výkon a velikost souboru výsledného dokumentu.

## Proč použít Aspose.CAD pro export 3‑D DGN V7?

- **Plná integrace s .NET** – není vyžadován COM ani nativní DLL.  
- **Podporuje 3‑D geometrii** – zachovává informace o hloubce při vykreslování do PDF.  
- **Detailní kontrola** – vyberte přesná rozvržení, měřítko a barvy pozadí.  
- **Cross‑platform** – funguje na Windows, Linuxu a macOS s .NET Core.

## Požadavky

Před začátkem se ujistěte, že máte:

- **Aspose.CAD pro .NET** – stáhněte jej z [zde](https://releases.aspose.com/cad/net/).  
- **Visual Studio** nebo jakékoli kompatibilní .NET IDE.  
- **Ukázkový soubor DGN** – pro tento návod použijeme `Nikon_D90_Camera.dgn` (součástí Aspose vzorového balíčku).  

Nyní, když je vše připraveno, ponořme se do kódu.

## Importovat jmenné prostory

Ve vašem .NET projektu importujte požadované jmenné prostory:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.ImageOptions;
```

## Krok 1: Nastavte adresář dokumentu

Vytvořte proměnnou, která ukazuje na složku, kde budou umístěny váš zdrojový DGN a výstupní soubory.

```csharp
string MyDir = "Your Document Directory";
```

## Krok 2: Načtěte soubor DGN

Načtěte soubor DGN jako `DgnImage`. Tento objekt vám poskytuje přístup k CAD datům a pipeline rasterizace.

```csharp
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";
string outFile = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Your code for further processing goes here
}
```

## Krok 3: Nastavte možnosti exportu PDF (Nastavení možností rasterizace CAD)

Zde **nastavujeme možnosti rasterizace CAD**, které určují, jak bude 3‑D model vykreslen do PDF. Můžete upravit velikost stránky, povolit automatické měřítko rozvržení, nastavit barvu pozadí a vybrat přesná rozvržení (pohledy), které chcete exportovat.

```csharp
var options = new PdfOptions
{
    VectorRasterizationOptions = new CadRasterizationOptions
    {
        PageWidth = 1500,
        PageHeight = 1500,
        AutomaticLayoutsScaling = true,
        BackgroundColor = Color.Black,
        Layouts = new string[] { "1", "2", "3", "9" } // Only export specified views
    }
};
```

## Krok 4: Uložte rastrový obrázek

Nakonec exportujte DGN do PDF souboru pomocí právě nastavených možností.

```csharp
dgnImage.Save(outFile, options);
```

## Časté problémy a řešení

| Problém | Řešení |
|-------|----------|
| **Prázdný PDF výstup** | Ověřte, že pole `Layouts` obsahuje správné identifikátory pohledů přítomné v souboru DGN. |
| **Nesprávné barvy** | Ujistěte se, že `BackgroundColor` je nastaven na požadovanou hodnotu; použijte `Color.White` pro světlé pozadí. |
| **Úzké hrdlo výkonu u velkých souborů** | Povolte `AutomaticLayoutsScaling` a zvažte snížení `PageWidth/PageHeight` pro menší rozlišení rastru. |
| **Licenční výjimka** | Nainstalujte platnou licenci Aspose.CAD před načtením obrázku, aby se zabránilo vodoznakům z trial verze. |

## Často kladené otázky

**Q: Mohu použít Aspose.CAD pro .NET s jinými formáty CAD souborů?**  
A: Ano, Aspose.CAD podporuje DWG, DXF, DWF, DGN a mnoho dalších formátů.

**Q: Jak mohu ošetřit výjimky při práci s Aspose.CAD?**  
A: Zabalte svůj kód do bloku `try‑catch` a prozkoumejte `Aspose.CAD.CADException` pro podrobné informace o chybě.

**Q: Je Aspose.CAD vhodný pro komerční projekty?**  
A: Rozhodně. Můžete zakoupit licenci [zde](https://purchase.aspose.com/buy).

**Q: Můžu vyzkoušet Aspose.CAD pro .NET před zakoupením?**  
A: Ano, je k dispozici bezplatná zkušební verze [zde](https://releases.aspose.com/).

**Q: Kde mohu najít komunitní podporu pro Aspose.CAD?**  
A: Připojte se k diskusnímu fóru [zde](https://forum.aspose.com/c/cad/19).

---

**Last Updated:** 2026-03-29  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}