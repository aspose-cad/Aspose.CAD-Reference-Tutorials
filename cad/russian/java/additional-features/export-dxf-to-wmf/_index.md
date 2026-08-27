---
date: 2026-06-09
description: Узнайте, как конвертировать DXF в WMF с помощью Aspose.CAD для Java,
  включая бесплатную пробную версию, поддержку Java 8+ и опциональный экспорт в PDF.
  Пошаговое руководство с примерами кода.
keywords:
- convert dxf to wmf
- aspose cad java
- aspose free trial
- aspose cad conversion
- export dxf pdf
linktitle: Экспортировать DXF в формат WMF с помощью Java
schemas:
- author: Aspose
  dateModified: '2026-06-09'
  description: Learn how to convert DXF to WMF with Aspose.CAD for Java, including
    a free trial, Java 8+ support, and optional PDF export. Step‑by‑step guide with
    code examples.
  headline: Convert DXF to WMF Using Aspose.CAD in Java
  type: TechArticle
- description: Learn how to convert DXF to WMF with Aspose.CAD for Java, including
    a free trial, Java 8+ support, and optional PDF export. Step‑by‑step guide with
    code examples.
  name: Convert DXF to WMF Using Aspose.CAD in Java
  steps:
  - name: Load DXF Drawing
    text: Image.load reads the DXF file into an Aspose.CAD Image object.
  - name: Configure Rasterization Options
    text: CadRasterizationOptions specifies page size, resolution, and background
      for rasterizing the CAD drawing.
  - name: Save as WMF
    text: ImageSaveOptions with SaveFormat.WMF tells Aspose.CAD to write the output
      as a Windows Metafile.
  - name: Dispose of Resources
    text: Calling image.close() releases native resources used by the Aspose.CAD Image
      object.
  - name: Optional – Export to PDF
    text: PdfOptions configures PDF‑specific settings when saving the image as a PDF
      document. > **Pro tip:** You can reuse the same `CadRasterizationOptions` object
      for PDF export by passing it to a `PdfOptions` instance, saving you a few lines
      of setup.
  type: HowTo
- questions:
  - answer: Yes. Load the file in a try‑with‑resources block and dispose of the `Image`
      object promptly. Adjust `CadRasterizationOptions.setPageWidth/Height` to a reasonable
      size to keep memory usage low.
    question: Can I convert large DXF files (hundreds of MB) without running out of
      memory?
  - answer: WMF is a flat vector format, so layer hierarchy is flattened, but line
      styles, colors, and hatch patterns are preserved.
    question: Does the WMF output retain layer information?
  - answer: Use `rasterizationOptions.setResolution(300);` to define DPI before saving.
    question: Is it possible to set a custom DPI for the WMF?
  - answer: Absolutely. Loop through a directory, load each file, and apply the same
      rasterization and save logic.
    question: Can I batch‑convert multiple DXF files in one run?
  - answer: Aspose.CAD for Java supports Java 8 and later, including Java 11, 17,
      and newer LTS releases.
    question: What versions of Java are supported?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Конвертировать DXF в WMF с помощью Aspose.CAD на Java
url: /ru/java/additional-features/export-dxf-to-wmf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Преобразование DXF в WMF с помощью Aspose.CAD в Java

## Введение

В этом руководстве вы узнаете, как **преобразовать DXF в WMF** с помощью Aspose.CAD для Java. Независимо от того, нужно ли вам внедрить CAD‑чертежи в отчет на базе Windows, создать легковесные векторные графики для документов Office или автоматизировать пакетные преобразования, преобразование DXF в WMF часто требуется в инженерных и отчетных конвейерах. Мы пройдем процесс загрузки DXF‑чертежа, настройки параметров растеризации, сохранения результата в WMF и, при желании, экспорта того же чертежа в PDF.

## Быстрые ответы
- **Можно ли преобразовать DXF в WMF с бесплатной пробной версией?** Да — Aspose предлагает полностью функциональную 30‑дневную пробную версию.  
- **Какая версия Java требуется?** Java 8 или новее.  
- **Нужна ли лицензия для запуска кода?** Лицензия требуется для продакшна; пробная версия подходит для разработки и тестирования.  
- **Является ли преобразование без потерь?** Векторные данные сохраняются; параметры растеризации позволяют контролировать разрешение.  
- **Могу ли я также экспортировать тот же чертеж в PDF?** Конечно — см. шаг «Экспорт в PDF» ниже.

