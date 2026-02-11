---
date: 2026-01-02
description: Узнайте, как экспортировать DWG в PDF, включать скрытые линии и конвертировать
  DWG в PDF с помощью Aspose.CAD для Java в этом пошаговом руководстве.
linktitle: Export DWG as PDF with Hidden Lines Using Java
second_title: Aspose.CAD Java API
title: Экспорт DWG в PDF с скрытыми линиями – Aspose.CAD для Java
url: /ru/java/cad-text-and-formatting/support-hidden-lines-in-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Экспорт DWG в PDF с скрытыми линиями – Aspose.CAD for Java

## Введение

В этом руководстве вы узнаете, как **экспортировать DWG в PDF** с сохранением скрытых линий, используя Aspose.CAD for Java. Независимо от того, нужно ли вам **конвертировать DWG в PDF**, создать руководство в стиле **dwg to pdf tutorial**, или просто **сохранить DWG как PDF** с поддержкой скрытых линий, мы пройдем каждый шаг. К концу вы получите готовое решение, которое можно добавить в любой Java‑проект.

## Быстрые ответы
- **Что покрывает это руководство?** Включение рендеринга скрытых линий при экспорте DWG в PDF с помощью Aspose.CAD for Java.  
- **Какая основная операция выполняется?** `export dwg as pdf`.  
- **Нужна ли лицензия?** Бесплатная пробная версия подходит для тестирования; коммерческая лицензия требуется для продакшна.  
- **Какие требования?** Среда разработки Java, библиотека Aspose.CAD for Java и файлы DWG.  
- **Сколько времени занимает реализация?** Около 10‑15 минут для базовой настройки.

## Что такое «export dwg as pdf»?
Экспорт файла DWG в PDF преобразует векторный чертёж CAD в формат Portable Document Format, сохраняя слои, типы линий и при необходимости рендеринг скрытых линий. Это упрощает обмен CAD‑дизайнами с заинтересованными сторонами, у которых может не быть CAD‑программного обеспечения.

## Почему включать скрытые линии при экспорте?
Скрытые линии обеспечивают более чёткое визуальное представление сложных 3‑D моделей на 2‑D странице, подчёркивая только видимые грани. Это повышает читаемость и часто требуется для инженерной документации.

## Требования

1. **Aspose.CAD for Java** – загрузите библиотеку с официального сайта [здесь](https://releases.aspose.com/cad/java/).  
2. **DWG файлы** – разместите исходные DWG‑чертежи в известной директории.  
3. **Среда разработки Java** – JDK 8+ и ваша любимая IDE (Eclipse, IntelliJ и т.д.).  

Теперь, когда всё готово, перейдём к коду.

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

Создайте Java‑проект и добавьте JAR‑файл Aspose.CAD в путь сборки. Затем укажите каталог, где находятся ваши DWG‑файлы.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

> **Совет:**уйте абсолютный путь или настройте относительный путь относительно папки ресурсов вашего проекта.

## Шаг 2: Загрузка DWG‑файла

Загрузите исходный DWG‑файл в объект `CadImage`, чтобы иметь возможность его обрабатывать.

```java
String sourceFilePath = dataDir + "Bottom_plate.dwg";
String outPath = dataDir + "Bottom_plate.pdf";
CadImage cadImage = (CadImage)Image.load(sourceFilePath);
```

## Шаг 3: Настройка параметров растеризации

Выберите слои, которые нужно включить, и задайте размер страницы, соответствующий оригинальному чертежу. Здесь мы включаем рендеринг скрытых линий, указывая нужный макет.

```java
List<String> list = Arrays.asList("Print","L1_RegMark","L2_RegMark");
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageHeight(cadImage.getHeight());
rasterizationOptions.setPageWidth(cadImage.getWidth()) ;
rasterizationOptions.setLayers(list);
```

## Шаг 4: Установка параметров PDF

Укажите Aspose.CAD растрировать векторные данные в PDF, используя макет «Model», чтобы скрытые линии оставались скрытыми.

```java
PdfOptions pdfOptions = new PdfOptions();
rasterizationOptions.setLayouts(new String[] { "Model" });
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Шаг 5: Сохранение результата

Наконец, экспортируйте DWG в PDF‑файл. Скрытые линии будут учитываться согласно выбранному макету.

```java
cadImage.save(outPath, pdfOptions);
System.out.println("\nThe DWG file exported successfully to PDF.\nFile saved at " + dataDir);
```

> **Распространённая ошибка:** Если не задать макет `"Model"`, все линии (включая скрытые) будут отображаться сплошными в PDF.

## Заключение

Теперь у вас есть полностью готовый к использованию метод **экспорта DWG в PDF** с поддержкой скрытых линий с помощью Aspose.CAD for Java. Этот подход можно интегрировать в инструменты пакетной обработки, веб‑сервисы или настольные приложения для автоматизации конвертации CAD в PDF.

## Часто задаваемые вопросы

### Q1: Можно ли использовать Aspose.CAD for Java с другими форматами CAD‑файлов?
A1: Да, Aspose.CAD поддерживает различные форматы CAD, такие как DWG, DXF, DWF и другие.

### Q2: Доступна ли бесплатная пробная версия Aspose.CAD for Java?
A2: Да, бесплатную пробную версию можно найти [здесь](https://releases.aspose.com/).

### Q3: Как получить поддержку по Aspose.CAD for Java?
A3: Посетите форум Aspose.CAD [здесь](https://forum.aspose.com/c/cad/19) для получения помощи от сообщества.

### Q4: Где найти подробную документацию по Aspose.CAD for Java?
A4: Обратитесь к документации [здесь](https://reference.aspose.com/cad/java/).

### Q5: Можно ли приобрести временную лицензию для Aspose.CAD for Java?
A5: Да, временную лицензию можно получить [здесь](https://purchase.aspose.com/temporary-license/).

### Q6: Работает ли этот метод для конвертации DWG в PDF в безголовой серверной среде?
A6: Абсолютно. Поскольку код использует только API Aspose.CAD, он работает без каких‑либо UI‑зависимостей, что делает его идеальным для серверной автоматизации.

---

**Последнее обновление:** 2026-01-02  
**Тестировано с:** Aspose.CAD for Java 24.12  
**Автор:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}