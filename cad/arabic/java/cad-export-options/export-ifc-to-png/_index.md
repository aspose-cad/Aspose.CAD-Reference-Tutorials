---
date: 2025-12-21
description: حوّل IFC إلى PNG بسهولة مع Aspose.CAD للـ Java. اتبع دليلنا خطوة بخطوة.
linktitle: Export IFC to PNG
second_title: Aspose.CAD Java API
title: تحويل IFC إلى PNG باستخدام Aspose.CAD للـ Java
url: /ar/java/cad-export-options/export-ifc-to-png/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تحويل IFC إلى PNG باستخدام Aspose.CAD للـ Java

## المقدمة

في هذا الدرس ستتعلم **كيفية تحويل IFC إلى PNG** باستخدام مكتبة Aspose.CAD القوية للـ Java. سواءً كنت تبني عارض BIM، أو تولد صورًا مصغرة لب portal بناء، أو تقوم بأتمتة خطوط توثيق، فإن تحويل ملفات IFC (Industry Foundation Classes) إلى صور نقطية هو طلب شائع. سنستعرض كل خطوة، نشرح السبب وراء الإعدادات، ونقدم لك نصائح للحصول على أفضل النتائج البصرية.

## إجابات سريعة
- **ما المكتبة المطلوبة؟** Aspose.CAD للـ Java (يتوفر نسخة تجريبية مجانية).  
- **ما إصدارات IFC المدعومة؟** معظم ملفات IFC 2x3 و IFC4 يتم التعامل معها.  
- **الوقت المعتاد للتحويل؟** بضع ثوانٍ للنماذج القياسية؛ يعتمد على حجم الملف.  
- **هل أحتاج إلى ترخيص؟** يلزم الحصول على ترخيص مؤقت للاستخدام في الإنتاج.  
- **هل يمكن تخصيص حجم الصورة؟** نعم – استخدم `CadRasterizationOptions` لتحديد العرض والارتفاع.

## ما هو “تحويل IFC إلى PNG”؟
تحويل IFC إلى PNG يعني تحويل نموذج بناء ثلاثي الأبعاد (IFC) إلى صورة نقطية ثنائية الأبعاد (PNG). هذه العملية تُسطّح الهندسة، تُطبق الأنماط البصرية الافتراضية، وتنتج صورة محمولة يمكن عرضها في المتصفحات، التقارير، أو التطبيقات المحمولة دون الحاجة إلى عارض CAD.

## لماذا نستخدم Aspose.CAD للـ Java؟
- **بدون برنامج CAD خارجي** – API نقي بلغة Java، يعمل على أي منصة.  
- **تصيير عالي الدقة** – يحافظ على أوزان الخطوط، الألوان، والطبقات.  
- **تحكم كامل** – خيارات التصوير النقطي تتيح لك تحديد الدقة، الخلفية، والمزيد.  
- **ترخيص سهل** – النسخ التجريبية والترخيص المؤقت يبسطان عملية التقييم.

## المتطلبات الأساسية

قبل أن نبدأ، تأكد من وجود ما يلي:

