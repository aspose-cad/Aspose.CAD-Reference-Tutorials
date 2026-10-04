---
date: 2026-10-04
description: Узнайте, как быстро конвертировать DWG в PNG и экспортировать CAD в PNG
  или другие растровые форматы с помощью Aspose.CAD for Java. Получайте высококачественные
  результаты быстро.
keywords:
- convert dwg to png
- dwg to raster image
- convert cad to pdf
- export cad as png
- convert dwg to jpeg
lastmod: 2026-10-04
linktitle: Конвертировать макет CAD в растровый формат изображения
og_description: Быстро конвертировать DWG в PNG с помощью Aspose.CAD for Java. Узнайте
  пошагово, как экспортировать CAD в PNG, JPEG, TIFF и другие форматы.
og_image_alt: 'Developer guide: Convert DWG to PNG and other raster formats using
  Aspose.CAD for Java'
og_title: Конвертировать DWG в PNG и другие растровые форматы с помощью Aspose.CAD
  for Java
schemas:
- author: Aspose
  dateModified: '2026-10-04'
  description: Learn how to quickly convert dwg to png and export cad as png or other
    raster formats using Aspose.CAD for Java. Get high‑quality results fast.
  headline: Convert DWG to PNG and other raster formats using Aspose.CAD for Java
  type: TechArticle
- description: Learn how to quickly convert dwg to png and export cad as png or other
    raster formats using Aspose.CAD for Java. Get high‑quality results fast.
  name: Convert DWG to PNG and other raster formats using Aspose.CAD for Java
  steps:
  - name: set up the resource directory
    text: Replace `"Your Document Directory"` with the absolute path where your CAD
      files reside. This directory will be used for both input and output files.
  - name: load the CAD file
    text: '`Image.load` parses the source file and creates an in‑memory representation
      that you can rasterize. You can load any supported format (DWG, DXF, DGN, etc.)
      – this is the **how to convert cad** part.'
  - name: configure rasterization options
    text: '`CadRasterizationOptions` defines how the vector data is turned into pixels.
      `setPageWidth` and `setPageHeight` control output resolution (larger values
      = higher DPI). `setLayouts` lets you **convert CAD to raster** for specific
      layouts; omit it to rasterize the whole drawing.'
  - name: set image options
    text: '`TiffOptions` (or `PngOptions` for PNG) tells Aspose which raster format
      to generate and lets you fine‑tune compression, color depth, and other format‑specific
      settings. Choose the options class that matches your desired output.'
  - name: save the resultant image
    text: Call `save` on the `Image` instance, passing the output file name and the
      options object. Change the file extension to `.png` (and use `PngOptions`) to
      **save CAD as PNG**. The same pattern works for JPEG, BMP, or PDF. > **Common
      pitfall:** Forgetting to match the file extension with the options cla
  type: HowTo
- questions:
  - answer: Yes, it supports over 30 CAD and raster formats, including DWG, DXF, DGN,
      and SVG.
    question: Is Aspose.CAD compatible with different CAD file formats?
  - answer: Absolutely. Adjust `setPageWidth`, `setPageHeight`, or `setResolution`
      in `CadRasterizationOptions` to achieve the desired DPI.
    question: Can I customize the resolution of the output raster image?
  - answer: Provide an array with all layout names to `setLayouts`, e.g., `new String[]{"Model","Layout1","Layout2"}`.
    question: How can I convert multiple CAD layouts in a single run?
  - answer: Yes—PNG, JPEG, BMP, PDF, and more are available via their respective `*Options`
      classes.
    question: Are there output formats besides TIFF supported?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community
      support and official assistance.
    question: Where can I get help or share my experience with Aspose.CAD?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- convert dwg
- Aspose.CAD
- Java raster conversion
- CAD image processing
title: Конвертировать DWG в PNG и другие растровые форматы с помощью Aspose.CAD for
  Java
url: /ru/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Преобразование DWG в PNG и другие растровые форматы с помощью Aspose.CAD для Java

## Введение

`Aspose.CAD for Java` — это библиотека, позволяющая программно преобразовывать CAD‑файлы в растровые изображения, такие как PNG, JPEG и TIFF. Преобразование DWG в PNG (или другие растровые форматы) является распространённой задачей, когда нужно поделиться чертежами CAD с коллегами, у которых нет CAD‑просмотрщика, внедрить дизайны в документацию или создать миниатюры для веб‑галерей. В этом руководстве вы узнаете, как быстро и надёжно выполнить convert dwg to png, независимо от того, работаете ли вы с полным файлом чертежа или только с конкретным макетом. Возможно, вам также потребуется **convert CAD to raster** для веб‑превью, инструментов отчётности или мобильных приложений.

## Быстрые ответы
- **Какая библиотека обрабатывает DWG в PNG?** Aspose.CAD for Java provides the conversion engine.  
- **Какие растровые форматы я могу экспортировать?** PNG, JPEG, TIFF, PDF, BMP, and more than 30 additional formats.  
- **Нужна ли лицензия для тестирования?** A free trial works for development; a commercial license is required for production.  
- **Можно ли выбрать конкретный макет?** Yes – use `setLayouts` to target “Model”, “Layout1”, etc.  
- **Возможен ли вывод с высоким разрешением?** Absolutely – adjust `setPageWidth` and `setPageHeight` (or `setResolution`) to control DPI.

## Что такое «convert dwg to png»?

Convert dwg to png means transforming a DWG vector drawing into a pixel‑based PNG image that can be displayed by any standard image viewer. This process rasterizes vector entities, preserving line weight, colors, and layers while translating them into a fixed‑resolution bitmap. The result is ideal for embedding in PDFs, Word documents, or web pages where vector support is limited.

## Почему экспортировать CAD в PNG (или другие растровые форматы)?

