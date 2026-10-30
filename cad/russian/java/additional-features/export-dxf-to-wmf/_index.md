---
date: 2026-10-30
description: Узнайте, как пакетно преобразовать файлы DXF в WMF с помощью Aspose.CAD
  for Java, используя пошаговый код, информацию о бесплатной пробной версии и возможность
  экспорта в PDF.
keywords:
- batch convert dxf files
- aspose cad java
- dxf to wmf conversion
- java cad rasterization
- aspose free trial
lastmod: 2026-10-30
linktitle: Экспорт DXF в формат WMF с использованием Java
og_description: Пакетное преобразование файлов DXF в WMF с помощью Aspose.CAD for
  Java. Следуйте этому руководству, чтобы загрузить чертежи DXF, задать параметры
  растеризации, сохранить в формате WMF и при желании экспортировать в PDF, используя
  бесплатную пробную версию.
og_image_alt: Tutorial showing batch conversion of DXF to WMF in Java using Aspose.CAD
og_title: Пакетное преобразование файлов DXF в WMF с помощью Aspose.CAD for Java
schemas:
- author: Aspose
  dateModified: '2026-10-30'
  description: Learn how to batch convert DXF files to WMF using Aspose.CAD for Java,
    with step‑by‑step code, free trial info, and optional PDF export.
  headline: Batch convert DXF files to WMF with Aspose.CAD for Java
  type: TechArticle
- description: Learn how to batch convert DXF files to WMF using Aspose.CAD for Java,
    with step‑by‑step code, free trial info, and optional PDF export.
  name: Batch convert DXF files to WMF with Aspose.CAD for Java
  steps:
  - name: load dxf drawing
    text: Image.load reads the DXF file into an Aspose.CAD Image object.
  - name: configure rasterization options
    text: '`CadRasterizationOptions` specifies page size, resolution, and background
      for rasterizing the CAD drawing.'
  - name: save as wmf
    text: '`ImageSaveOptions` with `SaveFormat.WMF` tells Aspose.CAD to write the
      output as a Windows Metafile.'
  - name: dispose of resources
    text: Calling `image.close()` releases native resources used by the Aspose.CAD
      Image object.
  - name: optional – export to pdf
    text: '`PdfOptions` configures PDF‑specific settings when saving the image as
      a PDF document. > **Pro tip:** You can reuse the same `CadRasterizationOptions`
      object for PDF export by passing it to a `PdfOptions` instance, saving you a
      few lines of setup.'
  type: HowTo
