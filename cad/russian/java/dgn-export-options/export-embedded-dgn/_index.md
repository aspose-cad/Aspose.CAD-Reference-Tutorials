---
title: Экспортируйте встроенный DGN в PDF с помощью Aspose.CAD для Java
linktitle: Экспорт встроенного DGN
second_title: API Aspose.CAD Java
description: Изучите пошаговое руководство по экспорту встроенных файлов DGN в PDF с помощью Aspose.CAD для Java. Усовершенствуйте свои приложения Java с помощью удобной манипуляции с файлами САПР.
type: docs
weight: 11
url: /ru/java/dgn-export-options/export-embedded-dgn/
---
## Введение

Добро пожаловать в это подробное руководство по экспорту встроенных файлов DGN с помощью Aspose.CAD для Java. Aspose.CAD — это мощная библиотека, которая позволяет разработчикам Java беспрепятственно работать с файлами САПР. В этом руководстве мы покажем вам процесс экспорта встроенных файлов DGN в PDF, используя пошаговые инструкции. Независимо от того, являетесь ли вы опытным разработчиком или только начинаете, это руководство поможет вам использовать возможности Aspose.CAD для улучшения ваших Java-приложений.

## Предварительные условия

Прежде чем мы углубимся в руководство, убедитесь, что у вас есть следующие предварительные условия:
- Среда разработки Java: убедитесь, что на вашем компьютере установлена среда разработки Java.
-  Aspose.CAD for Java: Загрузите и установите библиотеку Aspose.CAD for Java с сайта[здесь](https://releases.aspose.com/cad/java/).

## Импортировать пакеты

Для начала вам необходимо импортировать необходимые пакеты в ваш Java-проект. Добавьте в свой код следующие операторы импорта:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Теперь давайте разобьем пример кода на несколько шагов:

## Шаг 1. Настройте пути ввода и вывода

Определите путь к каталогу, в котором находится ваш документ, и укажите имя входного файла DWG.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
```

## Шаг 2. Загрузите файл DWG

 Загрузите файл DWG в`Image` объект с помощью Aspose.CAD.

```java
Image objImage = Image.load(fileName);
```

## Шаг 3. Настройте параметры растеризации

Настройте параметры растеризации, например макеты, которые будут включены в экспорт.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setLayouts(new String[] {"Model"});
```

## Шаг 4. Настройте параметры PDF

Настройте параметры PDF, включая параметры векторной растеризации.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Шаг 5: Сохраните PDF-файл

Сохраните PDF-файл с настроенными параметрами.
```java
objImage.save(dataDir + "BlockRefDgn.pdf", pdfOptions);
```

## Заключение

Поздравляем! Вы успешно экспортировали встроенный файл DGN в PDF с помощью Aspose.CAD для Java. В этом руководстве описаны основные шаги по интеграции Aspose.CAD в ваше приложение Java для эффективного управления файлами САПР.

## Часто задаваемые вопросы

### Вопрос 1: Могу ли я использовать Aspose.CAD для Java в коммерческом проекте?

 О1: Да, Aspose.CAD for Java — это коммерческая библиотека. Вы можете получить лицензию от[здесь](https://purchase.aspose.com/buy).

### В2: Существует ли бесплатная пробная версия?

 О2: Да, вы можете получить доступ к бесплатной пробной версии Aspose.CAD для Java.[здесь](https://releases.aspose.com/).

### Вопрос 3: Как я могу получить поддержку Aspose.CAD для Java?

О3: Вы можете обратиться за поддержкой к сообществу Aspose.CAD на сайте[Форум](https://forum.aspose.com/c/cad/19).

### В4: Что делать, если мне нужна временная лицензия?

 A4: Вы можете получить временную лицензию[здесь](https://purchase.aspose.com/temporary-license/).

### В5: Где я могу найти документацию?

 A5: документация доступна.[здесь](https://reference.aspose.com/cad/java/).