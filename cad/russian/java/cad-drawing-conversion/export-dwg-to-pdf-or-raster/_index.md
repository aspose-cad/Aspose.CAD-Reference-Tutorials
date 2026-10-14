---
date: 2026-10-14
description: Узнайте, как Java CAD библиотека Aspose.CAD для Java может быстро и точно
  экспортировать DWG в PDF или растровые изображения.
keywords:
- export dwg pdf
- high quality pdf
- dwg to pdf tutorial
- aspose cad java
- java cad library
lastmod: 2026-10-14
linktitle: Экспорт DWG в PDF и растровые изображения
og_description: Быстрый экспорт DWG в PDF с помощью Aspose.CAD для Java. Узнайте о
  высококачественном преобразовании в PDF, параметрах растрового вывода и лицензировании
  в этом пошаговом руководстве.
og_image_alt: Tutorial showing Java code to convert DWG drawings to PDF and raster
  formats with Aspose.CAD
og_title: Экспорт DWG в PDF и растровые изображения с использованием Java CAD библиотеки
  Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-10-14'
  description: Learn how the Java CAD library Aspose.CAD for Java can export DWG to
    PDF or raster images quickly and accurately.
  headline: Export DWG PDF and raster images using Java CAD library Aspose.CAD
  type: TechArticle
