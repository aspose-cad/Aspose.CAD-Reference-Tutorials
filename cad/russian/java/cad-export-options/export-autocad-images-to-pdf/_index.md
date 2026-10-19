---
date: 2026-10-19
description: Узнайте, как конвертировать DWG в PDF на Java с помощью Aspose.CAD. Это
  пошаговое руководство покажет, как экспортировать AutoCAD PDF, сохранить CAD в PDF
  и применить лицензию.
keywords:
- dwg to pdf java
- export autocad pdf
- java pdf export library
- aspose cad license
- save cad pdf
- customize pdf page size
lastmod: 2026-10-19
linktitle: Экспорт изображений AutoCAD в PDF
og_description: Узнайте, как конвертировать DWG в PDF на Java с помощью Aspose.CAD.
  Это руководство проведет вас через экспорт AutoCAD PDF, сохранение CAD в PDF и процесс
  лицензирования.
og_image_alt: 'Tutorial: convert DWG to PDF in Java with Aspose.CAD'
og_title: Конвертировать DWG в PDF на Java с использованием Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-10-19'
  description: Learn how to convert DWG to PDF in Java with Aspose.CAD. This step‑by‑step
    guide shows you how to export AutoCAD PDF, save CAD as PDF, and apply a license.
  headline: Convert DWG to PDF in Java using Aspose.CAD
  type: TechArticle
- description: Learn how to convert DWG to PDF in Java with Aspose.CAD. This step‑by‑step
    guide shows you how to export AutoCAD PDF, save CAD as PDF, and apply a license.
  name: Convert DWG to PDF in Java using Aspose.CAD
  steps:
  - name: set the resource directory path
    text: Replace `"Your Document Directory"` with the absolute path to the folder
      you created in the prerequisites. > **Pro tip:** Use `Paths.get(...).toAbsolutePath()`
      to avoid path‑related errors on different operating systems.
  - name: load the CAD image
    text: Loading the CAD file into an `Image` object gives you full access to Aspose.CAD’s
      rasterization engine. The `Image` class loads the DWG file and prepares it for
      conversion. > **Why this matters:** Once the drawing is in memory, you can query
      its layouts, layers, and metadata before rasterizing.
  - name: set rasterization options
    text: Adjust `pageWidth` and `pageHeight` to **customize PDF page size**. Enabling
      `setTypeOfEntities(TypeOfEntities.Entities3D)` allows full 3‑D rendering when
      needed. The `RasterizationOptions` object controls DPI, page dimensions, and
      entity types for the output. - `pageWidth` / `pageHeight` are measur
  - name: configure PDF options
    text: Tie the rasterization settings to the PDF output, ensuring the vector data
      is correctly transformed. The `PdfOptions` class links the rasterization configuration
      with the final PDF file.
  - name: save the PDF
    text: The resulting file, `Export3DImagestoPDF_out_.pdf`, is a **save cad as pdf**
      representation of your original AutoCAD drawing. The `save` method writes the
      rasterized image to a PDF file on disk.
  type: HowTo
- questions:
  - answer: Yes – the library supports DWG, DXF, DWF, DGN, and over 30 additional
      formats, giving you flexibility across projects.
    question: Can I use Aspose.CAD for Java with other CAD file formats?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to request a time‑limited license for evaluation.
    question: How do I obtain a temporary license for Aspose.CAD for Java?
  - answer: Absolutely. Use `setLayouts("Model")`, `setLayouts("Layout1")`, etc.,
      to choose which view is rendered into the PDF.
    question: Are there layout options for rasterization?
  - answer: Yes – modify `pageWidth` and `pageHeight` in the rasterization options
      to match any required page dimensions.
    question: Can I change the size of the output PDF file?
  - answer: The dedicated community is available at the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)
      where you can ask questions and share solutions.
    question: Where can I get help if I run into problems?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- dwg to pdf
- aspose.cad
- java cad conversion
- export autocad pdf
title: Конвертировать DWG в PDF на Java с использованием Aspose.CAD
url: /ru/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Экспорт PDF из AutoCAD – экспорт изображений AutoCAD в PDF с помощью Aspose.CAD для Java

## Введение

Если вам нужно **convert DWG to PDF in Java**, вы попали в нужное место. В этом руководстве показано, как экспортировать изображения AutoCAD в PDF с помощью Aspose.CAD for Java, чистой Java‑библиотеки, которая обрабатывает DWG, DXF, DWF и многие другие форматы CAD без нативных зависимостей. К концу вы сможете **save CAD as PDF**, настроить параметры растеризации, такие как размер страницы, и правильно применить **Aspose CAD license** для использования в продакшене.

## Быстрые ответы
- **Могу ли я конвертировать DWG в PDF с помощью Java?** Yes – Aspose.CAD for Java natively supports DWG, DXF and dozens of other CAD formats.  
- **Нужна ли лицензия?** A permanent **Aspose CAD license** removes all evaluation restrictions; a temporary license is available for testing.  
- **Какие версии Java поддерживаются?** Java 8 and higher are fully supported.  
- **Могу ли я управлять размерами страниц PDF?** Absolutely – set `pageWidth` and `pageHeight` in the rasterization options.  
- **Возможен ли 3‑D рендеринг?** Yes – enable `TypeOfEntities.Entities3D` to rasterize 3‑D entities.

## Что такое экспорт PDF из AutoCAD?
Экспорт PDF из AutoCAD — это процесс преобразования векторных чертежей CAD в портативный PDF‑документ. Он сохраняет слои, толщины линий, цвета и, при желании, 3‑D‑геометрию, облегчая обмен дизайнами с клиентами или их архивирование без необходимости в CAD‑программе.

