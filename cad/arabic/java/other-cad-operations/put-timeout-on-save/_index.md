---
title: انتهت مهلة الحفظ لـ CAD باستخدام Aspose.CAD
linktitle: ضع المهلة على الحفظ
second_title: Aspose.CAD جافا API
description: تعرف على كيفية تعزيز أداء تطبيق Java الخاص بك باستخدام Aspose.CAD. ضع مهلة لحفظ رسومات CAD. اتبع دليلنا خطوة بخطوة.
weight: 15
url: /ar/java/other-cad-operations/put-timeout-on-save/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# انتهت مهلة الحفظ لـ CAD باستخدام Aspose.CAD

## مقدمة

مرحبًا بك في البرنامج التعليمي حول وضع مهلة للحفظ باستخدام Aspose.CAD لـ Java. في هذا الدليل، سنرشدك خلال عملية تحديد مهلة لحفظ رسومات CAD لتحسين أداء التطبيق الخاص بك. Aspose.CAD for Java هي مكتبة قوية تتيح لك العمل مع ملفات CAD في تطبيقات Java الخاصة بك بسلاسة.

## المتطلبات الأساسية

قبل الغوص في البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:
-  Aspose.CAD لمكتبة Java: تأكد من دمج مكتبة Aspose.CAD لـ Java في مشروعك. يمكنك تحميل المكتبة من[موقع إلكتروني](https://releases.aspose.com/cad/java/).
- بيئة التطوير: قم بإعداد بيئة تطوير Java الخاصة بك باستخدام جميع الأدوات والتبعيات اللازمة.

## حزم الاستيراد

للبدء، قم باستيراد الحزم المطلوبة إلى مشروع Java الخاص بك. أضف الأسطر التالية في بداية ملف Java الخاص بك:

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterruptionTokenSource;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.concurrent.TimeUnit;
```

الآن، دعونا نقسم رمز المثال إلى تعليمات خطوة بخطوة:

## الخطوة 1: تعيين أدلة المصدر والإخراج

```java
final String SourceDir = Utils.getDataDir_DWGDrawings();
final String OutputDir = Utils.getDataDir_Output();
```

تأكد من أن لديك أدلة المصدر والإخراج الصحيحة لرسومات CAD الخاصة بك.

## الخطوة 2: إنشاء مصدر رمز المقاطعة

```java
final InterruptionTokenSource source = new com.aspose.cad.InterruptionTokenSource();
```

قم بتهيئة مصدر رمز المقاطعة لإدارة المقاطعات أثناء عملية الحفظ.

## الخطوة 3: تحميل رسم CAD

```java
final CadImage cadImageBig = (CadImage)Image.load(SourceDir + "Drawing11.dwg");
```

 قم بتحميل رسم CAD إلى ملف`CadImage` هدف.

## الخطوة 4: تكوين خيارات التنقيط

```java
CadRasterizationOptions rasterizationOptionsBig = new CadRasterizationOptions();
rasterizationOptionsBig.setPageWidth(cadImageBig.getSize().getWidth() / 2);
rasterizationOptionsBig.setPageHeight(cadImageBig.getSize().getHeight() / 2);
```

تكوين خيارات التنقيط لرسم CAD.

## الخطوة 5: تكوين خيارات PDF

```java
final PdfOptions CADfBig = new PdfOptions();
CADfBig.setVectorRasterizationOptions(rasterizationOptionsBig);
CADfBig.setInterruptionToken(source.getToken());
```

قم بإعداد خيارات PDF باستخدام خيارات تنقيط المتجهات ورمز المقاطعة.

## الخطوة 6: حفظ الرسم مع انتهاء المهلة

```java
cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
```

احفظ رسم CAD في ملف PDF مع انتهاء المهلة المحددة.

## الخطوة 7: التعامل مع المقاطعة

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

قم بإنشاء مؤشر ترابط للتعامل مع عملية الحفظ ومقاطعتها بعد انتهاء المهلة المحددة.

## خاتمة

تهانينا! لقد تعلمت بنجاح كيفية وضع مهلة للحفظ باستخدام Aspose.CAD لـ Java. يمكن لهذه الميزة أن تعزز بشكل كبير كفاءة تطبيقاتك المتعلقة بالتصميم بمساعدة الكمبيوتر (CAD).

## الأسئلة الشائعة

### س1: كيف يمكنني تنزيل Aspose.CAD لـ Java؟

 ج1: يمكنك تنزيله من[صفحة الإصدارات](https://releases.aspose.com/cad/java/).

### س2: أين يمكنني العثور على الوثائق الخاصة بـ Aspose.CAD لـ Java؟

 ج2: راجع[توثيق](https://reference.aspose.com/cad/java/) للحصول على معلومات شاملة.

### س3: هل هناك نسخة تجريبية مجانية متاحة؟

ج3: نعم، يمكنك الحصول على نسخة تجريبية مجانية من[هذا الرابط](https://releases.aspose.com/).

### س4: كيف يمكنني الحصول على ترخيص مؤقت؟

 ج4: زيارة[هنا](https://purchase.aspose.com/temporary-license/) للحصول على تفاصيل الترخيص المؤقت.

### س5: هل تحتاج إلى مساعدة أو لديك أسئلة؟

 ج5: توجه إلى[منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19) لدعم المجتمع.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
