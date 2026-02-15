---
date: 2026-02-15
description: تعلم كيفية إنشاء ملف PDF من CAD باستخدام Aspose.CAD للغة Java مع تخصيص
  القلم. يوضح هذا الدليل خطوة بخطوة كيفية تصدير CAD إلى PDF بكفاءة.
linktitle: Pen Support in Export
second_title: Aspose.CAD Java API
title: كيفية إنشاء ملف PDF من CAD مع دعم القلم في التصدير
url: /ar/java/advanced-cad-features/pen-support-in-export/
weight: 13
---

 keep them.

Now produce final content.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# دعم القلم في التصدير

## المقدمة

في عالم تحويلات CAD السريع الحركة، يحتاج المطورون غالبًا إلى **إنشاء PDF من CAD** مع الحفاظ على الدقة البصرية. تجعل Aspose.CAD for Java ذلك بسيطًا، حيث تقدم خيارات غنية مثل تخصيص القلم الذي يتيح لك ضبط أنماط الخط بدقة أثناء عملية التصدير. في هذا الدليل سنستعرض مثالًا عمليًا كاملًا يوضح كيفية **تصدير CAD إلى PDF** باستخدام إعدادات قلم مخصصة، بحيث يمكنك إنشاء ملفات PDF مصقولة مباشرةً من رسومات DXF.

## إجابات سريعة
- **ماذا يعني “إنشاء PDF من CAD”؟** تحويل رسم CAD (مثل DXF) إلى مستند PDF مع الحفاظ على جودة المتجه.  
- **أي مكتبة تتعامل مع تخصيص القلم؟** فئة `PenOptions` في Aspose.CAD for Java.  
- **هل يمكنني استخدام ذلك مع صيغ أخرى؟** نعم – نفس إعدادات القلم تنطبق على PNG، BMP، TIFF، إلخ.  
- **هل أحتاج إلى ترخيص؟** يلزم وجود ترخيص Aspose.CAD صالح للاستخدام في الإنتاج.  
- **ما هو الحد الأدنى لإصدار Java؟** Java 8 أو أعلى.

## ما هو “إنشاء PDF من CAD”؟
إنشاء PDF من CAD يعني تحويل رسم CAD إلى ملف PDF إما عن طريق التحويل إلى نقطية أو إلى متجهات. يتيح ذلك مشاركة سهلة، وطباعة، وأرشفة لتصاميم الهندسة دون الحاجة إلى برنامج CAD لدى الطرف المستلم.

## لماذا نستخدم دعم القلم عند تصدير CAD إلى PDF؟
يتيح لك دعم القلم التحكم في نهايات الخطوط (caps)، والاتصالات (joins)، والسُمك، مما يمنحك القدرة على مطابقة هوية الشركة أو معايير الرسومات التقنية. يكون ذلك مفيدًا بشكل خاص عندما لا يلبي عرض الخط الافتراضي متطلباتك البصرية.

## كيفية إنشاء PDF من CAD – دليل خطوة بخطوة
فيما يلي دليل عملي يغطي كل شيء من إعداد بيئتك إلى إنشاء ملف PDF النهائي. اتبع كل خطوة، وستحصل على حل جاهز للاستخدام لت **تصدير CAD إلى PDF** مع تحكم كامل في القلم.

## المتطلبات المسبقة

