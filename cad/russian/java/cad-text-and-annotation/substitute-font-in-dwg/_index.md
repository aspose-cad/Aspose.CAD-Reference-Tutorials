---
date: 2025-12-28
description: Узнайте, как загружать DWG‑файлы в Java‑проекты и задавать имя основного
  шрифта с помощью Aspose.CAD для Java. Пошаговое руководство для идеального отображения
  CAD‑визуализации.
linktitle: Substitute Font in DWG
second_title: Aspose.CAD Java API
title: Как загрузить DWG‑файл в Java и заменить шрифт с помощью Aspose.CAD
url: /ru/java/cad-text-and-annotation/substitute-font-in-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Как загрузить DWG файл в Java и заменить шрифт с помощью Aspose.CAD

## Introduction

Если вам нужно **загрузить DWG файл Java** в приложениях и придать чертежам аккуратный вид, замена шрифта — быстрый способ достичь этого. С Aspose.CAD for Java вы можете заменить стиль текста по умолчанию любым шрифтом, установленным в системе, гарантируя, что каждая аннотация будет выглядеть точно так, как вы ожидаете. В этом руководстве мы пройдем весь процесс — от загрузки DWG файла в Java до использования метода `setPrimaryFontName` для изменения шрифта.

## Quick Answers
- **What library do I need?** Aspose.CAD for Java.  
- **Can I load a DWG file in Java?** Yes, simply call `Image.load()` on the DWG path.  
- **Which method changes the font?** `setPrimaryFontName`.  
- **Do I need a license for production?** Yes, a commercial license is required.  
- **Is batch processing possible?** Absolutely – loop through multiple files with the same code.

## What is “load dwg file java”?

Загрузка DWG файла в среде Java означает чтение бинарных CAD‑данных в объект `Image`, которым может управлять Aspose.CAD. После загрузки файла у вас появляется полный программный доступ к слоям, стилям и текстовым объектам.

## Why substitute fonts in a DWG file?

- **Consistency:** Гарантирует, что все участники видят один и тот же шрифт, независимо от их локальных настроек.  
- **Readability:** Некоторые шрифты CAD по умолчанию трудно читаются на экране; замена на чистый шрифт, например Arial, повышает чёткость.  
- **Branding:** Соответствует техническим чертежам корпоративным руководствам по стилю.

## Prerequisites

- **Java Development Kit (JDK)** – любая современная версия (рекомендовано 8+).  
- **Aspose.CAD for Java** – скачайте с [website](https://releases.aspose.com/cad/java/).  
- **Sample DWG file** – чертеж, который вы хотите изменить (можете использовать любой DWG или DXF файл для тестов).

## Import Namespaces

В вашем Java‑проекте импортируйте необходимые классы для работы с Aspose.CAD. Эти импорты дают доступ к загрузке изображений, CAD‑специфичным объектам и манипуляции стилями.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject;
```

## Step‑by‑step guide to substitute the font

### Step 1: Load your DWG file (load dwg file java)

Сначала укажите API путь к вашему DWG (или DXF) файлу и загрузите его в объект `CadImage`.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage) Image.load(srcFile);
```

> **Pro tip:** Если вы работаете напрямую с DWG файлами, замените расширение `.dxf` на `.dwg` в переменной `srcFile`.

### Step 2: Iterate over the style table and set primary font name

Каждый CAD‑чертеж содержит коллекцию объектов стилей. Пройдитесь по ним и используйте метод `setPrimaryFontName` (API‑вызов, который **устанавливает основной шрифт**) для замены шрифта.

```java
for(Object style : cadImage.getStyles())
{
    // Set the font name
    ((com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject)style).setPrimaryFontName("Arial");
}
```

Вы можете изменить `"Arial"` на любой шрифт, установленный на машине, где выполняется код.

### Step 3: Save the modified drawing

После обновления шрифта запишите изменения в новый DWG файл (или перезапишите оригинал).

```java
cadImage.save(dataDir + "output.dwg", new DwgOptions());
```

Сохранённый файл теперь использует указанный вами шрифт, и любые текстовые аннотации будут отображаться этим типом шрифта.

## Common Issues and Solutions

| Issue | Solution |
|-------|----------|
| **Font not applied** | Убедитесь, что шрифт установлен в ОС и название написано точно. |
| **`Image.load` throws an exception** | Проверьте правильность пути к файлу и то, что файл поддерживается форматом DWG/DXF. |
| **Performance slowdown on large files** | Обрабатывайте файлы в отдельном потоке или пакетно, чтобы избежать блокировки UI. |

## FAQ's

### Q1: Can I revert font substitutions in my DWG file?

A1: Yes, you can revert font substitutions by reloading the original DWG file or using the undo functionality within your CAD software.

### Q2: Are there any limitations to font substitutions in Aspose.CAD for Java?

A2: Font substitution capabilities depend on the fonts available in the system. Ensure the desired font is accessible or consider embedding it in the DWG file.

### Q3: How can I handle font size adjustments during substitution?

A3: Font size adjustments can be made by accessing the style properties within Aspose.CAD and modifying the font size accordingly.

### Q4: Can I automate font substitution in a batch process?

A4: Yes, Aspose.CAD for Java supports batch processing. You can automate font substitutions across multiple DWG files using scripting or programming.

### Q5: Is Aspose.CAD for Java compatible with the latest CAD file formats?

A5: Yes, Aspose.CAD for Java is regularly updated to support the latest CAD file formats, ensuring compatibility with industry standards.

## Frequently Asked Questions

**Q: Does the `setPrimaryFontName` method affect only text entities?**  
A: It updates the primary font for the style table, which in turn influences all text objects that reference that style.

**Q: Can I use a custom font that is not installed on the system?**  
A: Aspose.CAD relies on the operating system’s font registry. To use a custom font, install it on the machine running the code.

**Q: Is it possible to change the font for a single layer only?**  
A: Yes, you can filter styles by layer name before calling `setPrimaryFontName`.

**Q: What version of Aspose.CAD is required for DWG 2022 files?**  
A: The latest release (as of 2025) fully supports DWG 2022. Always check the release notes for specific format support.

**Q: How do I handle licensing in a development environment?**  
A: Use a temporary evaluation license for testing. For production, embed your purchased license file using `License.setLicense("Aspose.Total.Java.lic");`.

---

**Last Updated:** 2025-12-28  
**Tested With:** Aspose.CAD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}