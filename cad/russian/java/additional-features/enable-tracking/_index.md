---
date: 2026-11-18
description: Узнайте, как экспортировать DWG в PDF, включить tracking и использовать
  пользовательский класс custom error handler Java с Aspose.CAD для Java. Включает
  конвертацию DXF‑to‑PDF.
keywords:
- export dwg to pdf
- custom error handler java
- dwg to pdf java
lastmod: 2026-11-18
linktitle: Enable Tracking в файлах DWG с помощью Java
og_description: Экспортируйте DWG в PDF и включите полное tracking в Java с Aspose.CAD.
  Узнайте, как использовать custom error handler, конвертировать DXF в PDF и регистрировать
  render warnings.
og_image_alt: Guide showing DWG to PDF conversion and tracking in Java with Aspose.CAD
og_title: Экспорт DWG в PDF с tracking, используя Aspose.CAD for Java
schemas:
- author: Aspose
  dateModified: '2026-11-18'
  description: Learn how to export DWG to PDF, enable tracking, and use a custom error
    handler Java class with Aspose.CAD for Java. Includes DXF‑to‑PDF conversion.
  headline: Export DWG to PDF and Enable Tracking with Aspose.CAD Java
  type: TechArticle
- questions:
  - answer: It activates Aspose.CAD’s render callbacks so you can see warnings and
      errors during export.
    question: What does “enable dwg tracking java” do?
  - answer: A trial works for testing; a commercial license is required for production
      use.
    question: Do I need a license?
  - answer: Yes – the same `PdfOptions` object used for DWG works for DXF, covering
      the *java convert dxf pdf* scenario.
    question: Can I also convert DXF to PDF?
  - answer: Java 8 or higher.
    question: Which JDK version is required?
  - answer: See the [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/)
      linked below.
    question: Where can I find more examples?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- export dwg to pdf
- aspose.cad java
- custom error handler
- dxf to pdf
- java cad conversion
title: Экспорт DWG в PDF и включение tracking с Aspose.CAD Java
url: /ru/java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Экспорт DWG в PDF и включение отслеживания с Aspose.CAD Java

## Введение

Экспорт DWG в PDF при сохранении полной видимости процесса конвертации является необходимым для современных команд, ориентированных на CAD. В этом руководстве вы узнаете **как включить отслеживание** в рабочих процессах DWG, конвертировать DXF в PDF в том же конвейере и фиксировать каждое предупреждение рендеринга с помощью **класса пользовательского обработчика ошибок Java**. К концу вы получите готовый к производству фрагмент кода, который не только создает PDF высокого качества, но и записывает диагностическую информацию для аудита и устранения неполадок.

## Быстрые ответы
- **Что делает “enable dwg tracking java”?** Он активирует обратные вызовы рендеринга Aspose.CAD, позволяя видеть предупреждения и ошибки во время экспорта.  
- **Нужна ли мне лицензия?** Пробная версия подходит для тестирования; для использования в продакшене требуется коммерческая лицензия.  
- **Могу ли я также конвертировать DXF в PDF?** Да — тот же объект `PdfOptions`, используемый для DWG, работает и с DXF, покрывая сценарий *java convert dxf pdf*.  
- **Какая версия JDK требуется?** Java 8 или выше.  
- **Где я могу найти больше примеров?** Смотрите [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/) ниже.

## Что такое экспорт DWG в PDF?

Экспорт DWG в PDF — это процесс преобразования оригинального чертежа AutoCAD (DWG) в портативный PDF‑документ с сохранением векторной точности, слоёв и аннотаций. **Aspose.CAD конвертирует DWG в PDF на чистом Java, поэтому вам никогда не понадобится лицензированная установка AutoCAD.** Эта конверсия сохраняет точные толщины линий, стили текста и геометрию макета, делая PDF подходящим для просмотра клиентом, архивирования или последующей обработки.

## Почему использовать Aspose.CAD для Java?

Aspose.CAD для Java предоставляет всестороннее решение на чистом Java для конвертации CAD, поддерживая более 50 форматов, обеспечивая высокую производительность и предоставляя встроенное отслеживание через обратные вызовы рендеринга. Оно не требует внешних зависимостей и может быть интегрировано в серверные конвейеры. Библиотека также включает эффективную по памяти обработку, позволяя конвертировать файлы до 500 страниц без загрузки всего документа в ОЗУ.

## Требования

