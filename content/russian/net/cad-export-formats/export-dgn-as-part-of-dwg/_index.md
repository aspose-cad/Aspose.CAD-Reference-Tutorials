---
title: Экспорт DGN как части DWG в Aspose.CAD для .NET
linktitle: Экспорт DGN как части DWG
second_title: Aspose.CAD .NET — формат файлов CAD и BIM
description: Узнайте, как экспортировать DGN как часть DWG в Aspose.CAD для .NET. Следуйте нашему пошаговому руководству для бесшовной интеграции.
type: docs
weight: 11
url: /ru/net/cad-export-formats/export-dgn-as-part-of-dwg/
---
## Введение

В мире .NET-разработки Aspose.CAD выделяется как мощная библиотека для работы с файлами автоматизированного проектирования (САПР). Это руководство проведет вас через процесс экспорта файла DGN (Дизайн) как части файла DWG (Чертеж) с помощью Aspose.CAD для .NET. Независимо от того, являетесь ли вы опытным разработчиком или только начинаете, это пошаговое руководство поможет вам использовать возможности Aspose.CAD для эффективного решения этой конкретной задачи.

## Предварительные условия

Прежде чем приступить к изучению руководства, убедитесь, что у вас есть следующие предварительные условия:

-  Aspose.CAD для .NET: убедитесь, что у вас установлена библиотека Aspose.CAD для .NET. Вы можете скачать его[здесь](https://releases.aspose.com/cad/net/).

- Среда разработки: настройте предпочитаемую среду разработки .NET, например Visual Studio.

- Базовые знания C#: познакомьтесь с языком программирования C#.

## Импортировать пространства имен

В свой проект C# включите необходимые пространства имен для доступа к функциональности Aspose.CAD. Добавьте следующие директивы using в начале файла кода:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

Теперь давайте разобьем предоставленный код на несколько шагов:

## Шаг 1. Определите пути к файлам

```csharp
//Пути к входным и выходным файлам
string fileName = "BlockRefDgn.dwg";
string outPath = fileName + ".pdf";
```

## Шаг 2. Создайте экземпляр PdfOptions

```csharp
// Создайте экземпляр класса PdfOptions для экспорта DWG в PDF.
PdfOptions exportOptions = new PdfOptions();
```

## Шаг 3. Загрузите файл DWG

```csharp
// Загрузите существующий файл DWG как изображение и преобразуйте его в тип CadImage.
using (CadImage cadImage = (CadImage)Image.Load(fileName))
```

## Шаг 4. Перебор сущностей

```csharp
// Перебрать каждый объект внутри файла DWG.
foreach (CadBaseEntity baseEntity in cadImage.Entities)
```

## Шаг 5. Проверьте тип объекта

```csharp
// Проверьте, является ли объект определением изображения
if (baseEntity.TypeName == CadEntityTypeName.DGNUNDERLAY)
```

## Шаг 6: Получите путь подложки

```csharp
// Если это определение изображения, получите внешнюю ссылку на объект.
CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
Console.WriteLine(dgnFile.UnderlayPath);
```

## Шаг 7: Определите параметры растеризации

```csharp
// Определите настройки для объекта CadRasterizationOptions.
exportOptions.VectorRasterizationOptions = new CadRasterizationOptions()
{
    PageWidth = 1600,
    PageHeight = 1600,
    Layouts = new string[] { "Model" },
    AutomaticLayoutsScaling = false,
    NoScaling = true,
    BackgroundColor = Color.Black,
    DrawType = CadDrawTypeMode.UseObjectColor
};
```

## Шаг 8. Экспортируйте DWG в PDF

```csharp
// Экспортируйте DWG в PDF, вызвав метод Save.
cadImage.Save(outPath, exportOptions);
```

## Заключение

Поздравляем! Вы успешно прошли процесс экспорта файла DGN как части файла DWG с помощью Aspose.CAD для .NET. В этом руководстве представлены основные шаги и фрагменты кода для беспрепятственного решения этой конкретной задачи.

## Часто задаваемые вопросы

### Вопрос 1: Могу ли я использовать Aspose.CAD для .NET в своих коммерческих проектах?
 А1: Да, вы можете. Посещать[здесь](https://purchase.aspose.com/buy) изучить варианты лицензирования.

### Вопрос 2. Существуют ли какие-либо ограничения на размер файлов DWG, которые я могу обрабатывать?
О2: Aspose.CAD поддерживает обработку больших файлов DWG, но могут применяться аппаратные ограничения.

### В3: Доступна ли пробная версия?
A3: Да, вы можете получить бесплатную пробную версию.[здесь](https://releases.aspose.com/).

### Вопрос 4: Как я могу получить временные лицензии?
 A4: Можно получить временные лицензии.[здесь](https://purchase.aspose.com/temporary-license/).

### Вопрос 5. Куда я могу обратиться за помощью, если у меня возникнут проблемы?
 A5: Вы можете посетить форум Aspose.CAD.[здесь](https://forum.aspose.com/c/cad/19) для поддержки.