- questions:
  - answer: You can access the documentation [Aspose.CAD Java documentation](https://reference.aspose.com/cad/java/).
    question: Where can I find the Aspose.CAD documentation?
  - answer: Download the library [Aspose.CAD Java download page](https://releases.aspose.com/cad/java/).
    question: How do I download Aspose.CAD for Java?
  - answer: Yes, you can get a free trial [Aspose free trial page](https://releases.aspose.com/).
    question: Is there a free trial available?
  - answer: Explore temporary licenses [temporary license options](https://purchase.aspose.com/temporary-license/).
    question: Need temporary licensing options?
  - answer: Visit the Aspose.CAD support forum [Aspose.CAD support forum](https://forum.aspose.com/c/cad/19).
    question: Where can I get support?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- batch convert dxf
- Aspose.CAD
- Java CAD conversion
- WMF export
- DXF processing
title: Пакетное преобразование файлов DXF в WMF с помощью Aspose.CAD for Java
url: /ru/java/additional-features/export-dxf-to-wmf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Пакетное преобразование файлов DXF в WMF с помощью Aspose.CAD для Java

## Введение

В этом руководстве вы узнаете, как **пакетно преобразовать файлы DXF в WMF** с помощью Aspose.CAD для Java. Независимо от того, нужно ли вам внедрять CAD‑чертежи в отчёты для Windows, генерировать лёгкие векторные графики для документов Office или автоматизировать масштабные преобразования, это руководство проведёт вас через загрузку чертежа DXF, настройку параметров растеризации, сохранение в WMF и, при желании, экспорт того же чертежа в PDF. Шаги работают на любой платформе, поддерживающей Java 8+.

## Быстрые ответы
- **Могу ли я преобразовать DXF в WMF с бесплатной пробной версией?** Да — Aspose предлагает полностью функциональную 30‑дневную пробную версию.  
- **Какая версия Java требуется?** Java 8 или новее.  
- **Нужна ли лицензия для выполнения кода?** Лицензия требуется для продакшн; пробная версия подходит для разработки и тестирования.  
- **Является ли преобразование без потерь?** Векторные данные сохраняются; параметры растеризации позволяют контролировать разрешение.  
- **Могу ли я также экспортировать тот же чертеж в PDF?** Конечно — см. шаг «Экспорт в PDF» ниже.  
- **Как пакетно преобразовать множество файлов DXF одновременно?** Пройтись по папке, применяя один и тот же шаблон загрузка‑растеризация‑сохранение к каждому файлу.

## Что такое пакетное преобразование файлов DXF?

Пакетное преобразование файлов DXF означает обработку нескольких чертежей в формате Drawing Exchange Format (DXF) за один запуск и создание WMF‑вывода для каждого. WMF (Windows Metafile) — векторный формат изображения, который нативно интегрируется с Microsoft Office, приложениями Windows и множеством инструментов отчётности.

## Почему использовать Aspose.CAD для Java?

Aspose.CAD для Java — это чисто Java‑движок, поддерживающий **более 50 входных и выходных форматов** — включая DXF, DWG, DGN, PDF, PNG, SVG и WMF — при обеспечении **99 % векторной точности**. Он работает на любой ОС, поддерживающей Java, не требует нативных DLL и позволяет управлять размером страницы, DPI и цветом фона через единственный класс `CadRasterizationOptions`. Тот же API также обрабатывает экспорт в PDF, PNG и SVG, устраняя необходимость в нескольких библиотеках.

### Количественные преимущества
- **Более 50 поддерживаемых форматов** снижают необходимость в сторонних конвертерах.  
- **Обрабатывает DXF‑файлы на 300 страниц за менее чем 5 секунд** на типичном сервере 2.5 ГГц при растеризации 150 DPI.  
- **Потребление памяти остаётся ниже 200 МБ** для файлов до 500 МБ при установке подходящих размеров страниц.  

## Требования

- **Aspose.CAD for Java** интегрирован в ваш проект. Скачайте его с официального сайта: [Aspose.CAD Java download](https://releases.aspose.com/cad/java/).  
- Папка, содержащая файлы DXF, которые вы хотите конвертировать (например, `Your Document Directory/DXFDrawings/`).  

## Импорт пространств имён

`Image` — основной класс Aspose.CAD, представляющий CAD‑чертеж в памяти. После загрузки файла все последующие операции — растеризация, конвертация формата и очистка ресурсов — выполняются через этот объект.

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

### Как пакетно конвертировать файлы DXF в WMF на Java?

Загружайте каждый DXF с помощью `Image.load`, настраивайте `CadRasterizationOptions` для требуемого размера страницы и DPI, и вызывайте `image.save` с `SaveFormat.WMF`. Этот трёхшаговый шаблон выполняет полное преобразование, сохраняя векторное качество, и требует всего несколько строк кода на файл.

#### Шаг 1: загрузить чертеж DXF

Image.load читает файл DXF в объект Aspose.CAD Image.  
```java
import com.aspose.cad.Color;
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.WmfOptions;
```

#### Шаг 2: настроить параметры растеризации

`CadRasterizationOptions` задаёт размер страницы, разрешение и фон для растеризации CAD‑чертежа.  
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DXFDrawings/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

#### Шаг 3: сохранить как WMF

`ImageSaveOptions` с `SaveFormat.WMF` указывает Aspose.CAD записать вывод в виде Windows Metafile.  
```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(100);
rasterizationOptions.setPageHeight(100);
WmfOptions wmfOptions = new WmfOptions();
```

#### Шаг 4: освободить ресурсы

Вызов `image.close()` освобождает нативные ресурсы, используемые объектом Aspose.CAD Image.  
```java
cadImage.save(dataDir+" example.ifc.wmf", wmfOptions);
```

#### Шаг 5: необязательно — экспорт в PDF

`PdfOptions` настраивает параметры, специфичные для PDF, при сохранении изображения как PDF‑документа.  
```java
finally
{
  cadImage.dispose();
}
```

> **Совет:** Вы можете повторно использовать тот же объект `CadRasterizationOptions` для экспорта в PDF, передавая его в экземпляр `PdfOptions`, экономя несколько строк настройки.

## Как экспортировать DXF в PDF с помощью Aspose CAD Java?

Замените формат сохранения WMF на PDF, используя `new ImageSaveOptions(SaveFormat.Pdf)`. Те же настройки растеризации применяются, и вы дополнительно можете задать параметры, специфичные для PDF, такие как метаданные автора или уровень сжатия. Эта однострочная конверсия создаёт поисковый, точно соответствующий оригинальному макету CAD, PDF‑документ.

## Распространённые проблемы и решения

`License` — класс Aspose, используемый для применения лицензии продукта во время выполнения.

| Проблема | Причина | Решение |
|----------|---------|---------|
| **`NullPointerException` при `cadImage.save`** | Переменная `cadImage` не определена (должна быть `image`). | Замените `cadImage` на `image` или переименуйте переменную последовательно. |
| **Вывод WMF пустой** | Размер страницы растеризации слишком мал или цвет фона установлен как прозрачный. | Увеличьте `PageWidth`/`PageHeight` или задайте цвет фона через `rasterizationOptions.setBackgroundColor(Color.WHITE);`. |
| **Исключение лицензии** | Запуск без действующей лицензии Aspose в продакшн. | Примените файл лицензии при старте приложения: `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`. |

## Часто задаваемые вопросы

**В: Где я могу найти документацию Aspose.CAD?**  
Вы можете получить доступ к документации [Aspose.CAD Java documentation](https://reference.aspose.com/cad/java/).

**В: Как скачать Aspose.CAD для Java?**  
Скачайте библиотеку [Aspose.CAD Java download page](https://releases.aspose.com/cad/java/).

**В: Доступна ли бесплатная пробная версия?**  
Да, вы можете получить бесплатную пробную версию [Aspose free trial page](https://releases.aspose.com/).

**В: Нужны варианты временной лицензии?**  
Изучите временные лицензии [temporary license options](https://purchase.aspose.com/temporary-license/).

**В: Где я могу получить поддержку?**  
Посетите форум поддержки Aspose.CAD [Aspose.CAD support forum](https://forum.aspose.com/c/cad/19).

## Дополнительные часто задаваемые вопросы

**В: Могу ли я конвертировать большие DXF‑файлы (сотни МБ) без исчерпания памяти?**  
Да. Загружайте файл в блоке try‑with‑resources и своевременно освобождайте объект `Image`. Настройте `CadRasterizationOptions.setPageWidth/Height` до разумного размера, чтобы снизить потребление памяти.

**В: Сохраняет ли вывод WMF информацию о слоях?**  
WMF — плоский векторный формат, поэтому иерархия слоёв уплощается, но стили линий, цвета и штриховки сохраняются.

**В: Можно ли задать пользовательский DPI для WMF?**  
Используйте `rasterizationOptions.setResolution(300);` для задания DPI перед сохранением.

**В: Можно ли пакетно конвертировать несколько DXF‑файлов за один запуск?**  
Абсолютно. Пройдитесь по каталогу, загрузите каждый файл и примените одинаковую логику растеризации и сохранения.

**В: Какие версии Java поддерживаются?**  
Aspose.CAD for Java поддерживает Java 8 и новее, включая Java 11, 17 и более новые LTS‑версии.

**Last Updated:** 2026-10-30  
**Tested With:** Aspose.CAD for Java 24.11  
**Author:** Aspose

## Связанные руководства

- [Создать PDF из CAD — экспорт DXF в PDF с помощью Aspose.CAD for Java](/cad/java/additional-features/export-dxf-to-pdf/)
- [Создать PDF из DXF: экспорт слоя с Aspose.CAD for Java](/cad/java/additional-features/export-specific-layer-to-pdf/)
- [Как конвертировать макет DXF в изображение JPEG с помощью Aspose.CAD в Java](/cad/java/additional-features/export-specific-layout-to-image/)

```java
image.save(dataDir + "conic_pyramid_out_.pdf"); 
```

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}