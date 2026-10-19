---
date: 2026-10-19
description: Узнайте, как экспортировать чертежи AutoCAD в PDF с пользовательским
  размером страницы PDF, используя Aspose.CAD for Java. Это пошаговое руководство
  охватывает преобразование DWG в PDF, параметры растеризации и лицензирование.
keywords:
- custom pdf page size
- export autocad to pdf
- save cad as pdf
- generate pdf from dwg
- dwg to pdf java
lastmod: 2026-10-19
linktitle: Экспорт изображений AutoCAD в PDF
og_description: Установите пользовательский размер страницы PDF при экспорте чертежей
  AutoCAD в PDF с помощью Aspose.CAD for Java. Узнайте о преобразовании DWG в PDF,
  настройках растеризации и лицензировании за несколько минут.
og_image_alt: Guide showing how to export AutoCAD drawings to PDF with custom page
  dimensions using Aspose.CAD for Java
og_title: Установите пользовательский размер страницы PDF при экспорте AutoCAD с помощью
  Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-10-19'
  description: Learn how to export AutoCAD drawings to PDF with a custom PDF page
    size using Aspose.CAD for Java. This step‑by‑step guide covers converting DWG
    to PDF, rasterization options, and licensing.
  headline: Set custom PDF page size for AutoCAD export with Aspose.CAD
  type: TechArticle
- description: Learn how to export AutoCAD drawings to PDF with a custom PDF page
    size using Aspose.CAD for Java. This step‑by‑step guide covers converting DWG
    to PDF, rasterization options, and licensing.
  name: Set custom PDF page size for AutoCAD export with Aspose.CAD
  steps:
  - name: set the resource directory path
    text: '> **Pro tip:** Replace `"Your Document Directory"` with the absolute path
      to the folder you created in the prerequisites.'
  - name: load the CAD image
    text: The `Image` class loads the CAD file and gives you access to Aspose.CAD’s
      rasterization engine. > **Why this matters:** Once the CAD file is loaded, you
      can manipulate rasterization options before rendering to PDF.
  - name: set rasterization options
    text: The `CadRasterizationOptions` class specifies how the CAD drawing is rasterized
      before being saved as PDF. Adjust `pageWidth` and `pageHeight` to define a **custom
      PDF page size**. You can also enable 3‑D rendering by uncommenting the `setTypeOfEntities`
      line. - `pageWidth` / `pageHeight` – measured
  - name: configure PDF options
    text: The `PdfOptions` class holds PDF‑specific settings and links the rasterization
      options to the output file, ensuring the custom page dimensions are applied
      correctly.
  - name: save the PDF
    text: The `save` method writes the rendered image to the specified PDF file. The
      resulting file, `Export3DImagestoPDF_out_.pdf`, is a **save cad as pdf** representation
      of your original AutoCAD drawing with the exact page dimensions you specified.
  type: HowTo
- questions:
  - answer: Yes, the library supports DWG, DXF, DWF, DGN, and many more, giving you
      flexibility across projects.
    question: Can I use Aspose.CAD for Java with other CAD file formats?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to request a time‑limited license for evaluation.
    question: How do I obtain a temporary license for Aspose.CAD for Java?
  - answer: Absolutely. Use `setLayouts("Model")` or specify other layout names to
      control which view is rendered.
    question: Are there layout options for rasterization?
  - answer: Yes – modify `pageWidth` and `pageHeight` in the rasterization options
      to any dimensions you need.
    question: Can I customize the size of the output PDF file?
  - answer: The dedicated [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) offers
      community support and official responses from the Aspose team.
    question: Where can I get help or discuss issues related to Aspose.CAD for Java?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- custom pdf page size
- Aspose.CAD
- Java CAD conversion
- PDF generation
- DWG export
title: Установите пользовательский размер страницы PDF при экспорте AutoCAD с помощью
  Aspose.CAD
url: /ru/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Экспорт PDF из AutoCAD — экспорт изображений AutoCAD в PDF с помощью Aspose.CAD for Java

## Введение

