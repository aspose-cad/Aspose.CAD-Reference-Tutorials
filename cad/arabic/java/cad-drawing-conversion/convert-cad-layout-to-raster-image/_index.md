---
date: 2026-10-04
description: تعلم كيفية تحويل DWG إلى PNG بسرعة وتصدير CAD كـ PNG أو تنسيقات raster
  أخرى باستخدام Aspose.CAD for Java. احصل على نتائج عالية الجودة بسرعة.
keywords:
- convert dwg to png
- dwg to raster image
- convert cad to pdf
- export cad as png
- convert dwg to jpeg
lastmod: 2026-10-04
linktitle: تحويل تخطيط CAD إلى تنسيق صورة raster
og_description: حوّل DWG إلى PNG بسرعة باستخدام Aspose.CAD for Java. تعلم خطوة بخطوة
  كيفية تصدير CAD كـ PNG، JPEG، TIFF، وأكثر.
og_image_alt: 'Developer guide: Convert DWG to PNG and other raster formats using
  Aspose.CAD for Java'
og_title: تحويل DWG إلى PNG وغيرها من تنسيقات raster باستخدام Aspose.CAD for Java
schemas:
- author: Aspose
  dateModified: '2026-10-04'
  description: Learn how to quickly convert dwg to png and export cad as png or other
    raster formats using Aspose.CAD for Java. Get high‑quality results fast.
  headline: Convert DWG to PNG and other raster formats using Aspose.CAD for Java
  type: TechArticle
- description: Learn how to quickly convert dwg to png and export cad as png or other
    raster formats using Aspose.CAD for Java. Get high‑quality results fast.
  name: Convert DWG to PNG and other raster formats using Aspose.CAD for Java
  steps:
  - name: set up the resource directory
    text: Replace `"Your Document Directory"` with the absolute path where your CAD
      files reside. This directory will be used for both input and output files.
  - name: load the CAD file
    text: '`Image.load` parses the source file and creates an in‑memory representation
      that you can rasterize. You can load any supported format (DWG, DXF, DGN, etc.)
      – this is the **how to convert cad** part.'
  - name: configure rasterization options
    text: '`CadRasterizationOptions` defines how the vector data is turned into pixels.
      `setPageWidth` and `setPageHeight` control output resolution (larger values
      = higher DPI). `setLayouts` lets you **convert CAD to raster** for specific
      layouts; omit it to rasterize the whole drawing.'
  - name: set image options
    text: '`TiffOptions` (or `PngOptions` for PNG) tells Aspose which raster format
      to generate and lets you fine‑tune compression, color depth, and other format‑specific
      settings. Choose the options class that matches your desired output.'
  - name: save the resultant image
    text: Call `save` on the `Image` instance, passing the output file name and the
      options object. Change the file extension to `.png` (and use `PngOptions`) to
      **save CAD as PNG**. The same pattern works for JPEG, BMP, or PDF. > **Common
      pitfall:** Forgetting to match the file extension with the options cla
  type: HowTo
- questions:
  - answer: Yes, it supports over 30 CAD and raster formats, including DWG, DXF, DGN,
      and SVG.
    question: Is Aspose.CAD compatible with different CAD file formats?
  - answer: Absolutely. Adjust `setPageWidth`, `setPageHeight`, or `setResolution`
      in `CadRasterizationOptions` to achieve the desired DPI.
    question: Can I customize the resolution of the output raster image?
  - answer: Provide an array with all layout names to `setLayouts`, e.g., `new String[]{"Model","Layout1","Layout2"}`.
    question: How can I convert multiple CAD layouts in a single run?
  - answer: Yes—PNG, JPEG, BMP, PDF, and more are available via their respective `*Options`
      classes.
    question: Are there output formats besides TIFF supported?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community
      support and official assistance.
    question: Where can I get help or share my experience with Aspose.CAD?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- convert dwg
- Aspose.CAD
- Java raster conversion
- CAD image processing
title: تحويل DWG إلى PNG وغيرها من تنسيقات raster باستخدام Aspose.CAD for Java
url: /ar/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تحويل DWG إلى PNG وغيرها من صيغ الرسوم النقطية باستخدام Aspose.CAD للـ Java

## مقدمة

`Aspose.CAD for Java` هي مكتبة تتيح التحويل البرمجي لملفات CAD إلى صور نقطية مثل PNG و JPEG و TIFF. تحويل DWG إلى PNG (أو صيغ صور نقطية أخرى) هو طلب شائع عندما تحتاج إلى مشاركة رسومات CAD مع زملاء لا يمتلكون عارض CAD، أو تضمين التصاميم في الوثائق، أو إنشاء صور مصغرة للمعارض على الويب. في هذا الدليل ستتعلم كيفية تحويل dwg إلى png بسرعة وبشكل موثوق، سواء كنت تعمل على ملف رسم كامل أو مجرد تخطيط محدد. قد تحتاج أيضًا إلى **convert CAD to raster** للمعاينات على الويب، أدوات التقارير، أو التطبيقات المحمولة.

