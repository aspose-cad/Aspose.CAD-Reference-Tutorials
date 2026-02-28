---
date: 2026-02-28
description: Узнайте, как создавать PDF из DWG, сохранять DWG в PDF и добавлять текст
  к чертежам DWG с помощью Aspose.CAD для Java — пошаговое руководство.
linktitle: Add Text in DWG
second_title: Aspose.CAD Java API
title: Создание PDF из DWG и добавление текста с помощью Aspose.CAD для Java
url: /ru/java/cad-text-and-annotation/add-text-in-dwg/
weight: 10
---

 Q&A.

Let's craft.

Be careful with bullet list formatting.

Also note "step-by-step in order". We'll translate each section.

Let's produce final content.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Создание PDF из DWG и добавление текста с помощью Aspose.CAD for Java

## Введение

Если вам нужно **создать PDF из файлов DWG**, одновременно вставив пользовательский текст, вы попали по адресу. В этом руководстве мы пройдем весь процесс — загрузка чертежа DWG, добавление текстовой аннотации и окончательное сохранение результата в PDF с помощью Aspose.CAD for Java. К концу вы поймёте, как **сохранить DWG как PDF**, настроить высоту текста и даже добавить базовые аннотации.

## Быстрые ответы
- **Можно ли конвертировать DWG в PDF на Java?** Да, Aspose.CAD for Java предоставляет простой API.  
- **Нужна ли лицензия для использования в продакшене?** Требуется коммерческая лицензия; доступна бесплатная пробная версия.  
- **Какой метод добавляет текст в DWG?** Используйте объект `CadText` и добавьте его в модельное пространство.  
- **Можно ли задать высоту текста?** Конечно — используйте `setTextHeight()` у экземпляра `CadText`.  
- **Является ли результат векторным?** При установке параметров растеризации в `UseObjectColor` PDF сохраняет высококачественные векторные данные.

## Что означает «создание PDF из DWG»?
Создание PDF из чертежа DWG означает преобразование родного формата CAD в широко поддерживаемый документ только для чтения, при этом сохраняется оригинальная геометрия. Такая конверсия необходима, когда нужно поделиться проектами со сторонами, у которых нет CAD‑программ.

## Почему стоит использовать Aspose.CAD for Java для конвертации DWG в PDF?
Aspose.CAD предлагает чисто Java‑решение, не требующее установки внешних CAD‑приложений. Он поддерживает **convert DWG to PDF**, сохраняет векторную точность и позволяет программно добавлять аннотации, такие как текст, размеры или пользовательскую графику, перед конвертацией.

## Предварительные требования

Прежде чем приступить к руководству, убедитесь, что у вас есть следующее:

- Библиотека Aspose.CAD for Java: скачайте и установите её со страницы [Aspose.CAD for Java page](https://releases.aspose.com/cad/java/).

- Java Development Kit (JDK): убедитесь, что на системе установлен последний JDK.

- DWG‑чертёж: подготовьте файл DWG, в который хотите добавить текст.

## Импорт пространств имён

В вашем Java‑коде импортируйте необходимые пространства имён для Aspose.CAD:

```java
import com.aspose.cad.Image;


import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Теперь разберём предоставленный фрагмент кода по нескольким шагам:

## Шаг 1: Настройка каталога документа и пути к файлу DWG

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String dwgPathToFile = dataDir + "SimpleEntites.dwg";
```

## Шаг 2: Загрузка изображения DWG

```java
Image image = Image.load(dwgPathToFile);
```

## Шаг 3: Создание объекта CadText (добавление текста в DWG)

```java
CadText cadText = new CadText();
cadText.setStyleType("Standard");
cadText.setDefaultValue("Some custom text");
cadText.setColorId(256);
cadText.setLayerName("0");
cadText.getFirstAlignment().setX(47.9);
cadText.getFirstAlignment().setY(5.56);
cadText.setTextHeight(0.8);          // set text height in DWG units
cadText.setScaleX(0);
```

## Шаг 4: Добавление текста в CadImage (вставка аннотации)

```java
CadImage cadImage = ((CadImage)(image));
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(cadText);
```

## Шаг 5: Настройка параметров PDF (подготовка к созданию PDF из DWG)

```java
PdfOptions pdfOptions = new PdfOptions();
```

## Шаг 6: Конфигурация CadRasterizationOptions (управление рендерингом PDF)

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

## Шаг 7: Сохранение изменённого DWG как PDF (dwg to pdf java)

```java
image.save(dataDir + "SimpleEntites_generated.dwg.pdf", pdfOptions);
```

Следуя этим шагам, вы сможете **create PDF from DWG**, добавить пользовательский текст и управлять высотой текста — всё это с помощью нескольких строк кода на Java.

## Как конвертировать DWG в PDF на Java в масштабе?
Если требуется **batch convert DWG PDF** файлов, оберните приведённый код в цикл, проходящий по папке с DWG‑чертежами. Регулируйте `pageHeight`/`pageWidth` только при необходимости, чтобы снизить потребление памяти, и переиспользуйте один экземпляр `PdfOptions` для каждого файла — это повысит производительность.

## Распространённые проблемы и советы

- **Текст не отображается?** Проверьте, что координаты X/Y находятся внутри границ чертежа и что слой видим.
- **Неправильная высота текста?** Скорректируйте `setTextHeight()`; значение задаётся в системе единиц чертежа.
- **PDF выглядит растровым?** Убедитесь, что установлен `CadDrawTypeMode.UseObjectColor` для сохранения векторной информации.
- **Производительность при работе с большими файлами?** Увеличивайте `pageHeight`/`pageWidth` только при необходимости; большие значения требуют больше памяти.

## Часто задаваемые вопросы

**В: Совместим ли Aspose.CAD со всеми версиями файлов DWG?**  
О: Aspose.CAD поддерживает различные версии DWG, обеспечивая совместимость с широким спектром CAD‑программ.

**В: Можно ли настроить шрифт и форматирование добавляемого текста?**  
О: Да, вы можете менять шрифт, стиль и другие параметры форматирования текста, добавляемого в DWG, используя Aspose.CAD.

**В: Доступна ли бесплатная пробная версия Aspose.CAD for Java?**  
О: Да, вы можете ознакомиться с возможностями Aspose.CAD, получив бесплатную пробную версию [здесь](https://releases.aspose.com/).

**В: Где найти подробную документацию по Aspose.CAD for Java?**  
О: Обратитесь к документации [здесь](https://reference.aspose.com/cad/java/) для получения детальной информации и примеров.

**В: Как получить поддержку или помощь по Aspose.CAD?**  
О: Посетите форум [Aspose.CAD forum](https://forum.aspose.com/c/cad/19), где можно задать вопросы и связаться с сообществом.

---

**Последнее обновление:** 2026-02-28  
**Тестировано с:** Aspose.CAD for Java 24.12  
**Автор:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}