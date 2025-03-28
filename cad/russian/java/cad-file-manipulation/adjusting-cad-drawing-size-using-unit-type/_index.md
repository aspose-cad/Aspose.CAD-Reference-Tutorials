---
title: Настройка размера чертежа САПР с использованием типа единицы измерения в Aspose.CAD для Java
linktitle: Настройка размера чертежа САПР с использованием типа единицы измерения
second_title: API Aspose.CAD Java
description: Исследуйте возможности Aspose.CAD для Java, позволяющие легко регулировать размеры чертежей САПР. Следуйте нашему пошаговому руководству для точности и адаптируемости.
weight: 14
url: /ru/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Настройка размера чертежа САПР с использованием типа единицы измерения в Aspose.CAD для Java

## Введение

В постоянно развивающейся сфере компьютерного проектирования (САПР) точность и адаптируемость имеют первостепенное значение. Одним из распространенных требований является настройка размера чертежей САПР в зависимости от конкретных типов единиц измерения. Aspose.CAD for Java становится мощным союзником, предоставляющим широкие возможности для программного управления файлами САПР.

## Предварительные условия

Прежде чем приступить к изучению руководства, убедитесь, что у вас есть следующие предварительные условия:

- Среда разработки Java: убедитесь, что на вашем компьютере установлена функциональная среда разработки Java.

-  Библиотека Aspose.CAD для Java: загрузите и интегрируйте библиотеку Aspose.CAD в свой проект Java. Вы можете получить библиотеку[здесь](https://releases.aspose.com/cad/java/).

## Импортировать пространства имен

В свой код Java включите необходимые пространства имен для доступа к функциям Aspose.CAD. Добавьте следующий импорт:

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Теперь давайте разобьем процесс настройки размера чертежа САПР с использованием типа единицы измерения на выполнимые шаги:

## Шаг 1: Определите каталог данных

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

Задайте путь к каталогу, в котором находятся ваши файлы САПР.

## Шаг 2. Загрузите чертеж САПР

```java
String sourceFilePath = dataDir + "sample.dwg";
Image image = Image.load(sourceFilePath);
```

 Загрузите чертеж САПР с помощью Aspose.CAD.`Image` сорт.

## Шаг 3. Создайте параметры BMP

```java
BmpOptions bmpOptions = new BmpOptions();
```

 Создайте экземпляр`BmpOptions` класс для экспорта макета САПР в формат BMP.

## Шаг 4. Настройте параметры растеризации

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

 Создайте экземпляр`CadRasterizationOptions` и связать его с`BmpOptions` для векторной растеризации.

## Шаг 5: Установите тип устройства

```java
cadRasterizationOptions.setUnitType(UnitType.Centimeter);
```

Укажите желаемый тип единицы измерения для чертежа САПР. В этом примере мы установили значение «Сантиметр».

## Шаг 6: Установите макеты

```java
cadRasterizationOptions.setLayouts(new String[] { "Model" });
```

Определите макеты, которые будут учитываться при экспорте. В данном случае мы выбрали макет «Модель».

## Шаг 7: Экспорт в BMP

```java
String outPath = sourceFilePath + ".bmp";
image.save(outPath, bmpOptions);
```

Наконец, сохраните измененный чертеж САПР в формате BMP.

## Заключение

С Aspose.CAD for Java настройка размеров чертежей САПР становится проще простого. Это руководство проведет вас через весь процесс, подчеркнув важность каждого шага для достижения точных результатов.

## Часто задаваемые вопросы

### Вопрос 1: Могу ли я использовать Aspose.CAD для Java с другими языками программирования?

О1: Aspose.CAD в основном поддерживает Java, но существуют версии для других языков, например .NET.

### Вопрос 2: Существуют ли какие-либо варианты лицензирования для Aspose.CAD?

 О2: Да, вы можете изучить варианты лицензирования и приобрести Aspose.CAD.[здесь](https://purchase.aspose.com/buy).

### Вопрос 3: Существует ли бесплатная пробная версия Aspose.CAD?

 О3: Конечно, вы можете получить доступ к бесплатной пробной версии.[здесь](https://releases.aspose.com/).

### Вопрос 4: Как я могу получить поддержку Aspose.CAD для Java?

 A4: Посетите форум Aspose.CAD.[здесь](https://forum.aspose.com/c/cad/19) за всестороннюю поддержку.

### Вопрос 5: Могу ли я получить временную лицензию на Aspose.CAD?

 О5: Да, вы можете приобрести временную лицензию.[здесь](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
