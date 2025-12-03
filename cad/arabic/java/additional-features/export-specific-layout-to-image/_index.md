---
date: 2025-12-03
description: تعلم كيفية تصدير ملفات DXF إلى صور باستخدام Java. يوضح هذا الدليل خطوة
  بخطوة كيفية تصدير تخطيطات DXF إلى JPEG أو PNG باستخدام Aspose.CAD for Java.
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

## مقدمة

إذا كنت بحاجة إلى معرفة **كيفية تصدير dxf** إلى صور باستخدام Java، فإن Aspose.CAD توفر واجهة برمجة تطبيقات بسيطة تتولى عنك الجزء الأكبر من العمل. في هذا الدرس سنستعرض العملية بالكامل — من تحميل رسم DXF (أو DWF) إلى اختيار التخطيط المحدد الذي تريد تصديره وأخيرًا حفظه كصورة نقطية. سواءً كنت تبني أداة تقارير، عارض CAD، أو خط أنابيب تحويل تلقائي، فإن إتقان هذه الخطوات سيوفر لك الوقت والجهد.

## إجابات سريعة
- **ما المكتبة المطلوبة؟** Aspose.CAD for Java  
- **هل يمكنني التصدير إلى PNG بدلاً من JPEG؟** نعم — استبدل `JpegOptions` بـ `PngOptions`.  
- **هل أحتاج إلى ترخيص للاستخدام في الإنتاج؟** يلزم وجود ترخيص صالح لـ Aspose.CAD للاستخدام التجاري.  
- **ما إصدارات Java المدعومة؟** Java 8 وأحدثها مدعومة بالكامل.  
- **هل يمكن تصدير تخطيطات متعددة في آن واحد؟** بالتأكيد — قم بالتكرار عبر قائمة الطبقات واحفظ كل تخطيط على حدة.

## ما هو “كيفية تصدير dxf” عمليًا؟
يعني تصدير تخطيط DXF تحويل بيانات الرسم القائمة على المتجهات إلى صورة نقطية (مثل JPEG أو PNG) مع الحفاظ على الدقة البصرية للطبقات المختارة. هذا مفيد عندما تحتاج إلى تضمين رسومات CAD في صفحات الويب، إنشاء صور مصغرة، أو إنشاء معاينات قابلة للطباعة.

## لماذا نستخدم Aspose.CAD for Java؟
- **لا حاجة لبرمجيات CAD خارجية** – المكتبة تتعامل مع التحليل والرستر داخليًا.  
- **تحكم دقيق في الطبقات** – يمكنك اختيار الطبقات (أو التخطيطات) التي تريد رسمها بدقة.  
- **تنسيقات إخراج متعددة** – JPEG، PNG، BMP، TIFF، وأكثر.  
- **متعددة المنصات** – تعمل على أي نظام تشغيل يدعم Java.

## المتطلبات المسبقة

قبل أن تبدأ، تأكد من وجود:

