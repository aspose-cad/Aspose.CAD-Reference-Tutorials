---
date: 2025-12-25
description: Узнайте, как экспортировать DWG в BMP с помощью Aspose.CAD для Java.
  Это пошаговое руководство показывает, как настроить размер чертежа CAD и эффективно
  преобразовать CAD в BMP.
linktitle: Adjusting CAD Drawing Size Using Unit Type
second_title: Aspose.CAD Java API
title: Экспорт DWG в BMP – Регулировка размера CAD с использованием типа единицы (Java)
url: /ru/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Экспорт DWG в BMP – Регулировка размера чертежа CAD с использованием типа единицы измерения в Aspose.CAD для Java

## Введение

When you need to **export DWG to BMP**, controlling the output size and unit of measurement is essential for downstream processing or printing. In this tutorial you’ll learn how to adjust CAD drawing size and convert CAD to BMP with Aspose.CAD for Java, using the `UnitType` property to define the measurement unit. The steps are explained in plain language, so you can follow along even if you’re new to the library.

## Быстрые ответы
- **Что означает «export DWG to BMP»?** Converting a DWG drawing into a BMP raster image.  
- **Какое свойство управляет размером вывода?** `CadRasterizationOptions.setUnitType()` sets the unit (e.g., centimeter).  
- **Нужна ли лицензия для запуска кода?** A free trial works for evaluation; a license is required for production.  
- **Можно ли выбрать другие макеты?** Yes, use `setLayouts()` to specify model or paper space layouts.  
- **Какие форматы вывода поддерживаются?** Besides BMP, you can export to PNG, JPEG, TIFF, etc., by changing the options class.

## Что такое **export DWG to BMP**?

Exporting DWG to BMP means rasterizing a vector‑based DWG file into a bitmap image (BMP). This is useful when you need a pixel‑perfect representation for legacy systems, image processing pipelines, or simple display scenarios.

## Зачем регулировать размер чертежа CAD с помощью **Unit Type**?

Setting the unit type lets you control the physical dimensions of the exported image without manually calculating scaling factors. This ensures that the bitmap matches real‑world measurements (e.g., centimeters), which is crucial for engineering drawings and printed documentation.

## Требования

Before diving into the tutorial, make sure you have the following prerequisites in place:

- **Java Development Environment** – A functional JDK (8 or later) and an IDE or build tool (Maven/Gradle).  
- **Aspose.CAD for Java Library** – Download and integrate the Aspose.CAD library into your Java project. You can obtain the library [here](https://releases.aspose.com/cad/java/).

## Импорт пространств имён

In your Java code, include the necessary namespaces to access Aspose.CAD functionalities. Add the following imports:

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Now, let's break down the process of adjusting CAD drawing size using unit type into manageable steps:

## Шаг 1: Определить каталог данных

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

Set the path for the directory where your CAD files are located.

## Шаг 2: Загрузить чертёж CAD

```java
String sourceFilePath = dataDir + "sample.dwg";
Image image = Image.load(sourceFilePath);
```

Load the CAD drawing using Aspose.CAD's `Image` class.

## Шаг 3: Создать параметры BMP

```java
BmpOptions bmpOptions = new BmpOptions();
```

Instantiate the `BmpOptions` class for exporting the CAD layout to BMP format.

## Шаг 4: Настроить параметры растеризации

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

Create an instance of `CadRasterizationOptions` and associate it with the `BmpOptions` for vector rasterization.

## Шаг 5: Установить тип единицы измерения

```java
cadRasterizationOptions.setUnitType(UnitType.Centimeter);
```

Specify the desired unit type for the CAD drawing. In this example, we've set it to **Centimeter**, which directly influences the exported image size when you **adjust CAD drawing size**.

## Шаг 6: Установить макеты

```java
cadRasterizationOptions.setLayouts(new String[] { "Model" });
```

Define the layouts to be considered during the export. In this case, we've selected the **"Model"** layout, but you can switch to paper space layouts if needed.

## Шаг 7: Экспортировать в BMP

```java
String outPath = sourceFilePath + ".bmp";
image.save(outPath, bmpOptions);
```

Finally, save the modified CAD drawing in BMP format. This step completes the **export DWG to BMP** workflow while preserving the size adjustments you configured.

## Распространённые проблемы и решения

| Проблема | Причина | Решение |
|----------|---------|----------|
| **Output image is too small** | Unit type not set or default (pixel) used | Call `setUnitType()` with the desired measurement (e.g., `UnitType.Centimeter`). |
| **Wrong layout exported** | Layout name typo | Verify layout names with a CAD viewer; use exact string in `setLayouts()`. |
| **License exception** | Running without a valid license in production | Apply a temporary or permanent license as described in the FAQ. |

## Часто задаваемые вопросы (расширенные)

**Q: Can I use Aspose.CAD for Java with other programming languages?**  
A: Aspose.CAD primarily supports Java, but there are versions available for other languages like .NET.

**Q: Are there any licensing options for Aspose.CAD?**  
A: Yes, you can explore licensing options and purchase Aspose.CAD [here](https://purchase.aspose.com/buy).

**Q: Is there a free trial available for Aspose.CAD?**  
A: Certainly, you can access a free trial [here](https://releases.aspose.com/).

**Q: How can I get support for Aspose.CAD for Java?**  
A: Visit the Aspose.CAD forum [here](https://forum.aspose.com/c/cad/19) for comprehensive support.

**Q: Can I obtain a temporary license for Aspose.CAD?**  
A: Yes, you can acquire a temporary license [here](https://purchase.aspose.com/temporary-license/).

---

**Последнее обновление:** 2025-12-25  
**Тестировано с:** Aspose.CAD for Java 24.10  
**Автор:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}