---
date: 2026-05-25
description: Узнайте, как экспортировать файлы dgn в изображения JPEG с помощью Aspose.CAD
  for Java. Это пошаговое руководство покажет, как эффективно преобразовать dgn в
  jpeg.
keywords:
- how to export dgn
- convert dgn to jpeg
- java convert cad to image
linktitle: Экспорт DGN в формате AutoCAD в растровый формат изображения
schemas:
- author: Aspose
  dateModified: '2026-05-25'
  description: Learn how to export dgn files to JPEG images with Aspose.CAD for Java.
    This step‑by‑step guide shows you how to convert dgn to jpeg efficiently.
  headline: How to Export DGN to JPEG with Aspose.CAD for Java
  type: TechArticle
- description: Learn how to export dgn files to JPEG images with Aspose.CAD for Java.
    This step‑by‑step guide shows you how to convert dgn to jpeg efficiently.
  name: How to Export DGN to JPEG with Aspose.CAD for Java
  steps:
  - name: '**Aspose.CAD Library** – download the latest JAR from the official site [here](https://releases.aspose.com/cad/java/).
      You can also explore other product releases [here](https://releases.aspose.com/).'
    text: '**Aspose.CAD Library** – download the latest JAR from the official site [here](https://releases.aspose.com/cad/java/).
      You can also explore other product releases [here](https://releases.aspose.com/).'
  - name: '**Java Development Kit (JDK)** – Java 8 or newer installed on your machine.'
    text: '**Java Development Kit (JDK)** – Java 8 or newer installed on your machine.'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or any Java‑compatible editor you prefer.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or any Java‑compatible editor you prefer.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD supports over 30 vector formats, including DWG, DXF, DWF,
      and SVG, enabling a single API for many conversion scenarios.
    question: Can I use Aspose.CAD for Java with other CAD file formats?
  - answer: Yes, you can access a free trial [here](https://releases.aspose.com/).
    question: Is there a free trial available for Aspose.CAD for Java?
  - answer: Refer to the official docs [here](https://reference.aspose.com/cad/java/).
    question: Where can I find documentation for Aspose.CAD for Java?
  - answer: Visit the support forum [here](https://forum.aspose.com/c/cad/19).
    question: How can I get support for Aspose.CAD for Java?
  - answer: You can buy a license [here](https://purchase.aspose.com/buy).
    question: Where can I purchase a license for Aspose.CAD for Java?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Как экспортировать DGN в JPEG с помощью Aspose.CAD for Java
url: /ru/java/dgn-export-options/exporting-dgn-to-raster-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Конвертация Java DGN в JPEG с Aspose.CAD — учебник

## Введение

В этом полном руководстве вы узнаете, **как экспортировать dgn** файлы в изображения JPEG с помощью Aspose.CAD для Java. Независимо от того, создаёте ли вы сервис пакетной обработки или добавляете генерацию предварительного просмотра «на лету» в CAD‑просмотрщик, это учебное пособие проведёт вас через каждый шаг, от загрузки исходного файла до сохранения растрового вывода. Вы также увидите практические советы, позволяющие держать ваш код чистым и производительным.

## Быстрые ответы
- **Какая библиотека нужна?** Aspose.CAD for Java (download [here](https://releases.aspose.com/cad/java/)).
- **Могу ли я конвертировать DGN в JPEG одной строкой?** Да – загрузите с помощью `CadImage.load` и вызовите `save` с `JpegOptions`.
- **Требуется ли лицензия для продакшна?** Да, коммерческая лицензия удаляет водяной знак оценки.
- **Какая версия Java поддерживается?** Java 8 по 17 полностью поддерживаются.
- **Какой максимальный размер DGN я могу обработать?** Файлы до 2 ГБ обрабатываются без загрузки всего файла в память.

## Что такое «как экспортировать dgn»?
*«Как экспортировать dgn»* относится к процессу преобразования файла проекта MicroStation DGN в другой формат, обычно растровое изображение, такое как JPEG, для более простого просмотра или обмена. Эта конверсия позволяет заинтересованным сторонам, не имеющим CAD‑программного обеспечения, просматривать проекты, встраивать изображения в документы или генерировать миниатюры для веб‑галерей, улучшая доступность и сотрудничество между командами.

## Почему использовать Aspose.CAD для Java?
Aspose.CAD поддерживает **более 30 форматов CAD** (включая DGN, DWG, DXF) и может рендерить файлы **до 2 ГБ** без необходимости оригинального CAD‑приложения. Его растровый движок обрабатывает многостраничные чертежи со скоростью **> 50 fps** на стандартном серверном оборудовании, предоставляя высококачественный JPEG‑вывод одним вызовом API.

## Предварительные требования

Before diving in, ensure you have:

1. **Библиотека Aspose.CAD** – скачайте последнюю JAR‑файл с официального сайта [here](https://releases.aspose.com/cad/java/). Вы также можете изучить другие релизы продуктов [here](https://releases.aspose.com/).  
2. **Java Development Kit (JDK)** – установлен Java 8 или новее на вашем компьютере.  
3. **IDE** – IntelliJ IDEA, Eclipse или любой совместимый с Java редактор по вашему выбору.

## Импорт пакетов

In your Java project, import the necessary Aspose.CAD classes:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
```

## Как экспортировать dgn в JPEG с помощью Aspose.CAD в Java?

Класс `CadImage` представляет CAD‑документ, загруженный в память, предоставляя методы для рендеринга и сохранения.

Загрузите ваш DGN‑файл с помощью `CadImage.load("source.dgn")`, настройте `JpegOptions` (включая качество и разрешение), задайте соответствующие `RasterizationOptions`, такие как размеры страницы и цвет фона, и, наконец, вызовите `image.save("output.jpg", jpegOptions)`. Этот трёхшаговый процесс обрабатывает преобразование вектор‑в‑растр, сохраняет толщину линий и записывает высококачественный JPEG‑файл менее чем за секунду для типичных чертежей.

## Шаг 1: Загрузка DGN файла

Класс `CadImage` представляет CAD‑документ, загруженный в память.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
DgnImage dgnImage = (DgnImage) Image.load(dataDir + "Nikon_D90_Camera.dgn");
```

## Шаг 2: Создание объекта JpegOptions

`JpegOptions` определяет параметры, специфичные для вывода JPEG, такие как качество сжатия и разрешение.

```java
ImageOptionsBase options = new JpegOptions();
```

## Шаг 3: Назначение параметров растеризации

`RasterizationOptions` определяет, как векторная графика преобразуется в растр, включая размер страницы, DPI, цвет фона и сглаживание.

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(600);
vectorOptions.setPageHeight(400);
vectorOptions.setNoScaling(true);
vectorOptions.setAutomaticLayoutsScaling(false);
options.setVectorRasterizationOptions(vectorOptions);
```

## Шаг 4: Сохранение преобразованного изображения

Вызов `save` записывает растровое изображение на диск, используя предоставленные вами параметры.

```java
OutputStream outStream = new FileOutputStream(dataDir + "ExportDGNToRasterImage_Out.jpg");
dgnImage.save(outStream, options);
```

### Общие сценарии использования

- **Генерация веб‑предпросмотра** – Преобразуйте инженерные чертежи в легкие JPEG‑миниатюры для быстрого отображения в браузерах.  
- **Пакетный архив** – Автоматизируйте конвертацию тысяч DGN‑файлов в JPEG для долгосрочного хранения без необходимости MicroStation.  
- **Отчётность** – Встраивайте снимки CAD в PDF или HTML‑отчёты напрямую из Java‑кода.

### Распространённые проблемы и решения

| Проблема | Решение |
|----------|---------|
| **Изображение пустое** | Убедитесь, что `RasterizationOptions.setPageWidth/Height` соответствует границам чертежа, и задайте непрозрачный фон. |
| **Низкое качество вывода** | Увеличьте `JpegOptions.setQuality(100)` и задайте более высокое DPI (например, `RasterizationOptions.setResolution(300)`). |
| **Ошибки нехватки памяти** | Используйте `CadImage.load` с `loadOptions.setLoadMode(LoadMode.Memory)`, чтобы потоково обрабатывать большие файлы. |

## Часто задаваемые вопросы

**В: Могу ли я использовать Aspose.CAD для Java с другими форматами CAD?**  
**О:** Да, Aspose.CAD поддерживает более 30 векторных форматов, включая DWG, DXF, DWF и SVG, позволяя использовать один API для множества сценариев конвертации.

**В: Доступна ли бесплатная пробная версия Aspose.CAD для Java?**  
**О:** Да, вы можете получить бесплатную пробную версию [here](https://releases.aspose.com/).

**В: Где я могу найти документацию по Aspose.CAD для Java?**  
**О:** Обратитесь к официальной документации [here](https://reference.aspose.com/cad/java/).

**В: Как я могу получить поддержку по Aspose.CAD для Java?**  
**О:** Посетите форум поддержки [here](https://forum.aspose.com/c/cad/19).

**В: Где я могу приобрести лицензию на Aspose.CAD для Java?**  
**О:** Вы можете купить лицензию [here](https://purchase.aspose.com/buy).

---

**Последнее обновление:** 2026-05-25  
**Тестировано с:** Aspose.CAD 24.11 for Java  
**Автор:** Aspose

## Связанные учебники

- [Легкий экспорт DGN в PDF AutoCAD с Aspose.CAD для Java](/cad/java/dgn-export-options/exporting-dgn-to-pdf/)
- [Экспорт DGN в DWG с Aspose.CAD для Java – учебник](/cad/java/dgn-export-options/)
- [Сохранить CAD как PNG – преобразовать чертеж CAD в растровый формат с помощью Aspose.CAD для Java](/cad/java/cad-drawing-conversion/convert-cad-drawing-to-raster-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}