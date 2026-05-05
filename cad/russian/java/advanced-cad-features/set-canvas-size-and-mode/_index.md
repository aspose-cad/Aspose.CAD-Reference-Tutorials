---
date: 2026-02-15
description: Узнайте, как задать размер страницы PDF и конвертировать CAD в PDF с
  помощью Aspose.CAD для Java, используя автоматическое масштабирование макета и экспорт
  в TIFF.
linktitle: Set PDF Page Size – Convert CAD to PDF
second_title: Aspose.CAD Java API
title: Задать размер страницы PDF – Конвертировать CAD в PDF (Java)
url: /ru/java/advanced-cad-features/set-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Установить размер холста и режим

## Введение

Если вам нужно **установить размер страницы PDF** при конвертации чертежей CAD в PDF, вы попали по адресу. В этом руководстве мы покажем, как использовать Aspose.CAD for Java для задания точных размеров холста, включения автоматического масштабирования компоновки и последующего экспорта результата в PDF и TIFF. Независимо от того, готовите ли вы инженерные схемы к печати или создаёте миниатюры для веб‑галереи, контроль над размером страницы и разрешением вывода имеет решающее значение.

## Быстрые ответы
- **Что означает «конвертировать CAD в PDF»?** Преобразование чертежа CAD (например, DXF, DWG) в PDF‑документ, который можно просматривать на любой платформе.  
- **Можно ли также экспортировать в TIFF?** Да — используйте `TiffOptions` для создания растровых изображений высокого разрешения.  
- **Какая опция управляет размером холста в Java?** `CadRasterizationOptions.setPageWidth/Height`.  
- **Что такое автоматическое масштабирование компоновки?** Флаг (`setAutomaticLayoutsScaling(true)`), сохраняющий оригинальные пропорции компоновки при изменении размера холста.  
- **Нужна ли лицензия для Aspose.CAD?** Для использования в продакшене требуется временная или постоянная лицензия.

## Как установить размер страницы PDF при конвертации CAD в PDF (Java)

Установка размера страницы PDF (или размера холста) позволяет задать окончательные размеры документа, что особенно полезно, когда необходимо **изменить размеры PDF** в соответствии со стандартами печати или требованиями интерфейса. Ниже мы пройдем каждый шаг, объясняя *почему* за каждой строкой кода.

## Что такое **convert CAD to PDF**?

Конвертация CAD в PDF означает взятие векторных инженерных чертежей и их рендеринг в виде страниц PDF, при этом сохраняются линии, слои и геометрия, а файл становится доступным для всех.

## Почему устанавливать размер холста **java**?

Установка размера холста в Java позволяет определить разрешение вывода и размеры страницы, гарантируя, что полученный PDF или TIFF соответствуют вашим требованиям к печати или отображению. Это также дает контроль над поведением масштабирования, что критично для чертежей большого формата.

## Предварительные требования

Прежде чем приступить к руководству, убедитесь, что выполнены следующие условия:

