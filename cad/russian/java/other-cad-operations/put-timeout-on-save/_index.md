---
date: 2026-06-19
description: Узнайте, как установить тайм‑аут при сохранении чертежей CAD с Aspose.CAD
  для Java. Повышайте производительность, избегайте зависаний и эффективно экспортируйте
  CAD в PDF.
keywords:
- how to set timeout
- convert dwg to pdf
- export cad to pdf
linktitle: Установить тайм‑аут при сохранении
schemas:
- author: Aspose
  dateModified: '2026-06-19'
  description: Learn how to set timeout on saving CAD drawings with Aspose.CAD for
    Java. Boost performance, avoid hangs, and export CAD to PDF efficiently.
  headline: How to Set Timeout on Save for CAD with Aspose.CAD
  type: TechArticle
- description: Learn how to set timeout on saving CAD drawings with Aspose.CAD for
    Java. Boost performance, avoid hangs, and export CAD to PDF efficiently.
  name: How to Set Timeout on Save for CAD with Aspose.CAD
  steps:
  - name: Set Source and Output Directories
    text: Ensure you have the correct source and output directories for your CAD drawings.
  - name: Create Interruption Token Source
    text: Initialize an interruption token source to manage interruptions during the
      save operation.
  - name: Load CAD Drawing
    text: The `CadImage` class is Aspose.CAD's core object that represents a CAD drawing
      in memory, offering methods for rendering and conversion.
  - name: Configure Rasterization Options
    text: '`CadRasterizationOptions` specifies how the CAD drawing is rasterized into
      an image. Configure rasterization options for the CAD drawing.'
  - name: Configure PDF Options
    text: '`PdfOptions` defines settings for saving a CAD drawing as a PDF document.
      Set up PDF options with vector rasterization options and the interruption token.'
  - name: Save Drawing with Timeout
    text: Save the CAD drawing to a PDF file with the specified timeout.
  - name: Handle Interruption
    text: '`OperationCanceledException` is thrown when a save operation exceeds the
      specified timeout. Create a thread to handle the save operation and interrupt
      it after a specified timeout.'
  type: HowTo
- questions:
  - answer: Yes, wrap each conversion in its own thread with a separate interruption
      token to enforce per‑file time limits.
    question: Can I use this feature to convert DWG to PDF in a batch job?
  - answer: The timeout mechanism is tied to the `InterruptionTokenSource` and works
      with any format that respects the token, including PDF, PNG, and SVG.
    question: Does the timeout work on all output formats?
  - answer: Aspose.CAD automatically discards incomplete output, so you won’t end
      up with corrupted PDFs.
    question: What happens to partially written files after a timeout?
  - answer: Yes, a valid Aspose.CAD license is required for commercial deployments;
      a free trial is available for evaluation.
    question: Is a license required for production use?
  - answer: The official Aspose.CAD documentation provides additional code snippets
      and best‑practice guidelines.
    question: Where can I find more examples of using interruption tokens?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Как установить тайм‑аут при сохранении CAD с Aspose.CAD
url: /ru/java/other-cad-operations/put-timeout-on-save/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Как установить тайм‑аут при сохранении CAD с Aspose.CAD

## Введение

В этом всестороннем руководстве вы узнаете **как установить тайм‑аут** при сохранении чертежей CAD с использованием Aspose.CAD для Java. Применение тайм‑аута предотвращает зависание длительных операций сохранения вашего приложения, что особенно важно, когда необходимо **экспортировать CAD в PDF** или **конвертировать DWG в PDF** в сценариях пакетной обработки. Aspose.CAD для Java поддерживает более 50 форматов CAD и может обрабатывать файлы со сотнями страниц без загрузки всего документа в память, обеспечивая предсказуемую производительность и использование ресурсов.

