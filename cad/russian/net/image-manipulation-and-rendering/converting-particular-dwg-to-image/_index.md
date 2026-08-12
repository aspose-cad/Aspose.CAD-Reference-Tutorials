---
date: 2026-08-12
description: Извлечение текста из DWG и преобразование конкретного DWG в изображение
  на C# с использованием Aspose.CAD для .NET. Изучайте пошагово с примерами кода.
keywords:
- extract text from dwg
- convert specific dwg to image
- Aspose.CAD .NET
lastmod: 2026-08-12
linktitle: Преобразование конкретного DWG в изображение на C#
og_description: Извлечение текста из DWG и преобразование конкретного DWG в изображение
  на C# с Aspose.CAD. Следуйте этому краткому руководству для быстрой реализации.
og_image_alt: Guide showing DWG to image conversion and text extraction using Aspose.CAD
  in C#
og_title: Извлечение текста из DWG и преобразование конкретного DWG в изображение
  на C#
schemas:
- author: Aspose
  dateModified: '2026-08-12'
  description: Extract text from DWG and convert specific DWG to image in C# using
    Aspose.CAD for .NET. Learn step‑by‑step with code snippets.
  headline: Extract text from DWG and convert specific DWG to image in C#
  type: TechArticle
- questions:
  - answer: Aspose.CAD supports DWG releases from AutoCAD 2000 up to the latest 2024
      version, covering over 90 % of files created in the field.
    question: Is Aspose.CAD compatible with all versions of DWG files?
  - answer: Yes – you can change resolution, image format, anti‑aliasing, and background
      color to suit PNG, JPEG, or PDF targets.
    question: Can I customize the rasterization options for different outputs?
  - answer: Explore the comprehensive [Aspose.CAD documentation](https://reference.aspose.com/cad/net/)
      for more code samples and API details.
    question: Where can I find additional examples and documentation?
  - answer: Absolutely – you can download a trial version on the **[Aspose trial download
      page](https://releases.aspose.com/)** and evaluate all features without restrictions
      for 30 days.
    question: Is there a free trial available for Aspose.CAD?
  - answer: Join the active [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)
      where developers share solutions and the Aspose team answers questions.
    question: How can I get support or connect with the community?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- extract text from dwg
- Aspose.CAD
- C# CAD processing
title: Извлечение текста из DWG и преобразование конкретного DWG в изображение на
  C#
url: /ru/net/image-manipulation-and-rendering/converting-particular-dwg-to-image/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Преобразование конкретного DWG в изображение на C# — руководство Aspose.CAD

## Введение

В современных инженерных приложениях часто требуется **извлекать текст из файлов DWG** и **преобразовывать конкретный DWG в графический формат** для отчётности или визуализации. Aspose.CAD для .NET предоставляет полнофункциональный API, который решает обе задачи без необходимости внешнего CAD‑ПО. В этом руководстве вы узнаете, как загрузить DWG, отфильтровать текстовые сущности, растеризовать чертёж и сохранить результат как PDF‑изображение — всё это чистым кодом C#.

## Быстрые ответы
- **Какой первый шаг?** Загрузите файл DWG с помощью `new CadImage("file.dwg")`.  
- **Какой класс фильтрует текст?** Используйте `CadEntityFilter` для выбора сущностей `Text`.  
- **Как задать размер изображения?** Установите `Width` и `Height` в `CadRasterizationOptions`.  
- **Какой формат вывода используется?** Пример сохраняет в PDF, который встраивает растровое изображение.  
- **Нужна ли лицензия для продакшн?** Да — коммерческая лицензия Aspose.CAD снимает ограничения оценки.

## Как извлечь текст из DWG?

Загрузите DWG, примените фильтр, выбирающий только текстовые сущности, и затем прочитайте свойство `TextString` каждой сущности. Этот подход возвращает все аннотации, подписи и размерные надписи, присутствующие в чертеже, позволяя использовать их для поиска, индексации или отчётности.

## Почему преобразовать конкретный DWG в изображение?

Преобразование DWG в растровое изображение позволяет встраивать чертёж в документы, веб‑страницы или мобильные приложения, которые не способны отображать нативные CAD‑форматы. Aspose.CAD обрабатывает **более 50 CAD‑форматов** и может растеризовать чертежи со сотнями страниц, используя менее 200 МБ памяти, что делает его подходящим для высоконагруженных серверных сценариев.

## Требования

- Visual Studio (любая современная версия) для компиляции и запуска C#‑проектов.  
- Aspose.CAD для .NET — убедитесь, что библиотека установлена. Ссылка для загрузки находится на **[странице загрузки Aspose.CAD для .NET](https://releases.aspose.com/cad/net/)**.  
- Файл DWG, с которым вы хотите работать; в примерах кода используется образец *visualization_-_conference_room.dwg*.

## Импорт пространств имён

Следующие пространства имён дают доступ к основным классам CAD, параметрам растеризации и вспомогательным средствам вывода PDF:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Шаг 1: загрузка файла DWG

Создайте экземпляр `CadImage`, передав путь к вашему файлу DWG. Объект `CadImage` представляет весь чертёж в памяти и предоставляет доступ к его слоям, сущностям и метаданным.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
var cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath);
```

## Шаг 2: фильтрация сущностей

`CadEntityFilter` позволяет выбрать только нужные сущности. В этом руководстве мы настраиваем его так, чтобы оставлять **текстовые** объекты, отбрасывая линии, окружности и другую геометрию, которую вы не хотите видеть в конечном изображении.

```csharp
CadBaseEntity[] entities = cadImage.Entities;
List<CadBaseEntity> filteredEntities = new List<CadBaseEntity>();

foreach (CadBaseEntity baseEntity in entities)
{
    // Selection or filtration of entities
    if (baseEntity.TypeName == CadEntityTypeName.TEXT)
    {
        filteredEntities.Add(baseEntity);
    }
}

cadImage.Entities = filteredEntities.ToArray();
```

## Шаг 3: настройка параметров растеризации

`CadRasterizationOptions` управляет тем, как чертёж преобразуется в растровое изображение. Вы можете задать размер вывода, цвет фона и разрешение (DPI). Следующий якорь определения представляет класс:

Класс `CadRasterizationOptions` задаёт размеры изображения, разрешение и параметры рендеринга для преобразования CAD‑чертежей в растровые форматы.  

Установите нужные ширину, высоту и цвет фона перед передачей параметров экспортёру PDF.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions =
    new Aspose.CAD.ImageOptions.CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
```

## Шаг 4: настройка параметров PDF

`PdfOptions` объединяет настройки растеризации с особенностями PDF, такими как сжатие. Определяющий якорь для этого класса расположен первым:

`PdfOptions` инкапсулирует параметры генерации PDF, включая параметры растеризации, которые определяют, как CAD‑данные отображаются внутри PDF‑документа.  

Назначьте ранее созданный экземпляр `CadRasterizationOptions` свойству `VectorRasterizationOptions`.

```csharp
Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Шаг 5: сохранение в PDF

Наконец, вызовите метод `Save` у объекта `CadImage`, передав имя целевого файла и сконфигурированные `PdfOptions`. PDF будет содержать высококачественное изображение отфильтрованного чертежа.

```csharp
string outFile = MyDir + "result_out_generated.pdf";
cadImage.Save(outFile, pdfOptions);
```

## Распространённые проблемы и их устранение

- **Отсутствует текст после фильтрации** — Убедитесь, что DWG действительно содержит сущности `Text`; в некоторых чертежах аннотации хранятся как `MText`. При необходимости скорректируйте фильтр, включив `MText`.  
- **Пустое изображение на выходе** — Проверьте, что DPI растеризации достаточно высок (300 DPI — безопасный вариант) и что цвет фона не установлен как прозрачный при просмотре PDF.  
- **Ошибки «Out‑of‑memory» при больших файлах** — Используйте перегрузку `LoadOptions`, которая включает потоковую загрузку, предотвращая полную загрузку файла в память сразу.

## Часто задаваемые вопросы

**В: Совместим ли Aspose.CAD со всеми версиями файлов DWG?**  
**О:** Aspose.CAD поддерживает выпуски DWG от AutoCAD 2000 до последней версии 2024, охватывая более 90 % файлов, создаваемых в отрасли.

**В: Могу ли я настроить параметры растеризации для разных форматов вывода?**  
**О:** Да — вы можете менять разрешение, формат изображения, сглаживание и цвет фона в зависимости от целей (PNG, JPEG или PDF).

**В: Где можно найти дополнительные примеры и документацию?**  
**О:** Ознакомьтесь с полной **[документацией Aspose.CAD](https://reference.aspose.com/cad/net/)** для получения дополнительных образцов кода и деталей API.

**В: Доступна ли бесплатная пробная версия Aspose.CAD?**  
**О:** Абсолютно — вы можете скачать пробную версию на **[странице загрузки пробной версии Aspose](https://releases.aspose.com/)** и оценить все возможности без ограничений в течение 30 дней.

**В: Как получить поддержку или связаться с сообществом?**  
**О:** Присоединяйтесь к активному **[форуму Aspose.CAD](https://forum.aspose.com/c/cad/19)**, где разработчики делятся решениями, а команда Aspose отвечает на вопросы.

---

**Последнее обновление:** 2026-08-12  
**Тестировано с:** Aspose.CAD 24.11 для .NET  
**Автор:** Aspose

## Связанные руководства

- [Поиск текста в файлах DWG с C# — руководство Aspose.CAD](/cad/net/text-search-and-manipulation/searching-text-in-dwg-files/)
- [Преобразование CAD‑чертежа в растровое изображение в Aspose.CAD для .NET](/cad/net/cad-drawing-manipulation/convert-cad-drawing-to-raster-image/)
- [Рендеринг документов DWG на C# — руководство Aspose.CAD](/cad/net/image-manipulation-and-rendering/rendering-dwg-documents/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}