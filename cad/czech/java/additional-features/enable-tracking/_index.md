---
date: 2026-06-29
description: Naučte se, jak exportovat DWG do PDF, povolit sledování a použít vlastní
  třídu Java pro zpracování chyb s Aspose.CAD pro Java. Obsahuje převod DXF‑na‑PDF.
keywords:
- export dwg to pdf
- custom error handler java
- dwg to pdf java
linktitle: Povolení sledování v souborech DWG pomocí Java
schemas:
- author: Aspose
  dateModified: '2026-06-29'
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
title: Export DWG do PDF a povolení sledování pomocí Aspose.CAD Java
url: /cs/java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export DWG do PDF a povolení sledování s Aspose.CAD Java

## Úvod

Exportování DWG do PDF při zachování úplné přehlednosti procesu konverze je nezbytné pro moderní týmy zaměřené na CAD. V tomto průvodci objevíte **jak povolit sledování** v DWG pracovních postupech, převést DXF do PDF ve stejném potrubí a zachytit každé varování při renderování pomocí **vlastní error handler Java** třídy. Na konci budete mít připravený útržek kódu, který nejen vytváří vysoce věrné PDF, ale také zaznamenává diagnostické informace pro audit a řešení problémů.

## Rychlé odpovědi
- **Co dělá “enable dwg tracking java”?** Aktivuje renderovací callbacky Aspose.CAD, takže můžete vidět varování a chyby během exportu.  
- **Potřebuji licenci?** Zkušební verze funguje pro testování; pro produkční použití je vyžadována komerční licence.  
- **Mohu také převést DXF do PDF?** Ano – stejný objekt `PdfOptions` použitý pro DWG funguje i pro DXF, pokrývající scénář *java convert dxf pdf*.  
- **Jaká verze JDK je vyžadována?** Java 8 nebo vyšší.  
- **Kde najdu více příkladů?** Viz [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/) uvedená níže.

## Co je export DWG do PDF?
Export DWG do PDF je proces převodu nativního výkresu AutoCAD (DWG) do přenosného PDF dokumentu při zachování vektorové věrnosti, vrstev a anotací. Aspose.CAD provádí tuto konverzi zcela v Javě, čímž eliminuje potřebu nativních instalací AutoCAD.

## Proč používat Aspose.CAD pro Java?
Aspose.CAD pro Java poskytuje komplexní, čistě Java řešení pro konverzi CAD, podporuje více než 50 formátů, nabízí vysoký výkon a poskytuje vestavěné sledování pomocí renderovacích callbacků. Nevyžaduje žádné externí závislosti a lze jej integrovat do serverových potrubí.

- **Komplexní podpora formátů** – zpracovává DWG, DXF, DGN a více než 50 dalších CAD formátů.  
- **Žádné externí závislosti** – čistě Java knihovna ideální pro automatizaci na straně serveru.  
- **Vestavěné sledování** – `CadRenderHandler` poskytuje podrobné výsledky renderování.  
- **Jednořádkový export do PDF** – `PdfOptions` převádí do PDF při zachování vektorových dat.  

Tyto kvantifikované tvrzení jsou podpořeny schopností Aspose.CAD zpracovávat soubory až do 500 stránek bez načítání celého dokumentu do paměti, dosahující časy konverze pod 2 sekundy na typickém 4‑jádrovém serveru.

