---
date: 2026-10-04
description: Узнайте, как искать текст в файлах DWG с использованием C# и Aspose.CAD
  для .NET. Извлекайте текст, читайте файлы DWG и повышайте эффективность ваших CAD‑приложений.
keywords:
- search text in dwg
- extract text from dwg
- c# read dwg file
- how to search dwg files
lastmod: 2026-10-04
linktitle: Поиск и обработка текста
og_description: Поиск текста в файлах DWG с использованием C# и Aspose.CAD для .NET.
  Извлекайте текст, читайте файлы DWG и улучшайте производительность CAD‑приложений.
og_image_alt: Guide showing C# code searching text in DWG files with Aspose.CAD
og_title: Поиск текста в файлах DWG с помощью C# и Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-10-04'
  description: Learn how to search text in DWG files using C# and Aspose.CAD for .NET.
    Extract text, read DWG files, and boost your CAD applications.
  headline: Search text in DWG files with C# using Aspose.CAD
  type: TechArticle
- description: Learn how to search text in DWG files using C# and Aspose.CAD for .NET.
    Extract text, read DWG files, and boost your CAD applications.
  name: Search text in DWG files with C# using Aspose.CAD
  steps:
  - name: install the Aspose.CAD NuGet package
    text: 'Open the NuGet Package Manager console and run: This adds the required
      assemblies and updates your project file.'
  - name: open the DWG file
    text: Create a `CadImage` instance by calling `Image.Load`. The method automatically
      detects the file format and prepares an in‑memory representation.
  - name: enumerate text fragments
    text: '`image.TextFragments` returns a collection of `TextFragment` objects, each
      exposing `Text`, `Location`, `Height`, and `LayerName`. You can iterate or LINQ‑filter
      this collection.'
  - name: apply your search criteria
    text: Use `String.Contains`, `Regex.IsMatch`, or any custom predicate to locate
      the exact text you need. For case‑insensitive searches, call `ToLowerInvariant()`
      on both sides.
  - name: handle the results
    text: Typical actions include logging the fragment’s coordinates, exporting to
      CSV, or highlighting the entity in a viewer. Because the API gives you the exact
      `Location`, you can feed it into any downstream CAD visualization component.
  type: HowTo
- questions:
  - answer: Yes. Provide the password via `CadLoadOptions.Password` when calling `Image.Load`.
    question: Can I search for text in password‑protected DWG files?
  - answer: Absolutely. Loop through a directory, load each file, and reuse the same
      LINQ filter – the library is thread‑safe for parallel processing.
    question: Does the API support searching across multiple DWG files at once?
  - answer: Aspose.CAD reports a **99 % success rate** on industry‑standard test sets,
      handling MTEXT, attribute definitions, and even embedded Unicode characters.
    question: How accurate is the text extraction for complex annotations?
  - answer: After obtaining the `Location` of each `TextFragment`, you can draw a
      temporary overlay using any CAD viewer that accepts geometry primitives.
    question: Is there a way to highlight found text in a viewer?
  - answer: The product uses a per‑developer or per‑server license model; a free evaluation
      license is available for 30 days.
    question: What licensing model applies to Aspose.CAD?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- CAD processing
- Aspose.CAD
- .NET
- DWG text search
title: Поиск текста в файлах DWG с помощью C# и Aspose.CAD
url: /ru/net/text-search-and-manipulation/
weight: 28
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Поиск текста в файлах DWG с помощью C# и Aspose.CAD

## Введение

В этом руководстве вы узнаете, как **search text in DWG** файлы с помощью C# используя мощную библиотеку Aspose.CAD для .NET. Независимо от того, нужно ли вам находить аннотации, извлекать значения атрибутов или создавать индекс для поиска, приведённые ниже шаги помогут вам реализовать надёжное, высокопроизводительное решение, работающее как на .NET Framework, так и на .NET Core.

## Краткие ответы

- **Какая библиотека обрабатывает поиск текста DWG?** Aspose.CAD for .NET.
- **Могу ли я извлечь текст из DWG?** Да — API возвращает строки plain‑text для любого найденного объекта.
- **Какие версии .NET поддерживаются?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.
- **Нужна ли лицензия для разработки?** Бесплатная временная лицензия подходит для оценки; полная лицензия требуется для продакшн.
- **Эффективна ли операция по использованию памяти?** Да, Aspose.CAD обрабатывает файлы потоково, позволяя работать с DWG, содержащими сотни страниц, без загрузки всего файла в RAM.

## Что такое поиск текста в DWG?

CadImage — объект Aspose.CAD, представляющий загруженный CAD‑чертёж, предоставляющий доступ к его сущностям, таким как фрагменты текста.  
TextFragment представляет отдельный фрагмент извлечённого текста, включая его содержимое и геометрическое расположение.

Фраза *search text in DWG* относится к программному поиску строковых данных — таких как имена слоёв, значения атрибутов или текст аннотаций — внутри файла чертежа DWG. Aspose.CAD предоставляет эту возможность через объект `CadImage` и коллекцию `TextFragment`, позволяя разработчикам эффективно извлекать и обрабатывать текст.

## Почему использовать Aspose.CAD для поиска текста в DWG?

