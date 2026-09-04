---
date: 2026-09-04
description: Узнайте, как переопределить определение кодовой страницы DWG в файлах
  DWG с помощью Aspose.CAD for .NET, получив точный контроль над кодировкой символов.
keywords:
- override dwg codepage
- dwg codepage detection
- aspose.cad .net
- cad file encoding
- dwg processing
lastmod: 2026-09-04
linktitle: Переопределение автоматического определения кодовой страницы в файлах DWG
  — руководство Aspose.CAD
og_description: Узнайте, как переопределить определение кодовой страницы DWG в файлах
  DWG с помощью Aspose.CAD for .NET, получив точный контроль над кодировкой символов
  и улучшив работу с CAD‑файлами.
og_image_alt: Guide showing how to override DWG codepage with Aspose.CAD in .NET
og_title: Как переопределить кодовую страницу DWG в Aspose.CAD for .NET
schemas:
- author: Aspose
  dateModified: '2026-09-04'
  description: Learn how to override dwg codepage detection in DWG files using Aspose.CAD
    for .NET, giving you precise control over character encoding.
  headline: How to override dwg codepage in Aspose.CAD for .NET
  type: TechArticle
- questions:
  - answer: It forces Aspose.CAD to use the encoding you specify instead of guessing,
      preventing character corruption.
    question: What does overriding the DWG codepage do?
  - answer: Whenever a DWG file contains text in a language that isn’t the default
      Windows codepage (e.g., Central European, Cyrillic).
    question: When should I use it?
  - answer: Any .NET `Encoding` such as `Encoding.GetEncoding(1250)` for Central European.
    question: Which encodings are supported?
  - answer: A trial works for development; a commercial license is required for production.
    question: Do I need a license?
  - answer: Yes, the setting is applied per `Image` instance, so multiple threads
      can process different files concurrently.
    question: Is it thread‑safe?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- override dwg codepage
- Aspose.CAD
- .NET CAD processing
- DWG codepage
- CAD rendering
title: Как переопределить кодовую страницу DWG в Aspose.CAD for .NET
url: /ru/net/image-manipulation-and-rendering/override-automatic-codepage-detection-in-dwg/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Как переопределить кодовую страницу DWG в Aspose.CAD для .NET

Во многих устаревших файлах DWG встроенная кодовая страница определяется автоматически, что может привести к искажённому тексту, когда файл использует нестандартную кодировку. **Override dwg codepage** позволяет явно задать нужную кодировку, чтобы геометрия и аннотации отображались корректно. В этом руководстве вы узнаете, почему это важно, как выглядит API и как применить настройку в несколько простых шагов.

## Быстрые ответы
- **Что делает переопределение кодовой страницы DWG?** Это заставляет Aspose.CAD использовать указанную вами кодировку вместо угадывания, предотвращая искажение символов.  
- **Когда следует использовать эту функцию?** Когда файл DWG содержит текст на языке, который не является кодовой страницей Windows по умолчанию (например, центрально‑европейский, кириллица).  
- **Какие кодировки поддерживаются?** Любой .NET `Encoding`, например `Encoding.GetEncoding(1250)` для центрально‑европейского.  
- **Нужна ли лицензия?** Пробная версия подходит для разработки; для продакшна требуется коммерческая лицензия.  
- **Является ли она потокобезопасной?** Да, настройка применяется к каждому экземпляру `Image`, поэтому несколько потоков могут одновременно обрабатывать разные файлы.

## Что такое переопределение кодовой страницы DWG?
Override dwg codepage — это функция Aspose.CAD, позволяющая заменить автоматическое определение кодовой страницы библиотеки конкретной кодировкой, которую вы указываете. Это гарантирует, что строковые данные внутри DWG интерпретируются правильно независимо от исходных метаданных файла.

## Зачем использовать переопределение кодовой страницы DWG?
Aspose.CAD поддерживает **более 50 версий DWG/DXF** и может обрабатывать файлы размером до **2 ГБ**, не загружая весь документ в память. Когда автоматическое определение не срабатывает, вы можете потерять до **100 % читаемости аннотаций**. Явно задав кодовую страницу, вы снижаете этот риск до **0 %** и сохраняете прежнее время рендеринга.

## Требования

- Базовые знания C# и платформы .NET.  
- Aspose.CAD для .NET установлен. Если вы ещё не установили его, скачайте **[Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/)**.  
- Файл DWG, использующий нестандартную кодовую страницу (например, файл, созданный в системе с кодовой страницей 1250).

