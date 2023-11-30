---
title: Экспорт DWG в PDF или растровые изображения — Руководство Aspose.CAD
linktitle: Экспорт DWG в PDF или растровые изображения
second_title: Aspose.CAD .NET — формат файлов CAD и BIM
description: Изучите подробное руководство по экспорту DWG в PDF или растровые изображения с помощью Aspose.CAD для .NET. Изучите шаги, предварительные требования и освойте работу с этой мощной библиотекой.
type: docs
weight: 11
url: /ru/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/
---
## Введение

Вы хотите легко конвертировать файлы DWG в PDF или растровые изображения в своем приложении .NET? Не смотрите дальше! Это пошаговое руководство проведет вас через весь процесс с использованием мощной библиотеки Aspose.CAD для .NET. Независимо от того, являетесь ли вы опытным разработчиком или только начинаете, это руководство подойдет для всех уровней навыков.

## Предварительные условия

Прежде чем мы углубимся в руководство, убедитесь, что у вас есть следующее:

- Базовое понимание программирования .NET.
-  Установлена библиотека Aspose.CAD for .NET. Если нет, скачайте его[здесь](https://releases.aspose.com/cad/net/).
- Ваша любимая интегрированная среда разработки (IDE), настроенная для разработки .NET.

## Импортировать пространства имен

Давайте начнем с импорта необходимых пространств имен в ваш проект .NET. Это гарантирует, что у вас есть доступ к функциям Aspose.CAD в вашем коде.

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

## Шаг 1. Загрузите файл DWG

Начните с загрузки файла DWG, который вы хотите конвертировать. Замените «Каталог вашего документа» на путь к файлу DWG.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Здесь находится ваш код для загрузки DWG.
}
```

## Шаг 2. Настройте экспорт PDF

Теперь давайте настроим параметры экспорта PDF. В этом примере показано, как настроить макет и выполнить преобразование единиц измерения.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };

// Проверьте и определите систему единиц
bool currentUnitIsMetric = false;
double currentUnitCoefficient = 1.0;
DefineUnitSystem(cadImage.UnitType, out currentUnitIsMetric, out currentUnitCoefficient);

// Здесь находится ваш код для настройки экспорта PDF.
```

## Шаг 3. Экспорт в PDF

Выполните экспорт в PDF, используя настроенные параметры.

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath, pdfOptions);
```

## Шаг 4. Экспорт в растровые изображения

Расширьте функциональность экспорта в растровые изображения, например PNG.

```csharp
// Размер А4 при разрешении 300 точек на дюйм — 2480 x 3508
rasterizationOptions.PageHeight = 3508;
rasterizationOptions.PageWidth = 2480;

PngOptions pngOptions = new PngOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath.Replace("pdf", "png"), pngOptions);
```

## Заключение

Поздравляем! Вы успешно научились использовать Aspose.CAD для .NET для экспорта файлов DWG как в PDF, так и в растровые изображения. Эта мощная библиотека упрощает процесс, делая его эффективным и удобным для разработчиков.

## Часто задаваемые вопросы

### Вопрос 1: Могу ли я использовать Aspose.CAD для .NET в своих коммерческих проектах?

 А1: Да, вы можете. Посещать[Purchase.aspose.com/buy](https://purchase.aspose.com/buy) для получения подробной информации о лицензировании.

### В2: Доступна ли бесплатная пробная версия?

 А2: Конечно! Получите бесплатную пробную версию[здесь](https://releases.aspose.com/).

### Вопрос 3: Как я могу получить поддержку Aspose.CAD для .NET?

 A3: Отправляйтесь в[Форум Aspose.CAD](https://forum.aspose.com/c/cad/19) для поддержки сообщества.

### Вопрос 4: Могу ли я получить временную лицензию для целей тестирования?

О4: Да, вы можете получить временную лицензию.[здесь](https://purchase.aspose.com/temporary-license/).

### В5: Где я могу найти подробную документацию?

 A5: Документация доступна по адресу[Aspose.CAD](https://reference.aspose.com/cad/net/).