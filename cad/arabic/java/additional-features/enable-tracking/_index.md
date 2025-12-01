---
date: 2025-12-01
description: تعلم كيفية ضبط حجم صفحة PDF، وتحويل DWG إلى PDF، وتمكين تتبع تغييرات
  DWG باستخدام Aspose.CAD للغة Java.
language: ar
linktitle: Set PDF Page Size and Track DWG with Java
second_title: Aspose.CAD Java API
title: تعيين حجم صفحة PDF وتتبع DWG باستخدام Aspose.CAD Java
url: /java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تعيين حجم صفحة PDF وتتبع DWG باستخدام Aspose.CAD Java

## مقدمة

عند التعاون في مشاريع CAD، غالبًا ما تحتاج إلى **تعيين حجم صفحة PDF** للحصول على تخطيط متسق، **تحويل DWG إلى PDF**، وتتبع كل تغيير يتم إجراؤه على الرسم. تجعل Aspose.CAD for Java كل ذلك ممكنًا في سير عمل واحد مبسط. في هذا البرنامج التعليمي سنستعرض الخطوات الدقيقة لـ **تعيين حجم صفحة PDF**، تمكين **تتبع تغييرات DWG**، وتصدير الرسم كملف PDF — كل ذلك باستخدام Java.

## إجابات سريعة
- **كيف يمكنني تعيين حجم صفحة PDF؟** استخدم `CadRasterizationOptions.setPageWidth()` و `setPageHeight()` قبل التصدير.  
- **هل يمكنني تتبع التغييرات أثناء التصدير؟** نعم – نفّذ `CadRenderHandler` مخصص لالتقاط نتائج التتبع.  
- **ما هي الطريقة التي تحول DWG إلى PDF؟** استدعِ `image.save(stream, pdfOptions)` بعد تكوين الخيارات.  
- **ما هي المتطلبات الأساسية؟** JDK، Aspose.CAD for Java، ومجلد يحتوي على ملفات DWG/DXF.  
- **هل يلزم وجود ترخيص للإنتاج؟** نعم، يلزم وجود ترخيص Aspose.CAD صالح للنشر غير التجريبي.

## ما هو “تعيين حجم صفحة PDF” في سياق تصدير DWG؟

تحديد حجم صفحة PDF يحدد أبعاد لوحة PDF الناتجة (العرض × الارتفاع بالبكسل). هذا أمر أساسي عندما تريد أن يتناسب الرسم المصدّر مع حجم ورق محدد أو تخطيط شاشة، مما يضمن ظهور جميع العناصر بالضبط في الموضع المتوقع.

## لماذا تمكين التتبع عند تصدير ملفات DWG؟

يسجل التتبع (أو تتبع التغييرات) أي مشاكل في العرض، أو خطوط مفقودة، أو كيانات غير مدعومة تحدث أثناء التحويل. من خلال التقاط هذه المعلومات يمكنك:
- تحديد المشكلات بسرعة التي تحتاج إلى إصلاح قبل التسليم النهائي.
- تقديم ملاحظات واضحة لأعضاء الفريق حول ما تم تغييره أو حذفه.
- الحفاظ على سجل تدقيق للقطاعات التي تتطلب الامتثال.

## المتطلبات المسبقة

