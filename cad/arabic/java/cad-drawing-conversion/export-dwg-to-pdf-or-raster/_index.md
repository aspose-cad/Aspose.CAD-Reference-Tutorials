---
date: 2026-02-17
description: تعلم كيف يمكن لمكتبة Java CAD Aspose.CAD للـ Java تصدير ملفات DWG إلى
  PDF أو صور نقطية بسرعة ودقة.
linktitle: Export DWG to PDF or Raster
second_title: Aspose.CAD Java API
title: تصدير DWG إلى PDF أو Raster باستخدام مكتبة Java CAD Aspose.CAD للـ Java
url: /ar/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تصدير DWG إلى PDF أو صورة نقطية باستخدام مكتبة Java CAD Aspose.CAD for Java

## المقدمة

في عالم التصميم بمساعدة الحاسوب (CAD) المتطور، يعتبر التعامل الفعال مع الرسومات أمرًا حيويًا. باستخدام **مكتبة Java CAD** **Aspose.CAD for Java** يمكنك **تصدير DWG إلى PDF** — أو صور نقطية — في بضع أسطر من الشيفرة فقط. يوضح هذا الدليل العملية بالكامل، من تحميل ملف DWG إلى إنشاء ملف PDF عالي الجودة، مع إبراز سبب كون Aspose.CAD Java المكتبة المفضلة لمهام تحويل CAD.

## إجابات سريعة
- **ماذا يغطي هذا الدليل؟** تصدير ملفات DWG إلى PDF أو صور نقطية باستخدام Aspose.CAD for Java.  
- **هل أحتاج إلى ترخيص؟** يتوفر ترخيص مؤقت مجاني للتقييم؛ يلزم الحصول على ترخيص كامل للإنتاج.  
- **ما نسخة Java المدعومة؟** أي بيئة تشغيل Java 8+ تعمل مع أحدث Aspose.CAD Java API.  
- **هل يمكنني تحويل DWG إلى صيغ صور أخرى؟** نعم – خيارات الرستر نفسها تتيح لك إخراج PNG، JPEG، BMP، إلخ.  
- **كم تستغرق عملية التحويل؟** عادةً أقل من ثانية للرسومات القياسية؛ قد تستغرق الملفات الكبيرة بضع ثوانٍ.

## لماذا تُعد مكتبة Java CAD الخيار الأفضل لتحويل DWG؟

- **تنفيذ Pure Java** – لا توجد ملفات DLL أصلية أو أدوات خارجية.  
- **معالجة دقيقة للوحدات** – يتم اكتشاف الوحدات المترية والإمبراطورية تلقائيًا.  
- **إخراج نقطي عالي الجودة** – تحكم دقيق في DPI وحجم الصفحة.  
- **دعم كامل لـ PDF** – إنشاء PDF يحافظ على المتجهات دون تبعيات إضافية.  
- **ترخيص مرن** – ابدأ بـ **ترخيص مؤقت Aspose** للاختبار، ثم قم بالترقية عند الانتقال إلى الإنتاج.

## ما هو “تصدير DWG إلى PDF”؟

تصدير DWG إلى PDF يعني تحويل رسم AutoCAD الأصلي إلى مستند PDF محمول ومستقل عن الجهاز. يحافظ PDF الناتج على البيانات المتجهة، الطبقات، والقياس، مما يجعله مثاليًا للمشاركة أو الطباعة أو الأرشفة.

## لماذا نستخدم Aspose.CAD Java لهذا التحويل؟

لأن **مكتبة Java CAD** تتولى كل شيء من تحويل الوحدات إلى الرستر داخليًا، مما يجنبك تعقيدات الأدوات الخارجية وتضمن نتائج متسقة عبر الأنظمة.

## المتطلبات المسبقة

قبل الغوص في الشيفرة، تأكد من وجود ما يلي:

- معرفة أساسية ببرمجة Java.  
- مكتبة Aspose.CAD for Java مثبتة. إذا لم تقم بتحميلها بعد، احصل عليها **[من هنا](https://releases.aspose.com/cad/java/)**.  
- ملف DWG للاختبار – يُستخدم الملف النموذجي **Bottom_plate.dwg** في هذا الدليل.

## استيراد المساحات الاسمية

في مشروع Java الخاص بك، استورد الفئات الضرورية لبدء عملية التحويل:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## دليل خطوة بخطوة

### الخطوة 1: تحميل ملف DWG

أولاً، حمّل رسم DWG الخاص بك باستخدام الفئة `Image`. هذا ينشئ تمثيلًا في الذاكرة يمكن لـ Aspose.CAD العمل معه.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

### الخطوة 2: تحديد نوع الوحدة

فهم ما إذا كان الرسم يستخدم وحدات مترية أو إمبراطورية أمر أساسي لضبط القياس بشكل صحيح. تُعيد الدالة المساعدة `IsMetric` (التنفيذ مُحذوف للاختصار) قيمة منطقية.

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

### الخطوة 3: ضبط خيارات الرستر

استنادًا إلى نظام الوحدات، قم بتكوين حجم الصفحة، المقياس، ونوع الوحدة المستهدف. هذه الخيارات تحدد كيفية رستر DWG قبل دمجه في PDF.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();

if (currentUnitIsMetric) {
    // Metric units
    double metersCoeff = 1 / 1000.0;
    double scaleFactor = metersCoeff / currentUnitCoefficient;
    rasterizationOptions.setPageWidth((float)(210 * scaleFactor));
    rasterizationOptions.setPageHeight((float)(297 * scaleFactor));
    rasterizationOptions.setUnitType(UnitType.Millimeter);
} else {
    // Imperial units
    rasterizationOptions.setPageWidth((float)(8.27f / currentUnitCoefficient));
    rasterizationOptions.setPageHeight((float)(11.69f / currentUnitCoefficient));
    rasterizationOptions.setUnitType(UnitType.Inch);
}
```

### الخطوة 4: تكوين خيارات PDF (pdf options cad)

أنشئ كائنًا من `PdfOptions` وأرفق إعدادات الرستر. هذا يخبر Aspose.CAD كيف يدمج المحتوى الرستري في ملف PDF النهائي.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

### الخطوة 5: حفظ كملف PDF

أخيرًا، صدّر الرسم إلى ملف PDF. تأخذ طريقة `save` مسار الإخراج وكائن `PdfOptions` المُكوَّن.

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

عند انتهاء الشيفرة، ستجد **Saved.pdf** في مجلد `DWGDrawings` الخاص بك، جاهزًا للتوزيع أو الأرشفة.

## كيفية تحويل DWG إلى صور نقطية باستخدام مكتبة Java CAD

إذا كنت تحتاج إلى صور نقطية بدلاً من PDF، استبدل ببساطة `PdfOptions` بخيارات الصورة النقطية المناسبة (مثل `PngOptions`، `JpegOptions`). يمكن إعادة استخدام نفس كائن `CadRasterizationOptions`، مما يتيح لك **تحويل DWG إلى صور نقطية** مع تغييرات قليلة في الشيفرة.

## كيفية إنشاء PDF من DWG باستخدام pdf options cad

المثال أعلاه بالفعل **ينتج PDF من DWG**. عبر تعديل `pdfOptions`—مثلاً، تعيين `pdfOptions.setCompress(true)`—يمكنك التحكم في حجم وجودة PDF. يوضح هذا مرونة واجهة برمجة تطبيقات **pdf options cad**.

## المشكلات الشائعة والنصائح

- **حجم الصفحة غير صحيح** – تحقق من منطق تحويل الوحدات؛ قد تتسبب المعاملات غير المتطابقة في صفحات ذات حجم مفرط.  
- **خطوط أو أوزان خطوط مفقودة** – تأكد من أن DWG يشير إلى جميع الموارد الخارجية قبل التحويل.  
- **الأداء مع الرسومات الكبيرة** – زد قيمة `DPI` في `CadRasterizationOptions` فقط عندما تكون الجودة العالية ضرورية؛ القيم الأقل تُسرّع المعالجة.  
- **قضايا الترخيص** – للتقييم يمكنك استخدام **ترخيص مؤقت Aspose**؛ يلزم الحصول على ترخيص كامل للبيئات الإنتاجية.

## الأسئلة المتكررة

**س: هل يمكنني استخدام Aspose.CAD for Java مع أطر عمل Java أخرى؟**  
ج: نعم، يتكامل Aspose.CAD for Java بسلاسة مع أطر عمل Java الشهيرة مثل Spring، Jakarta EE، وAndroid.

**س: هل يتوفر ترخيص مؤقت لـ Aspose.CAD for Java؟**  
ج: نعم، يمكنك الحصول على ترخيص مؤقت **[من هنا](https://purchase.aspose.com/temporary-license/)**.

**س: أين يمكنني العثور على دعم Aspose.CAD for Java؟**  
ج: زر **[منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19)** للحصول على مساعدة من المجتمع ومهندسي Aspose.

**س: كيف يمكنني شراء ترخيص لـ Aspose.CAD for Java؟**  
ج: يمكنك شراء ترخيص **[من هنا](https://purchase.aspose.com/buy)**.

**س: ما الوحدات التي يدعمها Aspose.CAD for Java؟**  
ج: يدعم Aspose.CAD for Java كلًا من الوحدات المترية والإمبراطورية، مع اكتشاف تلقائي لنظام وحدة الرسم.

**س: هل يمكنني تحويل DWG إلى صيغ صور أخرى (مثل PNG، JPEG) باستخدام نفس الـ API؟**  
ج: بالتأكيد. استبدل `PdfOptions` بخيارات الصورة النقطية المناسبة (مثل `PngOptions`) وأعد استخدام نفس `CadRasterizationOptions`.

## الخاتمة

يُظهر هذا الدليل كيفية **تصدير DWG إلى PDF** وصور نقطية باستخدام **مكتبة Java CAD** Aspose.CAD for Java. باتباع الخطوات التفصيلية، يمكنك دمج تحويل CAD موثوق به في أي تطبيق Java، سواء كنت تحتاج إلى ملفات PDF للتوثيق أو صور نقطية للعرض على الويب.

---

**آخر تحديث:** 2026-02-17  
**تم الاختبار مع:** Aspose.CAD for Java 24.10  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}