Если вам нужно **конвертировать DWG в PDF** и контролировать точные размеры выходного файла, вы попали по адресу. Это руководство покажет, как задать **пользовательский размер страницы PDF** при экспорте изображений AutoCAD в PDF с помощью Aspose.CAD for Java. К концу руководства вы узнаете, как загрузить DWG, настроить параметры растеризации, такие как DPI и ширина/высота страницы, применить лицензию и создать готовый к производству PDF.

## Быстрые ответы
- **Можно ли конвертировать DWG в PDF с помощью Java?** Да — Aspose.CAD for Java нативно поддерживает DWG, DXF, DWF и многие другие форматы CAD.  
- **Нужна ли лицензия для использования в продакшене?** Полная лицензия Aspose.CAD снимает все ограничения оценки; временная лицензия доступна для тестирования.  
- **Какие версии Java совместимы?** Библиотека работает с Java 8 и любой более новой JDK.  
- **Как изменить размеры страницы PDF?** Установите `pageWidth` и `pageHeight` в `PdfOptions.getRasterizationOptions()` на любой требуемый размер.  
- **Поддерживается ли 3‑D рендеринг?** Да — включите `TypeOfEntities.Entities3D` для растеризации 3‑D сущностей.

## Что такое экспорт PDF из AutoCAD?
Экспорт PDF из AutoCAD означает преобразование векторных CAD‑чертежей (DWG, DXF, DWF и т.д.) в переносимый PDF‑документ с сохранением слоёв, толщины линий и при необходимости 3‑D геометрии. Это позволяет делиться проектами с клиентами, архивировать чертежи или печатать без установки CAD‑программного обеспечения.

## Почему стоит использовать Aspose.CAD for Java для конвертации DWG в PDF?
Aspose.CAD for Java идеален для конвертации DWG в PDF, поскольку предлагает обширную поддержку форматов, работает на чистом Java без нативных зависимостей, обеспечивает высоко‑разрешающую растеризацию с полным контролем DPI и размера страницы, а также гибкую лицензирование, позволяющее начать с пробной версии и перейти к продакшн‑использованию.

- **Широкая поддержка форматов** — поддерживает более 50 входных и выходных форматов, включая DWG, DXF, DWF, DGN и PDF.  
- **Чистая Java‑реализация** — без нативных DLL и внешних зависимостей, поэтому развертывание просто на любой платформе.  
- **Высокое разрешение растеризации** — вы можете задавать DPI, размер страницы и макет, получая полный контроль над **пользовательским размером страницы PDF** результата.  
- **Масштабируемое лицензирование** — начните с бесплатной пробной версии, затем перейдите к постоянной **лицензии Aspose CAD**.  

## Требования

