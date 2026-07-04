---
date: 2026-07-04
description: Узнайте, как установить размер страницы PDF и экспортировать PDF из 3D‑изображений
  CAD с использованием Aspose.CAD для .NET — пошаговое руководство по конвертации
  DWG в PDF и сохранению CAD в PDF.
keywords:
- set pdf page size
- export pdf from cad
- convert dwg to pdf
- save cad as pdf
- cad to pdf tutorial
linktitle: Экспорт 3D‑изображений в PDF
schemas:
- author: Aspose
  dateModified: '2026-07-04'
  description: Learn how to set PDF page size and export PDF from 3D CAD images using
    Aspose.CAD for .NET – a step‑by‑step guide to convert DWG to PDF and save CAD
    as PDF.
  headline: Set PDF page size – Export 3D Images to PDF with Aspose.CAD
  type: TechArticle
- description: Learn how to set PDF page size and export PDF from 3D CAD images using
    Aspose.CAD for .NET – a step‑by‑step guide to convert DWG to PDF and save CAD
    as PDF.
  name: Set PDF page size – Export 3D Images to PDF with Aspose.CAD
  steps:
  - name: Load the CAD Image
    text: '`Image` class represents a CAD drawing loaded into memory, ready for rasterization.'
  - name: Configure Rasterization Options (Save CAD as PDF)
    text: '`RasterizationOptions` class defines how the CAD data is rasterized, including
      page size, DPI, and whether 3‑D entities are rendered.'
  - name: Set PDF Options (Create PDF from CAD)
    text: '`PdfOptions` class holds the output format settings and links the rasterization
      options to PDF generation.'
  - name: Save as PDF (Generate PDF from 3D Model)
    text: '`Save` method on the `Image` object writes the rasterized content to the
      specified PDF file, producing a ready‑to‑share document.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD supports more than 50 input and output formats, including
      DWG, DXF, DGN, STL, and IFC, ensuring flexibility for any project.
    question: Is Aspose.CAD compatible with all CAD file formats?
  - answer: Absolutely. Set `PageWidth` and `PageHeight` in `RasterizationOptions`
      to any size in points, inches, or millimetres before calling `Save`.
    question: Can I customize the page dimensions when exporting to PDF?
  - answer: Yes, you can obtain temporary licenses for Aspose.CAD by visiting [Temporary
      License](https://purchase.aspose.com/temporary-license/).
    question: Are temporary licenses available for Aspose.CAD?
  - answer: Head to the [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) for
      expert help and peer‑to‑peer advice.
    question: Where can I find additional support or community discussions?
  - answer: Yes, you can explore the features of Aspose.CAD by accessing the [free
      trial](https://releases.aspose.com/).
    question: Is there a free trial version of Aspose.CAD?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Установить размер страницы PDF – Экспорт 3D‑изображений в PDF с помощью Aspose.CAD
url: /ru/net/3d-image-export/exporting-3d-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Экспорт 3D‑изображений в PDF — руководство Aspose.CAD

## Введение

Если вам нужно **установить размер страницы PDF** при конвертации 3‑D CAD‑чертежа в PDF, вы попали в нужное место. В этом руководстве шаг за шагом показано, как загрузить CAD‑файл, настроить параметры растеризации — включая пользовательские размеры страницы, — и создать PDF высокого качества с помощью Aspose.CAD для .NET. В конце вы сможете **экспортировать PDF из CAD**, **сохранить CAD как PDF** и контролировать каждый элемент макета без установки AutoCAD.

## Быстрые ответы
- **Что означает «export PDF from CAD»?** Он преобразует CAD‑чертеж (DWG, DXF, DGN и др.) в PDF, который можно открыть на любом устройстве.  
- **Какая библиотека выполняет конвертацию?** Aspose.CAD for .NET обеспечивает растеризацию и экспорт в PDF без внешних зависимостей.  
- **Нужна ли лицензия?** Для использования в продакшене требуется временная или полная лицензия; доступна бесплатная пробная версия.  
- **Можно ли задать пользовательские размеры страницы?** Да — используйте `PageWidth` и `PageHeight` в `RasterizationOptions`.  
- **Сохранится ли 3‑D геометрия?** 3‑D объекты растеризуются; включите `TypeOfEntities.Entities3D` для полной поддержки 3‑D.

## Что означает «export PDF» в контексте CAD?

Экспорт PDF из CAD означает взятие CAD‑чертежа (DWG, DXF, DGN и др.) и преобразование его в PDF‑файл, который может содержать векторную графику, растеризованные 3‑D виды и точную информацию о макете страницы, что упрощает обмен с теми, у кого нет CAD‑программного обеспечения.

## Почему использовать Aspose.CAD для экспорта PDF?

Aspose.CAD позволяет вам **установить размер страницы PDF** и экспортировать PDF полностью в управляемом коде .NET. Он поддерживает более 50 форматов CAD, обрабатывает файлы до 2 ГБ без загрузки всего документа в память и сохраняет толщину линий, цвета и опциональное рендеринг 3‑D объектов с растеризацией DPI до 1200. Библиотека работает на Windows, Linux и macOS, поэтому созданные PDF работают на любой платформе.

## Требования

- **Aspose.CAD for .NET** установлен. Скачайте его со страницы [Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/).  
- Папка, содержащая CAD‑файлы, которые вы хотите конвертировать (например, `C:\CAD\`).  
- .NET 6.0 или новее (или .NET Framework 4.7.2).  

## Импорт пространств имён

`using`‑операторы импортируют пространства имён Aspose.CAD, необходимые для работы с параметрами растеризации и PDF.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

## Пошаговое руководство

### Как установить размер страницы PDF при экспорте CAD в PDF?

Загрузите ваш CAD‑файл, настройте размеры страницы в `RasterizationOptions`, привяжите эти параметры к экземпляру `PdfOptions` и вызовите `Save`. Этот четырёхшаговый процесс дает полный контроль над размером и качеством вывода, при этом код остаётся лаконичным.

### Шаг 1: Загрузка CAD‑изображения

Класс `Image` представляет CAD‑чертеж, загруженный в память и готовый к растеризации.  

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image cadImage = Image.Load(sourceFilePath))
{
    // Your code for loading the CAD image goes here
}
```

### Шаг 2: Настройка параметров растеризации (Сохранить CAD как PDF)

Класс `RasterizationOptions` определяет, как CAD‑данные растеризуются, включая размер страницы, DPI и рендеринг 3‑D объектов.  

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
// rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;

rasterizationOptions.Layouts = new string[] { "Model" };
```

### Шаг 3: Установка параметров PDF (Создание PDF из CAD)

Класс `PdfOptions` содержит настройки выходного формата и связывает параметры растеризации с генерацией PDF.  

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### Шаг 4: Сохранить как PDF (Генерация PDF из 3D‑модели)

Метод `Save` объекта `Image` записывает растеризованное содержимое в указанный PDF‑файл, создавая готовый к распространению документ.  

```csharp
MyDir = MyDir + "Export3DImagestoPDF_out.pdf";
cadImage.Save(MyDir, pdfOptions);
```

## Распространённые проблемы и решения

| Проблема | Причина | Решение |
|----------|---------|---------|
| **PDF пустой** | Неправильное имя макета или отсутствует макет `Model`. | Убедитесь, что `rasterizationOptions.Layouts` соответствует макету, присутствующему в CAD‑файле. |
| **Низкое разрешение** | DPI растеризации по умолчанию низкое. | Установите `rasterizationOptions.Resolution = 300;` перед сохранением. |
| **3‑D объекты не отображаются** | `TypeOfEntities` закомментирован. | Раскомментируйте `rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;`. |
| **Исключение лицензии** | Использование пробной версии без лицензии. | Примените временную или постоянную лицензию через `License license = new License(); license.SetLicense("Aspose.CAD.lic");`. |

## Часто задаваемые вопросы

**Q: Совместим ли Aspose.CAD со всеми форматами CAD‑файлов?**  
A: Да, Aspose.CAD поддерживает более 50 форматов ввода и вывода, включая DWG, DXF, DGN, STL и IFC, обеспечивая гибкость для любого проекта.

**Q: Можно ли настроить размеры страницы при экспорте в PDF?**  
A: Абсолютно. Установите `PageWidth` и `PageHeight` в `RasterizationOptions` на любой размер в пунктах, дюймах или миллиметрах перед вызовом `Save`.

**Q: Доступны ли временные лицензии для Aspose.CAD?**  
A: Да, временные лицензии для Aspose.CAD можно получить, посетив страницу [Temporary License](https://purchase.aspose.com/temporary-license/).

**Q: Где можно найти дополнительную поддержку или обсуждения сообщества?**  
A: Перейдите на [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) для получения экспертной помощи и советов от коллег.

**Q: Есть ли бесплатная пробная версия Aspose.CAD?**  
A: Да, вы можете ознакомиться с функциями Aspose.CAD, перейдя по ссылке [free trial](https://releases.aspose.com/).

## Заключение

Теперь у вас есть полноценный, готовый к продакшену метод **установить размер страницы PDF** и **экспортировать PDF из 3D CAD‑изображений** с помощью Aspose.CAD для .NET. Настраивая параметры растеризации, вы можете точно регулировать разрешение, макет страницы и рендеринг 3‑D объектов, чтобы удовлетворить любые требования к документации. Экспериментируйте с различными настройками DPI и размерами страницы, чтобы достичь идеального баланса между размером файла и визуальной точностью.

{{< blocks/products/products-backtop-button >}}

## Похожие руководства

- [Экспорт конкретных макетов в PDF — руководство Aspose.CAD](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)
- [Экспорт DWG в PDF или растровые изображения — руководство Aspose.CAD](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [Экспорт DGN в PDF в Aspose.CAD для .NET](/cad/net/cad-export-formats/export-dgn-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

--- 

**Последнее обновление:** 2026-07-04  
**Тестировано с:** Aspose.CAD 24.11 for .NET  
**Автор:** Aspose