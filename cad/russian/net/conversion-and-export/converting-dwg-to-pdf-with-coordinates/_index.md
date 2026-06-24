---
date: 2026-04-03
description: Узнайте, как установить окно просмотра и конвертировать DWG в PDF на
  C# с помощью Aspose.CAD. Этот учебник по преобразованию DWG в PDF демонстрирует
  точный экспорт с координатами.
keywords:
- how to set viewport
- dwg to pdf tutorial
- convert dwg to pdf c#
linktitle: Конвертация DWG в PDF с координатами на C#
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Как установить область просмотра при конвертации DWG в PDF с координатами в
  C# — руководство Aspose.CAD
url: /ru/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Преобразование DWG в PDF с координатами на C# — руководство Aspose.CAD

## Введение

Добро пожаловать в это подробное руководство по **how to set viewport** при преобразовании файлов DWG в PDF с указанными координатами с использованием Aspose.CAD для .NET. Управляя областью просмотра, вы получаете пиксельно‑точные PDF, точно соответствующие нужной области — идеально для строительных чертежей, предварительных просмотров планов этажей или любого BIM‑рабочего процесса.

## Быстрые ответы
- **Что означает “set viewport”?** Он определяет видимую область и масштабирование CAD‑чертежа во время растеризации.  
- **Какая библиотека обрабатывает конвертацию?** Aspose.CAD for .NET.  
- **Нужна ли лицензия?** Бесплатная пробная версия подходит для оценки; коммерческая лицензия требуется для продакшн‑использования.  
- **Поддерживаемые платформы?** Windows, Linux и macOS с .NET 5/6/7 или .NET Framework 4.6+.  
- **Типичное время реализации?** Около 10‑15 минут для базового преобразования.

## Предварительные требования

Перед началом убедитесь, что у вас есть следующие требования:

- **Aspose.CAD Library** – Скачайте и установите библиотеку Aspose.CAD для .NET. Вы можете найти библиотеку [здесь](https://releases.aspose.com/cad/net/).
- **Development Environment** – Visual Studio, Rider или любая IDE, поддерживающая разработку на .NET.
- **DWG File** – Подготовьте файл DWG для конвертации. Вы можете использовать предоставленный пример файла или ваш собственный DWG‑файл.

## Как установить область просмотра для точного экспорта PDF

Установка области просмотра — это основной шаг, позволяющий задать точную область чертежа, которую вы хотите отрисовать. В коде ниже мы создаём новый `CadVportTableObject`, позиционируем его с координатой верхнего‑левого угла и вычисляем ширину, высоту и соотношение сторон. Это реализация **how to set viewport**, которая управляет остальной частью конвертации.

## Импорт пространств имён

В вашем проекте C# импортируйте необходимые пространства имён:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadParameters;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.ImageOptions;
```

Разберём код пошагово для лучшего понимания:

## Шаг 1: Определить каталог документа

```csharp
string MyDir = "Your Document Directory";
```

## Шаг 2: Установить путь к исходному файлу DWG

```csharp
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
```

## Шаг 3: Загрузить файл DWG и настроить параметры растеризации

```csharp
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
    rasterizationOptions.Layouts = new string[] { "Model" };
    rasterizationOptions.NoScaling = true;
```

## Шаг 4: Определить координаты и область просмотра  

Здесь мы действительно **set the viewport** (how to set viewport), указывая верхний‑левый угол, ширину и высоту области, которую хотите экспортировать.

```csharp
    Point topLeft = new Point(500, 1000);
    double width = 3108;
    double height = 2489;

    CadVportTableObject newView = new CadVportTableObject();
    newView.Name = new CadStringParameter();
    newView.Name.Init("*Active");
    newView.CenterPoint.X = topLeft.X + width / 2f;
    newView.CenterPoint.Y = topLeft.Y - height / 2f;
    newView.ViewHeight.Value = height;
    newView.ViewAspectRatio.Value = width / height;
```

## Шаг 5: Применить настройки области просмотра

```csharp
    for (int i = 0; i < cadImage.ViewPorts.Count; i++)
    {
        CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
        if (cadImage.ViewPorts.Count == 1 || string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
        {
            cadImage.ViewPorts[i] = newView;
            break;
        }
    }
```

## Шаг 6: Настроить параметры PDF и экспортировать  

Теперь мы объединяем всё вместе и **convert DWG to PDF** с использованием подготовленных параметров растеризации.

```csharp
    Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
    pdfOptions.VectorRasterizationOptions = rasterizationOptions;

    MyDir = MyDir + "ConvertDWGToPDFBySupplyingCoordinates_out.pdf";
    cadImage.Save(MyDir, pdfOptions);
}
```

## Шаг 7: Показать сообщение об успехе

```csharp
Console.WriteLine("\nThe DWG file exported successfully to PDF.\nFile saved at " + MyDir);
```

## Общие сценарии использования

- **Construction documentation** – Создавайте печатные PDF‑файлы конкретных секций планов этажей.  
- **BIM coordination** – Экспортируйте только интересующую область для обнаружения конфликтов.  
- **Client presentations** – Предоставляйте чистый PDF выбранной комнаты или фасада без раскрытия всего чертежа.

## Заключение

Поздравляем! Вы успешно **converted DWG to PDF** с точными координатами и научились **how to set viewport** с помощью Aspose.CAD для .NET. Этот **dwg to pdf tutorial** демонстрирует, как **create pdf from dwg** и **export dwg as pdf c#**, сохраняя полный контроль над областью вывода.

## Часто задаваемые вопросы

### Q1: Могу ли я использовать Aspose.CAD с другими форматами CAD?

A1: Да, Aspose.CAD поддерживает различные форматы CAD, включая DWG, DXF, DWF и другие.

### Q2: Как я могу обрабатывать ошибки во время процесса конвертации?

A2: Реализуйте механизмы обработки ошибок с помощью блоков try‑catch для захвата и управления исключениями.

### Q3: Подходит ли Aspose.CAD как для Windows, так и для Linux сред?

A3: Да, Aspose.CAD совместим как с Windows, так и с Linux платформами.

### Q4: Могу ли я дополнительно настроить вывод PDF?

A4: Конечно! Исследуйте обширные возможности, предоставляемые Aspose.CAD, чтобы адаптировать вывод PDF под ваши конкретные требования.

### Q5: Где я могу найти дополнительную поддержку или обсуждения в сообществе?

A5: Посетите [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) для поддержки сообщества и обсуждений.

## Дополнительные часто задаваемые вопросы

**Q: Работает ли этот подход с большими файлами DWG (сотни МБ)?**  
A: Да. Растеризация выполняется постранично, и вы можете настроить `rasterizationOptions` (например, `Resolution`) для балансировки качества и использования памяти.

**Q: Могу ли я экспортировать несколько областей просмотра в отдельные страницы PDF?**  
A: Вы можете перебрать `cadImage.ViewPorts`, установить каждую как активную и вызвать `Save` для каждой страницы, затем объединить PDF‑файлы с помощью Aspose.PDF.

**Q: Можно ли добавить водяной знак в сгенерированный PDF?**  
A: После сохранения PDF вы можете открыть его с помощью Aspose.PDF и применить текстовый или графический водяной знак перед передачей пользователю.

---

**Last Updated:** 2026-04-03  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}