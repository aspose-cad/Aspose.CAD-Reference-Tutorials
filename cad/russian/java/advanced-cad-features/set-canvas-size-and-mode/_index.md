---
date: 2025-12-10
description: Узнайте, как конвертировать CAD в PDF с помощью Aspose.CAD for Java,
  задавая размер холста, автоматическое масштабирование макета и экспортируя в TIFF.
linktitle: Convert CAD to PDF – Set Canvas Size & Mode
second_title: Aspose.CAD Java API
title: Преобразовать CAD в PDF – установить размер холста и режим (Java)
url: /ru/java/advanced-cad-features/set-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Установить размер холста и режим

## Введение

Ищете способ **convert CAD to PDF**, имея полный контроль над размером холста и режимом рендеринга? Это подробное руководство проведёт вас через точные шаги по установке размера холста в Java, включению автоматического масштабирования макета и последующему экспорту результата в форматы PDF и TIFF с использованием Aspose.CAD. Независимо от того, улучшаете ли вы производственный конвейер или экспериментируете с прототипом, вы найдёте здесь чёткие, практические инструкции.

## Быстрые ответы
- **Что означает “convert CAD to PDF”?** Преобразование CAD‑чертежа (например, DXF, DWG) в PDF‑документ, который можно просматривать на любой платформе.  
- **Могу ли я также экспортировать в TIFF?** Да — используйте `TiffOptions` для создания растровых изображений высокого разрешения.  
- **Какая опция управляет размером холста в Java?** `CadRasterizationOptions.setPageWidth/Height`.  
- **Что такое автоматическое масштабирование макета?** Флаг (`setAutomaticLayoutsScaling(true)`), который сохраняет исходные пропорции макета при изменении размера холста.  
- **Нужна ли лицензия для Aspose.CAD?** Для использования в продакшене требуется временная или постоянная лицензия.

## Что такое **convert CAD to PDF**?

Преобразование CAD в PDF означает взятие векторных инженерных чертежей и их рендеринг в виде страниц PDF, с сохранением линий, слоёв и геометрии, делая файл универсально доступным.

## Зачем устанавливать размер холста **java**?

Установка размера холста в Java позволяет задать разрешение вывода и размеры страницы, гарантируя, что полученный PDF или TIFF соответствует требованиям к печати или отображению. Это также даёт контроль над поведением масштабирования, что важно для чертежей большого формата.

## Требования

Прежде чем приступать к руководству, убедитесь, что у вас есть следующие требования:

- Aspose.CAD for Java: Убедитесь, что библиотека Aspose.CAD установлена в вашей Java‑среде. Вы можете скачать её [здесь](https://releases.aspose.com/cad/java/).
- Document Directory: Создайте каталог документов для хранения ваших CAD‑файлов. Этот каталог будет использоваться в шагах руководства.

Теперь давайте начнём пошаговое руководство.

## Импорт пространств имён

На этом шаге мы импортируем необходимые пространства имён для запуска вашего проекта Aspose.CAD.

```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## Шаг 1: Импорт классов Aspose.CAD

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

В этом фрагменте кода мы задаём путь к каталогу ресурсов и загружаем DXF‑файл с помощью класса `Image` из Aspose.CAD.

## Шаг 2: Установить свойства **CadRasterizationOptions** (set canvas size java)

```java
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

Здесь мы создаём экземпляр `CadRasterizationOptions` и настраиваем свойства, такие как ширина страницы, высота страницы и **automatic layout scaling**. Это ядро **configure canvas mode** для вашего преобразования.

## Шаг 3: Создать PdfOptions и установить VectorRasterizationOptions

```java
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Set the VectorRasterizationOptions property
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Теперь мы создаём экземпляр `PdfOptions` и задаём его свойство `VectorRasterizationOptions` ранее сконфигурированным `CadRasterizationOptions`.

## Шаг 4: Экспорт в PDF (convert cad to pdf)

```java
// Export CAD to PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

Наконец, мы сохраняем CAD‑изображение в PDF‑файл, используя указанные параметры, завершая процесс **convert CAD to PDF**.

## Шаг 5: Создать TiffOptions и установить VectorRasterizationOptions (export cad to tiff)

```java
// Create an instance of TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Set the VectorRasterizationOptions property
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

На этом шаге мы создаём экземпляр `TiffOptions` и настраиваем его свойство `VectorRasterizationOptions`.

## Шаг 6: Экспорт в TIFF

```java
// Export CAD to TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

Наконец, мы сохраняем CAD‑изображение в TIFF‑файл, используя указанные параметры, демонстрируя, как **export CAD to TIFF** после настройки размера холста.

## Распространённые проблемы и решения

| Проблема | Причина | Решение |
|----------|---------|---------|
| PDF‑файл пустой | `setNoScaling(true)` отключает рендеринг для некоторых чертежей | Удалите `setNoScaling(true)` или установите его в `false`. |
| Разрешение TIFF выглядит низким | Ширина/высота страницы слишком мала | Увеличьте значения `setPageWidth` / `setPageHeight`. |
| Макет выглядит искажённым | Автоматическое масштабирование макета отключено | Убедитесь, что `setAutomaticLayoutsScaling(true)` включён. |

## Заключение

Поздравляем! Вы успешно **convert CAD to PDF** и **export CAD to TIFF**, одновременно **set canvas size java**, включив **automatic layout scaling** и изучив, как **configure canvas mode** для высококачественного вывода. Это руководство предоставляет надёжную основу для ваших проектов по конвертации CAD. Исследуйте дополнительные возможности в [документации Aspose.CAD](https://reference.aspose.com/cad/java/).

## Вопросы и ответы

### Q1: Можно ли использовать Aspose.CAD для Java с другими Java‑фреймворками?

A1: Да, Aspose.CAD разработан для бесшовной интеграции с различными Java‑фреймворками.

### Q2: Доступна ли временная лицензия для Aspose.CAD?

A2: Да, вы можете получить временную лицензию [здесь](https://purchase.aspose.com/temporary-license/).

### Q3: Где я могу получить поддержку сообщества для Aspose.CAD?

A3: Посетите [форум Aspose.CAD](https://forum.aspose.com/c/cad/19) для получения поддержки сообщества и обсуждений.

### Q4: Можно ли попробовать Aspose.CAD бесплатно?

A4: Конечно! Получите бесплатную пробную версию [здесь](https://releases.aspose.com/).

### Q5: Как приобрести Aspose.CAD для Java?

A5: Приобретите продукт [здесь](https://purchase.aspose.com/buy).

**Q: Влияет ли размер холста на качество векторных данных в PDF?**  
A: Нет. Размер холста управляет размерами страницы; векторные данные остаются независимыми от разрешения, обеспечивая чёткий рендеринг при любом уровне масштабирования.

**Q: Можно ли задать другое DPI для вывода TIFF?**  
A: Да. Отрегулируйте `rasterizationOptions.setResolution(dpiValue)` перед созданием `TiffOptions`.

---

**Последнее обновление:** 2025-12-10  
**Тестировано с:** Aspose.CAD for Java 24.12  
**Автор:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}