Exporting CAD as PNG gives you universal compatibility, fast loading, and easy embedding across all major platforms. Raster images load instantly compared to opening a heavy DWG file, and PNG’s loss‑less compression ensures visual fidelity. By controlling resolution, background color, and layout, you guarantee that every stakeholder sees the same appearance, whether the file is viewed on a desktop, mobile device, or within a browser.

## Общие сценарии использования

| Сценарий | Почему растровый вывод полезен |
|----------|--------------------------------|
| **Документация проекта** | Embedding PNGs in PDFs or Word docs avoids requiring CAD software for reviewers. |
| **Веб‑порталы** | Thumbnails generated from DWG files load instantly and improve user experience. |
| **Мобильные приложения** | Raster images display correctly on devices that lack CAD viewers. |
| **Автоматизированная отчётность** | Batch‑convert multiple layouts to PNG/JPEG for inclusion in charts or dashboards. |

## Требования

Before you start, make sure you have:

1. **Java development environment** – JDK 8 or newer installed and configured.  
2. **Aspose.CAD for Java** – Download the latest JAR from the [Aspose.CAD for Java documentation](https://reference.aspose.com/cad/java/).  

## Импорт пространств имён

`com.aspose.cad.Image` is the core class that represents any CAD file in memory. `com.aspose.cad.imageoptions.*` provides option objects for each raster format. Import the classes you’ll need to load a drawing, configure rasterization, and save the output.

> **Pro tip:** If you plan to **export CAD as PNG** instead of TIFF, replace `TiffOptions` with `PngOptions` (found in `com.aspose.cad.imageoptions.PngOptions`).

## Пошаговое руководство

### Шаг 1: настройка каталога ресурсов

Replace `"Your Document Directory"` with the absolute path where your CAD files reside. This directory will be used for both input and output files.

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

### Шаг 2: загрузка CAD‑файла

`Image.load` parses the source file and creates an in‑memory representation that you can rasterize. You can load any supported format (DWG, DXF, DGN, etc.) – this is the **how to convert cad** part.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";
```

### Шаг 3: настройка параметров растеризации

`CadRasterizationOptions` defines how the vector data is turned into pixels. `setPageWidth` and `setPageHeight` control output resolution (larger values = higher DPI). `setLayouts` lets you **convert CAD to raster** for specific layouts; omit it to rasterize the whole drawing.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### Шаг 4: установка параметров изображения

`TiffOptions` (or `PngOptions` for PNG) tells Aspose which raster format to generate and lets you fine‑tune compression, color depth, and other format‑specific settings. Choose the options class that matches your desired output.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
rasterizationOptions.setLayouts(new String[] {"Model", "Layout1"});
```

### Шаг 5: сохранение полученного изображения

Call `save` on the `Image` instance, passing the output file name and the options object. Change the file extension to `.png` (and use `PngOptions`) to **save CAD as PNG**. The same pattern works for JPEG, BMP, or PDF.

```java
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.setVectorRasterizationOptions(rasterizationOptions);
```

> **Common pitfall:** Forgetting to match the file extension with the options class will cause an `UnsupportedFormatException`. Always keep them in sync.

## Распространённые проблемы и решения

| Проблема | Решение |
|----------|---------|
| **Пустое изображение** | Verify that the layout names in `setLayouts` exactly match those in the source CAD file. |
| **PNG с низким разрешением** | Increase `setPageWidth` / `setPageHeight` or set `setResolution` on the rasterization options. |
| **Неподдерживаемая версия DWG** | Ensure you are using the latest Aspose.CAD version; older releases may not support newer DWG releases. |
| **Ошибки памяти при больших файлах** | Process pages one at a time or increase JVM heap (`-Xmx2g`). |

## Часто задаваемые вопросы

**Q: Совместим ли Aspose.CAD с различными форматами CAD‑файлов?**  
A: Yes, it supports over 30 CAD and raster formats, including DWG, DXF, DGN, and SVG.

**Q: Можно ли настроить разрешение выходного растрового изображения?**  
A: Absolutely. Adjust `setPageWidth`, `setPageHeight`, or `setResolution` in `CadRasterizationOptions` to achieve the desired DPI.

**Q: Как преобразовать несколько макетов CAD за один запуск?**  
A: Provide an array with all layout names to `setLayouts`, e.g., `new String[]{"Model","Layout1","Layout2"}`.

**Q: Поддерживаются ли форматы вывода, кроме TIFF?**  
A: Yes—PNG, JPEG, BMP, PDF, and more are available via their respective `*Options` classes.

**Q: Где можно получить помощь или поделиться опытом с Aspose.CAD?**  
A: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community support and official assistance.

## Заключение

By following these steps you can **convert DWG to PNG**, **export CAD as PNG**, **save CAD as JPEG**, or generate any other raster format you need. Aspose.CAD for Java handles the heavy lifting, letting you focus on integrating high‑quality images into your applications, documentation, or web portals. The library’s support for 30+ formats and its ability to render multi‑hundred‑page drawings without loading the entire file into memory make it a robust choice for enterprise‑grade CAD rasterization.

---

**Последнее обновление:** 2026-10-04  
**Тестировано с:** Aspose.CAD for Java 24.12  
**Автор:** Aspose  







```java
image.save(dataDir + "conic_pyramid_layoutstorasterimage_out_.tiff", options);
```

```bash
java -jar aspose-cad.jar -i input.dwg -o output.png -w 1200 -h 1200
```

## Связанные руководства

- [Быстрый экспорт DWG в PDF или растровый формат с помощью Java‑библиотеки Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Преобразовать DWG в BMP с помощью Aspose.CAD for Java](/cad/java/cad-export-options/export-to-bmp/)
- [Экспорт DWG в PDF: конкретный макет с использованием Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}