---
date: 2025-12-18
description: Изучите, как экспортировать DWG в PDF или растровые изображения на Java
  с помощью Aspose.CAD. Это пошаговое руководство обеспечивает точность, эффективность
  и простоту конвертации файлов DWG.
linktitle: Export DWG to PDF or Raster
second_title: Aspose.CAD Java API
title: Экспорт DWG в PDF или растр с использованием Aspose.CAD для Java
url: /ru/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Экспорт DWG в PDF или растровый формат с помощью Aspose.CAD для Java

## Introduction

В динамичном мире систем автоматизированного проектирования (CAD) эффективное управление чертежами имеет решающее значение. С **Aspose.CAD for Java** вы можете **экспортировать dwg в pdf** — или растровые изображения — всего в несколько строк кода. Этот учебник проведет вас через весь процесс, от загрузки файла DWG до создания PDF высокого качества, подчёркивая, почему Aspose.CAD Java является предпочтительной библиотекой для задач конвертации CAD.

## Quick Answers
- **Что покрывает этот учебник?** Экспорт файлов DWG в PDF или растровые изображения с использованием Aspose.CAD for Java.  
- **Нужна ли лицензия?** Доступна бесплатная временная лицензия для оценки; полная лицензия требуется для продакшн.  
- **Какая версия Java поддерживается?** Любой runtime Java 8+ работает с последним API Aspose.CAD Java.  
- **Могу ли я конвертировать DWG в другие форматы изображений?** Да — те же параметры растеризации позволяют выводить PNG, JPEG, BMP и т.д.  
- **Сколько времени занимает конвертация?** Обычно менее секунды для стандартных чертежей; более крупные файлы могут занять несколько секунд.

## What is “export dwg to pdf”?

Экспорт DWG в PDF означает преобразование родного чертежа AutoCAD в переносимый, независимый от устройства документ PDF. Полученный PDF сохраняет векторные данные, слои и масштабирование, что делает его идеальным для обмена, печати или архивирования.

## Why use Aspose.CAD Java for this conversion?
- **Нет внешних зависимостей** — чистый Java, без нативных DLL.  
- **Точное управление единицами** — автоматически учитывает метрические или имперские единицы.  
- **Высококачественный растровый вывод** — тонко настроенный DPI и контроль размера страницы.  
- **Полная поддержка PDF** — генерация PDF с сохранением векторов без дополнительных библиотек.

## Prerequisites

Перед тем как приступить к коду, убедитесь, что у вас есть:

- Базовые знания программирования на Java.  
- Установленная библиотека Aspose.CAD for Java. Если вы ещё не скачали её, получите её **[здесь](https://releases.aspose.com/cad/java/)**.  
- Файл DWG для тестирования — в этом руководстве используется пример **Bottom_plate.dwg**.

## Import Namespaces

В вашем Java‑проекте импортируйте необходимые классы для начала конвертации:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## Step‑by‑Step Guide

### Step 1: Load the DWG File

Сначала загрузите ваш DWG‑чертеж, используя класс `Image`. Это создаёт представление в памяти, с которым может работать Aspose.CAD.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

### Step 2: Determine Unit Type

Понимание того, использует ли чертеж метрические или имперские единицы, необходимо для правильного масштабирования. Вспомогательный метод `IsMetric` (реализация опущена для краткости) возвращает логический флаг.

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

### Step 3: Set Rasterization Options

В зависимости от системы единиц настройте размер страницы, масштаб и целевой тип единиц. Эти параметры определяют, как DWG будет растеризован перед тем, как будет упакован в PDF.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();

if (currentUnitIsMetric) {
    // Metric units
    double metersCoeff = 1 / 1000.0;
    double scaleFactor = metersCoeff / currentUnitCoefficient;
    rasterizationOptions.setPageWidth((float)(210 * scaleFactor));
    rasterizationOptions.setPageHeight((float)(297 * scaleFactor));
    rasterizationOptions.setUnitType(UnitType.Millimeter);
} else {
    // Imperial units
    rasterizationOptions.setPageWidth((float)(8.27f / currentUnitCoefficient));
    rasterizationOptions.setPageHeight((float)(11.69f / currentUnitCoefficient));
    rasterizationOptions.setUnitType(UnitType.Inch);
}
```

### Step 4: Configure PDF Options

Создайте экземпляр `PdfOptions` и прикрепите к нему настройки растеризации. Это указывает Aspose.CAD, как встроить растеризованный контент в окончательный PDF.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

### Step 5: Save as PDF

Наконец, экспортируйте чертеж в файл PDF. Метод `save` принимает путь вывода и настроенный `PdfOptions`.

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

Когда код завершит работу, вы найдёте **Saved.pdf** в вашей папке `DWGDrawings`, готовый к распространению или архивированию.

## Common Issues & Tips

- **Неправильный размер страницы** — проверьте логику преобразования единиц; несоответствующие коэффициенты могут привести к слишком большим страницам.  
- **Отсутствуют шрифты или толщины линий** — убедитесь, что DWG ссылается на все внешние ресурсы перед конвертацией.  
- **Производительность при больших чертежах** — увеличивайте параметр `DPI` в `CadRasterizationOptions` только при необходимости более высокого качества; более низкий DPI ускоряет обработку.

## Frequently Asked Questions

**В: Могу ли я использовать Aspose.CAD for Java с другими Java‑фреймворками?**  
О: Да, Aspose.CAD for Java без проблем интегрируется с популярными Java‑фреймворками, такими как Spring, Jakarta EE и Android.

**В: Доступна ли временная лицензия для Aspose.CAD for Java?**  
О: Да, вы можете получить временную лицензию **[здесь](https://purchase.aspose.com/temporary-license/)**.

**В: Где я могу найти поддержку для Aspose.CAD for Java?**  
О: Посетите **[форум Aspose.CAD](https://forum.aspose.com/c/cad/19)** для получения помощи от сообщества и инженеров Aspose.

**В: Как я могу приобрести лицензию для Aspose.CAD for Java?**  
О: Вы можете приобрести лицензию **[здесь](https://purchase.aspose.com/buy)**.

**В: Какие единицы измерения поддерживает Aspose.CAD for Java?**  
О: Aspose.CAD for Java поддерживает как метрические, так и имперские единицы, автоматически определяя систему единиц чертежа.

**В: Могу ли я конвертировать DWG в другие форматы изображений (например, PNG, JPEG) с помощью того же API?**  
О: Конечно. Замените `PdfOptions` на соответствующие параметры растрового изображения (например, `PngOptions`) и повторно используйте те же `CadRasterizationOptions`.

## Conclusion

В этом учебнике продемонстрировано, как **экспортировать dwg в pdf** и растровые изображения с помощью Aspose.CAD for Java. Следуя пошаговому руководству, вы сможете интегрировать надёжную конвертацию CAD в любое Java‑приложение, будь то PDF‑документация или растровые изображения для веб‑отображения.

---

**Last Updated:** 2025-12-18  
**Tested With:** Aspose.CAD for Java 24.10  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}