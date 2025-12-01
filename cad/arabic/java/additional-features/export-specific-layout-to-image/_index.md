---
date: 2025-12-01
description: تعلم كيفية تصدير ملفات DXF إلى صور باستخدام Aspose.CAD للـ Java. يوضح
  لك هذا الدليل خطوةً بخطوة كيفية تحويل DXF إلى صورة وأيضًا تحويل DWF إلى JPEG.
language: ar
linktitle: Export Specific DXF Layout to Image with Java
second_title: Aspose.CAD Java API
title: كيفية تصدير تخطيط DXF إلى صورة باستخدام Aspose.CAD في Java
url: /java/additional-features/export-specific-layout-to-image/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية تصدير تخطيط DXF إلى صورة باستخدام Aspose.CAD في Java

## المقدمة

إذا كنت بحاجة إلى **كيفية تصدير DXF** كرسومات نقطية في تطبيق Java، فإن Aspose.CAD for Java يجعل العملية مباشرة. في هذا البرنامج التعليمي ستشاهد بالضبط كيف **تحويل DXF إلى صورة** (وحتى **تحويل DWF إلى JPEG**) عن طريق اختيار تخطيط (طبقة) محدد من الملف المصدر. سنستعرض كل خطوة، من إعداد المشروع إلى حفظ ملف JPEG النهائي، حتى تتمكن من دمج الحل في قاعدة الشيفرة الخاصة بك بثقة.

## إجابات سريعة
- **ما المكتبة المطلوبة؟** Aspose.CAD for Java (يتوفر إصدار تجريبي مجاني).  
- **ما الصيغ التي يمكن تصديرها؟** DXF, DWF, DWG → JPEG, PNG, BMP, TIFF, إلخ.  
- **هل يمكن اختيار تخطيط/طبقة واحدة؟** نعم – استخدم `CadRasterizationOptions.setLayers()` لتحديد الطبقات المطلوبة.  
- **هل أحتاج إلى ترخيص للإنتاج؟** الترخيص التجاري مطلوب للاستخدام غير التجريبي.  
- **كم من الوقت تستغرق التنفيذ؟** حوالي 10‑15 دقيقة لتحويل أساسي.

## ما هو تصدير تخطيط DXF إلى صورة؟
تصدير تخطيط DXF يعني تحويل رسم متجه (DXF/DWF) إلى صيغة نقطية مثل JPEG. هذا مفيد عندما تحتاج إلى تضمين الرسومات في صفحات الويب، إنشاء صور مصغرة، أو مشاركتها مع مستخدمين لا يملكون برنامج CAD.

## لماذا تحويل DXF إلى صورة باستخدام Aspose.CAD؟
- **لا حاجة لبرنامج CAD خارجي** – التحويل يتم بالكامل داخل Java.  
- **تحكم دقيق** – يمكنك اختيار طبقات فردية، ضبط حجم الصفحة، DPI، ولون الخلفية.  
- **دعم صيغ واسع** – بالإضافة إلى JPEG يمكنك إخراج PNG, BMP, TIFF، وغيرها.  
- **دقة عالية** – المكتبة تحافظ على وزن الخطوط، الألوان، والخطوط أثناء التحويل إلى نقطية.

## المتطلبات المسبقة

قبل البدء، تأكد من وجود ما يلي:

- **Aspose.CAD for Java** – حمّل أحدث ملف JAR من [صفحة تحميل Aspose.CAD](https://releases.aspose.com/cad/java/).  
- بيئة تطوير Java (JDK 8 أو أعلى).  
- ملف **DXF/DWF** الذي تريد تحويله (المثال يستخدم `for_layers_test.dwf`).  

## استيراد المساحات الاسمية

أولاً، استورد الفئات التي ستحتاجها.  
```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.fileformats.dwf.whip.objects.DwfWhipLayer;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.dwf.DwfImage;
import com.aspose.cad.imageoptions.JpegOptions;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;
```

الآن لنفصِّل عملية التحويل خطوة بخطوة.

## الخطوة 1: تعيين دليل الموارد

حدد المجلد الذي يحتوي على ملف DXF/DWF المصدر.

```java
String dataDir = "Your Document Directory" + "DXFDrawings\\";
```

> **نصيحة احترافية:** استخدم مسارًا مطلقًا أو مسارًا نسبيًا إلى جذر مشروعك لتجنب `FileNotFoundException`.

## الخطوة 2: تحميل صورة DXF/DWF

حمّل الرسم باستخدام Aspose.CAD. المثال يستخدم ملف DWF، لكن نفس الشيفرة تعمل مع DXF.

```java
String srcFile = dataDir + "for_layers_test.dwf";
DwfImage image = (DwfImage) Image.load(srcFile);
```

> **لماذا DWF؟** المكتبة تتعامل مع DWF مماثلًا لـ DXF، لذا تنطبق نفس خيارات التحويل إلى نقطية، مما يتيح لك **تحويل DWF إلى JPEG** بسهولة.

## الخطوة 3: الحصول على أسماء الطبقات

استخرج جميع أسماء الطبقات حتى تتمكن من اختيار ما تريد تصديره.

```java
List<String> layersNames = image.getLayers().getLayersNames();
```

الآن لديك `List<String>` يحتوي على اسم كل تخطيط.

## الخطوة 4: تعيين خيارات التحويل إلى نقطية

قم بضبط حجم الصورة الناتجة، الدقة، وإعدادات التحويل الأخرى.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

عدّل `PageWidth` و `PageHeight` لتتناسب مع أبعاد الصورة المطلوبة. يمكنك أيضًا ضبط DPI عبر `setResolution`.

## الخطوة 5: تحديد الطبقات (اختيار التخطيط)

حوّل قائمة الطبقات إلى الصيغة المطلوبة بواسطة `setLayers()` واختر الطبقات التي تريد رسمها.

```java
String[] stringArray = Arrays.copyOf(layersNames.toArray(), layersNames.toArray().length, String[].class);
List<String> stringList = Arrays.asList(stringArray);
rasterizationOptions.setLayers(stringList);
```

إذا كنت تحتاج إلى تخطيط واحد فقط، استبدل `stringList` بقائمة تحتوي على اسم تلك الطبقة المحددة.

## الخطوة 6: تكوين خيارات JPEG

ضع إعدادات التحويل داخل كائن `JpegOptions`.

```java
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.setVectorRasterizationOptions(rasterizationOptions);
```

يمكنك أيضًا ضبط جودة JPEG (`jpegOptions.setQuality(90)`) إذا لزم الأمر.

## الخطوة 7: تصدير DXF/DWF إلى صورة

أخيرًا، احفظ الصورة المحوَّلة إلى القرص.

```java
String output = dataDir + "for_layers_test.jpg";
image.save(output, jpegOptions);
```

الملف `for_layers_test.jpg` الآن يحتوي على التخطيط المحدد مُرَسَّمًا كصورة JPEG عالية الجودة.

## القضايا الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|-------|-----|
| **صورة ناتجة فارغة** | اسم طبقة غير صحيح أو قائمة طبقات فارغة | تحقق من أن `layersNames` يحتوي على الأسماء المتوقعة ومرّر القائمة الصحيحة إلى `setLayers()`. |
| **خطأ نفاد الذاكرة** | أبعاد صفحة كبيرة جدًا | قلل `PageWidth/PageHeight` أو زد حجم heap للـ JVM (`-Xmx`). |
| **صيغة ملف غير مدعومة** | استخدام نسخة قديمة من Aspose.CAD | حدّث إلى أحدث ملف JAR من Aspose. |
| **جودة صورة منخفضة** | جودة JPEG الافتراضية منخفضة | استدعِ `jpegOptions.setQuality(95)` قبل الحفظ. |

## الأسئلة المتكررة

**س: هل يمكنني تصدير تخطيطات DXF متعددة في تشغيل واحد؟**  
ج: نعم. يمكنك تكرار حلقة عبر أسماء الطبقات المطلوبة، تحديث `rasterizationOptions.setLayers()` في كل تكرار، ثم استدعاء `image.save()` مع اسم ملف مخرج فريد.

**س: هل Aspose.CAD for Java متوافق مع جميع إصدارات Java؟**  
ج: المكتبة تدعم Java 8 وما فوق. راجع ملاحظات الإصدار لأي ملاحظات خاصة بالإصدار.

**س: كيف أتعامل مع الأخطاء أثناء التحويل؟**  
ج: غلف شيفرة التحويل داخل كتلة `try‑catch` والتقط `Exception` أو استثناءات Aspose المحددة لتسجيل أو عرض رسائل مفيدة.

**س: إلى أي صيغ صور أخرى يمكنني التصدير غير JPEG؟**  
ج: يمكنك استخدام `PngOptions`, `BmpOptions`, `TiffOptions`، إلخ، عن طريق استبدال `JpegOptions` بالفئة المناسبة.

**س: هل يمكنني تخصيص لون الخلفية أو سمك الخط؟**  
ج: نعم. توفر `CadRasterizationOptions` خصائص مثل `setBackgroundColor()` و `setLineWeight()` لضبط التفاصيل بدقة.

---

**آخر تحديث:** 2025-12-01  
**تم الاختبار مع:** Aspose.CAD for Java 24.11 (أحدث نسخة وقت كتابة هذا الدليل)  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}