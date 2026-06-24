---
date: 2026-04-03
description: Naučte se nastavit viewport a převést DWG do PDF v C# pomocí Aspose.CAD.
  Tento tutoriál převodu DWG na PDF ukazuje přesný export s koordináty.
keywords:
- how to set viewport
- dwg to pdf tutorial
- convert dwg to pdf c#
linktitle: Převod DWG na PDF s koordináty v C#
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Jak nastavit viewport při konverzi DWG do PDF s koordináty v C# – tutoriál
  Aspose.CAD
url: /cs/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Převod DWG na PDF s koordináty v C# – tutoriál Aspose.CAD

## Úvod

Vítejte v tomto komplexním tutoriálu o **jak nastavit viewport** při převodu souborů DWG na PDF se zadanými souřadnicemi pomocí Aspose.CAD pro .NET. Ovládáním viewportu získáte pixel‑dokonalé PDF, které přesně odpovídají požadované oblasti – ideální pro stavební výkresy, náhledy půdorysů nebo jakýkoli BIM workflow.

## Rychlé odpovědi
- **Co znamená „nastavit viewport“?** Definuje viditelnou oblast a měřítko CAD výkresu během rasterizace.  
- **Která knihovna provádí převod?** Aspose.CAD pro .NET.  
- **Potřebuji licenci?** Bezplatná zkušební verze funguje pro hodnocení; pro produkci je vyžadována komerční licence.  
- **Podporované platformy?** Windows, Linux a macOS s .NET 5/6/7 nebo .NET Framework 4.6+.  
- **Typická doba implementace?** Přibližně 10‑15 minut pro základní převod.

## Požadavky

Před zahájením se ujistěte, že máte následující požadavky:

- **Aspose.CAD Library** – Stáhněte a nainstalujte knihovnu Aspose.CAD pro .NET. Knihovnu najdete [zde](https://releases.aspose.com/cad/net/).
- **Development Environment** – Visual Studio, Rider nebo jakékoli IDE podporující vývoj v .NET.
- **DWG File** – Mějte připravený soubor DWG pro převod. Můžete použít poskytnutý ukázkový soubor nebo svůj vlastní DWG soubor.

## Jak nastavit viewport pro přesný export PDF

Nastavení viewportu je klíčovým krokem, který vám umožní definovat přesnou oblast výkresu, kterou chcete vykreslit. V níže uvedeném kódu vytvoříme nový `CadVportTableObject`, umístíme jej pomocí souřadnice vlevo nahoře a vypočítáme šířku, výšku a poměr stran. Toto je implementace **jak nastavit viewport**, která řídí zbytek převodu.

## Importovat jmenné prostory

Ve vašem C# projektu importujte potřebné jmenné prostory:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadParameters;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.ImageOptions;
```

Pojďme rozebrat kód krok za krokem pro lepší pochopení:

## Krok 1: Definovat adresář dokumentu

```csharp
string MyDir = "Your Document Directory";
```

## Krok 2: Nastavit cestu ke zdrojovému souboru DWG

```csharp
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
```

## Krok 3: Načíst soubor DWG a nakonfigurovat možnosti rasterizace

```csharp
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
    rasterizationOptions.Layouts = new string[] { "Model" };
    rasterizationOptions.NoScaling = true;
```

## Krok 4: Definovat souřadnice a viewport  

Zde skutečně **nastavujeme viewport** (jak nastavit viewport) zadáním levého horního rohu, šířky a výšky oblasti, kterou chcete exportovat.

```csharp
    Point topLeft = new Point(500, 1000);
    double width = 3108;
    double height = 2489;

    CadVportTableObject newView = new CadVportTableObject();
    newView.Name = new CadStringParameter();
    newView.Name.Init("*Active");
    newView.CenterPoint.X = topLeft.X + width / 2f;
    newView.CenterPoint.Y = topLeft.Y - height / 2f;
    newView.ViewHeight.Value = height;
    newView.ViewAspectRatio.Value = width / height;
```

## Krok 5: Použít nastavení viewportu

```csharp
    for (int i = 0; i < cadImage.ViewPorts.Count; i++)
    {
        CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
        if (cadImage.ViewPorts.Count == 1 || string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
        {
            cadImage.ViewPorts[i] = newView;
            break;
        }
    }
```

## Krok 6: Nakonfigurovat možnosti PDF a exportovat  

Nyní vše spojíme a **převádíme DWG na PDF** pomocí rasterizačních možností, které jsme právě připravili.

```csharp
    Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
    pdfOptions.VectorRasterizationOptions = rasterizationOptions;

    MyDir = MyDir + "ConvertDWGToPDFBySupplyingCoordinates_out.pdf";
    cadImage.Save(MyDir, pdfOptions);
}
```

## Krok 7: Zobrazit zprávu o úspěchu

```csharp
Console.WriteLine("\nThe DWG file exported successfully to PDF.\nFile saved at " + MyDir);
```

## Běžné případy použití

- **Stavební dokumentace** – Vytvořit tisknutelné PDF konkrétních částí půdorysu.  
- **Koordinace BIM** – Exportovat pouze oblast zájmu pro detekci kolizí.  
- **Prezentace pro klienty** – Poskytnout čisté PDF vybrané místnosti nebo elevace, aniž byste odhalili celý výkres.

## Závěr

Gratuluji! Úspěšně jste **převáděli DWG na PDF** s přesnými souřadnicemi a naučili se **jak nastavit viewport** pomocí Aspose.CAD pro .NET. Tento **dwg to pdf tutoriál** ukazuje, jak **vytvořit PDF z DWG** a **exportovat DWG jako PDF v C#**, přičemž máte plnou kontrolu nad výstupní oblastí.

## Často kladené otázky

### Q1: Mohu použít Aspose.CAD s jinými formáty CAD souborů?

A1: Ano, Aspose.CAD podporuje různé CAD formáty, včetně DWG, DXF, DWF a dalších.

### Q2: Jak mohu zpracovat chyby během procesu převodu?

A2: Implementujte mechanismy zpracování chyb pomocí bloků try‑catch k zachycení a správě výjimek.

### Q3: Je Aspose.CAD vhodný pro prostředí Windows i Linux?

A3: Ano, Aspose.CAD je kompatibilní s platformami Windows i Linux.

### Q4: Mohu dále přizpůsobit výstup PDF?

A4: Určitě! Prozkoumejte rozsáhlé možnosti, které Aspose.CAD poskytuje pro úpravu výstupu PDF podle vašich specifických požadavků.

### Q5: Kde mohu najít další podporu nebo komunitní diskuse?

A5: Navštivte [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) pro komunitní podporu a diskuse.

## Další často kladené otázky

**Q: Funguje tento přístup s velkými soubory DWG (stovky MB)?**  
A: Ano. Rasterizace se provádí stránka po stránce a můžete upravit `rasterizationOptions` (např. `Resolution`) pro vyvážení kvality a využití paměti.

**Q: Mohu exportovat více viewportů do samostatných PDF stránek?**  
A: Můžete iterovat přes `cadImage.ViewPorts`, nastavit každý jako aktivní a volat `Save` pro každou stránku, poté sloučit PDF pomocí Aspose.PDF.

**Q: Je možné přidat vodoznak do vygenerovaného PDF?**  
A: Po uložení PDF jej můžete znovu otevřít pomocí Aspose.PDF a aplikovat textový nebo obrázkový vodoznak před doručením uživateli.

---

**Poslední aktualizace:** 2026-04-03  
**Testováno s:** Aspose.CAD 24.11 for .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}