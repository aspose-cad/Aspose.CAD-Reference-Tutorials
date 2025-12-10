---
date: 2025-12-10
description: Узнайте, как создавать PDF из CAD с помощью Aspose.CAD для Java с автоматическим
  масштабированием макета. Это пошаговое руководство покажет, как эффективно и надёжно
  экспортировать CAD в PDF.
linktitle: Setting Auto Layout Scaling
second_title: Aspose.CAD Java API
title: Создание PDF из CAD – автоматическое масштабирование макета с Aspose.CAD Java
url: /ru/java/advanced-cad-features/setting-auto-layout-scaling/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Создание PDF из CAD – Автоматическое масштабирование макета с Aspose.CAD Java

## Введение

Если вам нужно **create PDF from CAD** быстро и с идеальным масштабированием, Aspose.CAD for Java готов помочь. Auto Layout Scaling автоматически корректирует размеры макета, чтобы полученный PDF выглядел точно так, как задумано, независимо от исходного размера страницы CAD. В этом руководстве мы пройдем весь процесс — от загрузки DXF‑файла до экспорта PDF — подчеркивая возможности **export CAD to PDF** библиотеки.

## Быстрые ответы

- **Что делает Auto Layout Scaling?** Он автоматически изменяет размер макетов CAD, чтобы они соответствовали целевым размерам страницы при растеризации.  
- **Какие форматы можно конвертировать?** Любой формат, поддерживаемый Aspose.CAD (например, DXF, DWG, DWF), может быть преобразован в PDF.  
- **Нужна ли лицензия для продакшн?** Да, для использования в не‑оценочных целях требуется коммерческая лицензия.  
- **Сколько времени занимает конверсия?** Обычно менее секунды для стандартных файлов на современном оборудовании.  
- **Можно ли изменить размер страницы?** Да, пользовательские размеры страницы можно задать через `CadRasterizationOptions`.

## Что означает «create PDF from CAD»?

Создание PDF из CAD — это процесс преобразования векторного инженерного чертежа (DXF, DWG и т.п.) в PDF‑документ. PDF сохраняет визуальную точность оригинального чертежа и может быть просмотрен на любой платформе.

## Почему использовать Auto Layout Scaling?

- **Consistent output:** Гарантирует, что все макеты заполняют страницу PDF без ручных вычислений размеров.  
- **Time‑saving:** Убира вручную подбирать коэффициенты масштабирования для каждого чертежа.  
- **High quality:** Сохраняет толщину линий и точность геометрии при конвертации.

## Требования

1. **Aspose.CAD for Java Library** — загрузите последнюю версию со [страницы загрузки](https://releases.aspose.com/cad/java/).  
2. **Resource Directory** — создайте папку на компьютере для хранения CAD‑файлов; замените `"Your Document Directory"` в коде на путь к этой папке.  
3. **Sample CAD File** — в этом руководстве используется `conic_pyramid.dxf`, который включён в набор примеров Aspose.

## Импорт пространств имён

Сначала импортируйте необходимые классы. Это даст доступ к загрузке изображений, растеризации и экспорту в PDF.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Шаг 1: Загрузка CAD‑файла

Загрузка исходного файла — первый шаг в **how to export CAD** в PDF‑документ.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

## Шаг 2: Создание параметров растеризации

Определите целевые размеры страницы. Этот блок также можно использовать для **set CAD page size** вручную, если нужен пользовательский макет.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

## Шаг 3: Включение Auto Layout Scaling

Включите функцию автоматического масштабирования. Это ядро **how to set scaling** для конвертации CAD‑в‑PDF.

```java
rasterizationOptions.setAutomaticLayoutsScaling(true);
```

## Шаг 4: Создание параметров PDF

Свяжите настройки растеризации с параметрами экспорта PDF.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Шаг 5: Экспорт в PDF

Наконец, сохраните отрисованное изображение как PDF‑файл. Этот шаг завершает workflow **convert DXF to PDF**.

```java
image.save(dataDir + "result_out_.pdf", pdfOptions);
```

Повторите указанные шаги для любых дополнительных CAD‑файлов, которые необходимо обработать.

## Распространённые проблемы и их решение

| Симптом | Вероятная причина | Решение |
|---------|-------------------|---------|
| Пустой PDF | Параметры растеризации не заданы или путь к файлу неверен | Проверьте путь `srcFile` и убедитесь, что `setPageWidth/Height` не равны нулю |
| Искажённое масштабирование | `setAutomaticLayoutsScaling` оставлен `false` | Включите автоматическое масштабирование или вручную вычислите коэффициент масштабирования |
| Отсутствуют слои | Исходный DXF содержит неподдерживаемые сущности | Проверьте примечания к выпуску Aspose.CAD на предмет поддерживаемых типов сущностей |

## Часто задаваемые вопросы

### Q1: Совместим ли Aspose.CAD for Java со всеми форматами CAD‑файлов?

A1: Aspose.CAD for Java поддерживает различные форматы CAD, включая DWG, DXF и DWF.

### Q2: Можно ли дополнительно настроить параметры масштабирования?

A2: Да, класс `CadRasterizationOptions` предоставляет множество свойств для тонкой настройки масштабирования и других параметров.

### Q3: Где можно найти дополнительную документацию по Aspose.CAD for Java?

A3: Обратитесь к [документации](https://reference.aspose.com/cad/java/) для получения подробной информации и примеров.

### Q4: Есть ли бесплатная пробная версия Aspose.CAD for Java?

A4: Да, вы можете попробовать [бесплатную пробную версию](https://releases.aspose.com/) для оценки возможностей Aspose.CAD for Java.

### Q5: Как получить поддержку или принять участие в обсуждениях по Aspose.CAD for Java?

A5: Посетите [форум Aspose.CAD](https://forum.aspose.com/c/cad/19), чтобы связаться с сообществом и получить помощь.

**Дополнительные часто задаваемые вопросы**

**Q: Как конвертировать файл DWG в PDF вместо DXF?**  
A: Тот же код работает; просто измените расширение файла в `srcFile` на `.dwg`.

**Q: Можно ли задать пользовательский DPI для PDF более высокого разрешения?**  
A: Да, используйте `rasterizationOptions.setResolution(300);` (или любой другой необходимый DPI).

**Q: Возможно ли встраивание шрифтов в генерируемый PDF?**  
A: Aspose.CAD растеризует чертеж, поэтому шрифты отображаются как векторы; отдельное встраивание шрифтов не требуется.

## Заключение

Следуя этому руководству, вы теперь знаете, как **create PDF from CAD** с помощью Aspose.CAD for Java и Auto Layout Scaling. Процесс упрощает workflow **export CAD to PDF**, обеспечивает согласованное масштабирование и экономит ценное время разработки. Не стесняйтесь экспериментировать с различными размерами страниц, разрешениями и форматами CAD, чтобы подобрать оптимальное решение для вашего проекта.

---

**Last Updated:** 2025-12-10  
**Tested With:** Aspose.CAD for Java 24.12 (latest)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}