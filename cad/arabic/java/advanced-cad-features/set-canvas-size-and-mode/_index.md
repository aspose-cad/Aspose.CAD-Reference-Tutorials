---
date: 2025-12-10
description: تعلم كيفية تحويل ملفات CAD إلى PDF باستخدام Aspose.CAD للغة Java مع ضبط
  حجم اللوحة، وتوسيع التخطيط تلقائيًا، وتصدير إلى TIFF.
linktitle: Convert CAD to PDF – Set Canvas Size & Mode
second_title: Aspose.CAD Java API
title: تحويل CAD إلى PDF – تعيين حجم اللوحة والوضع (Java)
url: /ar/java/advanced-cad-features/set-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تعيين حجم اللوحة ووضعها

## المقدمة

هل تبحث عن **convert CAD to PDF** مع التحكم الكامل في حجم اللوحة ووضعية العرض؟ يقدّم هذا الدليل الشامل الخطوات الدقيقة لتعيين حجم اللوحة في Java، وتمكين مقياس التخطيط التلقائي، ثم تصدير النتيجة إلى صيغتي PDF وTIFF باستخدام Aspose.CAD. سواءً كنت تُحسّن خط أنابيب الإنتاج أو تجرب نموذجًا أوليًا، ستجد هنا تعليمات واضحة وقابلة للتنفيذ.

## إجابات سريعة
- **ماذا يعني “convert CAD to PDF”؟** تحويل رسم CAD (مثل DXF، DWG) إلى مستند PDF يمكن عرضه على أي منصة.  
- **هل يمكنني أيضًا التصدير إلى TIFF؟** نعم—استخدم `TiffOptions` لإنشاء صور نقطية عالية الدقة.  
- **أي خيار يتحكم في حجم اللوحة في Java؟** `CadRasterizationOptions.setPageWidth/Height`.  
- **ما هو مقياس التخطيط التلقائي؟** علم (`setAutomaticLayoutsScaling(true)`) يحافظ على نسب التخطيط الأصلية عند تغيير حجم اللوحة.  
- **هل أحتاج إلى ترخيص لـ Aspose.CAD؟** يلزم الحصول على ترخيص مؤقت أو دائم للاستخدام في الإنتاج.

## ما هو **convert CAD to PDF**؟

تحويل CAD إلى PDF يعني أخذ الرسومات الهندسية القائمة على المتجهات وعرضها كصفحات PDF، مع الحفاظ على الخطوط والطبقات والهندسة مع جعل الملف متاحًا للجميع.

## لماذا نعيّن حجم اللوحة **java**؟

تعيين حجم اللوحة في Java يتيح لك تحديد دقة الإخراج وأبعاد الصفحة، مما يضمن أن ملف PDF أو TIFF الناتج يطابق متطلبات الطباعة أو العرض الخاصة بك. كما يمنحك تحكمًا في سلوك المقياس، وهو أمر أساسي للرسومات ذات الصيغ الكبيرة.

## المتطلبات المسبقة

قبل الغوص في الشرح، تأكد من توفر المتطلبات التالية:

