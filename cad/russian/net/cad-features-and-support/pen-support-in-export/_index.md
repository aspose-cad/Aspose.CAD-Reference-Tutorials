---
title: Увеличьте возможности экспорта САПР с помощью пользовательских параметров пера в Aspose.CAD для .NET
linktitle: Поддержка пера при экспорте
second_title: Aspose.CAD .NET — формат файлов CAD и BIM
description: Узнайте, как улучшить экспорт изображений САПР с помощью Aspose.CAD для .NET. Настройте параметры пера для создания потрясающих изображений в PDF, PNG, BMP и других форматах.
weight: 12
url: /ru/net/cad-features-and-support/pen-support-in-export/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Увеличьте возможности экспорта САПР с помощью пользовательских параметров пера в Aspose.CAD для .NET

## Введение

Aspose.CAD for .NET предоставляет мощный набор инструментов для работы с файлами автоматизированного проектирования (САПР), позволяя разработчикам беспрепятственно манипулировать и экспортировать изображения САПР. Одной из примечательных особенностей является поддержка пера во время экспорта, позволяющая пользователям настраивать параметры начала и конца перьев при экспорте изображений САПР в различные форматы, такие как PDF, PNG, BMP, GIF, JPEG2000, JPEG, PSD, TIFF и WMF.

В этом уроке мы углубимся в особенности поддержки пера при экспорте с использованием Aspose.CAD для .NET. Мы разберем каждый шаг, предоставив четкие объяснения и примеры, которые помогут вам в этом процессе.

## Предварительные условия

Прежде чем мы углубимся в руководство, убедитесь, что у вас есть следующие предварительные условия:

- Aspose.CAD for .NET установлен в вашей среде разработки. Вы можете скачать его с сайта[страница выпуска](https://releases.aspose.com/cad/net/).

- Базовое понимание форматов файлов САПР, в частности DXF (формат обмена чертежами).

- Практические знания языка программирования C#.

## Импортировать пространства имен

Для начала убедитесь, что вы импортировали необходимые пространства имен в свой проект C#:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Drawing;
using System.Drawing.Drawing2D;
```

## Шаг 1. Настройте каталог документов

Определите каталог, в котором находится ваш документ САПР:

```csharp
string MyDir = "Your Document Directory";
```

## Шаг 2. Загрузите изображение САПР.

Загрузите изображение САПР с помощью Aspose.CAD:

```csharp
string sourceFilePath = MyDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage)Image.Load(sourceFilePath);
```

## Шаг 3. Настройте параметры растеризации

Создайте параметры растеризации и PDF для настройки процесса экспорта:

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
PdfOptions pdfOptions = new PdfOptions();
```

## Шаг 4. Настройте параметры пера

Установите параметры начала и конца для ручек:

```csharp
rasterizationOptions.PenOptions = new PenOptions
{
   StartCap = LineCap.Flat,
   EndCap = LineCap.Flat
};
```

## Шаг 5. Примените параметры векторной растеризации

Примените параметры растеризации к параметрам PDF:

```csharp
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Шаг 6. Сохраните экспортированный PDF-файл

Сохраните изображение САПР с настроенными параметрами пера в виде файла PDF:

```csharp
cadImage.Save(MyDir + "9LHATT-A56_generated.pdf", pdfOptions);
```

## Заключение

В этом уроке мы рассмотрели поддержку пера в функции экспорта Aspose.CAD для .NET. Следуя пошаговому руководству, вы сможете легко настроить параметры начала и конца перьев, повысив гибкость экспорта изображений САПР.

Не стесняйтесь экспериментировать с различными вариантами пера, чтобы добиться желаемых визуальных эффектов в экспортированных изображениях.

## Часто задаваемые вопросы

### Вопрос 1. Могу ли я использовать эти параметры пера для других форматов изображений, кроме PDF?

О1: Да, параметры пера можно применять к различным форматам изображений, таким как PNG, BMP, GIF, JPEG и другим.

### Вопрос 2: Где я могу найти дополнительную документацию по Aspose.CAD для .NET?

 A2: См.[документация](https://reference.aspose.com/cad/net/) для получения подробной информации и примеров.

### Вопрос 3. Существует ли бесплатная пробная версия Aspose.CAD для .NET?

 О3: Да, вы можете получить доступ к бесплатной пробной версии.[здесь](https://releases.aspose.com/).

### Вопрос 4: Как я могу получить временные лицензии на Aspose.CAD для .NET?

 А4: Посетите[страница временной лицензии](https://purchase.aspose.com/temporary-license/) для вариантов временного лицензирования.

### Вопрос 5: Где я могу получить поддержку сообщества по Aspose.CAD for .NET?

 Ответ 5: Взаимодействуйте с сообществом на[Форум Aspose.CAD](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
