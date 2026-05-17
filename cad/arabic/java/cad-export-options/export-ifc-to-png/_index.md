---
date: 2026-02-20
description: حوّل ملفات IFC إلى PNG بسهولة مع Aspose.CAD للغة Java. اتبع دليلنا خطوة
  بخطوة.
linktitle: Export IFC to PNG
second_title: Aspose.CAD Java API
title: كيفية تحويل IFC إلى PNG باستخدام Aspose.CAD للغة جافا
url: /ar/java/cad-export-options/export-ifc-to-png/
weight: 18
---

 for Java 24.11" keep.

"**Author:** Aspose" keep.

Then closing shortcodes.

Finally backtop button shortcode.

Make sure to keep all shortcodes exactly.

Now produce final content.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تصدير IFC إلى PNG باستخدام Aspose.CAD for Java

## المقدمة

مرحبًا بكم في هذا البرنامج التعليمي خطوة بخطوة حول **كيفية تحويل IFC إلى PNG** باستخدام Aspose.CAD for Java. سواءً كنت تبني خط أنابيب BIM‑to‑image أو تحتاج إلى معاينات بصرية سريعة لنماذج IFC، فإن هذا الدليل يشرح لك كل التفاصيل حتى تتمكن من **تحويل IFC إلى PNG** بشكل موثوق في تطبيقات Java الخاصة بك.

## إجابات سريعة
- **ما المكتبة المطلوبة؟** Aspose.CAD for Java  
- **هل يمكنني تحويل IFC إلى PNG ببضع أسطر من الشيفرة؟** Yes – the core process fits in under 20 lines.  
- **هل أحتاج إلى ترخيص للإنتاج؟** A temporary license works for testing; a full license is required for commercial use.  
- **هل الإخراج قابل للتوسيع؟** The rasterization options let you set any pixel dimensions you need.  
- **ما نسخة Java المدعومة؟** Java 8 or higher.

## ما هو “convert IFC to PNG”؟
تحويل IFC (Industry Foundation Classes) إلى PNG يعني تحويل بيانات نموذج المبنى ثلاثي الأبعاد إلى صورة نقطية ثنائية الأبعاد. هذا مفيد لإنشاء صور مصغرة، أو تضمين النماذج في التقارير، أو إنشاء تصورات جاهزة للويب دون الحاجة إلى عارض CAD كامل.

## لماذا تستخدم Aspose.CAD for Java؟
- **دعم كامل** للعديد من صيغ CAD، بما في ذلك IFC.  
- **بدون تبعيات خارجية** – جافا صافية، سهل التكامل.  
- **تحكم دقيق** في عملية التحويل إلى نقطية (الدقة، الخلفية، وزن الخط).  
- **متعدد المنصات** – يعمل على Windows وLinux وmacOS.

## المتطلبات المسبقة

قبل أن نبدأ، تأكد من أن لديك ما يلي:

- **مكتبة Aspose.CAD** – قم بتنزيل وتثبيت مكتبة Aspose.CAD للـ Java من [رابط التحميل](https://releases.aspose.com/cad/java/).  
- **دليل المستندات** – مجلد على نظامك يحتوي على ملف IFC الذي تريد تحويله.

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
أولاً، حدد المجلد الذي يوجد فيه ملف IFC الخاص بك وقم بتحميله.

```java
String dataDir = "Your Document Directory" + "ExportingIFC/";
String fileName = dataDir + "example.ifc";
IfcImage cadImage = (IfcImage)Image.load(fileName);
```

> **لماذا هذا مهم:** تحميل الملف كـ `IfcImage` يمنحك إمكانية الوصول إلى خيارات التحويل إلى نقطية الخاصة بـ Cad لاحقًا.

### الخطوة 2: ضبط خيارات المتجه (التحويل إلى نقطية)
حدد أبعاد الإخراج وأي إعدادات أخرى متعلقة بالمتجه.

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

> يمكنك تعديل `PageWidth` و `PageHeight` للتحكم في دقة PNG النهائية، وهو أمر أساسي عندما **تحفظ ملفات PNG java** للطباعة عالية الجودة.

### الخطوة 3: تكوين خيارات PNG
اربط خيارات التحويل إلى نقطية بمصدّر PNG.

```java
PngOptions pngOptions = new PngOptions();
pngOptions.setVectorRasterizationOptions(vectorOptions);
```

### الخطوة 4: حفظ الصورة كـ PNG
أخيرًا، اكتب الصورة المحوّلة إلى ملف على القرص.

```java
String outPath = dataDir + "example.png";
cadImage.save(outPath, pngOptions);
```

> بعد هذه الخطوة تكون قد **قمت بتحويل IFC إلى PNG** بنجاح ويمكنك استخدام `example.png` الناتج في أي مكان تحتاج فيه إلى صورة نقطية.

## حالات الاستخدام الشائعة
- **إنشاء صور مصغرة** لنماذج BIM في بوابات الويب.  
- **إدراج لقطات مخطط الطوابق** في تقارير PDF.  
- **تحويل دفعات تلقائي** لمكتبات IFC الكبيرة لأغراض الأرشفة.

## استكشاف الأخطاء وإصلاحها والنصائح
- **مشكلات الذاكرة:** عند تحويل ملفات IFC الكبيرة جدًا، قم بزيادة مساحة الذاكرة للـ JVM (`-Xmx2g` أو أعلى).  
- **الملمس مفقود:** تأكد من أن ملف IFC يشير إلى موارد خارجية يمكن الوصول إليها من `dataDir`.  
- **نصيحة احترافية:** استخدم `vectorOptions.setBackgroundColor(Color.getWhite())` إذا كنت تحتاج خلفية بيضاء بدلاً من PNG الشفاف الافتراضي.

## الأسئلة المتكررة

### س1: هل Aspose.CAD متوافق مع جميع إصدارات ملفات IFC؟
A1: يدعم Aspose.CAD إصدارات مختلفة من ملفات IFC. راجع [الوثائق](https://reference.aspose.com/cad/java/) للحصول على تفاصيل التوافق.

### س2: هل يمكنني تخصيص خيارات التحويل إلى نقطية أكثر؟
A2: بالتأكيد! استكشف [الوثائق](https://reference.aspose.com/cad/java/) للحصول على خيارات تخصيص متقدمة.

### س3: هل تتوفر نسخة تجريبية؟
A3: نعم، يمكنك الوصول إلى النسخة التجريبية المجانية [هنا](https://releases.aspose.com/).

### س4: كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.CAD؟
A4: احصل على ترخيص مؤقت من [هذا الرابط](https://purchase.aspose.com/temporary-license/).

### س5: أين يمكنني طلب المساعدة أو مناقشة المشكلات؟
A5: زر [منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19) للحصول على دعم المجتمع.

## الأسئلة المتكررة

**س: هل يمكنني استخدام هذه الطريقة لتحويل صيغ CAD أخرى إلى PNG؟**  
A: نعم، يدعم Aspose.CAD العديد من الصيغ (DWG، DXF، DGN، إلخ). فقط غير امتداد الملف وحول إلى فئة الصورة المناسبة.

**س: هل تسمح المكتبة بتعيين DPI مخصص؟**  
A: يمكنك التحكم في DPI بشكل غير مباشر عن طريق ضبط `PageWidth`/`PageHeight` بالنسبة للحجم الفيزيائي المطلوب.

**س: هل إخراج PNG بدون فقدان؟**  
A: PNG هو تنسيق بدون فقدان، لذا تحتفظ الصورة النقطية بجودة بصرية كاملة للبيانات المتجهة.

## الخاتمة

لقد تعلمت الآن كيفية **تحويل IFC إلى PNG** بفعالية باستخدام Aspose.CAD for Java. باتباع هذه الخطوات يمكنك دمج تحويل IFC‑to‑PNG في أي سير عمل قائم على Java، سواء كان أداة سطح مكتب، خدمة على الخادم، أو وظيفة سحابية.

---

**Last Updated:** 2026-02-20  
**Tested With:** Aspose.CAD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}