---
date: 2026-06-19
description: تعلم كيفية تعيين مهلة عند حفظ رسومات CAD باستخدام Aspose.CAD لـ Java.
  قم بتحسين performance، وتجنب التعطل، وتصدير CAD إلى PDF بكفاءة.
keywords:
- how to set timeout
- convert dwg to pdf
- export cad to pdf
linktitle: تعيين مهلة عند الحفظ
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
title: كيفية تعيين مهلة عند الحفظ لـ CAD باستخدام Aspose.CAD
url: /ar/java/other-cad-operations/put-timeout-on-save/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية تعيين مهلة عند الحفظ لـ CAD باستخدام Aspose.CAD

## مقدمة

في هذا الدليل الشامل ستتعلم **كيفية تعيين مهلة** عند حفظ رسومات CAD باستخدام Aspose.CAD for Java. تطبيق مهلة يمنع عمليات الحفظ الطويلة من تعليق تطبيقك، وهو أمر مهم بشكل خاص عندما تحتاج إلى **export CAD to PDF** أو **convert DWG to PDF** في سيناريوهات المعالجة الدفعية. يدعم Aspose.CAD for Java أكثر من 50 تنسيق CAD ويمكنه التعامل مع ملفات مئات الصفحات دون تحميل المستند بالكامل في الذاكرة، مما يمنحك أداءً متوقعًا واستخدامًا ثابتًا للموارد.

## إجابات سريعة

- **ماذا تفعل المهلة؟** إنها تُلغي عملية الحفظ بعد فترة محددة، وتحرّر الخيط وتمنع تسرب الموارد.  
- **أي فئة تتحكم في المهلة؟** `InterruptionTokenSource` يوفر رمز الإلغاء المستخدم في روتين الحفظ.  
- **هل يمكنني ما زلت تصدير CAD إلى PDF بعد انتهاء المهلة؟** نعم – يمكنك التقاط استثناء الانقطاع وإعادة المحاولة أو تسجيل الفشل.  
- **هل أحتاج إلى ترخيص خاص؟** ترخيص Aspose.CAD العادي كافٍ؛ ميزة المهلة مدمجة.  
- **هل هذا النهج آمن للمتعدد الخيوط؟** نعم، عندما يتم تشغيل كل حفظ في خيط منفصل مع رمزه الخاص.

## ما هي المهلة في عمليات حفظ CAD؟

المهلة هي حد زمني قابل للتكوين، وعند تجاوزه، يجبر عملية الحفظ على التوقف وإثارة استثناء الانقطاع. هذا يحمي تطبيق Java الخاص بك من التوقفات غير المحدودة التي تسببها الرسومات المعقدة أو عنق الزجاجة في الإدخال/الإخراج.

## لماذا تعيين مهلة عند حفظ ملفات CAD؟

يمكن لـ Aspose.CAD **convert DWG to PDF** و **export CAD to PDF** في أقل من ثانية للرسومات النموذجية، لكن الملفات الكبيرة جدًا أو الفاسدة قد تستغرق دقائق. من خلال تعريف مهلة تضمن أن أي عملية حفظ واحدة لن تتجاوز، على سبيل المثال، 30 ثانية، مما يحافظ على استقرار إنتاجية الدفعات العامة ويمنع نقص الخيوط.

## المتطلبات المسبقة