- Aspose.CAD for Java: Убедитесь, что библиотека Aspose.CAD установлена в вашей среде Java. Вы можете скачать её [здесь](https://releases.aspose.com/cad/java/).
- Каталог документов: Создайте каталог для хранения ваших файлов CAD. Этот каталог будет использоваться в шагах руководства.

Теперь приступим к пошаговому руководству.

## Импорт пространств имён

На этом этапе мы импортируем необходимые пространства имён для начала работы над проектом Aspose.CAD.

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

В этом фрагменте кода мы задаём путь к каталогу ресурсов и загружаем файл DXF с помощью класса `Image` из Aspose.CAD.

## Шаг 2: Установить свойства **CadRasterizationOptions** (set canvas size java)

```java
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

Здесь мы создаём экземпляр `CadRasterizationOptions` и настраиваем такие свойства, как ширина страницы, высота страницы и **автоматическое масштабирование компоновки**. Это ядро **configure canvas mode** для вашей конвертации.

## Шаг 3: Создать PdfOptions и установить VectorRasterizationOptions

```java
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Set the VectorRasterizationOptions property
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Теперь мы создаём объект `PdfOptions` и задаём его свойство `VectorRasterizationOptions` ранее сконфигурированному `CadRasterizationOptions`.

## Шаг 4: Экспорт в PDF (convert cad to pdf)

```java
// Export CAD to PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

Наконец, сохраняем изображение CAD в файл PDF, используя указанные параметры, завершая процесс **convert CAD to PDF**.

## Шаг 5: Создать TiffOptions и установить VectorRasterizationOptions (export cad to tiff)

```java
// Create an instance of TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Set the VectorRasterizationOptions property
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

На этом этапе мы создаём объект `TiffOptions` и настраиваем его свойство `VectorRasterizationOptions`.

## Шаг 6: Экспорт в TIFF

```java
// Export CAD to TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

В конце сохраняем изображение CAD в файл TIFF с указанными параметрами, демонстрируя, как **export CAD to TIFF** после настройки размера холста.

## Распространённые проблемы и решения

| Проблема | Причина | Решение |
|----------|----------|----------|
| PDF выводится пустым | `setNoScaling(true)` отключает рендеринг для некоторых чертежей | Удалите `setNoScaling(true)` или установите его в `false`. |
| Разрешение TIFF выглядит низким | Ширина/высота страницы слишком малы | Увеличьте значения `setPageWidth` / `setPageHeight`. |
| Компоновка искажена | Отключено автоматическое масштабирование компоновки | Убедитесь, что включён `setAutomaticLayoutsScaling(true)`. |

## Почему следует регулировать размер холста и DPI?

Изменение размера холста напрямую влияет на разрешение растеризации вывода. Если нужно **увеличить разрешение TIFF**, просто увеличьте значения `setPageWidth` / `setPageHeight` или вызовите `rasterizationOptions.setResolution(300)` перед созданием `TiffOptions`. Это даст вам растровые изображения высокого качества, подходящие для печати или детального анализа.

## Часто задаваемые вопросы

### Q1: Можно ли использовать Aspose.CAD for Java с другими Java‑фреймворками?

A1: Да, Aspose.CAD разработан для бесшовной интеграции с различными Java‑фреймворками.

### Q2: Доступна ли временная лицензия для Aspose.CAD?

A2: Да, временную лицензию можно получить [здесь](https://purchase.aspose.com/temporary-license/).

### Q3: Где можно получить поддержку сообщества для Aspose.CAD?

A3: Посетите [форум Aspose.CAD](https://forum.aspose.com/c/cad/19) для получения поддержки и обсуждений.

### Q4: Можно ли попробовать Aspose.CAD бесплатно?

A4: Конечно! Получите бесплатную пробную версию [здесь](https://releases.aspose.com/).

### Q5: Как приобрести Aspose.CAD for Java?

A5: Приобрести продукт можно [здесь](https://purchase.aspose.com/buy).

**Дополнительные вопросы и ответы**

**В: Влияет ли размер холста на качество векторных элементов в PDF?**  
О: Нет. Размер холста определяет размеры страницы; векторные данные остаются независимыми от разрешения, обеспечивая чёткое отображение при любом масштабе.

**В: Можно ли задать другое DPI для вывода TIFF?**  
О: Да. Отрегулируйте `rasterizationOptions.setResolution(dpiValue)` перед созданием `TiffOptions`.

**В: Как **изменить размеры PDF** для уже существующего PDF без повторного рендеринга CAD?**  
О: Используйте Aspose.PDF, загрузите сгенерированный PDF и вызовите `pdf.getPages().setPageSize(PageSize.A4)` или задайте пользовательский размер.

**В: Какой лучший способ **конвертировать dxf в pdf**, сохраняя слои?**  
О: Оставьте `setAutomaticLayoutsScaling(true)` и избегайте `setNoScaling(true)`; это сохраняет видимость слоёв и точность компоновки.

## Заключение

Поздравляем! Вы успешно **convert CAD to PDF** и **export CAD to TIFF**, одновременно **set canvas size java**, включив **automatic layout scaling**, и научились **configure canvas mode** для получения высококачественного вывода. Это руководство закладывает прочную основу для ваших проектов по конвертации CAD. Исследуйте дополнительные возможности в [документации Aspose.CAD](https://reference.aspose.com/cad/java/).

---

**Последнее обновление:** 2026-02-15  
**Тестировано с:** Aspose.CAD for Java 24.12  
**Автор:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}