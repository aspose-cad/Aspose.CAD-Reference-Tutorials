---
title: دعم القلم في التصدير
linktitle: دعم القلم في التصدير
second_title: Aspose.CAD جافا API
description: التخصيص الرئيسي للقلم في تصدير CAD باستخدام Aspose.CAD لـ Java. اتبع دليلنا خطوة بخطوة للتكامل السلس.
weight: 13
url: /ar/java/advanced-cad-features/pen-support-in-export/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# دعم القلم في التصدير

## مقدمة

في المشهد المتطور باستمرار لتحويلات CAD (التصميم بمساعدة الكمبيوتر)، يظهر Aspose.CAD for Java كأداة قوية توفر إمكانات واسعة النطاق لمعالجة ملفات CAD. ومن بين ميزاته المتعددة الاستخدامات، يبرز دعم تخصيص القلم أثناء التصدير، مما يسمح للمستخدمين بتخصيص مظهر الصور المصدرة. سيرشدك هذا البرنامج التعليمي خلال عملية الاستفادة من دعم القلم في وظيفة التصدير، مع التركيز على التنفيذ العملي باستخدام Java.

## المتطلبات الأساسية

قبل الخوض في البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:

- بيئة تطوير Java: تأكد من إعداد بيئة تطوير Java وظيفية على جهازك.

-  مكتبة Aspose.CAD: قم بتنزيل مكتبة Aspose.CAD ودمجها في مشروع Java الخاص بك. يمكنك العثور على المكتبة[هنا](https://releases.aspose.com/cad/java/).

الآن، دعنا ننتقل إلى البرنامج التعليمي ونستكشف الخطوات اللازمة لتسخير دعم القلم أثناء تصدير CAD.

## استيراد مساحات الأسماء

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.PenOptions;
import com.aspose.cad.internal.imaging.LineCap;
```

## الخطوة 1: تحديد دليل المستندات الخاص بك

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

تأكد من استبدال "دليل المستندات الخاص بك" بالمسار الفعلي لمستندات CAD الخاصة بك.

## الخطوة 2: قم بتحميل ملف CAD

```java
String srcFile = dataDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage) Image.load(srcFile);
```

تتضمن هذه الخطوة تحميل ملف CAD، في هذه الحالة، "conic_pyramid.dxf"، باستخدام مكتبة Aspose.CAD.

## الخطوة 3: تكوين خيارات التنقيط

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(cadImage.getWidth() * 100);
rasterizationOptions.setPageHeight(cadImage.getHeight() * 100);
```

اضبط عرض الصفحة وارتفاعها وفقًا لمتطلباتك المحددة. تحدد هذه القيم أبعاد الصورة المصدرة.

## الخطوة 4: تخصيص خيارات القلم

```java
PenOptions penOts = new PenOptions();
penOts.setStartCap(LineCap.Flat);
penOts.setEndCap(LineCap.Flat);
```

قم بتخصيص أغطية البداية والنهاية للأقلام حسب الحاجة. ينطبق هذا التخصيص عند تصدير كائن CadImage إلى تنسيقات صور مختلفة.

## الخطوة 5: تكوين خيارات تصدير PDF

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

حدد خيارات التنقيط المتجه، بما في ذلك خيارات التنقيط التي تم تكوينها مسبقًا.

## الخطوة 6: احفظ ملف PDF الذي تم تصديره

```java
cadImage.save((dataDir + "9LHATT-A56_generated.pdf"), pdfOptions);
```

احفظ ملف PDF الذي تم تصديره باسم الملف المحدد ("9LHATT-A56_generated.pdf" في هذا المثال) والخيارات التي تم تكوينها.

## خاتمة

في الختام، فإن الاستفادة من دعم القلم أثناء تصدير CAD باستخدام Aspose.CAD لـ Java تمكن المستخدمين من تخصيص مظهر الصور المصدرة. باتباع هذا الدليل المفصّل خطوة بخطوة، تعلمت كيفية دمج تخصيص القلم بسلاسة في سير عمل تحويل CAD الخاص بك.

## الأسئلة الشائعة

### س1: هل يمكنني تخصيص خيارات القلم لتنسيقات أخرى غير PDF؟

ج1: نعم، ينطبق تخصيص القلم الموضح في هذا البرنامج التعليمي على تنسيقات الصور المختلفة، بما في ذلك PDF وPNG وBMP وGIF وJPEG2000 وJPEG وPSD وTIFF وWMF.

### س2: كيف يمكنني التعامل مع أغطية البداية والنهاية المختلفة للأقلام؟

 ج2: الاستفادة من`PenOptions` class لتعيين أحرف البداية والنهاية المرغوبة، مما يوفر المرونة في تحديد مظهر الخطوط.

### س3: ماذا لو لم أحدد خيارات القلم؟

ج3: إذا لم يتم تعيين خيارات القلم بشكل صريح، فسيستخدم النظام الأقلام الافتراضية الخاصة به، والتي قد تختلف باختلاف السياقات.

### س4: هل هناك اعتبارات محددة لخيارات التنقيط؟

A4: اضبط عرض الصفحة وارتفاعها في خيارات التنقيط للتحكم في أبعاد الصورة المصدرة.

### س5: أين يمكنني العثور على دعم إضافي أو مناقشات مجتمعية؟

 ج5: استكشف منتدى مجتمع Aspose.CAD على[هنا](https://forum.aspose.com/c/cad/19) للدعم والمناقشات.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
