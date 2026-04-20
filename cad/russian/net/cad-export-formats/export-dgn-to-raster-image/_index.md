---
date: 2026-03-24
description: Узнайте, как конвертировать dgn в png и сохранять CAD в jpeg с помощью
  Aspose.CAD для .NET — быстрый гид по преобразованию CAD в изображение.
linktitle: Export DGN to Raster Image
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Как конвертировать DGN в PNG в Aspose.CAD для .NET
url: /ru/net/cad-export-formats/export-dgn-to-raster-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Конвертация DGN в PNG с помощью Aspose.CAD для .NET

В современном .NET‑разработке **convert dgn to png** является распространённой задачей, когда нужно отображать CAD‑чертежи в вебе или встраивать их в отчёты. Aspose.CAD для .NET упрощает эту конверсию, позволяя превратить файл DGN в высококачественное растровое изображение всего несколькими строками кода. В этом руководстве мы пройдём весь процесс — от настройки проекта до сохранения окончательного PNG (или JPEG) файла.

## Быстрые ответы
- **Можно ли конвертировать DGN в PNG с помощью Aspose.CAD?** Да — достаточно настроить параметры растеризации и выбрать вывод в PNG или JPEG.  
- **Нужна ли лицензия для продакшн‑использования?** Для развертываний, не являющихся пробными, требуется действующая лицензия Aspose.CAD.  
- **Какие версии .NET поддерживаются?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7.  
- **Какие форматы изображений доступны?** PNG, JPEG, BMP, GIF, TIFF и другие.  
- **Нужна ли обработка исключений?** Обязательно — оберните конверсию в try/catch, чтобы обработать проблемы доступа к файлам.

## Что такое «convert dgn to png»?
Конвертация файла DGN (MicroStation) в PNG означает растеризацию векторных CAD‑данных в пиксельное изображение. Это полезно для создания превью, встраивания чертежей в HTML‑письма или генерации миниатюр для систем управления документами.

## Почему стоит использовать Aspose.CAD для конвертации CAD в изображение?
- **Без внешних зависимостей** — работает полностью в управляемом коде.  
- **Высокая точность** — сохраняет толщины линий, слои и цвета.  
- **Гибкий вывод** — переключайтесь между PNG, JPEG, BMP и др., изменяя одну опцию.  
- **Оптимизированная производительность** — растеризация быстрая даже для больших чертежей.

## Предварительные требования

Прежде чем начать, убедитесь, что у вас есть:

- **Aspose.CAD для .NET**, установленный в вашем проекте. Скачать можно с [website](https://reference.aspose.com/cad/net/).  
- Пример файла DGN (например, `Nikon_D90_Camera.dgn`) в известной директории.

## Импорт пространств имён

Добавьте необходимые `using`‑директивы, чтобы получить доступ к классам Aspose.CAD.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Шаг 1: Загрузка файла DGN

Загрузите исходный DGN в объект `CadImage`. Этот объект представляет CAD‑чертёж в памяти и будет источником для растеризации.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for further processing goes here
}
```

## Шаг 2: Определение параметров растеризации

Настройте, как CAD‑чертёж должен быть растеризован. Здесь можно задать размер изображения, масштаб и цвет фона.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## Шаг 3: Выбор формата вывода (PNG или JPEG)

Хотя в руководстве основной упор делается на PNG, вы также можете **save cad as jpeg**. Создайте соответствующий объект параметров изображения и привяжите к нему настройки растеризации.

```csharp
ImageOptionsBase options = new JpegOptions();   // Change to PngOptions() for PNG output
options.VectorRasterizationOptions = rasterizationOptions;
```

> **Pro tip:** Чтобы создать PNG‑файл, замените `new JpegOptions()` на `new PngOptions()`.

## Шаг 4: Сохранение растрового изображения

Наконец, вызовите `Save` у экземпляра `CadImage`, указав желаемое имя файла и объект параметров, который вы сконфигурировали.

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpg", options);
```

Если вы переключились на `PngOptions`, файл будет сохранён как `ExportDGNToRasterImage_out.png`.

## Распространённые проблемы и решения

| Issue | Cause | Fix |
|-------|-------|-----|
| **Blank output image** | `NoScaling` установлен неправильно или не выбран макет | Установите `AutomaticLayoutsScaling = true` или укажите нужный макет. |
| **Out‑of‑memory for large files** | Загрузка огромного DGN без потоковой передачи | Используйте `Image.Load(sourceFilePath, new LoadOptions { LoadOnDemand = true })`. |
| **Unsupported DGN version** | Старые версии MicroStation | Убедитесь, что используете последнюю версию Aspose.CAD, поддерживающую устаревшие форматы. |

## Часто задаваемые вопросы

**Q: Можно ли экспортировать DGN‑файлы в форматы, отличные от JPEG?**  
A: Да, Aspose.CAD для .NET поддерживает PNG, BMP, GIF, TIFF и другие — просто замените класс параметров (например, `new PngOptions()`).

**Q: Как правильно обрабатывать исключения во время конвертации?**  
A: Оберните код конвертации в блок `try/catch` и логируйте `Aspose.CAD.CadException` для получения подробной информации об ошибке.

**Q: Есть ли пробная версия Aspose.CAD для .NET?**  
A: Да, продукт доступен в бесплатной пробной версии. Подробнее см. [here](https://releases.aspose.com/).

**Q: Где можно получить поддержку или обсудить вопросы, связанные с Aspose.CAD для .NET?**  
A: Перейдите на [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) для общения с сообществом и получения помощи.

**Q: Как получить временную лицензию для Aspose.CAD для .NET?**  
A: Посетите [this link](https://purchase.aspose.com/temporary-license/) для получения временной лицензии, необходимой в процессе разработки.

## Заключение

Теперь вы знаете, как **convert dgn to png** (или JPEG) с помощью Aspose.CAD для .NET. Настраивая параметры растеризации и меняя класс параметров изображения, вы сможете адаптировать вывод под любые требования проекта. Экспериментируйте с различными размерами страниц, настройками DPI и форматами файлов, чтобы получить идеальное растровое изображение для вашего приложения.

---

**Last Updated:** 2026-03-24  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}