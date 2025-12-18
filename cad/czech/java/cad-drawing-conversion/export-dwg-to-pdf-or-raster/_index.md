---
date: 2025-12-18
description: Prozkoumejte, jak exportovat DWG do PDF nebo rastrových obrázků v Javě
  pomocí Aspose.CAD. Tento krok‑za‑krokem průvodce zajišťuje přesnost, efektivitu
  a snadnou konverzi souborů DWG.
linktitle: Export DWG to PDF or Raster
second_title: Aspose.CAD Java API
title: Export DWG do PDF nebo rastru pomocí Aspose.CAD pro Javu
url: /cs/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export DWG to PDF or Raster Using Aspose.CAD for Java

## Introduction

V dynamickém světě počítačově podporovaného návrhu (CAD) je efektivní práce s výkresy klíčová. S **Aspose.CAD for Java** můžete **export dwg to pdf** — nebo rastrové obrázky — pouze pomocí několika řádků kódu. Tento tutoriál vás provede celým procesem, od načtení souboru DWG až po vytvoření vysoce kvalitního PDF, a zároveň zdůrazní, proč je Aspose.CAD Java preferovanou knihovnou pro úlohy konverze CAD.

## Quick Answers
- **What does this tutorial cover?** Exporting DWG files to PDF or raster images using Aspose.CAD for Java.  
- **Do I need a license?** A free temporary license is available for evaluation; a full license is required for production.  
- **Which Java version is supported?** Any Java 8+ runtime works with the latest Aspose.CAD Java API.  
- **Can I convert DWG to other image formats?** Yes – the same rasterization options let you output PNG, JPEG, BMP, etc.  
- **How long does the conversion take?** Typically under a second for standard drawings; larger files may take a few seconds.

## What is “export dwg to pdf”?
Exportování DWG do PDF znamená převod nativního výkresu AutoCADu do přenosného, zařízení‑nezávislého PDF dokumentu. Výsledné PDF zachovává vektorová data, vrstvy a měřítko, což je ideální pro sdílení, tisk nebo archivaci.

## Why use Aspose.CAD Java for this conversion?
- **No external dependencies** – pure Java, no native DLLs.  
- **Accurate unit handling** – automatically respects metric or imperial units.  
- **High‑quality raster output** – fine‑tuned DPI and page size control.  
- **Full PDF support** – vector‑preserving PDF generation without additional libraries.

## Prerequisites

Než se pustíte do kódu, ujistěte se, že máte:

- Základní znalosti programování v Javě.  
- Nainstalovanou knihovnu Aspose.CAD for Java. Pokud jste ji ještě nestáhli, získáte ji **[here](https://releases.aspose.com/cad/java/)**.  
- DWG soubor pro testování – v tomto návodu je použita ukázková **Bottom_plate.dwg**.

## Import Namespaces

Ve vašem Java projektu importujte potřebné třídy pro zahájení konverze:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## Step‑by‑Step Guide

### Step 1: Load the DWG File

Nejprve načtěte svůj DWG výkres pomocí třídy `Image`. Tím vytvoříte paměťovou reprezentaci, se kterou může Aspose.CAD pracovat.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

### Step 2: Determine Unit Type

Pochopení, zda výkres používá metrické nebo imperiální jednotky, je nezbytné pro správné měřítko. Pomocná metoda `IsMetric` (implementace vynechána pro stručnost) vrací boolean příznak.

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

### Step 3: Set Rasterization Options

Na základě jednotkového systému nastavte velikost stránky, měřítko a cílový typ jednotek. Tyto možnosti určují, jak bude DWG rasterizován před zabalením do PDF.

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

### Step 4: Configure PDF Options

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

## Common Issues & Tips

- **Incorrect page size** – Double‑check the unit conversion logic; mismatched coefficients can produce oversized pages.  
- **Missing fonts or lineweights** – Ensure the DWG references any external resources before conversion.  
- **Performance on large drawings** – Increase the `DPI` setting in `CadRasterizationOptions` only when higher quality is required; lower DPI speeds up processing.

## Frequently Asked Questions

**Q: Can I use Aspose.CAD for Java with other Java frameworks?**  
A: Yes, Aspose.CAD for Java seamlessly integrates with popular Java frameworks such as Spring, Jakarta EE, and Android.

**Q: Is a temporary license available for Aspose.CAD for Java?**  
A: Yes, you can obtain a temporary license **[here](https://purchase.aspose.com/temporary-license/)**.

**Q: Where can I find support for Aspose.CAD for Java?**  
A: Visit the **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)** for assistance from the community and Aspose engineers.

**Q: How can I purchase a license for Aspose.CAD for Java?**  
A: You can purchase a license **[here](https://purchase.aspose.com/buy)**.

**Q: What units does Aspose.CAD for Java support?**  
A: Aspose.CAD for Java supports both metric and imperial units, automatically detecting the drawing’s unit system.

**Q: Can I convert DWG to other image formats (e.g., PNG, JPEG) using the same API?**  
A: Absolutely. Replace `PdfOptions` with the appropriate raster image options (e.g., `PngOptions`) and reuse the same `CadRasterizationOptions`.

## Conclusion

Tento tutoriál ukázal, jak **export dwg to pdf** a rastrové obrázky pomocí Aspose.CAD for Java. Dodržením krok‑za‑krokem průvodce můžete integrovat spolehlivou CAD konverzi do jakékoli Java aplikace, ať už potřebujete PDF pro dokumentaci nebo rastrové obrázky pro webové zobrazení.

---

**Last Updated:** 2025-12-18  
**Tested With:** Aspose.CAD for Java 24.10  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}