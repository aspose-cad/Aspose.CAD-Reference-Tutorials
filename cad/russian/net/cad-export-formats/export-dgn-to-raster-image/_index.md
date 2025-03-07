---
title: Экспорт DGN в растровое изображение в Aspose.CAD для .NET
linktitle: Экспорт DGN в растровое изображение
second_title: Aspose.CAD .NET — формат файлов CAD и BIM
description: Легко конвертируйте DGN в растровые изображения с помощью Aspose.CAD для .NET. Изучите пошаговое руководство и раскройте возможности .NET при работе с файлами САПР.
weight: 13
url: /ru/net/cad-export-formats/export-dgn-to-raster-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Экспорт DGN в растровое изображение в Aspose.CAD для .NET

## Введение

В динамичной сфере разработки .NET Aspose.CAD выступает в качестве мощного инструмента для обработки файлов автоматизированного проектирования (САПР). В этом руководстве рассматривается процесс экспорта файлов DGN в растровые изображения с использованием Aspose.CAD для .NET. Если вы заинтересованы в плавном преобразовании файлов DGN в визуально привлекательные растровые изображения, вы попали по адресу.

## Предварительные условия

Прежде чем мы отправимся в это путешествие, убедитесь, что у вас есть следующие предпосылки:

-  Aspose.CAD для .NET: убедитесь, что в вашем проекте .NET установлена библиотека Aspose.CAD. Вы можете найти библиотеку и соответствующую документацию на сайте[Веб-сайт](https://reference.aspose.com/cad/net/).

- Образец файла DGN: подготовьте файл DGN для преобразования. В нашем примере мы будем использовать «Nikon_D90_Camera.dgn».

Теперь давайте углубимся в пошаговое руководство.

## Импортировать пространства имен

Начните свой проект .NET с импорта необходимых пространств имен для Aspose.CAD. Этот шаг позволяет вам получить доступ к классам и методам, необходимым для преобразования DGN в растровые изображения.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Шаг 1. Загрузите файл DGN

 Начните с загрузки файла DGN в`CadImage` объект. Это обеспечивает основу для последующих операций.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Здесь находится ваш код для дальнейшей обработки
}
```

## Шаг 2. Определите параметры растеризации

 Создать`CadRasterizationOptions` объект и задайте различные свойства, чтобы настроить процесс растеризации в соответствии с вашими требованиями.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## Шаг 3. Создайте объект JpegOptions

 Поскольку мы стремимся преобразовать файл DGN в JPEG, создайте`JpegOptions` объект и назначьте ранее определенный`CadRasterizationOptions` к этому.

```csharp
ImageOptionsBase options = new JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
```

## Шаг 4. Сохраните растровое изображение

 Используйте`Save` метод`CadImage` для экспорта файла DGN в растровое изображение в нужном формате, в данном случае в JPEG.

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpg", options);
```

## Заключение

Поздравляем! Вы успешно прошли этапы экспорта файла DGN в растровое изображение с помощью Aspose.CAD для .NET. Это руководство предоставило вам необходимые знания для легкой интеграции этой функции в ваши проекты .NET.

## Часто задаваемые вопросы

### Вопрос 1. Могу ли я экспортировать файлы DGN в форматы, отличные от JPEG?

О1: Да, Aspose.CAD for .NET поддерживает различные форматы вывода. Вы можете соответствующим образом изменить параметры на шаге 3.

### Вопрос 2. Как обрабатывать исключения в процессе преобразования?

A2. Убедитесь, что у вас есть правильная обработка исключений, как показано в предоставленном коде, для устранения потенциальных проблем.

### Вопрос 3: Доступна ли пробная версия Aspose.CAD для .NET?

 О3: Да, вы можете изучить продукт, воспользовавшись бесплатной пробной версией. Посещать[здесь](https://releases.aspose.com/) Чтобы получить больше информации.

### Вопрос 4: Где я могу обратиться за помощью или обсудить вопросы, связанные с Aspose.CAD for .NET?

 A4: Отправляйтесь в[Форум Aspose.CAD](https://forum.aspose.com/c/cad/19) за поддержку сообщества и обсуждения.

### Вопрос 5: Как получить временную лицензию на Aspose.CAD для .NET?

 А5: Посетите[эта ссылка](https://purchase.aspose.com/temporary-license/)приобрести временную лицензию для ваших нужд разработки.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
