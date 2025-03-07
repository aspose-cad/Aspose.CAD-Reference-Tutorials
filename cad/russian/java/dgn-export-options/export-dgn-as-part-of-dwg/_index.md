---
title: Экспортируйте DGN в DWG с помощью Aspose.CAD для Java
linktitle: Экспорт DGN как части DWG
second_title: API Aspose.CAD Java
description: Узнайте, как экспортировать DGN как часть DWG с помощью Aspose.CAD для Java. Следуйте нашему пошаговому руководству для эффективного манипулирования файлами САПР.
weight: 10
url: /ru/java/dgn-export-options/export-dgn-as-part-of-dwg/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Экспортируйте DGN в DWG с помощью Aspose.CAD для Java

## Введение

В этом руководстве мы рассмотрим, как использовать Aspose.CAD для Java для экспорта файла DGN (MicroStation Design) как части файла DWG (чертеж AutoCAD). Aspose.CAD — мощная библиотека, предоставляющая комплексные функциональные возможности для работы с форматами файлов САПР. Это пошаговое руководство поможет вам понять процесс экспорта DGN как части DWG с использованием Java.

## Предварительные условия

Прежде чем мы углубимся в руководство, убедитесь, что у вас есть следующие предварительные условия:
1. Библиотека Aspose.CAD: Загрузите и установите библиотеку Aspose.CAD для Java. Вы можете найти библиотеку[здесь](https://releases.aspose.com/cad/java/).
2. Комплект разработки Java (JDK): убедитесь, что в вашей системе установлена Java.
3. Интегрированная среда разработки (IDE): выберите Java IDE, например Eclipse или IntelliJ, для более удобной разработки.

## Импортировать пакеты

В свой проект Java импортируйте необходимые пакеты Aspose.CAD, чтобы можно было манипулировать файлами САПР. Вот пример:

```java
import com.aspose.cad;
import com.aspose.cad.imageoptions;
import com.aspose.cad.fileformats.cad.cadconsts;
import com.aspose.cad.fileformats.cad;
import com.aspose.cad.fileformats.cad.cadobjects;
```

## Шаг 1. Установите пути к файлам

 Определите пути к входному и выходному файлу DWG. Обновите`dataDir`, `fileName` , и`outPath` переменные соответственно.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
String outPath = dataDir + "BlockRefDgn.dwg.pdf";
```

## Шаг 2. Создайте экземпляр PdfOptions

 Создайте экземпляр`PdfOptions` class, поскольку мы экспортируем файл DWG в формат PDF.

```java
PdfOptions exportOptions = new PdfOptions();
```

## Шаг 3. Загрузите файл DWG

 Загрузите существующий файл DWG как изображение и преобразуйте его в формат.`CadImage` тип.

```java
CadImage cadImage = (CadImage) Image.load(fileName);
```

## Шаг 4. Перебор сущностей

Просмотрите каждый объект внутри файла DWG и проверьте, является ли это определением изображения. Если да, получите внешнюю ссылку на объект.

```java
for (CadBaseEntity baseEntity : cadImage.getEntities()) {
    if (baseEntity.getTypeName() == CadEntityTypeName.DGNUNDERLAY) {
        CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
        System.out.println(dgnFile.getUnderlayPath());
    }
}
```

## Шаг 5: Определите параметры растеризации

 Определите настройки для`CadRasterizationOptions`объект, включая ширину, высоту страницы, макеты и цвет фона.

```java
CadRasterizationOptions vectorRasterizationOptions = new CadRasterizationOptions();
vectorRasterizationOptions.setPageWidth(1600);
vectorRasterizationOptions.setPageHeight(1600);
vectorRasterizationOptions.setLayouts(new String[] { "Model" });
vectorRasterizationOptions.setAutomaticLayoutsScaling(false);
vectorRasterizationOptions.setNoScaling(true);
vectorRasterizationOptions.setBackgroundColor(Color.getBlack());
vectorRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
```

## Шаг 6. Установите параметры векторной растеризации

Установите параметры векторной растеризации для экспорта.

```java
exportOptions.setVectorRasterizationOptions(vectorRasterizationOptions);
```

## Шаг 7. Экспорт DWG в PDF

 Наконец, экспортируйте DWG в PDF, вызвав`save` метод.

```java
cadImage.save(outPath, exportOptions);
```

## Заключение

Поздравляем! Вы успешно научились экспортировать файл DGN как часть файла DWG с помощью Aspose.CAD для Java. Эта мощная библиотека предоставляет широкие возможности для работы с файлами САПР, делая ваши задачи по манипулированию файлами САПР эффективными и простыми.

## Часто задаваемые вопросы

### Вопрос 1. Где я могу найти документацию по Aspose.CAD для Java?

 A1: документацию можно найти[здесь](https://reference.aspose.com/cad/java/).

### Вопрос 2. Как загрузить библиотеку Aspose.CAD для Java?

 A2: Вы можете скачать библиотеку с[эта ссылка](https://releases.aspose.com/cad/java/).

### Вопрос 3: Существует ли бесплатная пробная версия Aspose.CAD для Java?

 A3: Да, вы можете найти бесплатную пробную версию.[здесь](https://releases.aspose.com/).

### Вопрос 4: Где я могу получить временную лицензию на Aspose.CAD для Java?

 A4: Получите временную лицензию[здесь](https://purchase.aspose.com/temporary-license/).

### В5: Нужна помощь или есть вопросы?

 A5: Посетите форум поддержки сообщества Aspose.CAD.[здесь](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
