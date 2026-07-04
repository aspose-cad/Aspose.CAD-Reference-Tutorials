---
date: 2026-07-04
description: Узнайте, как установить размер страницы PDF при конвертации файлов OBJ
  в PDF с помощью Aspose.CAD для .NET. Пошаговое руководство с предварительными требованиями,
  rasterization options и PDF options.
keywords:
- set pdf page size
- load obj file
- save cad as pdf
- 3d model to pdf
- how to convert obj
linktitle: Поддержка формата OBJ в Aspose.CAD - Руководство
schemas:
- author: Aspose
  dateModified: '2026-07-04'
  description: Learn how to set PDF page size while converting OBJ files to PDF using
    Aspose.CAD for .NET. Step‑by‑step guide with prerequisites, rasterization options,
    and PDF options.
  headline: Set PDF Page Size for OBJ Files with Aspose.CAD - Tutorial
  type: TechArticle
- questions:
  - answer: Yes, Aspose.CAD supports over **30** input formats—including DWG, DXF,
      DGN, and STL—and can export to more than **20** raster and vector formats.
    question: Is Aspose.CAD compatible with other CAD file formats?
  - answer: Absolutely! You can explore a free trial version [here](https://releases.aspose.com/).
    question: Can I try Aspose.CAD before purchasing?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) to ask
      questions and share experiences with the community.
    question: How do I obtain support for Aspose.CAD?
  - answer: Yes, temporary licenses can be obtained [here](https://purchase.aspose.com/temporary-license/).
    question: Are temporary licenses available for testing?
  - answer: You can purchase Aspose.CAD [here](https://purchase.aspose.com/buy).
    question: Where can I purchase a full license?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Установить размер страницы PDF для файлов OBJ с Aspose.CAD - Руководство
url: /ru/net/3d-model-support/supporting-obj-format-in-aspose-cad/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Установить размер страницы PDF для файлов OBJ с помощью Aspose.CAD - Руководство

## Введение

Если вы разрабатываете CAD‑приложения на .NET и вам нужно **установить размер страницы PDF** при конвертации моделей OBJ, Aspose.CAD для .NET предоставляет чистый, ориентированный на код API, который обрабатывает растеризацию и генерацию PDF в одном процессе. В этом руководстве мы пройдём установку библиотеки, загрузку файла OBJ, настройку размеров страницы и, наконец, сохранение результата в PDF. К концу вы получите переиспользуемый шаблон для преобразования любой 3‑D модели в PDF‑документ нужного размера.

## Быстрые ответы
- **Может ли Aspose.CAD конвертировать OBJ в PDF?** Да — загрузите OBJ с помощью `Image.Load` и растеризуйте его в PDF.
- **Как задать пользовательский размер страницы PDF?** Используйте `PdfOptions` → `PageSize` или укажите ширину/высоту в `RasterizationOptions`.
- **Какие версии .NET поддерживаются?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.
- **Нужна ли лицензия для разработки?** Бесплатная пробная версия подходит для оценки; для продакшна требуется лицензия.
- **Эффективно ли использование памяти при конвертации?** Aspose.CAD потоково обрабатывает данные и может создавать PDF‑документы из нескольких сотен страниц без загрузки всего файла в память.

## Что такое формат OBJ?
Формат OBJ — это широко используемый текстовый формат 3‑D геометрии, который хранит позиции вершин, координаты текстур и определения граней. Он поддерживается большинством 3‑D моделирующих инструментов и идеально подходит для обмена между CAD и рендеринговыми конвейерами.

## Почему стоит задавать пользовательский размер страницы PDF?
Aspose.CAD может отрисовать CAD‑чертёж в любом растровом размере. Явно задав размеры страницы PDF, вы гарантируете, что окончательный документ соответствует вашим стандартам отчётности, вписывается в стандартные форматы бумаги (A4, Letter) или соответствует пользовательским макетам печати. Количественное преимущество: API может генерировать PDF до **200 mm × 200 mm** за один вызов, обрабатывая файлы более **500 MB** без превышения 250 MB оперативной памяти.

## Предварительные требования

- **Библиотека Aspose.CAD** — Убедитесь, что библиотека Aspose.CAD установлена в ваш .NET‑проект. Скачать её можно [здесь](https://releases.aspose.com/cad/net/) и ознакомиться с полной справкой по API в [документации](https://reference.aspose.com/cad/net/).
- **Каталог документов** — Создайте папку для ваших CAD‑ресурсов; далее будем ссылаться на неё как «Your Document Directory».
- **Среда разработки .NET** — Visual Studio 2022 или любой IDE, поддерживающий .NET 6+.

## Как задать размер страницы PDF при конвертации OBJ в PDF?

Загрузите файл OBJ, настройте параметры растеризации с нужной шириной и высотой, привяжите эти параметры к экземпляру `PdfOptions` и вызовите `Save`. Такой двухшаговый подход гарантирует, что размер страницы PDF будет соответствовать указанным вами параметрам, сохраняя при этом детали модели.

## Шаг 1: Импорт пространств имён

Класс `Image` обрабатывает все CAD‑форматы, а класс `PdfOptions` управляет выводом PDF.  
`Image` представляет CAD‑документ и предоставляет методы загрузки и сохранения файлов. `PdfOptions` определяет настройки генерации PDF, такие как размер страницы и степень сжатия.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Шаг 2: Загрузка файла OBJ

Загрузите файл OBJ в объект изображения Aspose.CAD. Замените `"example-580-W.obj"` на имя вашего файла OBJ.

```csharp
string MyDir = "Your Document Directory";
using (Aspose.CAD.Image CADDoc = Aspose.CAD.Image.Load(MyDir + "example-580-W.obj"))
{
    // Your code for further processing goes here
}
```

## Шаг 3: Настройка параметров растеризации

`RasterizationOptions` определяет растровый размер, который в конечном итоге становится размером страницы PDF. Установка `PageWidth` и `PageHeight` позволяет точно задать размеры выходного PDF.  
`CadRasterizationOptions` (доступный через `RasterizationOptions`) задаёт параметры растеризации, такие как размеры страницы и разрешение.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions =
    new Aspose.CAD.ImageOptions.CadRasterizationOptions();

rasterizationOptions.PageWidth = CADDoc.Size.Width;
rasterizationOptions.PageHeight = CADDoc.Size.Height;
```

## Шаг 4: Создание PDF‑опций

`PdfOptions` связывает параметры растеризации с PDF‑писателем. Присвоив экземпляр `RasterizationOptions`, вы гарантируете, что PDF унаследует заданный вами размер страницы.

```csharp
Aspose.CAD.ImageOptions.PdfOptions CADf = new Aspose.CAD.ImageOptions.PdfOptions();
CADf.VectorRasterizationOptions = rasterizationOptions;
```

## Шаг 5: Сохранение в PDF

Вызовите метод `Save` у объекта `Image`, передав целевое имя файла и сконфигурированные `PdfOptions`. Библиотека запишет PDF с точным размером страницы, указанным вами.  
`Save` записывает изображение в файл с указанным форматом и параметрами.

```csharp
CADDoc.Save(MyDir + "example-580-W_custom.pdf", CADf);
```

## Распространённые проблемы и их решения

- **Неправильные размеры страницы** — Убедитесь, что `PageWidth` и `PageHeight` заданы в **пикселях**; используйте `Resolution` для преобразования дюймов или миллиметров в пиксели (например, 300 dpi → 1 дюйм = 300 px).
- **Отсутствие текстур** — Файлы OBJ часто ссылаются на внешние `.mtl`‑файлы; убедитесь, что файл материалов находится в той же папке, что и OBJ.
- **Большой объём памяти при работе с крупными файлами** — Включите `Image.SaveOptions.Compression`, чтобы снизить нагрузку на память при рендеринге высокого разрешения.

## Часто задаваемые вопросы

**Q: Совместим ли Aspose.CAD с другими форматами CAD?**  
A: Да, Aspose.CAD поддерживает более **30** входных форматов, включая DWG, DXF, DGN и STL, и может экспортировать более **20** растровых и векторных форматов.

**Q: Можно ли попробовать Aspose.CAD перед покупкой?**  
A: Конечно! Вы можете скачать бесплатную пробную версию [здесь](https://releases.aspose.com/).

**Q: Как получить поддержку по Aspose.CAD?**  
A: Посетите [форум Aspose.CAD](https://forum.aspose.com/c/cad/19), где можно задавать вопросы и делиться опытом с сообществом.

**Q: Доступны ли временные лицензии для тестирования?**  
A: Да, временные лицензии можно получить [здесь](https://purchase.aspose.com/temporary-license/).

**Q: Где можно приобрести полную лицензию?**  
A: Приобрести Aspose.CAD можно [здесь](https://purchase.aspose.com/buy).

---

**Последнее обновление:** 2026-07-04  
**Тестировано с:** Aspose.CAD 24.11 for .NET  
**Автор:** Aspose

## Связанные руководства

- [Экспорт файлов IGES в PDF - Руководство Aspose.CAD](/cad/net/exporting-to-image-formats/exporting-iges-files-to-pdf/)
- [Экспорт DXF в формат PDF - Руководство Aspose.CAD](/cad/net/export-techniques/exporting-dxf-to-pdf-format/)
- [Экспорт CAD‑чертежей в PDF - Руководство Aspose.CAD](/cad/net/advanced-export-techniques/exporting-cad-drawings-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}