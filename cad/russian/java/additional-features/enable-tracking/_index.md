---
date: 2025-12-01
description: Узнайте, как установить размер страницы PDF, конвертировать DWG в PDF
  и включить отслеживание изменений DWG с помощью Aspose.CAD для Java.
language: ru
linktitle: Set PDF Page Size and Track DWG with Java
second_title: Aspose.CAD Java API
title: Установите размер страницы PDF и отслеживание DWG с помощью Aspose.CAD Java
url: /java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Установить размер страницы PDF и отслеживать DWG с Aspose.CAD Java

## Введение

При совместной работе над CAD‑проектами часто требуется **установить размер страницы PDF** для единообразного макета, **конвертировать DWG в PDF** и отслеживать каждое изменение чертежа. Aspose.CAD для Java делает всё это возможным в едином упрощённом рабочем процессе. В этом руководстве мы пройдём по точным шагам для **установки размера страницы PDF**, включения **отслеживания изменений DWG** и экспорта чертежа в PDF — всё с использованием Java.

## Быстрые ответы
- **Как установить размер страницы PDF?** Используйте `CadRasterizationOptions.setPageWidth()` и `setPageHeight()` перед экспортом.  
- **Можно ли отслеживать изменения во время экспорта?** Да — реализуйте собственный `CadRenderHandler` для получения результатов отслеживания.  
- **Какой метод конвертирует DWG в PDF?** Вызовите `image.save(stream, pdfOptions)` после настройки параметров.  
- **Какие основные предпосылки?** JDK, Aspose.CAD для Java и папка с файлами DWG/DXF.  
- **Нужна ли лицензия для продакшн?** Да, для не‑тестовых развертываний требуется действующая лицензия Aspose.CAD.

## Что означает «установить размер страницы PDF» в контексте экспорта DWG?

Установка размера страницы PDF определяет размеры результирующего канваса PDF (ширина × высота в пикселях). Это необходимо, когда нужно, чтобы экспортированный чертеж соответствовал определённому формату бумаги или экранному макету, гарантируя, что все элементы находятся точно там, где вы ожидаете.

## Почему включать отслеживание при экспорте файлов DWG?

Отслеживание (change‑tracking) фиксирует любые проблемы рендеринга, отсутствующие шрифты или неподдерживаемые сущности, возникающие во время конвертации. Захват этой информации позволяет:

- Быстро выявлять проблемы, требующие исправления перед окончательной поставкой.  
- Предоставлять чёткую обратную связь членам команды о том, что было изменено или опущено.  
- Вести журнал аудита для отраслей с высокими требованиями к соответствию.

## Предпосылки

- **Java Development Kit (JDK)** – любая современная версия (8+).  
- **Aspose.CAD для Java** – загрузите с официальной [страницы загрузки Aspose CAD](https://releases.aspose.com/cad/java/).  
- **Каталог документов** – папка, содержащая файлы DWG/DXF, которые необходимо обработать.

## Импорт пространств имён

Начните с импорта необходимых классов Aspose.CAD и стандартных классов Java I/O.

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

## Шаг 1: Загрузить файл DWG (или DXF)

Загрузите исходный чертеж в объект `Image`. Отрегулируйте путь, чтобы он указывал на вашу собственную директорию.

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## Шаг 2: Настроить параметры экспорта PDF (включая размер страницы)

Здесь мы задаём параметры PDF и явно **устанавливаем размер страницы PDF** — 800 × 600 пикселей. Именно здесь применяется основной ключевой запрос.

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);   // set PDF page width
cadRasterizationOptions.setPageHeight(600);  // set PDF page height
```

## Шаг 3: Реализовать отслеживание

Создайте собственный обработчик ошибок, который будет получать информацию об отслеживании во время процесса конвертации.

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## Шаг 4: Экспорт в PDF

С установленными параметрами и обработчиком отслеживания экспортируйте чертеж. Этот шаг **конвертирует DWG в PDF** (или DXF в PDF в нашем примере).

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## Шаг 5: Класс CadRenderHandler – захват результатов отслеживания

Класс `ErrorHandler` расширяет `CadRenderHandler` и выводит любые проблемы рендеринга, возникшие при **отслеживании изменений DWG** файлов.

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

## Распространённые проблемы и их решения

| Проблема | Почему происходит | Решение |
|----------|-------------------|---------|
| **Отсутствуют шрифты** | CAD‑файл ссылается на шрифты, не установленные на сервере. | Установите требуемые шрифты или внедрите их в исходный чертеж. |
| **Неподдерживаемые сущности** | Некоторые сущности DWG пока не поддерживаются Aspose.CAD. | Используйте вывод отслеживания для их идентификации и упростите чертеж. |
| **Неправильный размер страницы** | `setPageWidth/Height` не вызвано перед экспортом. | Убедитесь, что размер страницы установлен в `CadRasterizationOptions`, как показано выше. |

## Часто задаваемые вопросы

### Q1: Можно ли включить отслеживание для других форматов CAD‑файлов, используя Aspose.CAD для Java?

A1: Aspose.CAD в основном поддерживает отслеживание для файлов DWG/DXF. Для других форматов обратитесь к официальной документации, чтобы узнать о доступных возможностях.

### Q2: Как обрабатывать дополнительные параметры экспорта в Aspose.CAD для Java?

A2: Библиотека предлагает множество параметров, таких как DPI, цвет фона и векторный растр. Изучайте их в [Документации Aspose.CAD Java](https://reference.aspose.com/cad/java/).

### Q3: Есть ли доступна пробная версия Aspose.CAD для Java?

A3: Да, бесплатную пробную версию можно скачать на странице [Aspose.CAD Free Trial](https://releases.aspose.com/).

### Q4: Где можно получить помощь или обсудить проблемы, связанные с Aspose.CAD для Java?

A4: Сообщество на форуме [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) — отличное место для вопросов и обмена опытом.

### Q5: Как получить временную лицензию для Aspose.CAD для Java?

A5: Следуйте инструкциям на странице [Temporary License](https://purchase.aspose.com/temporary-license/) для запроса ограниченной по времени лицензии для оценки.

### Q6: Можно ли **конвертировать DWG в PDF**, сохраняя слои?

A6: Да. Настроив `CadRasterizationOptions`, вы можете сохранить информацию о слоях в результирующем PDF.

### Q7: Какой лучший способ **экспортировать DWG как PDF** с пользовательскими размерами страницы?

A7: Установите желаемую ширину и высоту с помощью `setPageWidth` и `setPageHeight` перед вызовом `image.save()` — как продемонстрировано в Шаге 2.

## Заключение

Следуя приведённым выше шагам, вы сможете **установить размер страницы PDF**, **конвертировать DWG в PDF** и **отслеживать изменения в файлах DWG** с помощью Aspose.CAD для Java. Этот рабочий процесс даёт полный контроль над макетом вывода и предоставляет ценные диагностические данные, обеспечивая плавное и безошибочное взаимодействие в CAD‑командах. Не стесняйтесь исследовать дополнительные параметры рендеринга и интегрировать этот код в более крупные автоматизированные конвейеры.

---

**Последнее обновление:** 2025-12-01  
**Тестировано с:** Aspose.CAD для Java 24.12 (последняя на момент написания)  
**Автор:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}