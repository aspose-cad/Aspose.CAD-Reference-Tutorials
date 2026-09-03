---
date: 2026-08-23
description: Узнайте, как создать viewport dwg c# с помощью Aspose.CAD. Это руководство
  охватывает загрузку DWG‑файла, настройку rasterization, определение viewport и сохранение
  результата в PDF.
keywords:
- create viewport dwg c#
- render dwg c#
- aspose.cad .net
lastmod: 2026-08-23
linktitle: Рендеринг DWG документов в C#
og_description: Узнайте, как создать viewport dwg c# с помощью Aspose.CAD в .NET.
  Это пошаговое руководство показывает loading, rasterizing, определение viewports
  и сохранение в PDF.
og_image_alt: Guide showing how to create viewport dwg c# with Aspose.CAD in .NET
og_title: Как создать viewport dwg c# с Aspose.CAD для .NET
schemas:
- author: Aspose
  dateModified: '2026-08-23'
  description: Learn how to create viewport dwg c# using Aspose.CAD. This guide covers
    loading a DWG file, configuring rasterization, defining a viewport, and saving
    the result as PDF.
  headline: How to create viewport dwg c# with Aspose.CAD for .NET
  type: TechArticle
- questions:
  - answer: Load the DWG file with `CadImage.Load`.
    question: What is the first step?
  - answer: '`Viewport` inside `CadRasterizationOptions`.'
    question: Which class defines the view area?
  - answer: Yes, using `PdfOptions` after rasterization.
    question: Can I output to PDF?
  - answer: A commercial license is required; a free trial works for evaluation.
    question: Do I need a license for production?
  - answer: Absolutely – Aspose.CAD works with .NET Framework, .NET Core, and .NET 5/6.
    question: Is .NET Core supported?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- create viewport dwg c#
- Aspose.CAD
- C# CAD rendering
- DWG to PDF
- CAD viewports
title: Как создать viewport dwg c# с Aspose.CAD для .NET
url: /ru/net/image-manipulation-and-rendering/rendering-dwg-documents/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Отображение DWG‑документов в C# – создание viewport dwg c# tutorial

## Введение

В этом всестороннем учебнике вы узнаете, как **create viewport dwg c#** с помощью Aspose.CAD и отрендерить файл DWG в PDF. Независимо от того, нужно ли вам извлечь конкретный макет, создать печатный лист или встроить CAD‑вид в отчёт, управление viewport даёт точный контроль над рендерингом. Aspose.CAD поддерживает **более 20 форматов CAD** и может обрабатывать файлы с тысячами сущностей без загрузки всего документа в память, что делает её идеальной для высокопроизводительных .NET‑приложений.

## Быстрые ответы
- **Какой первый шаг?** Загрузить DWG‑файл с помощью `CadImage.Load`.
- **Какой класс определяет область просмотра?** `Viewport` внутри `CadRasterizationOptions`.
- **Можно ли вывести в PDF?** Да, используя `PdfOptions` после растеризации.
- **Нужна ли лицензия для продакшна?** Требуется коммерческая лицензия; бесплатная trial‑версия подходит для оценки.
- **Поддерживается ли .NET Core?** Абсолютно – Aspose.CAD работает с .NET Framework, .NET Core и .NET 5/6.

## Требования

Прежде чем погрузиться в код, убедитесь, что у вас есть:

- Базовые знания программирования на C#.
- Установленная Visual Studio (любая современная версия).
- Библиотека Aspose.CAD, добавленная в ваш проект. Скачать её можно со [страницы загрузки Aspose.CAD](https://releases.aspose.com/cad/net/).
- Пример DWG‑файла, например **Bottom_plate.dwg**, чтобы следовать инструкциям.

## Импорт пространств имён

Добавьте необходимые директивы `using` в начало вашего C#‑файла, чтобы компилятор мог найти типы Aspose.CAD.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.FileFormats.Cad;
```

Теперь, когда окружение готово, давайте пошагово разберём реализацию.

## Как создать viewport dwg c#?

Чтобы создать пользовательский viewport, сначала загрузите DWG‑файл в объект `CadImage`, затем настройте `CadRasterizationOptions` с нужным макетом и масштабом. Определите регион, который хотите отобразить, создайте `CadVportTableObject` с вычисленными центром, высотой и соотношением сторон, замените активный viewport, задайте параметры PDF и, наконец, сохраните результат.

## Шаг 1: загрузить dwg файл

`CadImage.Load` загружает DWG‑файл в объект `CadImage`, представляющий чертёж CAD в памяти.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for loading the DWG file goes here.
}
```

## Шаг 2: настроить параметры растеризации

`CadRasterizationOptions` определяет, как CAD‑чертёж будет растеризован, включая выбор макета, масштаб и размер вывода.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };
rasterizationOptions.NoScaling = true;
// Additional rasterization configurations can be added here.
```

## Шаг 3: определить регион для отрисовки

`Point` задаёт координаты X и Y левого верхнего угла региона, который будет отрисован.

```csharp
Point topLeft = new Point(6156, 7053);
double width = 3108;
double height = 2489;
```

## Шаг 4: создать новый viewport

`CadVportTableObject` представляет объект viewport, контролирующий видимую область и соотношение сторон отрисованного чертежа.

```csharp
CadVportTableObject newView = new CadVportTableObject();
newView.Name.Value = "*Active";
newView.CenterPoint.X = topLeft.X + width / 2f;
newView.CenterPoint.Y = topLeft.Y - height / 2f;
newView.ViewHeight.Value = height;
newView.ViewAspectRatio.Value = width / height;
```

## Шаг 5: заменить активный viewport

Цикл заменяет активный viewport на только что созданный, применяя пользовательские настройки просмотра.

```csharp
for (int i = 0; i < cadImage.ViewPorts.Count; i++)
{
    CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
    if ((currentView.Name.Value == null && cadImage.ViewPorts.Count == 1) ||
    string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
    {
        cadImage.ViewPorts[i] = newView;
        break;
    }
}
```

## Шаг 6: настроить параметры PDF

`PdfOptions` конфигурирует параметры вывода PDF, такие как сжатие и метаданные.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Шаг 7: сохранить отрендеренный dwg как PDF

`image.Save` записывает отрендеренное изображение в файл, используя указанные параметры формата.

```csharp
cadImage.Save(MyDir, pdfOptions);
```

## Зачем использовать пользовательский viewport при рендеринге DWG?

Пользовательский viewport позволяет изолировать конкретный макет или регион, уменьшая размер файла и ускоряя рендеринг. Aspose.CAD может отрендерить 300‑страничный DWG менее чем за 2 секунды при использовании сфокусированного viewport, в то время как полное рендеринг может занять несколько секунд дольше.

## Распространённые проблемы и решения

- **Пустой вывод** – Убедитесь, что координаты viewport находятся внутри границ чертежа; используйте `CadImage.Size` для проверки границ.
- **Отсутствие слоёв** – Установите `CadRasterizationOptions.Layouts` в правильное имя макета; иначе макет по умолчанию может быть пустым.
- **Замедление производительности** – Отключите сглаживание в `CadRasterizationOptions`, если нужен только быстрый предварительный просмотр.

## Часто задаваемые вопросы

### Q1: Можно ли использовать Aspose.CAD с другими форматами CAD‑файлов?

A1: Да, Aspose.CAD поддерживает различные форматы, включая DWG, DXF, DWF и более 20 дополнительных типов CAD.

### Q2: Совместима ли Aspose.CAD с .NET Core?

A2: Да, Aspose.CAD работает с .NET Framework, .NET Core и последними версиями .NET.

### Q3: Как обрабатывать разные макеты в DWG‑файле?

A3: Укажите нужный макет через свойство `Layouts` у `CadRasterizationOptions` перед рендерингом.

### Q4: Есть ли особенности лицензирования при использовании Aspose.CAD?

A4: Подробности о лицензировании см. на [странице лицензирования Aspose.CAD](https://purchase.aspose.com/buy).

### Q5: Где можно получить дополнительную поддержку?

A5: Посетите [форум Aspose.CAD](https://forum.aspose.com/c/cad/19) для помощи сообщества и обсуждений.

### Q6: Можно ли рендерить напрямую в PNG вместо PDF?

A6: Да, замените `PdfOptions` на `PngOptions` и вызовите `image.Save("output.png", pngOptions)`.

### Q7: Как встроить отрендеренное изображение в приложение Windows Forms?

A7: Загрузите сохранённое изображение в элемент управления `PictureBox`, используя `Image.FromFile("output.png")`.

## Заключение

Теперь вы знаете, как **create viewport dwg c#** и отрендерить DWG‑файл в PDF (или другие растровые форматы) с помощью Aspose.CAD. Освоив манипуляцию viewport, вы получаете тонкий контроль над визуальным выводом, что необходимо для создания точных инженерных чертежей, отчётов или миниатюр. Исследуйте дополнительные параметры растеризации, экспериментируйте с различными форматами вывода и интегрируйте код в более крупные .NET‑службы или настольные утилиты.

---

**Last Updated:** 2026-08-23  
**Tested with:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose

## Связанные учебники

- [How to Set Viewport while Converting DWG to PDF with Coordinates in C# - Aspose.CAD Tutorial](/cad/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/)
- [Learn to Set CAD Rasterization Options – Export Specific Layouts to PDF with Aspose.CAD](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)
- [How to convert DWG to PDF and Raster Images using Aspose.CAD for .NET](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}