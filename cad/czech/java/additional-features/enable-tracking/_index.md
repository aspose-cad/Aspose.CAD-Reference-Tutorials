---
date: 2026-11-18
description: Naučte se, jak exportovat DWG do PDF, povolit sledování a použít vlastní
  třídu Java pro zpracování chyb s Aspose.CAD pro Java. Zahrnuje převod DXF na PDF.
keywords:
- export dwg to pdf
- custom error handler java
- dwg to pdf java
lastmod: 2026-11-18
linktitle: Povolit sledování v souborech DWG pomocí Java
og_description: Exportujte DWG do PDF a povolte úplné sledování v Java s Aspose.CAD.
  Naučte se používat vlastní zpracovatel chyb, převádět DXF do PDF a zaznamenávat
  varování při vykreslování.
og_image_alt: Guide showing DWG to PDF conversion and tracking in Java with Aspose.CAD
og_title: Export DWG do PDF se sledováním pomocí Aspose.CAD pro Java
schemas:
- author: Aspose
  dateModified: '2026-11-18'
  description: Learn how to export DWG to PDF, enable tracking, and use a custom error
    handler Java class with Aspose.CAD for Java. Includes DXF‑to‑PDF conversion.
  headline: Export DWG to PDF and Enable Tracking with Aspose.CAD Java
  type: TechArticle
- questions:
  - answer: It activates Aspose.CAD’s render callbacks so you can see warnings and
      errors during export.
    question: What does “enable dwg tracking java” do?
  - answer: A trial works for testing; a commercial license is required for production
      use.
    question: Do I need a license?
  - answer: Yes – the same `PdfOptions` object used for DWG works for DXF, covering
      the *java convert dxf pdf* scenario.
    question: Can I also convert DXF to PDF?
  - answer: Java 8 or higher.
    question: Which JDK version is required?
  - answer: See the [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/)
      linked below.
    question: Where can I find more examples?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- export dwg to pdf
- aspose.cad java
- custom error handler
- dxf to pdf
- java cad conversion
title: Export DWG do PDF a povolit sledování pomocí Aspose.CAD Java
url: /cs/java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export DWG do PDF a povolení sledování pomocí Aspose.CAD Java

## Úvod

Export DWG do PDF při zachování úplné přehlednosti o průběhu konverze je nezbytný pro moderní týmy zaměřené na CAD. V tomto průvodci se dozvíte **jak povolit sledování** v DWG pracovních postupech, převést DXF do PDF ve stejném potrubí a zachytit každé varování při vykreslování pomocí **vlastní třídy Java pro zpracování chyb**. Na konci budete mít připravený kód, který nejen vytváří vysoce věrné PDF, ale také zaznamenává diagnostické informace pro audit a řešení problémů.

## Rychlé odpovědi
- **Co dělá „enable dwg tracking java“?** Aktivuje renderovací zpětné volání Aspose.CAD, takže můžete během exportu vidět varování a chyby.  
- **Potřebuji licenci?** Zkušební verze funguje pro testování; pro produkční použití je vyžadována komerční licence.  
- **Mohu také převést DXF do PDF?** Ano – stejný objekt `PdfOptions` používaný pro DWG funguje i pro DXF, pokrývající scénář *java convert dxf pdf*.  
- **Jaká verze JDK je požadována?** Java 8 nebo vyšší.  
- **Kde najdu další příklady?** Viz [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/) uvedená níže.

## Co je export DWG do PDF?

Export DWG do PDF je proces převodu nativního výkresu AutoCAD (DWG) do přenositelného PDF dokumentu při zachování vektorové věrnosti, vrstev a anotací. **Aspose.CAD převádí DWG do PDF čistě v Javě, takže nikdy nepotřebujete licencovanou instalaci AutoCADu.** Tato konverze zachovává přesné tloušťky čar, styly textu a geometrii rozvržení, což činí PDF vhodným pro revizi klientem, archivaci nebo následné zpracování.

## Proč používat Aspose.CAD pro Java?

Aspose.CAD pro Java poskytuje komplexní řešení čistě v Javě pro konverzi CAD, podporuje více než 50 formátů, nabízí vysoký výkon a poskytuje vestavěné sledování pomocí renderovacích zpětných volání. Nevyžaduje žádné externí závislosti a lze jej integrovat do serverových potrubí. Knihovna také zahrnuje paměťově úsporné zpracování, umožňující konverzi souborů až do 500 stránek bez načítání celého dokumentu do RAM.

## Požadavky