## Что такое «преобразование DXF в WMF»?

Преобразование DXF в WMF означает взятие файла Drawing Exchange Format (DXF) — широко используемого формата CAD — и превращение его в Windows Metafile (WMF). WMF — это векторный формат изображения, который легко интегрируется с Microsoft Office, приложениями Windows и многими инструментами отчетности.

## Почему использовать Aspose.CAD для Java?

Aspose.CAD for Java предоставляет чисто Java‑движок без нативных DLL, который преобразует CAD‑файлы с **более чем 99 % векторной точности**, сохраняя слои, цвета, стили линий и штриховки. Он поддерживает **более 50 входных и выходных форматов** — включая DXF, DWG, DGN, PDF, PNG, SVG и WMF — позволяя точно настраивать размер страницы, DPI и цвет фона через встроенные параметры растеризации. Тот же API также обрабатывает экспорт в PDF, PNG и SVG, устраняя необходимость в нескольких библиотеках.

### Ключевые преимущества
- **Отсутствие внешних зависимостей** — чистый Java, работает на любой ОС, где запущен Java.  
- **Визуализация с высокой точностью** — сохраняет толщину линий, цвет и детали штриховки.  
- **Встроенная растеризация** — контроль размеров страницы, разрешения и фона.  
- **Все в одном** — те же классы экспортируют в WMF, PDF, PNG, SVG и т.д.

## Предварительные требования

