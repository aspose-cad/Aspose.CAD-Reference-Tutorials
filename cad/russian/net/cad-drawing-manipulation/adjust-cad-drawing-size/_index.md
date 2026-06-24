---
date: 2026-03-19
description: Узнайте, как изменять размер CAD‑чертежей в .NET с помощью Aspose.CAD,
  включая масштабирование единиц CAD‑чертежа и настройку размеров макета. Следуйте
  нашему пошаговому руководству.
linktitle: Adjusting CAD Drawing Size
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Как изменить размер CAD‑чертежей с помощью Aspose.CAD для .NET
url: /ru/net/cad-drawing-manipulation/adjust-cad-drawing-size/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Как изменить размер CAD‑чертежей с помощью Aspose.CAD for .NET

## Введение

Если вам нужно **изменять размер CAD**‑файлов непосредственно из вашего .NET‑приложения, вы попали по адресу. В этом руководстве мы покажем, как изменить настройки единиц CAD, масштабировать размеры чертежа и программно регулировать размер CAD с помощью Aspose.CAD for .NET. К концу руководства у вас будет готовое, пригодное для продакшна решение для изменения размера любого поддерживаемого формата CAD.

## Быстрые ответы
- **Какая библиотека требуется?** Aspose.CAD for .NET  
- **Можно ли изменить тип единицы?** Да – задайте `UnitType` в `CadRasterizationOptions`  
- **Нужна ли лицензия для продакшна?** Для использования без ограничений требуется действующая лицензия Aspose.CAD  
- **В какой формат изображения экспортируется пример?** BMP (но подходит любой поддерживаемый растровый формат)  
- **Сколько строк кода?** Менее 30 строк для полной операции изменения размера  

## Что означает «how to resize CAD» на практике?
Изменение размера CAD‑чертежа означает преобразование векторных данных в растровое изображение с определённым масштабом или единицей измерения (например, сантиметры, дюймы). Это полезно, когда нужно вставлять чертежи в отчёты, генерировать миниатюры или интегрировать визуалы CAD в веб‑страницы.

## Почему стоит менять размер CAD с помощью Aspose.CAD?
- **Без внешних CAD‑программ** – всё работает внутри вашего .NET‑кода.  
- **Тонкая настройка** единиц, макетов и параметров растеризации.  
- **Поддержка множества форматов** – один и тот же код работает с DWG, DXF, DWF и другими.  

## Предварительные требования

Прежде чем приступить, убедитесь, что у вас есть:

