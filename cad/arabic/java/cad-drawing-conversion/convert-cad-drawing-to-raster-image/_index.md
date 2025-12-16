---
date: 2025-12-16
description: تعلم كيفية تحويل CAD إلى PNG باستخدام Aspose.CAD للـ Java، مع تغطية تصدير
  DWG إلى صورة، حفظ CAD كـ PNG، وخيارات تحويل CAD إلى صورة نقطية.
linktitle: Convert CAD Drawing to Raster Image Format
second_title: Aspose.CAD Java API
title: كيفية تحويل CAD إلى PNG باستخدام Aspose.CAD للـ Java
url: /ar/java/cad-drawing-conversion/convert-cad-drawing-to-raster-image/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية تحويل CAD إلى PNG باستخدام Aspose.CAD للـ Java

في سير عمل الهندسة الحديثة، غالبًا ما تحتاج إلى **تحويل CAD إلى PNG** بحيث يمكن عرض الرسومات في المتصفحات، أو تضمينها في المستندات، أو مشاركتها مع أصحاب المصلحة الذين لا يمتلكون برنامج CAD. يشرح هذا البرنامج التعليمي العملية بالكامل — من تحميل ملف CAD إلى تصدير صورة PNG نقطية عالية الجودة — باستخدام مكتبة Aspose.CAD القوية للـ Java.

## إجابات سريعة
- **ما هو الهدف الأساسي؟** تحويل رسومات CAD إلى صور نقطية PNG.  
- **أي مكتبة تُستخدم؟** Aspose.CAD للـ Java.  
- **هل أحتاج إلى ترخيص؟** يتوفر إصدار تجريبي مجاني؛ يلزم وجود ترخيص للاستخدام في الإنتاج.  
- **هل يمكن تخصيص حجم الصورة؟** نعم، استخدم `CadRasterizationOptions` لتحديد العرض والارتفاع.  
- **ما هي صيغ CAD المدعومة؟** DWG، DXF، DWF، والعديد غيرها.

## ما معنى “تحويل CAD إلى PNG”؟
تحويل CAD إلى PNG يعني تحويل محتوى CAD القائم على المتجهات (DWG، DXF، إلخ) إلى صيغة صورة نقطية. تحتفظ PNG بالشفافية وجودة غير مضغوطة، مما يجعلها مثالية للمعاينات على الويب، والوثائق، والتقارير.

## لماذا تحويل CAD إلى PNG (CAD إلى صورة نقطية)؟
- **عرض عالمي:** تعمل PNG على أي جهاز دون الحاجة إلى عارض CAD خاص.  
- **تحميل سريع:** الصور النقطية تُحمَّل فورًا في صفحات الويب.  
- **سهولة التضمين:** يمكن إدراج PNG في ملفات PDF، ومستندات Word، أو عروض الشرائح.  
- **مظهر ثابت:** تحافظ على سماكة الخطوط، والألوان، والطبقات تمامًا كما صُممت.

## المتطلبات المسبقة
قبل البدء، تأكد من وجود ما يلي:

1. **بيئة تطوير Java** – JDK 8 أو أحدث مثبتة ومُعَدَّة.  
2. **مكتبة Aspose.CAD** – قم بتنزيل المكتبة وإضافتها إلى مشروعك. يمكنك العثور على المكتبة **[هنا](https://releases.aspose.com/cad/java/)**.

## استيراد المساحات الاسمية
أضف الاستيرادات المطلوبة إلى فئة Java الخاصة بك لتتمكن من العمل مع كائنات Aspose.CAD.

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## دليل خطوة بخطوة لتحويل CAD إلى PNG

### الخطوة 1: تحميل رسم CAD
أولاً، حمّل ملف CAD المصدر (DXF، DWG، إلخ) باستخدام `Image.load()`.

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

> **نصيحة احترافية:** احتفظ بملفات CAD في مجلد مخصص (مثل `CADConversion`) لتجنب مشاكل المسارات.

### الخطوة 2: تعيين خيارات التحويل النقطي (تصدير dwg إلى صورة)
حدد حجم الصورة الناتجة وإعدادات التحويل النقطي الأخرى.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
```

يمكنك أيضًا التحكم في لون الخلفية، وضع رسم الخطوط، وDPI هنا إذا لزم الأمر.

### الخطوة 3: إنشاء خيارات الصورة (حفظ CAD كـ PNG)
أنشئ كائن `PngOptions` وأرفق إعدادات التحويل النقطي.

```java
ImageOptionsBase options = new PngOptions();
options.setVectorRasterizationOptions(rasterizationOptions);
```

### الخطوة 4: حفظ الصورة النقطية (ملف CAD إلى PNG)
أخيرًا، اكتب ملف PNG إلى القرص.

```java
image.save(dataDir + "conic_pyramid_raster_image_out.png", options);
```

الملف الناتج `conic_pyramid_raster_image_out.png` هو تمثيل PNG عالي الدقة للرسم CAD الأصلي.

### كرر للملفات الأخرى
ما عليك سوى تغيير `srcFile` للإشارة إلى ملف CAD آخر وتشغيل الخطوات نفسها. يعمل نفس الكود مع DWG، DWF، وغيرها من الصيغ المدعومة.

## المشكلات الشائعة والحلول
| المشكلة | الحل |
|-------|----------|
| **إخراج PNG فارغ** | تحقق من أن ملف CAD المصدر تم تحميله بنجاح (`Image.load()` لا يجب أن يرمي استثناء). |
| **أبعاد غير صحيحة** | عدّل `PageWidth` / `PageHeight` أو اضبط DPI عبر `rasterizationOptions.setResolution(...)`. |
| **الطبقات مفقودة** | تأكد من أن طبقات ملف CAD غير مخفية؛ استخدم `CadRasterizationOptions.setDrawType(CadDrawTypeMode.Vector);`. |
| **أخطاء الترخيص** | استخدم ملف ترخيص Aspose.CAD صالح (`License license = new License(); license.setLicense("Aspose.CAD.lic");`). |

## الأسئلة المتكررة

**س1: هل Aspose.CAD متوافق مع جميع صيغ CAD؟**  
ج1: يدعم Aspose.CAD مجموعة واسعة من صيغ CAD، بما في ذلك DWG، DXF، DWF، وأكثر. راجع **[الوثائق](https://reference.aspose.com/cad/java/)** للقائمة الكاملة.

**س2: هل يمكنني تخصيص خيارات التحويل النقطي وفق احتياجاتي؟**  
ج2: نعم، يوفر Aspose.CAD مرونة في ضبط خيارات التحويل النقطي، مما يتيح لك تعديل الحجم، DPI، لون الخلفية، إلخ.

**س3: أين يمكنني العثور على دعم للاستفسارات المتعلقة بـ Aspose.CAD؟**  
ج3: زر **[منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19)** للحصول على المساعدة والتفاعل مع المجتمع.

**س4: هل يتوفر إصدار تجريبي مجاني لـ Aspose.CAD للـ Java؟**  
ج4: نعم، يمكنك استكشاف ميزات Aspose.CAD بالحصول على نسخة تجريبية مجانية **[هنا](https://releases.aspose.com/)**.

**س5: كيف يمكنني شراء Aspose.CAD للـ Java؟**  
ج5: لشراء Aspose.CAD للـ Java، زر **[صفحة الشراء](https://purchase.aspose.com/buy)**.

---

**آخر تحديث:** 2025-12-16  
**تم الاختبار مع:** Aspose.CAD للـ Java 24.11 (أحدث نسخة وقت الكتابة)  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}