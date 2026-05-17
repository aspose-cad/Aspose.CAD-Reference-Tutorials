---
date: 2026-02-20
description: Naučte se, jak exportovat PDF z AutoCAD pomocí Aspose.CAD pro Javu. Tento
  krok‑za‑krokem průvodce vám ukáže, jak **převést DWG na PDF**, **uložit CAD jako
  PDF** a jak řešit licencování.
linktitle: Export AutoCAD Images to PDF
second_title: Aspose.CAD Java API
title: Převod DWG na PDF – Export obrázků AutoCAD do PDF pomocí Aspose.CAD pro Java
url: /cs/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export AutoCAD PDF - Export AutoCAD Images to PDF with Aspose.CAD for Java

## Introduction

Hledáte **convert DWG to PDF** pomocí Javy? Už nehledejte! V tomto tutoriálu vás provedeme konverzí AutoCAD obrázků do PDF pomocí Aspose.CAD for Java, výkonné knihovny, která činí proces **convert DWG to PDF** bez námahy. Na konci pochopíte, jak **save CAD as PDF**, nastavit vlastní rasterizační parametry a pracovat s licencí Aspose.CAD pro produkční použití.

## Quick Answers
- **Can I convert DWG to PDF with Java?** Ano, Aspose.CAD for Java podporuje DWG, DXF a mnoho dalších formátů.  
- **Do I need a license?** **Aspose CAD license** je vyžadována pro neomezené používání; dočasná licence je k dispozici pro hodnocení.  
- **What Java version is supported?** Java 8+ (knihovna je kompatibilní se všemi moderními JDK).  
- **Can I customize PDF page size?** Rozhodně – upravte `pageWidth` a `pageHeight` v rasterizačních možnostech.  
- **Is 3‑D rasterization possible?** Ano, povolte `TypeOfEntities.Entities3D` pro plné 3‑D vykreslení.

## What is **export autocad pdf**?
Exportování AutoCAD PDF znamená převod vektorových CAD výkresů (DWG, DXF, DWF atd.) do přenosného PDF dokumentu při zachování vrstev, tlouštěk čar a volitelně 3‑D geometrie. To je užitečné pro sdílení návrhů s klienty, archivaci nebo tisk bez nutnosti CAD softwaru.

## Why Convert DWG to PDF with Aspose.CAD for Java?
- **Full format support** – funguje s DWG, DXF, DWF a mnoha dalšími.  
- **No external dependencies** – čistě Java knihovna, bez nativních DLL.  
- **High‑quality rasterization** – kontrola DPI, velikosti stránky a rozvržení, takže můžete **customize PDF page size** podle požadavků projektu.  
- **License flexibility** – začněte s bezplatnou zkušební verzí, poté přejděte na trvalou **Aspose CAD license**.  

## Prerequisites

Předtím, než se pustíte do práce, ujistěte se, že máte:

- **Java Development Environment** – nainstalovaný JDK 8 nebo novější.  
- **Aspose.CAD for Java Library** – stáhněte z [download link](https://releases.aspose.com/cad/java/).  
- **Document Directory** – složku na vašem počítači, kde budou umístěny zdrojové CAD soubory i generované PDF.

## Import Namespaces

Ve vašem Java projektu importujte potřebné třídy pro práci s Aspose.CAD:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

Nyní projděme kód krok za krokem.

## How to convert DWG to PDF with Aspose.CAD for Java

### Step 1: Set the Resource Directory Path

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **Pro tip:** Nahraďte `"Your Document Directory"` absolutní cestou ke složce, kterou jste vytvořili v předchozím kroku.

### Step 2: Load the CAD Image

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **Why this matters:** Načtení CAD souboru do objektu `Image` vám poskytne plný přístup k rasterizačnímu enginu Aspose.CAD.

### Step 3: Set Rasterization Options

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- Upravit `pageWidth` a `pageHeight` pro **customize PDF page size**.  
- Odkomentujte řádek `setTypeOfEntities`, pokud potřebujete **java convert cad pdf** pro 3‑D entity.  
- Volání `setLayouts` vybírá, které rozvržení (Model, Layout1, atd.) bude vykresleno.

### Step 4: Configure PDF Options

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Tímto propojujete rasterizační nastavení s výstupem PDF, což zajišťuje správný převod vektorových dat.

### Step 5: Save the PDF

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

Výsledný soubor `Export3DImagestoPDF_out_.pdf` je **save cad as pdf** reprezentací vašeho původního AutoCAD výkresu.

## Common Issues & Solutions

| Symptom | Likely Cause | Fix |
|---------|--------------|-----|
| Blank PDF output | Rasterization options not set or layout mismatch | Verify `setLayouts` matches the layout name in your CAD file. |
| Low‑resolution image | `pageWidth`/`pageHeight` too small | Increase dimensions or set a higher DPI via `rasterizationOptions.setResolution(...)`. |
| License exception | No valid license applied | Apply an **Aspose CAD license** or use a temporary license for testing. |

## Frequently Asked Questions

### Q1: Can I use Aspose.CAD for Java with other CAD file formats?
A1: Yes, Aspose.CAD supports a wide range of formats including DWG, DWF, DGN, and more, giving you flexibility in your projects.

### Q2: How can I obtain a temporary license for Aspose.CAD for Java?
A2: Visit [here](https://purchase.aspose.com/temporary-license/) to obtain a temporary license for evaluation.

### Q3: Are there any layout options for rasterization?
A3: Yes, you can customize layouts (e.g., `"Model"`, `"Layout1"`) through the `setLayouts` method to control which view is rendered.

### Q4: Can I customize the size of the output PDF file?
A4: Absolutely! Adjust the `pageWidth` and `pageHeight` parameters in the rasterization options to fit your desired dimensions.

### Q5: Where can I seek help or discuss issues related to Aspose.CAD for Java?
A5: Head over to the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for dedicated support and community discussions.

---

**Last Updated:** 2026-02-20  
**Tested With:** Aspose.CAD for Java 24.10  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}