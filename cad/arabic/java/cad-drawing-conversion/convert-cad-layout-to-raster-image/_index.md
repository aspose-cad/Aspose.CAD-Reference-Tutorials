---
date: 2025-12-18
description: تعلم كيفية تحويل DWG إلى PNG وغيرها من صيغ الصور النقطية باستخدام Aspose.CAD
  للغة Java. صدّر ملفات CAD بصيغة PNG مع نتائج عالية الجودة.
linktitle: Convert CAD Layout to Raster Image Format
second_title: Aspose.CAD Java API
title: تحويل DWG إلى PNG وصيغ نقطية أخرى باستخدام Aspose.CAD للـ Java
url: /ar/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تحويل DWG إلى PNG وغيرها من صيغ الرسوم النقطية باستخدام Aspose.CAD للـ Java

## المقدمة

تحويل DWG إلى PNG (أو صيغ صور نقطية أخرى) هو طلب شائع عندما تحتاج إلى مشاركة رسومات CAD مع زملاء لا يمتلكون عارض CAD، أو تضمين التصاميم في الوثائق، أو إنشاء صور مصغرة لمعارض الويب. تجعل Aspose.CAD للـ Java هذا التحويل بسيطًا، سواء كنت تعمل على ملف رسم كامل أو مجرد تخطيط محدد. في هذا البرنامج التعليمي سنستعرض الخطوات الدقيقة **لتحويل تخطيط CAD إلى صورة نقطية**—وهي التقنية نفسها التي يمكنك استخدامها لإنتاج مخرجات PNG أو JPEG أو TIFF أو PDF.

## إجابات سريعة
- **ما المكتبة التي تتعامل مع تحويل DWG إلى PNG؟** Aspose.CAD للـ Java  
- **ما الصيغ التي يمكن تصديرها؟** PNG، JPEG، TIFF، PDF، BMP، وأكثر  
- **هل أحتاج إلى ترخيص للاختبار؟** النسخة التجريبية المجانية تعمل للتطوير؛ الترخيص مطلوب للإنتاج  
- **هل يمكنني اختيار تخطيط محدد؟** نعم، استخدم `setLayouts` لاستهداف “Model”، “Layout1”، إلخ.  
- **هل يمكن الحصول على مخرجات عالية الدقة؟** بالتأكيد—قم بضبط `setPageWidth` و `setPageHeight` للتحكم في DPI  

## ما هو “convert dwg to png”؟

عبارة “convert dwg to png” تصف عملية أخذ ملف DWG قائم على المتجهات (الصيغة الأصلية للعديد من تطبيقات CAD) وتحويله إلى صورة PNG قائمة على البكسل. الصور النقطية مثالية للعرض على الويب، مشاركة البريد الإلكتروني، والدمج في برامج غير CAD.

## لماذا تصدير CAD كـ PNG (أو صيغ رسومية أخرى)؟

- **توافق عالمي:** PNG و JPEG مدعومان من قبل كل عارض صور ومتصفح تقريبًا.  
- **تحميل سريع:** الصور النقطية تُحمَّل فورًا مقارنة بفتح ملف DWG ثقيل.  
- **تضمين سهل:** أدرج PNG مباشرةً في Word أو PowerPoint أو HTML دون إضافات إضافية.  
- **مظهر ثابت:** تتحكم في الدقة، الخلفية، والتخطيط، مما يضمن أن كل طرف يرى نفس الصورة.

## المتطلبات المسبقة

قبل أن تبدأ، تأكد من وجود ما يلي:

