---
date: 2025-12-19
description: تعلم كيفية حفظ ملفات CAD بصيغة PNG باستخدام Aspose.CAD للغة Java، وتحويل
  ملفات DWG وDXF وغيرها من ملفات CAD إلى صور نقطية بكفاءة.
linktitle: Convert CAD Drawing to Raster Image Format
second_title: Aspose.CAD Java API
title: حفظ CAD كـ PNG – تحويل رسم CAD إلى تنسيق صورة نقطية باستخدام Aspose.CAD للـ
  Java
url: /ar/java/cad-drawing-conversion/convert-cad-drawing-to-raster-image/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# حفظ CAD كـ PNG – تحويل رسم CAD إلى تنسيق صورة نقطية باستخدام Aspose.CAD للـ Java

## المقدمة

في هذا الدرس، ستتعلم كيفية **حفظ CAD كـ PNG** باستخدام Aspose.CAD للـ Java. تحويل رسومات CAD إلى تنسيقات صور نقطية مثل PNG هو طلب شائع للمعاينات على الويب، والوثائق، والتقارير. يوفر Aspose.CAD طريقة موثوقة وعالية الأداء لإجراء **تحويل CAD إلى PNG** لملفات DWG وDXF وDWF والعديد من أنواع ملفات CAD الأخرى.

## إجابات سريعة
- **ما المكتبة التي تتعامل مع التحويل؟** Aspose.CAD للـ Java.  
- **هل يمكنني تحويل DWG إلى PNG؟** نعم – نفس الـ API يعمل مع DWG وDXF وغيرها من الصيغ.  
- **هل أحتاج إلى ترخيص للاستخدام الإنتاجي؟** يلزم ترخيص تجاري للاستخدام غير التجريبي.  
- **هل يمكن ضبط حجم الصورة النقطية؟** بالتأكيد – يمكنك تعيين عرض الصفحة، الارتفاع، وDPI عبر خيارات التحويل النقطي.  
- **كم يستغرق التحويل من الوقت؟** عادةً أقل من ثانية للرسومات القياسية؛ قد تستغرق الملفات الكبيرة وقتًا أطول.

## ما هو “حفظ CAD كـ PNG”؟
حفظ CAD كـ PNG يعني تحويل بيانات CAD القائمة على المتجهات إلى صورة قائمة على البكسل (PNG). تُعرف هذه العملية غالبًا بـ **convert cad to raster**، وتُحافظ على الدقة البصرية مع إنشاء تنسيق سهل الإدراج في صفحات الويب أو الرسائل الإلكترونية أو التقارير.

## لماذا نستخدم Aspose.CAD للـ Java؟
- **دعم واسع للملفات** – يعمل مع DWG وDXF وDWF وغيرها.  
- **بدون تبعيات خارجية** – جافا نقي، بدون ملفات DLL أصلية.  
- **تحكم دقيق** – تخصيص الدقة، لون الخلفية، وجودة العرض.  
- **أداء قابل للتوسع** – مناسب للمعالجة الدفعية أو التحويل الفوري.

## المتطلبات المسبقة

قبل الخوض في الدرس، تأكد من توفر المتطلبات المسبقة التالية:

1. بيئة تطوير Java: تأكد من وجود بيئة تطوير Java تعمل على جهازك.  
2. مكتبة Aspose.CAD: قم بتحميل وتكامل مكتبة Aspose.CAD للـ Java في مشروعك. يمكنك العثور على المكتبة [هنا](https://releases.aspose.com/cad/java/).

## استيراد المساحات الاسمية

في كود Java الخاص بك، استورد المساحات الاسمية اللازمة لاستخدام وظائف Aspose.CAD للـ Java بفعالية. هذه الخطوة حاسمة للوصول إلى الفئات والطرق المطلوبة.

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

الآن، دعنا نفصل عملية تحويل رسم CAD إلى صورة نقطية إلى خطوات مفصلة:

## الخطوة 1: تحميل رسم CAD

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

في هذه الخطوة، نقوم بتحميل رسم CAD من مسار الملف المحدد باستخدام طريقة `Image.load()`.

## الخطوة 2: ضبط خيارات التحويل النقطي

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
```

أنشئ كائنًا من `CadRasterizationOptions` واضبط عرض الصفحة وارتفاعها للصورة النقطية.

## الخطوة 3: إنشاء خيارات الصورة

```java
ImageOptionsBase options = new PngOptions();
options.setVectorRasterizationOptions(rasterizationOptions);
```

أنشئ كائنًا من `PngOptions` للصورة الناتجة واضبط خيارات التحويل النقطي للمتجهات.

## الخطوة 4: حفظ الصورة النقطية

```java
image.save(dataDir + "conic_pyramid_raster_image_out.png", options);
```

احفظ الصورة النقطية الناتجة إلى الدليل المحدد باستخدام طريقة `image.save()`.

كرر هذه الخطوات لملفات CAD الخاصة بك، وستكون قد نجحت في **تحويل صورة رسم CAD** إلى PNG.

## حالات الاستخدام الشائعة والنصائح
- **إنشاء معاينات ويب** – تحويل ملفات DWG الكبيرة إلى صور مصغرة PNG خفيفة للعرض السريع في المتصفح.  
- **إدراج في التقارير** – استخدم مخرجات PNG في تقارير PDF أو Word حيث لا تدعم ملفات CAD المتجهية.  
- **تحويل دفعي** – تكرار عبر مجلد من ملفات CAD وتطبيق نفس إعدادات التحويل النقطي للحصول على مخرجات متسقة.  
- **نصيحة احترافية:** اضبط `rasterizationOptions.setResolution()` لزيادة DPI للطباعة عالية الدقة.

## الخلاصة

ختامًا، تحويل رسومات CAD إلى صور نقطية باستخدام Aspose.CAD للـ Java هو عملية بسيطة. باتباع الخطوات الموضحة في هذا الدرس، يمكنك دمج هذه الوظيفة بفعالية في تطبيقات Java الخاصة بك وإجراء **convert dwg to png**، **export cad as png**، أو أي **cad to png conversion** أخرى تحتاجها.

## الأسئلة المتكررة

**س: كيف يمكنني تحويل ملف DWG إلى PNG مع لون خلفية مخصص؟**  
ج: اضبط خاصية `backgroundColor` في `CadRasterizationOptions` قبل إنشاء كائن `PngOptions`.

**س: هل من الممكن تحويل عدة ملفات CAD في عملية دفعة واحدة؟**  
ج: نعم—قم بلف خطوات التحميل، التحويل النقطي، والحفظ داخل حلقة تتكرر على مجموعة ملفاتك.

**س: ما هي جودة الصورة التي يمكن توقعها من الإعدادات الافتراضية؟**  
ج: الـ DPI الافتراضي (96) ينتج PNG بجودة شاشة؛ زد الـ DPI للحصول على نتائج بجودة طباعة.

**س: هل يدعم Aspose.CAD الخلفيات الشفافة في مخرجات PNG؟**  
ج: بالتأكيد. بشكل افتراضي، تُحفظ PNGs مع قناة ألفا؛ يمكنك أيضًا تحديد خلفية شفافة في خيارات التحويل النقطي.

**س: هل يمكنني تحويل ملفات CAD إلى تنسيقات نقطية أخرى مثل JPEG أو BMP؟**  
ج: نعم—استبدل `PngOptions` بـ `JpegOptions` أو `BmpOptions` مع الحفاظ على نفس إعدادات التحويل النقطي.

---

**آخر تحديث:** 2025-12-19  
**تم الاختبار مع:** Aspose.CAD للـ Java 24.12 (الأحدث)  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}