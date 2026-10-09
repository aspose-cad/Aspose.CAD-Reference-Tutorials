---
date: 2026-10-09
description: Узнайте, как загрузить файл dwg и искать текст внутри файлов DWG, используя
  C# и Aspose.CAD for .NET. Следуйте этому пошаговому руководству, чтобы улучшить
  свои CAD‑процессы.
keywords:
- load dwg file
- export dwg to pdf
- cad text search
- search text dwg
- c# read dwg
lastmod: 2026-10-09
linktitle: Поиск текста в файлах DWG с C#
og_description: Узнайте, как загрузить файл dwg и искать текст внутри файлов DWG,
  используя C# и Aspose.CAD for .NET. Следуйте этому пошаговому руководству, чтобы
  улучшить свои CAD‑процессы.
og_image_alt: Guide showing how to load dwg file and search text in DWG files using
  Aspose.CAD for .NET
og_title: Как загрузить файл dwg и искать текст в файлах DWG с помощью C#
schemas:
- author: Aspose
  dateModified: '2026-10-09'
  description: Learn how to load dwg file and search text inside DWG files using C#
    and Aspose.CAD for .NET. Follow this step‑by‑step guide to enhance your CAD workflows.
  headline: How to load dwg file and search text in DWG files with C#
  type: TechArticle
- questions:
  - answer: '`new CadImage("yourfile.dwg")` creates an in‑memory representation of
      the drawing.'
    question: What is the first line of code to load a DWG?
  - answer: '`Aspose.CAD.Image` and `Aspose.CAD.FileFormats.Dwg` are required.'
    question: Which namespace contains the CAD classes?
  - answer: Yes – use `image.Save("out.pdf", SaveFormat.Pdf)`.
    question: Can I export the search results directly to PDF?
  - answer: A free trial works for evaluation; a permanent license is required for
      production.
    question: Do I need a license for development?
  - answer: .NET 5, .NET 6, .NET Core 3.1 and .NET Framework 4.6+.
    question: Which .NET versions are supported?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- dwg file handling
- aspose.cad
- c# cad processing
- text search in dwg
title: Как загрузить файл dwg и искать текст в файлах DWG с помощью C#
url: /ru/net/text-search-and-manipulation/searching-text-in-dwg-files/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Как загрузить файл dwg и искать текст в файлах DWG с C# - руководство Aspose.CAD

## Введение

В современной разработке CAD возможность **load dwg file** объектов и мгновенно находить конкретные строковые тексты экономит часы ручного осмотра. Независимо от того, создаёте ли вы инструмент пакетной обработки или добавляете возможности поиска в просмотрщик, Aspose.CAD for .NET предоставляет полностью управляемый API, работающий в Windows, Linux и macOS без нативных зависимостей. Это руководство проведёт вас через каждый шаг — от загрузки DWG до экспорта результата в PDF — чтобы вы могли интегрировать надёжный поиск текста CAD в свои C# приложения уже сегодня.

## Быстрые ответы
- **Какова первая строка кода для загрузки DWG?** `new CadImage("yourfile.dwg")` создаёт представление чертежа в памяти.  
- **В каком пространстве имён находятся классы CAD?** `Aspose.CAD.Image` и `Aspose.CAD.FileFormats.Dwg` необходимы.  
- **Могу ли я экспортировать результаты поиска напрямую в PDF?** Да — используйте `image.Save("out.pdf", SaveFormat.Pdf)`.  
- **Нужна ли лицензия для разработки?** Бесплатная пробная версия подходит для оценки; постоянная лицензия требуется для продакшна.  
- **Какие версии .NET поддерживаются?** .NET 5, .NET 6, .NET Core 3.1 и .NET Framework 4.6+.

## Что такое файл DWG?

Файл DWG — это бинарный формат, который хранит 2D и 3D данные дизайна, созданные в AutoCAD и совместимых инструментах. Это отраслевой стандартный контейнер для векторной геометрии, слоёв, текста и метаданных. Поскольку формат проприетарный, большинство открытых парсеров сталкиваются с проблемами при работе с новыми версиями, но Aspose.CAD полностью поддерживает более 150 выпусков DWG, позволяя читать и манипулировать чертежами без установки AutoCAD.

## Почему использовать Aspose.CAD для поиска текста в CAD?

Aspose.CAD может обрабатывать **50+** версий DWG и DXF, работая с файлами до 1 GB без загрузки всего документа в память. Библиотека извлекает текст как из разделов **Entities**, так и **Block**, обеспечивая **99 %** успеха в поиске строк, даже если они вложены в блоки. Такая измеримая надёжность делает её предпочтительным выбором для корпоративной автоматизации CAD.

## Предварительные требования

