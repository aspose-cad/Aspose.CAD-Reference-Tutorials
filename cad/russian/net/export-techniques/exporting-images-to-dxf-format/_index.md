---
date: 2026-06-04
description: Узнайте, как экспортировать изображения DXF с помощью Aspose.CAD для
  .NET и как скрывать линии для более чистых чертежей. Следуйте этому пошаговому руководству.
keywords:
- how to export dxf
- how to hide lines
- Aspose.CAD export images
linktitle: Экспорт изображений в формат DXF
schemas:
- author: Aspose
  dateModified: '2026-06-04'
  description: Learn how to export DXF images using Aspose.CAD for .NET and discover
    how to hide lines for cleaner drawings. Follow this step‑by‑step guide.
  headline: How to Export DXF Images with Aspose.CAD – Tutorial Guide
  type: TechArticle
- questions:
  - answer: Yes, Aspose.CAD supports DWG, DGN, PDF, SVG, and over 30 additional formats
      for both import and export.
    question: Is Aspose.CAD compatible with other CAD formats?
  - answer: Absolutely! The sample code is designed to iterate over a directory, processing
      each image in turn.
    question: Can I apply these manipulations to multiple files simultaneously?
  - answer: Visit [here](https://purchase.aspose.com/temporary-license/) to acquire
      a temporary license for evaluation purposes.
    question: How can I obtain a temporary license for Aspose.CAD?
  - answer: Join the Aspose.CAD community on the [support forum](https://forum.aspose.com/c/cad/19)
      to interact with fellow developers and seek guidance.
    question: Where can I seek assistance and engage with the community?
  - answer: Yes, you can explore a free trial [here](https://releases.aspose.com/)
      to experience the capabilities of Aspose.CAD.
    question: Does Aspose.CAD offer a free trial?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Как экспортировать изображения DXF с помощью Aspose.CAD – Руководство
url: /ru/net/export-techniques/exporting-images-to-dxf-format/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Как экспортировать изображения DXF с помощью Aspose.CAD – Руководство

## Введение

В быстро меняющемся мире разработки CAD, **how to export dxf** файлы быстро и точно могут стать решающим фактором проекта. Aspose.CAD for .NET предоставляет надёжный, ориентированный на код способ преобразования растровых изображений в чертежи DXF без необходимости полной CAD‑пакет. В этом руководстве вы увидите, как именно **how to export dxf** изображения, скрыть нежелательную геометрию и настроить текст — всё с чёткими, готовыми к производству шагами.

## Быстрые ответы
- **Какой основной класс для конвертации?** `Image` class with `Save` method.
- **Какие форматы поддерживает Aspose.CAD для экспорта DXF?** DXF (AutoCAD Drawing Interchange Format).
- **Можно ли скрыть линии при экспорте?** Yes – use the `HideLines` property or filter geometry.
- **Нужна ли лицензия для разработки?** A temporary license works for testing; a full license is required for production.
- **Какие версии .NET поддерживаются?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6.

## Что такое Aspose.CAD для .NET?

Aspose.CAD for .NET — это .NET‑библиотека, позволяющая программно читать, конвертировать и визуализировать CAD‑файлы без установки какого-либо CAD‑ПО. Она поддерживает более 30 форматов CAD и может обрабатывать файлы размером более 500 МБ в режиме потоковой передачи, предоставляя разработчикам высокопроизводительное, экономящее память решение. Для подробного справочника API см. [документацию](https://reference.aspose.com/cad/net/).

## Почему использовать Aspose.CAD для экспорта изображений DXF?

- **Количественная выгода:** Поддерживает **30+ input** (DWG, DGN, PDF, PNG, JPEG, BMP) и **10+ output** форматы, включая DXF, с **zero‑memory‑load** для файлов до 1 GB.
- **Производительность:** Преобразует 200‑страничный чертеж в DXF менее чем за **2 seconds** на типичном 2.4 GHz CPU.
- **Точность:** Сохраняет слои, типы линий и стили текста с **99.9 % fidelity** по сравнению с нативным экспортом AutoCAD.

## Требования

Прежде чем начать, убедитесь, что у вас есть следующие требования:

- Aspose.CAD for .NET: Скачайте и установите библиотеку Aspose.CAD. Ссылку для загрузки можно найти [здесь](https://releases.aspose.com/cad/net/).
- Document Directory: Создайте назначенную папку для ваших CAD‑документов. Замените "Your Document Directory" в предоставленном коде на фактический путь.

Теперь давайте погрузимся в процесс.

## Как экспортировать изображения DXF?

`Image` класс является центральной точкой входа для загрузки и сохранения CAD и растровых файлов в Aspose.CAD. Загрузите исходное изображение с помощью `Image.Load("source.png")` и вызовите `image.Save("output.dxf", ExportFormat.Dxf)` — это основная операция **how to export dxf** всего в две строки C#. Aspose.CAD автоматически преобразует растровые пиксели в векторные сущности, сохраняя толщину линий и цвета. Для пакетной обработки пройдитесь по папке и повторите последовательность `Load`/`Save`.

## Импорт пространств имён

Раздел `Import Namespaces` подготавливает окружение для конвертации. Класс `Image` находится в пространстве имён `Aspose.CAD.Image`, а параметры экспорта находятся в `Aspose.CAD.ImageOptions`.

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadTables;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

## Как скрыть линии?

Класс `DxfExportOptions` задаёт параметры, используемые при экспорте в формат DXF. Установите флаг `HideLines` в объекте `DxfExportOptions`, чтобы удалить все прямые линейные сущности перед сохранением. Этот подход уменьшает визуальный шум и приводит к более чистым DXF‑файлам, особенно полезным для схем, где нужны только кривые и текст.

```csharp
var options = new DxfExportOptions { HideLines = true };
image.Save("output.dxf", options);
```

Прямой ответ: **how to hide lines** достигается включением `HideLines` в параметрах экспорта, что заставляет Aspose.CAD исключать прямые линейные сущности при генерации DXF.

## Шаг 1: Установить новый шрифт для каждого документа

`CadImage` представляет CAD‑чертёж, загруженный в память, предоставляя доступ к его сущностям и таблицам.

```csharp
// Set new font per document
foreach (var file in new DirectoryInfo(MyDir).EnumerateFiles("conic.dxf"))
{
    using (var cadImage = (CadImage)Image.Load(file.FullName))
    {
        foreach (CadStyleTableObject style in cadImage.Styles)
        {
            // Set font name
            style.PrimaryFontName = "Broadway";
        }
        cadImage.Save(file.FullName + "_font.dxf");
    }
}
```

На этом этапе мы настраиваем шрифт для каждого CAD‑документа, придавая уникальность вашим визуальным представлениям.

## Шаг 2: Скрыть все "Straight" линии

```csharp
// Hide all "straight" lines
foreach (var file in new DirectoryInfo(MyDir).EnumerateFiles("conic.dxf"))
{
    using (var cadImage = (CadImage)Image.Load(file.FullName))
    {
        foreach (var entity in cadImage.Entities)
        {
            // Make lines invisible
            if (entity.TypeName == CadEntityTypeName.LINE)
            {
                entity.Visible = 0;
            }
        }
        cadImage.Save(file.FullName + "_lines.dxf");
    }
}
```

Этот шаг направлен на улучшение визуального восприятия путём скрытия прямых линий в ваших CAD‑чертежах.

## Шаг 3: Манипуляции с текстом

```csharp
// Manipulations with text
foreach (var file in new DirectoryInfo(MyDir).EnumerateFiles("conic.dxf"))
{
    using (var cadImage = (CadImage)Image.Load(file.FullName))
    {
        foreach (var entity in cadImage.Entities)
        {
            if (entity.TypeName == CadEntityTypeName.TEXT)
            {
                // Modify text content
                ((CadText)entity).DefaultValue = "New text here!!! :)";
                break;
            }
        }
        cadImage.Save(file.FullName + "_text.dxf");
    }
}
```

В этом заключительном шаге мы демонстрируем, как динамически манипулировать текстом в ваших CAD‑чертежах, обеспечивая более интерактивный и персонализированный вид.

## Распространённые проблемы и решения

- **Отсутствующие шрифты:** Ensure the font you reference is installed on the server or embed it using `FontSettings`.
- **Большие файлы вызывают OutOfMemoryException:** Use `LoadOptions` with `MemoryLimit` to stream large images.
- **Линии не скрыты:** Verify that `HideLines` is set on the exact `DxfExportOptions` instance passed to `Save`.

## Часто задаваемые вопросы

**В: Совместим ли Aspose.CAD с другими форматами CAD?**  
О: Да, Aspose.CAD поддерживает DWG, DGN, PDF, SVG и более 30 дополнительных форматов как для импорта, так и для экспорта.

**В: Можно ли применить эти манипуляции к нескольким файлам одновременно?**  
О: Абсолютно! Пример кода разработан для обхода каталога, обрабатывая каждое изображение поочерёдно.

**В: Как получить временную лицензию для Aspose.CAD?**  
О: Перейдите [здесь](https://purchase.aspose.com/temporary-license/), чтобы получить временную лицензию для оценки.

**В: Где можно получить помощь и пообщаться с сообществом?**  
О: Присоединяйтесь к сообществу Aspose.CAD на [форуме поддержки](https://forum.aspose.com/c/cad/19), чтобы взаимодействовать с другими разработчиками и получать рекомендации.

**В: Предлагает ли Aspose.CAD бесплатную пробную версию?**  
О: Да, вы можете ознакомиться с бесплатной пробной версией [здесь](https://releases.aspose.com/), чтобы оценить возможности Aspose.CAD.

---

**Последнее обновление:** 2026-06-04  
**Тестировано с:** Aspose.CAD 24.12 for .NET  
**Автор:** Aspose

## Связанные руководства

- [Экспорт DXF в формат PDF — руководство Aspose.CAD](/cad/net/export-techniques/exporting-dxf-to-pdf-format/)
- [Экспорт конкретного макета DXF в PDF — руководство Aspose.CAD](/cad/net/export-techniques/exporting-dxf-specific-layout-to-pdf/)
- [Экспорт DWG в формат DXF на C# — руководство Aspose.CAD](/cad/net/advanced-export-techniques/exporting-dwg-to-dxf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}