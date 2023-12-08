---
title: Экспорт DGN в PDF в Aspose.CAD для .NET
linktitle: Экспорт DGN в PDF
second_title: Aspose.CAD .NET — формат файлов CAD и BIM
description: Узнайте, как легко экспортировать файлы DGN в PDF с помощью Aspose.CAD для .NET. Пошаговое руководство по беспрепятственному манипулированию файлами САПР.
type: docs
weight: 12
url: /ru/net/cad-export-formats/export-dgn-to-pdf/
---
## Введение

В мире .NET-разработки Aspose.CAD — это мощная библиотека, которая облегчает манипулирование и преобразование файлов САПР. Одна из распространенных задач, с которой часто сталкиваются разработчики, — это экспорт файлов DGN в формат PDF. В этом уроке мы шаг за шагом рассмотрим этот процесс, используя Aspose.CAD для .NET.

## Предварительные условия

Прежде чем приступить к изучению руководства, убедитесь, что у вас есть следующее:

- Практическое знание C# и .NET Framework.
-  Установлена библиотека Aspose.CAD for .NET. Вы можете скачать его[здесь](https://releases.aspose.com/cad/net/).
- Пример файла DGN, например «Nikon_D90_Camera.dgn» для этого урока.

## Импортировать пространства имен

В своем проекте C# начните с импорта необходимых пространств имен:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Шаг 1. Загрузите файл DGN

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage cadImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Ваш код здесь...
}
```

## Шаг 2. Настройте параметры растеризации

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## Шаг 3. Создайте параметры PDF

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Шаг 4. Сохраните в формате PDF.

```csharp
cadImage.Save(MyDir + "ExportDGNToPdf_out.pdf", pdfOptions);
```

## Заключение

Поздравляем! Вы успешно экспортировали файл DGN в PDF с помощью Aspose.CAD для .NET. В этом руководстве описаны основные шаги: от загрузки файла DGN до настройки параметров растеризации и сохранения вывода в формате PDF.

## Часто задаваемые вопросы

### Вопрос 1: Могу ли я использовать Aspose.CAD для .NET без предварительного знания САПР?

А1: Абсолютно! Aspose.CAD упрощает сложные задачи САПР, делая его доступным для разработчиков с различным опытом.

### Вопрос 2. Где я могу найти дополнительные примеры и документацию для Aspose.CAD?

 A2: Исследуйте[документация](https://reference.aspose.com/cad/net/) для подробных руководств и примеров.

### Вопрос 3: Существует ли бесплатная пробная версия Aspose.CAD?

A3: Да, вы можете получить бесплатную пробную версию.[здесь](https://releases.aspose.com/).

### Вопрос 4: Как я могу получить временные лицензии для Aspose.CAD?

 A4: Получите временные лицензии[здесь](https://purchase.aspose.com/temporary-license/).

### В5: Нужна помощь или есть вопросы?

A5: Посетите[Форум Aspose.CAD](https://forum.aspose.com/c/cad/19) для поддержки сообщества.