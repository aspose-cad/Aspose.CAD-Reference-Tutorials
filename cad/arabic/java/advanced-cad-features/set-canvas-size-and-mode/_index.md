---
date: 2026-08-29
description: تعلم كيفية تعيين حجم صفحة pdf وتحويل CAD إلى PDF باستخدام Aspose.CAD
  للـ Java، مع automatic layout scaling وتصدير TIFF.
keywords:
- set pdf page size
- convert cad to pdf
- canvas size java
- high resolution tiff
- change pdf dimensions
lastmod: 2026-08-29
linktitle: تعيين حجم صفحة pdf – تحويل cad إلى pdf
og_description: تعلم كيفية تعيين حجم صفحة pdf أثناء تحويل رسومات CAD إلى PDF في Java
  باستخدام Aspose.CAD. يغطي هذا الدليل canvas dimensions، automatic layout scaling،
  وتصدير إلى high‑resolution TIFF.
og_image_alt: Tutorial showing how to set pdf page size and convert CAD to PDF in
  Java
og_title: تعيين حجم صفحة pdf – تحويل CAD إلى PDF باستخدام Aspose في Java
schemas:
- author: Aspose
  dateModified: '2026-08-29'
  description: Learn how to set pdf page size and convert CAD to PDF using Aspose.CAD
    for Java, with automatic layout scaling and TIFF export.
  headline: Set pdf page size – convert cad to pdf (Java)
  type: TechArticle
- questions:
  - answer: No. Canvas size controls page dimensions; vector data remains resolution‑independent,
      ensuring crisp rendering at any zoom level.
    question: does the canvas size affect vector quality in the PDF?
  - answer: Yes. Adjust `rasterizationOptions.setResolution(dpiValue)` before creating
      `TiffOptions`.
    question: can I set a different DPI for the TIFF output?
  - answer: Use Aspose.PDF to load the generated PDF and call `pdf.getPages().setPageSize(PageSize.A4)`
      or a custom size.
    question: how can I change PDF dimensions for an existing PDF without re‑rendering
      the CAD?
  - answer: Keep `setAutomaticLayoutsScaling(true)` and avoid `setNoScaling(true)`;
      this retains layer visibility and layout fidelity.
    question: what is the best way to convert dxf to pdf while preserving layers?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- set pdf page size
- convert cad
- Aspose.CAD
- Java
- high resolution tiff
title: تعيين حجم صفحة pdf – تحويل cad إلى pdf (Java)
url: /ar/java/advanced-cad-features/set-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تعيين حجم صفحة PDF – تحويل CAD إلى PDF (Java)

## مقدمة

إذا كنت بحاجة إلى **تعيين حجم صفحة PDF** أثناء تحويل رسومات CAD إلى PDF، فقد وصلت إلى المكان الصحيح. في هذا البرنامج التعليمي سنوضح لك كيفية استخدام Aspose.CAD for Java لتحديد أبعاد القماش الدقيقة، وتمكين مقياس التخطيط التلقائي، ثم تصدير النتيجة إلى كل من PDF وTIFF. سواء كنت تُعد المخططات الهندسية للطباعة أو تُنشئ صورًا مصغرة لمعرض ويب، فإن التحكم في حجم الصفحة ودقة الإخراج أمر أساسي.

## إجابات سريعة
- **ما معنى “convert CAD to PDF”؟** تحويل رسم CAD (مثل DXF, DWG) إلى مستند PDF يمكن عرضه على أي منصة.  
- **هل يمكنني أيضًا التصدير إلى TIFF؟** نعم—استخدم `TiffOptions` لإنشاء صور نقطية عالية الدقة.  
- **ما الخيار الذي يتحكم في حجم القماش في Java؟** `CadRasterizationOptions.setPageWidth/Height`.  
- **ما هو مقياس التخطيط التلقائي؟** علامة (`setAutomaticLayoutsScaling(true)`) تحافظ على نسب التخطيط الأصلية عندما يتغير حجم القماش.  
- **هل أحتاج إلى ترخيص لـ Aspose.CAD؟** يلزم الحصول على ترخيص مؤقت أو دائم للاستخدام في الإنتاج.

## كيفية تعيين حجم صفحة PDF عند تحويل CAD إلى PDF في Java

