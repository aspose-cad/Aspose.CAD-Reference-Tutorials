---
date: 2026-08-29
description: Узнайте, как установить пользовательский размер страницы PDF и создать
  PDF из CAD с помощью Aspose.CAD for Java. Это пошаговое руководство охватывает экспорт
  CAD в PDF с использованием Auto Layout Scaling.
keywords:
- custom pdf page size
- create pdf from cad
- dwg to pdf java
- custom page size pdf
- java convert cad pdf
lastmod: 2026-08-29
linktitle: Настройка Auto Layout Scaling
og_description: Установите пользовательский размер страницы PDF при конвертации файлов
  CAD в PDF с помощью Aspose.CAD for Java. Следуйте пошаговому руководству по использованию
  Auto Layout Scaling и достигайте идеальных результатов макета.
og_image_alt: 'Tutorial: set custom pdf page size for CAD to PDF conversion using
  Aspose.CAD Java'
og_title: Установить пользовательский размер страницы PDF при экспорте CAD в PDF –
  Aspose.CAD Java
schemas:
- author: Aspose
  dateModified: '2026-08-29'
  description: Learn how to set a custom pdf page size and create PDF from CAD using
    Aspose.CAD for Java. This step‑by‑step guide covers export CAD to PDF with Auto
    Layout Scaling.
  headline: How to set custom pdf page size for CAD PDF export
  type: TechArticle
- description: Learn how to set a custom pdf page size and create PDF from CAD using
    Aspose.CAD for Java. This step‑by‑step guide covers export CAD to PDF with Auto
    Layout Scaling.
  name: How to set custom pdf page size for CAD PDF export
  steps:
  - name: load the CAD file
    text: Loading the source file is the first step in **how to export CAD** to a
      PDF document.
  - name: create rasterization options
    text: The `CadRasterizationOptions` class defines how the CAD drawing is rasterized
      and which page dimensions to use. It also lets you control DPI, background color,
      and other rendering details.
  - name: set auto layout scaling
    text: Enable the automatic scaling feature. This is the core of **how to set scaling**
      for a CAD‑to‑PDF conversion.
  - name: create PDF options
    text: Link the rasterization settings to the PDF export options.
  - name: export to PDF
    text: Finally, save the rendered image as a PDF file. This step completes the
      **convert dxf to pdf** workflow. Repeat the steps above for any additional CAD
      files you need to process, whether they are **DWG**, **DWF**, or other supported
      formats.
  type: HowTo
