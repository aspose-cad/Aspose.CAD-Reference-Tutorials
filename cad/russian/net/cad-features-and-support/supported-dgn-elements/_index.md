---
title: Поддерживаемые элементы DGN в Aspose.CAD для .NET
linktitle: Поддерживаемые элементы DGN
second_title: Aspose.CAD .NET — формат файлов CAD и BIM
description: Изучите мощные возможности Aspose.CAD for .NET для обработки файлов DGN. Следуйте нашему пошаговому руководству, чтобы без проблем работать с 2D- и 3D-элементами.
weight: 18
url: /ru/net/cad-features-and-support/supported-dgn-elements/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Поддерживаемые элементы DGN в Aspose.CAD для .NET

## Введение

Вы разработчик .NET и хотите беспрепятственно работать с файлами DGN? Aspose.CAD for .NET предоставляет надежное решение для эффективной обработки файлов DGN. В этом руководстве мы углубимся в поддерживаемые элементы DGN и проведем вас через процесс работы с Aspose.CAD для .NET.

## Предварительные условия

Прежде чем мы начнем, убедитесь, что у вас есть следующее:

- Базовые знания .NET-программирования.
- Visual Studio установлена на вашем компьютере.
-  Библиотека Aspose.CAD for .NET, которую вы можете скачать[здесь](https://releases.aspose.com/cad/net/).

## Импортировать пространства имен

Чтобы начать проект, импортируйте необходимые пространства имен в приложение .NET. Этот шаг гарантирует, что у вас есть доступ к функциям, предоставляемым Aspose.CAD для .NET.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.FileFormats.Dgn.DgnElements;
```

## Шаг 1. Загрузите файл DGN

Начните с загрузки существующего файла DGN в качестве CadImage в ваше .NET-приложение.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Ваш код здесь
}
```

## Шаг 2. Перебор элементов DGN

Перебирайте элементы DGN, используя цикл foreach. Aspose.CAD for .NET предоставляет множество типов элементов DGN, с которыми вы можете работать.

```csharp
foreach (DgnDrawingElementBase element in dgnImage.Elements)
{
    // Ваш код здесь
}
```

## Шаг 3. Обработка ранее поддерживаемых объектов

Обработка ранее поддерживаемых 2D-объектов, которые теперь поддерживаются и для 3D.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.Line:
    case DgnElementType.Ellipse:
    case DgnElementType.Curve:
    // Дополнительные случаи
        {
            // Ваш код здесь
            break;
        }
}
```

## Шаг 4. Обработка поддерживаемых 3D-объектов

Обработка поддерживаемых 3D-объектов, предоставляемых Aspose.CAD для .NET.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.SolidHeader3D:
    case DgnElementType.Cone:
    case DgnElementType.CellHeader:
        {
            // Ваш код здесь
            break;
        }
}
```

## Шаг 5: Экспортируйте и сохраните

Наконец, экспортируйте измененный файл DGN в растровое изображение и сохраните его в указанном каталоге.

```csharp
Console.WriteLine("\nThe DGN file exported successfully to raster image.\nFile saved at " + MyDir);
```

## Заключение

В этом руководстве мы изучили возможности Aspose.CAD для .NET по обработке и управлению файлами DGN. Следуя пошаговому руководству, вы сможете эффективно работать с поддерживаемыми элементами DGN, независимо от того, являются ли они 2D- или 3D-объектами. Aspose.CAD for .NET дает вам возможность легко интегрировать обработку файлов DGN в ваши .NET-приложения.

## Часто задаваемые вопросы

### Вопрос 1: Где я могу найти документацию по Aspose.CAD для .NET?

 A1: Вы можете найти документацию[здесь](https://reference.aspose.com/cad/net/).

### Вопрос 2: Как загрузить Aspose.CAD для .NET?

 A2: Вы можете скачать библиотеку[здесь](https://releases.aspose.com/cad/net/).

### Вопрос 3. Существует ли бесплатная пробная версия Aspose.CAD для .NET?

 О3: Да, вы можете получить доступ к бесплатной пробной версии.[здесь](https://releases.aspose.com/).

### Вопрос 4: Где я могу получить временные лицензии на Aspose.CAD for .NET?

 A4: Доступны временные лицензии.[здесь](https://purchase.aspose.com/temporary-license/).

### В5: Нужна помощь или есть вопросы?

 A5: Посетите сообщество Aspose.CAD for .NET.[форум поддержки](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
