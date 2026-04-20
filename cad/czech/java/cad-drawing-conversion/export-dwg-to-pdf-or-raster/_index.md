---
date: 2026-02-17
description: Naučte se, jak knihovna Aspose.CAD pro Javu může rychle a přesně exportovat
  DWG do PDF nebo rastrových obrázků.
linktitle: Export DWG to PDF or Raster
second_title: Aspose.CAD Java API
title: Export DWG do PDF nebo rastrového formátu pomocí Java CAD knihovny Aspose.CAD
  pro Java
url: /cs/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export DWG do PDF nebo rastrových formátů pomocí java cad knihovny Aspose.CAD pro Java

## Introduction

V dynamickém světě počítačově‑asistovaného návrhu (CAD) je efektivní práce s výkresy zásadní. S **java cad library** **Aspose.CAD for Java** můžete **export dwg to pdf** — nebo rastrové obrázky — pouze pomocí několika řádků kódu. Tento tutoriál vás provede celým procesem, od načtení souboru DWG až po vytvoření vysoce kvalitního PDF, a zároveň zdůrazní, proč je Aspose.CAD Java preferovanou knihovnou pro úlohy konverze CAD.

## Quick Answers
- **What does this tutorial cover?** Exportování souborů DWG do PDF nebo rastrových obrázků pomocí Aspose.CAD pro Java.  
- **Do I need a license?** K vyzkoušení je k dispozici bezplatná dočasná licence; pro produkční nasazení je vyžadována plná licence.  
- **Which Java version is supported?** Jakékoli prostředí Java 8+ funguje s nejnovější Aspose.CAD Java API.  
- **Can I convert DWG to other image formats?** Ano – stejné možnosti rasterizace vám umožní výstup PNG, JPEG, BMP atd.  
- **How long does the conversion take?** Obvykle méně než sekunda pro standardní výkresy; větší soubory mohou trvat několik sekund.

## Why java cad library is the best choice for DWG conversion?

- **Pure Java implementation** – bez nativních DLL nebo externích nástrojů.  
- **Accurate unit handling** – metrické i imperiální jednotky jsou detekovány automaticky.  
- **High‑quality raster output** – jemně laděné DPI a kontrola velikosti stránky.  
- **Full PDF support** – generování PDF zachovávající vektorová data bez dalších závislostí.  
- **Flexible licensing** – začněte s **temporary license aspose** pro testování a poté přejděte na plnou licenci při nasazení.

## What is “export dwg to pdf”?

Exportování DWG do PDF znamená převod nativního výkresu AutoCADu do přenosného, zařízení‑nezávislého PDF dokumentu. Výsledné PDF zachovává vektorová data, vrstvy a měřítko, což je ideální pro sdílení, tisk nebo archivaci.

## Why use Aspose.CAD Java for this conversion?

Protože **java cad library** interně řeší vše od konverze jednotek po rasterizaci, vyhnete se složitosti nástrojů třetích stran a získáte konzistentní výsledky napříč platformami.

## Prerequisites

