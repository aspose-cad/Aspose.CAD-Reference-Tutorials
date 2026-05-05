---
date: 2026-03-29
description: Узнайте, как конвертировать DGN в PNG с помощью Aspose.CAD для .NET.
  Это руководство также охватывает поддержку форматов файлов CAD и полный набор поддерживаемых
  элементов DGN.
linktitle: Supported DGN Elements
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Конвертировать DGN в PNG с помощью Aspose.CAD для .NET
url: /ru/net/cad-features-and-support/supported-dgn-elements/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Конвертировать DGN в PNG с помощью Aspose.CAD для .NET

## Введение

Вы .NET разработчик, ищущий способ **convert DGN to PNG** без проблем? Aspose.CAD для .NET предоставляет надежное решение для эффективной работы с файлами DGN. В этом руководстве мы подробно рассмотрим поддерживаемые элементы DGN, проведем вас через процесс работы с Aspose.CAD для .NET и покажем, как экспортировать эти элементы в PNG‑изображения.

## Краткие ответы
- **What does Aspose.CAD do?** Он читает, изменяет и конвертирует файлы CAD/BIM (включая DGN) в растровые форматы, такие как PNG.  
- **Can I convert 2D and 3D DGN elements?** Да — поддерживаются как 2‑D, так и 3‑D сущности.  
- **Which .NET versions are required?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Do I need a license for testing?** Доступна бесплатная пробная версия; для продакшн‑использования требуется лицензия.  
- **Where do I get the library?** Скачайте её с официального сайта Aspose (см. ссылку ниже).

## Что такое «convert DGN to PNG»?
Конвертация DGN в PNG означает рендеринг векторного чертежа DGN (2‑D или 3‑D) в растровый формат изображения (PNG). Это полезно, когда необходимо отображать CAD‑чертежи в вебе, встраивать их в отчёты или генерировать миниатюры без необходимости использовать CAD‑просмотрщик.

## Зачем использовать Aspose.CAD для .NET для поддержки форматов CAD‑файлов?
- **Full CAD file format support** – DGN, DWG, DXF, DWF и др.  
- **No external dependencies** – чистая .NET‑библиотека, без установки нативных CAD‑компонентов.  
- **High‑fidelity rendering** – сохраняет толщины линий, цвета и 3‑D‑геометрию.  
- **Batch processing** – легко обрабатывать множество файлов в серверном приложении.

## Требования

Прежде чем начать, убедитесь, что у вас есть следующее:

- Базовые знания программирования на .NET.  
- Установленная Visual Studio.  
- Aspose.CAD for .NET library, which you can download [here](https://releases.aspose.com/cad/net/).

## Импортировать пространства имён

Чтобы быстро начать проект, импортируйте необходимые пространства имён в ваше .NET‑приложение. Этот шаг гарантирует доступ к функционалу, предоставляемому Aspose.CAD для .NET.

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

## Как конвертировать DGN в PNG

Ниже представлено пошаговое руководство, которое проведёт вас через загрузку файла DGN, перебор его элементов, обработку как 2‑D, так и 3‑D сущностей и, наконец, экспорт результата в растровое изображение PNG.

### Шаг 1: Загрузить файл DGN

Начните с загрузки существующего файла DGN как `DgnImage` в вашем .NET‑приложении.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Your code here
}
```

### Шаг 2: Перебрать элементы DGN

Перебирайте элементы DGN с помощью цикла `foreach`. Aspose.CAD для .NET предоставляет разнообразные типы элементов DGN, с которыми вы можете работать.

```csharp
foreach (DgnDrawingElementBase element in dgnImage.Elements)
{
    // Your code here
}
```

### Шаг 3: Обработать ранее поддерживаемые 2‑D сущности

Эти сущности теперь также поддерживаются при 3‑D рендеринге. Оператор switch позволяет ветвить логику в зависимости от типа элемента.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.Line:
    case DgnElementType.Ellipse:
    case DgnElementType.Curve:
    // Additional cases
        {
            // Your code here
            break;
        }
}
```

### Шаг 4: Обработать поддерживаемые 3‑D сущности

Aspose.CAD добавляет полную поддержку нескольких 3‑D элементов DGN. Расширьте оператор switch для их обработки по необходимости.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.SolidHeader3D:
    case DgnElementType.Cone:
    case DgnElementType.CellHeader:
        {
            // Your code here
            break;
        }
}
```

### Шаг 5: Экспортировать и сохранить как PNG

После всех необходимых манипуляций экспортируйте чертёж DGN в растровое изображение PNG и сохраните его в указанную директорию.

```csharp
Console.WriteLine("\nThe DGN file exported successfully to raster image.\nFile saved at " + MyDir);
```

> **Pro tip:** Используйте `Image.Save` с `new PngOptions()` для управления разрешением, цветом фона и другими настройками, специфичными для PNG.

## Обзор поддержки форматов CAD‑файлов

Aspose.CAD для .NET не ограничивается DGN. Он также поддерживает DWG, DXF, DWF и многие другие форматы CAD, предоставляя единый API для работы с широким спектром инженерных чертежей. Это делает его идеальным для проектов, требующих **поддержки форматов CAD‑файлов** по нескольким стандартам.

## Распространённые проблемы и решения

| Проблема | Причина | Решение |
|----------|---------|----------|
| **Изображение пустое** | Экспортировано с нулевым DPI | Укажите `ResolutionX` и `ResolutionY` в `PngOptions`. |
| **Отсутствует 3‑D геометрия** | Тип элемента не обработан в switch | Добавьте недостающий случай `DgnElementType` и отрисуйте соответствующим образом. |
| **Недостаток памяти при больших файлах** | Загрузка всего файла сразу | Обрабатывайте элементы пакетами или используйте потоковую обработку, где это возможно. |

## Часто задаваемые вопросы

### Q1: Где я могу найти документацию по Aspose.CAD для .NET?
A1: Вы можете найти документацию [here](https://reference.aspose.com/cad/net/).

### Q2: Как скачать Aspose.CAD для .NET?
A2: Вы можете скачать библиотеку [here](https://releases.aspose.com/cad/net/).

### Q3: Доступна ли бесплатная пробная версия Aspose.CAD для .NET?
A3: Да, вы можете получить бесплатную пробную версию [here](https://releases.aspose.com/).

### Q4: Где можно получить временные лицензии для Aspose.CAD для .NET?
A4: Временные лицензии доступны [here](https://purchase.aspose.com/temporary-license/).

### Q5: Нужна помощь или есть вопросы?
A5: Посетите сообщество Aspose.CAD для .NET [support forum](https://forum.aspose.com/c/cad/19).

---

**Последнее обновление:** 2026-03-29  
**Тестировано с:** Aspose.CAD for .NET 24.11  
**Автор:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}