- **Aspose.CAD for Java**, интегрированный в ваш проект. Скачайте его с официального сайта: [Aspose.CAD Java download](https://releases.aspose.com/cad/java/).  
- **Каталог документов**, где хранятся ваши DXF‑файлы (например, `Your Document Directory/DXFDrawings/`).  

## Импорт пространств имён

Следующие импорты подключают классы Aspose.CAD, необходимые для загрузки, растеризации и сохранения CAD‑файлов.  
```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageSaveOptions;
import com.aspose.cad.fileformats.cad.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.CadImageInfo;
import com.aspose.cad.fileformats.cad.CadImageInfo;
import java.awt.Color;
```

## Пошаговое руководство

### Как преобразовать DXF в WMF в Java?

Загрузите ваш DXF‑файл с помощью `Image.load("yourFile.dxf")`, настройте `CadRasterizationOptions` для требуемого размера страницы и DPI, затем вызовите `image.save("output.wmf", new ImageSaveOptions(SaveFormat.WMF))`. Эта трёхшаговая схема выполняет полное преобразование, сохраняя векторное качество, и требует всего несколько строк кода.

#### Шаг 1: Загрузка DXF‑чертежа

Image.load читает DXF‑файл в объект Aspose.CAD Image.  
```java
import com.aspose.cad.Color;
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.WmfOptions;
```

#### Шаг 2: Настройка параметров растеризации

CadRasterizationOptions задаёт размер страницы, разрешение и фон для растеризации CAD‑чертежа.  
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DXFDrawings/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

#### Шаг 3: Сохранение как WMF

ImageSaveOptions с SaveFormat.WMF указывает Aspose.CAD записать вывод в виде Windows Metafile.  
```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(100);
rasterizationOptions.setPageHeight(100);
WmfOptions wmfOptions = new WmfOptions();
```

#### Шаг 4: Освобождение ресурсов

Вызов `image.close()` освобождает нативные ресурсы, используемые объектом Aspose.CAD Image.  
```java
cadImage.save(dataDir+" example.ifc.wmf", wmfOptions);
```

#### Шаг 5: Необязательно — экспорт в PDF

PdfOptions настраивает параметры, специфичные для PDF, при сохранении изображения как PDF‑документа.  
```java
finally
{
  cadImage.dispose();
}
```

> **Pro tip:** Вы можете повторно использовать тот же объект `CadRasterizationOptions` для экспорта в PDF, передав его в экземпляр `PdfOptions`, что сэкономит несколько строк настройки.

## Как экспортировать DXF в PDF с помощью Aspose CAD Java?

Экспорт в PDF следует тем же шагам загрузки и растеризации; просто замените формат сохранения WMF на PDF. Используйте `new ImageSaveOptions(SaveFormat.Pdf)` и при желании задайте параметры PDF, такие как уровень сжатия или метаданные автора. Эта однострочная конверсия создаёт поисковый, точно соответствующий оригинальному CAD‑макету PDF.

## Распространённые проблемы и решения

| Проблема | Причина | Решение |
|----------|---------|---------|
| **`NullPointerException` при `cadImage.save`** | Переменная `cadImage` не определена (должна быть `image`). | Замените `cadImage` на `image` или переименуйте переменную последовательно. |
| **Выходной WMF пустой** | Размер страницы растеризации слишком мал или цвет фона установлен как прозрачный. | Увеличьте `PageWidth`/`PageHeight` или задайте цвет фона через `rasterizationOptions.setBackgroundColor(Color.WHITE);`. |
| **Исключение лицензии** | Запуск без действующей лицензии Aspose в продакшн. | Примените файл лицензии при старте приложения: `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`. |

## Заключение

Теперь у вас есть полностью готовый к продакшену рабочий процесс **преобразования DXF в WMF** с помощью Aspose.CAD для Java, с дополнительным шагом **экспорта того же чертежа в PDF**. Этот подход обеспечивает высококачественный векторный вывод, который бесшовно интегрируется с инструментами отчетности и документации на базе Windows, при этом ваш код остаётся простым и без внешних зависимостей.

## Часто задаваемые вопросы

### Q1: Где можно найти документацию Aspose.CAD?

A1: Вы можете получить доступ к документации [здесь](https://reference.aspose.com/cad/java/).

### Q2: Как скачать Aspose.CAD для Java?

A2: Скачайте библиотеку [здесь](https://releases.aspose.com/cad/java/).

### Q3: Доступна ли бесплатная пробная версия?

A3: Да, вы можете получить бесплатную пробную версию [здесь](https://releases.aspose.com/).

### Q4: Нужны варианты временной лицензии?

A4: Изучите временные лицензии [здесь](https://purchase.aspose.com/temporary-license/).

### Q5: Где можно получить поддержку?

A5: Посетите форум поддержки Aspose.CAD [здесь](https://forum.aspose.com/c/cad/19).

## Часто задаваемые вопросы

**В:** Могу ли я преобразовать большие DXF‑файлы (сотни МБ), не исчерпывая память?  
**О:** Да. Загружайте файл в блоке try‑with‑resources и своевременно освобождайте объект `Image`. Настройте `CadRasterizationOptions.setPageWidth/Height` до разумного размера, чтобы снизить потребление памяти.

**В:** Сохраняет ли WMF информацию о слоях?  
**О:** WMF — плоский векторный формат, поэтому иерархия слоёв уплощается, но стили линий, цвета и штриховки сохраняются.

**В:** Можно ли задать пользовательский DPI для WMF?  
**О:** Используйте `rasterizationOptions.setResolution(300);` для определения DPI перед сохранением.

**В:** Могу ли я пакетно преобразовать несколько DXF‑файлов за один запуск?  
**О:** Конечно. Пройдитесь по каталогу, загрузите каждый файл и примените одинаковую логику растеризации и сохранения.

**В:** Какие версии Java поддерживаются?  
**О:** Aspose.CAD for Java поддерживает Java 8 и новее, включая Java 11, 17 и более новые LTS‑версии.

---

**Последнее обновление:** 2026-06-09  
**Тестировано с:** Aspose.CAD for Java 24.11  
**Автор:** Aspose

```java
image.save(dataDir + "conic_pyramid_out_.pdf"); 
```

## Связанные руководства

- [Создать PDF из CAD — экспорт DXF в PDF с помощью Aspose.CAD for Java](/cad/java/additional-features/export-dxf-to-pdf/)
- [Создать PDF из DXF: экспортировать слой с Aspose.CAD for Java](/cad/java/additional-features/export-specific-layer-to-pdf/)
- [Как преобразовать макет DXF в изображение JPEG с помощью Aspose.CAD в Java](/cad/java/additional-features/export-specific-layout-to-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}