- **Java Development Kit (JDK)** 8 nebo novější nainstalovaný na vašem počítači.  
- **Aspose.CAD pro Java** stažený z oficiálního [download link](https://releases.aspose.com/cad/java/).  
- **Aspose.CAD Free Trial** lze získat na stránce [Aspose.CAD Free Trial](https://releases.aspose.com/) , pokud potřebujete rychlé vyhodnocení.  
- Složka obsahující soubory DWG/DXF, které chcete převést.  

## Jak exportovat DWG do PDF?

Načtěte svůj zdrojový soubor, nakonfigurujte `PdfOptions`, připojte vlastní `CadRenderHandler` a zavolejte `save`. Tento end‑to‑end tok převádí DWG (nebo DXF) do PDF a zároveň vydává sledovací informace pro každý krok vykreslování, což zajišťuje, že všechna varování nebo chyby jsou zachyceny a mohou být zpracovány vývojáři nebo automatizovanými procesy.

## Importovat jmenné prostory

`CadRenderHandler` rozhraní přijímá diagnostiku vykreslování, jako jsou varování a chyby během konverze.  
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

## Krok 1: načíst soubor dwg/dxf  

`CadImage` představuje CAD výkres načtený do paměti a poskytuje přístup k jeho stránkám a vrstvám.  
```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## Krok 2: nakonfigurovat možnosti exportu PDF (jak převést dxf do pdf)

`PdfOptions` definuje nastavení výstupu PDF, zatímco `VectorRasterizationOptions` řídí parametry rasterizace, jako jsou DPI a barva pozadí.  
```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);
cadRasterizationOptions.setPageHeight(600);
```

## Krok 3: implementovat sledování (vlastní error handler java)

`ErrorHandler` rozšiřuje `CadRenderHandler` pro zachycení a zaznamenání zpráv o vykreslování, které jsou během konverzního procesu vyvolány.  
```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## Krok 4: export do PDF  

Volání metody `save` na instanci `CadImage` zapíše vykreslené PDF do zadané výstupní cesty.  
```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## Krok 5: třída CadRenderHandler  

`CadRenderHandler` je základní třída zpětného volání, která přijímá `RenderResult` obsahující podrobné zprávy po dokončení vykreslování.  
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

## Proč je to důležité

Povolení sledování vytváří auditní stopu, která splňuje požadavky na shodu v regulovaných odvětvích, jako jsou architektura, inženýrství a stavebnictví. Vlastní error handler vám také umožní integrovat kontrolu zdraví konverze CAD do CI/CD pipeline, automaticky označovat soubory, které vyžadují ruční revizi.

## Časté problémy a řešení

- **`NullPointerException` na `RenderResult`** – Ujistěte se, že používáte Aspose.CAD 23.10 nebo novější; starší verze neobsahují API `RenderResult`.  
- **Soubor nenalezen** – Zkontrolujte, že `dataDir` ukazuje na správnou složku a že název souboru odpovídá velikosti písmen.  
- **Chybí výstup sledování** – Ověřte, že instance `ErrorHandler` je správně přiřazena pomocí `cadRasterizationOptions.setRenderHandler(new ErrorHandler())`.  

## Často kladené otázky

**Q:** Mohu povolit sledování pro jiné CAD formáty pomocí Aspose.CAD pro Java?  
**A:** Sledování je primárně k dispozici pro DWG a DXF. Pro jiné formáty se podívejte do oficiální dokumentace, která ukazuje, které API poskytují renderovací zpětná volání.

**Q:** Jak mohu přizpůsobit další možnosti exportu, například nastavení PDF metadat?  
**A:** `PdfOptions` poskytuje vlastnosti jako `setTitle`, `setAuthor` a `setSubject`. Nastavte je před voláním `save`, aby se metadata vložila do výsledného PDF.

**Q:** Je zkušební verze dostačující pro vyhodnocení funkcí sledování?  
**A:** Ano, bezplatná zkušební verze zahrnuje plný přístup k API, což vám umožní testovat `CadRenderHandler` a export PDF bez omezení.

**Q:** Kde mohu získat komunitní podporu pro Aspose.CAD pro Java?  
**A:** Navštivte [Aspose.CAD forum](https://forum.aspose.com/c/cad/19), kde můžete klást otázky a sdílet zkušenosti s ostatními vývojáři.

**Q:** Jak získám dočasnou licenci pro automatizovaná testovací prostředí?  
**A:** Postupujte podle kroků na [Temporary License](https://purchase.aspose.com/temporary-license/), abyste vygenerovali časově omezený licenční soubor.

## Závěr

Po absolvování tohoto tutoriálu nyní víte, jak **exportovat DWG do PDF**, povolit end‑to‑end sledování a zpracovat převod DXF‑to‑PDF pomocí **vlastní třídy Java pro zpracování chyb**. Začleňte tyto úryvky do vašeho build pipeline, abyste získali přehled, zvýšili spolehlivost a splnili průmyslové požadavky na shodu při zpracování CAD dokumentů.

---

**Last Updated:** 2026-11-18  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

## Související tutoriály

- [Export DWG do PDF a převod CAD výkresů – Aspose.CAD Java tutoriál](/cad/java/cad-drawing-conversion/)
- [Export DWG do PDF nebo rastrování pomocí Aspose.CAD pro Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Export konkrétního rozvržení DWG do PDF pomocí Aspose.CAD pro Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}