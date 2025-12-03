---
date: 2025-12-03
description: Naučte se, jak nastavit velikost stránky PDF při převodu DWG na PDF a
  povolit sledování v souborech DWG pomocí Aspose.CAD pro Javu – kompletní průvodce
  exportem CAD výkresu do PDF s přesností.
language: cs
linktitle: Set PDF Page Size and Enable Tracking in DWG Files Using Java
second_title: Aspose.CAD Java API
title: Nastavte velikost stránky PDF a povolte sledování v souborech DWG pomocí Aspose.CAD
  v Javě
url: /java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Nastavení velikosti PDF stránky a povolení sledování v DWG souborech pomocí Aspose.CAD v Javě

## Úvod

Pokud potřebujete **set PDF page size** při *convert DWG to PDF* a zároveň sledovat případné problémy s renderováním, Aspose.CAD for Java vám poskytuje čistý programový způsob, jak to provést. V tomto tutoriálu projdeme přesné kroky pro konfiguraci rozměrů stránky, povolení sledování a export CAD výkresu do PDF – vše z Javy. Na konci pochopíte, proč je nastavení správné velikosti stránky důležité pro CAD výkresy a jak zachytit podrobné informace o sledování během exportu.

## Rychlé odpovědi
- **Co ovlivňuje „set PDF page size“?** Definuje šířku a výšku výsledného PDF plátna, což zajišťuje, že se váš výkres perfektně vejde.  
- **Potřebuji licenci pro použití této funkce?** Zkušební verze funguje pro testování; pro produkci je vyžadována komerční licence.  
- **Jaká verze Aspose.CAD je požadována?** Jakákoli recentní verze, která podporuje `CadRasterizationOptions`.  
- **Mohu to použít s jinými CAD formáty?** Příklad ukazuje DWG/DXF, ale stejný přístup funguje pro většinu podporovaných formátů.  
- **Jak dlouho trvá konverze?** Obvykle méně než sekunda pro středně velké soubory; větší výkresy mohou trvat déle.

## Co znamená „set PDF page size“ v kontextu exportu CAD?
Nastavení velikosti PDF stránky říká rendereru přesné rozměry (v pixelech nebo bodech) výstupního plátna. To je zvláště důležité u technických výkresů, kde je nutné zachovat měřítko a rozvržení. Bez explicitního nastavení velikosti stránky může PDF výchozí velikost oříznout nebo deformovat výkres.

## Proč nastavit velikost PDF stránky při exportu CAD výkresů?
- **Zachovat měřítko** – Inženýři se spoléhají na výtisky v pravém měřítku.  
- **Přizpůsobit papíru** – Vyberte A4, Letter nebo vlastní velikost odpovídající specifikacím projektu.  
- **Zlepšit čitelnost** – Větší stránky mohou zobrazit jemné detaily bez přiblížení.  
- **Konzistentní výstup** – Automatizované pipeline vytvářejí PDF se stejnými rozměry při každém spuštění.

## Jak nastavit velikost PDF stránky při konverzi DWG do PDF?
Níže nakonfigurujeme `CadRasterizationOptions` s vlastními hodnotami šířky a výšky před exportem. Tento krok přímo řeší hlavní klíčové slovo **set PDF page size**.

## Požadavky

- **Java Development Kit (JDK)** – Java 8 nebo novější nainstalovaná na vašem počítači.  
- **Aspose.CAD for Java** – Stáhněte z oficiální [Aspose CAD download page](https://releases.aspose.com/cad/java/).  
- **Adresář dokumentů** – Složka obsahující DWG/DXF soubory, které chcete zpracovat.

## Import jmenných prostorů

Nejprve importujte třídy, které budete potřebovat. Kódový blok zůstává nezměněn oproti původnímu tutoriálu.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.CadRenderResult;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.RenderResult;
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
```

## Krok 1: Načtení souboru DWG/DXF

Načtěte svůj zdrojový výkres. Upravte cestu tak, aby ukazovala na váš vlastní soubor.

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## Krok 2: Konfigurace možností exportu PDF (včetně velikosti stránky)

Zde nastavujeme šířku a výšku stránky – toto je místo, kde **set PDF page size**. Hodnoty jsou v pixelech; můžete je převést z palců nebo milimetrů podle potřeby.

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);   // <-- custom width
cadRasterizationOptions.setPageHeight(600);  // <-- custom height
```

> **Tip:** Pokud upřednostňujete standardní formáty papíru, použijte převod `1 inch = 72 points`. Pro stránku A4 (8.27 × 11.69 in) nastavte `pageWidth = 595` a `pageHeight = 842`.

## Krok 3: Implementace sledování

Sledování zachytí jakékoli problémy s renderováním. Připojíme vlastní handler, který bude vyvolán po exportu.

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## Krok 4: Export do PDF

Nyní proveďte konverzi. PDF bude vytvořeno s rozměry, které jste zadali, a jakékoli informace o sledování budou vytištěny do konzole.

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## Krok 5: Třída CadRenderHandler

Handler vypisuje všechny selhání, ke kterým během renderování došlo. To vám pomůže ladit problémy při **exporting CAD drawing PDF**.

```java
public static class ErrorHandler extends CadRasterizationOptions.CadRenderHandler {
    @Override
    public void invoke(CadRenderResult result) {
        System.out.println("Tracking results of exporting");

        if (result.isRenderComplete())
            return;

        System.out.println("Have some problems:");

        int idxError = 1;
        for (RenderResult rr : result.getFailures()) {
            System.out.printf("{0}. {1}, {2}", idxError, rr.getRenderCode(), rr.getMessage());
            idxError++;
        }
    }
}
```

## Časté problémy a řešení

| Problém | Příčina | Řešení |
|-------|-------|-----|
| **Blank PDF** | Velikost stránky nastavená na 0 nebo příliš malá | Ověřte, že `setPageWidth` a `setPageHeight` mají kladné hodnoty. |
| **Missing geometry** | Chyby při renderování zachycené handlerem | Prohlédněte výstup v konzoli z `ErrorHandler` a řešte konkrétní `RenderCode`. |
| **File not found** | Nesprávná cesta `dataDir` | Použijte absolutní cestu nebo se ujistěte, že adresář existuje. |
| **License exception** | Použití zkušební verze bez platné licence pro velké soubory | Aplikujte svou Aspose.CAD licenci před načtením obrázku. |

## Často kladené otázky

**Q: Mohu povolit sledování pro jiné CAD formáty pomocí Aspose.CAD for Java?**  
A: Aspose.CAD primárně podporuje DWG/DXF pro sledování. Pro jiné formáty konzultujte oficiální dokumentaci.

**Q: Jak mohu zvládnout další možnosti exportu v Aspose.CAD for Java?**  
A: Knihovna nabízí mnoho možností, jako DPI, barvu pozadí a vektorové rasterizace. Viz [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/) pro podrobnosti.

**Q: Existuje zkušební verze pro Aspose.CAD for Java?**  
A: Ano, můžete si stáhnout bezplatnou zkušební verzi z [Aspose.CAD Free Trial](https://releases.aspose.com/).

**Q: Kde mohu získat pomoc nebo diskutovat o problémech souvisejících s Aspose.CAD for Java?**  
A: Navštivte [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) pro komunitní podporu a oficiální odpovědi.

**Q: Jak získám dočasnou licenci pro Aspose.CAD for Java?**  
A: Postupujte podle kroků uvedených na stránce [Temporary License](https://purchase.aspose.com/temporary-license/).

**Poslední aktualizace:** 2025-12-03  
**Testováno s:** Aspose.CAD for Java 24.11 (nejnovější v době psaní)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}