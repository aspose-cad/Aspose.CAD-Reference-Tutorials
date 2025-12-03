---
date: 2025-12-03
description: Узнайте, как установить размер страницы PDF при конвертации DWG в PDF
  и включить отслеживание в файлах DWG с помощью Aspose.CAD для Java — полный гид
  по экспорту чертежей CAD в PDF с точностью.
language: ru
linktitle: Set PDF Page Size and Enable Tracking in DWG Files Using Java
second_title: Aspose.CAD Java API
title: Установите размер страницы PDF и включите отслеживание в файлах DWG с помощью
  Aspose.CAD на Java
url: /java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Установить размер страницы PDF и включить отслеживание в DWG‑файлах с помощью Aspose.CAD для Java

## Введение

Если вам нужно **установить размер страницы PDF** при *конвертации DWG в PDF* и одновременно отслеживать возможные проблемы рендеринга, Aspose.CAD для Java предоставляет чистый программный способ сделать и то, и другое. В этом руководстве мы пошагово покажем, как настроить размеры страницы, включить отслеживание и экспортировать чертеж CAD в PDF — все из Java. К концу вы поймёте, почему правильный размер страницы важен для чертежей CAD и как собрать подробную информацию об отслеживании во время процесса экспорта.

## Быстрые ответы
- **Что влияет «установить размер страницы PDF»?** Определяет ширину и высоту результирующего канваса PDF, гарантируя, что ваш чертеж полностью помещается.  
- **Нужна ли лицензия для использования этой функции?** Для тестирования работает пробная версия; для продакшна требуется коммерческая лицензия.  
- **Какая версия Aspose.CAD требуется?** Любая современная версия, поддерживающая `CadRasterizationOptions`.  
- **Можно ли использовать это с другими форматами CAD?** Пример показывает DWG/DXF, но тот же подход работает для большинства поддерживаемых форматов.  
- **Сколько времени занимает конвертация?** Обычно менее секунды для небольших файлов; более крупные чертежи могут потребовать больше времени.

## Что означает «установить размер страницы PDF» в контексте экспорта CAD?
Установка размера страницы PDF сообщает рендереру точные размеры (в пикселях или пунктах) выходного канваса. Это особенно важно для технических чертежей, где необходимо сохранять масштаб и расположение. Без явных настроек размера страницы PDF может по умолчанию использовать размер, который обрезает или искажает чертеж.

## Почему стоит устанавливать размер страницы PDF при экспорте CAD‑чертежей?
- **Сохранение масштаба** — инженеры полагаются на печать в истинном масштабе.  
- **Подгонка под бумагу** — выберите A4, Letter или пользовательский размер, соответствующий спецификациям проекта.  
- **Повышение читаемости** — большие страницы позволяют увидеть мелкие детали без увеличения.  
- **Последовательный вывод** — автоматизированные конвейеры генерируют PDF с одинаковыми размерами каждый раз.

## Как установить размер страницы PDF при конвертации DWG в PDF?
Далее мы настроим `CadRasterizationOptions` с пользовательскими значениями ширины и высоты перед экспортом. Этот шаг непосредственно решает задачу **установить размер страницы PDF**.

## Предварительные требования

- **Java Development Kit (JDK)** — Java 8 или новее, установленный на вашем компьютере.  
- **Aspose.CAD для Java** — скачайте с официальной [страницы загрузки Aspose CAD](https://releases.aspose.com/cad/java/).  
- **Каталог документов** — папка, содержащая DWG/DXF‑файлы, которые вы хотите обработать.

## Импорт пространств имён

Сначала импортируйте необходимые классы. Блок кода остаётся без изменений.

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

Загрузите исходный чертеж. Скорректируйте путь, указывающий на ваш файл.

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## Шаг 2: Настройка параметров экспорта PDF (включая размер страницы)

Здесь мы задаём ширину и высоту страницы — это место, где мы **устанавливаем размер страницы PDF**. Значения задаются в пикселях; при необходимости их можно преобразовать из дюймов или миллиметров.

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);   // <-- custom width
cadRasterizationOptions.setPageHeight(600);  // <-- custom height
```

> **Совет:** Если вам нужны стандартные размеры бумаги, используйте преобразование `1 дюйм = 72 пункта`. Для страницы A4 (8,27 × 11,69 дюйма) задайте `pageWidth = 595` и `pageHeight = 842`.

## Шаг 3: Реализация отслеживания

Отслеживание фиксирует любые проблемы рендеринга. Мы подключаем пользовательский обработчик, который будет вызван после экспорта.

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## Шаг 4: Экспорт в PDF

Теперь выполните конвертацию. PDF будет создан с указанными вами размерами, а информация об отслеживании будет выведена в консоль.

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## Шаг 5: Класс CadRenderHandler

Обработчик выводит любые сбои, произошедшие во время рендеринга. Это помогает отлаживать проблемы при **экспорте CAD‑чертежа в PDF**.

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

| Проблема | Причина | Решение |
|----------|---------|---------|
| **Пустой PDF** | Размер страницы установлен в 0 или слишком мал | Убедитесь, что `setPageWidth` и `setPageHeight` имеют положительные значения. |
| **Отсутствует геометрия** | Ошибки рендеринга, зафиксированные обработчиком | Просмотрите вывод консоли из `ErrorHandler` и устраните конкретный `RenderCode`. |
| **Файл не найден** | Неправильный путь `dataDir` | Используйте абсолютный путь или убедитесь, что каталог существует. |
| **Исключение лицензии** | Использование пробной версии без действующей лицензии для больших файлов | Примените вашу лицензию Aspose.CAD перед загрузкой изображения. |

## Часто задаваемые вопросы

**В: Можно ли включить отслеживание для других форматов CAD с помощью Aspose.CAD для Java?**  
О: Aspose.CAD в основном поддерживает DWG/DXF для отслеживания. Для других форматов см. официальную документацию.

**В: Как обрабатывать дополнительные параметры экспорта в Aspose.CAD для Java?**  
О: Библиотека предлагает множество опций, таких как DPI, цвет фона и векторный растр. См. [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/) для деталей.

**В: Доступна ли пробная версия Aspose.CAD для Java?**  
О: Да, вы можете скачать бесплатную пробную версию с [Aspose.CAD Free Trial](https://releases.aspose.com/).

**В: Где можно получить поддержку или обсудить вопросы, связанные с Aspose.CAD для Java?**  
О: Посетите [форум Aspose.CAD](https://forum.aspose.com/c/cad/19) для общения с сообществом и официальных ответов.

**В: Как получить временную лицензию для Aspose.CAD для Java?**  
О: Следуйте инструкциям на странице [Temporary License](https://purchase.aspose.com/temporary-license/).

---

**Последнее обновление:** 2025-12-03  
**Тестировано с:** Aspose.CAD для Java 24.11 (на момент написания)  
**Автор:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}