---
date: 2026-05-20
description: Узнайте, как конвертировать DWG в PDF, переопределяя автоматическое определение
  кодовой страницы с помощью Aspose.CAD for Java. Включает шаги экспорта dwg в pdf,
  советы по кодировке и устранению неполадок.
keywords:
- convert dwg pdf
- export dwg to pdf
- Aspose.CAD Java
linktitle: Переопределить автоматическое определение кодовой страницы в файлах DWG
schemas:
- author: Aspose
  dateModified: '2026-05-20'
  description: Learn how to convert DWG to PDF while overriding automatic code page
    detection using Aspose.CAD for Java. Includes export dwg to pdf steps, encoding
    tips, and troubleshooting.
  headline: Convert DWG to PDF – Override Code Page Detection in Java
  type: TechArticle
- description: Learn how to convert DWG to PDF while overriding automatic code page
    detection using Aspose.CAD for Java. Includes export dwg to pdf steps, encoding
    tips, and troubleshooting.
  name: Convert DWG to PDF – Override Code Page Detection in Java
  steps:
  - name: Set Up the Java Project
    text: Create a Maven or Gradle project and add the Aspose.CAD JAR to the classpath.
      This ensures the IDE can resolve the imported classes and that the runtime can
      locate the library.
  - name: Load the DWG File with a Specified Code Page
    text: Tell Aspose.CAD which encoding to use and whether to attempt recovery of
      malformed CIF/MIF data.
  - name: Export the CAD Image to PDF
    text: With the correct code page applied, you can safely export the drawing. The
      `PdfOptions` object lets you fine‑tune the PDF output (compression, rasterization,
      etc.).
  - name: Verify Success
    text: A simple console message confirms that the process completed without exceptions.
      You can repeat these steps for multiple DWG files, adjusting the source path
      and output name as needed.
  type: HowTo
- questions:
  - answer: It forces Aspose.CAD to use a specific character encoding instead of guessing.
    question: What does “override code page” mean?
  - answer: Yes – after setting the correct code page, you can save the CAD image
      as PDF.
    question: Can I export DWG directly to PDF?
  - answer: '`CodePages.Japanese` and `MifCodePages.Japanese` are the right choices.'
    question: Which encoding works for Japanese text?
  - answer: A commercial license is required; a temporary license is available for
      testing.
    question: Do I need a license for production use?
  - answer: Any recent version that supports `LoadOptions` and `PdfOptions`.
    question: What version of Aspose.CAD is needed?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Конвертировать DWG в PDF – Переопределить определение кодовой страницы в Java
url: /ru/java/dwg-file-operations/override-code-page-detection/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Преобразование DWG в PDF – Переопределение обнаружения кодовой страницы в Java

В этом полном руководстве вы узнаете **как преобразовать DWG в PDF**, переопределяя автоматическое определение кодовой страницы, которое может искажать текст. Aspose.CAD for Java предоставляет точный контроль над кодировкой символов, позволяя восстанавливать повреждённые данные CIF/MIF и генерировать надёжный PDF‑вывод. Независимо от того, создаёте ли вы пакетный конвертер или добавляете обработку CAD в более крупный Java‑сервис, нижеописанные шаги проведут вас через весь рабочий процесс — от настройки проекта до проверки результата.

## Быстрые ответы
- **Что означает «переопределить кодовую страницу»?** Это заставляет Aspose.CAD использовать конкретную кодировку символов вместо угадывания.
- **Можно ли экспортировать DWG напрямую в PDF?** Да — после установки правильной кодовой страницы вы можете сохранить изображение CAD как PDF.
- **Какая кодировка подходит для японского текста?** `CodePages.Japanese` и `MifCodePages.Japanese` являются правильным выбором.
- **Нужна ли лицензия для использования в продакшене?** Требуется коммерческая лицензия; временная лицензия доступна для тестирования.
- **Какая версия Aspose.CAD необходима?** Любая современная версия, поддерживающая `LoadOptions` и `PdfOptions`.

## Что такое «экспорт CAD в PDF»?
Экспорт CAD в PDF преобразует векторный чертёж DWG в универсально просматриваемый документ PDF фиксированного макета. Конверсия сохраняет все геометрические объекты, линии, слои и встроенный текст, одновременно уплощая чертёж в формат, который легко делиться, печатать, архивировать или встраивать в другие приложения без необходимости установки CAD‑программного обеспечения.

## Почему переопределять автоматическое обнаружение кодовой страницы?
Ручное указание кодовой страницы гарантирует правильную интерпретацию байтов текста, устраняя искажённые символы, которые часто появляются, когда автоопределение Aspose.CAD выбирает неверную устаревшую кодировку. Это особенно важно для нелатинских скриптов, таких как японский, кириллица или арабский, и обеспечивает соответствие экспортированного PDF оригинальному дизайну.

