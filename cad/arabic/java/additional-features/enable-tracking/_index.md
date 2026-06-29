---
date: 2026-02-10
description: دليل خطوة بخطوة حول كيفية تمكين التتبع في ملفات DWG باستخدام Aspose.CAD
  للغة Java وكيفية تحويل DXF إلى PDF مع معالج أخطاء مخصص.
linktitle: Enable Tracking in DWG Files Using Java
second_title: Aspose.CAD Java API
title: كيفية تمكين التتبع في ملفات DWG باستخدام Aspose.CAD في جافا
url: /ar/java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية تمكين التتبع في ملفات DWG باستخدام Aspose.CAD في Java

## المقدمة

إذا كنت تعمل على مشاريع CAD تعاونية، فإن معرفة **كيفية تمكين التتبع** في سير عمل DWG الخاصة بك تُغيّر قواعد اللعبة. فهي توفر لك نظرة فورية على مشاكل العرض، وتتيح لك اكتشاف أخطاء التحويل مبكرًا، وتبقي جميع أصحاب المصلحة على اطلاع. في هذا الدرس سنستعرض الخطوات الدقيقة لتمكين التتبع باستخدام Aspose.CAD للـ Java، وسنُظهر أيضًا **كيفية تحويل DXF إلى PDF** كجزء من نفس سير العمل. في النهاية ستحصل على مقتطف كامل جاهز للإنتاج يُبلغ عن الأخطاء عبر فئة **معالج الأخطاء المخصص Java** أثناء تصدير رسوماتك.

## إجابات سريعة
- **ماذا يفعل “enable dwg tracking java”?** يقوم بتنشيط ردود النداء لمعالجة الأخطاء في Aspose.CAD بحيث يمكنك رؤية مشاكل العرض أثناء التصدير.  
- **هل أحتاج إلى ترخيص؟** النسخة التجريبية تعمل للاختبار؛ الترخيص التجاري مطلوب للإنتاج.  
- **هل يمكنني أيضًا تحويل DXF إلى PDF؟** نعم – نفس `PdfOptions` المستخدمة لـ DWG تعمل مع DXF، مما يحقق سيناريو *java convert dxf pdf*.  
- **ما نسخة JDK المطلوبة؟** Java 8 أو أعلى.  
- **أين يمكنني العثور على مزيد من الأمثلة؟** راجع وثائق Aspose.CAD Java المرفقة أدناه.

## كيفية تمكين التتبع في ملفات DWG باستخدام Aspose.CAD

تمكين تتبع DWG في تطبيق Java يعني إرفاق معالج عرض مخصص يلتقط التحذيرات والأخطاء ومعلومات التشخيص الأخرى أثناء تحويل ملف CAD إلى صورة raster أو تصديره. هذه الرؤية تساعد المطورين على تصحيح مسارات التحويل وتضمن مخرجات ذات جودة أعلى.

## لماذا تستخدم Aspose.CAD للـ Java؟

- **دعم CAD كامل المميزات** – DWG، DXF، DGN، وأكثر.  
- **بدون تبعيات خارجية** – مكتبة Java صافية، مثالية لأتمتة الخوادم.  
- **تتبع مدمج** – نتائج عرض مفصلة عبر `CadRenderHandler`.  
- **تصدير PDF سهل** – تحويل بسطر واحد مع الحفاظ على البيانات المتجهة.  

## المتطلبات المسبقة

قبل أن نغوص في التنفيذ، تأكد من توفر المتطلبات المسبقة التالية:

