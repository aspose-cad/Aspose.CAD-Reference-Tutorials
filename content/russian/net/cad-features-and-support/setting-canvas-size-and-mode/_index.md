---
title: Настройка размера и режима холста в Aspose.CAD для .NET
linktitle: Настройка размера и режима холста
second_title: Aspose.CAD .NET — формат файлов CAD и BIM
description: Изучите пошаговое руководство по настройке размера и режима холста в Aspose.CAD для .NET. С легкостью оптимизируйте рендеринг САПР с помощью этого подробного руководства.
type: docs
weight: 16
url: /ru/net/cad-features-and-support/setting-canvas-size-and-mode/
---
## Введение

Готовы ли вы раскрыть весь потенциал Aspose.CAD для .NET и произвести революцию в своем опыте CAD-рендеринга? В этом пошаговом руководстве мы углубимся в тонкости настройки размера и режима холста с помощью мощной библиотеки Aspose.CAD. Независимо от того, являетесь ли вы опытным разработчиком или только начинаете, это руководство проведет вас через весь процесс, гарантируя, что вы эффективно используете возможности Aspose.CAD.

## Предварительные условия

Прежде чем мы углубимся в руководство, убедитесь, что у вас есть следующие предварительные условия:

-  Библиотека Aspose.CAD: загрузите и установите библиотеку Aspose.CAD с сайта[Веб-сайт Aspose.CAD](https://releases.aspose.com/cad/net/).

- Среда разработки: убедитесь, что на вашем компьютере установлена среда разработки .NET.

-  Образец файла САПР. В этом уроке мы будем использовать образец файла DXF. Вы можете найти один в[Документация Aspose.CAD](https://reference.aspose.com/cad/net/).

## Импортировать пространства имен

Для начала импортируйте необходимые пространства имен в начале вашего .NET-приложения:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Шаг 1. Загрузите файл САПР

Начните с загрузки файла САПР, используя следующий код:

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    //Здесь будет ваш код для дальнейших действий.
}
```

## Шаг 2. Создайте параметры CadRasterizationOptions.

 Создайте экземпляр`CadRasterizationOptions` и установите его свойства:

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
rasterizationOptions.NoScaling = false;
```

## Шаг 3. Создайте параметры PDF

 Создайте экземпляр`PdfOptions` и установить его`VectorRasterizationOptions` свойство:

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Шаг 4. Экспорт в PDF

Экспортируйте файл САПР в PDF, используя настроенные параметры:

```csharp
image.Save(MyDir + "result_out.pdf", pdfOptions);
```

## Шаг 5: Создайте TiffOptions

 Создайте экземпляр`TiffOptions` и установить его`VectorRasterizationOptions` свойство:

```csharp
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Шаг 6: Экспорт в TIFF

Экспортируйте файл CAD в TIFF, используя настроенные параметры:

```csharp
image.Save(MyDir + "result_out.tiff", tiffOptions);
```

## Заключение

Поздравляем! Вы успешно установили размер и режим холста в Aspose.CAD для .NET. Эта мощная функция открывает целый мир возможностей для рендеринга САПР. Поэкспериментируйте с различными вариантами и раскройте весь потенциал Aspose.CAD в своих .NET-приложениях.

## Часто задаваемые вопросы

### Вопрос 1: Могу ли я использовать Aspose.CAD с другими библиотеками .NET?

О1: Да, Aspose.CAD легко интегрируется с другими библиотеками .NET, предоставляя расширенные возможности для манипулирования САПР.

### Вопрос 2: Доступна ли бесплатная пробная версия Aspose.CAD?

 О2: Да, вы можете изучить возможности Aspose.CAD с помощью бесплатной пробной версии. Посещать[здесь](https://releases.aspose.com/) для начала.

### Вопрос 3: Как я могу получить поддержку Aspose.CAD?

 A3: Для получения поддержки и обсуждения посетите[Форум Aspose.CAD](https://forum.aspose.com/c/cad/19).

### Вопрос 4: Где я могу найти подробную документацию по Aspose.CAD?

 А4: См.[Документация Aspose.CAD](https://reference.aspose.com/cad/net/) для получения подробной информации и примеров.

### Вопрос 5: Как мне приобрести Aspose.CAD для .NET?

 A5: Чтобы приобрести Aspose.CAD, посетите[страница покупки](https://purchase.aspose.com/buy).