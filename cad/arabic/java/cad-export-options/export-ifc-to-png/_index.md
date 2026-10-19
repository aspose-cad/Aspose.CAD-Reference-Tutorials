---
date: 2026-10-19
description: تعلم كيفية إنشاء ملفات IFC بصور مصغرة PNG باستخدام Aspose.CAD for Java
  في بضع أسطر من الشيفرة فقط.
keywords:
- create png thumbnail ifc
- ifc to png conversion
- aspose cad java
- java image processing
- bIM visualization
lastmod: 2026-10-19
linktitle: تصدير IFC إلى PNG
og_description: أنشئ ملفات IFC بصور مصغرة PNG بسهولة باستخدام Aspose.CAD for Java.
  يوضح لك هذا الدليل خطوة بخطوة كيفية تحميل النماذج، تحويلها إلى رسومات نقطية، وحفظها
  كصور PNG عالية الجودة.
og_image_alt: Developer guide showing Java code that converts IFC files to PNG thumbnails
  using Aspose.CAD
og_title: إنشاء صورة مصغرة PNG لملفات IFC باستخدام Aspose.CAD for Java
schemas:
- author: Aspose
  dateModified: '2026-10-19'
  description: Learn how to create PNG thumbnail IFC files with Aspose.CAD for Java
    in just a few lines of code.
  headline: How to create PNG thumbnail IFC with Aspose.CAD for Java
  type: TechArticle
- description: Learn how to create PNG thumbnail IFC files with Aspose.CAD for Java
    in just a few lines of code.
  name: How to create PNG thumbnail IFC with Aspose.CAD for Java
  steps:
  - name: load the IFC file
    text: First, point to the folder where your IFC file lives and load it with `CadImage.load`.
      `CadImage.load` reads a CAD file and returns an image object that can be rasterized.
      > **Why this matters:** Loading the file as a `CadImage` gives you access to
      vector‑raster conversion options that control resol
  - name: set rasterization options
    text: Define the output dimensions and any other vector‑related settings through
      `VectorRasterizationOptions`. `VectorRasterizationOptions` lets you specify
      output size, background color, and other rasterization parameters. > Adjust
      `PageWidth` and `PageHeight` to control the final PNG resolution, which i
  - name: configure PNG options
    text: Link the rasterization options to the PNG exporter by creating a `PngOptions`
      instance.
  - name: save the image as PNG
    text: Finally, write the rasterized image to disk using the `save` method. `save`
      writes the rasterized image to the specified file path in the chosen format.
      > After this step you have successfully **created a PNG thumbnail IFC** and
      can use the resulting `example.png` anywhere you need a raster image.
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD supports many formats (DWG, DXF, DGN, etc.). Simply change
      the file extension and load the appropriate image class.
    question: Can I use this approach to convert other CAD formats to PNG?
  - answer: DPI is controlled indirectly via `PageWidth`/`PageHeight`. Adjust these
      values relative to the desired physical size to achieve the required DPI.
    question: Does the library let me set a custom DPI?
  - answer: PNG is a lossless format, so the rasterized image retains the full visual
      fidelity of the original vector data.
    question: Is the PNG output loss‑less?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- ifc conversion
- png thumbnail
- aspose.cad
- java image processing
- bim visualization
title: كيفية إنشاء صورة مصغرة PNG لملفات IFC باستخدام Aspose.CAD for Java
url: /ar/java/cad-export-options/export-ifc-to-png/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تصدير IFC إلى PNG باستخدام Aspose.CAD للـ Java

## مقدمة

في هذا البرنامج التعليمي ستتعلم كيفية **إنشاء ملفات PNG مصغرة لـ IFC** باستخدام Aspose.CAD للـ Java. سواء كنت بحاجة إلى معاينات سريعة لبورتال BIM، أو إنشاء مصغرات لنظام إدارة المستندات، أو أتمتة التحويلات الدفعية، فإن الخطوات أدناه تتيح لك تحويل نموذج IFC ثلاثي الأبعاد إلى صورة PNG ثنائية الأبعاد واضحة في بضع أسطر من كود Java.

## إجابات سريعة
- **ما المكتبة المطلوبة؟** Aspose.CAD for Java.  
- **هل يمكنني إنشاء PNG مصغرة لـ IFC في بضع أسطر من الكود؟** نعم – سير العمل الكامل يتناسب مع أقل من 20 سطرًا.  
- **هل أحتاج إلى ترخيص للإنتاج؟** ترخيص مؤقت يعمل للاختبار؛ ترخيص كامل مطلوب للنشر التجاري.  
- **هل الإخراج قابل للتوسيع؟** يمكنك ضبط أي أبعاد بكسل، لذا يتوسع PNG إلى أي حجم تحتاجه.  
- **ما نسخة Java المدعومة؟** Java 8 أو أعلى.