## Предварительные требования
- **Java Development Environment** – JDK 8+ и ваша предпочтительная IDE.  
- **Aspose.CAD for Java** – Скачайте библиотеку с официального сайта [here](https://releases.aspose.com/cad/java/).  
- **DWG Sample File** – Используйте предоставленный `SimpleEntities.dwg` или любой другой DWG, который нужно конвертировать.

## Импорт пакетов
Классы `Document`, `LoadOptions` и `PdfOptions` являются ядром процесса конвертации.

Класс `Document` представляет чертёж CAD в памяти, предоставляя методы загрузки, манипуляции и сохранения файла в различных форматах.  
Класс `LoadOptions` позволяет указать кодовую страницу и параметры восстановления при загрузке DWG‑файла.  
Класс `PdfOptions` управляет настройками PDF, такими как сжатие, растеризация и метаданные.

В вашем Java‑проекте импортируйте необходимые классы Aspose.CAD:

```java
import com.aspose.cad.CodePages;
import com.aspose.cad.Image;
import com.aspose.cad.LoadOptions;
import com.aspose.cad.MifCodePages;
import com.aspose.cad.fileformats.cad.CadImage;
```

## Как преобразовать DWG в PDF с переопределением кодовой страницы?
Загрузите DWG‑файл с помощью `LoadOptions`, указав точную кодовую страницу, затем вызовите метод `save` у полученного `CadImage`, передав сконфигурированный экземпляр `PdfOptions`. Такой двухшаговый подход гарантирует правильную интерпретацию текста и сохранение оригинального качества чертежа, слоёв и векторной точности в сгенерированном PDF.

### Шаг 1: Настройка проекта Java
Создайте проект Maven или Gradle и добавьте JAR‑файл Aspose.CAD в classpath. Это обеспечит возможность IDE разрешать импортированные классы и позволит среде выполнения находить библиотеку.

### Шаг 2: Загрузка DWG‑файла с указанной кодовой страницей
Укажите Aspose.CAD, какую кодировку использовать, и следует ли пытаться восстановить повреждённые данные CIF/MIF.

```java
String SourceDir = "Your Document Directory";
String dwgPathToFile = SourceDir + "SimpleEntites.dwg";
LoadOptions opts = new LoadOptions();
opts.setSpecifiedEncoding(CodePages.Japanese);
opts.setSpecifiedMifEncoding(MifCodePages.Japanese);
opts.setRecoverMalformedCifMif(false);
CadImage cadImage = (CadImage) Image.load(dwgPathToFile, opts);
```

### Шаг 3: Экспорт изображения CAD в PDF
С применённой правильной кодовой страницей вы можете безопасно экспортировать чертёж. Объект `PdfOptions` позволяет тонко настроить вывод PDF (сжатие, растеризацию и т.д.).

```java
// Perform export or other operations with cadImage
// For example, exporting to PDF
PdfOptions pdfOptions = new PdfOptions();
cadImage.save("output.pdf", pdfOptions);
```

### Шаг 4: Проверка успешности
Простое сообщение в консоли подтверждает, что процесс завершён без исключений.

```java
System.out.println("OverrideAutomaticCodePageDetectionDwg executed successfully");
```

Вы можете повторять эти шаги для нескольких DWG‑файлов, при необходимости меняя путь к исходному файлу и имя выходного файла.

## Распространённые проблемы и решения
- **По‑прежнему появляются мусорные символы:** Проверьте, что `specifiedEncoding` соответствует кодовой странице оригинального DWG. При необходимости используйте другой элемент перечисления `CodePages`.  
- **`NullPointerException` при `cadImage.save`:** Убедитесь, что DWG‑файл загружается корректно; проверьте путь и права доступа к файлу.  
- **Размер PDF велик:** Включите сжатие в `PdfOptions` (например, `pdfOptions.setCompress(true)`), чтобы уменьшить размер файла без потери качества.

## Часто задаваемые вопросы

**Q1: Совместим ли Aspose.CAD со всеми версиями файлов DWG?**  
A1: Aspose.CAD поддерживает более 30 версий DWG, включая AutoCAD 2018 и более ранние выпуски.

**Q2: Можно ли использовать Aspose.CAD в коммерческих проектах?**  
A2: Да, для продакшн‑использования требуется коммерческая лицензия. Приобрести лицензию можно [here](https://purchase.aspose.com/buy).

**Q3: Есть ли ограничения в бесплатной пробной версии?**  
A1: Пробная версия накладывает ограничения на размер и набор функций; см. официальную документацию для подробностей.

**Q4: Как получить поддержку по Aspose.CAD?**  
A4: Посетите сообщество [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) для получения помощи и обсуждения.

**Q5: Доступна ли временная лицензия для тестовых целей?**  
A5: Да, временную лицензию можно запросить [here](https://purchase.aspose.com/temporary-license/).

---

**Последнее обновление:** 2026-05-20  
**Тестировано с:** Aspose.CAD for Java 24.11 (latest at time of writing)  
**Автор:** Aspose

## Связанные руководства

- [Экспорт DWG в PDF и преобразование CAD‑чертежей – руководство Aspose.CAD Java](/cad/java/cad-drawing-conversion/)
- [Экспорт конкретного макета DWG в PDF с использованием Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Экспорт DWG в PDF или растр с помощью Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-wrap-class >}}