Aspose.CAD поддерживает **30+ CAD и BIM форматов** (включая DWG, DXF, DGN, DWF) и может обрабатывать файлы размером до **500 MB** без полной загрузки в память. Библиотека гарантирует **99 % точность извлечения текста** на сложных чертежах, что является измеримым улучшением по сравнению со многими open‑source парсерами, которые часто пропускают встроенный MTEXT или атрибуты блоков.

## Как искать текст в файлах DWG с помощью C#?

Image.Load — статический метод, который читает CAD‑файл и возвращает экземпляр CadImage.  

Загрузите DWG с помощью `Image.Load`, получите коллекцию `TextFragments` и отфильтруйте её с помощью LINQ, используя ваш поисковый термин. Этот лаконичный шаблон работает за линейное время относительно количества текстовых сущностей, не требует дополнительных библиотек и стабильно работает как в .NET Framework, так и в .NET Core.

### Шаг 1: установить пакет Aspose.CAD NuGet

Откройте консоль менеджера пакетов NuGet и выполните:

```
Install-Package Aspose.CAD
```

### Шаг 2: открыть файл DWG

Создайте экземпляр `CadImage`, вызвав `Image.Load`. Метод автоматически определяет формат файла и подготавливает его представление в памяти.

### Шаг 3: перечислить фрагменты текста

`image.TextFragments` возвращает коллекцию объектов `TextFragment`, каждый из которых предоставляет `Text`, `Location`, `Height` и `LayerName`. Вы можете итерировать или отфильтровать эту коллекцию с помощью LINQ.

### Шаг 4: применить критерии поиска

Используйте `String.Contains`, `Regex.IsMatch` или любой пользовательский предикат для поиска точного текста. Для поиска без учёта регистра вызывайте `ToLowerInvariant()` для обеих сторон.

### Шаг 5: обработать результаты

Обычные действия включают запись координат фрагмента в журнал, экспорт в CSV или подсветку сущности в просмотрщике. Поскольку API предоставляет точный `Location`, вы можете передать его в любой последующий компонент визуализации CAD.

## Как извлечь текст из DWG?

TextFragment — объект, содержащий извлечённый текст и связанные метаданные, такие как позиция и слой.  

Извлечение текста идентично поиску; просто перечислите коллекцию `TextFragment` и прочитайте свойство `TextFragment.Text` у каждого элемента. Вы можете объединить строки в один документ, записать их в CSV‑файл или добавить в поисковый индекс для быстрого доступа к нескольким чертежам.

## Распространённые подводные камни и устранение неполадок

- **Missing MTEXT:** Некоторые более старые версии DWG хранят многострочный текст в атрибутах блоков. Убедитесь, что также проверяете `image.Blocks` на наличие объектов `Attribute`.
- **Encoding issues:** Файлы DWG могут использовать не‑Unicode кодовые страницы. Установите `image.LoadOptions.Encoding` в соответствующее `System.Text.Encoding` перед загрузкой.
- **Large files:** Для файлов размером более 200 MB включите `image.LoadOptions.Streaming = true`, чтобы удерживать использование памяти ниже 100 MB.

## Часто задаваемые вопросы

**Q: Могу ли я искать текст в защищённых паролем файлах DWG?**  
**A:** Да. Укажите пароль через `CadLoadOptions.Password` при вызове `Image.Load`.

**Q: Поддерживает ли API поиск по нескольким файлам DWG одновременно?**  
**A:** Абсолютно. Пройдитесь по каталогу, загрузите каждый файл и повторно используйте тот же LINQ‑фильтр — библиотека потокобезопасна для параллельной обработки.

**Q: Насколько точным является извлечение текста для сложных аннотаций?**  
**A:** Aspose.CAD сообщает **99 % успеха** на отраслевых тестовых наборах, обрабатывая MTEXT, определения атрибутов и даже встроенные Unicode‑символы.

**Q: Есть ли способ подсветить найденный текст в просмотрщике?**  
**A:** После получения `Location` каждого `TextFragment` вы можете нарисовать временную наложенную графику, используя любой CAD‑просмотрщик, принимающий геометрические примитивы.

**Q: Какая модель лицензирования применяется к Aspose.CAD?**  
**A:** Продукт использует модель лицензирования per‑developer или per‑server; бесплатная оценочная лицензия доступна на 30 дней.

---

**Последнее обновление:** 2026-10-04  
**Тестировано с:** Aspose.CAD 24.11 for .NET  
**Автор:** Aspose  

## Учебники по поиску и манипуляции текстом

### [Поиск текста в файлах DWG с C# - учебник Aspose.CAD](./searching-text-in-dwg-files/)

```csharp
using Aspose.CAD;
using Aspose.CAD.ImageOptions;

// Load the DWG file
using var image = (CadImage)Image.Load("sample.dwg");

// Retrieve all text fragments
var fragments = image.TextFragments;

// Filter fragments that contain the target string
var matches = fragments.Where(t => t.Text.Contains("TargetString"));
```

## Связанные учебники

- [Конвертировать DWG в PDF и добавить текст в C# – учебник Aspose.CAD](/cad/net/dwg-file-manipulation/adding-text-to-dwg/)
- [Как конвертировать DWG в PDF и растровые изображения с помощью Aspose.CAD для .NET](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [Как отрисовать CAD и конвертировать DWG – Aspose.CAD .NET](/cad/net/conversion-and-export/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}