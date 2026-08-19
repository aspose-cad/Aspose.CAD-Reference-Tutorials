---
date: 2026-03-21
description: Узнайте, как создать PDF из DWG и экспортировать DGN в составе DWG с
  помощью Aspose.CAD для .NET. Это руководство также показывает, как преобразовать
  DWG в PDF и настроить параметры PDF.
linktitle: Export DGN as Part of DWG
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Создание PDF из DWG и экспорт DGN как части DWG – Aspose.CAD для .NET
url: /ru/net/cad-export-formats/export-dgn-as-part-of-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Создание PDF из DWG и экспорт DGN как части DWG – Aspose.CAD для .NET

## Введение

Если вам нужно **создать PDF из** файлов DWG, одновременно внедрив дизайн DGN как часть DWG, Aspose.CAD для .NET делает это простым. В этом руководстве мы пройдем весь рабочий процесс: загрузка DWG, поиск встроенного DGN‑подложки, настройка параметров растеризации и, наконец, экспорт результата в документ PDF. Независимо от того, создаёте ли вы пакетный инструмент конвертации, движок отчётности или сервис интеграции CAD‑BIM, приведённые ниже шаги дадут вам надёжную, готовую к продакшну основу.

## Быстрые ответы
- **Какая библиотека обрабатывает конвертацию DWG → PDF?** Aspose.CAD для .NET  
- **Можно ли экспортировать DGN‑подложку при создании PDF?** Да – подложка доступна через `CadDgnUnderlay`.  
- **Какой метод задаёт параметры PDF?** `PdfOptions` совместно с `CadRasterizationOptions`.  
- **Нужна ли лицензия для коммерческого использования?** Да, требуется действующая лицензия Aspose.CAD.  
- **Поддерживаемые версии .NET?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## Что означает «создание PDF из DWG»?

Создание PDF из файла DWG подразумевает рендеринг векторного чертежа в растровый или векторный PDF‑документ. Этот процесс полезен для обмена чертежами с заинтересованными сторонами, у которых нет CAD‑программ, для архивирования или генерации печатных отчётов. Aspose.CAD упрощает задачу, беря на себя парсинг сущностей DWG и предоставляя тонкую настройку вывода через `PdfOptions`.

## Почему экспортировать DGN как часть DWG?

Подложка DGN часто представляет справочную геометрию из проектов MicroStation. Экспортируя DGN вместе с DWG, вы сохраняете исходный контекст дизайна, обеспечивая полное отображение набора чертежей для downstream‑пользователей. Это особенно ценно в многодисциплинарных проектах, где одновременно используются файлы DWG и DGN.

## Предварительные требования