حمّل ملف CAD الخاص بك، وقم بتكوين `CadRasterizationOptions` بالعرض والارتفاع المطلوبين، ومكّن مقياس التخطيط التلقائي، ثم احفظ النتيجة كملف PDF. يتيح لك هذا النهج المكوّن من خطوتين التحكم في الأبعاد الدقيقة لصفحة الإخراج دون التضحية بجودة المتجه.

## ما هو تحويل CAD إلى PDF؟

يعني تحويل CAD إلى PDF أخذ الرسومات الهندسية القائمة على المتجهات وتحويلها إلى صفحات PDF، مع الحفاظ على الخطوط والطبقات والهندسة مع جعل الملف متاحًا عالميًا. تقوم العملية بتحويل الرسم إلى نقطية وفقًا للخيارات المحددة، مما ينتج PDF يمكن فتحه على أي جهاز دون الحاجة إلى برنامج CAD، ويحتفظ بالوضوح البصري للتصميم الأصلي.

## لماذا تعيين حجم القماش في Java؟

يتيح لك تعيين حجم القماش في Java تحديد دقة الإخراج وأبعاد الصفحة، مما يضمن أن PDF أو TIFF الناتج يتطابق مع متطلبات الطباعة أو العرض الخاصة بك. كما يمنحك التحكم في سلوك التحجيم، وهو أمر أساسي للرسومات ذات الصيغ الكبيرة.

## المتطلبات المسبقة

قبل الغوص في البرنامج التعليمي، تأكد من توفر المتطلبات المسبقة التالية:

