---
date: 2026-01-22
description: Узнайте, как установить тайм‑аут при сохранении CAD в PDF с помощью Aspose.CAD
  для Java. Повышайте производительность с этим пошаговым руководством.
linktitle: Put Timeout on Save
second_title: Aspose.CAD Java API
title: Как установить тайм‑аут при сохранении CAD с Aspose.CAD
url: /ru/java/other-cad-operations/put-timeout-on-save/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Тайм‑аут при сохранении CAD с Aspose.CAD

## Введение

Добро пожаловать в руководство по **установке тайм‑аута** при сохран тайм‑аут?** Он прерывает операцию сохраненияая длительные зависания.  
- **Какой формат используется в примере?** Чертёж CAD сохраняется в файл PDF.  
- **Нужна ли лицензия?** Для использования в продакшене требуется временная или постоянная лицензия Aspose.CAD.  
- **Какая версия Java поддерживается?** Код работает с Java 8 им‑аут при сохранении

### Что такое тайм‑аут в контексте Aspose.CAD?
Тайм‑аут — это механизм защиты, который останавливает длительный процесс растеризации или конвертации. Предоставив `InterruptionTokenSource`, вы можете сигнализировать библиотеке прервать операцию после заданного периода, обеспечивая тайм‑аут при сохранении CAD в PDF?
Сохранение больших или сложных чертежей CAD может потреблять значительные ресурсы CPU и памяти. Добавление тайм‑аута:
- Предотвращает зависание приложения.  
- Позволяет корректно обрабатывать длительные задачи.  
- Улучшает общий пользовательский опыт, особенно в веб‑ или UI‑ориентированных средах.

## Требования

- **Aspose.CAD for Java Library** – Убедитесь, что библиотека интегрирована в ваш проект. Вы можете скачать библиотеку с [веб‑сайта](https://releases.aspose.com/cad/java/).  
- **Среда разработки** – Java IDE (IntelliJ, Eclipse и др.) с установленным JDK 8+.

## Импорт пакетов

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterruptionTokenSource;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.concurrent.TimeUnit;
```

Теперь разберём пример кода пошагово:

## Шаг 1: Установите каталоги исходных и выходных файлов

```java
final String SourceDir = Utils.getDataDir_DWGDrawings();
final String OutputDir = Utils.getDataDir_Output();
```

Убедитесь, что указали правильные каталоги исходных и выходных файлов для ваших чертежей CAD.

## Шаг 2: Создайте Interruption Token Source

```java
final InterruptionTokenSource source = new com.aspose.cad.InterruptionTokenSource();
```

Инициализируйте источник токена прерывания для управления прерываниями во время операции сохранения.

## Шаг 3: Загрузите чертёж CAD

```java
final CadImage cadImageBig = (CadImage)Image.load(SourceDir + "Drawing11.dwg");
```

Загрузите чертёж CAD в объект `CadImage`.

## Шаг 4: Настройте параметры растеризации

```java
CadRasterizationOptions rasterizationOptionsBig = new CadRasterizationOptions();
rasterizationOptionsBig.setPageWidth(cadImageBig.getSize().getWidth() / 2);
rasterizationOptionsBig.setPageHeight(cadImageBig.getSize().getHeight() / 2);
```

Настройте параметры растеризации для чертежа CAD.

## Шаг 5: Настройте параметры PDF

```java
final PdfOptions CADfBig = new PdfOptions();
CADfBig.setVectorRasterizationOptions(rasterizationOptionsBig);
CADfBig.setInterruptionToken(source.getToken());
```

Настройте параметры PDF с параметрами векторной растеризации и токеном прерывания.

## Шаг 6: Сохраните чертёж с тайм‑аутом

```java
cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
```

Сохраните чертёж CAD в файл PDF с указанным тайм‑аутом.

## Шаг 7: Обработайте прерывание

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

Создайте поток для выполнения операции сохранения и прервите её после заданного тайм‑аута.

## Распространённые ошибки и устранение неполадок

- **Тайм‑аут слишком короткий** – Если чертёж большой, очень короткий тайм‑аут может прервать операцию до её завершения. Увеличьте длительность сна или скорректируйте параметры растеризации.  
- **Отсутствует лицензия** – Запуск без действующей лицензии вызовет исключение. Примените временную или постоянную лицензию перед выполнением кода.  
- **Неправильные пути** – Убедитесь, что `SourceDir` и `OutputDir` указывают на существующие папки; иначе `Image.load` или `save` завершатся с ошибкой.

## Часто задаваемые вопросы

**В: Как скачать Aspose.CAD for Java?**  
О: Вы можете скачать её со [страницы релизов](https://releases.aspose.com/cad/java/).

**В: Где найти документацию по Aspose.CAD for Java?**  
О: Обратитесь к [документации](https://reference.aspose.com/cad/java/) для получения полной информации.

**В: Доступна ли бесплатная пробная версия?**  
О: Да, вы можете получить бесплатную пробную версию по [этой ссылке](https://releases.aspose.com/).

**В: Как получить временную лицензию?**  
О: Перейдите [сюда](https://purchase.aspose.com/temporary-license/) для получения информации о временной лицензии.

**В: Нужна помощь или есть вопросы?**  
О: Перейдите на [форум Aspose.CAD](https://forum.aspose.com/c/cad/19) для получения поддержки от сообщества.

## Заключение

Поздравляем! Теперь вы знаете **как установить тайм‑аут** для операций сохранения при конвертации чертежей CAD в PDF с использованием Aspose.CAD for Java. Реализация этого тайм‑аута повышает надёжность и отзывчивость ваших приложений, связанных с CAD.

---

**Последнее обновление:** 2026-01-22  
**Тестировано с:** Aspose.CAD for Java 24.11 (latest)  
**Автор:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}