- **Aspose.CAD для .NET** – скачайте его [здесь](https://releases.aspose.com/cad/net/).  
- **Среда разработки** – Visual Studio (любая современная версия) или ваш предпочтительный .NET IDE.  
- **Базовые знания C#** – вы должны быть уверены в синтаксисе C# и структуре .NET‑проекта.

## Импорт пространств имён

Добавьте необходимые директивы `using` в начало вашего C#‑файла:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Пошаговое руководство

### Шаг 1: Определите пути к файлам

Укажите входной файл DWG и имя выходного PDF.

```csharp
// Input and Output file paths
string fileName = "BlockRefDgn.dwg";
string outPath = fileName + ".pdf";
```

### Шаг 2: Создайте экземпляр `PdfOptions` (задать параметры PDF)

`PdfOptions` позволяет управлять тем, как генерируется PDF, включая размер страницы, сжатие и метаданные.

```csharp
// Create an instance of PdfOptions class for exporting DWG to PDF
PdfOptions exportOptions = new PdfOptions();
```

### Шаг 3: Загрузите файл DWG

Загрузите DWG как `CadImage`, чтобы иметь возможность исследовать его сущности.

```csharp
// Load the existing DWG file as an image and convert it to CadImage type
using (CadImage cadImage = (CadImage)Image.Load(fileName))
```

### Шаг 4: Переберите сущности

Пройдитесь по каждой сущности чертежа, чтобы найти DGN‑подложку.

```csharp
// Iterate through each entity inside the DWG file
foreach (CadBaseEntity baseEntity in cadImage.Entities)
```

### Шаг 5: Проверьте тип сущности (как экспортировать dgn)

Определите, является ли текущая сущность DGN‑подложкой.

```csharp
// Check if the entity is an image definition
if (baseEntity.TypeName == CadEntityTypeName.DGNUNDERLAY)
```

### Шаг 6: Получите путь к подложке

Извлеките путь внешней ссылки на файл DGN.

```csharp
// If it's an image definition, get the external reference to the object
CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
Console.WriteLine(dgnFile.UnderlayPath);
```

### Шаг 7: Задайте параметры растеризации (конвертировать dwg в pdf)

Настройте, как DWG будет растеризован перед помещением в PDF.

```csharp
// Define settings for CadRasterizationOptions object
exportOptions.VectorRasterizationOptions = new CadRasterizationOptions()
{
    PageWidth = 1600,
    PageHeight = 1600,
    Layouts = new string[] { "Model" },
    AutomaticLayoutsScaling = false,
    NoScaling = true,
    BackgroundColor = Color.Black,
    DrawType = CadDrawTypeMode.UseObjectColor
};
```

### Шаг 8: Экспортируйте DWG в PDF

Наконец, сохраните отрендеренное изображение как PDF‑файл.

```csharp
// Export the DWG to PDF by calling Save method
cadImage.Save(outPath, exportOptions);
```

## Распространённые проблемы и решения

| Проблема | Причина | Решение |
|----------|---------|----------|
| **`Image.Load` бросает “File not found”** | Неправильный путь или отсутствующий файл. | Используйте абсолютный путь или убедитесь, что DWG скопирован в папку вывода. |
| **Путь к подложке пустой** | DGN‑подложка не встроена или ссылка повреждена. | Проверьте, что DWG действительно содержит DGN‑подложку и что внешний файл DGN доступен. |
| **PDF‑вывод пустой** | Параметры растеризации заданы с нулевыми размерами. | Скорректируйте `PageWidth`/`PageHeight` или установите `NoScaling = false`. |
| **Исключение лицензии** | Запуск без действующей лицензии Aspose.CAD. | Примените лицензию перед загрузкой изображения: `License lic = new License(); lic.SetLicense("Aspose.CAD.lic");` |

## Часто задаваемые вопросы

### В1: Можно ли использовать Aspose.CAD для .NET в коммерческих проектах?
ОТВ: Да, можно. Посетите [здесь](https://purchase.aspose.com/buy) для ознакомления с вариантами лицензирования.

### В2: Есть ли ограничения по размеру файлов DWG, которые можно обрабатывать?
ОТВ: Aspose.CAD поддерживает работу с большими DWG‑файлами, однако могут действовать ограничения аппаратного обеспечения.

### В3: Доступна ли пробная версия?
ОТВ: Да, бесплатную пробную версию можно получить [здесь](https://releases.aspose.com/).

### В4: Как получить временные лицензии?
ОТВ: Временные лицензии можно получить [здесь](https://purchase.aspose.com/temporary-license/).

### В5: Где можно получить помощь, если возникнут проблемы?
ОТВ: Обратитесь к форуму Aspose.CAD [здесь](https://forum.aspose.com/c/cad/19) для поддержки.

**В: Как задать дополнительные метаданные PDF (author, title и т.д.)?**  
О: Используйте свойства `exportOptions.Metadata` перед вызовом `Save`.

**В: Можно ли экспортировать несколько макетов в отдельные страницы PDF?**  
О: Да – задайте `Layouts = new string[] { "Layout1", "Layout2" }` в `CadRasterizationOptions`.

**В: Поддерживает ли Aspose.CAD конвертацию DWG в другие форматы изображений?**  
О: Абсолютно. Вы можете экспортировать в PNG, JPEG, SVG и другие, используя соответствующие перегрузки `Image.Save`.

---

**Последнее обновление:** 2026-03-21  
**Тестировано с:** Aspose.CAD 24.11 для .NET  
**Автор:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}