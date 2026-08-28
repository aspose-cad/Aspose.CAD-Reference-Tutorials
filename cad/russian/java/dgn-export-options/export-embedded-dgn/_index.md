---
date: 2026-06-14
description: Узнайте, как экспортировать CAD в PDF и конвертировать DGN в PDF с помощью
  Aspose.CAD for Java. Пошаговое руководство для разработчиков Java.
keywords:
- export cad to pdf
- convert dwg to pdf
- convert dgn to pdf
- java convert cad pdf
- batch convert dgn pdf
linktitle: Экспорт встроенного DGN
schemas:
- author: Aspose
  dateModified: '2026-06-14'
  description: Learn how to export CAD to PDF and convert DGN to PDF using Aspose.CAD
    for Java. Step‑by‑step guide for Java developers.
  headline: Export CAD to PDF – Export Embedded DGN with Aspose.CAD for Java
  type: TechArticle
- description: Learn how to export CAD to PDF and convert DGN to PDF using Aspose.CAD
    for Java. Step‑by‑step guide for Java developers.
  name: Export CAD to PDF – Export Embedded DGN with Aspose.CAD for Java
  steps:
  - name: Set Up Input and Output Paths
    text: Define the directory that contains your source file and specify the DWG
      that holds the embedded DGN.
  - name: Load DWG File
    text: '`Image` loads the DWG and automatically detects any embedded DGN data,
      exposing it for further processing.'
  - name: Configure Rasterization Options
    text: Select which layout(s) you want to include in the PDF. In this example we
      export only the **Model** layout, which is the most common view for engineering
      drawings.
  - name: Configure PDF Options
    text: Attach the rasterization settings to the PDF export options so that the
      final document respects the chosen layout and DPI.
  - name: Save PDF File
    text: Finally, write the PDF to disk using the configured options. The `save`
      method writes the configured image to the target file format on disk.
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD for Java is a commercial library. You can obtain a license
      from [here](https://purchase.aspose.com/buy).
    question: Can I use Aspose.CAD for Java in a commercial project?
  - answer: Yes, you can access a free trial of Aspose.CAD for Java [here](https://releases.aspose.com/).
    question: Is there a free trial available?
  - answer: You can seek support from the Aspose.CAD community on the [forum](https://forum.aspose.com/c/cad/19).
    question: How can I get support for Aspose.CAD for Java?
  - answer: You can obtain a temporary license [here](https://purchase.aspose.com/temporary-license/).
    question: What if I need a temporary license?
  - answer: The documentation is available [here](https://reference.aspose.com/cad/java/).
    question: Where can I find the official documentation?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Экспорт CAD в PDF – Экспорт встроенного DGN с Aspose.CAD for Java
url: /ru/java/dgn-export-options/export-embedded-dgn/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Экспорт CAD в PDF – экспорт встроенного DGN с помощью Aspose.CAD for Java

## Введение

В этом руководстве вы узнаете **как экспортировать CAD в PDF**, преобразуя встроенный файл DGN в PDF‑документ высокого качества с помощью Aspose.CAD for Java. Aspose.CAD — мощная библиотека, предоставляющая Java‑разработчикам полный контроль над обработкой CAD‑файлов, будь то **конвертация DGN в PDF**, **конвертация DWG в PDF** или просто рендеринг чертежей в другие форматы. Следуйте пошаговому руководству ниже, и вы сможете интегрировать эту возможность в свои приложения за считанные минуты.

## Быстрые ответы
- **Что означает «экспорт CAD в PDF»?** Преобразует CAD‑чертежи (DWG, DGN и т.д.) в PDF‑файлы, сохраняя векторное качество.  
- **Какая библиотека используется?** Aspose.CAD for Java.  
- **Нужна ли лицензия?** Для продакшн‑использования лицензия обязательна; доступна бесплатная пробная версия.  
- **Какие основные требования?** Среда разработки Java и JAR‑файл Aspose.CAD for Java.  
- **Можно ли настроить вывод?** Да — можно выбирать макеты, задавать параметры растеризации и управлять настройками PDF.

## Что такое «экспорт CAD в PDF»?

Экспорт CAD в PDF преобразует нативный CAD‑чертеж (DWG, DGN и т.д.) в PDF‑файл, сохраняющий исходную векторную геометрию, слои и макет, позволяя любому пользователю просматривать, печатать или делиться дизайном без CAD‑программ. Такое преобразование создает кроссплатформенный документ, выглядящий одинаково при любом масштабе, что делает его идеальным для совместной работы и архивирования.

## Почему стоит использовать Aspose.CAD for Java для конвертации DGN в PDF?

Aspose.CAD for Java предоставляет чисто Java‑решение, устраняющее необходимость во внешних CAD‑инструментах, гарантирует точную векторную точность получаемых PDF и предлагает обширные параметры настройки, такие как выбор макета, управление DPI и встраивание шрифтов, что делает его подходящим как для простых, так и для корпоративных задач конвертации.

- **Отсутствие внешних зависимостей** — работает полностью на Java на любой ОС.  
- **Сохранение векторных данных** — PDF остаются чёткими при любом увеличении.  
- **Тонкая настройка** — выбор конкретных макетов, установка DPI растеризации и встраивание шрифтов.  
- **Готовность к корпоративному использованию** — поддержка файлов до **2 GB**, пакетная обработка тысяч чертежей и гибкая лицензия.  

## Предварительные требования

Прежде чем приступить, убедитесь, что у вас есть следующее:

- **Среда разработки Java** — установлен и настроен JDK 8 или выше.  
- **Aspose.CAD for Java** — скачайте последнюю версию JAR файла [здесь](https://releases.aspose.com/cad/java/).  

## Импорт пакетов

Операторы `import` импортируют необходимые классы Aspose.CAD.  
`Image` — основной класс, представляющий любой растеризуемый CAD‑файл, а `PdfOptions` и `RasterizationOptions` позволяют точно настроить вывод PDF.  
`CadRasterizationOptions` задаёт параметры растеризации, такие как DPI, размер страницы и макет для рендеринга CAD.

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Как экспортировать CAD в PDF с помощью Aspose.CAD for Java?

Процесс начинается с загрузки DWG‑файла, содержащего встроенный DGN, затем задаются параметры растеризации для определения разрешения и макета вывода, эти параметры привязываются к объекту `PdfOptions`, и, наконец, вызывается метод `save` для создания PDF. Такой подход обеспечивает высококачественный, сохраняющий векторную точность результат при минимальном объёме кода.

Ниже представлена чёткая пошаговая инструкция, показывающая, как преобразовать встроенный DGN‑файл (хранящийся внутри DWG) в PDF.

### Шаг 1: Настройка путей ввода и вывода

Определите каталог, содержащий исходный файл, и укажите DWG, в котором находится встроенный DGN.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
```

### Шаг 2: Загрузка DWG‑файла

`Image` загружает DWG и автоматически обнаруживает любые встроенные данные DGN, делая их доступными для дальнейшей обработки.

```java
Image objImage = Image.load(fileName);
```

### Шаг 3: Настройка параметров растеризации

Выберите, какие макеты включить в PDF. В этом примере экспортируется только макет **Model**, который является наиболее распространённым представлением инженерных чертежей.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setLayouts(new String[] {"Model"});
```

### Шаг 4: Настройка параметров PDF

Привяжите настройки растеризации к параметрам экспорта PDF, чтобы окончательный документ учитывал выбранный макет и DPI.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Шаг 5: Сохранение PDF‑файла

Наконец, запишите PDF на диск, используя сконфигурированные параметры. Метод `save` сохраняет настроенное изображение в целевой формат файла.

```java
objImage.save(dataDir + "BlockRefDgn.pdf", pdfOptions);
```

## Конвертация DWG в PDF — дополнительный совет

Если ваш исходный файл — обычный DWG (без встроенного DGN), вы можете повторно использовать тот же код — просто измените `fileName`, указав путь к нужному DWG. Параметры растеризации и PDF остаются теми же, обеспечивая единообразный процесс **конвертации DWG в PDF**.

## Распространённые проблемы и их решения

| Проблема | Причина | Решение |
|----------|---------|---------|
| **Пустой PDF‑файл** | Несоответствие имени макета | Убедитесь, что имя макета, переданное в `setLayouts`, точно совпадает с именем макета в исходном файле (учитывается регистр). |
| **Исключение лицензии** | Использование пробной версии без лицензии | Примените действующую лицензию Aspose.CAD перед загрузкой изображения (`License license = new License(); license.setLicense("Aspose.CAD.lic");`). |
| **Файл не найден** | Неправильный путь `dataDir` | Используйте абсолютный путь или убедитесь, что относительный путь корректен относительно рабочей директории проекта. |
| **Низкое разрешение графики** | DPI растеризации по умолчанию низкое | Установите `rasterizationOptions.setResolution(300)` или скорректируйте `setPageWidth/Height` для увеличения DPI. |

## Часто задаваемые вопросы

**В: Можно ли использовать Aspose.CAD for Java в коммерческом проекте?**  
О: Да, Aspose.CAD for Java — коммерческая библиотека. Приобрести лицензию можно [здесь](https://purchase.aspose.com/buy).

**В: Доступна ли бесплатная пробная версия?**  
О: Да, бесплатную пробную версию Aspose.CAD for Java можно получить [здесь](https://releases.aspose.com/).

**В: Как получить поддержку по Aspose.CAD for Java?**  
О: Обратитесь к сообществу Aspose.CAD на [форуме](https://forum.aspose.com/c/cad/19).

**В: Где взять временную лицензию?**  
О: Временную лицензию можно получить [здесь](https://purchase.aspose.com/temporary-license/).

**В: Где найти официальную документацию?**  
О: Документация доступна [здесь](https://reference.aspose.com/cad/java/).

## Заключение

Теперь вы знаете, как **экспортировать CAD в PDF**, в частности, как **конвертировать DGN в PDF** и даже **конвертировать DWG в PDF** с помощью Aspose.CAD for Java. Следуя приведённым шагам, вы сможете внедрить бесшовную конвертацию CAD‑в‑PDF в любое Java‑решение, предоставляя пользователям PDFs высокого качества без необходимости в дополнительном CAD‑ПО.

---

**Последнее обновление:** 2026-06-14  
**Тестировано с:** Aspose.CAD for Java 24.12  
**Автор:** Aspose

{{< blocks/products/products-backtop-button >}}

## Связанные руководства

- [Экспорт DGN в DWG с Aspose.CAD for Java – Руководство](/cad/java/dgn-export-options/)
- [Лёгкий экспорт DGN в AutoCAD PDF с Aspose.CAD for Java](/cad/java/dgn-export-options/exporting-dgn-to-pdf/)
- [dwg to pdf java – Экспорт CAD в PDF с Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}