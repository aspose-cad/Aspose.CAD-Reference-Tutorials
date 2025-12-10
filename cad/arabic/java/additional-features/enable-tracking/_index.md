---
date: 2025-12-09
description: تعلم كيفية تمكين تتبع DWG في Java وشاهد أيضًا كيفية تحويل DXF إلى PDF
  باستخدام Aspose.CAD. يوضح لك هذا الدليل خطوة بخطوة سير العمل الكامل لمشاريع CAD
  التعاونية.
linktitle: Enable Tracking in DWG Files Using Java
second_title: Aspose.CAD Java API
title: تمكين التتبع في ملفات DWG باستخدام Aspose.CAD في Java
url: /ar/java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تمكين التتبع في ملفات DWG باستخدام Aspose.CAD في Java

## مقدمة

في سير عمل CAD الحديث، القدرة على **enable dwg tracking java** أمر أساسي للفرق التي تحتاج إلى مراقبة التغييرات، واكتشاف الأخطاء مبكرًا، والحفاظ على توافق جميع أصحاب المصلحة. يشرح هذا الدليل الخطوات الدقيقة لتفعيل التتبع لملفات DWG باستخدام Aspose.CAD للـ Java، وسترى أيضًا كيفية **java convert dxf pdf** كجزء من عملية التصدير. في النهاية، ستحصل على مقتطف جاهز للتنفيذ لا يقتصر على التحويل فقط بل يُبلغ أيضًا عن أي مشكلات في العرض.

## إجابات سريعة
- **ماذا يفعل “enable dwg tracking java”?** It activates Aspose.CAD’s error‑handling callbacks so you can see rendering problems during export.  
- **هل أحتاج إلى ترخيص؟** A trial works for testing; a commercial license is required for production.  
- **هل يمكنني أيضًا تحويل DXF إلى PDF؟** Yes – the same `PdfOptions` used for DWG works for DXF, fulfilling the *java convert dxf pdf* scenario.  
- **ما نسخة JDK المطلوبة؟** Java 8 or higher.  
- **أين يمكنني العثور على المزيد من الأمثلة؟** Check the Aspose.CAD Java Documentation linked below.

## ما هو enable dwg tracking java؟
تفعيل تتبع DWG في تطبيق Java يعني ربط معالج عرض مخصص يلتقط التحذيرات والأخطاء ومعلومات تشخيصية أخرى أثناء تحويل ملف CAD إلى صورة نقطية أو تصديره. هذه الرؤية تساعد المطورين على تصحيح مسارات التحويل وتضمن جودة أعلى للمنتجات النهائية.

## لماذا نستخدم Aspose.CAD للـ Java؟
- **دعم CAD كامل الميزات** – DWG, DXF, DGN, وأكثر.  
- **بدون تبعيات خارجية** – مكتبة Java صافية، مثالية لأتمتة الخوادم.  
- **تتبع مدمج** – نتائج عرض مفصلة عبر `CadRenderHandler`.  
- **تصدير PDF سهل** – تحويل بسطر واحد مع الحفاظ على البيانات المتجهة.

## المتطلبات المسبقة

قبل الغوص في التنفيذ، تأكد من توفر المتطلبات التالية:

- Java Development Kit (JDK): تأكد من تثبيت Java على نظامك.  
- Aspose.CAD للـ Java: قم بتنزيل وتثبيت Aspose.CAD للـ Java من [download link](https://releases.aspose.com/cad/java/).  
- دليل المستندات: حضّر مجلدًا يحتوي على ملفات DWG الخاصة بك.

## استيراد المساحات الاسمية

في مشروع Java الخاص بك، ابدأ باستيراد المساحات الاسمية الضرورية للاستفادة من وظائف Aspose.CAD:

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

## الخطوة 2: تكوين خيارات تصدير PDF

قم بإعداد خيارات تصدير PDF، مع تحديد خيارات التحويل المتجهية للـ CAD. هذا أيضًا يوضح قدرة *java convert dxf pdf*:

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);
cadRasterizationOptions.setPageHeight(600);
```

## الخطوة 3: تنفيذ التتبع

نفّذ التتبع باستخدام فئة معالج أخطاء مخصصة. هذه الفئة ستلتقط مشكلات العرض وتظهرها في وحدة التحكم:

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

## المشكلات الشائعة والحلول

- **`NullPointerException` على `RenderResult`** – تأكد من أنك تستخدم Aspose.CAD الإصدار 23.10 أو أحدث؛ الإصدارات القديمة لا تحتوي على واجهة `RenderResult`.  
- **الملف غير موجود** – تحقق من أن `dataDir` يشير إلى المجلد الصحيح وأن اسم الملف مطابق تمامًا، بما في ذلك حالة الأحرف.  
- **عدم وجود مخرجات التتبع** – تأكد من أن `ErrorHandler` المخصص تم تعيينه بشكل صحيح إلى `cadRasterizationOptions.RenderResult`.

## الأسئلة المتكررة

**س:** هل يمكنني تمكين التتبع لتنسيقات ملفات CAD أخرى باستخدام Aspose.CAD للـ Java؟  
**ج:** Aspose.CAD يدعم أساسًا تتبع DWG. بالنسبة للتنسيقات الأخرى، راجع الوثائق الرسمية.

**س:** كيف يمكنني التعامل مع خيارات تصدير إضافية في Aspose.CAD للـ Java؟  
**ج:** استكشف الوثائق الشاملة على [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/).

**س:** هل هناك نسخة تجريبية متاحة لـ Aspose.CAD للـ Java؟  
**ج:** نعم، يمكنك الوصول إلى النسخة التجريبية عبر [Aspose.CAD Free Trial](https://releases.aspose.com/).

**س:** أين يمكنني طلب المساعدة أو مناقشة المشكلات المتعلقة بـ Aspose.CAD للـ Java؟  
**ج:** زر [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) للحصول على دعم المجتمع.

**س:** كيف أحصل على ترخيص مؤقت لـ Aspose.CAD للـ Java؟  
**ج:** اتبع العملية الموضحة في [Temporary License](https://purchase.aspose.com/temporary-license/).

## الخلاصة

تفعيل تتبع DWG في Java باستخدام Aspose.CAD لا يمنحك فقط رؤية لمشكلات التحويل بل يبسط أيضًا سير عمل التصميم التعاوني. باتباع الخطوات أعلاه يمكنك **enable dwg tracking java**، تحويل DXF إلى PDF، ومعالجة أي مشكلات عرض بسلاسة.

---

**آخر تحديث:** 2025-12-09  
**تم الاختبار مع:** Aspose.CAD for Java 24.12  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}