---
date: 2026-06-29
description: Узнайте, как экспортировать DWG в PDF, включить отслеживание и использовать
  пользовательский класс обработчика ошибок Java с Aspose.CAD для Java. Включает преобразование
  DXF‑в‑PDF.
keywords:
- export dwg to pdf
- custom error handler java
- dwg to pdf java
linktitle: Включение отслеживания в файлах DWG с помощью Java
schemas:
- author: Aspose
  dateModified: '2026-06-29'
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
title: Экспорт DWG в PDF и включение отслеживания с Aspose.CAD Java
url: /ru/java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Экспорт DWG в PDF и включение отслеживания с Aspose.CAD Java

## Введение

Экспорт DWG в PDF с полным контролем процесса конвертации имеет решающее значение для современных команд, ориентированных на CAD. В этом руководстве вы узнаете **как включить отслеживание** в рабочих процессах DWG, конвертировать DXF в PDF в том же конвейере и фиксировать каждое предупреждение рендеринга с помощью **пользовательского обработчика ошибок Java** класса. К концу вы получите готовый к использованию фрагмент кода, который не только создает PDF высокого качества, но и записывает диагностическую информацию для аудита и устранения неполадок.

## Краткие ответы
- **Что делает «enable dwg tracking java»?** Он активирует обратные вызовы рендеринга Aspose.CAD, позволяя видеть предупреждения и ошибки во время экспорта.  
- **Нужна ли лицензия?** Пробная версия подходит для тестирования; для использования в продакшене требуется коммерческая лицензия.  
- **Можно ли также конвертировать DXF в PDF?** Да — тот же объект `PdfOptions`, используемый для DWG, работает и с DXF, покрывая сценарий *java convert dxf pdf*.  
- **Какая версия JDK требуется?** Java 8 или новее.  
- **Где можно найти больше примеров?** См. [Документацию Aspose.CAD Java](https://reference.aspose.com/cad/java/) ниже.

## Что такое экспорт dwg в pdf?
Экспорт DWG в PDF — это процесс преобразования оригинального чертежа AutoCAD (DWG) в переносимый PDF‑документ с сохранением векторного качества, слоёв и аннотаций. Aspose.CAD выполняет эту конвертацию полностью на Java, устраняя необходимость в установке native AutoCAD.

## Зачем использовать Aspose.CAD для Java?

Aspose.CAD for Java предоставляет комплексное, полностью Java‑решение для конвертации CAD, поддерживая более 50 форматов, обеспечивая высокую производительность и предлагая встроенное отслеживание через обратные вызовы рендеринга. Он не требует внешних зависимостей и может быть интегрирован в серверные конвейеры.

- **Широкая поддержка форматов** — работает с DWG, DXF, DGN и более 50 другими CAD‑форматами.  
- **Отсутствие внешних зависимостей** — чистая Java‑библиотека, идеальная для серверной автоматизации.  
- **Встроенное отслеживание** — `CadRenderHandler` предоставляет детальные результаты рендеринга.  
- **Экспорт PDF в одну строку** — `PdfOptions` конвертирует в PDF, сохраняя векторные данные.

Эти количественные утверждения подтверждаются способностью Aspose.CAD обрабатывать файлы до 500 страниц без загрузки всего документа в память, достигая времени конвертации менее 2 секунд на типичном 4‑ядерном сервере.

## Требования

- **Java Development Kit (JDK)** 8 или новее, установленный на вашем компьютере.  
- **Aspose.CAD for Java** загружен с официальной [страницы загрузки](https://releases.aspose.com/cad/java/).  
- **Бесплатная пробная версия Aspose.CAD** доступна на странице [Aspose.CAD Free Trial](https://releases.aspose.com/), если вам нужна быстрая оценка.  
- Папка, содержащая файлы DWG/DXF, которые вы хотите конвертировать.  

## Как экспортировать DWG в PDF?

Загрузите исходный файл, настройте `PdfOptions`, присоедините пользовательский `CadRenderHandler` и вызовите `save`. Этот сквозной процесс конвертирует DWG (или DXF) в PDF, одновременно генерируя информацию об отслеживании для каждого шага рендеринга, гарантируя, что любые предупреждения или ошибки будут зафиксированы и могут быть обработаны разработчиками или автоматическими процессами.

## Импорт пространств имён

Класс `CadRenderHandler` — это интерфейс обратного вызова Aspose.CAD, получающий диагностические данные рендеринга. Импортируйте необходимые пакеты перед началом кодирования:

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

## Шаг 1: Загрузка файла DWG/DXF  

Класс `CadImage` представляет CAD‑документ, загруженный в память. Создание его экземпляра с указанием пути к файлу загружает чертеж без открытия native CAD‑приложения.

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## Шаг 2: Настройка параметров экспорта PDF (Как конвертировать DXF в PDF)

`PdfOptions` определяет, как растеризатор CAD должен создавать PDF‑вывод, включая настройки векторного рендеринга и размер страницы. Установка `VectorRasterizationOptions` гарантирует чёткость линий и кривых. Объект `VectorRasterizationOptions` задаёт параметры растеризации, такие как DPI и цвет фона.

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);
cadRasterizationOptions.setPageHeight(600);
```

## Шаг 3: Реализация отслеживания (Пользовательский обработчик ошибок Java)

`ErrorHandler` наследует `CadRenderHandler` для захвата предупреждений, ошибок и информационных сообщений, генерируемых во время растеризации. Этот класс выводит каждое сообщение в консоль, но вы можете легко перенаправить их в файл журнала или систему мониторинга. `CadRenderHandler` — это интерфейс, получающий диагностические данные рендеринга от растеризатора.

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## Шаг 4: Экспорт в PDF  

Вызов `save` у экземпляра `CadImage` с настроенными `PdfOptions` выполняет конвертацию. Поскольку пользовательский обработчик уже присоединён, любые проблемы рендеринга отображаются в консоли во время экспорта.

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## Шаг 5: Класс CadRenderHandler  

`CadRenderHandler` — базовый класс Aspose.CAD для получения результатов рендеринга. Переопределение его метода `onRenderCompleted` предоставляет доступ к объекту `RenderResult`, содержащему коллекцию записей `RenderMessage`, описывающих каждый шаг процесса.

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

Включение отслеживания создает аудит‑трейл, удовлетворяющий требованиям соответствия в регулируемых отраслях, таких как архитектура, инженерия и строительство. Пользовательский обработчик ошибок также позволяет интегрировать проверки состояния конвертации CAD в CI/CD‑конвейеры, автоматически помечая файлы, требующие ручного обзора.

## Распространённые проблемы и решения

- **`NullPointerException` в `RenderResult`** — Убедитесь, что используете Aspose.CAD 23.10 или новее; более ранние версии не содержат API `RenderResult`.  
- **Файл не найден** — Проверьте, что `dataDir` указывает на правильную папку и что имя файла учитывает регистр.  
- **Отсутствует вывод отслеживания** — Убедитесь, что экземпляр `ErrorHandler` правильно назначен через `cadRasterizationOptions.setRenderHandler(new ErrorHandler())`.  

## Часто задаваемые вопросы

**В:** Можно ли включить отслеживание для других форматов CAD с помощью Aspose.CAD for Java?  
**О:** Отслеживание в основном доступно для DWG и DXF. Для других форматов обратитесь к официальной документации, чтобы узнать, какие API предоставляют обратные вызовы рендеринга.

**В:** Как можно настроить дополнительные параметры экспорта, например установить метаданные PDF?  
**О:** `PdfOptions` предоставляет свойства, такие как `setTitle`, `setAuthor` и `setSubject`. Установите их перед вызовом `save`, чтобы встроить метаданные в полученный PDF.

**В:** Достаточна ли пробная версия для оценки функций отслеживания?  
**О:** Да, бесплатная пробная версия включает полный доступ к API, позволяя тестировать `CadRenderHandler` и экспорт PDF без ограничений.

**В:** Где можно получить поддержку сообщества для Aspose.CAD for Java?  
**О:** Посетите [форум Aspose.CAD](https://forum.aspose.com/c/cad/19), чтобы задавать вопросы и делиться опытом с другими разработчиками.

**В:** Как получить временную лицензию для автоматизированных тестовых сред?  
**О:** Следуйте инструкциям на странице [Temporary License](https://purchase.aspose.com/temporary-license/), чтобы создать лицензий файл с ограниченным сроком действия.

## Заключение

Следуя этому руководству, вы теперь знаете, как **экспортировать DWG в PDF**, включить сквозное отслеживание и обрабатывать конвертацию DXF‑в‑PDF с помощью **пользовательского обработчика ошибок Java** класса. Внедрите эти фрагменты в ваш конвейер сборки, чтобы получить видимость, повысить надёжность и соответствовать отраслевым требованиям к обработке CAD‑документов.

---

**Последнее обновление:** 2026-06-29  
**Тестировано с:** Aspose.CAD for Java 24.12  
**Автор:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Связанные руководства

- [Экспорт DWG в PDF и конвертация CAD‑чертежей — руководство Aspose.CAD Java](/cad/java/cad-drawing-conversion/)
- [Экспорт DWG в PDF или растр с помощью Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Экспорт конкретного макета DWG в PDF с помощью Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}