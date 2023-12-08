---
title: Экспорт встроенных файлов DGN — Учебное пособие по Aspose.CAD
linktitle: Экспорт встроенных файлов DGN
second_title: Aspose.CAD .NET — формат файлов CAD и BIM
description: Откройте для себя возможности Aspose.CAD для .NET. Научитесь легко экспортировать встроенные файлы DGN в PDF с помощью этого пошагового руководства.
type: docs
weight: 14
url: /ru/net/export-techniques/exporting-embedded-dgn-files/
---
## Введение

В динамичном мире разработки программного обеспечения Aspose.CAD для .NET выделяется как мощный инструмент для работы с файлами автоматизированного проектирования (САПР). Это руководство проведет вас через процесс экспорта встроенных файлов DGN с помощью Aspose.CAD для .NET. Независимо от того, являетесь ли вы опытным разработчиком или любопытным новичком, это пошаговое руководство поможет вам эффективно использовать возможности Aspose.CAD.

## Предварительные условия

Прежде чем приступить к изучению руководства, убедитесь, что у вас есть следующие предварительные условия:

1.  Aspose.CAD для .NET: загрузите и установите библиотеку с сайта[Aspose.CAD для .NET](https://releases.aspose.com/cad/net/).

2. Среда разработки: настройте среду разработки .NET с помощью Visual Studio или любой другой предпочтительной IDE.

3. Пример файла DXF: в этом уроке мы будем использовать файл «conic_pyramid.dxf». Убедитесь, что он доступен в указанном вами каталоге документов.

## Импортировать пространства имен

Обязательно импортируйте в свой код C# необходимые пространства имен:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
```

## Шаг 1. Загрузите файл DXF

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    //Здесь будет ваш код для дальнейших действий.
}
```

## Шаг 2. Установите параметры растеризации

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new[] { "Model" };
```

## Шаг 3. Установите параметры PDF

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Шаг 4. Сохраните в формате PDF.

```csharp
cadImage.Save(MyDir + "conic_pyramid.pdf", pdfOptions);
```

## Шаг 5. Отображение сообщения об успехе

```csharp
Console.WriteLine("\nThe DXF drawing exported successfully to PDF.\nFile saved at " + MyDir);
```

## Заключение

Поздравляем! Вы успешно экспортировали встроенный файл DGN в PDF с помощью Aspose.CAD для .NET. В этом руководстве описаны основные шаги, предоставляющие вам основу для изучения более продвинутых функций, предлагаемых Aspose.CAD.

## Часто задаваемые вопросы

### Вопрос 1: Могу ли я использовать Aspose.CAD для .NET с другими языками программирования?

О1: Aspose.CAD в основном поддерживает .NET, но Aspose предоставляет библиотеки для различных языков, включая Java и Python.

### Вопрос 2: Существует ли бесплатная пробная версия Aspose.CAD для .NET?

 О2: Да, вы можете получить бесплатную пробную версию на сайте[здесь](https://releases.aspose.com/).

### Вопрос 3: Где я могу найти подробную документацию по Aspose.CAD для .NET?

 A3: обратитесь к документации[здесь](https://reference.aspose.com/cad/net/).

### Вопрос 4: Как получить временную лицензию на Aspose.CAD для .NET?

 A4: Получите временную лицензию[здесь](https://purchase.aspose.com/temporary-license/).

### Вопрос 5: Нужна помощь или вы хотите взаимодействовать с сообществом?

A5: Посетите[Форум Aspose.CAD](https://forum.aspose.com/c/cad/19) за поддержку и обсуждения.