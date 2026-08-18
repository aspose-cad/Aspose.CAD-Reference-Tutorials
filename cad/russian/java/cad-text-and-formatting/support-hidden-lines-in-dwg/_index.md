---
date: 2026-03-05
description: Узнайте, как экспортировать DWG в PDF, включать скрытые линии и конвертировать
  DWG в PDF с помощью Aspose.CAD для Java в этом пошаговом руководстве.
linktitle: Export DWG as PDF Using Java
second_title: Aspose.CAD Java API
title: Экспорт DWG в PDF с скрытыми линиями – Aspose.CAD для Java
url: /ru/java/cad-text-and-formatting/support-hidden-lines-in-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Экспорт DWG в PDF с скрытыми линиями – Aspose.CAD для Java

## Введение

В этом руководстве вы узнаете, как **export dwg to pdf**, сохраняя скрытые линии, используя Aspose.CAD for Java. Независимо от того, нужно ли вам **convert DWG to PDF**, создать руководство в стиле **dwg to pdf tutorial**, или просто **save DWG as PDF** с поддержкой скрытых линий, мы проведём вас через каждый шаг. К концу вы получите готовое решение, которое можно добавить в любой проект Java.

## Быстрые ответы
- **Что охватывает это руководство?** Включение рендеринга скрытых линий при экспорте DWG в PDF с помощью Aspose.CAD for Java.  
- **Какая основная операция выполняется?** `export dwg to pdf`.  
- **Нужна ли лицензия?** Бесплатная пробная версия подходит для тестирования; для продакшна требуется коммерческая лицензия.  
- **Какие предпосылки?** Среда разработки Java, библиотека Aspose.CAD for Java и файлы DWG.  
- **Сколько времени занимает реализация?** Около 10‑15 минут для базовой настройки.

## Что такое “export dwg to pdf”?
Экспорт файла DWG в PDF преобразует векторный CAD‑чертёж в формат Portable Document Format, сохраняя слои, типы линий и опциональный рендеринг скрытых линий. Это упрощает обмен CAD‑дизайнами с заинтересованными сторонами, у которых может не быть CAD‑программного обеспечения.

## Как включить скрытые линии при экспорте DWG в PDF
Скрытые линии управляются через параметр layout в настройках растеризации. Выбирая макет **Model**, Aspose.CAD сообщает рендереру рассматривать скрытые ребра как невидимые, предоставляя чистое 2‑D представление 3‑D модели.

## Почему включать скрытые линии при экспорте?
Скрытые линии обеспечивают более чёткое визуальное представление сложных 3‑D моделей на 2‑D странице, подчёркивая только видимые ребра. Это повышает читаемость и часто требуется для инженерной документации.

## Предпосылки

1. **Aspose.CAD for Java** – загрузите библиотеку с официального сайта [здесь](https://releases.aspose.com/cad/java/).  
2. **DWG files** – храните исходные чертежи DWG в известном каталоге.  
3. **Java development environment** – JDK 8+ и ваша предпочтительная IDE (Eclipse, IntelliJ и т.д.).  

Теперь, когда всё готово, приступим к коду.

## Импорт пространств имён

Начните с импорта необходимых классов, чтобы работать с CAD‑изображениями и параметрами PDF.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.Arrays;
import java.util.List;
```

## Шаг 1: Настройка проекта

Создайте Java‑проект и добавьте JAR‑файл Aspose.CAD в путь сборки. Затем задайте каталог, содержащий ваши файлы DWG.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

> **Pro tip:** Используйте абсолютный путь или настройте относительный путь, исходя из папки ресурсов вашего проекта.

## Шаг 2: Загрузка DWG файла

Загрузите исходный файл DWG в объект `CadImage`, чтобы иметь возможность его обрабатывать.

```java
String sourceFilePath = dataDir + "Bottom_plate.dwg";
String outPath = dataDir + "Bottom_plate.pdf";
CadImage cadImage = (CadImage)Image.load(sourceFilePath);
```

## Шаг 3: Настройка параметров растеризации

Выберите слои, которые хотите включить, и задайте размер страницы, соответствующий оригинальному чертежу. Здесь мы включаем рендеринг скрытых линий, указывая макет.

```java
List<String> list = Arrays.asList("Print","L1_RegMark","L2_RegMark");
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageHeight(cadImage.getHeight());
rasterizationOptions.setPageWidth(cadImage.getWidth()) ;
rasterizationOptions.setLayers(list);
```

## Шаг 4: Установка параметров PDF

Сообщите Aspose.CAD растрировать векторные данные в PDF, используя макет “Model”, чтобы скрытые линии оставались скрытыми.

```java
PdfOptions pdfOptions = new PdfOptions();
rasterizationOptions.setLayouts(new String[] { "Model" });
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Шаг 5: Сохранение результата

Наконец, экспортируйте DWG в файл PDF. Скрытые линии будут соблюдены в соответствии с выбранным макетом.

```java
cadImage.save(outPath, pdfOptions);
System.out.println("\nThe DWG file exported successfully to PDF.\nFile saved at " + dataDir);
```

> **Common Pitfall:** Если забыть установить макет в `"Model"`, все линии (включая скрытые) будут отображаться сплошными в PDF.

## Распространённые проблемы и решения

| Проблема | Почему происходит | Как исправить |
|----------|-------------------|---------------|
| PDF показывает все линии сплошными | Макет не установлен на **Model** | Убедитесь, что вызвано `rasterizationOptions.setLayouts(new String[] { "Model" });` перед сохранением. |
| Отсутствуют слои в выводе | Неправильные имена слоёв | Проверьте имена слоёв в файле DWG и точно соответствуйте им в `list`. |
| Ошибка «Out‑of‑memory» при больших файлах | Большой размер растеризации | Уменьшите размеры страницы или, если возможно, обрабатывайте чертёж частями. |

## Часто задаваемые вопросы

### Вопрос 1: Могу ли я использовать Aspose.CAD for Java с другими форматами CAD‑файлов?
**Ответ:** Да, Aspose.CAD поддерживает различные CAD‑форматы, такие как DWG, DXF, DWF и другие.

### Вопрос 2: Доступна ли бесплатная пробная версия Aspose.CAD for Java?
**Ответ:** Да, бесплатную пробную версию можно найти [здесь](https://releases.aspose.com/).

### Вопрос 3: Как получить поддержку Aspose.CAD for Java?
**Ответ:** Посетите форум Aspose.CAD [здесь](https://forum.aspose.com/c/cad/19) для получения поддержки от сообщества.

### Вопрос 4: Где найти подробную документацию по Aspose.CAD for Java?
**Ответ:** Обратитесь к документации [здесь](https://reference.aspose.com/cad/java/).

### Вопрос 5: Можно ли приобрести временную лицензию для Aspose.CAD for Java?
**Ответ:** Да, временную лицензию можно получить [здесь](https://purchase.aspose.com/temporary-license/).

### Вопрос 6: Работает ли этот метод для конвертации DWG в PDF в безголовом серверном окружении?
**Ответ:** Абсолютно. Поскольку код использует только API Aspose.CAD, он работает без каких‑либо UI‑зависимостей, что делает его идеальным для серверной автоматизации.

## Заключение

Теперь у вас есть полностью готовый к использованию метод **export dwg to pdf** с поддержкой скрытых линий, реализованный с помощью Aspose.CAD for Java. Этот подход можно интегрировать в пакетные инструменты обработки, веб‑службы или настольные приложения для автоматизации конвертации CAD в PDF.

---

**Last Updated:** 2026-03-05  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}