- Aspose.CAD for Java: تأكد من تثبيت مكتبة Aspose.CAD في بيئة Java الخاصة بك. يمكنك تنزيل مكتبة Aspose.CAD for Java من [هنا](https://releases.aspose.com/cad/java/).
- دليل المستندات: قم بإعداد دليل لتخزين ملفات CAD الخاصة بك. سيتم الإشارة إلى هذا الدليل في خطوات البرنامج التعليمي.

الآن، لنبدأ دليل الخطوة بخطوة.

## استيراد مساحات الأسماء

في هذه الخطوة، سنستورد مساحات الأسماء الضرورية لبدء مشروع Aspose.CAD الخاص بك.

`Image` هي الفئة الرئيسية المستخدمة لتحميل ملفات CAD.

```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## الخطوة 1: استيراد فئات Aspose.CAD

توفر فئة `Image` طرقًا لتحميل وحفظ رسومات CAD.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

في هذا المقتطف، نقوم بإعداد مسار دليل الموارد ونحمّل ملف DXF باستخدام فئة `Image` من Aspose.CAD.

## الخطوة 2: تعيين خصائص CadRasterizationOptions (تعيين حجم القماش في Java)

`CadRasterizationOptions` يحدد إعدادات التحويل إلى نقطية مثل حجم الصفحة والتحجيم لتحويل CAD إلى نقطية.

```java
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

هنا، ننشئ مثيلًا من `CadRasterizationOptions` ونضبط الخصائص مثل عرض الصفحة، ارتفاع الصفحة، و**مقياس التخطيط التلقائي**. هذا هو جوهر **تكوين وضع القماش** لتحويلك.

## الخطوة 3: إنشاء PdfOptions وتعيين vectorRasterizationOptions

`PdfOptions` يحدد إعدادات إخراج PDF للتحويل.

```java
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Set the VectorRasterizationOptions property
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

الآن، ننشئ مثيلًا من `PdfOptions` ونعيّن خاصية `VectorRasterizationOptions` إلى `CadRasterizationOptions` التي تم تكوينها مسبقًا.

## الخطوة 4: تصدير إلى PDF (تحويل CAD إلى PDF)

```java
// Export CAD to PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

أخيرًا، نحفظ صورة CAD كملف PDF باستخدام الخيارات المحددة، مكملين عملية **تحويل CAD إلى PDF**.

## الخطوة 5: إنشاء TiffOptions وتعيين vectorRasterizationOptions (تصدير CAD إلى TIFF)

`TiffOptions` يضبط معلمات إخراج TIFF مثل الضغط والدقة.

```java
// Create an instance of TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Set the VectorRasterizationOptions property
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## الخطوة 6: تصدير إلى TIFF

```java
// Export CAD to TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

أخيرًا، نحفظ صورة CAD كملف TIFF باستخدام الخيارات المحددة، موضحين كيفية **تصدير CAD إلى TIFF** بعد تكوين حجم القماش.

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|-------|-----|
| ملف PDF الناتج فارغ | `setNoScaling(true)` يعطل العرض لبعض الرسومات | أزل `setNoScaling(true)` أو عيّنه إلى `false`. |
| دقة TIFF منخفضة | عرض/ارتفاع الصفحة صغير جدًا | زد قيم `setPageWidth` / `setPageHeight`. |
| التخطيط مشوه | مقياس التخطيط التلقائي معطل | تأكد من تمكين `setAutomaticLayoutsScaling(true)`. |

## لماذا تعديل حجم القماش و DPI؟

تغيير حجم القماش يؤثر مباشرة على دقة التحويل إلى نقطية للإخراج. إذا كنت بحاجة إلى **زيادة دقة TIFF**، ما عليك سوى رفع قيم `setPageWidth` / `setPageHeight` أو استدعاء `rasterizationOptions.setResolution(300)` قبل إنشاء `TiffOptions`. هذا يمنحك صورًا نقطية عالية الجودة مناسبة للطباعة أو الفحص التفصيلي.

## الأسئلة المتكررة

**س1: هل يمكنني استخدام Aspose.CAD for Java مع أطر Java الأخرى؟**  
ج: نعم، تم تصميم Aspose.CAD لتتكامل بسلاسة مع أطر Java المختلفة.

**س2: هل تتوفر ترخيص مؤقت لـ Aspose.CAD؟**  
ج: نعم، يمكنك الحصول على صفحة الترخيص المؤقت من [هنا](https://purchase.aspose.com/temporary-license/).

**س3: أين يمكنني الحصول على دعم المجتمع لـ Aspose.CAD؟**  
ج: زر منتدى Aspose.CAD [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) للحصول على دعم المجتمع والنقاشات.

**س4: هل يمكنني تجربة Aspose.CAD مجانًا؟**  
ج: بالتأكيد! احصل على صفحة تحميل التجربة المجانية من [هنا](https://releases.aspose.com/).

**س5: كيف يمكنني شراء Aspose.CAD for Java؟**  
ج: اشترِ Aspose.CAD for Java من [هنا](https://purchase.aspose.com/buy).

**س: هل يؤثر حجم القماش على جودة المتجه في PDF؟**  
ج: لا. حجم القماش يتحكم في أبعاد الصفحة؛ تظل بيانات المتجه مستقلة عن الدقة، مما يضمن عرضًا واضحًا عند أي مستوى تكبير.

**س: هل يمكنني تعيين DPI مختلف لإخراج TIFF؟**  
ج: نعم. اضبط `rasterizationOptions.setResolution(dpiValue)` قبل إنشاء `TiffOptions`.

**س: كيف يمكنني تغيير أبعاد PDF لملف PDF موجود دون إعادة تحويل CAD؟**  
ج: استخدم Aspose.PDF لتحميل PDF المُنشأ واستدعِ `pdf.getPages().setPageSize(PageSize.A4)` أو حجم مخصص.

**س: ما هي أفضل طريقة لتحويل dxf إلى pdf مع الحفاظ على الطبقات؟**  
ج: احتفظ بـ `setAutomaticLayoutsScaling(true)` وتجنب `setNoScaling(true)`؛ هذا يحافظ على رؤية الطبقات ودقة التخطيط.

## الخلاصة

تهانينا! لقد نجحت في **تحويل CAD إلى PDF** و**تصدير CAD إلى TIFF** مع **تعيين حجم القماش في Java**، مفعلاً **مقياس التخطيط التلقائي**، وتعلمت كيفية **تكوين وضع القماش** للحصول على مخرجات عالية الجودة. يوفر هذا البرنامج التعليمي أساسًا قويًا لمشاريع تحويل CAD الخاصة بك. استكشف المزيد من الميزات والإمكانات في [وثائق Aspose.CAD](https://reference.aspose.com/cad/java/).

---

**آخر تحديث:** 2026-08-29  
**تم الاختبار مع:** Aspose.CAD for Java 24.12  
**المؤلف:** Aspose

## دروس ذات صلة

- [تعيين حجم القماش – ميزات CAD المتقدمة مع Aspose.CAD for Java](/cad/java/advanced-cad-features/)
- [تصدير DWG إلى PDF في Java – تعيين حجم صفحة PDF باستخدام Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)
- [تعيين حجم صفحة مخصص – PDF من CAD مع مقياس التخطيط التلقائي](/cad/java/advanced-cad-features/setting-auto-layout-scaling/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}