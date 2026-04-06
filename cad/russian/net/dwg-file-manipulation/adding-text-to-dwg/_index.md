---
date: 2026-04-06
description: Узнайте, как конвертировать DWG в PDF и добавить пользовательский текст
  с помощью C# и Aspose.CAD. Это пошаговое руководство охватывает создание PDF из
  DWG, вставку текстового объекта и изменение шрифта текста в DWG.
keywords:
- convert dwg to pdf
- generate pdf from dwg
- insert text entity
- change dwg text font
- aspose cad dwg pdf
linktitle: Добавление текста в DWG‑файлы на C#
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Преобразовать DWG в PDF и добавить текст в C# – учебник Aspose.CAD
url: /ru/net/dwg-file-manipulation/adding-text-to-dwg/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Конвертация DWG в PDF и добавление текста в C# – руководство Aspose.CAD

## Введение

В быстро меняющемся мире CAD и разработки на .NET преобразование **DWG в PDF** с вставкой пользовательских аннотаций является частой задачей. Независимо от того, нужно ли вам создавать печатные чертежи для клиентов или встраивать динамические заметки непосредственно в DWG, Aspose.CAD делает эту работу простой. В этом руководстве вы узнаете, как **конвертировать DWG в PDF**, **добавить текстовый объект** и даже **изменить шрифт текста DWG** с помощью C#.

## Быстрые ответы
- **Какой библиотекой лучше всего выполнять конвертацию DWG‑в‑PDF?** Aspose.CAD for .NET  
- **Могу ли я добавить пользовательский текст при конвертации?** Да — создайте объект `CadText` и добавьте его перед сохранением.  
- **Нужна ли лицензия для использования в продакшене?** Требуется коммерческая лицензия; доступна бесплатная пробная версия.  
- **Какие версии .NET поддерживаются?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Можно ли изменить шрифт текста?** Да, отрегулируйте свойства `CadText`, такие как `StyleType` и `TextHeight`.

## Что такое «конвертация dwg в pdf»?

Преобразование файла DWG в PDF превращает векторный чертеж CAD в широко распространяемый, независимый от устройства документ. PDF сохраняет оригинальную геометрию и слои, одновременно позволяя встраивать аннотации, текст или другие метаданные. Aspose.CAD автоматически обрабатывает растеризацию и векторную отрисовку, поэтому вам не требуется стороннее CAD‑программное обеспечение на сервере.

## Почему добавлять текст в DWG перед конвертацией?

Встраивание текста непосредственно в DWG дает полный контроль над размещением, стилем и назначением слоя. Когда файл позже конвертируется в PDF, текст отображается точно в том месте, где вы его разместили, сохраняя задумку дизайна и устраняя необходимость последующей обработки в PDF‑редакторе.

## Требования

Прежде чем начать, убедитесь, что у вас есть:

- **Aspose.CAD Library** – загрузите её по [download link](https://releases.aspose.com/cad/net/).  
- **Рабочая среда .NET** (Visual Studio 2022, .NET 6 или любая совместимая версия).  
- **Папка для тестовых файлов** – в руководстве мы будем ссылаться на неё как `MyDir`.

Теперь давайте пошагово пройдем процесс.

## Импорт пространств имён

Добавьте необходимые директивы `using`, чтобы получить доступ к классам Aspose.CAD.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects.AttEntities;
using Aspose.CAD.ImageOptions;
```

## Шаг 1: Загрузка файла DWG

Загрузите исходный файл DWG в объект `Image`. Этот объект предоставляет доступ к базовым CAD‑сущностям.

```csharp
string dwgPathToFile = MyDir + "SimpleEntites.dwg";
using (Image image = Image.Load(dwgPathToFile))
{
    // Subsequent steps will be performed inside this block
}
```

## Шаг 2: Создание объекта CadText (вставка текстового объекта)

Класс `CadText` представляет одну строку текста в DWG. Здесь мы задаём его стиль, значение, цвет, слой и позицию. Отрегулируйте `StyleType` или `TextHeight`, чтобы **изменить шрифт текста DWG**.

```csharp
CadText cadText = new CadText();
cadText.StyleType = "Standard";          // Font/style – change to alter DWG text font
cadText.DefaultValue = "Some custom text";
cadText.ColorId = 256;                    // 256 = ByLayer (you can use a specific ACI color)
cadText.LayerName = "0";
cadText.FirstAlignment.X = 47.90;
cadText.FirstAlignment.Y = 5.56;
cadText.TextHeight = 0.8;                 // Height influences visual size
cadText.ScaleX = 0.0;
```

## Шаг 3: Добавление текстового объекта в Model Space

Model Space DWG содержит большинство объектов чертежа. Добавив наш `CadText` в блок `*Model_Space`, текст становится частью чертежа.

```csharp
CadImage cadImage = (CadImage)image;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadText);
```

## Шаг 4: Настройка параметров PDF (генерация PDF из DWG)

Настройте параметры растеризации, которые управляют тем, как DWG преобразуется в PDF. Вы можете изменить размер страницы, тип отрисовки и макет.

```csharp
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;
cadRasterizationOptions.PageHeight = 1600;
cadRasterizationOptions.PageWidth = 1600;
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## Шаг 5: Сохранение изменённого DWG в PDF

