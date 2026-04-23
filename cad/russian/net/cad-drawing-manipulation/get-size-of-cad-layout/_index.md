---
date: 2026-03-21
description: Узнайте, как получить размер макета CAD в .NET с помощью Aspose.CAD.
  Следуйте нашему пошаговому руководству для эффективной работы с CAD‑файлами.
linktitle: Get Size of CAD Layout
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Получить размер макета CAD в Aspose.CAD для .NET
url: /ru/net/cad-drawing-manipulation/get-size-of-cad-layout/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Получить размер макета CAD в Aspose.CAD для .NET

## Introduction

В этом всестороннем руководстве вы узнаете, **как получить размер макета CAD** с помощью библиотеки Aspose.CAD для .NET. Независимо от того, создаёте ли вы просмотрщик CAD, генерируете миниатюры или вам нужны точные размеры макета для последующей обработки, знание точного размера каждого макета имеет решающее значение. Мы пройдём весь процесс — от загрузки чертежа до извлечения размеров макета и, при желании, сохранения их в виде изображений — чтобы вы могли уверенно интегрировать эту возможность в свои приложения.

## Quick Answers
- **Что означает “получить размер макета CAD”?** Это означает получение ширины и высоты (в единицах чертежа) каждого непустого макета в файле CAD.  
- **Какая библиотека поддерживает это?** Aspose.CAD for .NET предоставляет простой API для доступа к информации о макетах.  
- **Нужна ли лицензия?** Бесплатная пробная версия подходит для оценки; коммерческая лицензия требуется для использования в продакшене.  
- **Поддерживаемые форматы?** DWG, DXF и многие другие форматы CAD/BIM полностью поддерживаются.  
- **Типичное время реализации?** Около 10‑15 минут для базовой процедуры получения размеров.

## What is “get CAD layout size”?
Получение размера макета CAD означает извлечение геометрических границ каждого макета (бумажного пространства), определённого в чертеже CAD. Эти границы выражаются в родных единицах чертежа (обычно миллиметры или дюймы) и полезны для таких задач, как масштабирование, печать или создание превью‑изображений.

## Why retrieve CAD layout size with Aspose.CAD?
- **Не требуется программное обеспечение CAD** – Работает полностью на стороне сервера.  
- **Кроссплатформенный** – Работает с .NET Framework, .NET Core и .NET 5/6+.  
- **Точные измерения** – Возвращает точные границы, как они хранятся в файле, избегая ручного парсинга.  
- **Лёгкая интеграция** – Простые вызовы API естественно вписываются в существующие проекты C#.

## Prerequisites

Прежде чем перейти к коду, убедитесь, что у вас есть следующее:

- Aspose.CAD for .NET установлен. Вы можете скачать его со [страницы загрузки Aspose.CAD for .NET](https://releases.aspose.com/cad/net/).
- Один или несколько файлов CAD (DWG, DXF и т.д.), которые вы хотите проанализировать. В этом руководстве используются `conic_pyramid.dxf` и `Bottom_plate.dwg` в качестве примеров.

## Import Namespaces

В вашем .NET‑проекте начните с импорта необходимых пространств имён:

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.ImageOptions;
```

## Step 1: Set Up the Document Directory

### Шаг 1: Настройте каталог документов

Укажите папку, содержащую ваши файлы CAD. Замените заполнитель реальным путём на вашем компьютере.

```csharp
string MyDir = "Your Document Directory";
```

## Step 2: Specify CAD File Paths

### Шаг 2: Укажите пути к файлам CAD

Создайте массив, указывающий на каждый файл CAD, который вы хотите обработать.

```csharp
string[] sourceFilePaths = new[]
{
    MyDir + "conic_pyramid.dxf",
    MyDir + "Bottom_plate.dwg"
};
```

## Step 3: Iterate Through CAD Files

### Шаг 3: Переберите файлы CAD

Загрузите каждый файл, определите его формат и подготовьте извлечение информации о макетах.

```csharp
foreach (var sourceFilePath in sourceFilePaths)
{
    string extension = Path.GetExtension(sourceFilePath);
    using (CadImage cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath))
    {
        // ... (continue to the next step)
    }
}
```

## Step 4: Get Non‑Empty Layouts

### Шаг 4: Получите непустые макеты

Нужен вспомогательный метод, который возвращает только те макеты, которые действительно содержат элементы чертежа. Пустые макеты игнорируются, так как у них нет размеров для отчёта.

```csharp
private static List<string> GetNotEmptyLayouts(Image cadImage, string extension)
{
    // ... (continue to the next step)
}
```

## Step 5: Get Layouts for DWG Files

### Шаг 5: Получите макеты для файлов DWG

Файлы DWG хранят информацию о макетах в таблице `HeaderVariables`. Следующий метод извлекает имена всех непустых макетов для чертежа DWG.

```csharp
private static List<string> GetNotEmptyLayoutsForDwg(CadImage cadImage)
{
    // ... (continue to the next step)
}
```

## Step 6: Get Layouts for DXF Files

### Шаг 6: Получите макеты для файлов DXF

Файлы DXF используют другую структуру. Этот метод парсит коллекцию `Tables`, чтобы найти макеты бумажного пространства, содержащие сущности.

```csharp
private static List<string> GetNotEmptyLayoutsForDxf(CadImage cadImage)
{
    // ... (continue to the next step)
}
```

## Step 7: Retrieve Layout Size and Save as Image

### Шаг 7: Получите размер макета и сохраните как изображение

Наконец, пройдитесь по каждому найденному макету, прочитайте его границы и при желании отрендерите макет в файл изображения для визуальной проверки.

```csharp
foreach (string layout in layouts)
{
    // ... (continue to the next step)
}
```

## Common Issues & Tips

## Общие проблемы и советы

- **Отсутствуют имена макетов:** Убедитесь, что файл CAD действительно содержит макеты бумажного пространства; в некоторых файлах есть только модельное пространство.  
- **Неправильные единицы:** Размер возвращается в родных единицах чертежа. При необходимости преобразуйте в миллиметры или дюймы.  
- **Производительность:** Загрузка очень больших файлов DWG/DXF может требовать много памяти; рассмотрите возможность асинхронной обработки файлов или их пакетирования.

## Frequently Asked Questions

## Часто задаваемые вопросы

**Q: Совместим ли Aspose.CAD со всеми форматами файлов CAD?**  
A: Да, Aspose.CAD поддерживает широкий спектр форматов, включая DWG, DXF, DGN и многие типы BIM‑файлов.

**Q: Могу ли я настроить параметры сохранения изображения?**  
A: Конечно! Вы можете изменить `CadRasterizationOptions` (формат, разрешение, цвет фона и т.д.), чтобы удовлетворить ваши конкретные требования.

**Q: Где я могу найти дополнительную документацию?**  
A: Обратитесь к [документации Aspose.CAD](https://reference.aspose.com/cad/net/) для подробных справок по API и дополнительных примеров.

**Q: Доступна ли бесплатная пробная версия?**  
A: Да, вы можете ознакомиться с Aspose.CAD с помощью [бесплатной пробной версии](https://releases.aspose.com/).

**Q: Как я могу получить техническую поддержку?**  
A: Для технической поддержки посетите [форум Aspose.CAD](https://forum.aspose.com/c/cad/19).

---

**Последнее обновление:** 2026-03-21  
**Тестировано с:** Aspose.CAD 24.11 for .NET  
**Автор:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}