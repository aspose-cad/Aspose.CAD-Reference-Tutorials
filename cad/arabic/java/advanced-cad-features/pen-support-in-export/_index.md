---
date: 2025-12-10
description: تعلم كيفية إنشاء ملف PDF من CAD باستخدام Aspose.CAD للغة Java مع تخصيص
  القلم. يوضح هذا الدليل خطوة بخطوة كيفية تصدير CAD إلى PDF بكفاءة.
linktitle: Pen Support in Export
second_title: Aspose.CAD Java API
title: كيفية إنشاء ملف PDF من CAD مع دعم القلم في التصدير
url: /ar/java/advanced-cad-features/pen-support-in-export/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# دعم القلم في التصدير

## المقدمة

في عالم تحويلات CAD السريع الحركة، يحتاج المطورون غالبًا إلى **create PDF from CAD** مع الحفاظ على الدقة البصرية. تجعل Aspose.CAD for Java ذلك سهلًا، حيث تقدم خيارات غنية مثل تخصيص القلم التي تتيح لك ضبط أنماط الخطوط بدقة أثناء عملية التصدير. في هذا الدليل سنستعرض مثالًا عمليًا كاملًا يوضح كيفية **export CAD to PDF** باستخدام إعدادات قلم مخصصة، لتتمكن من إنشاء ملفات PDF مصقولة مباشرةً من رسومات DXF.

## إجابات سريعة
- **ماذا يعني “create PDF from CAD”?** تحويل رسم CAD (مثل DXF) إلى مستند PDF مع الحفاظ على جودة المتجه.  
- **أي مكتبة تتعامل مع تخصيص القلم؟** فئة `PenOptions` في Aspose.CAD for Java.  
- **هل يمكنني استخدام ذلك لتنسيقات أخرى؟** نعم – نفس إعدادات القلم تنطبق على PNG، BMP، TIFF، إلخ.  
- **هل أحتاج إلى ترخيص؟** يلزم وجود ترخيص صالح لـ Aspose.CAD للاستخدام في بيئة الإنتاج.  
- **ما هو الحد الأدنى لإصدار Java؟** Java 8 أو أعلى.

## ما هو “create PDF from CAD”؟
إنشاء PDF من CAD يعني تحويل أو رسم ملف CAD إلى ملف PDF إما بطريقة نقطية أو بطريقة متجهة. يتيح ذلك مشاركة التصاميم الهندسية بسهولة، وطباعة، وأرشفة دون الحاجة إلى برنامج CAD لدى المتلقي.

## لماذا نستخدم دعم القلم عند تصدير CAD إلى PDF؟
يدعم القلم التحكم في نهايات الخطوط (caps) والاتصالات (joins) والسُمك، مما يمنحك القدرة على مطابقة العلامة التجارية للشركة أو معايير الرسومات التقنية. يكون ذلك مفيدًا بشكل خاص عندما لا يلبي عرض الخط الافتراضي متطلباتك البصرية.

## المتطلبات المسبقة

- **بيئة تطوير Java** – JDK يعمل (الإصدار 8 أو أحدث) وIDE أو أداة بناء من اختيارك.  
- **مكتبة Aspose.CAD** – حمّل أحدث ملف JAR من الموقع الرسمي [هنا](https://releases.aspose.com/cad/java/).  
- **ملف DXF تجريبي** – في هذا الدرس سنستخدم `conic_pyramid.dxf`.

الآن بعد أن أعددنا الأساس، لنغص في الشيفرة.

## استيراد الحزم

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.PenOptions;
import com.aspose.cad.internal.imaging.LineCap;
```

## الخطوة 1: تحديد دليل المستند الخاص بك

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

> **نصيحة احترافية:** استبدل `"Your Document Directory"` بالمسار المطلق حيث توجد ملفات DXF الخاصة بك.

## الخطوة 2: تحميل ملف CAD

```java
String srcFile = dataDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage) Image.load(srcFile);
```

تقوم طريقة `Image.load` بقراءة ملف DXF وإنشاء كائن `CadImage` يمكننا التلاعب به.

## الخطوة 3: تكوين خيارات التحويل إلى نقطية

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(cadImage.getWidth() * 100);
rasterizationOptions.setPageHeight(cadImage.getHeight() * 100);
```