## إجابات سريعة
- **ما المكتبة التي تتعامل مع DWG إلى PNG؟** Aspose.CAD for Java توفر محرك التحويل.  
- **ما صيغ الرسوم النقطية التي يمكنني تصديرها؟** PNG، JPEG، TIFF، PDF، BMP، وأكثر من 30 صيغة إضافية.  
- **هل أحتاج إلى ترخيص للاختبار؟** النسخة التجريبية المجانية تعمل للتطوير؛ الترخيص التجاري مطلوب للإنتاج.  
- **هل يمكنني اختيار تخطيط محدد؟** نعم – استخدم `setLayouts` لاستهداف “Model”، “Layout1”، إلخ.  
- **هل يمكن الحصول على مخرجات عالية الدقة؟** بالتأكيد – عدل `setPageWidth` و `setPageHeight` (أو `setResolution`) للتحكم في DPI.

## ما هو “convert dwg to png”؟

تحويل dwg إلى png يعني تحويل رسم DWG المتجه إلى صورة PNG قائمة على البكسل يمكن عرضها بواسطة أي عارض صور قياسي. هذه العملية تقوم بتحويل الكيانات المتجهة إلى نقطية، مع الحفاظ على وزن الخطوط، الألوان، والطبقات مع تحويلها إلى صورة bitmap ذات دقة ثابتة. النتيجة مثالية للتضمين في ملفات PDF، مستندات Word، أو صفحات الويب حيث يكون دعم المتجهات محدودًا.

## لماذا تصدير CAD كـ PNG (أو صيغ رسومية أخرى)؟

تصدير CAD كـ PNG يمنحك توافقًا عالميًا، تحميلًا سريعًا، وتضمينًا سهلاً عبر جميع المنصات الرئيسية. الصور النقطية تُحمّل فورًا مقارنة بفتح ملف DWG ثقيل، وضغط PNG بدون فقد يضمن الحفاظ على الجودة البصرية. من خلال التحكم في الدقة، لون الخلفية، والتخطيط، تضمن أن كل صاحب مصلحة يرى نفس المظهر، سواء تم عرض الملف على سطح مكتب، جهاز محمول، أو داخل متصفح.

## حالات الاستخدام الشائعة
| السيناريو | لماذا يساعد الإخراج النقطي |
|----------|----------------------------|
| **توثيق المشروع** | إدراج PNGs في ملفات PDF أو Word يجنب الحاجة إلى برنامج CAD للمراجعين. |
| **بوابات الويب** | الصور المصغرة المولدة من ملفات DWG تُحمّل فورًا وتحسّن تجربة المستخدم. |
| **تطبيقات الهواتف المحمولة** | الصور النقطية تُعرض بشكل صحيح على الأجهزة التي لا تحتوي على عارض CAD. |
| **التقارير الآلية** | تحويل دفعات متعددة من التخطيطات إلى PNG/JPEG لتضمينها في المخططات أو لوحات التحكم. |

## المتطلبات المسبقة

قبل البدء، تأكد من وجود:

