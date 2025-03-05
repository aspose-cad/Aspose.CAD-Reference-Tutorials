---
title: Легкий экспорт DGN в AutoCAD PDF с помощью Aspose.CAD для Java
linktitle: Экспорт DGN в формате AutoCAD в PDF
second_title: API Aspose.CAD Java
description: Изучите пошаговое руководство по экспорту файлов DGN в формат AutoCAD в PDF с помощью Aspose.CAD для Java. Легко улучшите возможности обработки САПР вашего Java-приложения.
type: docs
weight: 12
url: /ru/java/dgn-export-options/exporting-dgn-to-pdf/
---
## Введение

Добро пожаловать в это подробное руководство по использованию Aspose.CAD для Java для экспорта файлов DGN в формате AutoCAD в PDF. Если вы хотите расширить возможности вашего Java-приложения по обработке файлов САПР, Aspose.CAD — отличный выбор. В этом уроке мы шаг за шагом проведем вас через процесс экспорта файлов DGN.


## Предварительные условия
Прежде чем мы углубимся в руководство, убедитесь, что у вас есть следующие предварительные условия:
-  Библиотека Aspose.CAD: убедитесь, что у вас установлена библиотека Aspose.CAD для Java. Вы можете скачать его[здесь](https://releases.aspose.com/cad/java/).
- Каталог документов: настройте каталог документов, в котором будут храниться входные и выходные файлы.

## Импортировать пакеты

В свой Java-проект импортируйте необходимые пакеты для доступа к функциям Aspose.CAD:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Теперь давайте разобьем пример кода на несколько шагов:

## Шаг 1. Определите пути к файлам

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

Обязательно замените «Каталог ваших документов» фактическим путем, по которому расположены ваши файлы.

## Шаг 2. Загрузите изображение DGN.

```java
DgnImage objImage = (DgnImage) Image.load(fileName);
```

Загрузите файл DGN с помощью Aspose.CAD.

## Шаг 3. Установите параметры экспорта PDF

```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); // Экспорт определенных представлений
options.setVectorRasterizationOptions(vectorOptions);
```

Определите параметры экспорта PDF, включая размеры страницы и настройки макета.

## Шаг 4. Сохраните PDF-файл

```java
objImage.save(outFile, options);
```

Сохраните экспортированный PDF-файл.

Повторите эти шаги для любых дополнительных файлов DGN, которые вы хотите преобразовать. Поздравляем! Вы успешно экспортировали файлы DGN в формат AutoCAD в PDF с помощью Aspose.CAD для Java.

## Заключение

В этом руководстве мы рассмотрели, как использовать Aspose.CAD для Java для расширения возможностей вашего приложения по обработке файлов САПР. Благодаря простым инструкциям и примерам кода вы теперь можете легко экспортировать файлы DGN в формат AutoCAD в формате PDF.

## Часто задаваемые вопросы

### Вопрос 1: Совместим ли Aspose.CAD со всеми форматами файлов САПР?

О1: Да, Aspose.CAD поддерживает широкий спектр форматов САПР, обеспечивая универсальность при работе с различными типами файлов.

### Вопрос 2. Могу ли я настроить параметры экспорта PDF?

А2: Абсолютно. Как показано в руководстве, вы можете настроить такие параметры, как размеры и макеты страниц, в соответствии со своими требованиями.

### Вопрос 3. Где я могу найти дополнительную поддержку или помощь?

 A3: Посетите[Форум Aspose.CAD](https://forum.aspose.com/c/cad/19) за поддержку сообщества и обсуждения.

### В4: Доступна ли бесплатная пробная версия?

 О4: Да, вы можете получить доступ к бесплатной пробной версии.[здесь](https://releases.aspose.com/).

### В5: Как я могу получить временную лицензию?

 A5: Получите временную лицензию[здесь](https://purchase.aspose.com/temporary-license/).