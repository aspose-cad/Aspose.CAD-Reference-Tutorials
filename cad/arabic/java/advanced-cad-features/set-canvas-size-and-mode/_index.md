---
date: 2026-02-15
description: تعلم كيفية تعيين حجم صفحة PDF وتحويل CAD إلى PDF باستخدام Aspose.CAD
  للـ Java، مع التحجيم التلقائي للتصميم وتصدير TIFF.
linktitle: Set PDF Page Size – Convert CAD to PDF
second_title: Aspose.CAD Java API
title: تحديد حجم صفحة PDF – تحويل CAD إلى PDF (Java)
url: /ar/java/advanced-cad-features/set-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تحديد حجم القماش ووضعه

## المقدمة

إذا كنت بحاجة إلى **تحديد حجم صفحة PDF** أثناء تحويل رسومات CAD إلى PDF، فقد وصلت إلى المكان الصحيح. في هذا الدرس سنوضح لك كيفية استخدام Aspose.CAD for Java لتحديد أبعاد القماش بدقة، وتمكين مقياس التخطيط التلقائي، ثم تصدير النتيجة إلى كل من PDF و TIFF. سواء كنت تُعد مخططات هندسية للطباعة أو تُنشئ صورًا مصغرة لمعرض ويب، فإن التحكم في حجم الصفحة ودقة الإخراج أمر أساسي.

## إجابات سريعة
- **ماذا يعني “تحويل CAD إلى PDF”؟** تحويل رسم CAD (مثل DXF, DWG) إلى مستند PDF يمكن عرضه على أي منصة.  
- **هل يمكنني أيضًا التصدير إلى TIFF؟** نعم—استخدم `TiffOptions` لإنشاء صور نقطية عالية الدقة.  
- **أي خيار يتحكم في حجم القماش في Java؟** `CadRasterizationOptions.setPageWidth/Height`.  
- **ما هو مقياس التخطيط التلقائي؟** علم (`setAutomaticLayoutsScaling(true)`) يحافظ على نسب التخطيط الأصلية عندما يتغير حجم القماش.  
- **هل أحتاج إلى ترخيص لـ Aspose.CAD؟** يلزم الحصول على ترخيص مؤقت أو دائم للاستخدام في الإنتاج.

## كيفية تحديد حجم صفحة PDF عند تحويل CAD إلى PDF (Java)

تحديد حجم صفحة PDF (أو حجم القماش) يتيح لك التحكم في الأبعاد النهائية للمستند، وهو مفيد بشكل خاص عندما تحتاج إلى **تغيير أبعاد PDF** لتتناسب مع معايير الطباعة أو متطلبات واجهة المستخدم. أدناه نستعرض كل خطوة، موضحين *السبب* وراء كل سطر من الشيفرة.

## ما هو **تحويل CAD إلى PDF**؟

تحويل CAD إلى PDF يعني أخذ رسومات هندسية مبنية على المتجهات وتحويلها إلى صفحات PDF، مع الحفاظ على الخطوط، الطبقات، والهندسة مع جعل الملف متاحًا للجميع.

## لماذا تحديد حجم القماش **java**؟

تحديد حجم القماش في Java يتيح لك تعريف دقة الإخراج وأبعاد الصفحة، مما يضمن أن PDF أو TIFF الناتج يطابق متطلبات الطباعة أو العرض الخاصة بك. كما يمنحك التحكم في سلوك المقياس، وهو أمر ضروري للرسومات ذات الصيغ الكبيرة.

## المتطلبات المسبقة

قبل الغوص في الدرس، تأكد من توفر المتطلبات التالية:

