---
date: 2025-12-03
description: تعلم كيفية ضبط حجم صفحة PDF أثناء تحويل DWG إلى PDF وتمكين التتبع في
  ملفات DWG باستخدام Aspose.CAD للغة Java – دليل كامل لتصدير رسومات CAD بصيغة PDF
  بدقة.
language: ar
linktitle: Set PDF Page Size and Enable Tracking in DWG Files Using Java
second_title: Aspose.CAD Java API
title: تعيين حجم صفحة PDF وتمكين التتبع في ملفات DWG باستخدام Aspose.CAD في Java
url: /java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تعيين حجم صفحة PDF وتمكين التتبع في ملفات DWG باستخدام Aspose.CAD في Java

## المقدمة

إذا كنت بحاجة إلى **تعيين حجم صفحة PDF** عند *تحويل DWG إلى PDF* وتريد أيضًا تتبع أي مشكلات في العرض، فإن Aspose.CAD for Java يوفّر لك طريقة برمجية نظيفة للقيام بالأمرين معًا. في هذا الدرس سنستعرض الخطوات الدقيقة لتكوين أبعاد الصفحة، تمكين التتبع، وتصدير رسم CAD كملف PDF — كل ذلك من خلال Java. في النهاية ستفهم لماذا يُعَدُّ تعيين الحجم الصحيح للصفحة مهمًا لرسومات CAD وكيفية التقاط معلومات تتبع مفصلة أثناء عملية التصدير.

## إجابات سريعة
- **ماذا يؤثر “تعيين حجم صفحة PDF”؟** يحدد عرض وارتفاع لوحة PDF الناتجة، مما يضمن أن الرسم يتناسب تمامًا.  
- **هل أحتاج إلى ترخيص لاستخدام هذه الميزة؟** النسخة التجريبية تكفي للاختبار؛ يلزم ترخيص تجاري للإنتاج.  
- **ما نسخة Aspose.CAD المطلوبة؟** أي نسخة حديثة تدعم `CadRasterizationOptions`.  
- **هل يمكنني استخدام ذلك مع صيغ CAD أخرى؟** المثال يوضح DWG/DXF، لكن نفس النهج يعمل مع معظم الصيغ المدعومة.  
- **كم يستغرق التحويل؟** عادةً أقل من ثانية للملفات المتوسطة؛ قد تستغرق الرسومات الكبيرة وقتًا أطول.

## ما معنى “تعيين حجم صفحة PDF” في سياق تصدير CAD؟
تعيين حجم صفحة PDF يخبر أداة العرض بالأبعاد الدقيقة (بالبكسل أو النقاط) للوحة الإخراج. هذا مهم بشكل خاص للرسومات التقنية حيث يجب الحفاظ على المقياس والتخطيط. بدون إعداد صريح لحجم الصفحة، قد يختار PDF حجمًا افتراضيًا يقتطع أو يشوّه الرسم.

## لماذا نعين حجم صفحة PDF عند تصدير رسومات CAD؟
- **الحفاظ على المقياس** – يعتمد المهندسون على طبعات دقيقة المقياس.  
- **التناسب مع الورق** – اختر A4 أو Letter أو حجمًا مخصصًا يتوافق مع مواصفات المشروع.  
- **تحسين قابلية القراءة** – الصفحات الأكبر تُظهر التفاصيل الدقيقة دون الحاجة للتكبير.  
- **إنتاجية ثابتة** – خطوط الأنابيب الآلية تُنتج ملفات PDF بأبعاد متطابقة في كل مرة.

## كيف نعين حجم صفحة PDF عند تحويل DWG إلى PDF؟
سنعمل أدناه على تكوين `CadRasterizationOptions` بقيم عرض وارتفاع مخصصة قبل التصدير. هذه الخطوة تتعامل مباشرة مع الكلمة المفتاحية **تعيين حجم صفحة PDF**.

## المتطلبات المسبقة