## Быстрые ответы
- **Что делает тайм‑аут?** Он прерывает операцию сохранения после указанного периода, освобождая поток и предотвращая утечки ресурсов.  
- **Какой класс управляет тайм‑аутом?** `InterruptionTokenSource` предоставляет токен отмены, используемый процедурой сохранения.  
- **Могу ли я всё ещё экспортировать CAD в PDF после тайм‑аута?** Да — вы можете перехватить исключение прерывания и повторить попытку или записать ошибку в журнал.  
- **Нужна ли специальная лицензия?** Обычной лицензии Aspose.CAD достаточно; функция тайм‑аута встроена.  
- **Является ли этот подход потокобезопасным?** Да, когда каждое сохранение выполняется в отдельном потоке со своим токеном.

## Что такое тайм‑аут в операциях сохранения CAD?

Тайм‑аут — это настраиваемый временной лимит, который при превышении принудительно останавливает процесс сохранения и генерирует исключение прерывания. Это защищает ваше Java‑приложение от бесконечных зависаний, вызванных сложными чертежами или узкими местами ввода‑вывода.

## Зачем устанавливать тайм‑аут при сохранении файлов CAD?

Aspose.CAD может **конвертировать DWG в PDF** и **экспортировать CAD в PDF** менее чем за секунду для типичных чертежей, но чрезвычайно большие или повреждённые файлы могут занимать минуты. Определяя тайм‑аут, вы гарантируете, что любое отдельное сохранение не превысит, например, 30 секунд, поддерживая стабильную пропускную способность пакетной обработки и предотвращая истощение потоков.

## Требования