- Aspose.CAD for Java: تأكد من تثبيت مكتبة Aspose.CAD في بيئة Java الخاصة بك. يمكنك تنزيلها [هنا](https://releases.aspose.com/cad/java/).
- دليل المستندات: أنشئ دليلًا لتخزين ملفات CAD الخاصة بك. سيُشار إلى هذا الدليل في خطوات الدرس.

الآن، لنبدأ بالدليل خطوة بخطوة.

## استيراد المساحات الاسمية

في هذه الخطوة، سنستورد المساحات الاسمية اللازمة لبدء مشروع Aspose.CAD الخاص بك.

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

في هذا المقتطف، نقوم بتحديد مسار دليل الموارد ونحمّل ملف DXF باستخدام فئة `Image` الخاصة بـ Aspose.CAD.

## الخطوة 2: ضبط خصائص **CadRasterizationOptions** (تحديد حجم القماش java)

```java
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

هنا، ننشئ كائنًا من `CadRasterizationOptions` ونُكوّن الخصائص مثل عرض الصفحة، ارتفاع الصفحة، و**مقياس التخطيط التلقائي**. هذا هو جوهر **تكوين وضع القماش** للتحويل الخاص بك.

## الخطوة 3: إنشاء PdfOptions وتعيين VectorRasterizationOptions

```java
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Set the VectorRasterizationOptions property
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

الآن، ننشئ كائنًا من `PdfOptions` ونعيّن خاصية `VectorRasterizationOptions` له إلى كائن `CadRasterizationOptions` الذي تم تكوينه مسبقًا.

## الخطوة 4: التصدير إلى PDF (تحويل cad إلى pdf)

```java
// Export CAD to PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

أخيرًا، نحفظ صورة CAD إلى ملف PDF باستخدام الخيارات المحددة، مكملين عملية **تحويل CAD إلى PDF**.

## الخطوة 5: إنشاء TiffOptions وتعيين VectorRasterizationOptions (تصدير cad إلى tiff)

```java
// Create an instance of TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Set the VectorRasterizationOptions property
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

في هذه الخطوة، نُعدّ كائنًا من `TiffOptions` ونُكوّن خاصية `VectorRasterizationOptions` الخاصة به.

## الخطوة 6: التصدير إلى TIFF

```java
// Export CAD to TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

أخيرًا، نحفظ صورة CAD إلى ملف TIFF باستخدام الخيارات المحددة، موضحين كيفية **تصدير CAD إلى TIFF** بعد ضبط حجم القماش.

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|-------|-----|
| ملف PDF الناتج فارغ | `setNoScaling(true)` يعطل العرض لبعض الرسومات | احذف `setNoScaling(true)` أو عيّنه إلى `false`. |
| دقة TIFF منخفضة | عرض/ارتفاع الصفحة صغير جدًا | زد قيم `setPageWidth` / `setPageHeight`. |
| التخطيط مشوّه | مقياس التخطيط التلقائي معطل | تأكد من تمكين `setAutomaticLayoutsScaling(true)`. |

## لماذا تعديل حجم القماش وDPI؟

تغيير حجم القماش يؤثر مباشرة على دقة الترصيص (Rasterization) للإخراج. إذا كنت بحاجة إلى **زيادة دقة TIFF**، ما عليك سوى رفع قيم `setPageWidth` / `setPageHeight` أو استدعاء `rasterizationOptions.setResolution(300)` قبل إنشاء `TiffOptions`. سيمنحك ذلك صورًا نقطية عالية الجودة مناسبة للطباعة أو الفحص التفصيلي.

## الأسئلة المتكررة

### س1: هل يمكنني استخدام Aspose.CAD for Java مع أطر عمل Java أخرى؟

ج1: نعم، تم تصميم Aspose.CAD للتكامل السلس مع مختلف أطر عمل Java.

### س2: هل تتوفر رخصة مؤقتة لـ Aspose.CAD؟

ج2: نعم، يمكنك الحصول على رخصة مؤقتة [هنا](https://purchase.aspose.com/temporary-license/).

### س3: أين يمكنني الحصول على دعم المجتمع لـ Aspose.CAD؟

ج3: زر منتدى [Aspose.CAD](https://forum.aspose.com/c/cad/19) للحصول على الدعم والمناقشات.

### س4: هل يمكنني تجربة Aspose.CAD مجانًا؟

ج4: بالتأكيد! احصل على نسخة تجريبية مجانية [هنا](https://releases.aspose.com/).

### س5: كيف يمكنني شراء Aspose.CAD for Java؟

ج5: اشترِ المنتج [هنا](https://purchase.aspose.com/buy).

**أسئلة وإجابات إضافية**

**س: هل يؤثر حجم القماش على جودة المتجهات في PDF؟**  
ج: لا. حجم القماش يتحكم في أبعاد الصفحة؛ تبقى بيانات المتجهات مستقلة عن الدقة، مما يضمن عرضًا واضحًا عند أي مستوى تكبير.

**س: هل يمكنني تعيين DPI مختلف لإخراج TIFF؟**  
ج: نعم. عدّل `rasterizationOptions.setResolution(dpiValue)` قبل إنشاء `TiffOptions`.

**س: كيف يمكنني **تغيير أبعاد PDF** لملف PDF موجود دون إعادة تصيير CAD؟**  
ج: استخدم Aspose.PDF لتحميل الـ PDF المُنتج واستدعِ `pdf.getPages().setPageSize(PageSize.A4)` أو حجم مخصص آخر.

**س: ما هي أفضل طريقة **لتحويل dxf إلى pdf** مع الحفاظ على الطبقات؟**  
ج: احتفظ بـ `setAutomaticLayoutsScaling(true)` وتجنب `setNoScaling(true)`؛ فهذا يحافظ على رؤية الطبقات ودقة التخطيط.

## الخلاصة

تهانينا! لقد نجحت في **تحويل CAD إلى PDF** و**تصدير CAD إلى TIFF** مع **تحديد حجم القماش java**، مفعّلاً **مقياس التخطيط التلقائي**، وتعلمت كيفية **تكوين وضع القماش** للحصول على مخرجات عالية الجودة. يوفر هذا الدرس أساسًا قويًا لمشاريع تحويل CAD الخاصة بك. استكشف المزيد من الميزات والاحتمالات في [توثيق Aspose.CAD](https://reference.aspose.com/cad/java/).

---

**آخر تحديث:** 2026-02-15  
**تم الاختبار مع:** Aspose.CAD for Java 24.12  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}