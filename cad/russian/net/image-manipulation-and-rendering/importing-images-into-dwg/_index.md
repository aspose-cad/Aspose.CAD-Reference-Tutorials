---
date: 2026-08-17
description: Узнайте, как добавить изображение в файлы dwg с использованием C# и Aspose.CAD
  для .NET. Это руководство проведет вас через импорт изображений, установку точек
  вставки и экспорт в PDF.
keywords:
- add image to dwg
- convert dwg to pdf
- set insertion point dwg
- embed png in dwg
- save dwg as pdf
lastmod: 2026-08-17
linktitle: Импорт изображений в файлы DWG с помощью C#
og_description: Узнайте, как добавить изображение в файлы dwg с помощью C#. Этот учебник
  охватывает импорт изображений, установку точек вставки и конвертацию dwg в pdf с
  помощью Aspose.CAD.
og_image_alt: Guide showing C# code to embed an image into a DWG file using Aspose.CAD
og_title: Как добавить изображение в файлы dwg с помощью C# и Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-08-17'
  description: Learn how to add image to dwg files using C# and Aspose.CAD for .NET.
    This guide walks you through importing images, setting insertion points, and exporting
    to PDF.
  headline: How to add image to dwg files with C# using Aspose.CAD
  type: TechArticle
- description: Learn how to add image to dwg files using C# and Aspose.CAD for .NET.
    This guide walks you through importing images, setting insertion points, and exporting
    to PDF.
  name: How to add image to dwg files with C# using Aspose.CAD
  steps:
  - name: set up your document directory
    text: Prepare the folder that contains the source DWG and the image you want to
      embed.
  - name: load the dwg file
    text: The `CadImage` class represents a DWG drawing and provides access to its
      entities, layers, and metadata.
  - name: define the image properties
    text: Create an `Image` object that points to the raster file (e.g., PNG) and
      specify its format.
  - name: set insertion point dwg and vectors
    text: Specify where the image should appear inside the drawing and how it should
      be scaled. The insertion point is defined by a 2‑D coordinate, while the vectors
      control width and height.
  - name: create and configure the raster image
    text: Instantiate a `RasterImage` object, assign the image data, and set any additional
      rendering options.
  - name: add image to dwg file
    text: Insert the configured raster image into the DWG’s entities collection so
      it becomes part of the drawing.
  - name: save as pdf (export dwg to pdf)
    text: After embedding the image you can **convert dwg to pdf** or **save dwg as
      pdf** with a single call. This is useful for sharing the drawing with stakeholders
      who don’t have CAD software.
  type: HowTo