- **Aspose.CAD for Java** – حمّل أحدث ملف JAR من [موقع Aspose](https://releases.aspose.com/cad/java/).  
- **مجموعة تطوير Java (JDK) 8+** مثبتة ومُعَدة في بيئة التطوير المتكاملة أو أداة البناء الخاصة بك.  
- ملف DXF (أو DWF) يحتوي على التخطيط الذي تريد تصديره.

## استيراد المساحات الاسمية

لبدء العمل، استورد الفئات الضرورية في مشروع Java الخاص بك:

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

الآن لنفصل كل خطوة بالتفصيل.

## كيفية تصدير تخطيط DXF إلى صورة – خطوة بخطوة

### الخطوة 1: تعيين دليل الموارد  
حدد المجلد الذي يحتوي على ملف DXF/DWF المصدر.

```java
String dataDir = "Your Document Directory" + "DXFDrawings\\";
```

> **نصيحة احترافية:** استبدل `"Your Document Directory"` بالمسار المطلق على جهازك أو استخدم مسارًا نسبيًا من جذر المشروع.

### الخطوة 2: تحميل صورة DXF (أو DWF)  
يمكن لـ Aspose.CAD قراءة صيغتي DXF و DWF. في هذا المثال نقوم بتحميل ملف DWF يحتوي على طبقات متعددة.

```java
String srcFile = dataDir + "for_layers_test.dwf";
DwfImage image = (DwfImage) Image.load(srcFile);
```

> إذا كنت تعمل بملف DXF بحت، ما عليك سوى تغيير الامتداد إلى `.dxf` وتحويله إلى `CadImage`.

### الخطوة 3: الحصول على أسماء الطبقات  
استرجع جميع أسماء الطبقات (التخطيطات) المتاحة لتتمكن من اختيار ما تريد تصديره.

```java
List<String> layersNames = image.getLayers().getLayersNames();
```

الآن لديك `List<String>` يحتوي على أسماء مثل `"Layer_0"`، `"Layer_1"`، إلخ.

### الخطوة 4: تعيين خيارات الرستر  
قم بتكوين حجم الصورة الناتجة وغيرها من معلمات الرستر.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

يمكنك تعديل `PageWidth` و `PageHeight` لتتناسب مع الدقة المطلوبة.

### الخطوة 5: تحديد الطبقات (أو التخطيط) للتصدير  
اختر التخطيط المحدد الذي تريد تصديره. هنا نقوم بتصدير **جميع** الطبقات، لكن يمكنك تصفية القائمة لتشمل تخطيطًا واحدًا فقط.

```java
String[] stringArray = Arrays.copyOf(layersNames.toArray(), layersNames.toArray().length, String[].class);
List<String> stringList = Arrays.asList(stringArray);
rasterizationOptions.setLayers(stringList);
```

> **لماذا هذا مهم:** بتقليل مجموعة `Layers` تقل حجم الملف وتسرع عملية الرسم.

### الخطوة 6: تكوين خيارات JPEG (أو PNG)  
أنشئ كائن خيارات للتنسيق المطلوب. المثال يستخدم JPEG، لكن يمكنك **java convert dxf png** ببساطة عن طريق استبدال `JpegOptions` بـ `PngOptions`.

```java
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### الخطوة 7: تصدير DXF إلى صورة  
أخيرًا، احفظ التخطيط المرسوم كصورة على القرص.

```java
String output = dataDir + "for_layers_test.jpg";
image.save(output, jpegOptions);
```

إذا كنت تفضّل PNG، غير امتداد الملف إلى `.png` واستخدم `PngOptions` في الخطوة السابقة.

> **النتيجة:** تم الآن تخزين تخطيط DXF المحدد كصورة عالية الجودة جاهزة للعرض أو المشاركة أو المعالجة الإضافية.

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|---------|--------|-----|
| **NullPointerException عند `image.getLayers()`** | الملف ليس DWF/DXF أو أنه تالف. | تحقق من مسار الملف المصدر وتأكد من أن الملف بصيغة CAD مدعومة. |
| **الصورة الناتجة فارغة** | لم يتم اختيار أي طبقة في `rasterizationOptions.setLayers()`. | تأكد من أن قائمة الطبقات تحتوي على أسماء التخطيطات المطلوبة. |
| **دقة الصورة منخفضة** | `PageWidth`/`PageHeight` صغيرة جدًا. | زد الأبعاد أو عيّن `rasterizationOptions.setResolution(300)` للحصول على DPI أعلى. |
| **LicenseException** | تشغيل بدون ترخيص Aspose.CAD صالح. | قم بتطبيق ملف الترخيص باستخدام `License license = new License(); license.setLicense("Aspose.CAD.lic");` قبل تحميل الصورة. |

## الأسئلة المتكررة

**س: هل يمكنني تصدير عدة تخطيطات DXF في عملية واحدة؟**  
ج: نعم. كرّر عبر قائمة `layersNames`، عيّن كل طبقة (أو مجموعة طبقات) في `CadRasterizationOptions`، واستدعِ `image.save()` لكل تكرار.

**س: هل Aspose.CAD for Java متوافق مع Java 11 وما بعدها؟**  
ج: بالتأكيد. المكتبة مبنية على .NET Standard وتعمل مع أي نسخة Java تدعم تبعيات JAR المطلوبة.

**س: كيف أتعامل مع الأخطاء أثناء التحويل؟**  
ج: ضع منطق التحميل والحفظ داخل كتلة `try‑catch` والتقط `Exception` أو استثناءات Aspose المحددة لتسجيلها أو إعادة رميها حسب الحاجة.

**س: هل هناك تنسيقات إخراج أخرى غير JPEG؟**  
ج: نعم. يدعم Aspose.CAD PNG، BMP، TIFF، GIF، وPDF. استبدل فئة الخيارات (`JpegOptions`، `PngOptions`، إلخ) وفقًا لذلك.

**س: هل يمكنني تخصيص لون الخلفية أو سمك الخط؟**  
ج: توفر فئة `CadRasterizationOptions` خصائص مثل `setBackgroundColor()` و `setLineWidth()` لضبط مخرجات الرستر بدقة.

## الخاتمة

أصبح لديك الآن وصفة كاملة وجاهزة للإنتاج حول **كيفية تصدير dxf** إلى صور نقطية باستخدام Aspose.CAD for Java. من خلال تعديل خيارات الرستر وتنسيق الإخراج، يمكنك تكييف التحويل لتلبية احتياجات الصور المصغرة، الطباعة عالية الدقة، أو PNG جاهز للويب. لا تتردد في تجربة تصفية الطبقات، إعدادات DPI، وتنسيقات الصور المختلفة لتلبية متطلبات مشروعك بدقة.

---

**آخر تحديث:** 2025-12-03  
**تم الاختبار مع:** Aspose.CAD for Java 24.12  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}