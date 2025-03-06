---
title: Экспорт DWG в PDF или растр с помощью Aspose.CAD для Java
linktitle: Экспорт DWG в PDF или растр
second_title: API Aspose.CAD Java
description: Изучите простой процесс экспорта файлов DWG в PDF или растровые изображения в Java с помощью Aspose.CAD. Это пошаговое руководство обеспечивает точность и эффективность.
weight: 13
url: /ru/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Экспорт DWG в PDF или растр с помощью Aspose.CAD для Java

## Введение

В динамичном мире автоматизированного проектирования (САПР) эффективная обработка чертежей имеет решающее значение. Aspose.CAD for Java предоставляет мощное решение для экспорта файлов DWG в PDF или растровые изображения. Это руководство проведет вас через весь процесс, гарантируя, что вы сможете использовать весь потенциал Aspose.CAD для Java.

## Предварительные условия

Прежде чем приступить к изучению руководства, убедитесь, что у вас есть следующее:

- Базовое понимание программирования на Java.
-  Установлена библиотека Aspose.CAD for Java. Если нет, скачайте его[здесь](https://releases.aspose.com/cad/java/).
- Файл DWG для целей тестирования. Вы можете использовать предоставленный файл «Bottom_plate.dwg».

## Импортировать пространства имен

В вашем проекте Java импортируйте необходимые пространства имен, чтобы запустить процесс:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## Шаг 1. Загрузите файл DWG

 Начните с загрузки файла DWG с помощью Aspose.CAD.`Image` сорт:

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

## Шаг 2: Определите тип устройства

Далее проверьте тип единицы измерения загруженного файла DWG:

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

## Шаг 3. Установите параметры растеризации

В зависимости от типа объекта настройте параметры растеризации:

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();

if (currentUnitIsMetric) {
    // Метрические единицы
    double metersCoeff = 1 / 1000.0;
    double scaleFactor = metersCoeff / currentUnitCoefficient;
    rasterizationOptions.setPageWidth((float)(210 * scaleFactor));
    rasterizationOptions.setPageHeight((float)(297 * scaleFactor));
    rasterizationOptions.setUnitType(UnitType.Millimeter);
} else {
    // Имперские единицы
    rasterizationOptions.setPageWidth((float)(8.27f / currentUnitCoefficient));
    rasterizationOptions.setPageHeight((float)(11.69f / currentUnitCoefficient));
    rasterizationOptions.setUnitType(UnitType.Inch);
}
```

## Шаг 4. Настройте параметры PDF

Настройте параметры экспорта PDF:

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

## Шаг 5. Сохраните в формате PDF.

Наконец, сохраните файл DWG в формате PDF:

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

И вот оно! Вы успешно экспортировали файл DWG в PDF с помощью Aspose.CAD для Java.

## Заключение

В этом руководстве представлено пошаговое руководство по использованию Aspose.CAD для Java для экспорта файлов DWG в PDF или растровые изображения. Эта библиотека упрощает процесс, позволяя эффективно обрабатывать чертежи САПР в ваших Java-приложениях.

## Часто задаваемые вопросы

### Вопрос 1: Могу ли я использовать Aspose.CAD для Java с другими платформами Java?

О1: Да, Aspose.CAD для Java легко интегрируется с популярными платформами Java.

### Вопрос 2: Доступна ли временная лицензия для Aspose.CAD для Java?

 О2: Да, вы можете получить временную лицензию.[здесь](https://purchase.aspose.com/temporary-license/).

### Вопрос 3. Где я могу найти поддержку Aspose.CAD для Java?

 A3: Посетите[Форум Aspose.CAD](https://forum.aspose.com/c/cad/19) за помощь сообщества.

### Вопрос 4: Как я могу приобрести лицензию на Aspose.CAD для Java?

 A4: Вы можете приобрести лицензию[здесь](https://purchase.aspose.com/buy).

### Вопрос 5: Какие модули поддерживает Aspose.CAD for Java?

A5: Aspose.CAD для Java поддерживает как метрические, так и британские единицы измерения.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