- **مجموعة تطوير Java (JDK)** – Java 8 أو أحدث مثبتة على جهازك.  
- **Aspose.CAD for Java** – حمّلها من [صفحة تنزيل Aspose CAD الرسمية](https://releases.aspose.com/cad/java/).  
- **دليل المستندات** – مجلد يحتوي على ملفات DWG/DXF التي تريد معالجتها.

## استيراد المساحات الاسمية

أولاً، استورد الفئات التي ستحتاجها. كتلة الشيفرة تبقى كما هي من الدرس الأصلي.

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

## الخطوة 1: تحميل ملف DWG/DXF

حمّل الرسم المصدر. عدّل المسار ليتوافق مع ملفك الخاص.

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## الخطوة 2: تكوين خيارات تصدير PDF (بما في ذلك حجم الصفحة)

هنا نحدد عرض وارتفاع الصفحة — هذه هي النقطة التي **نُعين فيها حجم صفحة PDF**. القيم بوحدة البكسل؛ يمكنك التحويل من البوصة أو المليمتر حسب الحاجة.

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);   // <-- custom width
cadRasterizationOptions.setPageHeight(600);  // <-- custom height
```

> **نصيحة:** إذا كنت تفضّل أحجام ورق قياسية، استخدم التحويل `1 بوصة = 72 نقطة`. لصفحة A4 (8.27 × 11.69 بوصة)، عيّن `pageWidth = 595` و `pageHeight = 842`.

## الخطوة 3: تنفيذ التتبع

التتبع يلتقط أي مشكلات في العرض. نرفق معالجًا مخصصًا سيتم استدعاؤه بعد عملية التصدير.

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## الخطوة 4: التصدير إلى PDF

الآن نفّذ التحويل. سيُنشأ ملف PDF بالأبعاد التي حددتها، وستُطبع أي معلومات تتبع إلى وحدة التحكم.

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## الخطوة 5: فئة CadRenderHandler

المعالج يطبع أي فشل حدث أثناء العرض. يساعدك ذلك على تصحيح المشكلات عند **تصدير رسم CAD كملف PDF**.

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

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|-------|-----|
| **PDF فارغ** | تم تعيين حجم الصفحة إلى 0 أو قيمة صغيرة جدًا | تأكد من أن `setPageWidth` و `setPageHeight` قيمهما موجبة. |
| **غياب الهندسة** | أخطاء عرض تم التقاطها بواسطة المعالج | راجع مخرجات وحدة التحكم من `ErrorHandler` وتعامل مع `RenderCode` المحدد. |
| **الملف غير موجود** | مسار `dataDir` غير صحيح | استخدم مسارًا مطلقًا أو تأكد من وجود الدليل. |
| **استثناء الترخيص** | استخدام النسخة التجريبية بدون ترخيص صالح للملفات الكبيرة | طبّق ترخيص Aspose.CAD قبل تحميل الصورة. |

## الأسئلة المتكررة

**س: هل يمكنني تمكين التتبع لصيغ CAD أخرى باستخدام Aspose.CAD for Java؟**  
 يدعم Aspose.CAD أساسًا DWG/DXF للتتبع. بالنسبة للصيغ الأخرى، راجع الوثائق الرسمية.

**س: كيف يمكنني التعامل مع خيارات تصدير إضافية في Aspose.CAD for Java؟**  
ج: المكتبة توفر العديد من الخيارات مثل DPI، لون الخلفية، والرستر المتجه. راجع [توثيق Aspose.CAD Java](https://reference.aspose.com/cad/java/) للمزيد من التفاصيل.

**س: هل تتوفر نسخة تجريبية من Aspose.CAD for Java؟**  
ج: نعم، يمكنك تنزيل نسخة تجريبية مجانية من [Aspose.CAD Free Trial](https://releases.aspose.com/).

**س: أين يمكنني طلب المساعدة أو مناقشة المشكلات المتعلقة بـ Aspose.CAD for Java؟**  
ج: زر [منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19) للحصول على دعم المجتمع والإجابات الرسمية.

**س: كيف أحصل على ترخيص مؤقت لـ Aspose.CAD for Java؟**  
ج: اتبع الخطوات الموضحة في صفحة [الترخيص المؤقت](https://purchase.aspose.com/temporary-license/).

---

**آخر تحديث:** 2025-12-03  
**تم الاختبار مع:** Aspose.CAD for Java 24.11 (أحدث نسخة وقت الكتابة)  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}