- Aspose.CAD for Java: تأكد من تثبيت مكتبة Aspose.CAD في بيئة Java الخاصة بك. يمكنك تنزيلها [هنا](https://releases.aspose.com/cad/java/).

- دليل المستندات: أنشئ دليلًا لتخزين ملفات CAD الخاصة بك. سيُشار إلى هذا الدليل في خطوات الشرح.

الآن، لنبدأ الدليل خطوة بخطوة.

## استيراد النطاقات

في هذه الخطوة، سنستورد النطاقات اللازمة لبدء مشروع Aspose.CAD الخاص بك.

```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## الخطوة 1: استيراد فئات Aspose.CAD

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

في هذا المقتطف، نحدد مسار دليل الموارد ونحمّل ملف DXF باستخدام فئة `Image` الخاصة بـ Aspose.CAD.

## الخطوة 2: تعيين خصائص **CadRasterizationOptions** (set canvas size java)

```java
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

هنا، ننشئ كائنًا من `CadRasterizationOptions` ونضبط الخصائص مثل عرض الصفحة، ارتفاع الصفحة، و**مقياس التخطيط التلقائي**. هذا هو جوهر **configure canvas mode** للتحويل الخاص بك.

## الخطوة 3: إنشاء PdfOptions وتعيين VectorRasterizationOptions

```java
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Set the VectorRasterizationOptions property
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

الآن، ننشئ كائنًا من `PdfOptions` ونعيّن خاصية `VectorRasterizationOptions` إلى كائن `CadRasterizationOptions` الذي تم تكوينه مسبقًا.

## الخطوة 4: التصدير إلى PDF (convert cad to pdf)

```java
// Export CAD to PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

أخيرًا، نحفظ صورة CAD كملف PDF باستخدام الخيارات المحددة، مكتملين عملية **convert CAD to PDF**.

## الخطوة 5: إنشاء TiffOptions وتعيين VectorRasterizationOptions (export cad to tiff)

```java
// Create an instance of TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Set the VectorRasterizationOptions property
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

في هذه الخطوة، نُعد كائنًا من `TiffOptions` ونضبط خاصية `VectorRasterizationOptions` الخاصة به.

## الخطوة 6: التصدير إلى TIFF

```java
// Export CAD to TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

أخيرًا، نحفظ صورة CAD كملف TIFF باستخدام الخيارات المحددة، موضحين كيفية **export CAD to TIFF** بعد تكوين حجم اللوحة.

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|-------|-----|
| ملف PDF الناتج فارغ | `setNoScaling(true)` يعطل العرض لبعض الرسومات | أزل `setNoScaling(true)` أو اضبطه على `false`. |
| دقة TIFF منخفضة | عرض/ارتفاع الصفحة صغير جدًا | زد قيم `setPageWidth` / `setPageHeight`. |
| التخطيط مشوّه | مقياس التخطيط التلقائي غير مفعّل | تأكد من تمكين `setAutomaticLayoutsScaling(true)`. |

## الخلاصة

تهانينا! لقد نجحت في **convert CAD to PDF** و**export CAD to TIFF** مع **set canvas size java**، مفعّلاً **automatic layout scaling**، وتعلمت كيفية **configure canvas mode** للحصول على مخرجات عالية الجودة. يوفر هذا الشرح أساسًا قويًا لمشاريع تحويل CAD الخاصة بك. استكشف المزيد من الميزات والاحتمالات في [توثيق Aspose.CAD](https://reference.aspose.com/cad/java/).

## الأسئلة المتكررة

### س1: هل يمكنني استخدام Aspose.CAD for Java مع أطر عمل Java أخرى؟

ج1: نعم، تم تصميم Aspose.CAD لتتكامل بسلاسة مع مختلف أطر عمل Java.

### س2: هل يتوفر ترخيص مؤقت لـ Aspose.CAD؟

ج2: نعم، يمكنك الحصول على ترخيص مؤقت [هنا](https://purchase.aspose.com/temporary-license/).

### س3: أين يمكنني الحصول على دعم المجتمع لـ Aspose.CAD؟

ج3: زر [منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19) للحصول على دعم المجتمع والنقاشات.

### س4: هل يمكنني تجربة Aspose.CAD مجانًا؟

ج4: بالتأكيد! احصل على نسخة تجريبية مجانية [هنا](https://releases.aspose.com/).

### س5: كيف يمكنني شراء Aspose.CAD for Java؟

ج5: اشترِ المنتج [هنا](https://purchase.aspose.com/buy).

**أسئلة وإجابات إضافية**

**س: هل يؤثر حجم اللوحة على جودة المتجهات في PDF؟**  
ج: لا. حجم اللوحة يتحكم بأبعاد الصفحة؛ تظل بيانات المتجهات مستقلة عن الدقة، مما يضمن عرضًا واضحًا عند أي مستوى تكبير.

**س: هل يمكنني تعيين DPI مختلف لإخراج TIFF؟**  
ج: نعم. اضبط `rasterizationOptions.setResolution(dpiValue)` قبل إنشاء `TiffOptions`.

---

**آخر تحديث:** 2025-12-10  
**تم الاختبار مع:** Aspose.CAD for Java 24.12  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}