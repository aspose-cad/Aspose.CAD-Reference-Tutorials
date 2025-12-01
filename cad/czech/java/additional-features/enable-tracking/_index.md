---
date: 2025-12-01
description: Naučte se, jak nastavit velikost stránky PDF, převést DWG na PDF a povolit
  sledování změn DWG pomocí Aspose.CAD pro Javu.
language: cs
linktitle: Set PDF Page Size and Track DWG with Java
second_title: Aspose.CAD Java API
title: Nastavte velikost stránky PDF a sledujte DWG pomocí Aspose.CAD Java
url: /java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Nastavení velikosti PDF stránky a sledování DWG pomocí Aspose.CAD Java

## Úvod

Při spolupráci na CAD projektech často potřebujete **nastavit velikost PDF stránky** pro jednotné rozvržení, **převést DWG na PDF** a sledovat každou změnu provedenou v výkresu. Aspose.CAD pro Java umožňuje vše toto v jednom, zjednodušeném pracovním postupu. V tomto tutoriálu projdeme konkrétní kroky k **nastavení velikosti PDF stránky**, povolení **sledování změn DWG** a exportu výkresu jako PDF – vše pomocí Javy.

## Rychlé odpovědi
- **Jak nastavit velikost PDF stránky?** Použijte `CadRasterizationOptions.setPageWidth()` a `setPageHeight()` před exportem.  
- **Mohu sledovat změny během exportu?** Ano – implementujte vlastní `CadRenderHandler` pro zachycení výsledků sledování.  
- **Která metoda převádí DWG na PDF?** Zavolejte `image.save(stream, pdfOptions)` po nastavení možností.  
- **Jaké jsou hlavní předpoklady?** JDK, Aspose.CAD pro Java a složka s DWG/DXF soubory.  
- **Je licence vyžadována pro produkci?** Ano, pro nasazení mimo zkušební režim je potřeba platná licence Aspose.CAD.

## Co znamená „nastavit velikost PDF stránky“ v kontextu exportu DWG?

Nastavení velikosti PDF stránky určuje rozměry výsledného PDF plátna (šířka × výška v pixelech). To je nezbytné, když chcete, aby exportovaný výkres odpovídal konkrétní velikosti papíru nebo rozvržení obrazovky, a zajistit, že všechny prvky se zobrazí přesně tam, kde očekáváte.

## Proč povolit sledování při exportu DWG souborů?

Sledování (nebo change‑tracking) zaznamenává jakékoli problémy při renderování, chybějící fonty nebo nepodporované entity, které se objeví během konverze. Zachycen těchto informací můžete:

- Rychle identifikovat problémy, které je potřeba opravit před finálním dodáním.  
- Poskytnout jasnou zpětnou vazbu členům týmu o tom, co bylo změněno nebo vynecháno.  
- Udržet auditní stopu pro odvětví s přísnými požadavky na shodu.

## Předpoklady

- **Java Development Kit (JDK)** – libovolná aktuální verze (8+).  
- **Aspose.CAD pro Java** – stáhněte z oficiální [Aspose CAD download page](https://releases.aspose.com/cad/java/).  
- **Adresář dokumentů** – složka obsahující DWG/DXF soubory, které chcete zpracovat.

## Import Namespaces

Začněte importováním potřebných tříd Aspose.CAD a standardních Java I/O tříd.

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

## Krok 1: Načtení DWG (nebo DXF) souboru

Načtěte svůj výchozí výkres do objektu `Image`. Upravit cestu tak, aby ukazovala na váš vlastní adresář.

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## Krok 2: Konfigurace možností exportu do PDF (včetně velikosti stránky)

Zde nastavíme PDF možnosti a explicitně **nastavíme velikost PDF stránky** na 800 × 600 pixelů. Toto je místo, kde se použije primární klíčové slovo.

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);   // set PDF page width
cadRasterizationOptions.setPageHeight(600);  // set PDF page height
```

## Krok 3: Implementace sledování

Vytvořte vlastní handler chyb, který během konverze získá informace o sledování.

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## Krok 4: Export do PDF

S nastavenými možnostmi a sledovacím handlerem exportujte výkres. Tento krok **převádí DWG na PDF** (nebo DXF na PDF v našem příkladu).

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## Krok 5: Třída CadRenderHandler – zachycení výsledků sledování

Třída `ErrorHandler` rozšiřuje `CadRenderHandler` a vypisuje jakékoli problémy při renderování, které nastaly během **sledování změn DWG** souborů.

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

## Časté problémy a jejich řešení

| Problém | Proč se vyskytuje | Oprava |
|-------|----------------|-----|
| **Chybějící fonty** | CAD soubor odkazuje na fonty, které nejsou nainstalovány na serveru. | Nainstalujte požadované fonty nebo je vložte do zdrojového výkresu. |
| **Nepodporované entity** | Některé DWG entity zatím nejsou podporovány Aspose.CAD. | Pomocí výstupu sledování je identifikujte a zjednodušte výkres. |
| **Nesprávná velikost stránky** | `setPageWidth/Height` nebylo zavoláno před exportem. | Ujistěte se, že velikost stránky je nastavena v `CadRasterizationOptions` podle výše uvedeného příkladu. |

## Často kladené otázky

### Q1: Mohu povolit sledování i pro jiné CAD formáty pomocí Aspose.CAD pro Java?

A1: Aspose.CAD primárně podporuje sledování pro DWG/DXF soubory. Pro jiné formáty si prosím prostudujte oficiální dokumentaci, abyste zjistili, jaké funkce jsou k dispozici.

### Q2: Jak mohu zvládnout další možnosti exportu v Aspose.CAD pro Java?

A2: Knihovna nabízí mnoho možností, jako DPI, barvu pozadí a vektorové rasterizace. Prozkoumejte je v [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/).

### Q3: Existuje zkušební verze Aspose.CAD pro Java?

A3: Ano, můžete si stáhnout bezplatnou zkušební verzi z [Aspose.CAD Free Trial](https://releases.aspose.com/).

### Q4: Kde mohu získat pomoc nebo diskutovat o problémech souvisejících s Aspose.CAD pro Java?

A4: Komunitní fórum na [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) je skvělým místem pro kladení otázek a sdílení zkušeností.

### Q5: Jak získat dočasnou licenci pro Aspose.CAD pro Java?

A5: Postupujte podle kroků popsaných na stránce [Temporary License](https://purchase.aspose.com/temporary-license/), kde můžete požádat o časově omezenou licenci pro evaluaci.

### Q6: Mohu **převést DWG na PDF** při zachování vrstev?

A6: Ano. Konfigurací `CadRasterizationOptions` můžete zachovat informace o vrstvách v výsledném PDF.

### Q7: Jaký je nejlepší způsob, jak **exportovat DWG jako PDF** s vlastními rozměry stránky?

A7: Nastavte požadovanou šířku a výšku pomocí `setPageWidth` a `setPageHeight` před voláním `image.save()` – přesně tak, jak je demonstrováno ve Krok 2.

## Závěr

Dodržením výše uvedených kroků můžete **nastavit velikost PDF stránky**, **převést DWG na PDF** a **sledovat změny v DWG souborech** pomocí Aspose.CAD pro Java. Tento pracovní postup vám poskytuje plnou kontrolu nad výstupním rozvržením a zároveň cennou diagnostiku, která udržuje vaši CAD spolupráci plynulou a bez chyb. Neváhejte prozkoumat další možnosti renderování a integrovat tento kód do větších automatizačních pipeline.

---

**Poslední aktualizace:** 2025-12-01  
**Testováno s:** Aspose.CAD pro Java 24.12 (nejnovější v době psaní)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}