- questions:
  - answer: Aspose.CAD for Java supports a broad range of formats, including DWG,
      DXF, DWF, and more than 30 additional CAD types.
    question: Is Aspose.CAD for Java compatible with all CAD file formats?
  - answer: Yes, the `CadRasterizationOptions` class provides properties for fine‑tuning
      scaling, DPI, background color, and other rasterization settings.
    question: Can I customize the scaling options further?
  - answer: Refer to the [documentation](https://reference.aspose.com/cad/java/) for
      in‑depth information and examples.
    question: Where can I find additional documentation for Aspose.CAD for Java?
  - answer: Yes, you can explore a [free trial](https://releases.aspose.com/) to experience
      the capabilities of Aspose.CAD for Java.
    question: Is there a free trial available for Aspose.CAD for Java?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) to connect
      with the community and seek support.
    question: How can I seek assistance or engage in discussions about Aspose.CAD
      for Java?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- custom pdf page size
- Aspose.CAD
- Java CAD conversion
title: Как установить пользовательский размер страницы PDF при экспорте CAD в PDF
url: /ru/java/advanced-cad-features/setting-auto-layout-scaling/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Установить пользовательский размер PDF‑страницы – создать PDF из CAD с автоматическим масштабированием раскладки

## Введение

Если вам нужно **установить пользовательский размер PDF‑страницы** при **создании PDF из CAD** файлов быстро и с идеальным масштабированием, Aspose.CAD for Java вам поможет. Auto Layout Scaling автоматически изменяет размеры раскладок CAD, заполняя целевые размеры страницы, гарантируя, что полученный PDF соответствует требуемому размеру листа независимо от исходного чертежа. В этом руководстве мы пройдём весь процесс — от загрузки файла DXF до экспорта PDF — выделяя возможности библиотеки по **экспорту CAD в PDF** и показывая, как также **конвертировать DWG в PDF** или **увеличить разрешение PDF**, если это необходимо.

## Быстрые ответы
- **Что делает Auto Layout Scaling?** Он автоматически изменяет размеры раскладок CAD, чтобы они соответствовали целевым размерам страницы при растеризации.  
- **Какие форматы CAD я могу конвертировать?** Любой формат, поддерживаемый Aspose.CAD (например, DXF, DWG, DWF), может быть конвертирован в PDF.  
- **Нужна ли лицензия для продакшна?** Да, для использования не в режиме оценки требуется коммерческая лицензия.  
- **Сколько времени занимает типичная конверсия?** На современном оборудовании стандартный файл конвертируется менее чем за секунду.  
- **Можно ли изменить размер страницы?** Конечно — используйте `CadRasterizationOptions` для установки пользовательских размеров страницы.

## Что такое «создание PDF из CAD»?

Создание PDF из CAD означает преобразование векторного инженерного чертежа (DXF, DWG и т.д.) в PDF‑документ путём растеризации. PDF сохраняет визуальную точность оригинального чертежа, при этом его можно просматривать на любой платформе, и он открывается на устройствах, не поддерживающих нативные форматы CAD.

## Почему использовать автоматическое масштабирование раскладки?

Auto Layout Scaling гарантирует, что каждая раскладка полностью заполняет страницу PDF без ручных расчётов, экономя ваше время и устраняя ошибки масштабирования. Он также обеспечивает точное сохранение толщины линий и цветов при разных размерах вывода. Это обеспечивает последовательный, высококачественный результат для десятков файлов CAD и поддерживает пакетную обработку крупных проектов.

## Необходимые условия

1. **Библиотека Aspose.CAD for Java** – скачайте последнюю версию со [страницы загрузки](https://releases.aspose.com/cad/java/).  
2. **Каталог ресурсов** – создайте папку на вашем компьютере для хранения файлов CAD; замените `"Your Document Directory"` в коде на этот путь.  
3. **Пример файла CAD** – для данного руководства мы будем использовать `conic_pyramid.dxf`, который включён в набор образцов данных Aspose.

## Импорт пространств имён

Сначала импортируйте необходимые классы. Это даст нам доступ к загрузке изображений, растеризации и функциям экспорта в PDF.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Как установить пользовательский размер страницы PDF из CAD

Прежде чем перейти к пошаговому коду, разъясним, почему важны пользовательские размеры страниц. Установка **пользовательского размера PDF‑страницы** позволяет соответствовать отраслевым стандартам листов (A4, A1, Letter) или определить индивидуальное полотно, что необходимо для нормативных представлений, технических руководств или печати высокого разрешения.

### Шаг 1: загрузить файл CAD

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### Шаг 2: создать параметры растеризации

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

### Шаг 3: установить автоматическое масштабирование раскладки

```java
rasterizationOptions.setAutomaticLayoutsScaling(true);
```

### Шаг 4: создать параметры PDF

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Шаг 5: экспортировать в PDF

```java
image.save(dataDir + "result_out_.pdf", pdfOptions);
```

Повторите указанные шаги для любых дополнительных файлов CAD, которые необходимо обработать, будь то **DWG**, **DWF** или другие поддерживаемые форматы.

## Распространённые сценарии использования

| Сценарий | Зачем устанавливать пользовательский размер страницы? |
|----------|-----------------------------|
| **Подача строительных чертежей** | Соответствует PDF стандартным размерам листов A1/A2, требуемым регуляторными органами. |
| **Встраивание в технические руководства** | Гарантирует, что чертеж вписывается в предопределённый макет руководства без дополнительного масштабирования. |
| **Печать высокого разрешения** | Позволяет увеличить DPI (например, `rasterizationOptions.setResolution(300)`) при сохранении постоянных размеров страницы. |

## Распространённые проблемы и их устранение

| Симптом | Вероятная причина | Решение |
|---------|--------------|-----|
| Пустой PDF‑файл | Параметры растеризации не заданы или путь к файлу неверный | Проверьте путь `srcFile` и убедитесь, что `setPageWidth/Height` не равны нулю |
| Искажённое масштабирование | `setAutomaticLayoutsScaling` оставлен `false` | Включите автоматическое масштабирование или вручную вычислите коэффициент масштабирования |
| Отсутствуют слои | Исходный DXF содержит неподдерживаемые сущности | Проверьте примечания к выпуску Aspose.CAD на предмет поддерживаемых типов сущностей |

Aspose.CAD поддерживает конвертацию **более 30 форматов CAD** и может обрабатывать файлы размером до **500 МБ** без загрузки всего документа в память, обеспечивая быстрые и экономные по памяти конверсии для корпоративных нагрузок.

## Часто задаваемые вопросы

**В: Совместим ли Aspose.CAD for Java со всеми форматами CAD‑файлов?**  
О: Aspose.CAD for Java поддерживает широкий спектр форматов, включая DWG, DXF, DWF и более 30 дополнительных типов CAD.

**В: Можно ли дополнительно настроить параметры масштабирования?**  
О: Да, класс `CadRasterizationOptions` предоставляет свойства для точной настройки масштабирования, DPI, цвета фона и других параметров растеризации.

**В: Где можно найти дополнительную документацию по Aspose.CAD for Java?**  
О: Обратитесь к [документации](https://reference.aspose.com/cad/java/) для подробной информации и примеров.

**В: Доступна ли бесплатная пробная версия Aspose.CAD for Java?**  
О: Да, вы можете попробовать [бесплатную пробную версию](https://releases.aspose.com/), чтобы оценить возможности Aspose.CAD for Java.

**В: Как получить помощь или принять участие в обсуждениях Aspose.CAD for Java?**  
О: Посетите [форум Aspose.CAD](https://forum.aspose.com/c/cad/19), чтобы связаться с сообществом и получить поддержку.

**Дополнительные часто задаваемые вопросы**

**В: Как конвертировать файл DWG в PDF вместо DXF?**  
О: Тот же код работает; просто измените расширение файла в `srcFile` на `.dwg`.

**В: Можно ли установить пользовательский DPI для PDF более высокого разрешения?**  
О: Да, используйте `rasterizationOptions.setResolution(300);` (или любой необходимый DPI).

**В: Можно ли встроить шрифты в сгенерированный PDF?**  
О: Aspose.CAD растеризует чертеж, поэтому шрифты отображаются как векторы; отдельное встраивание шрифтов не требуется.

## Заключение

Следуя этому руководству, вы теперь знаете, как **установить пользовательский размер PDF‑страницы** и **создать PDF из CAD** файлов с помощью Aspose.CAD for Java и Auto Layout Scaling. Процесс упрощает рабочий поток **экспорта CAD в PDF**, обеспечивает согласованное масштабирование и экономит ваше ценное время разработки. Не стесняйтесь экспериментировать с различными размерами страниц, разрешениями и форматами CAD, чтобы соответствовать потребностям вашего проекта, будь то **конвертация DWG в PDF**, **увеличение разрешения PDF** или создание пакетного процессора **java CAD в PDF**.

---

**Last updated:** 2026-08-29  
**Tested with:** Aspose.CAD for Java 24.12 (latest)  
**Author:** Aspose

## Связанные руководства

- [Как установить размер PDF‑страницы и включить отслеживание процесса рендеринга CAD с использованием Aspose.CAD for Java](/cad/java/advanced-cad-features/enable-tracking-for-cad-rendering-process/)
- [Установить размер PDF‑страницы – Конвертировать CAD в PDF (Java)](/cad/java/advanced-cad-features/set-canvas-size-and-mode/)
- [Быстро экспортировать DWG в PDF или растр с помощью java‑библиотеки Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}