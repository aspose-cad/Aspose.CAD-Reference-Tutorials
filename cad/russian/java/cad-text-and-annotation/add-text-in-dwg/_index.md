---
date: 2025-12-28
description: Узнайте, как создать PDF из DWG, сохранить DWG в PDF и добавить текст
  к чертежам DWG с помощью Aspose.CAD for Java — пошаговое руководство.
linktitle: Add Text in DWG
second_title: Aspose.CAD Java API
title: Создание PDF из DWG и добавление текста с помощью Aspose.CAD для Java
url: /ru/java/cad-text-and-annotation/add-text-in-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Создать PDF из DWG и добавить текст с помощью Aspose.CAD for Java

## Введение

Если вам нужно **создать PDF из DWG** файлов и одновременно вставить пользовательский текст, вы попали по адресу. В этом руководстве мы пройдем весь процесс — загрузка чертежа DWG, добавление текстовой аннотации и, наконец, сохранение результата в виде PDF с помощью Aspose.CAD for Java. К концу вы поймёте, как **сохранить DWG как PDF**, настроить высоту текста и даже добавить базовые аннотации.

## Быстрые ответы
- **Могу ли я конвертировать DWG в PDF на Java?** Да, Aspose.CAD for Java предоставляет простой API.  
- **Нужна ли лицензия для использования в продакшене?** Требуется коммерческая лицензия; доступна бесплатная пробная версия.  
- **Какой метод добавляет текст в DWG?** Используйте объект `CadText` и добавьте его в модельное пространство.  
- **Можно ли задать высоту текста?** Конечно — вызовите `setTextHeight()` у экземпляра `CadText`.  
- **Является ли вывод векторным?** При установке параметров растеризации в `UseObjectColor` PDF сохраняет высококачественные векторные данные.

## Предварительные требования

Прежде чем приступить к руководству, убедитесь, что у вас есть следующее:

- Библиотека Aspose.CAD for Java: загрузите и установите библиотеку со страницы [страница Aspose.CAD for Java](https://releases.aspose.com/cad/java/).

- Java Development Kit (JDK): убедитесь, что на вашей системе установлен последний JDK.

- DWG‑чертёж: подготовьте файл DWG, в который вы хотите добавить текст.

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

Теперь разберём предоставленный фрагмент кода на несколько шагов:

## Шаг 1: Настройте каталог документа и путь к файлу DWG

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String dwgPathToFile = dataDir + "SimpleEntites.dwg";
```

## Шаг 2: Загрузите изображение DWG

```java
Image image = Image.load(dwgPathToFile);
```

## Шаг 3: Создайте объект CadText (добавьте текст в DWG)

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

## Шаг 4: Добавьте текст в CadImage (вставьте аннотацию)

```java
CadImage cadImage = ((CadImage)(image));
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(cadText);
```

## Шаг 5: Настройте параметры PDF (подготовка к созданию PDF из DWG)

```java
PdfOptions pdfOptions = new PdfOptions();
```

## Шаг 6: Настройте CadRasterizationOptions (управление рендерингом PDF)

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

## Шаг 7: Сохраните изменённый DWG как PDF (dwg в pdf java)

```java
image.save(dataDir + "SimpleEntites_generated.dwg.pdf", pdfOptions);
```

Следуя этим шагам, вы сможете **создать PDF из DWG**, добавить пользовательский текст и управлять высотой текста — всё это с помощью нескольких строк кода на Java.

## Зачем добавлять текст в DWG и конвертировать в PDF?

Добавление текста непосредственно в файл DWG полезно для:

- **Разметка дизайнов** с примечаниями или номерами деталей.  
- **Создание печатной документации**, где PDF служит как только для чтения, широко поддерживаемый формат.  
- **Автоматизация пакетной обработки** больших библиотек CAD без ручного редактирования.

## Распространённые проблемы и советы

- **Текст не отображается?** Проверьте, что координаты X/Y находятся в пределах границ чертежа и что слой видим.  
- **Неправильная высота текста?** Отрегулируйте `setTextHeight()`; значение задаётся в системе единиц чертежа.  
- **PDF выглядит растровым?** Убедитесь, что `CadDrawTypeMode.UseObjectColor` установлен для сохранения векторной информации.  
- **Производительность при больших файлах?** Увеличивайте `pageHeight`/`pageWidth` только при необходимости; большие значения потребляют больше памяти.

## Часто задаваемые вопросы

**В: Совместим ли Aspose.CAD со всеми версиями файлов DWG?**  
О: Aspose.CAD поддерживает различные версии файлов DWG, обеспечивая совместимость с широким спектром CAD‑программ.

**В: Могу ли я настроить шрифт и форматирование добавленного текста?**  
О: Да, вы можете настроить шрифт, стиль и другие параметры форматирования текста, добавляемого в файлы DWG с помощью Aspose.CAD.

**В: Доступна ли бесплатная пробная версия Aspose.CAD for Java?**  
О: Да, вы можете ознакомиться с возможностями Aspose.CAD, получив бесплатную пробную версию [здесь](https://releases.aspose.com/).

**В: Где я могу найти подробную документацию по Aspose.CAD for Java?**  
О: Обратитесь к документации [здесь](https://reference.aspose.com/cad/java/) для получения подробной информации и примеров.

**В: Как я могу получить поддержку или помощь по Aspose.CAD?**  
О: Посетите [форум Aspose.CAD](https://forum.aspose.com/c/cad/19), чтобы получить помощь и связаться с сообществом.

---

**Последнее обновление:** 2025-12-28  
**Тестировано с:** Aspose.CAD for Java 24.12  
**Автор:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}