- description: Learn how the Java CAD library Aspose.CAD for Java can export DWG to
    PDF or raster images quickly and accurately.
  name: Export DWG PDF and raster images using Java CAD library Aspose.CAD
  steps:
  - name: Load the DWG file
    text: First, load your DWG drawing using the `Image` class. This creates an in‑memory
      representation that Aspose.CAD can work with.
  - name: Determine unit type
    text: Understanding whether the drawing uses metric or imperial units is essential
      for correct scaling. The helper method `IsMetric` (implementation omitted for
      brevity) returns a boolean flag.
  - name: Set rasterization options
    text: The `CadRasterizationOptions` class defines rasterization parameters such
      as DPI, page size, and unit conversion. Based on the unit system, configure
      page size, scaling, and the target unit type. These options drive how the DWG
      is rasterized before being wrapped into a PDF.
  - name: Configure PDF options (pdf options cad)
    text: The `PdfOptions` class specifies PDF‑specific settings, including compression
      and metadata. Create a `PdfOptions` instance and attach the rasterization settings.
      This tells Aspose.CAD how to embed the rasterized content into the final PDF.
  - name: Save as PDF
    text: The `save` method writes the image to the given file path using the supplied
      options. Finally, export the drawing to a PDF file. The `save` method takes
      the output path and the configured `PdfOptions`. When the code finishes, you’ll
      find **Saved.pdf** in your `DWGDrawings` folder, ready for distribu
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD for Java seamlessly integrates with popular Java frameworks
      such as Spring, Jakarta EE, and Android.
    question: Can I use Aspose.CAD for Java with other Java frameworks?
  - answer: Yes, you can obtain a temporary license **[obtain a temporary license](https://purchase.aspose.com/temporary-license/)**.
    question: Is a temporary license available for Aspose.CAD for Java?
  - answer: Visit the **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)** for
      assistance from the community and Aspose engineers.
    question: Where can I find support for Aspose.CAD for Java?
  - answer: You can purchase a license **[purchase a license](https://purchase.aspose.com/buy)**.
    question: How can I purchase a license for Aspose.CAD for Java?
  - answer: Aspose.CAD for Java supports both metric and imperial units, automatically
      detecting the drawing’s unit system.
    question: What units does Aspose.CAD for Java support?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- export dwg
- aspose.cad
- java cad conversion
title: Экспорт DWG в PDF и растровые изображения с использованием Java CAD библиотеки
  Aspose.CAD
url: /ru/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Экспорт DWG PDF и растровых изображений с помощью Java CAD библиотеки Aspose.CAD

## Введение

Экспорт DWG в PDF является частой потребностью инженеров, архитекторов и всех, кому нужно делиться CAD‑чертежами, не раскрывая исходный формат файла. С **Aspose.CAD for Java** вы можете **export dwg pdf** — или растровые изображения — всего в несколько строк кода Java, сохраняя векторную точность и точность макета. Этот учебник проведёт вас через загрузку DWG‑файла, настройку растеризации и сохранение результата в виде PDF высокого качества или изображения. Вы также увидите, почему Aspose.CAD является предпочтительной Java CAD библиотекой для надёжного кросс‑платформенного преобразования.

Для руководства, сосредоточенного только на конвертации в PDF, см. [Учебник по экспорту DWG в PDF](/java/cad-drawing-conversion/export-dwg-to-pdf/).

## Быстрые ответы
- **Что охватывает этот учебник?** Экспорт файлов DWG в PDF или растровые изображения с использованием Aspose.CAD for Java.  
- **Нужна ли лицензия?** Доступна бесплатная временная лицензия для оценки; полная лицензия требуется для продакшн‑использования.  
- **Какая версия Java поддерживается?** Любая среда выполнения Java 8+ совместима с последним Aspose.CAD Java API.  
- **Могу ли я конвертировать DWG в другие форматы изображений?** Да — те же параметры растеризации позволяют выводить PNG, JPEG, BMP и т.д.  
- **Сколько времени занимает конвертация?** Обычно менее секунды для стандартных чертежей; более крупные файлы могут занимать несколько секунд.

## Почему Java CAD библиотека является лучшим выбором для конвертации DWG?

Aspose.CAD for Java — лучший выбор, потому что предоставляет чистую Java‑реализацию, не требующую нативных DLL, автоматически определяет метрические или имперские единицы, выдаёт растровый вывод до 1200 DPI и генерирует PDF, сохраняющие векторные данные, без внешних зависимостей. Библиотека также предлагает гибкую модель лицензирования, позволяющую начать с временной лицензии и масштабировать до корпоративного использования.

## Что такое «export dwg to pdf»?

`Export dwg pdf` — процесс преобразования исходного DWG‑чертежа в PDF‑документ с сохранением векторных данных, слоёв и масштабирования. Такое преобразование создаёт независимый от устройства файл, который можно просматривать на любой платформе без необходимости в AutoCAD. Поскольку PDF сохраняет векторную информацию, текст остаётся поисковым, а графика — чёткой при любом масштабе, что делает его идеальным для документации, проверки клиентом и архивного хранения.

## Почему использовать Aspose.CAD Java для этой конвертации?

Вам следует использовать Aspose.CAD Java, потому что библиотека обрабатывает преобразование единиц, растеризацию и встраивание PDF внутри, устраняя необходимость в сторонних инструментах или сложных конвейерах командной строки. Его API разработан для разработчиков: один объект `Image` представляет чертеж, а несколько объектов конфигурации позволяют точно настроить DPI, размер страницы и сжатие. Результат — согласованный, повторяемый вывод на Windows, Linux и macOS.

## Требования

Перед тем как приступить к коду, убедитесь, что у вас есть:

- Базовые знания программирования на Java.  
- Установленную библиотеку Aspose.CAD for Java. Если вы ещё не скачали её, получите её **[скачать Aspose.CAD for Java](https://releases.aspose.com/cad/java/)**.  
- Файл DWG для тестирования — в этом руководстве используется пример **Bottom_plate.dwg**.

## Импорт пространств имён

В вашем Java‑проекте импортируйте необходимые классы, чтобы начать конвертацию:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## Пошаговое руководство

### Шаг 1: Загрузка DWG‑файла

Сначала загрузите ваш DWG‑чертеж, используя класс `Image`. Это создаёт представление в памяти, с которым может работать Aspose.CAD.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

### Шаг 2: Определение типа единиц

Понимание того, использует ли чертеж метрические или имперские единицы, необходимо для правильного масштабирования. Вспомогательный метод `IsMetric` (реализация опущена для краткости) возвращает логический флаг.

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

### Шаг 3: Установка параметров растеризации

Класс `CadRasterizationOptions` определяет параметры растеризации, такие как DPI, размер страницы и преобразование единиц. В зависимости от системы единиц настройте размер страницы, масштабирование и целевой тип единиц. Эти параметры определяют, как DWG будет растеризован перед упаковкой в PDF.

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

### Шаг 4: Настройка параметров PDF (pdf options cad)

Класс `PdfOptions` задаёт специфические для PDF настройки, включая сжатие и метаданные. Создайте экземпляр `PdfOptions` и прикрепите к нему параметры растеризации. Это указывает Aspose.CAD, как встроить растеризованное содержимое в конечный PDF.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

### Шаг 5: Сохранение в PDF

Метод `save` записывает изображение в указанный путь файла, используя предоставленные параметры. В конце экспортируйте чертеж в PDF‑файл. Метод `save` принимает путь вывода и настроенный `PdfOptions`.

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

После завершения кода вы найдёте **Saved.pdf** в папке `DWGDrawings`, готовый к распространению или архивированию.

## Как конвертировать DWG в растровые изображения с помощью Java CAD библиотеки?

Вы можете конвертировать DWG в растровые форматы, заменив `PdfOptions` на класс параметров, специфичный для растра, такой как `PngOptions` или `JpegOptions`. Повторно используйте тот же экземпляр `CadRasterizationOptions`, измените формат вывода и вызовите метод `save` с новым объектом параметров. Такой подход позволяет генерировать PNG, JPEG, BMP или TIFF файлы, изменив лишь одну строку кода, сохраняя последовательность рабочего процесса.

## Как сгенерировать PDF DWG с использованием PDF‑опций CAD?

Приведённый выше пример уже **generates pdf dwg** вывод. Чтобы точно настроить размер PDF, включите сжатие, вызвав `pdfOptions.setCompress(true)`. Вы также можете встраивать пользовательские метаданные, задавать версию PDF или добавлять защиту паролем через дополнительные свойства `PdfOptions`. Эти настройки дают вам полный контроль над конечным PDF, не выходя из Java‑кода.

## Распространённые проблемы и советы

- **Неправильный размер страницы** – Проверьте логику преобразования единиц; несоответствующие коэффициенты могут привести к слишком большим страницам.  
- **Отсутствие шрифтов или толщин линий** – Убедитесь, что DWG ссылается на все внешние ресурсы перед конвертацией.  
- **Производительность при больших чертежах** – Увеличивайте параметр `DPI` в `CadRasterizationOptions` только когда требуется более высокое качество; более низкий DPI ускоряет обработку.  
- **Вопросы лицензирования** – Для оценки вы можете использовать **temporary license Aspose**; полная лицензия требуется для продакшн‑развёртываний.

## Часто задаваемые вопросы

**В: Могу ли я использовать Aspose.CAD for Java с другими Java‑фреймворками?**  
**О:** Да, Aspose.CAD for Java без проблем интегрируется с популярными Java‑фреймворками, такими как Spring, Jakarta EE и Android.

**В: Доступна ли временная лицензия для Aspose.CAD for Java?**  
**О:** Да, вы можете получить временную лицензию **[получить временную лицензию](https://purchase.aspose.com/temporary-license/)**.

**В: Где я могу найти поддержку для Aspose.CAD for Java?**  
**О:** Посетите **[форум Aspose.CAD](https://forum.aspose.com/c/cad/19)** для получения помощи от сообщества и инженеров Aspose.

**В: Как я могу приобрести лицензию для Aspose.CAD for Java?**  
**О:** Вы можете приобрести лицензию **[приобрести лицензию](https://purchase.aspose.com/buy)**.

**В: Какие единицы поддерживает Aspose.CAD for Java?**  
**О:** Aspose.CAD for Java поддерживает как метрические, так и имперские единицы, автоматически определяя систему единиц чертежа.

**В: Могу ли я конвертировать DWG в другие форматы изображений (например, PNG, JPEG) с помощью того же API?**  
**О:** Конечно. Замените `PdfOptions` на соответствующие параметры растрового изображения (например, `PngOptions`) и повторно используйте тот же `CadRasterizationOptions`.

## Заключение

В этом учебнике показано, как **export dwg pdf** и растровые изображения с помощью **java cad library** Aspose.CAD for Java. Следуя пошаговому руководству, вы сможете интегрировать надёжную CAD‑конвертацию в любое Java‑приложение, будь то PDF‑документы для документации или растровые изображения для веб‑отображения. Чистая Java‑природа библиотеки, высококачественный вывод и гибкое лицензирование делают её отличным выбором как для небольших утилит, так и для масштабных корпоративных конвейеров.

---

**Последнее обновление:** 2026-10-14  
**Тестировано с:** Aspose.CAD for Java 24.10  
**Автор:** Aspose

## Связанные учебники

- [Экспорт DWG в PDF: конкретный макет с использованием Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Экспорт DWG в PDF в Java – установка размера страницы PDF с Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)
- [Экспорт DWG в PDF с скрытыми линиями – Aspose.CAD for Java](/cad/java/cad-text-and-formatting/support-hidden-lines-in-dwg/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}