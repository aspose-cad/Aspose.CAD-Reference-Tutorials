---
title: Добавление водяных знаков в чертежи САПР - Учебное пособие по Aspose.CAD для Java
linktitle: Добавить водный знак
second_title: API Aspose.CAD Java
description: Улучшите свои чертежи САПР с помощью персонализированных водяных знаков с помощью Aspose.CAD для Java. Следуйте нашему пошаговому руководству для бесшовной интеграции.
type: docs
weight: 12
url: /ru/java/other-cad-operations/add-watermark/
---
## Введение

Добро пожаловать в это подробное руководство по добавлению водяных знаков в чертежи САПР с помощью Aspose.CAD для Java. В этом руководстве вы узнаете, как эффективно интегрировать водяные знаки, улучшая ваши документы САПР с помощью персонализированных сообщений или фирменного стиля. Aspose.CAD для Java предоставляет мощный набор функций, упрощающих процесс добавления водяных знаков.

## Предварительные условия

Прежде чем мы углубимся в руководство, убедитесь, что у вас есть следующие предварительные условия:

-  Aspose.CAD для Java: убедитесь, что в вашей среде Java установлена библиотека Aspose.CAD. Вы можете скачать его[здесь](https://releases.aspose.com/cad/java/).
- Java Development Kit (JDK): убедитесь, что в вашей системе установлена последняя версия JDK.

## Импортировать пакеты

Для начала импортируйте в свой Java-проект необходимые пакеты Aspose.CAD:

```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.Cad3DPoint;
import com.aspose.cad.fileformats.cad.cadobjects.CadMText;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Шаг 1. Добавьте новый МТЕКСТ

```java
//добавить новый МТЕКСТ
CadMText watermark = new CadMText();
watermark.setText("Watermark message");
watermark.setInitialTextHeight(40);
watermark.setInsertionPoint(new Cad3DPoint(300, 40));
watermark.setLayerName("0");
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(watermark);
```

## Шаг 2. Добавьте простой объект, например текст

Вы также можете добавить более простой объект, например текст:

```java
// или добавьте более простой объект, например текст
CadText text = new CadText();
text.setDefaultValue("Watermark text");
text.setTextHeight(40);
text.setFirstAlignment(new Cad3DPoint(300, 40));
text.setLayerName("0") ;
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(text);
```

## Шаг 3. Экспорт в PDF

Экспортируйте чертеж САПР с добавленным водяным знаком в файл PDF:

```java
// экспортировать в pdf
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setLayouts(new String[]{"Model"});
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
cadImage.save(dataDir + "AddWatermark_out.pdf", pdfOptions);

```

## Заключение

Поздравляем! Вы успешно добавили водяные знаки на свои чертежи САПР с помощью Aspose.CAD для Java. Этот простой, но мощный процесс позволяет персонализировать дизайн или защитить его с помощью брендинга.

## Часто задаваемые вопросы

### Вопрос 1: Совместим ли Aspose.CAD со всеми форматами файлов САПР?

A1: Aspose.CAD поддерживает различные форматы САПР, включая DWG, DXF, DWT и DWF.

### В2: Могу ли я настроить внешний вид текста водяного знака?

О2: Да, вы имеете полный контроль над внешним видом водяного знака, включая размер, цвет и положение текста.

### Вопрос 3: Доступна ли пробная версия Aspose.CAD для Java?

 A3: Да, вы можете скачать пробную версию.[здесь](https://releases.aspose.com/).

### Вопрос 4: Как я могу получить поддержку Aspose.CAD?

 А4: Посетите[Форум Aspose.CAD](https://forum.aspose.com/c/cad/19) для поддержки сообщества.

### Вопрос 5: Где я могу найти полную документацию по Aspose.CAD для Java?

 A5: См.[документация](https://reference.aspose.com/cad/java/) для получения подробной информации.