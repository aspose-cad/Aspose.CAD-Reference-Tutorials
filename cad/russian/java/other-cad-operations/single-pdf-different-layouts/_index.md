---
title: Создание динамических PDF-файлов с помощью Aspose.CAD для Java
linktitle: Один PDF-файл с разными макетами
second_title: API Aspose.CAD Java
description: Создавайте потрясающие PDF-файлы с разнообразными макетами на основе чертежей САПР с помощью Aspose.CAD для Java. Простая интеграция и мощные функции для разработчиков Java.
weight: 16
url: /ru/java/other-cad-operations/single-pdf-different-layouts/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Создание динамических PDF-файлов с помощью Aspose.CAD для Java

## Введение

Добро пожаловать в мир Aspose.CAD для Java, мощной библиотеки, которая позволяет разработчикам легко манипулировать чертежами САПР. В этом уроке мы углубимся в создание отдельных PDF-файлов с разными макетами с помощью Aspose.CAD для Java. Независимо от того, являетесь ли вы опытным разработчиком или только начинаете, это пошаговое руководство проведет вас через весь процесс.

## Предварительные условия

Прежде чем мы отправимся в это путешествие, убедитесь, что у вас есть следующие предварительные условия:
- Среда Java: убедитесь, что на вашем компьютере установлена Java.
-  Библиотека Aspose.CAD: загрузите и установите библиотеку Aspose.CAD для Java с сайта[ссылка для скачивания](https://releases.aspose.com/cad/java/).
- Каталог документов: создайте каталог для чертежей DWG.

## Импортировать пакеты

В свой Java-проект импортируйте необходимые пакеты:

```java
import com.aspose.cad.Image;
import com.aspose.cad.SizeF;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.VectorRasterizationOptions;
```

## Шаг 1. Загрузите чертеж САПР

 Начните с загрузки чертежа САПР в`CadImage` объект:

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
CadImage cadImage = (CadImage)Image.load(dataDir + "City skyway map.dwg");
```

## Шаг 2. Настройте параметры растеризации

Настройте параметры растеризации для изображения САПР:

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1000);
rasterizationOptions.setPageHeight(1000);
```

## Шаг 3. Настройка размеров страницы макета

Определите нестандартные размеры для нескольких макетов на чертеже САПР:

```java
rasterizationOptions.getLayoutPageSizes().addItem("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.getLayoutPageSizes().addItem("8.5 x 11 Plot", new SizeF(1000, 100));
```

## Шаг 4. Установите параметры PDF

Настройте параметры PDF, включая настройки растеризации:

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Шаг 5. Сохраните в формате PDF.

Сохраните обработанное изображение САПР в формате PDF:

```java
cadImage.save(dataDir + "singlePDF_out.pdf", pdfOptions);
```

Поздравляем! Вы успешно создали один PDF-файл с разными макетами, используя Aspose.CAD для Java.

## Заключение

В этом руководстве мы рассмотрели плавную интеграцию Aspose.CAD для Java для создания PDF-файлов с различными макетами на основе чертежей САПР. Гибкость и надежные функции библиотеки делают ее идеальным выбором для задач манипулирования САПР.

## Часто задаваемые вопросы

### Вопрос 1: Могу ли я использовать Aspose.CAD для Java с другими библиотеками Java?

О1: Да, Aspose.CAD for Java предназначен для полной интеграции с другими библиотеками Java, обеспечивая обширную функциональность.

### В2: Доступна ли пробная версия?

 А2: Абсолютно! Вы можете получить доступ к бесплатной пробной версии[здесь](https://releases.aspose.com/).

### В3: Где я могу найти дополнительную поддержку?

 A3: Посетите[Форум Aspose.CAD](https://forum.aspose.com/c/cad/19) за поддержку сообщества и обсуждения.

### Вопрос 4: Как получить временную лицензию?

 A4: Вы можете получить временную лицензию[здесь](https://purchase.aspose.com/temporary-license/).

### В5: Где я могу приобрести полную версию?

A5: Приобретите полную версию Aspose.CAD для Java.[здесь](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
