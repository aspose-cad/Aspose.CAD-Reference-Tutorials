---
title: Установите размер и режим холста
linktitle: Установите размер и режим холста
second_title: API Aspose.CAD Java
description: Исследуйте возможности Aspose.CAD для Java с помощью нашего пошагового руководства по настройке размера и режима холста. Легко конвертируйте файлы САПР в форматы PDF и TIFF.
type: docs
weight: 16
url: /ru/java/advanced-cad-features/set-canvas-size-and-mode/
---
## Введение

Вы хотите использовать возможности Aspose.CAD для Java для улучшения процесса преобразования САПР? Это подробное руководство проведет вас через этапы настройки размера и режима холста с помощью Aspose.CAD для Java. Независимо от того, являетесь ли вы опытным разработчиком или только начинаете, это руководство предоставит вам необходимую информацию.

## Предварительные условия

Прежде чем приступить к изучению руководства, убедитесь, что у вас есть следующие предварительные условия:

-  Aspose.CAD для Java: убедитесь, что в вашей среде Java установлена библиотека Aspose.CAD. Вы можете скачать его[здесь](https://releases.aspose.com/cad/java/).

- Каталог документов: настройте каталог документов для хранения файлов САПР. Этот каталог будет упоминаться в шагах руководства.

Теперь давайте начнем с пошагового руководства.

## Импортировать пространства имен

На этом этапе мы импортируем необходимые пространства имен для запуска вашего проекта Aspose.CAD.
```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## Шаг 1. Импортируйте классы Aspose.CAD

```java
// Путь к каталогу ресурсов.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

 В этом фрагменте мы устанавливаем путь к каталогу ресурсов и загружаем файл DXF с помощью Aspose.CAD.`Image` сорт.

## Шаг 2. Установите свойства CadRasterizationOptions

```java
// Создайте экземпляр CadRasterizationOptions и установите его различные свойства.
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

 Здесь мы создаем экземпляр`CadRasterizationOptions` и настройте такие свойства, как ширина страницы, высота страницы и параметры масштабирования.

## Шаг 3. Создайте PdfOptions и установите VectorRasterizationOptions.

```java
// Создайте экземпляр PdfOptions.
PdfOptions pdfOptions = new PdfOptions();

// Установите свойство VectorRasterizationOptions.
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

 Теперь мы создаем`PdfOptions` экземпляр и установите его`VectorRasterizationOptions` свойство к ранее настроенному`CadRasterizationOptions`.

## Шаг 4. Экспорт в PDF

```java
// Экспорт САПР в PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

Наконец, мы сохраняем изображение САПР в файл PDF, используя указанные параметры.

## Шаг 5. Создайте TiffOptions и установите VectorRasterizationOptions.

```java
// Создайте экземпляр TiffOptions.
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Установите свойство VectorRasterizationOptions.
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

На этом этапе мы настраиваем`TiffOptions` экземпляр и настроить его`VectorRasterizationOptions` свойство.

## Шаг 6: Экспорт в TIFF

```java
// Экспорт САПР в TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

Наконец, мы сохраняем изображение САПР в файл TIFF, используя указанные параметры.

## Заключение

 Поздравляем! Вы успешно установили размер и режим холста с помощью Aspose.CAD для Java. Это руководство обеспечивает прочную основу для ваших проектов по преобразованию САПР. Узнайте больше о функциях и возможностях в[Документация Aspose.CAD](https://reference.aspose.com/cad/java/).

## Часто задаваемые вопросы

### Вопрос 1: Могу ли я использовать Aspose.CAD для Java с другими платформами Java?

О1: Да, Aspose.CAD предназначен для полной интеграции с различными платформами Java.

### Вопрос 2: Доступна ли временная лицензия для Aspose.CAD?

 О2: Да, вы можете получить временную лицензию.[здесь](https://purchase.aspose.com/temporary-license/).

### Вопрос 3: Где я могу получить поддержку сообщества для Aspose.CAD?

 A3: Посетите[Форум Aspose.CAD](https://forum.aspose.com/c/cad/19) за поддержку сообщества и обсуждения.

### Вопрос 4: Могу ли я попробовать Aspose.CAD бесплатно?

 А4: Абсолютно! Получите бесплатную пробную версию[здесь](https://releases.aspose.com/).

### Вопрос 5: Как мне приобрести Aspose.CAD для Java?

 A5: Приобретите продукт[здесь](https://purchase.aspose.com/buy).