- Základní znalost programování v jazyce Java.  
- Knihovna Aspose.CAD for Java nainstalovaná. Pokud jste ji ještě ne stáhli, získáte ji **[here](https://releases.aspose.com/cad/java/)**.  
- DWG soubor pro testování – v tomto návodu je použita ukázka **Bottom_plate.dwg**.

## Import Namespaces

Ve vašem Java projektu importujte potřebné třídy, aby konverze mohla začít:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## Step‑by‑Step Guide

### Step 1: Load the DWG File

Nejprve načtěte svůj DWG výkres pomocí třídy `Image`. Tím vytvoříte reprezentaci v paměti, se kterou může Aspose.CAD pracovat.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

### Step 2: Determine Unit Type

Pochopení, zda výkres používá metrické nebo imperiální jednotky, je nezbytné pro správné měřítko. Pomocná metoda `IsMetric` (implementace vynechána pro stručnost) vrací boolean hodnotu.

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

### Step 3: Set Rasterization Options

Na základě systému jednotek nastavte velikost stránky, měřítko a cílový typ jednotek. Tyto možnosti určují, jak bude DWG rasterizován před zabalením do PDF.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();

if (currentUnitIsMetric) {
    // Metric units
    double metersCoeff = 1 / 1000.0;
    double scaleFactor = metersCoeff / currentUnitCoefficient;
    rasterizationOptions.setPageWidth((float)(210 * scaleFactor));
    rasterizationOptions.setPageHeight((float)(297 * scaleFactor));
    rasterizationOptions.setUnitType(UnitType.Millimeter);
} else {
    // Imperial units
    rasterizationOptions.setPageWidth((float)(8.27f / currentUnitCoefficient));
    rasterizationOptions.setPageHeight((float)(11.69f / currentUnitCoefficient));
    rasterizationOptions.setUnitType(UnitType.Inch);
}
```

### Step 4: Configure PDF Options (pdf options cad)

Vytvořte instanci `PdfOptions` a připojte nastavení rasterizace. Tím řeknete Aspose.CAD, jak vložit rasterizovaný obsah do finálního PDF.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

### Step 5: Save as PDF

Nakonec exportujte výkres do PDF souboru. Metoda `save` přijímá výstupní cestu a nakonfigurované `PdfOptions`.

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

Po dokončení kódu najdete **Saved.pdf** ve složce `DWGDrawings`, připravený k distribuci nebo archivaci.

## How to convert dwg raster images with java cad library

Pokud potřebujete místo PDF rastrové obrázky, jednoduše nahraďte `PdfOptions` odpovídajícími možnostmi pro rastrový obrázek (např. `PngOptions`, `JpegOptions`). Stejnou instanci `CadRasterizationOptions` můžete znovu použít, což vám umožní **convert dwg raster** soubory s minimálními změnami kódu.

## How to generate pdf dwg using pdf options cad

Výše uvedený příklad již **generates pdf dwg** výstup. Úpravou `pdfOptions` — například nastavením `pdfOptions.setCompress(true)` — můžete ovládat velikost a kvalitu PDF. To ukazuje flexibilitu API **pdf options cad**.

## Common Issues & Tips

- **Incorrect page size** – Zkontrolujte logiku konverze jednotek; nesprávné koeficienty mohou způsobit příliš velké stránky.  
- **Missing fonts or lineweights** – Ujistěte se, že DWG odkazuje na všechny externí zdroje před konverzí.  
- **Performance on large drawings** – Zvyšte nastavení `DPI` v `CadRasterizationOptions` jen tehdy, když je vyžadována vyšší kvalita; nižší DPI urychlí zpracování.  
- **License concerns** – Pro vyzkoušení můžete použít **temporary license aspose**; pro produkční nasazení je nutná plná licence.

## Frequently Asked Questions

**Q: Can I use Aspose.CAD for Java with other Java frameworks?**  
A: Ano, Aspose.CAD for Java se bez problémů integruje s populárními Java frameworky jako Spring, Jakarta EE a Android.

**Q: Is a temporary license available for Aspose.CAD for Java?**  
A: Ano, dočasnou licenci můžete získat **[here](https://purchase.aspose.com/temporary-license/)**.

**Q: Where can I find support for Aspose.CAD for Java?**  
A: Navštivte **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)** pro pomoc od komunity a inženýrů Aspose.

**Q: How can I purchase a license for Aspose.CAD for Java?**  
A: Licenci můžete zakoupit **[here](https://purchase.aspose.com/buy)**.

**Q: What units does Aspose.CAD for Java support?**  
A: Aspose.CAD for Java podporuje jak metrické, tak imperiální jednotky a automaticky detekuje systém jednotek výkresu.

**Q: Can I convert DWG to other image formats (e.g., PNG, JPEG) using the same API?**  
A: Rozhodně. Nahraďte `PdfOptions` odpovídajícími možnostmi pro rastrový obrázek (např. `PngOptions`) a znovu použijte stejný `CadRasterizationOptions`.

## Conclusion

Tento tutoriál ukázal, jak **export dwg to pdf** a rastrové obrázky pomocí **java cad library** Aspose.CAD pro Java. Dodržením krok‑za‑krokem průvodce můžete integrovat spolehlivou CAD konverzi do jakékoli Java aplikace, ať už potřebujete PDF pro dokumentaci nebo rastrové obrázky pro webové zobrazení.

---

**Last Updated:** 2026-02-17  
**Tested With:** Aspose.CAD for Java 24.10  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}