- **مكتبة Aspose.CAD** – حمّلها وثبتها من [رابط التحميل](https://releases.aspose.com/cad/java/).  
- **مجموعة تطوير جافا (JDK)** – الإصدار 8 أو أحدث.  
- **مجلد** يحتوي على ملف IFC الذي تريد تحويله.

## استيراد المساحات الاسمية

في مشروع Java الخاص بك، استورد الفئات اللازمة:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## دليل خطوة بخطوة

### الخطوة 1: تحميل ملف IFC

```java
String dataDir = "Your Document Directory" + "ExportingIFC/";
String fileName = dataDir + "example.ifc";
IfcImage cadImage = (IfcImage)Image.load(fileName);
```

هنا نقوم بتحميل ملف IFC المصدر إلى كائن `IfcImage`. تقوم Aspose.CAD تلقائيًا بتحليل بنية IFC وتحضيرها للتصوير النقطي.

### الخطوة 2: ضبط خيارات المتجه (التصوير النقطي)

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

`CadRasterizationOptions` يتحكم في طريقة تسطيح الهندسة ثلاثية الأبعاد. عدّل `PageWidth` و `PageHeight` لتتناسب مع دقة PNG المطلوبة. القيم الأكبر تعطي صورًا ذات تفاصيل أعلى ولكنها تستهلك المزيد من الذاكرة.

### الخطوة 3: تكوين إعدادات تصدير PNG

```java
PngOptions pngOptions = new PngOptions();
pngOptions.setVectorRasterizationOptions(vectorOptions);
```

`PngOptions` يحدد لـ Aspose.CAD أن ينتج ملف PNG ويربط إعدادات التصوير النقطي التي عُرّفت في الخطوة السابقة.

### الخطوة 4: حفظ الصورة كـ PNG

```java
String outPath = dataDir + "example.png";
cadImage.save(outPath, pngOptions);
```

طريقة `save` تكتب الصورة المصوّرة إلى القرص. بعد تنفيذ هذا السطر، ستجد `example.png` في نفس الدليل الذي يحتوي على ملف IFC المصدر.

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|-------|-----|
| **صورة PNG فارغة** | تم ضبط عرض/ارتفاع خيارات التصوير النقطي إلى 0 أو قيمة صغيرة جدًا. | تأكد من أن `PageWidth` و `PageHeight` أعداد صحيحة موجبة (مثلاً 1500). |
| **غياب الطبقات أو الألوان** | العرض الافتراضي قد يخفي بعض الطبقات. | استخدم `vectorOptions.setRenderMode(CadRenderMode.Wireframe)` أو عدّل رؤية الطبقات عبر الـ API إذا لزم الأمر. |
| **خطأ نفاد الذاكرة** للملفات الكبيرة | دقة عالية جدًا تستهلك الكثير من الذاكرة. | قلل الدقة أو عالج النموذج على أقسام. |

## الأسئلة المتكررة

### س1: هل Aspose.CAD متوافق مع جميع إصدارات ملفات IFC؟

ج1: يدعم Aspose.CAD إصدارات مختلفة من ملفات IFC. راجع [الوثائق](https://reference.aspose.com/cad/java/) للحصول على تفاصيل التوافق.

### س2: هل يمكنني تخصيص خيارات التصوير النقطي أكثر؟

ج2: بالتأكيد! استكشف [الوثائق](https://reference.aspose.com/cad/java/) للحصول على خيارات تخصيص متقدمة.

### س3: هل هناك نسخة تجريبية متاحة؟

ج3: نعم، يمكنك الحصول على النسخة التجريبية المجانية [من هنا](https://releases.aspose.com/).

### س4: كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.CAD؟

ج4: احصل على ترخيص مؤقت من [هذا الرابط](https://purchase.aspose.com/temporary-license/).

### س5: أين يمكنني طلب المساعدة أو مناقشة المشكلات؟

ج5: زر منتدى [Aspose.CAD](https://forum.aspose.com/c/cad/19) للحصول على دعم المجتمع.

## أسئلة شائعة إضافية

**س: هل يمكنني تحويل عدة ملفات IFC دفعيًا؟**  
ج: نعم. ضع منطق التحميل والحفظ داخل حلقة تتكرر على قائمة مسارات الملفات.

**س: كيف أغيّر لون خلفية PNG؟**  
ج: اضبط `vectorOptions.setBackgroundColor(Color.getWhite())` (أو أي `java.awt.Color`) قبل إنشاء `PngOptions`.

**س: هل يمكن التصدير إلى صيغ نقطية أخرى مثل JPEG أو BMP؟**  
ج: بالتأكيد. استبدل `PngOptions` بـ `JpegOptions` أو `BmpOptions` وعدّل أي إعدادات خاصة بالصيغ.

**س: هل يجب تحرير الموارد بعد التحويل؟**  
ج: استدعِ `cadImage.dispose()` عند الانتهاء لتحرير الذاكرة الأصلية.

---

**آخر تحديث:** 2025-12-21  
**تم الاختبار مع:** Aspose.CAD للـ Java 24.12 (أحدث نسخة وقت الكتابة)  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}