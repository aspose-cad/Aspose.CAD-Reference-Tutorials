---
date: 2026-06-29
description: Узнайте, как создать PDF из DWG и настроить макет PDF, используя Aspose.CAD
  for Java. Простая интеграция для разработчиков Java.
keywords:
- create pdf from dwg
- convert cad to pdf
- pdf different page sizes
- export dwg to pdf
- customize pdf layout
linktitle: Один PDF с разными макетами
schemas:
- author: Aspose
  dateModified: '2026-06-29'
  description: Learn how to create PDF from DWG and customize PDF layout using Aspose.CAD
    for Java. Easy integration for Java developers.
  headline: Create PDF from DWG with Aspose.CAD for Java
  type: TechArticle
- questions:
  - answer: Yes, Aspose.CAD for Java integrates seamlessly with libraries such as
      Apache POI, Jackson, or Spring Boot.
    question: Can I use Aspose.CAD for Java with other Java libraries?
  - answer: Absolutely! You can access a free trial version [here](https://releases.aspose.com/).
    question: Is there a trial version available?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community
      support and discussions.
    question: Where can I find additional support?
  - answer: You can obtain a temporary license [here](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license?
  - answer: Purchase the full version of Aspose.CAD for Java [here](https://purchase.aspose.com/buy).
    question: Where can I purchase the full version?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Создание PDF из DWG с помощью Aspose.CAD for Java
url: /ru/java/other-cad-operations/single-pdf-different-layouts/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Создать PDF из DWG с помощью Aspose.CAD для Java

## Введение

В этом руководстве вы **создадите PDF из DWG** файлов и примените несколько макетов разных размеров страниц с использованием Aspose.CAD для Java. Независимо от того, нужно ли вам генерировать строительные чертежи, инженерные схемы или готовые к маркетингу PDF, приведённые ниже шаги покажут, как конвертировать CAD‑чертежи в PDF, настроить размеры каждого макета и создать один многостраничный документ — без выхода из вашей Java‑среды.

## Краткие ответы
- **Что охватывает руководство?** Преобразование чертежа DWG в один PDF с несколькими размерами страниц.  
- **Какая библиотека требуется?** Aspose.CAD для Java (последняя версия).  
- **Нужна ли лицензия?** Бесплатная пробная версия подходит для разработки; для продакшна требуется коммерческая лицензия.  
- **Можно ли экспортировать в другие форматы?** Да — API также поддерживает экспорт в PNG, JPEG и SVG.  
- **Достаточно ли Java 8?** Библиотека работает с Java 8 и более новыми средами выполнения.

## Что такое «create pdf from dwg»?

**Create PDF from DWG** означает преобразование нативного файла AutoCAD DWG в документ PDF с сохранением векторной точности, слоёв и толщины линий, а также возможностью настройки макета. Aspose.CAD выполняет эту конверсию полностью в памяти, поэтому внешнее CAD‑программное обеспечение не требуется, а полученный PDF можно сразу редактировать или печатать.

## Почему настраивать макет PDF из DWG?

Aspose.CAD поддерживает **30+ форматов CAD** и может генерировать PDF размером до **500 МБ** без загрузки всего файла в память. Определяя отдельные размеры страниц для каждого макета, вы можете создавать печатные листы, соответствующие стандартам ISO, ANSI или пользовательским размерам — измеримое преимущество, экономящее время и устраняющее ручную пост‑обработку.

## Требования

Прежде чем мы начнём, убедитесь, что у вас есть следующие требования:
- Java Environment: Убедитесь, что Java установлена на вашем компьютере.  
- Aspose.CAD Library: Скачайте и установите библиотеку Aspose.CAD для Java по [download link](https://releases.aspose.com/cad/java/).  
- Document Directory: Создайте каталог для ваших DWG‑чертежей.

## Импорт пакетов

Класс `CadImage` является основным объектом Aspose.CAD, представляющим CAD‑чертеж в памяти. Импортируйте необходимые пространства имён перед началом работы:

```java
import com.aspose.cad.Image;
import com.aspose.cad.SizeF;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.VectorRasterizationOptions;
```

## Шаг 1: Загрузка CAD‑чертежа

`CadImage` загружает файл DWG и предоставляет доступ к его векторным данным. Начните с загрузки вашего CAD‑чертежа в объект `CadImage`:

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
CadImage cadImage = (CadImage)Image.load(dataDir + "City skyway map.dwg");
```

## Шаг 2: Настройка параметров растеризации

`RasterizationOptions` определяет, как векторы CAD растеризуются перед помещением в PDF. Настройте параметры растеризации для CAD‑изображения:

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1000);
rasterizationOptions.setPageHeight(1000);
```

## Шаг 3: Настройка размеров страниц макета

`PdfOptions` позволяет назначать отдельные размеры страниц каждому макету внутри DWG. Определите пользовательские размеры для нескольких макетов в CAD‑чертежe:

```java
rasterizationOptions.getLayoutPageSizes().addItem("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.getLayoutPageSizes().addItem("8.5 x 11 Plot", new SizeF(1000, 100));
```

## Шаг 4: Установка параметров PDF

`PdfOptions` — контейнер, объединяющий настройки растеризации и определения макетов. Настройте параметры PDF, включив настройки растеризации:

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Шаг 5: Сохранить как PDF

`PdfSaveOptions` завершает конверсию и записывает выходной файл. Сохраните обработанное CAD‑изображение в формате PDF:

```java
cadImage.save(dataDir + "singlePDF_out.pdf", pdfOptions);
```

Поздравляем! Вы успешно **create pdf from dwg** с разными размерами страниц, используя Aspose.CAD для Java.

## Распространённые проблемы и решения

- **Пустые страницы в результирующем PDF** – Убедитесь, что значения `PageSize` соответствуют фактическим размерам макета в файле DWG.  
- **Ошибки нехватки памяти при больших чертежах** – Используйте `CadImage.load(..., LoadOptions)` с `LoadOptions.setLoadMode(LoadMode.Memory)`, чтобы потоково считывать файл вместо полной загрузки.  
- **Неправильное масштабирование** – Отрегулируйте `RasterizationOptions.setPageWidth` и `setPageHeight` в соответствии с требуемым DPI (точек на дюйм).

## Часто задаваемые вопросы

**В: Можно ли использовать Aspose.CAD для Java с другими Java‑библиотеками?**  
Да, Aspose.CAD для Java без проблем интегрируется с такими библиотеками, как Apache POI, Jackson или Spring Boot.

**В: Доступна ли пробная версия?**  
Конечно! Вы можете получить бесплатную пробную версию [здесь](https://releases.aspose.com/).

**В: Где можно найти дополнительную поддержку?**  
Посетите [форум Aspose.CAD](https://forum.aspose.com/c/cad/19) для получения поддержки от сообщества и обсуждений.

**В: Как получить временную лицензию?**  
Вы можете получить временную лицензию [здесь](https://purchase.aspose.com/temporary-license/).

**В: Где можно приобрести полную версию?**  
Приобретите полную версию Aspose.CAD для Java [здесь](https://purchase.aspose.com/buy).

---

**Последнее обновление:** 2026-06-29  
**Тестировано с:** Aspose.CAD для Java 24.10  
**Автор:** Aspose

## Связанные руководства

- [Экспорт DWG в PDF или растеризованный формат с помощью Aspose.CAD для Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Экспорт макетов CAD в PDF с Aspose.CAD для Java](/cad/java/cad-export-options/export-cad-layouts-to-pdf/)
- [Экспорт конкретного макета DWG в PDF с помощью Aspose.CAD для Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-wrap-class >}}