قم بتعديل أبعاد الصفحة للتحكم في دقة PDF الناتج. الضرب في 100 يعطي مخرجات عالية الدقة مناسبة للطباعة.

## الخطوة 4: تخصيص خيارات القلم

```java
PenOptions penOts = new PenOptions();
penOts.setStartCap(LineCap.Flat);
penOts.setEndCap(LineCap.Flat);
```

هنا نحدد كلًا من نهايات القلم (start و end caps) إلى `Flat`. يمكنك تجربة قيم `LineCap` أخرى (مثل `Round` أو `Square`) للحصول على تأثيرات بصرية مختلفة.

## الخطوة 5: تكوين خيارات تصدير PDF

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

كائن `PdfOptions` يربط إعدادات التحويل إلى نقطية بعملية تصدير PDF.

## الخطوة 6: حفظ ملف PDF المُصدّر

```java
cadImage.save((dataDir + "9LHATT-A56_generated.pdf"), pdfOptions);
```

تنفيذ هذا السطر يكتب ملف PDF باسم `9LHATT-A56_generated.pdf` إلى مجلد `dataDir` الخاص بك، مع تطبيق نمط القلم المخصص الذي حددته.

## حالات الاستخدام الشائعة

- **الوثائق التقنية** – تضمين رسومات هندسية دقيقة في كتيبات PDF.  
- **التقارير الآلية** – إنشاء ملفات PDF من بيانات CAD بشكل فوري في خدمات الويب.  
- **مراقبة الجودة** – تطبيق نهايات خطوط مخصصة لتسليط الضوء على خطوط القياس أو التحملات.

## استكشاف الأخطاء وإصلاحها والنصائح

- **مسار ملف غير صحيح** – تأكد من أن `dataDir` ينتهي بفاصل ملفات (`/` أو `\\`).  
- **ترخيص مفقود** – بدون ترخيص صالح تعمل المكتبة في وضع التقييم، مما قد يضيف علامات مائية.  
- **أنماط خطوط غير متوقعة** – تحقق مرة أخرى من ضبط `PenOptions` قبل استدعاء `save`؛ وإلا ستُستخدم الإعدادات الافتراضية.

## الأسئلة المتكررة

### س1: هل يمكنني تخصيص خيارات القلم لتنسيقات غير PDF؟

نعم، تخصيص القلم الموضح في هذا الدرس ينطبق على تنسيقات صور متعددة، بما في ذلك PDF، PNG، BMP، GIF، JPEG2000، JPEG، PSD، TIFF، و WMF.

### س2: كيف يمكنني التعامل مع أغطية بداية ونهاية مختلفة للأقلام؟

استخدم فئة `PenOptions` لتحديد أغطية البداية والنهاية المطلوبة، مما يمنحك مرونة في تعريف مظهر الخطوط.

### س3: ماذا لو لم أحدد خيارات القلم؟

إذا لم يتم تحديد خيارات القلم صراحةً، سيستخدم النظام الأقلام الافتراضية، والتي قد تختلف حسب السياق.

### س4: هل هناك اعتبارات محددة لخيارات التحويل إلى نقطية؟

قم بتعديل عرض وارتفاع الصفحة في خيارات التحويل إلى نقطية للتحكم في أبعاد الصورة المصدرة.

### س5: أين يمكنني العثور على دعم إضافي أو مناقشات المجتمع؟

استكشف منتدى مجتمع Aspose.CAD على [هنا](https://forum.aspose.com/c/cad/19) للحصول على الدعم والمناقشات.

**آخر تحديث:** 2025-12-10  
**تم الاختبار مع:** Aspose.CAD 24.11 for Java  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}