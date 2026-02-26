---
date: 2026-01-10
description: Узнайте, как экспортировать DGN в DWG и конвертировать MicroStation DGN
  в AutoCAD DWG с помощью Aspose.CAD для Java. Пошаговое руководство.
linktitle: Export DGN as Part of DWG
second_title: Aspose.CAD Java API
title: Экспорт DGN в DWG с помощью Aspose.CAD для Java
url: /ru/java/dgn-export-options/export-dgn-as-part-of-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Экспорт DGN в DWG с помощью Aspose.CAD для Java

## Введение

В этом руководстве вы узнаете, как **экспортировать dgn в dwg** и встроить дизайн MicroStation DGN в файл AutoCAD DWG с помощью библиотеки Aspose.CAD для Java. Независимо от того, переносите ли вы устаревшие чертежи MicroStation или хотите комбинировать DGN‑подложки с DWG‑макетами, данное руководство проведёт вас через каждый шаг — от настройки окружения до создания PDF‑предпросмотра готового DWG.

## Быстрые ответы
- **Что достигается при “экспорте dgn в dwg”?** Встраивается подложка DGN в DWG, обеспечивая бесшовный просмотр в AutoCAD.
- **В какой формат можно экспортировать результат для быстрого просмотра?** Вы можете **экспортировать CAD‑файл в pdf** с помощью `PdfOptions`.
- **Нужна ли лицензия для запуска кода?** Для использования в продакшене требуется временная или платная лицензия Aspose.CAD.
- **Какая версия Java поддерживается?** Java 8 и выше работают с последним выпуском Aspose.CAD для Java.
- **Есть ли бесплатная пробная версия?** Да — загрузите пробную версию с сайта Aspose.

## Что такое “экспорт dgn в dwg”?
Экспорт DGN в DWG означает преобразование или встраивание дизайна MicroStation DGN в виде подложки внутри чертежа AutoCAD DWG. Это позволяет специалистам CAD использовать существующие DGN‑активы без необходимости заново создавать геометрию.

## Почему преобразовывать MicroStation DGN в AutoCAD DWG?
- **Сотрудничество:** Команды, использующие AutoCAD, могут напрямую просматривать и редактировать содержимое DGN.
- **Стандартизация:** DWG является де‑факто форматом для многих последующих процессов (например, генерация PDF, 3D‑рендеринг).
- **Сохранение:** Оригинальные ссылки DGN остаются нетронутыми, уменьшая риск потери данных.

## Предварительные требования

