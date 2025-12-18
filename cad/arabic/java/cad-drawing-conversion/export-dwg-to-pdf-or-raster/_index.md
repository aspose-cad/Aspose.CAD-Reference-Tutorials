---
date: 2025-12-18
description: استكشف كيفية تصدير ملفات DWG إلى PDF أو صور نقطية في Java باستخدام Aspose.CAD.
  يضمن هذا الدليل خطوة بخطوة الدقة والكفاءة وسهولة تحويل ملفات DWG.
linktitle: Export DWG to PDF or Raster
second_title: Aspose.CAD Java API
title: تصدير DWG إلى PDF أو صورة نقطية باستخدام Aspose.CAD للـ Java
url: /ar/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تصدير DWG إلى PDF أو صورة نقطية باستخدام Aspose.CAD للـ Java

## المقدمة

في عالم التصميم بمساعدة الحاسوب (CAD) المتطور، يُعد التعامل الفعّال مع الرسومات أمرًا حيويًا. باستخدام **Aspose.CAD للـ Java** يمكنك **تصدير dwg إلى pdf** — أو إلى صور نقطية — في بضع أسطر من الشيفرة فقط. يوضح هذا الدليل العملية بالكامل، من تحميل ملف DWG إلى إنشاء ملف PDF عالي الجودة، مع إبراز سبب كون Aspose.CAD Java المكتبة المفضلة لمهام تحويل CAD.

## إجابات سريعة
- **ما الذي يغطيه هذا الدليل؟** تصدير ملفات DWG إلى PDF أو صور نقطية باستخدام Aspose.CAD للـ Java.  
- **هل أحتاج إلى ترخيص؟** يتوفر ترخيص مؤقت مجاني للتقييم؛ يلزم الحصول على ترخيص كامل للإنتاج.  
- **ما نسخة Java المدعومة؟** أي بيئة تشغيل Java 8+ تعمل مع أحدث API لـ Aspose.CAD Java.  
- **هل يمكنني تحويل DWG إلى صيغ صور أخرى؟** نعم – تسمح خيارات الرستر نفسها بإنتاج PNG، JPEG، BMP، إلخ.  
- **كم تستغرق عملية التحويل؟** عادةً أقل من ثانية للرسومات القياسية؛ قد تستغرق الملفات الكبيرة بضع ثوانٍ.

## ما معنى “export dwg to pdf”؟
يعني تصدير DWG إلى PDF تحويل رسم AutoCAD الأصلي إلى مستند PDF محمول ومستقل عن الجهاز. يحافظ PDF الناتج على البيانات المتجهية، الطبقات، والقياس، مما يجعله مثاليًا للمشاركة، الطباعة، أو الأرشفة.

## لماذا نستخدم Aspose.CAD Java لهذا التحويل؟
- **بدون تبعيات خارجية** – جافا صافية، بدون ملفات DLL أصلية.  
- **معالجة دقيقة للوحدات** – يحترم تلقائيًا الوحدات المترية أو الإمبريالية.  
- **إخراج نقطي عالي الجودة** – تحكم دقيق في DPI وحجم الصفحة.  
- **دعم كامل للـ PDF** – إنشاء PDF يحافظ على المتجهات دون الحاجة إلى مكتبات إضافية.

## المتطلبات المسبقة

قبل الغوص في الشيفرة، تأكد من وجود ما يلي:

- معرفة أساسية ببرمجة Java.  
- مكتبة Aspose.CAD للـ Java مثبتة. إذا لم تقم بتحميلها بعد، احصل عليها **[من هنا](https://releases.aspose.com/cad/java/)**.  
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

أولاً، حمّل رسم DWG باستخدام الفئة `Image`. هذا ينشئ تمثيلًا في الذاكرة يمكن لـ Aspose.CAD التعامل معه.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

### الخطوة 2: تحديد نوع الوحدة

فهم ما إذا كان الرسم يستخدم الوحدات المترية أو الإمبريالية أمر أساسي للحصول على مقياس صحيح. تُعيد الطريقة المساعدة `IsMetric` (التنفيذ مُهمل للاختصار) قيمة منطقية.

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

### الخطوة 3: ضبط خيارات الرستر

استنادًا إلى نظام الوحدات، اضبط حجم الصفحة، المقياس، ونوع الوحدة المستهدف. تُحدد هذه الخيارات كيفية رستر DWG قبل دمجه في PDF.

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

### الخطوة 4: تكوين خيارات PDF

أنشئ كائنًا من `PdfOptions` وأرفق إعدادات الرستر. هذا يخبر Aspose.CAD كيف يدمج المحتوى الرستري في ملف PDF النهائي.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

### الخطوة 5: حفظ كملف PDF

أخيرًا، صدّر الرسم إلى ملف PDF. تأخذ طريقة `save` مسار الإخراج وإعدادات `PdfOptions` المُكوَّنة.

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

عند انتهاء الشيفرة، ستجد **Saved.pdf** في مجلد `DWGDrawings` الخاص بك، جاهزًا للتوزيع أو الأرشفة.

## المشكلات الشائعة والنصائح

- **حجم الصفحة غير صحيح** – تحقق من منطق تحويل الوحدات؛ قد تُنتج معاملات غير متطابقة صفحات ذات حجم زائد.  
- **الخطوط أو سمك الخط مفقود** – تأكد من أن DWG يشير إلى أي موارد خارجية قبل التحويل.  
- **الأداء مع الرسومات الكبيرة** – زد قيمة `DPI` في `CadRasterizationOptions` فقط عندما تحتاج إلى جودة أعلى؛ قيمة DPI أقل تُسرّع المعالجة.

## الأسئلة المتكررة

**س: هل يمكنني استخدام Aspose.CAD للـ Java مع أطر عمل Java أخرى؟**  
ج: نعم، يتكامل Aspose.CAD للـ Java بسلاسة مع أطر عمل Java الشهيرة مثل Spring، Jakarta EE، وAndroid.

**س: هل يتوفر ترخيص مؤقت لـ Aspose.CAD للـ Java؟**  
ج: نعم، يمكنك الحصول على ترخيص مؤقت **[من هنا](https://purchase.aspose.com/temporary-license/)**.

**س: أين يمكنني العثور على دعم لـ Aspose.CAD للـ Java؟**  
ج: زر **[منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19)** للحصول على مساعدة من المجتمع ومهندسي Aspose.

**س: كيف يمكنني شراء ترخيص لـ Aspose.CAD للـ Java؟**  
ج: يمكنك شراء ترخيص **[من هنا](https://purchase.aspose.com/buy)**.

**س: ما الوحدات التي يدعمها Aspose.CAD للـ Java؟**  
ج: يدعم Aspose.CAD للـ Java كلًا من الوحدات المترية والإمبريالية، مع اكتشاف تلقائي لنظام وحدة الرسم.

**س: هل يمكنني تحويل DWG إلى صيغ صور أخرى (مثل PNG، JPEG) باستخدام نفس الـ API؟**  
ج: بالتأكيد. استبدل `PdfOptions` بخيارات الصورة النقطية المناسبة (مثل `PngOptions`) وأعد استخدام نفس `CadRasterizationOptions`.

## الخاتمة

عرض هذا الدليل كيفية **export dwg to pdf** وإلى صور نقطية باستخدام Aspose.CAD للـ Java. باتباع الدليل خطوة بخطوة، يمكنك دمج تحويل CAD موثوق به في أي تطبيق Java، سواء كنت تحتاج إلى ملفات PDF للتوثيق أو صور نقطية للعرض على الويب.

---

**آخر تحديث:** 2025-12-18  
**تم الاختبار مع:** Aspose.CAD للـ Java 24.10  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}