---
title: ضبط حجم رسم CAD باستخدام نوع الوحدة مع Aspose.CAD لـ Java
linktitle: ضبط حجم رسم CAD باستخدام نوع الوحدة
second_title: Aspose.CAD جافا API
description: اكتشف قوة Aspose.CAD لـ Java في ضبط أحجام رسم CAD دون عناء. اتبع دليلنا خطوة بخطوة للحصول على الدقة والقدرة على التكيف.
type: docs
weight: 14
url: /ar/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/
---
## مقدمة

في عالم التصميم بمساعدة الكمبيوتر (CAD) المتطور باستمرار، تعد الدقة والقدرة على التكيف أمرًا بالغ الأهمية. أحد المتطلبات الشائعة هو ضبط حجم رسومات CAD بناءً على أنواع الوحدات المحددة. يظهر Aspose.CAD for Java كحليف قوي، حيث يوفر إمكانات سلسة لمعالجة ملفات CAD برمجيًا.

## المتطلبات الأساسية

قبل الغوص في البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:

- بيئة تطوير Java: تأكد من إعداد بيئة تطوير Java وظيفية على جهازك.

-  Aspose.CAD لمكتبة Java: قم بتنزيل مكتبة Aspose.CAD ودمجها في مشروع Java الخاص بك. يمكنك الحصول على المكتبة[هنا](https://releases.aspose.com/cad/java/).

## استيراد مساحات الأسماء

في كود Java الخاص بك، قم بتضمين مساحات الأسماء الضرورية للوصول إلى وظائف Aspose.CAD. أضف الواردات التالية:

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

الآن، دعنا نقسم عملية ضبط حجم رسم CAD باستخدام نوع الوحدة إلى خطوات يمكن التحكم فيها:

## الخطوة 1: تحديد دليل البيانات

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

قم بتعيين المسار للدليل الذي توجد به ملفات CAD الخاصة بك.

## الخطوة 2: تحميل رسم CAD

```java
String sourceFilePath = dataDir + "sample.dwg";
Image image = Image.load(sourceFilePath);
```

 قم بتحميل رسم CAD باستخدام Aspose.CAD`Image` فصل.

## الخطوة 3: إنشاء خيارات BMP

```java
BmpOptions bmpOptions = new BmpOptions();
```

 إنشاء مثيل`BmpOptions` فئة لتصدير تخطيط CAD إلى تنسيق BMP.

## الخطوة 4: تكوين خيارات التنقيط

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

 إنشاء مثيل ل`CadRasterizationOptions` وربطه مع`BmpOptions` لتنقيط المتجهات.

## الخطوة 5: ضبط نوع الوحدة

```java
cadRasterizationOptions.setUnitType(UnitType.Centimeter);
```

حدد نوع الوحدة المطلوبة لرسم CAD. في هذا المثال، قمنا بتعيينه إلى سنتيمتر.

## الخطوة 6: تعيين التخطيطات

```java
cadRasterizationOptions.setLayouts(new String[] { "Model" });
```

حدد التخطيطات التي يجب مراعاتها أثناء التصدير. في هذه الحالة، قمنا باختيار تخطيط "النموذج".

## الخطوة 7: التصدير إلى BMP

```java
String outPath = sourceFilePath + ".bmp";
image.save(outPath, bmpOptions);
```

وأخيرًا، احفظ رسم CAD المعدل بتنسيق BMP.

## خاتمة

مع Aspose.CAD لـ Java، أصبح ضبط أحجام رسم CAD أمرًا سهلاً. يرشدك هذا البرنامج التعليمي خلال العملية، مع التركيز على أهمية كل خطوة في تحقيق نتائج دقيقة.

## الأسئلة الشائعة

### س1: هل يمكنني استخدام Aspose.CAD لـ Java مع لغات برمجة أخرى؟

ج1: يدعم Aspose.CAD Java بشكل أساسي، ولكن هناك إصدارات متاحة للغات أخرى مثل .NET.

### س2: هل هناك أي خيارات ترخيص لـ Aspose.CAD؟

 ج2: نعم، يمكنك استكشاف خيارات الترخيص وشراء Aspose.CAD[هنا](https://purchase.aspose.com/buy).

### س3: هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.CAD؟

 ج3: بالتأكيد، يمكنك الوصول إلى النسخة التجريبية المجانية[هنا](https://releases.aspose.com/).

### س4: كيف يمكنني الحصول على دعم Aspose.CAD لـ Java؟

 ج4: قم بزيارة منتدى Aspose.CAD[هنا](https://forum.aspose.com/c/cad/19) للحصول على الدعم الشامل.

### س5: هل يمكنني الحصول على ترخيص مؤقت لـ Aspose.CAD؟

 ج5: نعم، يمكنك الحصول على ترخيص مؤقت[هنا](https://purchase.aspose.com/temporary-license/).