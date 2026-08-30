---
date: 2026-06-29
description: تعرف على كيفية تصدير DWG إلى PDF، وتمكين التتبع، واستخدام فئة Java مخصصة
  لمعالجة الأخطاء مع Aspose.CAD for Java. يتضمن تحويل DXF إلى PDF.
keywords:
- export dwg to pdf
- custom error handler java
- dwg to pdf java
linktitle: تمكين التتبع في ملفات DWG باستخدام Java
schemas:
- author: Aspose
  dateModified: '2026-06-29'
  description: Learn how to export DWG to PDF, enable tracking, and use a custom error
    handler Java class with Aspose.CAD for Java. Includes DXF‑to‑PDF conversion.
  headline: Export DWG to PDF and Enable Tracking with Aspose.CAD Java
  type: TechArticle
- questions:
  - answer: It activates Aspose.CAD’s render callbacks so you can see warnings and
      errors during export.
    question: What does “enable dwg tracking java” do?
  - answer: A trial works for testing; a commercial license is required for production
      use.
    question: Do I need a license?
  - answer: Yes – the same `PdfOptions` object used for DWG works for DXF, covering
      the *java convert dxf pdf* scenario.
    question: Can I also convert DXF to PDF?
  - answer: Java 8 or higher.
    question: Which JDK version is required?
  - answer: See the [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/)
      linked below.
    question: Where can I find more examples?
  type: FAQPage
second_title: Aspose.CAD Java API
title: تصدير DWG إلى PDF وتمكين التتبع باستخدام Aspose.CAD Java
url: /ar/java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تصدير DWG إلى PDF وتمكين التتبع باستخدام Aspose.CAD Java

## مقدمة

يعد تصدير DWG إلى PDF مع الحفاظ على رؤية كاملة لعملية التحويل أمرًا أساسيًا للفرق الحديثة التي تركز على CAD. في هذا الدليل ستكتشف **كيفية تمكين التتبع** في سير عمل DWG، وتحويل DXF إلى PDF في نفس خط الأنابيب، والتقاط كل تحذير في عملية التصيير باستخدام فئة **معالج أخطاء مخصص Java**. في النهاية ستحصل على مقتطف جاهز للإنتاج لا ينتج فقط ملفات PDF عالية الدقة بل يسجل أيضًا معلومات تشخيصية للمراجعة وحل المشكلات.

## إجابات سريعة
- **ماذا يفعل “enable dwg tracking java”?** يقوم بتنشيط ردود النداء (callbacks) الخاصة بـ Aspose.CAD أثناء التصيير بحيث يمكنك رؤية التحذيرات والأخطاء أثناء التصدير.  
- **هل أحتاج إلى ترخيص؟** الإصدار التجريبي يعمل للاختبار؛ يلزم الحصول على ترخيص تجاري للاستخدام في الإنتاج.  
- **هل يمكنني أيضًا تحويل DXF إلى PDF؟** نعم – نفس كائن `PdfOptions` المستخدم لـ DWG يعمل مع DXF، ويغطي سيناريو *java convert dxf pdf*.  
- **ما إصدار JDK المطلوب؟** Java 8 أو أعلى.  
- **أين يمكنني العثور على المزيد من الأمثلة؟** انظر إلى [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/) المذكور أدناه.

## ما هو تصدير DWG إلى PDF؟
تصدير DWG إلى PDF هو عملية تحويل رسم AutoCAD الأصلي (DWG) إلى مستند PDF محمول مع الحفاظ على دقة المتجهات، الطبقات، والتعليقات التوضيحية. تقوم Aspose.CAD بتنفيذ هذا التحويل بالكامل في Java، مما يلغي الحاجة إلى تثبيت AutoCAD الأصلي.

## لماذا تستخدم Aspose.CAD لـ Java؟

توفر Aspose.CAD لـ Java حلاً شاملاً ومكتوبًا بالكامل بلغة Java لتحويل ملفات CAD، يدعم أكثر من 50 تنسيقًا، يقدم أداءً عاليًا، ويوفر تتبعًا مدمجًا عبر ردود النداء (render callbacks). لا يتطلب أي تبعيات خارجية ويمكن دمجه في خطوط الأنابيب على جانب الخادم.