Наконец, экспортируйте изменённый чертеж. Полученный PDF будет включать только что вставленный текст.

```csharp
image.Save(MyDir + "SimpleEntites_generated.pdf", pdfOptions);
```

> **Pro tip:** Если вам нужен PDF более высокого разрешения, увеличьте `PageHeight` и `PageWidth` пропорционально.

## Распространённые проблемы и решения

| Проблема | Причина | Решение |
|----------|---------|---------|
| Текст не отображается в PDF | Неправильный слой или идентификатор цвета | Убедитесь, что `LayerName` существует и `ColorId` установлен в видимый цвет (например, 7 для белого). |
| Текст расположен неверно | Неправильные координаты выравнивания | Проверьте значения `FirstAlignment.X/Y` относительно единиц чертежа. |
| PDF пустой | Параметры растеризации не заданы | Установите `DrawType` в `UseObjectColor` или `UseObjectLineWeight`. |

## Часто задаваемые вопросы (существующие)

### Вопрос 1: Совместим ли Aspose.CAD со всеми версиями файлов DWG?

A1: Aspose.CAD поддерживает широкий спектр версий файлов DWG, обеспечивая совместимость с различным CAD‑программным обеспечением.

### Вопрос 2: Можно ли добавить несколько текстовых объектов в один файл DWG с помощью Aspose.CAD?

A2: Да, вы можете добавить несколько текстовых объектов в файл DWG, повторяя процесс, описанный в руководстве.

### Вопрос 3: Как изменить шрифт и стиль текста в Aspose.CAD?

A3: Чтобы изменить шрифт и стиль текста, отрегулируйте свойства объекта `CadText` перед его добавлением в файл DWG.

### Вопрос 4: Есть ли лицензионные ограничения при использовании Aspose.CAD в коммерческом проекте?

A5: Да, убедитесь, что вы соблюдаете условия лицензирования Aspose.CAD. Смотрите [Aspose.CAD Purchase](https://purchase.aspose.com/buy) для деталей.

### Вопрос 5: Где я могу получить помощь или обсудить вопросы, связанные с Aspose.CAD?

A5: Посетите [форум Aspose.CAD](https://forum.aspose.com/c/cad/19), чтобы связаться с сообществом и получить поддержку.

## Дополнительные часто задаваемые вопросы

**Вопрос:** Как сгенерировать PDF из DWG без добавления текста?  
**Ответ:** Пропустите шаг создания `CadText` и напрямую настройте `PdfOptions` перед вызовом `image.Save(...)`.

**Вопрос:** Можно ли программно изменить цвет текста?  
**Ответ:** Да, установите `cadText.ColorId` в конкретный номер цвета ACI (например, 1 для красного).

**Вопрос:** Можно ли вставить многострочный текст?  
**Ответ:** Используйте `CadMText` для многострочных текстовых блоков; подход аналогичен `CadText`.

**Вопрос:** Поддерживает ли Aspose.CAD пакетную конвертацию нескольких файлов DWG?  
**Ответ:** Да — пройдитесь по каталогу с DWG‑файлами, примените те же шаги и сохраните каждый в PDF.

## Заключение

Теперь у вас есть полностью готовый к продакшену рабочий процесс для **конвертации DWG в PDF**, **добавления пользовательского текста** и **настройки внешнего вида текста** с использованием C# и Aspose.CAD. Эта техника идеальна для автоматической генерации чертежей, конвейеров отчетности или любой ситуации, когда необходимо обогащать CAD‑файлы «на лету».

---

**Последнее обновление:** 2026-04-06  
**Тестировано с:** Aspose.CAD 24.11 for .NET  
**Автор:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}