---
date: 2026-10-14
description: تعرّف على كيفية تمكين مكتبة Java CAD Aspose.CAD للـ Java من تصدير DWG
  إلى PDF أو raster images بسرعة ودقة.
keywords:
- export dwg pdf
- high quality pdf
- dwg to pdf tutorial
- aspose cad java
- java cad library
lastmod: 2026-10-14
linktitle: تصدير DWG و PDF و raster images
og_description: تصدير DWG إلى PDF بسرعة باستخدام Aspose.CAD للـ Java. تعرّف على تحويل
  PDF عالي الجودة، خيارات raster، والترخيص في هذا الدليل خطوة بخطوة.
og_image_alt: Tutorial showing Java code to convert DWG drawings to PDF and raster
  formats with Aspose.CAD
og_title: تصدير DWG و PDF و raster images باستخدام مكتبة Java CAD Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-10-14'
  description: Learn how the Java CAD library Aspose.CAD for Java can export DWG to
    PDF or raster images quickly and accurately.
  headline: Export DWG PDF and raster images using Java CAD library Aspose.CAD
  type: TechArticle
- description: Learn how the Java CAD library Aspose.CAD for Java can export DWG to
    PDF or raster images quickly and accurately.
  name: Export DWG PDF and raster images using Java CAD library Aspose.CAD
  steps:
  - name: Load the DWG file
    text: First, load your DWG drawing using the `Image` class. This creates an in‑memory
      representation that Aspose.CAD can work with.
  - name: Determine unit type
    text: Understanding whether the drawing uses metric or imperial units is essential
      for correct scaling. The helper method `IsMetric` (implementation omitted for
      brevity) returns a boolean flag.
  - name: Set rasterization options
    text: The `CadRasterizationOptions` class defines rasterization parameters such
      as DPI, page size, and unit conversion. Based on the unit system, configure
      page size, scaling, and the target unit type. These options drive how the DWG
      is rasterized before being wrapped into a PDF.
  - name: Configure PDF options (pdf options cad)
    text: The `PdfOptions` class specifies PDF‑specific settings, including compression
      and metadata. Create a `PdfOptions` instance and attach the rasterization settings.
      This tells Aspose.CAD how to embed the rasterized content into the final PDF.
  - name: Save as PDF
    text: The `save` method writes the image to the given file path using the supplied
      options. Finally, export the drawing to a PDF file. The `save` method takes
      the output path and the configured `PdfOptions`. When the code finishes, you’ll
      find **Saved.pdf** in your `DWGDrawings` folder, ready for distribu
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD for Java seamlessly integrates with popular Java frameworks
      such as Spring, Jakarta EE, and Android.
    question: Can I use Aspose.CAD for Java with other Java frameworks?
  - answer: Yes, you can obtain a temporary license **[obtain a temporary license](https://purchase.aspose.com/temporary-license/)**.
    question: Is a temporary license available for Aspose.CAD for Java?
  - answer: Visit the **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)** for
      assistance from the community and Aspose engineers.
    question: Where can I find support for Aspose.CAD for Java?
  - answer: You can purchase a license **[purchase a license](https://purchase.aspose.com/buy)**.
    question: How can I purchase a license for Aspose.CAD for Java?
  - answer: Aspose.CAD for Java supports both metric and imperial units, automatically
      detecting the drawing’s unit system.
    question: What units does Aspose.CAD for Java support?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- export dwg
- aspose.cad
- java cad conversion
title: تصدير DWG و PDF و raster images باستخدام مكتبة Java CAD Aspose.CAD
url: /ar/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تصدير ملفات DWG PDF والصور النقطية باستخدام مكتبة CAD للغة Java Aspose.CAD

## المقدمة

يُعد تصدير DWG إلى PDF مطلبًا شائعًا للمهندسين والمعماريين وأي شخص يحتاج إلى مشاركة رسومات CAD دون الكشف عن تنسيق الملف الأصلي. باستخدام **Aspose.CAD for Java**، يمكنك **export dwg pdf** — أو الصور النقطية — في بضع أسطر من كود Java فقط، مع الحفاظ على دقة المتجهات وتحديد التخطيط. يوضح هذا الدرس كيفية تحميل ملف DWG، وضبط خيارات الرستر، وحفظ النتيجة كملف PDF عالي الجودة أو كصورة. ستتعرف أيضًا على سبب كون Aspose.CAD المكتبة المفضلة لتحويل CAD في Java بموثوقية وعبر منصات متعددة.

للحصول على دليل مركّز حول تحويل PDF فقط، راجع [دليل تحويل DWG إلى PDF](/java/cad-drawing-conversion/export-dwg-to-pdf/).

## إجابات سريعة
- **ما الذي يغطيه هذا الدرس؟** تصدير ملفات DWG إلى PDF أو الصور النقطية باستخدام Aspose.CAD للغة Java.  
- **هل أحتاج إلى ترخيص؟** يتوفر ترخيص مؤقت مجاني للتقييم؛ يلزم ترخيص كامل للإنتاج.  
- **ما إصدار Java المدعوم؟** أي بيئة تشغيل Java 8+ تعمل مع أحدث Aspose.CAD Java API.  
- **هل يمكنني تحويل DWG إلى صيغ صور أخرى؟** نعم – تسمح خيارات الرستر نفسها بإخراج PNG، JPEG، BMP، إلخ.  
- **كم يستغرق التحويل من وقت؟** عادةً أقل من ثانية للرسومات القياسية؛ قد تستغرق الملفات الكبيرة بضع ثوانٍ.

## لماذا مكتبة CAD للغة Java هي الخيار الأفضل لتحويل DWG؟

Aspose.CAD for Java هو الخيار الأفضل لأنه يوفر تنفيذًا بحتًا للغة Java لا يتطلب ملفات DLL أصلية، يكتشف تلقائيًا الوحدات المترية أو الإمبراطورية، ينتج مخرجات رستر بدقة تصل إلى 1200 DPI، ويولد ملفات PDF تحافظ على المتجهات دون الاعتماد على مكونات خارجية. كما تقدم المكتبة نموذج ترخيص مرن يتيح لك البدء بترخيص مؤقت والتوسع إلى الاستخدام المؤسسي.

## ما هو “export dwg to pdf”؟

`Export dwg pdf` هو عملية تحويل ملف رسم DWG الأصلي إلى مستند PDF مع الحفاظ على بيانات المتجهات، الطبقات، والقياس. ينتج عن هذا التحويل ملفًا مستقلًا عن الجهاز يمكن عرضه على أي منصة دون الحاجة إلى AutoCAD. بما أن PDF يحتفظ بالمعلومات المتجهة، يبقى النص قابلًا للبحث وتظل الرسومات واضحة عند أي مستوى تكبير، مما يجعله مثاليًا للتوثيق، مراجعة العملاء، والتخزين الأرشيفي.

## لماذا نستخدم Aspose.CAD Java لهذا التحويل؟

يجب عليك استخدام Aspose.CAD Java لأن المكتبة تتعامل مع تحويل الوحدات، الرستر، وتضمين PDF داخليًا، مما يلغي الحاجة إلى أدوات طرف ثالث أو خطوط أنابيب معقدة عبر سطر الأوامر. تم تصميم API للمطورين: كائن `Image` واحد يمثل الرسم، وعدد قليل من كائنات التكوين تسمح بضبط DPI، حجم الصفحة، والضغط. النتيجة هي مخرجات متسقة وقابلة للتكرار عبر بيئات Windows وLinux وmacOS.

## المتطلبات المسبقة

قبل الغوص في الكود، تأكد من وجود ما يلي:

- معرفة أساسية ببرمجة Java.  
- مكتبة Aspose.CAD للغة Java مثبتة. إذا لم تقم بتنزيلها بعد، احصل عليها **[download Aspose.CAD for Java](https://releases.aspose.com/cad/java/)**.  
- ملف DWG للاختبار – يتم استخدام العينة **Bottom_plate.dwg** في هذا الدليل.  

## استيراد مساحات الأسماء

في مشروع Java الخاص بك، استورد الفئات الضرورية لبدء عملية التحويل:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## دليل خطوة بخطوة

### الخطوة 1: تحميل ملف DWG

أولاً، حمّل رسم DWG الخاص بك باستخدام فئة `Image`. هذا ينشئ تمثيلًا في الذاكرة يمكن لـ Aspose.CAD العمل معه.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

### الخطوة 2: تحديد نوع الوحدة

فهم ما إذا كان الرسم يستخدم وحدات مترية أو إمبراطورية أمر أساسي للتدرج الصحيح. تُعيد الطريقة المساعدة `IsMetric` (التنفيذ محذوف للاختصار) قيمة منطقية.

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

### الخطوة 3: ضبط خيارات الرستر

فئة `CadRasterizationOptions` تحدد معلمات الرستر مثل DPI، حجم الصفحة، وتحويل الوحدات. بناءً على نظام الوحدات، قم بتكوين حجم الصفحة، التدرج، ونوع الوحدة المستهدف. هذه الخيارات تتحكم في كيفية رستر DWG قبل دمجه في PDF.

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

فئة `PdfOptions` تحدد إعدادات PDF الخاصة، بما في ذلك الضغط والبيانات الوصفية. أنشئ كائن `PdfOptions` وأرفق إعدادات الرستر. هذا يخبر Aspose.CAD كيف يدمج المحتوى الرستري في ملف PDF النهائي.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

### الخطوة 5: حفظ كملف PDF

طريقة `save` تكتب الصورة إلى المسار المحدد باستخدام الخيارات المقدمة. أخيرًا، صدّر الرسم إلى ملف PDF. تأخذ طريقة `save` مسار الإخراج وكائن `PdfOptions` المكوَّن.

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

عند انتهاء الكود، ستجد **Saved.pdf** في مجلد `DWGDrawings` الخاص بك، جاهزًا للتوزيع أو الأرشفة.

## كيف يمكن تحويل صور رستر DWG باستخدام مكتبة CAD للغة Java؟

يمكنك تحويل DWG إلى صيغ رسترية عن طريق استبدال `PdfOptions` بفئة خيارات رسترية مثل `PngOptions` أو `JpegOptions`. أعد استخدام نفس كائن `CadRasterizationOptions`، عدل صيغة الإخراج، واستدعِ طريقة `save` مع كائن الخيارات الجديد. يتيح لك هذا إنشاء ملفات PNG أو JPEG أو BMP أو TIFF بسطر واحد فقط، مع الحفاظ على سير العمل ثابتًا.

## كيف يمكن إنشاء PDF DWG باستخدام خيارات PDF CAD؟

المثال أعلاه بالفعل **generates pdf dwg**. لضبط حجم PDF بدقة، فعّل الضغط عبر استدعاء `pdfOptions.setCompress(true)`. يمكنك أيضًا تضمين بيانات وصفية مخصصة، ضبط إصدار PDF، أو إضافة حماية بكلمة مرور من خلال خصائص `PdfOptions` الإضافية. تمنحك هذه التعديلات تحكمًا كاملاً في ملف PDF النهائي دون مغادرة قاعدة كود Java.

## المشكلات الشائعة والنصائح

- **حجم الصفحة غير صحيح** – تحقق مرة أخرى من منطق تحويل الوحدات؛ قد تؤدي المعاملات غير المتطابقة إلى صفحات بحجم كبير.  
- **الخطوط أو أوزان الخطوط مفقودة** – تأكد من أن DWG يشير إلى أي موارد خارجية قبل التحويل.  
- **الأداء مع الرسومات الكبيرة** – قم بزيادة إعداد `DPI` في `CadRasterizationOptions` فقط عندما تكون الجودة العالية مطلوبة؛ DPI أقل يسرّع المعالجة.  
- **مشكلات الترخيص** – للتقييم يمكنك استخدام **ترخيص مؤقت Aspose**؛ يلزم ترخيص كامل للنشر في بيئة الإنتاج.

## الأسئلة المتكررة

**س: هل يمكنني استخدام Aspose.CAD للغة Java مع أطر عمل Java أخرى؟**  
نعم، Aspose.CAD للغة Java يتكامل بسلاسة مع أطر عمل Java الشهيرة مثل Spring و Jakarta EE و Android.

**س: هل يتوفر ترخيص مؤقت لـ Aspose.CAD للغة Java؟**  
نعم، يمكنك الحصول على ترخيص مؤقت **[obtain a temporary license](https://purchase.aspose.com/temporary-license/)**.

**س: أين يمكنني العثور على الدعم لـ Aspose.CAD للغة Java؟**  
زر **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)** للحصول على المساعدة من المجتمع ومهندسي Aspose.

**س: كيف يمكنني شراء ترخيص لـ Aspose.CAD للغة Java؟**  
يمكنك شراء ترخيص **[purchase a license](https://purchase.aspose.com/buy)**.

**س: ما الوحدات التي يدعمها Aspose.CAD للغة Java؟**  
يدعم Aspose.CAD للغة Java كلًا من الوحدات المترية والإمبراطورية، مع اكتشاف تلقائي لنظام وحدة الرسم.

**س: هل يمكنني تحويل DWG إلى صيغ صور أخرى (مثل PNG، JPEG) باستخدام نفس API؟**  
بالطبع. استبدل `PdfOptions` بخيارات صورة رسترية مناسبة (مثل `PngOptions`) وأعد استخدام نفس `CadRasterizationOptions`.

## الخاتمة

يوضح هذا الدرس كيفية **export dwg pdf** والصور النقطية باستخدام **java cad library** Aspose.CAD للغة Java. باتباع دليل الخطوة‑بخطوة، يمكنك دمج تحويل CAD الموثوق به في أي تطبيق Java، سواء كنت تحتاج إلى ملفات PDF للتوثيق أو صور رسترية للعرض على الويب. طبيعة المكتبة النقية للغة Java، وجودة المخرجات العالية، ونموذج الترخيص المرن يجعلها خيارًا قويًا لكل من الأدوات الصغيرة وخطوط الأنابيب المؤسسية الكبيرة.

---

**آخر تحديث:** 2026-10-14  
**تم الاختبار مع:** Aspose.CAD for Java 24.10  
**المؤلف:** Aspose

## دروس ذات صلة

- [تصدير DWG إلى PDF: تخطيط محدد باستخدام Aspose.CAD للغة Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [تصدير DWG إلى PDF في Java – ضبط حجم صفحة PDF باستخدام Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)
- [تصدير DWG إلى PDF مع الخطوط المخفية – Aspose.CAD للغة Java](/cad/java/cad-text-and-formatting/support-hidden-lines-in-dwg/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}