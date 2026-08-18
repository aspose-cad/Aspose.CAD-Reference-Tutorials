---
date: 2026-03-05
description: Узнайте, как установить тайм‑аут при сохранении при конвертации DWG в
  PDF с помощью Aspose.CAD для .NET. Повышайте эффективность и контроль в ваших .NET‑приложениях.
linktitle: Setting Timeout on Save Operation
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Как установить тайм‑аут при операции сохранения — руководство Aspose.CAD
url: /ru/net/advanced-cad-techniques/setting-timeout-on-save-operation/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Как установить тайм‑аут при операции сохранения - руководство Aspose.CAD

## Introduction

В этом руководстве вы узнаете **как установить тайм‑аут** при сохранении CAD, техника, которая помогает избежать зависания длительных конвертаций. Управление тайм‑аутом особенно полезно, когда вы **конвертируете DWG в PDF** или **экспортируете CAD PDF** файлы в пакетных заданиях или веб‑службах. Aspose.CAD for .NET предоставляет чистый API, позволяющий контролировать операцию сохранения, одновременно используя мощный движок растеризации.

## Quick Answers
- **Что контролирует тайм‑аут?** Он прерывает операцию сохранения/экспорта, если она длится дольше указанного периода.  
- **Какие форматы получают наибольшую выгоду?** Конвертация больших DWG‑файлов в PDF или растровые изображения, где время обработки может варьироваться.  
- **Нужна ли лицензия?** Для использования в продакшене требуется действующая лицензия Aspose.CAD; бесплатная пробная версия подходит для оценки.  
- **Можно ли настроить длительность?** Да — просто измените значение `Thread.Sleep` (в миллисекундах) в соответствии с вашими потребностями.  
- **Подходит ли этот подход для async?** Пример использует `Task.Factory.StartNew`, что упрощает интеграцию в асинхронные рабочие процессы.

## What is “how to set timeout” in the context of CAD saving?

Установка тайм‑аута означает привязку `InterruptionToken` к параметрам сохранения и вызов прерывания после заданного интервала. Это предотвращает бесконечное зависание операции, обеспечивая предсказуемую производительность и лучшее управление ресурсами.

## Why use Aspose.CAD to convert DWG to PDF with a timeout?

- **Надёжность:** Гарантирует, что неконтролируемая конверсия не заблокирует ваш сервис.  
- **Масштабируемость:** Позволяет обрабатывать множество файлов параллельно, не опасаясь, что один файл задержит конвейер.  
- **Качество:** Сохраняет высокоточную растеризацию Aspose.CAD, добавляя при этом механизмы безопасности.

## Prerequisites

Прежде чем приступить, убедитесь, что у вас есть следующее:

- **Aspose.CAD for .NET** – интегрирован в ваш проект. Скачать можно [здесь](https://releases.aspose.com/cad/net/).
- **Document Directory** – папка, в которой будут находиться исходные DWG‑файлы и создаваемые PDF.

## Import Namespaces

Сначала импортируйте пространства имён, предоставляющие классы, необходимые для растеризации, параметров PDF и механизма прерывания.

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Threading;
using System.Threading.Tasks;
```

## How to Set Timeout on Save Operation

Ниже представлено пошаговое руководство. Каждый шаг содержит краткое объяснение, за которым следует оригинальный блок кода (без изменений).

### Step 1: Load CAD Drawing

Шаг 1: Загрузка CAD‑рисунка

Мы загружаем исходный DWG‑файл из указанной директории. Метод `Image.Load` возвращает объект `Image`, представляющий CAD‑рисунок.

```csharp
// Example: Loading CAD Drawing
string SourceDir = "Your Document Directory";
string OutputDir = "Your Document Directory";

using (Image cadDrawing = Image.Load(SourceDir + "Drawing11.dwg"))
{
    // Code for subsequent steps will be placed here
}
```

### Step 2: Configure Rasterization Options

Шаг 2: Настройка параметров растеризации

Установите параметры растеризации так, чтобы экспортируемый PDF соответствовал размерам оригинального рисунка. Здесь вы задаёте ширину и высоту страницы, а также другие настройки рендеринга.

```csharp
// Example: Configuring Rasterization Options
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = cadDrawing.Size.Width;
rasterizationOptions.PageHeight = cadDrawing.Size.Height;
```

### Step 3: Create PDF Options (Export CAD PDF)

Шаг 3: Создание параметров PDF (Экспорт CAD PDF)

Создайте экземпляр `PdfOptions` и привяжите к нему настройки растеризации. Этот объект будет передан методу `Save` для генерации PDF‑версии DWG‑файла.

```csharp
// Example: Creating PDF Options
PdfOptions CADf = new PdfOptions();
CADf.VectorRasterizationOptions = rasterizationOptions;
```

### Step 4: Implement Timeout Mechanism

Шаг 4: Реализация механизма тайм‑аута

Мы используем `InterruptionTokenSource` для получения токена, способного прервать операцию сохранения. Фоновая задача выполняет экспорт, в то время как основной поток спит заданное время тайм‑аута (например, 10 секунд). После сна вызываем `Interrupt()`, чтобы отменить операцию, если она всё ещё выполняется.

```csharp
// Example: Implementing Timeout Mechanism
using (var its = new InterruptionTokenSource())
{
    CADf.InterruptionToken = its.Token;

    var exportTask = Task.Factory.StartNew(() =>
    {
        cadDrawing.Save(OutputDir + "PutTimeoutOnSave_out.pdf", CADf);
    });

    Thread.Sleep(10000); // Set your desired timeout duration in milliseconds
    its.Interrupt();

    exportTask.Wait();
}
```

### Step 5: Finalize and Confirm

Шаг 5: Завершение и подтверждение

После экспорта (или прерывания) выведите сообщение подтверждения в консоль. В реальном приложении вы можете записать результат в журнал или вызвать событие.

```csharp
// Example: Finalizing and Confirming
Console.WriteLine("PutTimeoutOnSave executed successfully");
```

## Common Issues and Solutions

| Проблема | Причина | Решение |
|-------|-------|--------|
| Экспорт зависает бесконечно | Токен прерывания не привязан | Убедитесь, что `CADf.InterruptionToken = its.Token;` установлен перед запуском задачи. |
| PDF пустой или повреждённый | Неправильный путь к выходной директории | Проверьте, что `OutputDir` заканчивается разделителем пути и имя файла корректно. |
| Тайм‑аут слишком короткий, приводит к преждевременному прерыванию | Значение `Thread.Sleep` слишком мало для больших файлов | Увеличьте длительность сна или вычислите адаптивный тайм‑аут в зависимости от размера файла. |

## Frequently Asked Questions

**Q1: Можно ли настроить длительность тайм‑аута?**  
A: Конечно. Измените значение, передаваемое в `Thread.Sleep` (в миллисекундах), чтобы соответствовать вашим ожиданиям по производительности.

**Q2: Есть ли другие параметры растеризации?**  
A: Да. `CadRasterizationOptions` предоставляет свойства, такие как `Resolution`, `BackgroundColor` и `DrawType`, позволяющие точно настроить вывод PDF.

**Q3: Как обрабатывать прерывания в приложении?**  
A: Используйте классы `InterruptionToken` и `InterruptionTokenSource`, как показано. Они обеспечивают потокобезопасный способ отмены длительных операций.

**Q4: Подходит ли Aspose.CAD для 2D и 3D CAD‑файлов?**  
A: Он поддерживает широкий спектр 2D и 3D форматов, включая DWG, DXF, DGN и другие.

**Q5: Где можно получить дополнительную помощь или поддержку сообщества?**  
A: Посетите [форум Aspose.CAD](https://forum.aspose.com/c/cad/19) для обсуждений, примеров кода и советов по устранению неполадок.

## Conclusion

Следуя приведённым выше шагам, вы теперь знаете, **как установить тайм‑аут** для операций сохранения CAD, что позволяет надёжно **конвертировать DWG в PDF** или **экспортировать CAD PDF** файлы без риска зависания процессов. Внедрите этот шаблон в пакетные конвертеры, веб‑службы или любой автоматизированный конвейер, где важна предсказуемость.

---

**Последнее обновление:** 2026-03-05  
**Тестировано с:** Aspose.CAD 24.12 for .NET  
**Автор:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}