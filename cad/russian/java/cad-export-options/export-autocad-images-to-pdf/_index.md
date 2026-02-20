---
date: 2026-02-20
description: Узнайте, как экспортировать PDF из AutoCAD с помощью Aspose.CAD для Java.
  Это пошаговое руководство покажет, как **конвертировать DWG в PDF**, **сохранить
  CAD в PDF** и работать с лицензированием.
linktitle: Export AutoCAD Images to PDF
second_title: Aspose.CAD Java API
title: Конвертировать DWG в PDF — экспортировать изображения AutoCAD в PDF с помощью
  Aspose.CAD для Java
url: /ru/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Экспорт PDF из AutoCAD — Экспорт изображений AutoCAD в PDF с помощью Aspose.CAD для Java

## Introduction

Ищете способ **convert DWG to PDF** с помощью Java? Вы попали по адресу! В этом руководстве мы пошагово покажем, как конвертировать изображения AutoCAD в PDF с помощью Aspose.CAD for Java — мощной библиотеки, упрощающей процесс **convert DWG to PDF**. К концу вы поймёте, как **save CAD as PDF**, настроить параметры растеризации и использовать лицензию Aspose.CAD для продакшн‑использования.

## Quick Answers
- **Can I convert DWG to PDF with Java?** Да, Aspose.CAD for Java обрабатывает DWG, DXF и многие другие форматы.  
- **Do I need a license?** Требуется **Aspose CAD license** для неограниченного использования; временная лицензия доступна для оценки.  
- **What Java version is supported?** Java 8+ (библиотека совместима со всеми современными JDK).  
- **Can I customize PDF page size?** Конечно — измените `pageWidth` и `pageHeight` в параметрах растеризации.  
- **Is 3‑D rasterization possible?** Да, включите `TypeOfEntities.Entities3D` для полной 3‑D визуализации.

## What is **export autocad pdf**?
Экспорт AutoCAD PDF означает преобразование векторных CAD‑чертежей (DWG, DXF, DWF и др.) в переносимый PDF‑документ с сохранением слоёв, толщины линий и, при необходимости, 3‑D геометрии. Это удобно для обмена проектами с клиентами, архивирования или печати без необходимости установки CAD‑программного обеспечения.

## Why Convert DWG to PDF with Aspose.CAD for Java?
- **Full format support** — работает с DWG, DXF, DWF и многими другими.  
- **No external dependencies** — чистая Java‑библиотека, без нативных DLL.  
- **High‑quality rasterization** — контроль над DPI, размером страницы и компоновкой, так что вы можете **customize PDF page size** в соответствии с требованиями проекта.  
- **License flexibility** — начните с бесплатной пробной версии, затем перейдите на постоянную **Aspose CAD license**.  

## Prerequisites

Перед началом убедитесь, что у вас есть:

- **Java Development Environment** — установлен JDK 8 или новее.  
- **Aspose.CAD for Java Library** — скачайте по [download link](https://releases.aspose.com/cad/java/).  
- **Document Directory** — папка на вашем компьютере, где будут находиться исходные CAD‑файлы и сгенерированные PDF.

## Import Namespaces

В вашем Java‑проекте импортируйте необходимые классы для работы с Aspose.CAD:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

Теперь пройдёмся по коду шаг за шагом.

## How to convert DWG to PDF with Aspose.CAD for Java

### Step 1: Set the Resource Directory Path

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **Pro tip:** Замените `"Your Document Directory"` на абсолютный путь к папке, которую вы создали в разделе требований.

### Step 2: Load the CAD Image

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **Why this matters:** Загрузка CAD‑файла в объект `Image` даёт полный доступ к движку растеризации Aspose.CAD.

### Step 3: Set Rasterization Options

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- Настройте `pageWidth` и `pageHeight`, чтобы **customize PDF page size**.  
- Раскомментируйте строку `setTypeOfEntities`, если вам нужен **java convert cad pdf** для 3‑D сущностей.  
- Вызов `setLayouts` выбирает, какой макет (Model, Layout1 и т.д.) будет отрисован.

### Step 4: Configure PDF Options

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Это связывает параметры растеризации с выводом PDF, гарантируя корректное преобразование векторных данных.

### Step 5: Save the PDF

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

Полученный файл `Export3DImagestoPDF_out_.pdf` представляет собой **save cad as pdf** версию вашего оригинального чертежа AutoCAD.

## Common Issues & Solutions

| Symptom | Likely Cause | Fix |
|---------|--------------|-----|
| Blank PDF output | Rasterization options not set or layout mismatch | Verify `setLayouts` matches the layout name in your CAD file. |
| Low‑resolution image | `pageWidth`/`pageHeight` too small | Increase dimensions or set a higher DPI via `rasterizationOptions.setResolution(...)`. |
| License exception | No valid license applied | Apply an **Aspose CAD license** or use a temporary license for testing. |

## Frequently Asked Questions

### Q1: Can I use Aspose.CAD for Java with other CAD file formats?
A1: Yes, Aspose.CAD supports a wide range of formats including DWG, DWF, DGN, and more, giving you flexibility in your projects.

### Q2: How can I obtain a temporary license for Aspose.CAD for Java?
A2: Visit [here](https://purchase.aspose.com/temporary-license/) to obtain a temporary license for evaluation.

### Q3: Are there any layout options for rasterization?
A3: Yes, you can customize layouts (e.g., `"Model"`, `"Layout1"`) through the `setLayouts` method to control which view is rendered.

### Q4: Can I customize the size of the output PDF file?
A4: Absolutely! Adjust the `pageWidth` and `pageHeight` parameters in the rasterization options to fit your desired dimensions.

### Q5: Where can I seek help or discuss issues related to Aspose.CAD for Java?
A5: Head over to the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for dedicated support and community discussions.

---

**Last Updated:** 2026-02-20  
**Tested With:** Aspose.CAD for Java 24.10  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}