Прежде чем приступить к руководству, убедитесь, что у вас есть следующие предварительные условия:
- **Aspose.CAD for Java Library** – Убедитесь, что библиотека Aspose.CAD for Java интегрирована в ваш проект. Вы можете скачать библиотеку с [веб‑сайта](https://releases.aspose.com/cad/java/).
- **Development Environment** – Настройте вашу среду разработки Java со всеми необходимыми инструментами и зависимостями.

## Импорт пакетов

Чтобы начать, импортируйте необходимые пакеты в ваш Java‑проект. Добавьте следующие строки в начало вашего Java‑файла:

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterruptionTokenSource;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.concurrent.TimeUnit;
```

Теперь разберём пример кода пошагово:

## Как установить тайм‑аут при сохранении чертежей CAD?

Загрузите ваш CAD‑файл, создайте `InterruptionTokenSource` с нужным тайм‑аутом и передайте токен в параметры сохранения PDF. Если операция превысит тайм‑аут, Aspose.CAD бросит `OperationCanceledException`, который вы можете перехватить для корректной обработки сбоя.

### Шаг 1: Установите каталоги источника и вывода

```java
final String SourceDir = Utils.getDataDir_DWGDrawings();
final String OutputDir = Utils.getDataDir_Output();
```

Убедитесь, что указали правильные каталоги источника и вывода для ваших CAD‑чертежей.

### Шаг 2: Создайте источник токена прерывания

```java
final InterruptionTokenSource source = new com.aspose.cad.InterruptionTokenSource();
```

Инициализируйте источник токена прерывания для управления прерываниями во время операции сохранения.

### Шаг 3: Загрузите CAD‑чертёж

Класс `CadImage` — основной объект Aspose.CAD, представляющий CAD‑чертёж в памяти, предоставляющий методы для рендеринга и конвертации.

```java
final CadImage cadImageBig = (CadImage)Image.load(SourceDir + "Drawing11.dwg");
```

### Шаг 4: Настройте параметры растеризации

`CadRasterizationOptions` определяет, как CAD‑чертёж растеризуется в изображение.

```java
CadRasterizationOptions rasterizationOptionsBig = new CadRasterizationOptions();
rasterizationOptionsBig.setPageWidth(cadImageBig.getSize().getWidth() / 2);
rasterizationOptionsBig.setPageHeight(cadImageBig.getSize().getHeight() / 2);
```

Настройте параметры растеризации для CAD‑чертежа.

### Шаг 5: Настройте параметры PDF

`PdfOptions` определяет настройки для сохранения CAD‑чертежа в виде PDF‑документа.

```java
final PdfOptions CADfBig = new PdfOptions();
CADfBig.setVectorRasterizationOptions(rasterizationOptionsBig);
CADfBig.setInterruptionToken(source.getToken());
```

Настройте параметры PDF с параметрами векторной растеризации и токеном прерывания.

### Шаг 6: Сохраните чертёж с тайм‑аутом

```java
cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
```

Сохраните CAD‑чертёж в PDF‑файл с указанным тайм‑аутом.

### Шаг 7: Обработайте прерывание

`OperationCanceledException` выбрасывается, когда операция сохранения превышает указанный тайм‑аут.

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

Создайте поток для выполнения операции сохранения и прервите его после заданного тайм‑аута.

## Распространённые проблемы и решения

- **Тайм‑аут слишком короткий** – Если вы получаете частые прерывания, увеличьте значение тайм‑аута, чтобы учесть более крупные чертежи.  
- **InterruptedException не перехвачен** – Всегда оборачивайте вызов сохранения в блок try‑catch для `OperationCanceledException`, чтобы предотвратить падение приложения.  
- **Потребление памяти** – Используйте `PdfOptions.setVectorRasterizationOptions` для потоковой передачи вывода вместо загрузки всего файла в память.

## Часто задаваемые вопросы

**Q: Могу ли я использовать эту функцию для конвертации DWG в PDF в пакетной задаче?**  
A: Да, оберните каждую конвертацию в отдельный поток с отдельным токеном прерывания, чтобы применять ограничения времени для каждого файла.

**Q: Работает ли тайм‑аут со всеми форматами вывода?**  
A: Механизм тайм‑аута привязан к `InterruptionTokenSource` и работает с любым форматом, который учитывает токен, включая PDF, PNG и SVG.

**Q: Что происходит с частично записанными файлами после тайм‑аута?**  
A: Aspose.CAD автоматически удаляет неполный вывод, поэтому вы не получите повреждённые PDF‑файлы.

**Q: Требуется ли лицензия для использования в продакшене?**  
A: Да, для коммерческих развертываний требуется действующая лицензия Aspose.CAD; бесплатная пробная версия доступна для оценки.

**Q: Где можно найти больше примеров использования токенов прерывания?**  
A: Официальная документация Aspose.CAD предоставляет дополнительные фрагменты кода и рекомендации по лучшим практикам.

## Дополнительные ресурсы

- [releases page](https://releases.aspose.com/cad/java/) – Прямая страница загрузки последних выпусков Aspose.CAD для Java.  
- [documentation](https://reference.aspose.com/cad/java/) – Полная ссылка на API и руководства разработчика.  
- [this link](https://releases.aspose.com/) – Общие релизы продуктов Aspose.  
- [here](https://purchase.aspose.com/temporary-license/) – Получить временную лицензию для тестирования.  
- [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) – Поддержка сообщества и обсуждения.

## Заключение

Теперь вы освоили **как установить тайм‑аут** при сохранении CAD‑чертежей с Aspose.CAD для Java. Интегрируя `InterruptionTokenSource` в ваш рабочий процесс, вы можете надёжно **экспортировать CAD в PDF** или **конвертировать DWG в PDF** без риска длительных зависаний, поддерживая отзывчивость и масштабируемость вашего приложения.

---

**Последнее обновление:** 2026-06-19  
**Тестировано с:** Aspose.CAD for Java 24.12  
**Автор:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Связанные руководства

- [Экспорт DWG в PDF или растеризованный формат с использованием Aspose.CAD для Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Экспорт конкретного макета DWG в PDF с использованием Aspose.CAD для Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Конвертация DWG в PNG и другие растерные форматы с использованием Aspose.CAD для Java](/cad/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}