## ما هو “تحويل IFC إلى PNG”؟

تحويل IFC (Industry Foundation Classes) إلى PNG يعني تحويل نموذج المبنى ثلاثي الأبعاد إلى صورة نقطية ثنائية الأبعاد. هذه العملية تنشئ مصغرة بصرية يمكن عرضها في المتصفحات أو التقارير أو التطبيقات المحمولة دون الحاجة إلى عارض CAD كامل.

## لماذا نستخدم Aspose.CAD للـ Java؟

يدعم Aspose.CAD **أكثر من 30 تنسيق CAD و BIM**، بما في ذلك IFC و DWG و DXF و DGN، ويمكنه معالجة ملفات تصل إلى **2 GB** دون تحميل المستند بالكامل في الذاكرة. المكتبة مكتوبة بلغة Java فقط، ولا تعتمد على أي مكونات خارجية، وتعمل على Windows و Linux و macOS، مما يجعلها مثالية لتوليد الصور على الخادم.  
توفر عملية تمثيل نقطي عالية الأداء، ودعمًا واسعًا للتنسيقات، وتكاملًا سهلاً مع تطبيقات Java.

## المتطلبات المسبقة

- **مكتبة Aspose.CAD** – قم بتنزيل أحدث JAR من [رابط التحميل](https://releases.aspose.com/cad/java/).  
- **مجموعة تطوير Java** – JDK 8 أو أحدث مثبت على جهازك.  
- **ملف مصدر IFC** – ضع الملف في مجلد يمكنك الإشارة إليه من الكود.

## استيراد مساحات الأسماء

توفر حزمة `com.aspose.cad` جميع الفئات التي تحتاجها. `CadImage` هي نقطة الدخول لتحميل ملفات CAD، بينما `PngOptions` تُعد إعدادات التمثيل النقطي.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## كيفية إنشاء PNG مصغرة لـ IFC في Java؟

حمّل ملف IFC، عرّف خيارات التمثيل النقطي، واحفظ النتيجة كصورة PNG – هذا هو سير العمل الكامل للتحويل. الأقسام التالية تفصل كل خطوة، بحيث يمكنك نسخ‑لصق الشفرات في مشروعك وتشغيلها فورًا.

### الخطوة 1: تحميل ملف IFC
أولاً، حدد المجلد الذي يوجد فيه ملف IFC وقم بتحميله باستخدام `CadImage.load`.  
`CadImage.load` يقرأ ملف CAD ويعيد كائن صورة يمكن تمثيله نقطيًا.

```java
String dataDir = "Your Document Directory" + "ExportingIFC/";
String fileName = dataDir + "example.ifc";
IfcImage cadImage = (IfcImage)Image.load(fileName);
```

> **لماذا هذا مهم:** تحميل الملف كـ `CadImage` يمنحك إمكانية الوصول إلى خيارات تحويل المتجه إلى نقطي التي تتحكم في الدقة، لون الخلفية، وسمك الخط.

### الخطوة 2: ضبط خيارات التمثيل النقطي
عرّف أبعاد الإخراج وأي إعدادات أخرى متعلقة بالمتجه عبر `VectorRasterizationOptions`.  
`VectorRasterizationOptions` يتيح لك تحديد حجم الإخراج، لون الخلفية، وغيرها من معلمات التمثيل النقطي.

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

> قم بضبط `PageWidth` و `PageHeight` للتحكم في دقة PNG النهائية، وهو أمر أساسي عندما **تحفظ ملفات PNG java** للطباعة عالية الجودة أو المصغرات على الويب.

### الخطوة 3: تكوين خيارات PNG
اربط خيارات التمثيل النقطي بمصدّر PNG بإنشاء مثيل من `PngOptions`.

```java
PngOptions pngOptions = new PngOptions();
pngOptions.setVectorRasterizationOptions(vectorOptions);
```

### الخطوة 4: حفظ الصورة كـ PNG
أخيرًا، اكتب الصورة الممثلة نقطيًا إلى القرص باستخدام طريقة `save`.  
`save` يكتب الصورة الممثلة نقطيًا إلى مسار الملف المحدد بالتنسيق المختار.

```java
String outPath = dataDir + "example.png";
cadImage.save(outPath, pngOptions);
```

> بعد هذه الخطوة تكون قد **أنشأت PNG مصغرة لـ IFC** بنجاح ويمكنك استخدام `example.png` الناتج في أي مكان تحتاج فيه إلى صورة نقطية.

## حالات الاستخدام الشائعة
- **إنشاء مصغرات** لنماذج BIM في بوابات الويب.  
- **إدراج لقطات مخططات الطوابق** في تقارير PDF أو Word.  
- **تحويل دفعي آلي** لمكتبات IFC الكبيرة لأغراض الأرشفة أو مشاريع النقل.

## استكشاف الأخطاء والنصائح
- **مشكلات الذاكرة:** بالنسبة لملفات IFC الكبيرة جدًا، قم بزيادة مساحة heap للـ JVM (`-Xmx2g` أو أعلى).  
- **الملمس مفقود:** تأكد من أن الموارد الخارجية لملف IFC يمكن الوصول إليها من `dataDir`.  
- **نصيحة احترافية:** استخدم `vectorOptions.setBackgroundColor(Color.getWhite())` إذا كنت تفضل خلفية بيضاء بدلاً من PNG الشفاف الافتراضي.

## الأسئلة المتكررة

### س1: هل Aspose.CAD متوافق مع جميع إصدارات ملفات IFC؟
ج1: يدعم Aspose.CAD إصدارات IFC المختلفة. راجع [التوثيق](https://reference.aspose.com/cad/java/) للحصول على معلومات تفصيلية حول التوافق.

### س2: هل يمكنني تخصيص خيارات التمثيل النقطي أكثر؟
ج2: بالتأكيد! استكشف [التوثيق](https://reference.aspose.com/cad/java/) للحصول على إعدادات متقدمة مثل التحكم في DPI، وإزالة التعرجات، وسمك الخط.

### س3: هل تتوفر نسخة تجريبية؟
ج3: نعم، يمكنك تنزيل النسخة التجريبية المجانية من [Aspose.CAD free trial](https://releases.aspose.com/).

### س4: كيف يمكنني الحصول على ترخيص مؤقت للاختبار؟
ج4: احصل على ترخيص مؤقت من [صفحة الترخيص المؤقت لـ Aspose.CAD](https://purchase.aspose.com/temporary-license/).

### س5: أين يمكنني طرح الأسئلة أو الإبلاغ عن المشكلات؟
ج5: انضم إلى المجتمع في [منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19) للحصول على الدعم من مهندسي Aspose وزملاء المطورين.

## الأسئلة المتكررة

**س: هل يمكنني استخدام هذه الطريقة لتحويل تنسيقات CAD أخرى إلى PNG؟**  
**ج:** نعم، يدعم Aspose.CAD العديد من التنسيقات (DWG، DXF، DGN، إلخ). ما عليك سوى تغيير امتداد الملف وتحميل الفئة المناسبة للصورة.

**س: هل تسمح المكتبة بتعيين DPI مخصص؟**  
**ج:** يتم التحكم في DPI بشكل غير مباشر عبر `PageWidth`/`PageHeight`. اضبط هذه القيم بالنسبة إلى الحجم الفيزيائي المطلوب لتحقيق DPI المطلوب.

**س: هل إخراج PNG خالٍ من الفقدان؟**  
**ج:** PNG هو تنسيق خالٍ من الفقدان، لذا تحتفظ الصورة الممثلة نقطيًا بجودة بصرية كاملة للبيانات المتجهة الأصلية.

## الخاتمة

أصبح لديك الآن طريقة كاملة وجاهزة للإنتاج **لإنشاء ملفات PNG مصغرة لـ IFC** باستخدام Aspose.CAD للـ Java. دمج هذه الخطوات في أدوات سطح المكتب، أو الخدمات على الخادم، أو وظائف السحابة لأتمتة خطوط أنابيب تصور BIM وتقديم مصغرات سريعة وعالية الجودة للمستخدمين النهائيين.

---

**Last Updated:** 2026-10-19  
**Tested With:** Aspose.CAD for Java 24.11  
**Author:** Aspose

## دروس ذات صلة

- [كيفية تحويل STL إلى PNG باستخدام Aspose.CAD للـ Java](/cad/java/cad-export-options/export-stl-to-png/)
- [تحويل DWG إلى PNG – حفظ CAD كـ PNG باستخدام Aspose.CAD للـ Java](/cad/java/cad-drawing-conversion/convert-cad-drawing-to-raster-image/)
- [تصدير DWG إلى PDF في Java – ضبط حجم صفحة PDF باستخدام Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}