## Почему конвертировать DWG в PDF с помощью Aspose.CAD for Java?
Aspose.CAD поддерживает **50+ input and output formats**, обрабатывает чертежи из нескольких сотен страниц без загрузки всего файла в память и работает на любой платформе, поддерживающей Java 8+. Библиотека предоставляет полный контроль над DPI, размером страницы и макетом, поэтому вы можете **customize PDF page size** в соответствии с точными спецификациями проекта, и всё это без установки нативных DLL.

## Требования

- **Java Development Kit** – JDK 8 или более поздняя версия, установленная на вашей рабочей станции.  
- **Aspose.CAD for Java** – загрузите последнюю JAR‑файл по [download link](https://releases.aspose.com/cad/java/).  
- **Working directory** – папка, в которой будут храниться исходные файлы DWG и сгенерированные PDF.

## Импорт пространств имён

Класс `Image` представляет любой растеризуемый чертеж CAD, а `RasterizationOptions` и `PdfOptions` позволяют точно настроить процесс конвертации.

Класс `Image` — это объект верхнего уровня Aspose.CAD, который хранит чертеж CAD в памяти.  
Класс `RasterizationOptions` определяет, как векторные данные растеризуются перед записью в PDF.  
Класс `PdfOptions` объединяет параметры растеризации с параметрами вывода, специфичными для PDF.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

Теперь пройдёмся по коду шаг за шагом.

## Как конвертировать DWG в PDF с помощью Aspose.CAD for Java?

Чтобы конвертировать файл DWG в PDF с помощью Aspose.CAD for Java, загрузите чертеж с помощью класса Image, настройте CadRasterizationOptions (например, DPI, размер страницы и типы сущностей), оберните эти параметры в PdfOptions и затем вызовите метод save, указав имя файла с расширением .pdf. Эта последовательность гарантирует правильную растеризацию векторных данных и то, что полученный PDF соответствует требованиям к макету.

### Шаг 1: установить путь к каталогу ресурсов

Замените `"Your Document Directory"` на абсолютный путь к папке, которую вы создали в разделе требований.

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **Pro tip:** Используйте `Paths.get(...).toAbsolutePath()`, чтобы избежать ошибок, связанных с путями, на разных операционных системах.

### Шаг 2: загрузить изображение CAD

Загрузка файла CAD в объект `Image` предоставляет полный доступ к движку растеризации Aspose.CAD.

Класс `Image` загружает файл DWG и подготавливает его к конвертации.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **Почему это важно:** Как только чертеж находится в памяти, вы можете запросить его макеты, слои и метаданные перед растеризацией.

### Шаг 3: установить параметры растеризации

Отрегулируйте `pageWidth` и `pageHeight`, чтобы **customize PDF page size**. Включение `setTypeOfEntities(TypeOfEntities.Entities3D)` позволяет выполнять полное 3‑D‑рендеринг при необходимости.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- `pageWidth` / `pageHeight` измеряются в пунктах (1 pt = 1/72 in).  
- Раскомментируйте строку `setTypeOfEntities` для 3‑D растеризации.  
- `setLayouts` выбирает, какой макет (Model, Layout1 и т.д.) будет отрисован.

### Шаг 4: настроить параметры PDF

Свяжите настройки растеризации с выводом PDF, обеспечивая корректное преобразование векторных данных.

Класс `PdfOptions` связывает конфигурацию растеризации с конечным PDF‑файлом.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Шаг 5: сохранить PDF

Полученный файл `Export3DImagestoPDF_out_.pdf` представляет собой **save cad as pdf** вашего оригинального чертежа AutoCAD.

Метод `save` записывает растеризованное изображение в PDF‑файл на диск.

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

## Распространённые проблемы и решения

| Симптом | Вероятная причина | Решение |
|---------|-------------------|---------|
| Пустой PDF | Rasterization options not set or layout mismatch | Verify `setLayouts` matches the layout name in your CAD file. |
| Изображение низкого разрешения | `pageWidth`/`pageHeight` too small | Increase dimensions or set a higher DPI via `rasterizationOptions.setResolution(...)`. |
| Исключение лицензии | No valid license applied | Apply an **Aspose CAD license** or use a temporary license for testing. |

## Часто задаваемые вопросы

**В: Могу ли я использовать Aspose.CAD for Java с другими форматами файлов CAD?**  
A: Да – библиотека поддерживает DWG, DXF, DWF, DGN и более 30 дополнительных форматов, предоставляя гибкость в проектах.

**В: Как я могу получить временную лицензию для Aspose.CAD for Java?**  
A: Перейдите на страницу [temporary license page](https://purchase.aspose.com/temporary-license/), чтобы запросить ограниченную по времени лицензию для оценки.

**В: Есть ли параметры макета для растеризации?**  
A: Конечно. Используйте `setLayouts("Model")`, `setLayouts("Layout1")` и т.д., чтобы выбрать, какой вид будет отрисован в PDF.

**В: Могу ли я изменить размер выходного PDF‑файла?**  
A: Да – измените `pageWidth` и `pageHeight` в параметрах растеризации, чтобы соответствовать требуемым размерам страницы.

**В: Где я могу получить помощь, если возникнут проблемы?**  
A: Специальное сообщество доступно на форуме [Aspose.CAD forum](https://forum.aspose.com/c/cad/19), где вы можете задавать вопросы и делиться решениями.

---

**Последнее обновление:** 2026-10-19  
**Тестировано с:** Aspose.CAD for Java 24.10  
**Автор:** Aspose

## Связанные руководства

- [Экспорт DWG в PDF на Java – Установить размер страницы PDF с помощью Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)
- [Экспорт DWG в PDF: конкретный макет с использованием Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Экспорт DWG в PDF и включить отслеживание с Aspose.CAD Java](/cad/java/additional-features/enable-tracking/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}