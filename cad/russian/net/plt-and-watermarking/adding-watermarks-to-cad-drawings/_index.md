---
title: Добавление водяных знаков в чертежи САПР — Руководство Aspose.CAD
linktitle: Добавление водяных знаков в чертежи САПР
second_title: Aspose.CAD .NET — формат файлов CAD и BIM
description: Улучшите свои чертежи САПР с помощью профессиональных водяных знаков с помощью Aspose.CAD для .NET. Следуйте нашему пошаговому руководству для создания персонализированного и привлекательного дизайна.
weight: 11
url: /ru/net/plt-and-watermarking/adding-watermarks-to-cad-drawings/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Добавление водяных знаков в чертежи САПР — Руководство Aspose.CAD

## Введение

Хотите улучшить свои чертежи САПР, добавив профессиональные водяные знаки? Aspose.CAD for .NET предоставляет надежное решение для простой интеграции водяных знаков в ваши файлы САПР. В этом пошаговом руководстве мы покажем вам процесс добавления водяных знаков с помощью Aspose.CAD, гарантируя, что ваши рисунки не только передают важную информацию, но и несут ваш уникальный знак.

## Предварительные условия

Прежде чем приступить к изучению руководства, убедитесь, что у вас есть следующее:
-  Aspose.CAD для .NET: убедитесь, что у вас установлена библиотека Aspose.CAD. Вы можете скачать его[здесь](https://releases.aspose.com/cad/net/).
- Каталог ваших документов: создайте каталог для хранения чертежей САПР.
Теперь давайте начнем с добавления водяных знаков на ваши чертежи САПР!

## Импортировать пространства имен

Начните с импорта необходимых пространств имен в ваш проект .NET:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Шаг 1. Загрузите чертеж САПР

```csharp
// Путь к каталогу документов.
string MyDir = "Your Document Directory";
using (CadImage cadImage = (CadImage)Image.Load(MyDir + "Drawing11.dwg")) {
```

## Шаг 2. Добавьте водяной знак в формате МТЕКСТ.

```csharp
// Добавить новый МТЕКСТ
CadMText watermark = new CadMText();
watermark.Text = "Watermark message";
watermark.InitialTextHeight = 40;
watermark.InsertionPoint = new Cad3DPoint(300, 40);
watermark.LayerName = "0";
cadImage.BlockEntities["*Model_Space"].AddEntity(watermark);
```

## Шаг 3: Или добавьте водяной знак в виде текста

```csharp
// Альтернативно добавьте более простой объект, например Текст.
CadText text = new CadText();
text.DefaultValue = "Watermark text";
text.TextHeight = 40;
text.FirstAlignment = new Cad3DPoint(300, 40);
text.LayerName = "0";
cadImage.BlockEntities["*Model_Space"].AddEntity(text);
```

## Шаг 4. Экспорт в PDF

```csharp
// Экспортируйте чертеж САПР с водяным знаком в PDF.
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.Layouts = new[] { "Model" };
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
cadImage.Save(MyDir + "AddWatermark_out.pdf", pdfOptions);
```

Повторите эти шаги для разных чертежей, и вы мгновенно получите профессионально выглядящие файлы САПР с водяными знаками!

## Заключение

Поздравляем! Вы успешно научились добавлять водяные знаки на чертежи САПР с помощью Aspose.CAD для .NET. Этот простой, но мощный процесс позволяет персонализировать проекты, сохраняя при этом целостность технических чертежей.

## Часто задаваемые вопросы

### В1: Могу ли я настроить внешний вид водяного знака?

О1: Да, вы можете настроить текст, шрифт, размер и положение водяного знака в соответствии со своими предпочтениями.

### Вопрос 2: Совместим ли Aspose.CAD с различными форматами файлов САПР?

A2: Aspose.CAD поддерживает различные форматы файлов САПР, включая DWG и DXF, обеспечивая широкую совместимость.

### Вопрос 3. Могу ли я добавить несколько водяных знаков в один чертеж САПР?

А3: Абсолютно! Вы можете добавить столько водяных знаков, сколько необходимо, обеспечивая гибкость для различных вариантов использования.

### Вопрос 4: Предлагает ли Aspose.CAD бесплатную пробную версию?

О4: Да, вы можете изучить возможности Aspose.CAD с помощью бесплатной пробной версии. Возьми[здесь](https://releases.aspose.com/).

### Вопрос 5: Где я могу найти поддержку Aspose.CAD?

 A5: По любым вопросам или помощи посетите[Форум Aspose.CAD](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