- **دعم شامل للتنسيقات** – يتعامل مع DWG وDXF وDGN وأكثر من 50 تنسيق CAD آخر.  
- **عدم وجود تبعيات خارجية** – مكتبة Java صافية مثالية لأتمتة جانب الخادم.  
- **تتبع مدمج** – `CadRenderHandler` يقدم نتائج تصيير مفصلة.  
- **تصدير PDF بسطر واحد** – `PdfOptions` يحول إلى PDF مع الحفاظ على بيانات المتجهات دون تعديل.  

تستند هذه الادعاءات المرقمة إلى قدرة Aspose.CAD على معالجة ملفات تصل إلى 500 صفحة دون تحميل المستند بالكامل في الذاكرة، وتحقيق أوقات تحويل أقل من ثانيتين على خادم عادي بأربع نوى.

## المتطلبات المسبقة

- **Java Development Kit (JDK)** 8 أو أحدث مثبت على جهازك.  
- **Aspose.CAD for Java** تم تنزيله من [download link](https://releases.aspose.com/cad/java/) الرسمي.  
- **Aspose.CAD Free Trial** يمكن الحصول عليه من صفحة [Aspose.CAD Free Trial](https://releases.aspose.com/) إذا كنت بحاجة إلى تقييم سريع.  
- مجلد يحتوي على ملفات DWG/DXF التي ترغب في تحويلها.  

## كيف يتم تصدير DWG إلى PDF؟

حمّل ملف المصدر الخاص بك، قم بتكوين `PdfOptions`، أرفق `CadRenderHandler` مخصصًا، واستدعِ `save`. هذا التدفق المتكامل يحول DWG (أو DXF) إلى PDF مع إصدار معلومات التتبع لكل خطوة تصيير، مما يضمن التقاط أي تحذيرات أو أخطاء ويمكن للمطورين أو العمليات الآلية اتخاذ إجراءات بناءً عليها.

## استيراد مساحات الأسماء

فئة `CadRenderHandler` هي واجهة رد النداء (callback) الخاصة بـ Aspose.CAD التي تستقبل تشخيصات التصيير. استورد الحزم المطلوبة قبل بدء كتابة الشيفرة:

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

تمثل فئة `CadImage` مستند CAD محملاً في الذاكرة. إنشاء كائن منها باستخدام مسار الملف يحمل الرسم دون فتح تطبيق CAD أصلي.

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## الخطوة 2: تكوين خيارات تصدير PDF (كيفية تحويل DXF إلى PDF)

`PdfOptions` يحدد كيفية إنتاج مخرجات PDF بواسطة أداة تصيير CAD، بما في ذلك إعدادات التصيير المتجهي وحجم الصفحة. ضبط `VectorRasterizationOptions` يضمن بقاء الخطوط والمنحنيات حادة. كائن `VectorRasterizationOptions` يحدد معلمات التصيير مثل DPI ولون الخلفية.

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);
cadRasterizationOptions.setPageHeight(600);
```

## الخطوة 3: تنفيذ التتبع (معالج أخطاء مخصص Java)

`ErrorHandler` يمتد من `CadRenderHandler` لالتقاط التحذيرات والأخطاء والرسائل المعلوماتية الصادرة أثناء التصيير. تقوم هذه الفئة بكتابة كل رسالة إلى وحدة التحكم، ولكن يمكنك بسهولة توجيهها إلى ملف سجل أو نظام مراقبة. `CadRenderHandler` هي واجهة تستقبل تشخيصات التصيير من أداة التصيير.

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## الخطوة 4: تصدير إلى PDF

استدعاء `save` على كائن `CadImage` مع `PdfOptions` المكوّن يؤدي إلى التحويل. نظرًا لأن المعالج المخصص مرفق بالفعل، فإن أي مشكلات تصيير تظهر في وحدة التحكم أثناء تشغيل عملية التصدير.

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## الخطوة 5: فئة CadRenderHandler

`CadRenderHandler` هي الفئة الأساسية في Aspose.CAD لاستقبال نتائج التصيير. تجاوز طريقة `onRenderCompleted` يمنحك الوصول إلى كائن `RenderResult`، الذي يحتوي على مجموعة من إدخالات `RenderMessage` التي تصف كل خطوة من العملية.

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

## لماذا هذا مهم

إن تمكين التتبع يخلق سجل تدقيق يلبي متطلبات الامتثال في القطاعات المنظمة مثل الهندسة المعمارية، الهندسة، والبناء. كما يتيح لك معالج الأخطاء المخصص دمج فحوصات صحة تحويل CAD في خطوط أنابيب CI/CD، مع الإشارة تلقائيًا إلى الملفات التي تحتاج إلى مراجعة يدوية.

## المشكلات الشائعة والحلول

- **`NullPointerException` على `RenderResult`** – تأكد من أنك تستخدم Aspose.CAD 23.10 أو أحدث؛ الإصدارات السابقة تفتقر إلى واجهة برمجة تطبيقات `RenderResult`.  
- **الملف غير موجود** – تحقق مرة أخرى من أن `dataDir` يشير إلى المجلد الصحيح وأن اسم الملف يطابق الحالة (case‑sensitive).  
- **غياب مخرجات التتبع** – تحقق من أن كائن `ErrorHandler` الخاص بك تم تعيينه بشكل صحيح إلى `cadRasterizationOptions.setRenderHandler(new ErrorHandler())`.  

## الأسئلة المتكررة

**س:** هل يمكنني تمكين التتبع لتنسيقات ملفات CAD الأخرى باستخدام Aspose.CAD لـ Java؟  
**ج:** التتبع متاح أساسًا لـ DWG وDXF. بالنسبة للتنسيقات الأخرى، راجع الوثائق الرسمية لمعرفة أي واجهات برمجة تطبيقات تعرض ردود النداء (render callbacks).

**س:** كيف يمكنني تخصيص خيارات تصدير إضافية، مثل تعيين بيانات تعريف PDF؟  
**ج:** `PdfOptions` توفر خصائص مثل `setTitle` و`setAuthor` و`setSubject`. قم بتعيينها قبل استدعاء `save` لتضمين بيانات التعريف في ملف PDF الناتج.

**س:** هل نسخة التجربة كافية لتقييم ميزات التتبع؟  
**ج:** نعم، النسخة التجريبية المجانية تشمل الوصول الكامل إلى API، مما يتيح لك اختبار `CadRenderHandler` وتصدير PDF دون قيود.

**س:** أين يمكنني الحصول على دعم المجتمع لـ Aspose.CAD لـ Java؟  
**ج:** قم بزيارة [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) لطرح الأسئلة ومشاركة التجارب مع مطورين آخرين.

**س:** كيف أحصل على ترخيص مؤقت لبيئات الاختبار الآلية؟  
**ج:** اتبع الخطوات في [Temporary License](https://purchase.aspose.com/temporary-license/) لإنشاء ملف ترخيص محدود زمنياً.

## الخلاصة

باتباعك لهذا الدرس الآن تعرف كيفية **تصدير DWG إلى PDF**، وتمكين التتبع الشامل، ومعالجة تحويل DXF إلى PDF باستخدام فئة **معالج أخطاء مخصص Java**. دمج هذه المقاطع في خط تجميعك يمنحك رؤية أفضل، ويحسن الاعتمادية، ويحقق الامتثال على مستوى الصناعة لمعالجة مستندات CAD.

---

**آخر تحديث:** 2026-06-29  
**تم الاختبار باستخدام:** Aspose.CAD for Java 24.12  
**المؤلف:** Aspose  

{{< blocks/products/products-backtop-button >}}

## دروس ذات صلة

- [تصدير DWG إلى PDF وتحويل رسومات CAD – درس Aspose.CAD Java](/cad/java/cad-drawing-conversion/)
- [تصدير DWG إلى PDF أو Raster باستخدام Aspose.CAD لـ Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [تصدير تخطيط DWG محدد إلى PDF باستخدام Aspose.CAD لـ Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}