- **Java Development Kit (JDK)** – أي نسخة حديثة (8+).  
- **Aspose.CAD for Java** – حمّل من [صفحة تحميل Aspose CAD الرسمية](https://releases.aspose.com/cad/java/).  
- **Document Directory** – مجلد يحتوي على ملفات DWG/DXF التي تريد معالجتها.

## استيراد مساحات الأسماء

ابدأ باستيراد الفئات الضرورية من Aspose.CAD وفئات الإدخال/الإخراج القياسية في Java.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.CadRenderResult;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.RenderResult;
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
```

## الخطوة 1: تحميل ملف DWG (أو DXF)

حمّل الرسم المصدر إلى كائن `Image`. عدّل المسار ليشير إلى الدليل الخاص بك.

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## الخطوة 2: تكوين خيارات تصدير PDF (بما في ذلك حجم الصفحة)

هنا نقوم بتعيين خيارات PDF ونحدد صراحةً **حجم صفحة PDF** إلى 800 × 600 بكسل. هذا هو المكان الذي يُطبق فيه الكلمة المفتاحية الأساسية.

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);   // set PDF page width
cadRasterizationOptions.setPageHeight(600);  // set PDF page height
```

## الخطوة 3: تنفيذ التتبع

أنشئ معالج أخطاء مخصص سيتلقى معلومات التتبع أثناء عملية التحويل.

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## الخطوة 4: تصدير إلى PDF

مع وجود الخيارات ومعالج التتبع، قم بتصدير الرسم. هذه الخطوة **تحول DWG إلى PDF** (أو DXF إلى PDF في مثالنا).

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## الخطوة 5: فئة CadRenderHandler – التقاط نتائج التتبع

فئة `ErrorHandler` تمتد من `CadRenderHandler` وتطبع أي مشاكل في العرض حدثت أثناء **تتبع تغييرات ملفات DWG**.

```java
public static class ErrorHandler extends CadRasterizationOptions.CadRenderHandler {
    @Override
    public void invoke(CadRenderResult result) {
        System.out.println("Tracking results of exporting");

        if (result.isRenderComplete())
            return;

        System.out.println("Have some problems:");

        int idxError = 1;
        for (RenderResult rr : result.getFailures()) {
            System.out.printf("{0}. {1}, {2}", idxError, rr.getRenderCode(), rr.getMessage());
            idxError++;
        }
    }
}
```

## المشكلات الشائعة وكيفية حلها

| المشكلة | سبب حدوثها | الحل |
|---------|------------|------|
| **خطوط مفقودة** | ملف CAD يشير إلى خطوط غير مثبتة على الخادم. | قم بتثبيت الخطوط المطلوبة أو تضمينها في الرسم المصدر. |
| **كيانات غير مدعومة** | بعض كيانات DWG غير مدعومة بعد من قبل Aspose.CAD. | استخدم مخرجات التتبع لتحديدها وتبسيط الرسم. |
| **حجم صفحة غير صحيح** | `setPageWidth/Height` لم يتم استدعاؤه قبل التصدير. | تأكد من تعيين حجم الصفحة في `CadRasterizationOptions` كما هو موضح أعلاه. |

## الأسئلة المتكررة

### س1: هل يمكنني تمكين التتبع لتنسيقات ملفات CAD أخرى باستخدام Aspose.CAD for Java؟

ج1: يدعم Aspose.CAD أساسًا التتبع لملفات DWG/DXF. بالنسبة للتنسيقات الأخرى، راجع الوثائق الرسمية لمعرفة الميزات المتاحة.

### س2: كيف يمكنني التعامل مع خيارات تصدير إضافية في Aspose.CAD for Java؟

ج2: توفر المكتبة العديد من الخيارات مثل DPI، لون الخلفية، ورسترزة المتجهات. استكشفها في [توثيق Aspose.CAD Java](https://reference.aspose.com/cad/java/).

### س3: هل هناك نسخة تجريبية متاحة لـ Aspose.CAD for Java؟

ج3: نعم، يمكنك تحميل نسخة تجريبية مجانية من [Aspose.CAD Free Trial](https://releases.aspose.com/).

### س4: أين يمكنني طلب المساعدة أو مناقشة المشكلات المتعلقة بـ Aspose.CAD for Java؟

ج4: منتدى المجتمع على [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) هو مكان ممتاز لطرح الأسئلة ومشاركة التجارب.

### س5: كيف أحصل على ترخيص مؤقت لـ Aspose.CAD for Java؟

ج5: اتبع الخطوات الموضحة في صفحة [Temporary License](https://purchase.aspose.com/temporary-license/) لطلب ترخيص مؤقت لتقييم المنتج.

### س6: هل يمكنني **تحويل DWG إلى PDF** مع الحفاظ على الطبقات؟

ج6: نعم. من خلال تكوين `CadRasterizationOptions` يمكنك الحفاظ على معلومات الطبقات في ملف PDF الناتج.

### س7: ما هي أفضل طريقة لـ **تصدير DWG كـ PDF** بأبعاد صفحة مخصصة؟

ج7: عيّن العرض والارتفاع المطلوبين باستخدام `setPageWidth` و `setPageHeight` قبل استدعاء `image.save()` – تمامًا كما هو موضح في الخطوة 2.

## الخلاصة

باتباع الخطوات السابقة يمكنك **تعيين حجم صفحة PDF**، **تحويل DWG إلى PDF**، و**تتبع التغييرات في ملفات DWG** باستخدام Aspose.CAD for Java. يمنحك هذا سير العمل تحكمًا كاملاً في تخطيط المخرجات مع توفير تشخيصات قيمة تحافظ على سلاسة التعاون في CAD وخلوه من الأخطاء. لا تتردد في استكشاف خيارات العرض الإضافية ودمج هذا الكود في خطوط أنابيب أتمتة أكبر.

---

**آخر تحديث:** 2025-12-01  
**تم الاختبار مع:** Aspose.CAD for Java 24.12 (latest at time of writing)  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}