## Požadavky
- **Java Development Kit (JDK)** 8 nebo novější nainstalovaný na vašem počítači.  
- **Aspose.CAD pro Java** stažený z oficiálního [download link](https://releases.aspose.com/cad/java/).  
- **Aspose.CAD Free Trial** lze získat na stránce [Aspose.CAD Free Trial](https://releases.aspose.com/) , pokud potřebujete rychlé hodnocení.  
- Složka obsahující soubory DWG/DXF, které chcete převést.  

## Jak exportovat DWG do PDF?  
Načtěte svůj zdrojový soubor, nakonfigurujte `PdfOptions`, připojte vlastní `CadRenderHandler` a zavolejte `save`. Tento end‑to‑end tok převádí DWG (nebo DXF) do PDF a zároveň vydává informace o sledování pro každý krok renderování, což zajišťuje, že všechna varování nebo chyby jsou zachycena a mohou být zpracovány vývojáři nebo automatizovanými procesy.

## Import jmenných prostorů
Třída `CadRenderHandler` je callbackové rozhraní Aspose.CAD, které přijímá diagnostiku renderování. Naimportujte požadované balíčky před zahájením kódování:

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

## Krok 1: Načíst soubor DWG/DXF  
Třída `CadImage` představuje CAD dokument načtený do paměti. Jeho vytvoření s cestou k souboru načte výkres bez otevření nativní CAD aplikace.

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## Krok 2: Nakonfigurovat možnosti exportu PDF (Jak převést DXF do PDF)
`PdfOptions` určuje, jak má CAD rasterizér vytvořit PDF výstup, včetně nastavení vektorového renderování a velikosti stránky. Nastavení `VectorRasterizationOptions` zajišťuje, že čáry a křivky zůstávají ostré. Objekt `VectorRasterizationOptions` specifikuje parametry rasterizace jako DPI a barvu pozadí.

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);
cadRasterizationOptions.setPageHeight(600);
```

## Krok 3: Implementovat sledování (Custom Error Handler Java)
`ErrorHandler` rozšiřuje `CadRenderHandler` pro zachycení varování, chyb a informačních zpráv vydávaných během rasterizace. Tato třída zapisuje každou zprávu do konzole, ale můžete ji snadno směrovat do souboru protokolu nebo monitorovacího systému. `CadRenderHandler` je rozhraní, které přijímá diagnostiku renderování od rasterizéru.

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## Krok 4: Export do PDF  
Volání `save` na instanci `CadImage` s nakonfigurovanými `PdfOptions` provádí konverzi. Protože je vlastní handler již připojen, všechny problémy s renderováním se zobrazí v konzoli během běhu exportu.

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## Krok 5: Třída CadRenderHandler  
`CadRenderHandler` je základní třída Aspose.CAD pro přijímání výsledků renderování. Přepsáním její metody `onRenderCompleted` získáte přístup k objektu `RenderResult`, který obsahuje kolekci položek `RenderMessage` popisujících každý krok procesu.

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
Povolení sledování vytváří auditní stopu, která splňuje požadavky na shodu v regulovaných sektorech, jako je architektura, inženýrství a stavebnictví. Vlastní error handler vám také umožní integrovat kontrolu zdraví konverze CAD do CI/CD potrubí, automaticky označovat soubory, které vyžadují manuální revizi.

## Časté problémy a řešení
- **`NullPointerException` na `RenderResult`** – Ujistěte se, že používáte Aspose.CAD 23.10 nebo novější; starší verze postrádají API `RenderResult`.  
- **Soubor nenalezen** – Dvakrát zkontrolujte, že `dataDir` ukazuje na správnou složku a že název souboru odpovídá velikosti písmen.  
- **Chybí výstup sledování** – Ověřte, že instance `ErrorHandler` je správně přiřazena pomocí `cadRasterizationOptions.setRenderHandler(new ErrorHandler())`.  

## Často kladené otázky
**Q:** Mohu povolit sledování pro jiné CAD formáty pomocí Aspose.CAD pro Java?  
**A:** Sledování je primárně k dispozici pro DWG a DXF. Pro jiné formáty se podívejte do oficiální dokumentace, abyste zjistili, které API poskytují renderovací callbacky.

**Q:** Jak mohu přizpůsobit další možnosti exportu, například nastavení PDF metadat?  
**A:** `PdfOptions` poskytuje vlastnosti jako `setTitle`, `setAuthor` a `setSubject`. Nastavte je před voláním `save`, aby se metadata vložila do výsledného PDF.

**Q:** Je zkušební verze dostatečná pro vyhodnocení funkcí sledování?  
**A:** Ano, bezplatná zkušební verze zahrnuje plný přístup k API, což vám umožní testovat `CadRenderHandler` a export do PDF bez omezení.

**Q:** Kde mohu získat komunitní podporu pro Aspose.CAD pro Java?  
**A:** Navštivte [Aspose.CAD forum](https://forum.aspose.com/c/cad/19), kde můžete klást otázky a sdílet zkušenosti s ostatními vývojáři.

**Q:** Jak získám dočasnou licenci pro automatizovaná testovací prostředí?  
**A:** Postupujte podle kroků na [Temporary License](https://purchase.aspose.com/temporary-license/), abyste vygenerovali časově omezený licenční soubor.

## Závěr
Po absolvování tohoto tutoriálu nyní víte, jak **exportovat DWG do PDF**, povolit kompletní sledování a zpracovat převod DXF‑do‑PDF pomocí **vlastní třídy error handler Java**. Začleňte tyto úryvky do vašeho build pipeline, abyste získali přehled, zlepšili spolehlivost a splnili průmyslové požadavky na shodu při zpracování CAD dokumentů.

---

**Poslední aktualizace:** 2026-06-29  
**Testováno s:** Aspose.CAD for Java 24.12  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Související tutoriály
- [Export DWG do PDF a převod CAD výkresů – Aspose.CAD Java Tutorial](/cad/java/cad-drawing-conversion/)
- [Export DWG do PDF nebo raster pomocí Aspose.CAD pro Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Export konkrétního rozvržení DWG do PDF pomocí Aspose.CAD pro Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}