- Java Development Kit (JDK): تأكد من تثبيت Java على نظامك.  
- Aspose.CAD للـ Java: قم بتنزيل وتثبيت Aspose.CAD للـ Java من [رابط التحميل](https://releases.aspose.com/cad/java/).  
- دليل المستندات: حضّر دليلًا يحتوي على ملفات DWG الخاصة بك.

## استيراد المساحات الاسمية

في مشروع Java الخاص بك، ابدأ باستيراد المساحات الاسمية اللازمة للاستفادة من وظائف Aspose.CAD:

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

## الخطوة 1: تحميل ملف DWG

ابدأ بتحميل ملف DWG (أو DXF) إلى تطبيق Java الخاص بك. عدّل مسار الملف وفقًا لذلك:

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## الخطوة 2: تكوين خيارات تصدير PDF (كيفية تحويل DXF إلى PDF)

قم بإعداد خيارات تصدير PDF، مع تحديد خيارات rasterization المتجهة لـ CAD. هذا أيضًا يوضح قدرة *java convert dxf pdf*:

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);
cadRasterizationOptions.setPageHeight(600);
```

## الخطوة 3: تنفيذ التتبع (معالج الأخطاء المخصص Java)

نفّذ التتبع باستخدام فئة معالج الأخطاء المخصص. هذه الفئة ستلتقط مشاكل العرض وتعرضها في وحدة التحكم:

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## الخطوة 4: التصدير إلى PDF

ابدأ عملية التصدير لتحويل ملف DWG/DXF إلى PDF مع تمكين التتبع:

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## الخطوة 5: فئة CadRenderHandler

عرّف فئة `ErrorHandler` (التي تمتد من `CadRenderHandler`) لمعالجة نتائج العرض وإخراج معلومات التتبع:

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

من خلال تمكين التتبع ستحصل على سجل تدقيق واضح لكل خطوة تحويل. هذا ذو قيمة خاصة في الصناعات المنظمة (العمارة، الهندسة، البناء) حيث يُطلب إثبات دقة العرض لتدقيق الامتثال. كما يوفر معالج الأخطاء المخصص وسيلة لتسجيل المشكلات في نظام مراقبة أو لتفعيل محاولات إعادة تلقائية.

## المشكلات الشائعة والحلول

- **`NullPointerException` على `RenderResult`** – تأكد من أنك تستخدم Aspose.CAD الإصدار 23.10 أو أحدث؛ الإصدارات القديمة تفتقر إلى واجهة `RenderResult`.  
- **الملف غير موجود** – تحقق من أن `dataDir` يشير إلى المجلد الصحيح وأن اسم الملف يطابق تمامًا، بما في ذلك حالة الأحرف.  
- **عدم وجود مخرجات التتبع** – تأكد من أن `ErrorHandler` المخصص تم تعيينه بشكل صحيح إلى `cadRasterizationOptions.RenderResult`.  

## الأسئلة المتكررة

**س:** هل يمكنني تمكين التتبع لتنسيقات ملفات CAD الأخرى باستخدام Aspose.CAD للـ Java؟  
**ج:** يدعم Aspose.CAD أساسًا تتبع DWG. بالنسبة للتنسيقات الأخرى، راجع الوثائق الرسمية.

**س:** كيف يمكنني التعامل مع خيارات تصدير إضافية في Aspose.CAD للـ Java؟  
**ج:** استكشف الوثائق الشاملة على [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/).

**س:** هل تتوفر نسخة تجريبية من Aspose.CAD للـ Java؟  
**ج:** نعم، يمكنك الوصول إلى النسخة التجريبية عبر [Aspose.CAD Free Trial](https://releases.aspose.com/).

**س:** أين يمكنني طلب المساعدة أو مناقشة المشكلات المتعلقة بـ Aspose.CAD للـ Java؟  
**ج:** زر [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) للحصول على دعم المجتمع.

**س:** كيف أحصل على ترخيص مؤقت لـ Aspose.CAD للـ Java؟  
**ج:** اتبع العملية الموضحة في [Temporary License](https://purchase.aspose.com/temporary-license/).

## الخاتمة

تمكين تتبع DWG في Java باستخدام Aspose.CAD لا يمنحك فقط رؤية لمشكلات التحويل بل يُبسّط أيضًا سير عمل التصميم التعاوني. باتباع الخطوات أعلاه يمكنك **كيفية تمكين التتبع**، تحويل DXF إلى PDF، ومعالجة أي مشكلات عرض بسلاسة.

---

**آخر تحديث:** 2026-02-10  
**تم الاختبار مع:** Aspose.CAD for Java 24.12  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}