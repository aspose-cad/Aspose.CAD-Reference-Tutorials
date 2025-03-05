---
title: Создание одного PDF-файла с разными макетами — Руководство Aspose.CAD
linktitle: Создание одного PDF-файла с разными макетами
second_title: Aspose.CAD .NET — формат файлов CAD и BIM
description: Создайте один PDF-файл с разными макетами, используя Aspose.CAD для .NET. Следуйте нашему пошаговому руководству для плавной интеграции и эффективного создания PDF-файлов.
type: docs
weight: 13
url: /ru/net/advanced-cad-techniques/creating-single-pdf-with-different-layouts/
---
## Введение

Вы хотите создать один PDF-документ из чертежа САПР с различными макетами, используя Aspose.CAD для .NET? Это пошаговое руководство проведет вас через весь процесс, поможет добиться плавной интеграции и эффективного создания PDF-файлов. Aspose.CAD для .NET предоставляет мощные функции для программного управления чертежами САПР, и в этом руководстве мы сосредоточимся на создании одного PDF-файла с различными макетами.

## Предварительные условия

Прежде чем приступить к изучению руководства, убедитесь, что у вас есть следующие предварительные условия:

-  Aspose.CAD для .NET: убедитесь, что у вас установлен Aspose.CAD для .NET. Вы можете скачать его с[здесь](https://releases.aspose.com/cad/net/).

- Среда разработки: настройте среду разработки .NET и получите базовое представление о программировании на C#.

## Импортировать пространства имен

В свой проект C# включите необходимые пространства имен для использования функций Aspose.CAD for .NET:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Шаг 1. Загрузите изображение САПР.

```csharp
// Путь к каталогу документов.
string MyDir = "Your Document Directory";

using (CadImage cadImage = (CadImage)Image.Load(MyDir + "City skyway map.dwg"))
{
    // Здесь находится ваш код для шага 1.
}
```

## Шаг 2. Настройте параметры растеризации

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1000;
rasterizationOptions.PageHeight = 1000;

// Нестандартные размеры для нескольких макетов
rasterizationOptions.LayoutPageSizes.Add("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.LayoutPageSizes.Add("8.5 x 11 Plot", new SizeF(1000, 100));
```

## Шаг 3. Определите параметры PDF

```csharp
PdfOptions pdfOptions = new PdfOptions() { VectorRasterizationOptions = rasterizationOptions };
```

## Шаг 4. Сохраните в формате PDF.

```csharp
cadImage.Save(MyDir + "singlePDF_out.pdf", pdfOptions);
```

Теперь вы успешно создали один PDF-документ с разными макетами, используя Aspose.CAD для .NET. Не стесняйтесь изучать дополнительные функции и настраивать код в соответствии с вашими конкретными требованиями.

## Заключение

В этом уроке мы рассмотрели процесс создания одного PDF-файла из чертежа САПР с различными макетами с использованием Aspose.CAD для .NET. Эта мощная библиотека упрощает задачи манипулирования САПР и обеспечивает гибкость для различных сценариев.

## Часто задаваемые вопросы

### Вопрос 1: Могу ли я использовать Aspose.CAD для .NET с другими форматами САПР?

О1: Да, Aspose.CAD for .NET поддерживает различные форматы САПР, такие как DWG, DXF, DGN и другие.

### В2: Доступна ли бесплатная пробная версия?

 О2: Да, вы можете воспользоваться бесплатной пробной версией.[здесь](https://releases.aspose.com/).

### Вопрос 3: Как я могу получить поддержку Aspose.CAD для .NET?

 A3: Посетите[Форум Aspose.CAD](https://forum.aspose.com/c/cad/19) для поддержки сообщества.

### В4: Где я могу найти подробную документацию?

 A4: обратитесь к документации.[здесь](https://reference.aspose.com/cad/net/).

### Вопрос 5: Могу ли я приобрести лицензию на Aspose.CAD для .NET?

 A5: Да, вы можете купить лицензию.[здесь](https://purchase.aspose.com/buy).