قبل الغوص في البرنامج التعليمي، تأكد من أن لديك المتطلبات المسبقة التالية:
- **Aspose.CAD for Java Library** – تأكد من دمج مكتبة Aspose.CAD for Java في مشروعك. يمكنك تنزيل المكتبة من [website](https://releases.aspose.com/cad/java/).
- **Development Environment** – قم بإعداد بيئة تطوير Java الخاصة بك مع جميع الأدوات والاعتمادات اللازمة.

## استيراد الحزم

لبدء العمل، استورد الحزم المطلوبة في مشروع Java الخاص بك. أضف السطور التالية في بداية ملف Java الخاص بك:

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterruptionTokenSource;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.concurrent.TimeUnit;
```

الآن، دعنا نقسم كود المثال إلى تعليمات خطوة بخطوة:

## كيفية تعيين مهلة عند حفظ رسومات CAD؟

حمّل ملف CAD الخاص بك، أنشئ `InterruptionTokenSource` بالمهلة المطلوبة، ومرّر الرمز إلى خيارات حفظ PDF. إذا تجاوزت العملية المهلة، فإن Aspose.CAD يرمي `OperationCanceledException`، والذي يمكنك التقاطه لمعالجة الفشل بلطف.

### الخطوة 1: تعيين مجلدات المصدر والإخراج

```java
final String SourceDir = Utils.getDataDir_DWGDrawings();
final String OutputDir = Utils.getDataDir_Output();
```

تأكد من أن لديك مجلدات المصدر والإخراج الصحيحة لرسومات CAD الخاصة بك.

### الخطوة 2: إنشاء مصدر رمز الانقطاع

```java
final InterruptionTokenSource source = new com.aspose.cad.InterruptionTokenSource();
```

قم بتهيئة مصدر رمز الانقطاع لإدارة الانقطاعات أثناء عملية الحفظ.

### الخطوة 3: تحميل رسم CAD

الفئة `CadImage` هي الكائن الأساسي في Aspose.CAD الذي يمثل رسم CAD في الذاكرة، وتوفر طرقًا للتصيير والتحويل.

```java
final CadImage cadImageBig = (CadImage)Image.load(SourceDir + "Drawing11.dwg");
```

### الخطوة 4: تكوين خيارات التحويل إلى نقطية

`CadRasterizationOptions` يحدد كيفية تحويل رسم CAD إلى صورة نقطية.

```java
CadRasterizationOptions rasterizationOptionsBig = new CadRasterizationOptions();
rasterizationOptionsBig.setPageWidth(cadImageBig.getSize().getWidth() / 2);
rasterizationOptionsBig.setPageHeight(cadImageBig.getSize().getHeight() / 2);
```

قم بتكوين خيارات التحويل إلى نقطية لرسم CAD.

### الخطوة 5: تكوين خيارات PDF

`PdfOptions` يحدد الإعدادات لحفظ رسم CAD كوثيقة PDF.

```java
final PdfOptions CADfBig = new PdfOptions();
CADfBig.setVectorRasterizationOptions(rasterizationOptionsBig);
CADfBig.setInterruptionToken(source.getToken());
```

قم بإعداد خيارات PDF مع خيارات التحويل إلى نقطية المتجهية ورمز الانقطاع.

### الخطوة 6: حفظ الرسم مع مهلة

```java
cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
```

احفظ رسم CAD إلى ملف PDF باستخدام المهلة المحددة.

### الخطوة 7: معالجة الانقطاع

`OperationCanceledException` يُرمى عندما تتجاوز عملية الحفظ المهلة المحددة.

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

أنشئ خيطًا لمعالجة عملية الحفظ وقم بإنهائه بعد مهلة محددة.

## المشكلات الشائعة والحلول

- **المهلة قصيرة جدًا** – إذا تلقيت انقطاعات متكررة، قم بزيادة قيمة المهلة لاستيعاب الرسومات الأكبر.  
- **InterruptedException غير مُلتقطة** – دائمًا احيط استدعاء الحفظ بكتلة try‑catch لـ `OperationCanceledException` لمنع تعطل التطبيق.  
- **استهلاك الذاكرة** – استخدم `PdfOptions.setVectorRasterizationOptions` لتدفق الإخراج بدلاً من تحميل الملف بالكامل في الذاكرة.

## الأسئلة المتكررة

**س: هل يمكنني استخدام هذه الميزة لتحويل DWG إلى PDF في مهمة دفعية؟**  
ج: نعم، قم بلف كل تحويل في خيط منفصل مع رمز انقطاع منفصل لفرض حدود زمنية لكل ملف.

**س: هل تعمل المهلة على جميع صيغ الإخراج؟**  
ج: آلية المهلة مرتبطة بـ `InterruptionTokenSource` وتعمل مع أي صيغة تحترم الرمز، بما في ذلك PDF و PNG و SVG.

**س: ماذا يحدث للملفات المكتوبة جزئيًا بعد انتهاء المهلة؟**  
ج: يقوم Aspose.CAD تلقائيًا بحذف الإخراج غير المكتمل، لذا لن تحصل على ملفات PDF تالفة.

**س: هل يلزم ترخيص للاستخدام في الإنتاج؟**  
ج: نعم، يلزم وجود ترخيص Aspose.CAD صالح للنشر التجاري؛ تتوفر نسخة تجريبية مجانية للتقييم.

**س: أين يمكنني العثور على مزيد من الأمثلة لاستخدام رموز الانقطاع؟**  
ج: توفر وثائق Aspose.CAD الرسمية مقتطفات شفرة إضافية وإرشادات لأفضل الممارسات.

## موارد إضافية

- [صفحة الإصدارات](https://releases.aspose.com/cad/java/) – Direct download page for the latest Aspose.CAD for Java releases.  
- [التوثيق](https://reference.aspose.com/cad/java/) – Full API reference and developer guides.  
- [هذا الرابط](https://releases.aspose.com/) – General Aspose product releases.  
- [هنا](https://purchase.aspose.com/temporary-license/) – Obtain a temporary license for testing.  
- [منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19) – Community support and discussions.

## الخلاصة

لقد أصبحت الآن متمكنًا من **كيفية تعيين مهلة** لحفظ رسومات CAD باستخدام Aspose.CAD for Java. من خلال دمج `InterruptionTokenSource` في سير عملك يمكنك بثقة **export CAD to PDF** أو **convert DWG to PDF** دون المخاطرة بتعطيلات طويلة، مع الحفاظ على استجابة تطبيقك وقابليته للتوسع.

---

**آخر تحديث:** 2026-06-19  
**تم الاختبار مع:** Aspose.CAD for Java 24.12  
**المؤلف:** Aspose  

{{< blocks/products/products-backtop-button >}}

## دروس ذات صلة

- [تصدير DWG إلى PDF أو Raster باستخدام Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [تصدير تخطيط DWG المحدد إلى PDF باستخدام Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [تحويل DWG إلى PNG وغيرها من صيغ Raster باستخدام Aspose.CAD for Java](/cad/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}