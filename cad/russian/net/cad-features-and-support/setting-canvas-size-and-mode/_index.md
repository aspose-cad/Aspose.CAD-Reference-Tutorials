---
date: 2026-03-29
description: Узнайте, как создать PDF из CAD, установить размер холста и экспортировать
  CAD в PDF или TIFF с помощью Aspose.CAD для .NET в этом пошаговом руководстве.
linktitle: Setting Canvas Size and Mode
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 'Как создать PDF из CAD: установить размер холста и режим в Aspose.CAD для
  .NET'
url: /ru/net/cad-features-and-support/setting-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Настройка размера холста и режима в Aspose.CAD для .NET

## Введение

Готовы **создавать PDF из CAD** файлов, контролируя размеры вывода? В этом руководстве мы пройдем настройку размера холста и режима, загрузку CAD‑файла и экспорт его в PDF или TIFF с помощью Aspose.CAD для .NET. Независимо от того, нужно ли вам **конвертировать DXF в PDF**, создавать высоко‑разрешенные чертежи или просто настроить область растеризации, приведённые ниже шаги предоставят надёжное решение, готовое к использованию в продакшене.

## Быстрые ответы
- **Что означает “create PDF from CAD”?** Преобразование CAD‑чертежа (например, DXF, DWG) в PDF‑документ, сохраняющий векторные и растровые детали.  
- **Какая опция контролирует размер вывода?** `CadRasterizationOptions.PageWidth` и `PageHeight` (размер холста).  
- **Можно ли также экспортировать в TIFF?** Да — используйте `TiffOptions` с теми же настройками растеризации.  
- **Нужна ли лицензия для продакшена?** Требуется коммерческая лицензия; доступна бесплатная пробная версия.  
- **Поддерживаемые версии .NET?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## Что такое “create PDF from CAD”?
Создание PDF из CAD означает рендеринг CAD‑чертежа в формат, ориентированный на страницу (PDF), который можно просматривать, печатать или делиться им без необходимости в CAD‑программе. Aspose.CAD берёт на себя сложную часть, позволяя задавать размер холста, масштабирование и формат вывода.

## Зачем задавать размер холста при создании PDF из CAD?
Задание размера холста дает вам точный контроль над разрешением и размерами получаемого PDF или TIFF. Это особенно полезно, когда:
- Подготовка чертежей к печати на конкретных размерах бумаги.  
- Создание миниатюр или высоко‑разрешённых изображений для веб‑предпросмотра.  
- Обеспечение согласованного макета в нескольких документах.

## Предварительные требования

- Библиотека Aspose.CAD: Скачайте и установите библиотеку Aspose.CAD с [веб‑сайта Aspose.CAD](https://releases.aspose.com/cad/net/).
- Среда разработки: Убедитесь, что на вашем компьютере настроена .NET‑среда разработки.
- Пример CAD‑файла: Для этого руководства мы будем использовать пример DXF‑файла. Вы можете найти его в [документации Aspose.CAD](https://reference.aspose.com/cad/net/).

## Импорт пространств имён

First, import the namespaces required for CAD processing:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Как создать PDF из CAD с пользовательским размером холста

### Шаг 1: Загрузка CAD‑файла

We start by **loading the CAD file** (e.g., a DXF) into an `Image` object. This is the point where you **load CAD file** into memory.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    // Your code for further steps will go here
}
```

### Шаг 2: Создание CadRasterizationOptions

Create a `CadRasterizationOptions` instance and define the canvas size. The `PageWidth` and `PageHeight` properties let you **set canvas size** to the exact dimensions you need.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
rasterizationOptions.NoScaling = false;
```

### Шаг 3: Создание PdfOptions (Экспорт CAD в PDF)

Link the rasterization settings to a `PdfOptions` object. This configuration enables you to **export CAD to PDF** with the custom canvas you defined.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### Шаг 4: Экспорт в PDF (Конвертация DXF в PDF)

Now save the image as a PDF. This step **creates PDF from CAD** using the options we set.

```csharp
image.Save(MyDir + "result_out.pdf", pdfOptions);
```

### Шаг 5: Создание TiffOptions (Экспорт CAD в TIFF)

If you also need a raster image, configure `TiffOptions`. The same rasterization options are reused, so the **export CAD to TIFF** respects the canvas size.

```csharp
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.VectorRasterizationOptions = rasterizationOptions;
```

### Шаг 6: Экспорт в TIFF

Finally, save the drawing as a TIFF file.

```csharp
image.Save(MyDir + "result_out.tiff", tiffOptions);
```

## Распространённые проблемы и решения

- **Холст выглядит обрезанным** — Убедитесь, что `AutomaticLayoutsScaling` установлен в `true`, а `NoScaling` — в `false`, чтобы чертеж масштабировался под размер холста.  
- **PDF низкого разрешения** — Увеличьте `PageWidth`/`PageHeight` или задайте `Resolution` в `CadRasterizationOptions`.  
- **Ошибка файл не найден** — Убедитесь, что `MyDir` указывает на существующий каталог и имя DXF‑файла точно совпадает.

## Часто задаваемые вопросы

### Вопрос 1: Могу ли я использовать Aspose.CAD с другими .NET‑библиотеками?
A1: Да, Aspose.CAD бесшовно интегрируется с другими .NET‑библиотеками, предоставляя расширенные возможности для работы с CAD.

### Вопрос 2: Доступна ли бесплатная пробная версия Aspose.CAD?
A2: Да, вы можете ознакомиться с функциями Aspose.CAD, используя бесплатную пробную версию. Перейдите [сюда](https://releases.aspose.com/), чтобы начать.

### Вопрос 3: Как получить поддержку Aspose.CAD?
A3: Для получения поддержки и обсуждений посетите [форум Aspose.CAD](https://forum.aspose.com/c/cad/19).

### Вопрос 4: Где найти полную документацию по Aspose.CAD?
A4: Обратитесь к [документации Aspose.CAD](https://reference.aspose.com/cad/net/) для получения подробной информации и примеров.

### Вопрос 5: Как приобрести Aspose.CAD для .NET?
A5: Чтобы приобрести Aspose.CAD, перейдите на [страницу покупки](https://purchase.aspose.com/buy).

**Дополнительные вопросы и ответы**

**Вопрос: Могу ли я экспортировать многостраничный CAD‑чертеж в один PDF?**  
A: Да. Установите `PageCount` в `CadRasterizationOptions`, и библиотека объединит страницы в один PDF.

**Вопрос: Влияет ли размер холста на качество векторных данных?**  
A: Векторные данные остаются независимыми от разрешения; размер холста влияет только на растеризованные элементы и разрешение изображения.

---

**Последнее обновление:** 2026-03-29  
**Тестировано с:** Aspose.CAD 24.11 for .NET  
**Автор:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}