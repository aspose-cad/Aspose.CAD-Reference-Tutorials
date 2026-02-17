---
date: 2026-02-17
description: تعلم كيفية تحويل DWG إلى PNG وتصدير CAD كـ PNG أو صيغ نقطية أخرى باستخدام
  Aspose.CAD للغة Java. احصل على نتائج عالية الجودة بسرعة.
linktitle: Convert CAD Layout to Raster Image Format
second_title: Aspose.CAD Java API
title: تحويل DWG إلى PNG وصيغ نقطية أخرى باستخدام Aspose.CAD للغة Java
url: /ar/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/
weight: 12
---

.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تحويل DWG إلى PNG وصيغ الراستر الأخرى باستخدام Aspose.CAD للـ Java

## المقدمة

تحويل DWG إلى PNG (أو صيغ صور الراستر الأخرى) هو طلب شائع عندما تحتاج إلى مشاركة رسومات CAD مع زملائك الذين لا يمتلكون عارض CAD، أو تضمين التصاميم في الوثائق، أو إنشاء صور مصغرة لمعارض الويب. **في هذا الدليل ستتعلم كيفية تحويل dwg إلى png بسرعة وبشكل موثوق**، سواء كنت تعمل على ملف رسم كامل أو مجرد تخطيط محدد. قد تحتاج أيضًا إلى **convert CAD to raster** لعرض المعاينات على الويب، أو أدوات التقارير، أو التطبيقات المحمولة. تجعل Aspose.CAD للـ Java هذا التحويل بسيطًا وتمنحك التحكم الكامل في الدقة، واختيار التخطيط، وصيغة الإخراج.

## إجابات سريعة
- **ما المكتبة التي تتعامل مع DWG إلى PNG؟** Aspose.CAD للـ Java  
- **ما الصيغ التي يمكن تصديرها؟** PNG، JPEG، TIFF، PDF، BMP، وأكثر  
- **هل أحتاج إلى ترخيص للاختبار؟** نسخة تجريبية مجانية تعمل للتطوير؛ الترخيص مطلوب للإنتاج  
- **هل يمكنني اختيار تخطيط محدد؟** نعم، استخدم `setLayouts` لاستهداف “Model”، “Layout1”، إلخ.  
- **هل الإخراج بدقة عالية ممكن؟** بالتأكيد—عدّل `setPageWidth` و `setPageHeight` للتحكم في DPI  

## ما هو “convert dwg to png”؟

عبارة “convert dwg to png” تصف عملية أخذ ملف DWG قائم على المتجهات (الصيغة الأصلية للعديد من تطبيقات CAD) وتحويله إلى صورة PNG قائمة على البكسل. صور الراستر مثالية للعرض على الويب، ومشاركة البريد الإلكتروني، والدمج في برامج غير CAD.

## لماذا تصدير CAD كـ PNG (أو صيغ الراستر الأخرى)؟

- **توافق عالمي:** PNG و JPEG مدعومان من قبل كل عارض صور ومتصفح تقريبًا.  
- **تحميل سريع:** صور الراستر تُحمَّل فورًا مقارنة بفتح ملف DWG ثقيل.  
- **تضمين سهل:** أدخل PNG مباشرةً في Word أو PowerPoint أو HTML دون إضافات إضافية.  
- **مظهر ثابت:** تتحكم في الدقة، الخلفية، والتخطيط، مما يضمن أن كل صاحب مصلحة يرى نفس الصورة.  

## حالات الاستخدام الشائعة

| السيناريو | لماذا يساعد إخراج الراستر |
|----------|---------------------------|
| **توثيق المشروع** | تضمين PNG في ملفات PDF أو Word يجنب الحاجة إلى برنامج CAD للمراجعين. |
| **بوابات الويب** | الصور المصغرة المولدة من ملفات DWG تُحمَّل فورًا وتحسّن تجربة المستخدم. |
| **التطبيقات المحمولة** | صور الراستر تُعرض بشكل صحيح على الأجهزة التي لا تمتلك عارض CAD. |
| **التقارير الآلية** | تحويل دفعة من التخطيطات إلى PNG/JPEG لتضمينها في المخططات أو لوحات التحكم. |

## المتطلبات المسبقة

قبل أن تبدأ، تأكد من وجود:

1. **بيئة تطوير جافا** – JDK 8 أو أحدث مثبتة ومُكوَّنة.  
2. **Aspose.CAD للـ Java** – حمّل أحدث JAR من [توثيق Aspose.CAD للـ Java](https://reference.aspose.com/cad/java/).  

## استيراد المساحات الاسمية

أولاً، استورد الفئات التي ستحتاجها. هذه الاستيرادات تمنحك الوصول إلى تحميل الصور، خيارات الرستر، وإعدادات إخراج TIFF/PNG.

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

> **نصيحة احترافية:** إذا كنت تخطط لـ **export CAD as PNG** بدلاً من TIFF، استبدل `TiffOptions` بـ `PngOptions` (الموجودة في `com.aspose.cad.imageoptions.PngOptions`).

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

يمكنك تحميل أي صيغة مدعومة (DWG، DXF، DGN، إلخ). هذه هي **how to convert cad**—فقط أشِر إلى الملف ودع Aspose يتولى التحليل.

### الخطوة 3: تكوين خيارات الرستر

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
rasterizationOptions.setLayouts(new String[] {"Model", "Layout1"});
```

- `setPageWidth` / `setPageHeight` يتحكمان في دقة الإخراج (القيم الأكبر = DPI أعلى).  
- `setLayouts` يتيح لك **convert CAD to raster** لتخطيطات محددة؛ احذفها إذا أردت رستر كامل الرسم.

### الخطوة 4: تعيين خيارات الصورة

```java
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.setVectorRasterizationOptions(rasterizationOptions);
```

إذا كنت تفضّل PNG، أنشئ كائن `PngOptions` بدلاً من `TiffOptions`. هنا حيث تقوم **export CAD as PNG**.

### الخطوة 5: حفظ الصورة الناتجة

```java
image.save(dataDir + "conic_pyramid_layoutstorasterimage_out_.tiff", options);
```

غيّر امتداد الملف إلى `.png` (واستخدم كائن الخيارات `PngOptions`) لـ **save CAD as JPEG/PNG**.

> **مشكلة شائعة:** نسيان مطابقة امتداد الملف مع فئة الخيارات سيتسبب في حدوث `UnsupportedFormatException`. احرص دائمًا على توافقهما.

## المشكلات الشائعة والحلول

| المشكلة | الحل |
|---------|------|
| **صورة إخراج فارغة** | تأكد من أن أسماء التخطيطات في `setLayouts` تطابق تمامًا تلك الموجودة في ملف CAD الأصلي. |
| **PNG منخفض الدقة** | زد من `setPageWidth` / `setPageHeight` أو اضبط `setResolution` في خيارات الرستر. |
| **إصدار DWG غير مدعوم** | تأكد من أنك تستخدم أحدث نسخة من Aspose.CAD؛ الإصدارات القديمة قد لا تدعم إصدارات DWG الحديثة. |
| **أخطاء الذاكرة في الملفات الكبيرة** | عالج الصفحات واحدةً تلو الأخرى أو زد حجم ذاكرة JVM (`-Xmx2g`). |

## الأسئلة المتكررة

**س: هل Aspose.CAD متوافق مع صيغ CAD المختلفة؟**  
ج: نعم، يدعم DWG، DXF، DGN، والعديد غيرها.

**س: هل يمكنني تخصيص دقة صورة الراستر الناتجة؟**  
ج: بالتأكيد. عدّل `setPageWidth`، `setPageHeight`، أو `setResolution` في `CadRasterizationOptions`.

**س: كيف يمكنني تحويل عدة تخطيطات CAD في تشغيل واحد؟**  
ج: قدم مصفوفة تحتوي على جميع أسماء التخطيطات إلى `setLayouts`، مثال: `new String[]{"Model","Layout1","Layout2"}`.

**س: هل هناك صيغ إخراج غير TIFF مدعومة؟**  
ج: نعم—PNG، JPEG، BMP، PDF، وأكثر متاحة عبر فئات `*Options` الخاصة بها.

**س: أين يمكنني الحصول على مساعدة أو مشاركة تجربتي مع Aspose.CAD؟**  
ج: زر [منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19) للحصول على دعم المجتمع والمساعدة الرسمية.

## الخلاصة

باتباع هذه الخطوات يمكنك **convert DWG to PNG**، **export CAD as PNG**، **save CAD as JPEG**، أو توليد أي صيغة راستر أخرى تحتاجها. تتولى Aspose.CAD للـ Java الجزء الصعب، مما يتيح لك التركيز على دمج الصور عالية الجودة في تطبيقاتك، وثائقك، أو بوابات الويب.

---

**آخر تحديث:** 2026-02-17  
**تم الاختبار مع:** Aspose.CAD للـ Java 24.12  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}