- **بيئة تطوير Java** – JDK يعمل (8 أو أحدث) وIDE أو أداة بناء حسب اختيارك.  
- **مكتبة Aspose.CAD** – قم بتنزيل أحدث JAR من الموقع الرسمي [هنا](https://releases.aspose.com/cad/java/).  
- **ملف DXF تجريبي** – سنستخدم في هذا الشرح `conic_pyramid.dxf`.

الآن بعد أن وضعنا الأساس، دعنا نغوص في الشيفرة.

## استيراد المساحات الاسمية

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.PenOptions;
import com.aspose.cad.internal.imaging.LineCap;
```

## الخطوة 1: تعريف دليل المستند الخاص بك

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

> **نصيحة احترافية:** استبدل `"Your Document Directory"` بالمسار المطلق حيث توجد ملفات DXF الخاصة بك.

## الخطوة 2: تحميل ملف CAD

```java
String srcFile = dataDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage) Image.load(srcFile);
```

طريقة `Image.load` تقرأ ملف DXF وتُنشئ كائن `CadImage` يمكننا التلاعب به.

## الخطوة 3: تكوين خيارات التحويل إلى نقطية

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(cadImage.getWidth() * 100);
rasterizationOptions.setPageHeight(cadImage.getHeight() * 100);
```

قم بضبط أبعاد الصفحة للتحكم في دقة PDF الناتج. الضرب في 100 يعطي مخرجات عالية الدقة مناسبة للطباعة.

## الخطوة 4: تخصيص خيارات القلم

```java
PenOptions penOts = new PenOptions();
penOts.setStartCap(LineCap.Flat);
penOts.setEndCap(LineCap.Flat);
```

هنا نضبط كل من نهايات القلم (start و end) إلى `Flat`. يمكنك تجربة قيم `LineCap` أخرى (مثل `Round`، `Square`) للحصول على تأثيرات بصرية مختلفة.

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

تشغيل هذا السطر يكتب ملف PDF باسم `9LHATT-A56_generated.pdf` إلى مجلد `dataDir` الخاص بك، مع تطبيق نمط القلم المخصص الذي حددته.

## حالات الاستخدام الشائعة

- **الوثائق التقنية** – تضمين رسومات هندسية دقيقة في أدلة PDF.  
- **التقارير الآلية** – إنشاء ملفات PDF من بيانات CAD مباشرةً في خدمات الويب.  
- **مراقبة الجودة** – تطبيق نهايات خطوط مخصصة لتسليط الضوء على خطوط القياس أو التحملات.

## استكشاف الأخطاء وإصلاحها والنصائح

- **مسار ملف غير صحيح** – تأكد من أن `dataDir` ينتهي بفاصل ملفات (`/` أو `\\`).  
- **الترخيص مفقود** – بدون ترخيص صالح تعمل المكتبة في وضع التقييم، مما قد يضيف علامات مائية.  
- **أنماط خطوط غير متوقعة** – تحقق مرة أخرى من ضبط `PenOptions` قبل استدعاء `save`؛ وإلا سيتم استخدام الإعدادات الافتراضية.

## الأسئلة المتكررة

### س1: هل يمكنني تخصيص خيارات القلم لصيغ أخرى غير PDF؟
A1: نعم، تخصيص القلم الموضح في هذا الشرح ينطبق على صيغ صور متعددة، بما في ذلك PDF، PNG، BMP، GIF، JPEG2000، JPEG، PSD، TIFF، و WMF.

### س2: كيف يمكنني التعامل مع نهايات مختلفة للقلم (start و end)؟
A2: استخدم فئة `PenOptions` لتعيين النهايات المطلوبة (start و end)، مما يوفر مرونة في تحديد مظهر الخطوط.

### س3: ماذا لو لم أحدد خيارات القلم؟
A3: إذا لم يتم ضبط خيارات القلم صراحةً، سيستخدم النظام الأقلام الافتراضية، والتي قد تختلف في سياقات مختلفة.

### س4: هل هناك اعتبارات خاصة لخيارات التحويل إلى نقطية؟
A4: اضبط عرض وارتفاع الصفحة في خيارات التحويل إلى نقطية للتحكم في أبعاد الصورة المصدرة.

### س5: أين يمكنني العثور على دعم إضافي أو مناقشات المجتمع؟
A5: استكشف منتدى مجتمع Aspose.CAD على [هنا](https://forum.aspose.com/c/cad/19) للحصول على الدعم والمناقشات.

---

**آخر تحديث:** 2026-02-15  
**تم الاختبار مع:** Aspose.CAD 24.11 for Java  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}