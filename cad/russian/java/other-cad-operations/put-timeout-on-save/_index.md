---
title: Тайм-аут сохранения для САПР с помощью Aspose.CAD
linktitle: Поставьте таймаут на сохранение
second_title: API Aspose.CAD Java
description: Узнайте, как повысить производительность вашего Java-приложения с помощью Aspose.CAD. Установите тайм-аут для сохранения чертежей САПР. Следуйте нашему пошаговому руководству.
weight: 15
url: /ru/java/other-cad-operations/put-timeout-on-save/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Тайм-аут сохранения для САПР с помощью Aspose.CAD

## Введение

Добро пожаловать в руководство по установке тайм-аута при сохранении с использованием Aspose.CAD для Java. В этом руководстве мы покажем вам процесс установки времени ожидания для сохранения чертежей САПР, чтобы повысить производительность вашего приложения. Aspose.CAD for Java — это мощная библиотека, которая позволяет вам легко работать с файлами САПР в ваших приложениях Java.

## Предварительные условия

Прежде чем приступить к изучению руководства, убедитесь, что у вас есть следующие предварительные условия:
-  Библиотека Aspose.CAD for Java: убедитесь, что в ваш проект интегрирована библиотека Aspose.CAD for Java. Вы можете скачать библиотеку с сайта[Веб-сайт](https://releases.aspose.com/cad/java/).
- Среда разработки: настройте среду разработки Java со всеми необходимыми инструментами и зависимостями.

## Импортировать пакеты

Для начала импортируйте необходимые пакеты в свой Java-проект. Добавьте следующие строки в начало вашего Java-файла:

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterruptionTokenSource;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.concurrent.TimeUnit;
```

Теперь давайте разобьем пример кода на пошаговые инструкции:

## Шаг 1. Установите исходный и выходной каталоги

```java
final String SourceDir = Utils.getDataDir_DWGDrawings();
final String OutputDir = Utils.getDataDir_Output();
```

Убедитесь, что у вас есть правильные исходные и выходные каталоги для ваших чертежей САПР.

## Шаг 2. Создайте источник токена прерывания

```java
final InterruptionTokenSource source = new com.aspose.cad.InterruptionTokenSource();
```

Инициализируйте источник токена прерывания, чтобы управлять прерываниями во время операции сохранения.

## Шаг 3. Загрузите чертеж САПР

```java
final CadImage cadImageBig = (CadImage)Image.load(SourceDir + "Drawing11.dwg");
```

 Загрузите чертеж САПР в`CadImage` объект.

## Шаг 4. Настройте параметры растеризации

```java
CadRasterizationOptions rasterizationOptionsBig = new CadRasterizationOptions();
rasterizationOptionsBig.setPageWidth(cadImageBig.getSize().getWidth() / 2);
rasterizationOptionsBig.setPageHeight(cadImageBig.getSize().getHeight() / 2);
```

Настройте параметры растеризации для чертежа САПР.

## Шаг 5. Настройте параметры PDF

```java
final PdfOptions CADfBig = new PdfOptions();
CADfBig.setVectorRasterizationOptions(rasterizationOptionsBig);
CADfBig.setInterruptionToken(source.getToken());
```

Настройте параметры PDF с параметрами векторной растеризации и маркером прерывания.

## Шаг 6. Сохраните рисунок с тайм-аутом

```java
cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
```

Сохраните чертеж САПР в файл PDF с указанным временем ожидания.

## Шаг 7: Обработка прерываний

```java
java.lang.Thread thread = new java.lang.Thread(new Runnable() {
    @Override
    public void run() {
        try {
            cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
        } catch (Throwable th) {
            System.out.println("interrupted !!!");
        }
    }
});
thread.start();
TimeUnit.SECONDS.sleep(3);
source.interrupt();
thread.join();
```

Создайте поток для обработки операции сохранения и прервите ее по истечении заданного времени ожидания.

## Заключение

Поздравляем! Вы успешно научились устанавливать таймаут при сохранении с помощью Aspose.CAD для Java. Эта функция может значительно повысить эффективность ваших приложений, связанных с САПР.

## Часто задаваемые вопросы

### Вопрос 1: Как загрузить Aspose.CAD для Java?

 A1: Вы можете скачать его с[страница релизов](https://releases.aspose.com/cad/java/).

### Вопрос 2. Где я могу найти документацию по Aspose.CAD для Java?

 A2: См.[документация](https://reference.aspose.com/cad/java/) для получения исчерпывающей информации.

### В3: Есть ли бесплатная пробная версия?

О3: Да, вы можете получить бесплатную пробную версию на сайте[эта ссылка](https://releases.aspose.com/).

### Вопрос 4: Как получить временную лицензию?

 А4: Посетите[здесь](https://purchase.aspose.com/temporary-license/) для получения информации о временной лицензии.

### В5: Нужна помощь или есть вопросы?

 A5: Отправляйтесь в[Форум Aspose.CAD](https://forum.aspose.com/c/cad/19) для поддержки сообщества.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