- questions:
  - answer: The core library is .NET‑specific, but Aspose offers equivalent APIs for
      Java, Python and other platforms.
    question: Can I use Aspose.CAD for .NET with other programming languages?
  - answer: Yes, you can explore a free trial on the [Aspose free trial page](https://releases.aspose.com/).
    question: Is a free trial available for Aspose.CAD?
  - answer: The documentation is available in the [Aspose.CAD .NET API reference](https://reference.aspose.com/cad/net/).
    question: Where can I find detailed documentation for Aspose.CAD?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to get a temporary license.
    question: How do I obtain a temporary license for Aspose.CAD?
  - answer: Yes, you can seek support and engage with the community in the [Aspose.CAD
      community forum](https://forum.aspose.com/c/cad/19).
    question: Are there community forums for Aspose.CAD support?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- CAD
- Aspose.CAD
- C# image processing
- DWG manipulation
title: Как добавить изображение в файлы dwg с помощью C# и Aspose.CAD
url: /ru/net/image-manipulation-and-rendering/importing-images-into-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Как добавить изображение в файлы dwg с помощью C# и Aspose.CAD

## Введение

Добавление изображения в файл DWG является обычной задачей, когда необходимо обогатить чертежи CAD логотипами, фотографиями или растровой графикой. В этом учебнике вы узнаете, как **add image to dwg** программно с использованием C# и Aspose.CAD для .NET, а затем при желании преобразовать результат в PDF. Шаги разбиты, чтобы вы могли копировать‑вставлять каждый раздел в свой проект.

## Быстрые ответы
- **Какая библиотека выполняет задачу?** Aspose.CAD for .NET.
- **Можно ли встраивать PNG‑файлы?** Да – поддерживаются PNG, JPEG, BMP и другие растровые форматы.
- **Нужна ли лицензия для разработки?** Бесплатная пробная версия подходит для тестирования; для продакшна требуется коммерческая лицензия.
- **Поддерживается ли экспорт в PDF?** Абсолютно – вы можете конвертировать обновлённый DWG в PDF одной строкой.
- **Какие версии .NET совместимы?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7.

## Что такое файл DWG?

Файл DWG — это собственный бинарный формат Autodesk AutoCAD для хранения векторной геометрии, слоёв и метаданных чертежа. Он широко используется в архитектуре, инженерии и строительстве, а Aspose.CAD может читать и записывать этот формат без необходимости установки AutoCAD.

## Почему добавлять изображение в dwg с помощью Aspose.CAD?

Aspose.CAD поддерживает **50+ input and output formats**, может обрабатывать файлы размером более 500 МБ без загрузки всего документа в память и предоставляет детерминированный API, работающий в безголовых серверных средах. Это делает пакетную обработку DWG‑чертежей быстрой и надёжной.

## Предварительные требования
- Базовые знания программирования на C#.
- Aspose.CAD for .NET установлен. Вы можете скачать его со [страницы загрузки Aspose.CAD for .NET](https://releases.aspose.com/cad/net/). Также можно ознакомиться с другими продуктами Aspose на [странице релизов Aspose](https://releases.aspose.com/).
- Среда разработки, например Visual Studio 2022 или новее.

## Как добавить изображение в dwg с помощью Aspose.CAD?

Загрузите целевой DWG, создайте объект растрового изображения, описывающий картинку, которую хотите встроить, задайте точку вставки и векторы масштабирования, затем прикрепите изображение к чертежу. В конце сохраните изменённый DWG или экспортируйте его напрямую в PDF. Весь процесс требует лишь нескольких вызовов API и выполняется менее чем за секунду для типичных двухстраничных чертежей.

### Импорт пространств имён
Include the namespaces that expose the CAD classes you’ll need.

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

### Шаг 1: настройте каталог вашего документа
Prepare the folder that contains the source DWG and the image you want to embed.

```csharp
string MyDir = "Your Document Directory";
```

### Шаг 2: загрузите файл dwg
The `CadImage` class represents a DWG drawing and provides access to its entities, layers, and metadata.

```csharp
string dwgPathToFile = MyDir + "Drawing11.dwg";
CadImage cadImage1 = (CadImage)Image.Load(dwgPathToFile);
```

### Шаг 3: определите свойства изображения
Create an `Image` object that points to the raster file (e.g., PNG) and specify its format.

```csharp
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.ObjectHandle = "A3B4";
```

### Шаг 4: задайте точку вставки dwg и векторы
Specify where the image should appear inside the drawing and how it should be scaled. The insertion point is defined by a 2‑D coordinate, while the vectors control width and height.

```csharp
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

### Шаг 5: создайте и настройте растровое изображение
Instantiate a `RasterImage` object, assign the image data, and set any additional rendering options.

```csharp
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.ImageDefReference = "A3B4";
cadRasterImage.DisplayFlags = 7;
cadRasterImage.ClippingState = 0;
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(639.5, 561.5));
```

### Шаг 6: добавьте изображение в файл dwg
Insert the configured raster image into the DWG’s entities collection so it becomes part of the drawing.

```csharp
CadImage cadImage = (CadImage)cadImage1;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadRasterImage);

List<CadBaseObject> list = new List<CadBaseObject>(cadImage.Objects);
list.Add(cadRasterImageDef);
cadImage.Objects = list.ToArray();
```

### Шаг 7: сохранить как pdf (экспорт dwg в pdf)
After embedding the image you can **convert dwg to pdf** or **save dwg as pdf** with a single call. This is useful for sharing the drawing with stakeholders who don’t have CAD software.

```csharp
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;

cadRasterizationOptions.PageHeight = 1600;
cadRasterizationOptions.PageWidth = 1600;
cadRasterizationOptions.Layouts = new string[] { "Model" };
cadImage1.Save(MyDir + "export2.pdf", pdfOptions);
```

## Как конвертировать dwg в pdf после вставки изображения?

Call the `Save` method on the `CadImage` instance, passing `SaveFormat.Pdf` and optionally a `PdfOptions` object to control page size, rasterization, and metadata. Aspose.CAD preserves the embedded raster image, layers, and line weights, producing a faithful PDF representation that can be opened in any viewer. This conversion is performed in a single line of code.

## Распространённые проблемы и решения
- **Image appears at the wrong location** – double‑check the insertion point coordinates and the direction vectors; they are relative to the drawing’s origin.
- **Large images cause memory spikes** – use the `Resize` option on the raster image before insertion, or work with a lower‑resolution copy.
- **PDF export loses vector quality** – ensure you are saving with `PdfOptions` that retain vector data; raster images are always embedded as they are.

## Часто задаваемые вопросы

**Q: Can I use Aspose.CAD for .NET with other programming languages?**  
A: The core library is .NET‑specific, but Aspose offers equivalent APIs for Java, Python and other platforms.

**Q: Is a free trial available for Aspose.CAD?**  
A: Yes, you can explore a free trial on the [Aspose free trial page](https://releases.aspose.com/).

**Q: Where can I find detailed documentation for Aspose.CAD?**  
A: The documentation is available in the [Aspose.CAD .NET API reference](https://reference.aspose.com/cad/net/).

**Q: How do I obtain a temporary license for Aspose.CAD?**  
A: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/) to get a temporary license.

**Q: Are there community forums for Aspose.CAD support?**  
A: Yes, you can seek support and engage with the community in the [Aspose.CAD community forum](https://forum.aspose.com/c/cad/19).

---

**Last Updated:** 2026-08-17  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose

## Связанные руководства

- [Exporting DWG to PDF or Raster Images - Aspose.CAD Guide](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [Exporting DWG to DXF Format in C# - Aspose.CAD Tutorial](/cad/net/advanced-export-techniques/exporting-dwg-to-dxf/)
- [Exporting Specific Layouts to PDF - Aspose.CAD Guide](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}