- Библиотека Aspose.CAD for .NET: скачайте и установите её со [страницы загрузки Aspose.CAD for .NET](https://releases.aspose.com/cad/net/).  
- Пример CAD‑чертежа: файл, например `sample.dwg`, размещённый в каталоге `document` вашего проекта.  

## Импорт пространств имён

Сначала импортируйте пространства имён, которые дают доступ к классам Aspose.CAD.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Шаг 1: Загрузка CAD‑чертежа

Загрузите исходный файл в объект `Image`. Этот объект представляет CAD‑чертеж в памяти и будет основой для всех последующих операций.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "sample.dwg";

// Load a CAD drawing in an instance of Image
using (var image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // Your code here...
}
```

## Шаг 2: Создание BmpOptions (или другого растрового формата)

`BmpOptions` указывает Aspose.CAD, как рендерить векторные данные при сохранении в виде bitmap. При необходимости можно заменить его на `PngOptions`, `JpegOptions` и т.д., в зависимости от целевого формата.

```csharp
Aspose.CAD.ImageOptions.BmpOptions bmpOptions = new Aspose.CAD.ImageOptions.BmpOptions();
```

## Шаг 3: Настройка CadRasterizationOptions

`CadRasterizationOptions` содержит основные параметры масштабирования, преобразования единиц и выбора макета. Привязка его к свойству `VectorRasterizationOptions` объекта `BmpOptions` гарантирует, что растеризатор использует ваши настройки.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions cadRasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
bmpOptions.VectorRasterizationOptions = cadRasterizationOptions;
```

## Шаг 4: Установка UnitType (изменение единицы CAD)

Здесь мы меняем единицу CAD с значения по умолчанию на сантиметры. Именно здесь реализуется ключевое слово **change cad unit**, и оно напрямую влияет на окончательный размер изображения.

```csharp
cadRasterizationOptions.UnitType = Aspose.CAD.ImageOptions.UnitType.Centimeter;
```

## Шаг 5: Выбор макетов (установка CAD‑макетов)

Если ваш чертеж содержит несколько макетов (например, Model, Sheet1), укажите, какие из них нужно растеризовать. Выбор правильного макета важен, когда вы **set cad layouts** для получаемого результата.

```csharp
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## Шаг 6: Экспорт в BMP (изменение размера CAD‑чертежа)

Наконец, сохраните растеризованное изображение. Выходной файл будет отражать новый размер, единицу измерения и выбранный макет – тем самым завершая операцию **resize CAD drawing**.

```csharp
string outPath = sourceFilePath + ".bmp";
image.Save(outPath, bmpOptions);
```

Теперь у вас есть BMP‑файл, представляющий изменённый по размеру CAD‑чертеж, готовый к дальнейшей обработке или отображению.

## Распространённые проблемы и решения

| Проблема | Почему происходит | Решение |
|----------|-------------------|----------|
| Изображение размытое | По умолчанию низкое DPI (dots per inch) | Установите `cadRasterizationOptions.Resolution = 300;` перед сохранением |
| Выбран неправильный макет | Ошибка в названии макета | Проверьте точное имя макета в CAD‑просмотрщике или в коллекции `Layouts` |
| Преобразование единиц выглядит некорректно | Смешивание метрических и имперских единиц | Убедитесь, что `UnitType` соответствует желаемой системе измерения |

## Часто задаваемые вопросы

### Q1: Совместим ли Aspose.CAD for .NET со всеми форматами CAD?

A1: Aspose.CAD for .NET поддерживает широкий спектр форматов CAD, включая DWG, DXF, DWF и другие. Полный список см. в [документации](https://reference.aspose.com/cad/net/).

### Q2: Можно ли изменить размер нескольких макетов одновременно?

A2: Да, можно изменить размер нескольких макетов, настроив массив `Layouts` в `CadRasterizationOptions`.

### Q3: Где получить поддержку по Aspose.CAD for .NET?

A3: Посетите [форум Aspose.CAD](https://forum.aspose.com/c/cad/19) для получения помощи от сообщества.

### Q4: Есть ли бесплатная пробная версия?

A4: Да, вы можете попробовать [бесплатную trial‑версию](https://releases.aspose.com/) для оценки возможностей Aspose.CAD for .NET.

### Q5: Как получить временную лицензию для Aspose.CAD for .NET?

A5: Получить временную лицензию для тестирования можно [здесь](https://purchase.aspose.com/temporary-license/).

## Часто задаваемые вопросы (повтор)

**В: Как масштабировать CAD‑чертеж без изменения типа единицы?**  
О: Отрегулируйте свойство `Zoom` у `CadRasterizationOptions` (например, `cadRasterizationOptions.Zoom = 2.0;`), чтобы удвоить размер, сохранив исходную единицу измерения.

**В: Можно ли экспортировать в другие форматы, кроме BMP?**  
О: Конечно. Замените `BmpOptions` на `PngOptions`, `JpegOptions` или любой другой поддерживаемый класс растрового формата.

**В: Можно ли пакетно обрабатывать папку чертежей?**  
О: Да. Пройдитесь циклом по файлам в каталоге, примените ту же логику растеризации и сохраните каждый результат под уникальным именем.

---

**Последнее обновление:** 2026-03-19  
**Тестировано с:** Aspose.CAD for .NET 24.11 (на момент написания)  
**Автор:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}