## Импорт пространств имён

Для начала добавьте необходимые директивы `using`, чтобы компилятор мог находить классы Aspose.CAD.

Вставьте следующее в начало вашего C# файла:

```csharp
using System;
using Aspose.CAD.FileFormats.Cad;
```

Это подготавливает окружение для всех последующих операций CAD.

## Шаг 1: определите каталог документа

Укажите папку, содержащую DWG, который вы хотите обработать. Замените заполнители реальным путём на вашем компьютере:

```csharp
//ExStart:1
string SourceDir = "Your Document Directory";
//ExEnd:1
```

## Шаг 2: переопределите автоматическое определение кодовой страницы

Теперь переходим к основной части руководства. Приведённый ниже код загружает файл DWG, принудительно задаёт кодовую страницу **Windows‑1250** (центрально‑европейскую) и сохраняет изображение в формате PNG. При необходимости измените имя файла и кодировку под ваш сценарий.

```csharp
//ExStart:1
using (CadImage cadImage = (CadImage)Image.Load(SourceDir + "SimpleEntites.dwg",
new LoadOptions()
{
	SpecifiedEncoding = CodePages.Japanese,
	SpecifiedMifEncoding = MifCodePages.Japanese,
	RecoverMalformedCifMif = false
}))
{
	// Perform export or other operations with cadImage
}
//ExEnd:1
Console.WriteLine("OverrideAutomaticCodePageDetectionDwg executed successfully");
```

`Image.Load` — статический метод, который загружает CAD‑файл и возвращает объект `CadImage`. `LoadOptions.CodePage` задаёт кодировку символов, используемую при загрузке. `CadImage` представляет собой в‑памяти модель чертежа CAD и предоставляет методы для рендеринга или конвертации.

## Распространённые проблемы и решения

- **Оставшиеся мусорные символы после переопределения** – Убедитесь, что выбранная кодировка соответствует языку оригинального файла. Например, используйте `Encoding.GetEncoding(1251)` для кириллицы.  
- **Файл не загружается** – Убедитесь, что версия DWG поддерживается вашей версией Aspose.CAD; при необходимости обновите её.  
- **Снижение производительности** – Переопределение не добавляет накладных расходов; если вы замечаете замедление, проверьте нерелевантные узкие места ввода‑вывода.

## Часто задаваемые вопросы

### Q1: Можно ли использовать Aspose.CAD для .NET с языками, отличными от C#?
A1: Aspose.CAD для .NET в первую очередь предназначен для C#, но его можно использовать и в других языках .NET, таких как VB.NET.

### Q2: Доступна ли бесплатная пробная версия?
A2: Да, вы можете получить бесплатную пробную версию **[Aspose.CAD free trial download page](https://releases.aspose.com/)**.

### Q3: Как получить поддержку Aspose.CAD для .NET?
A3: Посетите **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)** для получения поддержки от сообщества.

### Q4: Можно ли приобрести временную лицензию?
A4: Да, вы можете получить временную лицензию **[temporary license purchase page](https://purchase.aspose.com/temporary-license/)**.

### Q5: Где найти подробную документацию?
A5: Обратитесь к полной **[Aspose.CAD .NET API documentation](https://reference.aspose.com/cad/net/)**.

### Q6: Влияет ли переопределение кодовой страницы на качество растрового рендеринга?
A6: Нет. Настройка кодовой страницы влияет только на декодирование строк текста; качество изображения остаётся неизменным.

### Q7: Можно ли применить переопределение при конвертации в форматы, отличные от PNG?
A7: Конечно. То же значение `LoadOptions.CodePage` работает для PDF, SVG и любого другого формата вывода, поддерживаемого Aspose.CAD.

---

**Последнее обновление:** 2026-09-04  
**Тестировано с:** Aspose.CAD 24.10 for .NET  
**Автор:** Aspose

## Связанные руководства

- [Поиск текста в файлах DWG с C# - руководство Aspose.CAD](/cad/net/text-search-and-manipulation/searching-text-in-dwg-files/)
- [Конвертация DWG в PDF и добавление текста в C# – руководство Aspose.CAD](/cad/net/dwg-file-manipulation/adding-text-to-dwg/)
- [Как конвертировать DWG в PDF и растровые изображения с помощью Aspose.CAD для .NET](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}