1. **بيئة تطوير Java** – JDK 8 أو أحدث مثبتة ومُعَدَّة.  
2. **Aspose.CAD للـ Java** – حمّل أحدث ملف JAR من [توثيق Aspose.CAD للـ Java](https://reference.aspose.com/cad/java/).  

## استيراد المساحات الاسمية

أولًا، استورد الفئات التي ستحتاجها. هذه الاستيرادات تمنحك الوصول إلى تحميل الصور، خيارات التحويل إلى رسومي، وإعدادات إخراج TIFF/PNG.

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

> **نصيحة احترافية:** إذا كنت تخطط للتصدير إلى PNG بدلاً من TIFF، استبدل `TiffOptions` بـ `PngOptions` (الموجودة في `com.aspose.cad.imageoptions.PngOptions`).

## دليل خطوة بخطوة

### الخطوة 1: إعداد دليل الموارد

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";
```

استبدل `"Your Document Directory"` بالمسار المطلق حيث توجد ملفات CAD الخاصة بك.

### الخطوة 2: تحميل ملف CAD

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

يمكنك تحميل أي صيغة مدعومة (DWG، DXF، DGN، إلخ). هذه هي **كيفية تحويل cad**—فقط أشِر إلى الملف ودع Aspose يتولى التحليل.

### الخطوة 3: تكوين خيارات التحويل إلى رسومي

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
rasterizationOptions.setLayouts(new String[] {"Model", "Layout1"});
```

- `setPageWidth` / `setPageHeight` يتحكمان في دقة الإخراج (القيم الأكبر = DPI أعلى).  
- `setLayouts` يتيح لك **تحويل cad إلى رسومي** لتخطيطات محددة؛ احذفها إذا أردت تحويل الرسم بالكامل.

### الخطوة 4: تعيين خيارات الصورة

```java
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.setVectorRasterizationOptions(rasterizationOptions);
```

إذا كنت تفضّل PNG، أنشئ كائن `PngOptions` بدلاً من `TiffOptions`. هنا حيث تقوم **بتصدير cad كـ png**.

### الخطوة 5: حفظ الصورة الناتجة

```java
image.save(dataDir + "conic_pyramid_layoutstorasterimage_out_.tiff", options);
```

غيّر امتداد الملف إلى `.png` (واستبدل كائن الخيارات بـ `PngOptions`) لتقوم **بحفظ CAD كـ JPEG/PNG**.

> **مشكلة شائعة:** نسيان مطابقة امتداد الملف مع فئة الخيارات سيتسبب في حدوث `UnsupportedFormatException`. احرص دائمًا على توافقهما.

## المشكلات الشائعة والحلول

| المشكلة | الحل |
|-------|----------|
| **صورة ناتجة فارغة** | تأكد من أن أسماء التخطيطات في `setLayouts` تتطابق تمامًا مع تلك الموجودة في ملف CAD المصدر. |
| **PNG منخفض الدقة** | زد من قيم `setPageWidth` / `setPageHeight` أو اضبط `setResolution` في خيارات التحويل إلى رسومي. |
| **إصدار DWG غير مدعوم** | تأكد من أنك تستخدم أحدث نسخة من Aspose.CAD؛ الإصدارات القديمة قد لا تدعم إصدارات DWG الحديثة. |
| **أخطاء الذاكرة في الملفات الكبيرة** | عالج الصفحات واحدةً تلو الأخرى أو زد حجم heap الخاص بـ JVM (`-Xmx2g`). |

## الأسئلة المتكررة

**س: هل Aspose.CAD متوافق مع صيغ CAD المختلفة؟**  
ج: نعم، يدعم DWG، DXF، DGN، والعديد من الصيغ الأخرى.

**س: هل يمكنني تخصيص دقة الصورة النقطية الناتجة؟**  
ج: بالتأكيد. اضبط `setPageWidth`، `setPageHeight`، أو `setResolution` في `CadRasterizationOptions`.

**س: كيف يمكنني تحويل عدة تخطيطات CAD في تشغيل واحد؟**  
ج: قدم مصفوفة تحتوي على جميع أسماء التخطيطات إلى `setLayouts`، مثل `new String[]{"Model","Layout1","Layout2"}`.

**س: هل هناك صيغ إخراج غير TIFF مدعومة؟**  
ج: نعم—PNG، JPEG، BMP، PDF، وأكثر متاحة عبر فئات `*Options` الخاصة بها.

**س: أين يمكنني الحصول على مساعدة أو مشاركة تجربتي مع Aspose.CAD؟**  
ج: زر [منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19) للدعم المجتمعي والمساعدة الرسمية.

## الخلاصة

باتباع هذه الخطوات يمكنك **تحويل DWG إلى PNG**، **تصدير CAD كـ PNG**، **حفظ CAD كـ JPEG**، أو إنشاء أي صيغة رسومية أخرى تحتاجها. تتولى Aspose.CAD للـ Java الجزء الصعب، مما يتيح لك التركيز على دمج صور عالية الجودة في تطبيقاتك، وثائقك، أو بوابات الويب.

---

**آخر تحديث:** 2025-12-18  
**تم الاختبار مع:** Aspose.CAD للـ Java 24.12  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}