1. **بيئة تطوير Java** – JDK 8 أو أحدث مثبتة ومُكوّنة.  
2. **Aspose.CAD for Java** – حمّل أحدث JAR من [Aspose.CAD for Java documentation](https://reference.aspose.com/cad/java/).  

## استيراد مساحات الأسماء

`com.aspose.cad.Image` هي الفئة الأساسية التي تمثل أي ملف CAD في الذاكرة. `com.aspose.cad.imageoptions.*` توفر كائنات الخيارات لكل صيغة نقطية. استورد الفئات التي تحتاجها لتحميل الرسم، تكوين التحويل إلى نقطية، وحفظ النتيجة.

> **نصيحة محترف:** إذا كنت تخطط إلى **export CAD as PNG** بدلاً من TIFF، استبدل `TiffOptions` بـ `PngOptions` (الموجودة في `com.aspose.cad.imageoptions.PngOptions`).

## دليل خطوة بخطوة

### الخطوة 1: إعداد دليل الموارد

استبدل `"Your Document Directory"` بالمسار المطلق حيث توجد ملفات CAD الخاصة بك. سيُستخدم هذا الدليل لكل من ملفات الإدخال والإخراج.

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

### الخطوة 2: تحميل ملف CAD

`Image.load` يقوم بتحليل الملف المصدر وإنشاء تمثيل في الذاكرة يمكنك تحويله إلى نقطية. يمكنك تحميل أي صيغة مدعومة (DWG، DXF، DGN، إلخ) – هذا هو الجزء المتعلق بـ **how to convert cad**.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";
```

### الخطوة 3: تكوين خيارات التحويل إلى نقطية

`CadRasterizationOptions` تحدد كيفية تحويل البيانات المتجهة إلى بكسلات. `setPageWidth` و `setPageHeight` يتحكمان في دقة الإخراج (قيم أكبر = DPI أعلى). `setLayouts` يتيح لك **convert CAD to raster** لتخطيطات محددة؛ احذفها لتحويل الرسم بالكامل.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### الخطوة 4: ضبط خيارات الصورة

`TiffOptions` (أو `PngOptions` لـ PNG) تخبر Aspose أي صيغة نقطية يجب توليدها وتتيح لك ضبط الضغط، عمق اللون، وإعدادات الصيغة الخاصة الأخرى. اختر فئة الخيارات التي تتطابق مع الإخراج المطلوب.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
rasterizationOptions.setLayouts(new String[] {"Model", "Layout1"});
```

### الخطوة 5: حفظ الصورة الناتجة

استدعِ `save` على كائن `Image`، مع تمرير اسم ملف الإخراج وكائن الخيارات. غيّر امتداد الملف إلى `.png` (واستخدم `PngOptions`) لـ **save CAD as PNG**. نفس النمط يعمل مع JPEG، BMP، أو PDF.

```java
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.setVectorRasterizationOptions(rasterizationOptions);
```

> **مشكلة شائعة:** نسيان مطابقة امتداد الملف مع فئة الخيارات سيتسبب في حدوث `UnsupportedFormatException`. احرص دائمًا على توافقهما.

## المشكلات الشائعة والحلول
| المشكلة | الحل |
|---------|------|
| **صورة ناتجة فارغة** | تحقق من أن أسماء التخطيطات في `setLayouts` تطابق تمامًا تلك الموجودة في ملف CAD الأصلي. |
| **PNG منخفض الدقة** | زد `setPageWidth` / `setPageHeight` أو اضبط `setResolution` في خيارات التحويل إلى نقطية. |
| **إصدار DWG غير مدعوم** | تأكد من أنك تستخدم أحدث نسخة من Aspose.CAD؛ الإصدارات القديمة قد لا تدعم إصدارات DWG الحديثة. |
| **أخطاء الذاكرة في الملفات الكبيرة** | عالج الصفحات واحدةً تلو الأخرى أو زد حجم ذاكرة JVM (`-Xmx2g`). |

## الأسئلة المتكررة

**س: هل Aspose.CAD متوافق مع صيغ ملفات CAD المختلفة؟**  
ج: نعم، يدعم أكثر من 30 صيغة CAD وصيغ نقطية، بما في ذلك DWG، DXF، DGN، و SVG.

**س: هل يمكنني تخصيص دقة الصورة النقطية الناتجة؟**  
ج: بالتأكيد. عدل `setPageWidth`، `setPageHeight`، أو `setResolution` في `CadRasterizationOptions` لتحقيق DPI المطلوب.

**س: كيف يمكنني تحويل عدة تخطيطات CAD في تشغيل واحد؟**  
ج: قدم مصفوفة تحتوي على جميع أسماء التخطيطات إلى `setLayouts`، مثال: `new String[]{"Model","Layout1","Layout2"}`.

**س: هل هناك صيغ إخراج غير TIFF مدعومة؟**  
ج: نعم—PNG، JPEG، BMP، PDF، وأكثر متاحة عبر فئات `*Options` الخاصة بها.

**س: أين يمكنني الحصول على مساعدة أو مشاركة تجربتي مع Aspose.CAD؟**  
ج: زر [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) للحصول على دعم المجتمع والمساعدة الرسمية.

## الخلاصة

باتباع هذه الخطوات يمكنك **convert DWG to PNG**، **export CAD as PNG**، **save CAD as JPEG**، أو توليد أي صيغة نقطية أخرى تحتاجها. Aspose.CAD for Java يتولى الجزء الثقيل، مما يتيح لك التركيز على دمج صور عالية الجودة في تطبيقاتك، وثائقك، أو بوابات الويب. دعم المكتبة لأكثر من 30 صيغة وقدرتها على معالجة رسومات مئات الصفحات دون تحميل الملف بالكامل إلى الذاكرة يجعلها خيارًا قويًا لتقنيات CAD على مستوى المؤسسات.

---

**Last Updated:** 2026-10-04  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  







```java
image.save(dataDir + "conic_pyramid_layoutstorasterimage_out_.tiff", options);
```

```bash
java -jar aspose-cad.jar -i input.dwg -o output.png -w 1200 -h 1200
```

## الدروس ذات الصلة

- [تصدير DWG بسرعة إلى PDF أو رسومي باستخدام مكتبة java cad Aspose.CAD للـ Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [تحويل DWG إلى BMP باستخدام Aspose.CAD للـ Java](/cad/java/cad-export-options/export-to-bmp/)
- [تصدير DWG إلى PDF: تخطيط محدد باستخدام Aspose.CAD للـ Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}