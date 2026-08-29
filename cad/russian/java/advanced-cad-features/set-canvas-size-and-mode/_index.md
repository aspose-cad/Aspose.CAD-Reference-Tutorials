---
date: 2026-08-29
description: Узнайте, как установить размер страницы PDF и конвертировать CAD в PDF
  с помощью Aspose.CAD для Java, используя автоматическое масштабирование макета и
  экспорт в TIFF.
keywords:
- set pdf page size
- convert cad to pdf
- canvas size java
- high resolution tiff
- change pdf dimensions
lastmod: 2026-08-29
linktitle: Установить размер страницы PDF – конвертировать CAD в PDF
og_description: Узнайте, как установить размер страницы PDF при конвертации чертежей
  CAD в PDF в Java с использованием Aspose.CAD. Это руководство охватывает размеры
  холста, автоматическое масштабирование макета и экспорт в высоко‑разрешающий TIFF.
og_image_alt: Tutorial showing how to set pdf page size and convert CAD to PDF in
  Java
og_title: Установить размер страницы PDF – конвертировать CAD в PDF с Aspose в Java
schemas:
- author: Aspose
  dateModified: '2026-08-29'
  description: Learn how to set pdf page size and convert CAD to PDF using Aspose.CAD
    for Java, with automatic layout scaling and TIFF export.
  headline: Set pdf page size – convert cad to pdf (Java)
  type: TechArticle
- questions:
  - answer: No. Canvas size controls page dimensions; vector data remains resolution‑independent,
      ensuring crisp rendering at any zoom level.
    question: does the canvas size affect vector quality in the PDF?
  - answer: Yes. Adjust `rasterizationOptions.setResolution(dpiValue)` before creating
      `TiffOptions`.
    question: can I set a different DPI for the TIFF output?
  - answer: Use Aspose.PDF to load the generated PDF and call `pdf.getPages().setPageSize(PageSize.A4)`
      or a custom size.
    question: how can I change PDF dimensions for an existing PDF without re‑rendering
      the CAD?
  - answer: Keep `setAutomaticLayoutsScaling(true)` and avoid `setNoScaling(true)`;
      this retains layer visibility and layout fidelity.
    question: what is the best way to convert dxf to pdf while preserving layers?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- set pdf page size
- convert cad
- Aspose.CAD
- Java
- high resolution tiff
title: Установить размер страницы PDF – конвертировать CAD в PDF (Java)
url: /ru/java/advanced-cad-features/set-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Установить размер страницы PDF – конвертировать CAD в PDF (Java)

## Введение

Если вам необходимо **set pdf page size** при конвертации чертежей CAD в PDF, вы попали по адресу. В этом руководстве мы покажем, как использовать Aspose.CAD for Java для задания точных размеров холста, включения автоматического масштабирования макета и последующего экспорта результата в PDF и TIFF. Независимо от того, готовите ли вы инженерные схемы к печати или создаёте миниатюры для веб‑галереи, контроль над размером страницы и разрешением вывода имеет решающее значение.

## Быстрые ответы
- **Что означает “convert CAD to PDF”?** Преобразование чертежа CAD (например, DXF, DWG) в PDF‑документ, который можно просматривать на любой платформе.  
- **Могу ли я также экспортировать в TIFF?** Да — используйте `TiffOptions` для создания растровых изображений высокого разрешения.  
- **Какой параметр управляет размером холста в Java?** `CadRasterizationOptions.setPageWidth/Height`.  
- **Что такое автоматическое масштабирование макета?** Флаг (`setAutomaticLayoutsScaling(true)`), сохраняющий оригинальные пропорции макета при изменении размера холста.  
- **Нужна ли лицензия для Aspose.CAD?** Для использования в продакшене требуется временная или постоянная лицензия.

## Как установить размер страницы PDF при конвертации CAD в PDF на Java

Загрузите ваш CAD‑файл, настройте `CadRasterizationOptions` с нужной шириной и высотой, включите автоматическое масштабирование макета и затем сохраните результат в PDF. Такой двухшаговый подход позволяет точно задавать размеры выходной страницы без потери векторного качества.

## Что такое convert CAD to PDF?

Конвертация CAD в PDF означает преобразование векторных инженерных чертежей в PDF‑страницы, сохраняющие линии, слои и геометрию, делая файл универсально доступным. Процесс растеризует рисунок согласно указанным параметрам, создавая PDF, который можно открыть на любом устройстве без необходимости CAD‑программ, при этом сохраняет визуальную точность оригинального дизайна.

## Почему устанавливать размер холста в Java?

Установка размера холста в Java позволяет задать разрешение вывода и размеры страницы, гарантируя, что полученный PDF или TIFF соответствуют требованиям печати или отображения. Это также даёт контроль над поведением масштабирования, что критично для чертежей большого формата.

## Требования

Перед тем как приступить к руководству, убедитесь, что у вас есть следующие компоненты:

- Aspose.CAD for Java: Убедитесь, что библиотека Aspose.CAD установлена в вашей Java‑среде. Вы можете скачать библиотеку Aspose.CAD for Java [здесь](https://releases.aspose.com/cad/java/).
- Каталог документов: Создайте каталог для хранения ваших CAD‑файлов. Этот каталог будет использоваться в шагах руководства.

Итак, приступим к пошаговому руководству.

## Импорт пространств имён

В этом шаге мы импортируем необходимые пространства имён для запуска вашего проекта Aspose.CAD.

`Image` — основной класс, используемый для загрузки CAD‑файлов.

```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## Шаг 1: импортировать классы Aspose.CAD

Класс `Image` предоставляет методы для загрузки и сохранения CAD‑чертежей.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

В этом фрагменте кода мы задаём путь к каталогу ресурсов и загружаем DXF‑файл с помощью класса `Image` из Aspose.CAD.

## Шаг 2: установить свойства CadRasterizationOptions (set canvas size java)

`CadRasterizationOptions` задаёт параметры растеризации, такие как размер страницы и масштабирование для конвертации CAD в растр.

```java
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

Здесь мы создаём экземпляр `CadRasterizationOptions` и настраиваем свойства, такие как ширина страницы, высота страницы и **automatic layout scaling**. Это ядро **configure canvas mode** для вашей конвертации.

## Шаг 3: создать PdfOptions и установить vectorRasterizationOptions

`PdfOptions` определяет параметры вывода PDF для конвертации.

```java
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Set the VectorRasterizationOptions property
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Теперь мы создаём экземпляр `PdfOptions` и задаём его свойство `VectorRasterizationOptions` ранее сконфигурированным `CadRasterizationOptions`.

## Шаг 4: экспорт в PDF (convert CAD to PDF)

```java
// Export CAD to PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

Наконец, мы сохраняем изображение CAD в PDF‑файл, используя указанные параметры, завершая процесс **convert CAD to PDF**.

## Шаг 5: создать TiffOptions и установить vectorRasterizationOptions (export CAD to TIFF)

`TiffOptions` настраивает параметры вывода TIFF, такие как сжатие и разрешение.

```java
// Create an instance of TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Set the VectorRasterizationOptions property
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

На этом этапе мы создаём экземпляр `TiffOptions` и задаём его свойство `VectorRasterizationOptions`.

## Шаг 6: экспорт в TIFF

```java
// Export CAD to TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

В конце мы сохраняем изображение CAD в TIFF‑файл с указанными параметрами, демонстрируя, как **export CAD to TIFF** после настройки размера холста.

## Распространённые проблемы и решения

| Проблема | Причина | Решение |
|----------|---------|----------|
| PDF‑файл пустой | `setNoScaling(true)` отключает рендеринг для некоторых чертежей | Удалите `setNoScaling(true)` или установите значение `false`. |
| Разрешение TIFF выглядит низким | Ширина/высота страницы слишком малы | Увеличьте значения `setPageWidth` / `setPageHeight`. |
| Макет искажен | Отключено автоматическое масштабирование макета | Убедитесь, что включён `setAutomaticLayoutsScaling(true)`. |

## Почему следует регулировать размер холста и DPI?

Изменение размера холста напрямую влияет на разрешение растеризации выходного файла. Если вам нужно **increase TIFF resolution**, просто увеличьте значения `setPageWidth` / `setPageHeight` или вызовите `rasterizationOptions.setResolution(300)` перед созданием `TiffOptions`. Это даст вам растровые изображения высокого качества, подходящие для печати или детального анализа.

## Часто задаваемые вопросы

**Q1: могу ли я использовать Aspose.CAD for Java с другими Java‑фреймворками?**  
A: Да, Aspose.CAD разработан для бесшовной интеграции с различными Java‑фреймворками.

**Q2: доступна ли временная лицензия для Aspose.CAD?**  
A: Да, временную лицензию можно получить [здесь](https://purchase.aspose.com/temporary-license/).

**Q3: где я могу получить поддержку сообщества для Aspose.CAD?**  
A: Посетите форум Aspose.CAD [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) для получения поддержки и обсуждений.

**Q4: могу ли я попробовать Aspose.CAD бесплатно?**  
A: Конечно! Скачать бесплатную пробную версию можно [здесь](https://releases.aspose.com/).

**Q5: как приобрести Aspose.CAD for Java?**  
A: Приобрести Aspose.CAD for Java можно [здесь](https://purchase.aspose.com/buy).

### Дополнительные вопросы и ответы

**Q: влияет ли размер холста на векторное качество в PDF?**  
A: Нет. Размер холста управляет размерами страницы; векторные данные остаются независимыми от разрешения, обеспечивая чёткое отображение при любом масштабе.

**Q: могу ли я задать другое DPI для вывода TIFF?**  
A: Да. Настройте `rasterizationOptions.setResolution(dpiValue)` перед созданием `TiffOptions`.

**Q: как изменить размеры PDF для уже существующего PDF без повторного рендеринга CAD?**  
A: Используйте Aspose.PDF, загрузите сгенерированный PDF и вызовите `pdf.getPages().setPageSize(PageSize.A4)` или задайте пользовательский размер.

**Q: какой лучший способ конвертировать DXF в PDF, сохраняя слои?**  
A: Оставьте `setAutomaticLayoutsScaling(true)` и избегайте `setNoScaling(true)`; это сохраняет видимость слоёв и точность макета.

## Заключение

Поздравляем! Вы успешно **convert CAD to PDF** и **export CAD to TIFF**, при этом **set canvas size java**, включив **automatic layout scaling**, и научились **configure canvas mode** для получения высококачественных результатов. Это руководство предоставляет надёжную основу для ваших проектов по конвертации CAD. Изучайте дополнительные возможности в [документации Aspose.CAD](https://reference.aspose.com/cad/java/).

---

**Last Updated:** 2026-08-29  
**Tested with:** Aspose.CAD for Java 24.12  
**Author:** Aspose

## Связанные руководства

- [Установить размер холста – Расширенные функции CAD с Aspose.CAD for Java](/cad/java/advanced-cad-features/)
- [Экспорт DWG в PDF на Java – Установить размер страницы PDF с Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)
- [Установить пользовательский размер страницы – PDF из CAD с автоматическим масштабированием макета](/cad/java/advanced-cad-features/setting-auto-layout-scaling/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}