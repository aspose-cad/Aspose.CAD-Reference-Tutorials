---
title: تصدير تخطيطات CAD إلى PDF باستخدام Aspose.CAD لـ Java
linktitle: تصدير تخطيطات CAD إلى PDF
second_title: Aspose.CAD جافا API
description: استكشف Aspose.CAD لـ Java لتصدير تخطيطات CAD إلى PDF بسهولة. فعالة وموثوقة وصديقة للمطورين.
type: docs
weight: 11
url: /ar/java/cad-export-options/export-cad-layouts-to-pdf/
---
## مقدمة

في مجال التصميم بمساعدة الكمبيوتر (CAD) الذي يتطور باستمرار، يبرز Aspose.CAD for Java كأداة قوية لمعالجة ملفات CAD وتحويلها. في هذا البرنامج التعليمي، سنرشدك خلال عملية تصدير تخطيطات CAD إلى PDF باستخدام Aspose.CAD لـ Java. سواء كنت مطورًا متمرسًا أو مجرد غوص في عالم التصميم بمساعدة الكمبيوتر (CAD)، سيساعدك هذا الدليل التفصيلي خطوة بخطوة على الاستفادة من الإمكانات الكاملة لمكتبة Java متعددة الاستخدامات هذه.

## المتطلبات الأساسية

قبل أن نتعمق في البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:

-  Aspose.CAD لـ Java: تأكد من تثبيت المكتبة. يمكنك تنزيله من موقع Aspose[هنا](https://releases.aspose.com/cad/java/).

- بيئة تطوير Java: تأكد من إعداد بيئة تطوير Java على جهازك.

الآن بعد أن قمت بإعداد كل شيء، فلنبدأ بالبرنامج التعليمي.

## استيراد مساحات الأسماء

في كود Java الخاص بك، ابدأ باستيراد مساحات الأسماء الضرورية. توفر هذه الواردات إمكانية الوصول إلى الفئات والأساليب اللازمة للعمل مع Aspose.CAD لـ Java.

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterpolationMode;
import com.aspose.cad.SmoothingMode;
import com.aspose.cad.TextRenderingHint;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

## الخطوة 1: قم بتحميل ملف CAD

 ابدأ بتحميل ملف CAD في تطبيق Java الخاص بك باستخدام ملف`Image.load` طريقة. يستبدل`"conic_pyramid.dxf"` مع المسار إلى ملف CAD الخاص بك.

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

## الخطوة 2: تعيين خيارات التنقيط

 إنشاء مثيل ل`CadRasterizationOptions` لتحديد كيفية تنقيط كيانات CAD. اضبط المعلمات مثل عرض الصفحة وارتفاع الصفحة وقياس التخطيط وفقًا لمتطلباتك.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(false);
rasterizationOptions.setContentAsBitmap(true);
rasterizationOptions.setLayouts(new String[]{"Model"});
```

## الخطوة 3: ضبط خيارات PDF

 إنشاء مثيل ل`PdfOptions` وربطها بخيارات التنقيط. بالإضافة إلى ذلك، قم بتعيين خيارات الرسومات لتصدير PDF، مثل وضع التجانس وتلميح عرض النص ووضع الاستيفاء.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.getGraphicsOptions().setSmoothingMode(SmoothingMode.HighQuality);
rasterizationOptions.getGraphicsOptions().setTextRenderingHint(TextRenderingHint.AntiAliasGridFit);
rasterizationOptions.getGraphicsOptions().setInterpolationMode(InterpolationMode.HighQualityBicubic);
```

## الخطوة 4: التصدير إلى PDF

 وأخيرًا، قم بتصدير تخطيطات CAD إلى ملف PDF باستخدام ملف`save` طريقة`cadImage` هدف.

```java
cadImage.save(dataDir + "CADLayoutsToPDF_out_.pdf", pdfOptions);
```

تهانينا! لقد نجحت في تصدير تخطيطات CAD إلى PDF باستخدام Aspose.CAD لـ Java. لا تتردد في استكشاف الميزات والوظائف الإضافية التي يقدمها Aspose.CAD لتحسين تجربة معالجة ملفات CAD الخاصة بك.

## خاتمة

في هذا البرنامج التعليمي، تناولنا عملية تصدير تخطيطات CAD إلى PDF باستخدام Aspose.CAD لـ Java. بفضل ميزاته القوية وواجهة برمجة التطبيقات (API) سهلة الاستخدام، يعمل Aspose.CAD على تمكين المطورين من العمل بكفاءة مع ملفات CAD في تطبيقات Java الخاصة بهم.

## الأسئلة الشائعة

### س1: هل يمكنني استخدام Aspose.CAD لـ Java مع تنسيقات ملفات CAD الأخرى؟

 ج1: نعم، يدعم Aspose.CAD تنسيقات CAD المتنوعة، بما في ذلك DWG وDXF وDWF والمزيد. تحقق من الوثائق[هنا](https://reference.aspose.com/cad/java/) للحصول على قائمة كاملة.

### س2: هل تتوفر نسخة تجريبية مجانية من Aspose.CAD لـ Java؟

 ج2: نعم، يمكنك استكشاف ميزات Aspose.CAD من خلال النسخة التجريبية المجانية[هنا](https://releases.aspose.com/).

### س3: كيف يمكنني الحصول على دعم Aspose.CAD لـ Java؟

 ج3: قم بزيارة منتدى Aspose.CAD[هنا](https://forum.aspose.com/c/cad/19) لدعم المجتمع. للحصول على دعم متميز، فكر في شراء ترخيص[هنا](https://purchase.aspose.com/buy).

### س4: ما الفرق بين تحجيم التخطيط التلقائي واليدوي؟

A4: يقوم تغيير حجم التخطيط التلقائي بضبط حجم التخطيط استنادًا إلى أبعاد الصفحة المحددة، بينما يسمح لك تغيير الحجم اليدوي بتعيين قيم تغيير الحجم المخصصة.

### س5: هل يمكنني تخصيص مظهر ملفات PDF المصدرة؟

ج5: نعم، يمكنك تخصيص خيارات الرسومات في التعليمات البرمجية للتحكم في جودة ومظهر ملف PDF المُصدَّر.