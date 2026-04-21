---
date: 2026-03-29
description: Узнайте, как настроить параметры растеризации CAD и экспортировать DGN
  в PDF с поддержкой 3D, используя Aspose.CAD для .NET.
linktitle: Support of 3D for DGN V7
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Настройка параметров растеризации CAD для DGN V7 3D
url: /ru/net/cad-features-and-support/support-of-3d-for-dgn-v7/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Настройка параметров растеризации CAD для DGN V7 3D

## Введение

В этом всестороннем руководстве вы узнаете **как настроить параметры растеризации CAD**, чтобы экспортировать 3‑D файл DGN V7 в PDF с помощью Aspose.CAD для .NET. Независимо от того, создаёте ли вы просмотрщик CAD, инструмент отчётности или автоматизированный конвейер конвертации, освоение этих настроек даёт вам точный контроль над размером страницы, масштабированием макета, цветами фона и конкретными видами, которые вы хотите отобразить. Давайте пройдём процесс шаг за шагом.

## Быстрые ответы
- **Что означает «configure CAD rasterization options»?**  
  Это относится к установке свойств, таких как размеры страницы, масштабирование, цвет фона и выбор макета, перед преобразованием CAD‑файла в растровый формат (например, PDF).
- **Как экспортировать DGN в PDF с поддержкой 3‑D?**  
  Загрузите DGN с помощью `DgnImage`, определите `PdfOptions` + `CadRasterizationOptions`, затем вызовите `Save`.
- **Нужна ли лицензия для использования в продакшене?**  
  Да — для развертывания требуется коммерческая лицензия; доступна бесплатная пробная версия.
- **Какие версии .NET поддерживаются?**  
  .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.
- **Можно ли выбрать конкретные виды для экспорта?**  
  Конечно — задайте массив `Layouts` в параметрах растеризации.

## Что такое «configure CAD rasterization options»?

Настройка параметров растеризации CAD означает настройку того, как чертёж CAD растеризуется (преобразуется из вектора в растровое изображение или PDF). Регулируя эти параметры, вы контролируете визуальный результат, производительность и размер файла получаемого документа.

## Почему использовать Aspose.CAD для экспорта 3‑D DGN V7?

- **Полная интеграция с .NET** – не требуется COM или нативные DLL.  
- **Поддерживает 3‑D геометрию** – сохраняет информацию о глубине при рендеринге в PDF.  
- **Тонкий контроль** – выбирайте точные макеты, масштабирование и цвета фона.  
- **Кросс‑платформенный** – работает на Windows, Linux и macOS с .NET Core.

## Требования

Перед началом убедитесь, что у вас есть:

- **Aspose.CAD for .NET** – скачайте его по ссылке [here](https://releases.aspose.com/cad/net/).  
- **Visual Studio** или любой совместимый .NET IDE.  
- **Пример файла DGN** – для данного руководства будем использовать `Nikon_D90_Camera.dgn` (включён в пакет примеров Aspose).  

Теперь, когда всё готово, перейдём к коду.

## Импорт пространств имён

В вашем .NET проекте импортируйте необходимые пространства имён:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.ImageOptions;
```

## Шаг 1: Настройте каталог документов

Создайте переменную, указывающую на папку, где находятся ваш исходный DGN и файлы вывода.

```csharp
string MyDir = "Your Document Directory";
```

## Шаг 2: Загрузите файл DGN

Загрузите файл DGN как `DgnImage`. Этот объект предоставляет доступ к данным CAD и конвейеру растеризации.

```csharp
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";
string outFile = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Your code for further processing goes here
}
```

## Шаг 3: Настройте параметры экспорта PDF (Configure CAD Rasterization Options)

Здесь мы **настраиваем параметры растеризации CAD**, определяющие, как 3‑D модель будет отрисована в PDF. Вы можете изменить размер страницы, включить автоматическое масштабирование макетов, задать цвет фона и выбрать точные макеты (виды), которые хотите экспортировать.

```csharp
var options = new PdfOptions
{
    VectorRasterizationOptions = new CadRasterizationOptions
    {
        PageWidth = 1500,
        PageHeight = 1500,
        AutomaticLayoutsScaling = true,
        BackgroundColor = Color.Black,
        Layouts = new string[] { "1", "2", "3", "9" } // Only export specified views
    }
};
```

## Шаг 4: Сохраните растровое изображение

Наконец, экспортируйте DGN в PDF‑файл, используя только что настроенные параметры.

```csharp
dgnImage.Save(outFile, options);
```

## Распространённые проблемы и решения

| Проблема | Решение |
|----------|---------|
| **Пустой PDF‑файл** | Убедитесь, что массив `Layouts` содержит правильные идентификаторы видов, присутствующие в файле DGN. |
| **Неправильные цвета** | Убедитесь, что `BackgroundColor` установлен в нужное значение; используйте `Color.White` для светлого фона. |
| **Узкое место производительности при больших файлах** | Включите `AutomaticLayoutsScaling` и рассмотрите возможность уменьшения `PageWidth/PageHeight` для снижения разрешения растра. |
| **Исключение лицензии** | Установите действительную лицензию Aspose.CAD перед загрузкой изображения, чтобы избежать водяных знаков пробной версии. |

## Часто задаваемые вопросы

**В: Можно ли использовать Aspose.CAD для .NET с другими форматами CAD‑файлов?**  
О: Да, Aspose.CAD поддерживает DWG, DXF, DWF, DGN и многие другие форматы.

**В: Как обрабатывать исключения при работе с Aspose.CAD?**  
О: Оберните ваш код в блок `try‑catch` и проверяйте `Aspose.CAD.CADException` для получения подробной информации об ошибке.

**В: Подходит ли Aspose.CAD для коммерческих проектов?**  
О: Абсолютно. Вы можете приобрести лицензию [here](https://purchase.aspose.com/buy).

**В: Можно ли попробовать Aspose.CAD для .NET перед покупкой?**  
О: Да, бесплатная пробная версия доступна [here](https://releases.aspose.com/).

**В: Где можно найти поддержку сообщества для Aspose.CAD?**  
О: Присоединяйтесь к форуму обсуждения [here](https://forum.aspose.com/c/cad/19).

---

**Последнее обновление:** 2026-03-29  
**Тестировано с:** Aspose.CAD 24.11 for .NET  
**Автор:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}