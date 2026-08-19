---
date: 2026-03-16
description: Узнайте, как конвертировать DWG в PDF или растровые изображения с помощью
  Aspose.CAD для .NET. Этот пошаговый учебник по преобразованию CAD в PDF охватывает
  экспорт DWG в форматы изображений, такие как PNG, и показывает, как эффективно экспортировать
  DWG в файлы изображений.
linktitle: Exporting DWG to PDF or Raster Images
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Как конвертировать DWG в PDF и растровые изображения с помощью Aspose.CAD для
  .NET
url: /ru/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Экспорт DWG в PDF или растровые изображения — руководство Aspose.CAD

## Введение

Если вам необходимо **конвертировать DWG в PDF** (или в растровые форматы, такие как PNG) напрямую из .NET‑приложения, вы попали по адресу. В этом руководстве мы пошагово рассмотрим, как использовать Aspose.CAD для .NET для выполнения конвертации, объясним, почему эта библиотека является надёжным выбором, и покажем, как обрабатывать как PDF, так и вывод изображений всего несколькими строками кода.

## Быстрые ответы
- **Какая библиотека обрабатывает конвертацию DWG?** Aspose.CAD for .NET  
- **Могу ли я экспортировать DWG в PNG, а также в PDF?** Да — те же параметры растеризации работают для обоих форматов.  
- **Нужна ли лицензия для разработки?** Бесплатная пробная версия подходит для тестирования; коммерческая лицензия требуется для продакшна.  
- **Какие версии .NET поддерживаются?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Обрабатывается ли конвертация единиц автоматически?** Вы можете задать систему единиц вручную (метрическую или имперскую), как показано в коде.

## Что такое «конвертация DWG в PDF»?
Конвертация DWG в PDF означает преобразование CAD‑чертежа (DWG) в портативный документ только для просмотра (PDF). Это удобно для обмена проектами с заинтересованными сторонами, у которых нет CAD‑программ, создания печатной документации или архивирования чертежей в универсальном читаемом формате.

## Почему использовать Aspose.CAD для этой конвертации?
- **Без внешних зависимостей** — библиотека полностью работает в управляемом коде.  
- **Высокая точность** — сохраняет слои, толщины линий и информацию о раскладке.  
- **Встроенные параметры растра** — позволяют экспортировать в PNG, JPEG, BMP и др. с помощью одного объекта конфигурации.  
- **Кроссплатформенный** — работает на Windows, Linux и macOS с .NET Core.

## Требования

Перед тем как приступить к руководству, убедитесь, что у вас есть:

- Базовое понимание программирования на .NET.  
- Установлена библиотека Aspose.CAD for .NET. Если нет, скачайте её [здесь](https://releases.aspose.com/cad/net/).  
- Ваш любимый интегрированный набор разработки (IDE), настроенный для разработки на .NET.

## Импорт пространств имён

Начнём с импорта необходимых пространств имён в ваш проект .NET. Это обеспечивает доступ к функционалу Aspose.CAD в вашем коде.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
```

## Шаг 1: Загрузка файла DWG

Начните с загрузки DWG‑файла, который нужно конвертировать. Замените `"Your Document Directory"` на путь к вашему DWG‑файлу.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for loading DWG goes here
}
```

## Шаг 2: Настройка экспорта PDF (Как экспортировать DWG в PDF)

Теперь настроим параметры экспорта PDF. Этот пример демонстрирует, как задать раскладку и обработать конвертацию единиц.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };

// Check and define the unit system
bool currentUnitIsMetric = false;
double currentUnitCoefficient = 1.0;
DefineUnitSystem(cadImage.UnitType, out currentUnitIsMetric, out currentUnitCoefficient);

// Your code for setting up PDF export goes here
```

## Шаг 3: Экспорт в PDF

Выполните экспорт в PDF, используя настроенные параметры.

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath, pdfOptions);
```

## Шаг 4: Экспорт в растровые изображения (экспорт dwg в изображение)

Расширьте функциональность, чтобы экспортировать в растровые изображения, например PNG.

```csharp
// A4 size at 300 DPI - 2480 x 3508
rasterizationOptions.PageHeight = 3508;
rasterizationOptions.PageWidth = 2480;

PngOptions pngOptions = new PngOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath.Replace("pdf", "png"), pngOptions);
```

## Распространённые проблемы и решения

| Проблема | Почему происходит | Как исправить |
|----------|-------------------|---------------|
| **Пустые страницы в PDF** | Макет указан неправильно | Убедитесь, что `rasterizationOptions.Layouts` содержит правильное имя макета (например, `"Model"`). |
| **Неправильные размеры** | Несоответствие DPI или размера страницы | Отрегулируйте `PageHeight`, `PageWidth` и значения DPI в `CadRasterizationOptions`. |
| **Неправильные единицы** | Конвертация единиц не определена | Используйте `DefineUnitSystem`, чтобы задать `currentUnitIsMetric` и `currentUnitCoefficient` на основе `cadImage.UnitType`. |
| **Исключение лицензии** | Ограничения пробной версии | Примените временную или постоянную лицензию перед вызовом `Image.Load`. |

## Часто задаваемые вопросы

### Q1: Могу ли я использовать Aspose.CAD для .NET в своих коммерческих проектах?
A1: Да, можете. Посетите [purchase.aspose.com/buy](https://purchase.aspose.com/buy) для деталей лицензирования.

### Q2: Доступна ли бесплатная пробная версия?
A2: Конечно! Получите бесплатную пробную версию [здесь](https://releases.aspose.com/).

### Q3: Как я могу получить поддержку Aspose.CAD для .NET?
A3: Перейдите на [форум Aspose.CAD](https://forum.aspose.com/c/cad/19) для поддержки сообщества.

### Q4: Можно ли получить временную лицензию для тестирования?
A4: Да, вы можете получить временную лицензию [здесь](https://purchase.aspose.com/temporary-license/).

### Q5: Где я могу найти подробную документацию?
A5: Документация доступна на [Aspose.CAD](https://reference.aspose.com/cad/net/).

### Q6: Как **сохранить CAD как PNG** с высоким качеством?
A6: Установите `PageHeight` и `PageWidth` в требуемые пиксельные размеры и выберите DPI 300 или выше в `CadRasterizationOptions`.

### Q7: Какой лучший способ **конвертировать dwg**, когда исходный файл содержит несколько макетов?
A7: Заполните `rasterizationOptions.Layouts` всеми именами макетов, которые нужно экспортировать, затем пройдитесь по каждому макету и вызовите `Save` для каждого формата вывода.

---

**Последнее обновление:** 2026-03-16  
**Тестировано с:** Aspose.CAD 24.11 for .NET  
**Автор:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}