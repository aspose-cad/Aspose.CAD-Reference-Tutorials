---
date: 2026-06-14
description: Naučte se, jak exportovat CAD do PDF a převést DGN na PDF pomocí Aspose.CAD
  pro Java. Podrobný návod krok za krokem pro vývojáře Java.
keywords:
- export cad to pdf
- convert dwg to pdf
- convert dgn to pdf
- java convert cad pdf
- batch convert dgn pdf
linktitle: Export vloženého DGN
schemas:
- author: Aspose
  dateModified: '2026-06-14'
  description: Learn how to export CAD to PDF and convert DGN to PDF using Aspose.CAD
    for Java. Step‑by‑step guide for Java developers.
  headline: Export CAD to PDF – Export Embedded DGN with Aspose.CAD for Java
  type: TechArticle
- description: Learn how to export CAD to PDF and convert DGN to PDF using Aspose.CAD
    for Java. Step‑by‑step guide for Java developers.
  name: Export CAD to PDF – Export Embedded DGN with Aspose.CAD for Java
  steps:
  - name: Set Up Input and Output Paths
    text: Define the directory that contains your source file and specify the DWG
      that holds the embedded DGN.
  - name: Load DWG File
    text: '`Image` loads the DWG and automatically detects any embedded DGN data,
      exposing it for further processing.'
  - name: Configure Rasterization Options
    text: Select which layout(s) you want to include in the PDF. In this example we
      export only the **Model** layout, which is the most common view for engineering
      drawings.
  - name: Configure PDF Options
    text: Attach the rasterization settings to the PDF export options so that the
      final document respects the chosen layout and DPI.
  - name: Save PDF File
    text: Finally, write the PDF to disk using the configured options. The `save`
      method writes the configured image to the target file format on disk.
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD for Java is a commercial library. You can obtain a license
      from [here](https://purchase.aspose.com/buy).
    question: Can I use Aspose.CAD for Java in a commercial project?
  - answer: Yes, you can access a free trial of Aspose.CAD for Java [here](https://releases.aspose.com/).
    question: Is there a free trial available?
  - answer: You can seek support from the Aspose.CAD community on the [forum](https://forum.aspose.com/c/cad/19).
    question: How can I get support for Aspose.CAD for Java?
  - answer: You can obtain a temporary license [here](https://purchase.aspose.com/temporary-license/).
    question: What if I need a temporary license?
  - answer: The documentation is available [here](https://reference.aspose.com/cad/java/).
    question: Where can I find the official documentation?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Export CAD do PDF – Export vloženého DGN pomocí Aspose.CAD pro Java
url: /cs/java/dgn-export-options/export-embedded-dgn/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export CAD do PDF – Export vloženého DGN pomocí Aspose.CAD pro Java

## Úvod

V tomto tutoriálu objevíte **jak exportovat CAD do PDF** převodem vloženého souboru DGN na vysoce‑kvalitní PDF dokument pomocí Aspose.CAD pro Java. Aspose.CAD je robustní knihovna, která poskytuje vývojářům Java plnou kontrolu nad manipulací CAD souborů, ať už potřebujete **převést DGN do PDF**, **převést DWG do PDF**, nebo jen vykreslit CAD výkresy v jiných formátech. Postupujte podle níže uvedeného krok‑za‑krokem průvodce a během několika minut budete schopni tuto funkci integrovat do svých aplikací.

## Rychlé odpovědi
- **Co znamená „export CAD do PDF“?** Převádí CAD výkresy (DWG, DGN atd.) do PDF souborů při zachování vektorové kvality.  
- **Která knihovna se používá?** Aspose.CAD pro Java.  
- **Potřebuji licenci?** Licence je vyžadována pro produkční nasazení; je k dispozici bezplatná zkušební verze.  
- **Jaké jsou hlavní předpoklady?** Vývojové prostředí Java a JAR Aspose.CAD pro Java.  
- **Mohu přizpůsobit výstup?** Ano – můžete vybrat rozvržení, nastavit možnosti rasterizace a ovládat nastavení PDF.

## Co je „export CAD do PDF“?

Export CAD do PDF převádí nativní CAD výkres (DWG, DGN atd.) do PDF souboru, který zachovává původní vektorovou geometrii, vrstvy a rozvržení, což umožňuje komukoli prohlížet, tisknout nebo sdílet návrh bez CAD softwaru. Tato transformace vytváří platformně nezávislý dokument, který vypadá identicky při jakémkoli zvětšení, což je ideální pro spolupráci i archivaci.

## Proč použít Aspose.CAD pro Java k převodu DGN do PDF?

Aspose.CAD pro Java poskytuje čistě Java řešení, které eliminuje potřebu externích CAD nástrojů, zajišťuje přesnou vektorovou věrnost ve výsledných PDF a nabízí rozsáhlé konfigurační možnosti, jako je výběr rozvržení, řízení DPI a vkládání fontů, což je ideální jak pro jednoduché, tak pro podnikové úlohy převodu.

- **Žádné externí závislosti** – funguje čistě v Javě na jakémkoli OS.  
- **Zachovává vektorová data** – PDF zůstávají ostré při jakémkoli zvětšení.  
- **Detailní kontrola** – vyberte konkrétní rozvržení, nastavte DPI rasterizace a vložte fonty.  
- **Podnikové nasazení** – podporuje soubory až do **2 GB**, hromadné zpracování tisíců výkresů a flexibilní licencování.  

## Předpoklady

Než začneme, ujistěte se, že máte následující:

- **Vývojové prostředí Java** – nainstalovaný a nakonfigurovaný JDK 8 nebo vyšší.  
- **Aspose.CAD pro Java** – stáhněte nejnovější JAR z [zde](https://releases.aspose.com/cad/java/).  

## Import balíčků

`import` příkazy přinášejí požadované třídy Aspose.CAD do rozsahu.  
`Image` je základní třída, která představuje jakýkoli rasterizovatelný CAD soubor, zatímco `PdfOptions` a `RasterizationOptions` vám umožňují jemně doladit výstup PDF.  
`CadRasterizationOptions` určuje parametry rasterizace, jako jsou DPI, velikost stránky a rozvržení pro vykreslování CAD.

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Jak exportovat CAD do PDF pomocí Aspose.CAD pro Java?

Proces začíná načtením souboru DWG, který obsahuje vložený DGN, následným nastavením parametrů rasterizace pro definování výstupního rozlišení a rozvržení, přiřazením těchto parametrů k objektu PdfOptions a nakonec voláním metody `save` pro vytvoření PDF. Tento přístup zajišťuje vysoce kvalitní výsledky zachovávající vektory s minimálním množstvím kódu.

Níže je přehledný číslovaný průvodce, který přesně ukazuje, jak převést vložený soubor DGN (uložený uvnitř DWG) do PDF.

### Krok 1: Nastavte vstupní a výstupní cesty

Definujte adresář, který obsahuje váš zdrojový soubor, a uveďte DWG, který obsahuje vložený DGN.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
```

### Krok 2: Načtěte soubor DWG

`Image` načte DWG a automaticky detekuje jakákoli vložená data DGN, která zpřístupní pro další zpracování.

```java
Image objImage = Image.load(fileName);
```

### Krok 3: Nakonfigurujte možnosti rasterizace

Vyberte, které rozvržení (rozvržení) chcete zahrnout do PDF. V tomto příkladu exportujeme pouze rozvržení **Model**, které je nejčastěji používaným pohledem pro technické výkresy.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setLayouts(new String[] {"Model"});
```

### Krok 4: Nakonfigurujte PDF možnosti

Přiřaďte nastavení rasterizace k možnostem exportu PDF, aby finální dokument respektoval vybrané rozvržení a DPI.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Krok 5: Uložte PDF soubor

Nakonec zapište PDF na disk pomocí nakonfigurovaných možností. Metoda `save` zapíše nakonfigurovaný obrázek do cílového formátu souboru na disku.

```java
objImage.save(dataDir + "BlockRefDgn.pdf", pdfOptions);
```

## Převod DWG do PDF – doplňková rada

Pokud je váš zdrojový soubor obyčejný DWG (bez vloženého DGN), můžete znovu použít stejný kód – jednoduše změňte `fileName`, aby ukazoval na DWG, který chcete převést. Možnosti rasterizace a PDF zůstávají stejné, což vám poskytuje konzistentní workflow **convert DWG to PDF**.

## Časté problémy a řešení

| Problém | Důvod | Řešení |
|-------|--------|----------|
| **Prázdný výstup PDF** | Nesoulad názvu rozvržení | Ověřte, že název rozvržení předaný do `setLayouts` přesně odpovídá rozvržení ve zdrojovém souboru (rozlišuje velká a malá písmena). |
| **Výjimka licence** | Použití zkušební verze bez licence | Aplikujte platnou licenci Aspose.CAD před načtením obrázku (`License license = new License(); license.setLicense("Aspose.CAD.lic");`). |
| **Soubor nenalezen** | Nesprávná cesta `dataDir` | Použijte absolutní cestu nebo zajistěte, aby relativní cesta byla správná vzhledem k pracovnímu adresáři projektu. |
| **Grafika s nízkým rozlišením** | Výchozí DPI rasterizace je nízké | Nastavte `rasterizationOptions.setResolution(300)` nebo upravte `setPageWidth/Height` pro zvýšení DPI. |

## Často kladené otázky

**Q:** **Mohu použít Aspose.CAD pro Java v komerčním projektu?**  
**A:** **Ano, Aspose.CAD pro Java je komerční knihovna. Licenci můžete získat [zde](https://purchase.aspose.com/buy).**

**Q:** **Je k dispozici bezplatná zkušební verze?**  
**A:** **Ano, můžete získat bezplatnou zkušební verzi Aspose.CAD pro Java [zde](https://releases.aspose.com/).**

**Q:** **Jak mohu získat podporu pro Aspose.CAD pro Java?**  
**A:** **Podporu můžete získat od komunity Aspose.CAD na [fóru](https://forum.aspose.com/c/cad/19).**

**Q:** **Co když potřebuji dočasnou licenci?**  
**A:** **Dočasnou licenci můžete získat [zde](https://purchase.aspose.com/temporary-license/).**

**Q:** **Kde najdu oficiální dokumentaci?**  
**A:** **Dokumentace je k dispozici [zde](https://reference.aspose.com/cad/java/).**

## Závěr

Nyní jste se naučili, jak **exportovat CAD do PDF**, konkrétně jak **převést DGN do PDF** a dokonce **převést DWG do PDF** pomocí Aspose.CAD pro Java. Dodržením výše uvedených kroků můžete integrovat bezproblémový převod CAD‑na‑PDF do jakéhokoli řešení založeného na Javě a poskytovat uživatelům vysoce kvalitní PDF bez potřeby dalšího CAD softwaru.

---

**Poslední aktualizace:** 2026-06-14  
**Testováno s:** Aspose.CAD pro Java 24.12  
**Autor:** Aspose

{{< blocks/products/products-backtop-button >}}

## Související tutoriály

- [Export DGN do DWG pomocí Aspose.CAD pro Java – Tutoriál](/cad/java/dgn-export-options/)
- [Jednoduchý export DGN do AutoCAD PDF pomocí Aspose.CAD pro Java](/cad/java/dgn-export-options/exporting-dgn-to-pdf/)
- [dwg do pdf java – Export CAD do PDF pomocí Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}