- **Java Development Kit** — установлен JDK 8 или новее.  
- **Aspose.CAD for Java** — скачайте последнюю JAR‑библиотеку по [download link](https://releases.aspose.com/cad/java/).  
- **Рабочий каталог** — папка, содержащая исходные DWG‑файлы и получающая сгенерированные PDF‑файлы.

## Импорт пространств имён

Класс `Image` — основной объект Aspose.CAD, представляющий CAD‑чертеж в памяти. Импортируйте необходимые пакеты перед началом кодирования.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

Теперь пройдёмся по коду шаг за шагом.

## Как задать пользовательский размер страницы PDF при экспорте DWG в PDF?

Загрузите ваш DWG, задайте желаемую ширину и высоту страницы, затем сохраните результат как PDF — всё, что нужно для создания PDF с пользовательским размером страницы. Ниже показана точная последовательность и минимальный необходимый код.

### Шаг 1: установить путь к каталогу ресурсов

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **Pro tip:** Замените `"Your Document Directory"` на абсолютный путь к папке, которую вы создали в разделе требований.

### Шаг 2: загрузить CAD‑изображение

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **Why this matters:** После загрузки CAD‑файла вы можете изменять параметры растеризации перед рендерингом в PDF.

### Шаг 3: задать параметры растеризации

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- `pageWidth` / `pageHeight` — измеряется в пикселях; измените эти значения, чтобы соответствовать A4, Letter или любой пользовательской размерности.  
- `setTypeOfEntities(TypeOfEntities.Entities3D)` — рендерит 3‑D сущности при необходимости.  
- `setLayouts` — выбирает, какой макет (Model, Layout1 и т.д.) растеризовать.

### Шаг 4: настроить параметры PDF

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Шаг 5: сохранить PDF

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

Полученный файл `Export3DImagestoPDF_out_.pdf` представляет собой **save cad as pdf** версию вашего оригинального чертежа AutoCAD с точно заданными размерами страницы.

## Распространённые проблемы и решения

| Симптом | Вероятная причина | Решение |
|---------|-------------------|---------|
| Пустой PDF | Параметры растеризации не заданы или несоответствие макета | Проверьте, что `setLayouts` соответствует имени макета в вашем CAD‑файле. |
| Низкое разрешение изображения | `pageWidth`/`pageHeight` слишком малы или DPI низкое | Увеличьте размеры или вызовите `rasterizationOptions.setResolution(...)` с более высоким DPI. |
| Исключение лицензии | Не применена действующая лицензия | Примените постоянную лицензию Aspose.CAD или используйте временную лицензию для тестирования. |

## Часто задаваемые вопросы

**Q: Можно ли использовать Aspose.CAD for Java с другими форматами CAD‑файлов?**  
A: Да, библиотека поддерживает DWG, DXF, DWF, DGN и многие другие, предоставляя гибкость в разных проектах.

**Q: Как получить временную лицензию для Aspose.CAD for Java?**  
A: Перейдите на страницу [temporary license page](https://purchase.aspose.com/temporary-license/) и запросите ограниченную по времени лицензию для оценки.

**Q: Есть ли варианты выбора макета для растеризации?**  
A: Конечно. Используйте `setLayouts("Model")` или укажите другие имена макетов, чтобы контролировать, какой вид будет отрисован.

**Q: Можно ли настроить размер выходного PDF‑файла?**  
A: Да — измените `pageWidth` и `pageHeight` в параметрах растеризации на любые необходимые вам размеры.

**Q: Где можно получить помощь или обсудить проблемы, связанные с Aspose.CAD for Java?**  
A: На специализированном [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) вы найдёте поддержку сообщества и официальные ответы от команды Aspose.

## Дополнительные FAQ (формат, удобный для ИИ)

**Q: Требует ли Aspose.CAD какие‑либо нативные библиотеки на Windows или Linux?**  
A: Нет. Aspose.CAD for Java — это чисто Java‑библиотека, поэтому она работает на любой платформе, поддерживающей JDK, без дополнительных нативных DLL.

**Q: Какой максимальный размер DWG‑файла может обработать библиотека?**  
A: Библиотека способна обрабатывать чертежи с несколькими сотнями страниц (до 500 МБ) без загрузки всего файла в память благодаря потоковой архитектуре.

**Q: Можно ли пакетно конвертировать множество DWG‑файлов в PDF за один запуск?**  
A: Да. Пройдитесь по каталогу, загрузите каждый файл с помощью `Image.load()`, примените одинаковые параметры растеризации и вызовите `save()` для каждого выходного PDF.

**Q: Какую производительность можно ожидать на типичном сервере?**  
A: Конвертация 100‑страничного DWG при 300 DPI на стандартном процессоре 2.5 GHz занимает примерно 12 секунд, согласно тестам Aspose.

**Q: Сохраняет ли библиотека информацию о слоях в PDF?**  
A: Хотя вывод растеризуется, визуальное представление слоёв, толщины линий и цветов точно воспроизводится.

---

**Последнее обновление:** 2026-10-19  
**Тестировано с:** Aspose.CAD for Java 24.10  
**Автор:** Aspose

## Связанные руководства

- [Экспорт DWG в PDF и включение отслеживания с Aspose.CAD Java](/cad/java/additional-features/enable-tracking/)
- [Экспорт DWG в PDF: конкретный макет с использованием Aspose.CAD Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Экспорт DWG в BMP и корректировка размера CAD с использованием типа единицы в Aspose.CAD for Java](/cad/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}