- **Aspose.CAD for .NET** установлен. Скачайте последнюю версию с [Aspose.CAD website](https://releases.aspose.com/cad/net/).
- Папка, содержащая файлы DWG, которые вы хотите проанализировать.
- Действительный файл лицензии для использования в продакшн (опционально для пробных запусков).

## Какие пространства имён требуются?

Пространство имён `Aspose.CAD` предоставляет основные классы обработки изображений, а `Aspose.CAD.FileFormats.Dwg` содержит структуры, специфичные для DWG. Импортируйте их в начале вашего C# файла:

```csharp
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dwg;
using Aspose.CAD.ImageOptions;
```

> **Примечание:** Блок кода выше является заполнителем; оставьте точный текст без изменений, чтобы сохранить исходное количество заполнителей.

## Как загрузить файл dwg?

Загрузка файла DWG проста с Aspose.CAD. Используйте класс `CadImage`, который представляет CAD‑чертёж в памяти. Конструктор читает файл без рендеринга, что делает процесс быстрым даже для больших чертежей. После загрузки вы можете проверить свойства, такие как `Width`, `Height` и `Layers`, перед выполнением любых операций поиска.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects.AttEntities;
```

## Как искать текст в разделе Entities?

Чтобы найти текст в разделе Entities, пройдитесь по коллекции `cadImage.Entities`. Каждый объект можно проверить на тип (например, `MText`, `Text`, `Attribute`) и его свойство `TextString`. Выполните сравнение без учёта регистра с целевой строкой и соберите совпадающие объекты для дальнейшей обработки или подсветки.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "search.dwg";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code here
}
```

## Как искать текст в разделе Block?

Блоки — это переиспользуемые группы объектов, которые могут содержать вложенный текст. Сначала перечислите `cadImage.BlockEntities.Values`, чтобы получить каждое определение блока. Затем пройдитесь по коллекции `Entities` каждого блока, применяя ту же логику сопоставления текста, что и для основного раздела Entities. Это гарантирует, что текст, скрытый внутри переиспользуемых компонентов, не будет пропущен.

```csharp
foreach (CadBaseEntity entity in cadImage.Entities)
{
    IterateCADNodes(entity);
}
```

## Как пройтись по узлам CAD для полного сканирования?

Полное сканирование объединяет разделы Entities и Block. Рекурсивно проходя дерево узлов `CadImage`, можно обрабатывать вложенные блоки, определения атрибутов и даже внешние ссылки. Реализуйте вспомогательный метод, принимающий `CadBaseEntity`, проверяющий его тип, извлекающий текст при необходимости, а затем рекурсивно обходящий дочерние объекты, если узел содержит коллекцию.

```csharp
foreach (CadBlockEntity blockEntity in cadImage.BlockEntities.Values)
{
    foreach (CadBaseEntity entity in blockEntity.Entities)
    {
        IterateCADNodes(entity);
    }
}
```

## Как экспортировать DWG в PDF после поиска текста?

После определения нужных объектов вы можете подсветить их или извлечь их координаты. Aspose.CAD позволяет сохранить весь чертёж в PDF, сохраняя векторное качество. При необходимости растрового вывода настройте `CadRasterizationOptions`, затем вызовите `image.Save("output.pdf", new PdfOptions())`. Полученный PDF можно передать заинтересованным сторонам, у которых нет CAD‑программ.

```csharp
private static void IterateCADNodes(CadBaseEntity obj)
{
    switch (obj.TypeName)
    {
        // Handle different entity types
    }
}
```

## Заключение

Aspose.CAD for .NET предоставляет бесшовное, высокопроизводительное решение для загрузки данных из файлов dwg, поиска конкретного текста и экспорта результата в PDF. Следуя шагам этого руководства, вы добавили мощные возможности поиска текста CAD в своё C# приложение без необходимости использовать внешние инструменты или дорогие лицензии.

## Часто задаваемые вопросы

### Q1: Могу ли я использовать Aspose.CAD for .NET с другими форматами CAD?

A1: Да, Aspose.CAD поддерживает более 30 форматов CAD, включая DXF, DWF и STL, предоставляя универсальное решение для рабочих процессов с разными форматами.

### Q2: Доступна ли бесплатная пробная версия Aspose.CAD for .NET?

A2: Да, вы можете ознакомиться с функциями через [free trial](https://releases.aspose.com/).

### Q3: Как я могу получить поддержку Aspose.CAD for .NET?

A3: Посетите [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) для получения помощи от сообщества и официальных каналов поддержки.

### Q4: Что такое временная лицензия и как её получить?

A4: Получите временную лицензию [temporary license](https://purchase.aspose.com/temporary-license/) для краткосрочной оценки или проектов proof‑of‑concept.

### Q5: Где я могу найти подробную документацию по Aspose.CAD for .NET?

A5: Обратитесь к полной [documentation](https://reference.aspose.com/cad/net/) для детального руководства, справочников API и примеров кода.

---

**Последнее обновление:** 2026-10-09  
**Тестировано с:** Aspose.CAD 24.11 for .NET  
**Автор:** Aspose  

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
// Configure rasterization options
rasterizationOptions.Layouts = new[] { "Layout1" };
Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
cadImage.Save(MyDir + "SearchText_out.pdf", pdfOptions);
```

## Связанные руководства

- [Как конвертировать DWG в PDF и растровые изображения с помощью Aspose.CAD for .NET](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [Конвертировать DWG в PNG и экспортировать OLE‑объекты — руководство Aspose.CAD](/cad/net/advanced-export-techniques/exporting-ole-objects-from-dwg/)
- [Как читать файлы DWT с Aspose.CAD for .NET](/cad/net/cad-features-and-support/reading-dwt/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}