Прежде чем приступить к руководству, убедитесь, что у вас есть следующие компоненты:
1. **Библиотека Aspose.CAD:** Скачайте и установите библиотеку Aspose.CAD для Java. Библиотеку можно найти [здесь](https://releases.aspose.com/cad/java/).
2. **Java Development Kit (JDK):** Убедитесь, что Java установлена в вашей системе.
3. **Интегрированная среда разработки (IDE):** Выберите Java‑IDE, например Eclipse или IntelliJ, для более комфортной разработки.

## Импорт пакетов

В вашем Java‑проекте импортируйте необходимые пакеты Aspose.CAD для работы с CAD‑файлами. Пример:

```java
import com.aspose.cad;
import com.aspose.cad.imageoptions;
import com.aspose.cad.fileformats.cad.cadconsts;
import com.aspose.cad.fileformats.cad;
import com.aspose.cad.fileformats.cad.cadobjects;
```

## Шаг 1: Установка путей к файлам

Определите входные и выходные пути к файлу DWG. Обновите переменные `dataDir`, `fileName` и `outPath` соответственно.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
String outPath = dataDir + "BlockRefDgn.dwg.pdf";
```

## Шаг 2: Создание экземпляра PdfOptions

Создайте экземпляр класса `PdfOptions`, так как мы **экспортируем CAD‑файл в PDF** для быстрой проверки.

```java
PdfOptions exportOptions = new PdfOptions();
```

## Шаг 3: Загрузка файла DWG

Загрузите существующий файл DWG как изображение и преобразуйте его в тип `CadImage`.

```java
CadImage cadImage = (CadImage) Image.load(fileName);
```

## Шаг 4: Перебор сущностей

Пройдитесь по каждой сущности внутри DWG и проверьте, является ли она определением изображения. Если да, получите внешнюю ссылку на объект.

```java
for (CadBaseEntity baseEntity : cadImage.getEntities()) {
    if (baseEntity.getTypeName() == CadEntityTypeName.DGNUNDERLAY) {
        CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
        System.out.println(dgnFile.getUnderlayPath());
    }
}
```

## Шаг 5: Определение параметров растеризации

Задайте настройки для объекта `CadRasterizationOptions`, включая ширину и высоту страницы, макеты и цвет фона.

```java
CadRasterizationOptions vectorRasterizationOptions = new CadRasterizationOptions();
vectorRasterizationOptions.setPageWidth(1600);
vectorRasterizationOptions.setPageHeight(1600);
vectorRasterizationOptions.setLayouts(new String[] { "Model" });
vectorRasterizationOptions.setAutomaticLayoutsScaling(false);
vectorRasterizationOptions.setNoScaling(true);
vectorRasterizationOptions.setBackgroundColor(Color.getBlack());
vectorRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
```

## Шаг 6: Установка параметров векторной растеризации

Установите параметры векторной растеризации для экспорта.

```java
exportOptions.setVectorRasterizationOptions(vectorRasterizationOptions);
```

## Шаг 7: Экспорт DWG в PDF

Наконец, экспортируйте DWG в PDF, вызвав метод `save`.

```java
cadImage.save(outPath, exportOptions);
```

## Распространённые проблемы и решения

| Проблема | Причина | Решение |
|----------|---------|---------|
| **Подложка DGN не отображается** | В DWG отсутствует сущность `DGNUNDERLAY`. | Убедитесь, что исходный DWG содержит ссылку на DGN. |
| **PDF пустой** | Параметры растеризации заданы нулевыми или выбран неверный макет. | Проверьте, что `setPageWidth`/`setPageHeight` положительные, а `setLayouts` соответствует имени макета DWG. |
| **Исключение лицензии** | Запуск без действующей лицензии Aspose.CAD. | Примените временную или приобретённую лицензию перед вызовом любых методов API. |

## Часто задаваемые вопросы

### Q1: Где найти документацию по Aspose.CAD для Java?

A1: Документацию можно найти [здесь](https://reference.aspose.com/cad/java/).

### Q2: Как скачать библиотеку Aspose.CAD для Java?

A2: Библиотеку можно скачать по [этой ссылке](https://releases.aspose.com/cad/java/).

### Q3: Есть ли бесплатная пробная версия Aspose.CAD для Java?

A3: Да, бесплатную пробную версию можно получить [здесь](https://releases.aspose.com/).

### Q4: Где получить временную лицензию для Aspose.CAD для Java?

A4: Временную лицензию можно получить [здесь](https://purchase.aspose.com/temporary-license/).

### Q5: Нужна помощь или есть вопросы?

A5: Посетите форум поддержки сообщества Aspose.CAD [здесь](https://forum.aspose.com/c/cad/19).

### Q6: Можно ли преобразовать полученный PDF обратно в DWG?

A6: PDF представляет собой растровый предварительный просмотр; обратное преобразование в DWG требует отдельного инструмента обратного проектирования.

### Q7: Работает ли этот подход с другими CAD‑форматами, например DWF или DXF?

A7: Да, Aspose.CAD поддерживает множество форматов; достаточно изменить расширения файлов и параметры растеризации соответственно.

---

**Последнее обновление:** 2026-01-10  
**Тестировано с:** Aspose.CAD для Java 24.11  
**Автор:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}