---
date: 2026-03-24
description: Naučte se, jak převést DGN na PDF (a PNG) s 3D podporou pro DGN V7 pomocí
  Aspose.CAD pro .NET – krok za krokem průvodce.
linktitle: 3D Support for DGN V7
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Převod DGN na PDF (3D podpora) s Aspose.CAD pro .NET
url: /cs/net/cad-features-and-support/3d-support-for-dgn-v7/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Převod DGN na PDF (3D podpora) s Aspose.CAD pro .NET

## Úvod

V moderních CAD pracovních postupech je schopnost **převést DGN na PDF** rychle a zachovat 3‑D geometrii nezbytná. Ať už vytváříte dokumentaci, sdílíte návrhy s ne‑CAD uživateli nebo archivujete projekty, Aspose.CAD pro .NET vám poskytuje spolehlivý způsob, jak převést soubory DGN V7 na výstupy PDF (a dokonce PNG) vysoké kvality. V tomto tutoriálu vás provedeme přesné kroky potřebné k povolení 3D podpory a vytvoření PDF ze souboru DGN.

## Rychlé odpovědi
- **Co tutoriál pokrývá?** Povolení 3D podpory a převod DGN V7 na PDF pomocí Aspose.CAD pro .NET.  
- **Jaký primární formát je vytvořen?** PDF (s volitelným exportem PNG).  
- **Potřebuji licenci?** Bezplatná zkušební verze funguje pro testování; pro produkční nasazení je vyžadována komerční licence.  
- **Podporované verze .NET?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Jak dlouho trvá implementace?** Přibližně 10‑15 minut pro základní převod.

## Co znamená „převod DGN na PDF“?

Převod DGN na PDF znamená vykreslení vektorových dat uložených v souboru MicroStation DGN do přenosného formátu dokumentu, který lze zobrazit na jakémkoli zařízení bez specializovaného CAD softwaru. S 3‑D rasterizačním enginem Aspose.CAD převod zachovává rozvržení, barvy a hloubkové indicie, čímž poskytuje věrnou vizuální reprezentaci.

## Proč použít Aspose.CAD pro tento převod?

- **Plná 3‑D rasterizace** – zachovává informace o hloubce a rozvržení.  
- **Žádné externí závislosti** – čistá .NET knihovna, není potřeba MicroStation.  
- **Více výstupních formátů** – PDF, PNG, JPEG, TIFF atd. (sekundární klíčové slovo *convert dgn to png* je podporováno přímo z krabice).  
- **Cross‑platform** – funguje na Windows, Linuxu i macOS.

## Požadavky

Před začátkem se ujistěte, že máte následující:

- Aspose.CAD pro .NET nainstalovaný. Můžete jej stáhnout ze [stránky ke stažení Aspose.CAD pro .NET](https://releases.aspose.com/cad/net/).
- Platný soubor DGN V7, který chcete zpracovat.
- Vývojové prostředí .NET (Visual Studio, VS Code nebo CLI). Pokyny k instalaci jsou k dispozici v [.NET dokumentaci](https://docs.microsoft.com/en-us/dotnet/core/install/).

## Importujte jmenné prostory

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

Tyto jmenné prostory vám poskytují přístup k základním třídám Aspose.CAD a standardním .NET utilitám.

## Krok 1: Nastavte prostředí

Definujte, kde se nachází váš zdrojový soubor DGN a kam má být uložen výstupní PDF.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";
```

> **Tip:** Použijte `Path.Combine` pro platformově nezávislou konstrukci cesty.

## Krok 2: Načtěte soubor DGN

Vytvořte instanci `DgnImage` načtením souboru pomocí `Image.Load`. Tento krok připraví CAD data pro rasterizaci.

```csharp
using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Code snippet continues...
}
```

## Krok 3: Nakonfigurujte možnosti exportu

Nastavte `PdfOptions` spolu s `CadRasterizationOptions`. Zde řídíte velikost stránky, pozadí a které rozvržení (pohledy) exportovat.

```csharp
var options = new PdfOptions
{
    VectorRasterizationOptions = new CadRasterizationOptions
    {
        PageWidth = 1500,
        PageHeight = 1500,
        CenterDrawing = true,
        AutomaticLayoutsScaling = true,
        BackgroundColor = Color.Black,
        Layouts = new string[] { "1", "2", "3", "9" } // Export specific views
    }
};
```

Pokud místo toho potřebujete **převést DGN na PNG**, jednoduše nahraďte `PdfOptions` za `PngOptions` a zachovejte stejné nastavení rasterizace.

## Krok 4: Uložte výsledek

Nakonec zapište vykreslený výstup na požadované místo.

```csharp
string outFile = "Your Output Directory"; // Specify the output directory
dgnImage.Save(outFile, options);
```

Po spuštění najdete soubor PDF (nebo PNG, pokud jste změnili možnosti), který věrně představuje původní 3‑D výkres DGN.

## Časté problémy a tipy

- **Chybějící rozvržení:** Ujistěte se, že názvy rozvržení v `Layouts` odpovídají těm v souboru DGN; jinak budou ignorovány.  
- **Velké soubory:** Postupně zvyšujte `PageWidth`/`PageHeight`, aby nedošlo k vysoké spotřebě paměti.  
- **Přesnost barev:** Pokud se pozadí jeví tmavé, ověřte, že `BackgroundColor` je nastaven na požadovanou hodnotu (např. `Color.White`).

## Závěr

Nyní ovládáte, jak **převést DGN na PDF** s plnou 3‑D podporou pomocí Aspose.CAD pro .NET. Tento pracovní postup lze integrovat do automatizovaných pipeline, desktopových utilit nebo webových služeb k poskytování CAD vizualizací jakémukoli publiku.

## Často kladené otázky

### Q1: Mohu pomocí tohoto přístupu zpracovávat více souborů DGN současně?

A1: Ano, můžete upravit kód tak, aby zpracovával více souborů ve smyčce nebo jako součást dávkového zpracování.

### Q2: Jaké další exportní formáty podporuje Aspose.CAD pro .NET?

A2: Aspose.CAD pro .NET podporuje různé exportní formáty, včetně PDF, PNG, JPG a dalších. Podrobnosti najdete v [dokumentaci](https://reference.aspose.com/cad/net/).

### Q3: Je Aspose.CAD pro .NET kompatibilní s nejnovějšími verzemi .NET Core?

A3: Ano, Aspose.CAD pro .NET je navržen tak, aby byl kompatibilní s nejnovějšími verzemi .NET Core. Ujistěte se, že máte ve svém prostředí nainstalovanou odpovídající verzi.

### Q4: Mohu dále přizpůsobit nastavení exportu pro své konkrétní požadavky?

A4: Rozhodně! Poskytnutý kód nabízí výchozí bod. Další možnosti a konfigurace můžete prozkoumat v [dokumentaci Aspose.CAD](https://reference.aspose.com/cad/net/).

### Q5: Kde mohu získat pomoc nebo sdílet své zkušenosti s Aspose.CAD pro .NET?

A5: Připojte se ke komunitě Aspose.CAD na [fóru](https://forum.aspose.com/c/cad/19), kde můžete komunikovat s ostatními vývojáři a požádat o pomoc.

---

**Poslední aktualizace:** 2026-03-24  
**Testováno s:** Aspose.CAD 24.11 pro .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}