- **Java Development Kit (JDK)** 8 или новее, установленный на вашем компьютере.  
- **Aspose.CAD for Java** загружен с официальной [download link](https://releases.aspose.com/cad/java/).  
- **Aspose.CAD Free Trial** можно получить со страницы [Aspose.CAD Free Trial](https://releases.aspose.com/), если вам нужна быстрая оценка.  
- Папка, содержащая файлы DWG/DXF, которые вы хотите конвертировать.  

## Как экспортировать DWG в PDF?

Загрузите исходный файл, настройте `PdfOptions`, присоедините пользовательский `CadRenderHandler` и вызовите `save`. Этот сквозной процесс конвертирует DWG (или DXF) в PDF, одновременно генерируя информацию об отслеживании для каждого шага рендеринга, гарантируя, что все предупреждения или ошибки будут зафиксированы и могут быть обработаны разработчиками или автоматическими процессами.

## Импорт пространств имён

Интерфейс `CadRenderHandler` получает диагностические данные рендеринга, такие как предупреждения и ошибки, во время конвертации.  
```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.CadRenderResult;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.RenderResult;
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
```

## Шаг 1: загрузить файл dwg/dxf  

`CadImage` представляет собой CAD‑чертеж, загруженный в память, и предоставляет доступ к его страницам и слоям.  
```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## Шаг 2: настроить параметры экспорта PDF (как конвертировать dxf в pdf)

`PdfOptions` определяет настройки вывода PDF, а `VectorRasterizationOptions` управляет параметрами растеризации, такими как DPI и цвет фона.  
```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);
cadRasterizationOptions.setPageHeight(600);
```

## Шаг 3: реализовать отслеживание (пользовательский обработчик ошибок java)

`ErrorHandler` расширяет `CadRenderHandler` для захвата и записи сообщений рендеринга, генерируемых во время процесса конвертации.  
```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## Шаг 4: экспортировать в pdf  

Вызов метода `save` у экземпляра `CadImage` записывает отрендеренный PDF по указанному пути вывода.  
```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## Шаг 5: класс CadRenderHandler  

`CadRenderHandler` — базовый класс обратного вызова, получающий `RenderResult`, содержащий подробные сообщения после завершения рендеринга.  
```java
public static class ErrorHandler extends CadRasterizationOptions.CadRenderHandler {
    @Override
    public void invoke(CadRenderResult result) {
        System.out.println("Tracking results of exporting");

        if (result.isRenderComplete())
            return;

        System.out.println("Have some problems:");

        int idxError = 1;
        for (RenderResult rr : result.getFailures()) {
            System.out.printf("{0}. {1}, {2}", idxError, rr.getRenderCode(), rr.getMessage());
            idxError++;
        }
    }
}
```

## Почему это важно

Включение отслеживания создает аудит‑трассу, удовлетворяющую требованиям соответствия в регулируемых секторах, таких как архитектура, инженерия и строительство. Пользовательский обработчик ошибок также позволяет интегрировать проверки состояния конвертации CAD в CI/CD‑конвейеры, автоматически помечая файлы, требующие ручного обзора.

## Распространённые проблемы и решения

- **`NullPointerException` на `RenderResult`** – Убедитесь, что используете Aspose.CAD 23.10 или новее; более ранние версии не имеют API `RenderResult`.  
- **Файл не найден** – Проверьте, что `dataDir` указывает на правильную папку и что имя файла совпадает с учётом регистра.  
- **Отсутствует вывод отслеживания** – Убедитесь, что ваш экземпляр `ErrorHandler` правильно назначен в `cadRasterizationOptions.setRenderHandler(new ErrorHandler())`.  

## Часто задаваемые вопросы

**Q:** Могу ли я включить отслеживание для других форматов CAD, используя Aspose.CAD для Java?  
**A:** Отслеживание в основном доступно для DWG и DXF. Для других форматов обратитесь к официальной документации, чтобы узнать, какие API предоставляют обратные вызовы рендеринга.

**Q:** Как я могу настроить дополнительные параметры экспорта, например установить метаданные PDF?  
**A:** `PdfOptions` предоставляет свойства, такие как `setTitle`, `setAuthor` и `setSubject`. Установите их перед вызовом `save`, чтобы встроить метаданные в полученный PDF.

**Q:** Достаточна ли пробная версия для оценки функций отслеживания?  
**A:** Да, бесплатная пробная версия включает полный доступ к API, позволяя тестировать `CadRenderHandler` и экспорт PDF без ограничений.

**Q:** Где я могу получить поддержку сообщества для Aspose.CAD для Java?  
**A:** Посетите [Aspose.CAD forum](https://forum.aspose.com/c/cad/19), чтобы задавать вопросы и делиться опытом с другими разработчиками.

**Q:** Как получить временную лицензию для автоматизированных тестовых сред?  
**A:** Следуйте инструкциям на странице [Temporary License](https://purchase.aspose.com/temporary-license/), чтобы создать лицензийный файл с ограниченным сроком действия.

## Заключение

Следуя этому руководству, вы теперь знаете, как **экспортировать DWG в PDF**, включить сквозное отслеживание и обрабатывать конвертацию DXF‑в‑PDF с помощью **пользовательского обработчика ошибок Java**. Внедрите эти фрагменты кода в ваш конвейер сборки, чтобы получить видимость, повысить надёжность и соответствовать отраслевым требованиям к обработке CAD‑документов.

---

**Последнее обновление:** 2026-11-18  
**Тестировано с:** Aspose.CAD for Java 24.12  
**Автор:** Aspose  

## Связанные руководства

- [Экспорт DWG в PDF и конвертация CAD‑чертежей – руководство Aspose.CAD Java](/cad/java/cad-drawing-conversion/)
- [Экспорт DWG в PDF или растеризацию с помощью Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Экспорт конкретного макета DWG в PDF с использованием Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}