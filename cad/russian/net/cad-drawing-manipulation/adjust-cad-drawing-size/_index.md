---
title: Настройка размера чертежа САПР в Aspose.CAD для .NET
linktitle: Настройка размера чертежа САПР
second_title: Aspose.CAD .NET — формат файлов CAD и BIM
description: Узнайте, как легко корректировать размеры чертежей САПР в .NET с помощью Aspose.CAD. Следуйте нашему пошаговому руководству для плавного изменения размера.
weight: 10
url: /ru/net/cad-drawing-manipulation/adjust-cad-drawing-size/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Настройка размера чертежа САПР в Aspose.CAD для .NET

## Введение

Вы хотите плавно регулировать размер чертежей САПР в своих приложениях .NET? Aspose.CAD for .NET предоставляет надежное решение, позволяющее легко изменять размеры чертежей САПР. В этом руководстве мы проведем вас через весь процесс, разбив каждый шаг, чтобы вы поняли тонкости изменения размера чертежей САПР с помощью Aspose.CAD.

## Предварительные условия

Прежде чем мы углубимся в руководство, убедитесь, что у вас есть следующие предварительные условия:

- Библиотека Aspose.CAD for .NET: загрузите и установите библиотеку из[Страница загрузки Aspose.CAD для .NET](https://releases.aspose.com/cad/net/).
- Образец чертежа САПР. Убедитесь, что у вас есть образец файла чертежа САПР (например, «sample.dwg») в каталоге документов.

## Импортировать пространства имен

Начните с импорта необходимых пространств имен в ваше .NET-приложение. Этот шаг имеет решающее значение для доступа к функциям, предоставляемым Aspose.CAD для .NET.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Шаг 1. Загрузите чертеж САПР

Начните с загрузки чертежа САПР в экземпляр класса Aspose.CAD.Image. Убедитесь, что у вас правильный путь к файлу образца чертежа.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "sample.dwg";

// Загрузите чертеж САПР в экземпляр изображения.
using (var image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // Ваш код здесь...
}
```

## Шаг 2. Создайте BmpOptions

Создайте экземпляр класса BmpOptions, который отвечает за указание параметров при сохранении чертежа САПР в виде файла BMP.

```csharp
Aspose.CAD.ImageOptions.BmpOptions bmpOptions = new Aspose.CAD.ImageOptions.BmpOptions();
```

## Шаг 3. Установите параметры CadRasterizationOptions.

Создайте экземпляр класса CadRasterizationOptions и настройте его свойства для векторной растеризации.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions cadRasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
bmpOptions.VectorRasterizationOptions = cadRasterizationOptions;
```

## Шаг 4. Установите свойство UnitType

Задайте свойство UnitType CadRasterizationOptions, чтобы указать тип единицы измерения для изменения размера. В этом примере установлено значение «Сантиметр».

```csharp
cadRasterizationOptions.UnitType = Aspose.CAD.ImageOptions.UnitType.Centimeter;
```

## Шаг 5. Установите свойство макетов

Укажите макеты, которые вы хотите включить в рисунок с измененным размером, задав свойство «Макеты».

```csharp
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## Шаг 6: Экспорт в BMP

Наконец, сохраните макет с измененным размером как файл BMP, используя метод Save.

```csharp
string outPath = sourceFilePath + ".bmp";
image.Save(outPath, bmpOptions);
```

Теперь вы успешно отрегулировали размер вашего чертежа САПР с помощью Aspose.CAD for .NET!

## Заключение

В этом уроке мы рассмотрели процесс изменения размера чертежей САПР в .NET с помощью Aspose.CAD. Выполнив эти шаги, вы сможете легко интегрировать эту функцию в свои приложения, обеспечивая удобство работы с пользователем.

## Часто задаваемые вопросы

### Вопрос 1. Совместим ли Aspose.CAD for .NET со всеми форматами САПР?

 A1: Aspose.CAD for .NET поддерживает широкий спектр форматов САПР, включая DWG, DXF, DWF и другие. Проверить[документация](https://reference.aspose.com/cad/net/) для полного списка.

### Вопрос 2. Могу ли я изменить размер нескольких макетов одновременно?

О2: Да, вы можете изменить размер нескольких макетов, настроив массив макетов в CadRasterizationOptions.

### Вопрос 3. Где я могу получить поддержку Aspose.CAD для .NET?

 A3: Посетите[Форум Aspose.CAD](https://forum.aspose.com/c/cad/19) за общественную поддержку и помощь.

### В4: Доступна ли бесплатная пробная версия?

 A4: Да, вы можете изучить[бесплатная пробная версия](https://releases.aspose.com/) оценить возможности Aspose.CAD для .NET.

### Вопрос 5: Как я могу получить временную лицензию на Aspose.CAD для .NET?

 A5: Получите временную лицензию для целей тестирования.[здесь](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
