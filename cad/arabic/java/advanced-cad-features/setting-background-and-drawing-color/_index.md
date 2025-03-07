---
title: ضبط الخلفية ولون الرسم باستخدام Aspose.CAD لـ Java
linktitle: ضبط الخلفية ولون الرسم
second_title: Aspose.CAD جافا API
description: قم بتحويل ملفات CAD إلى PDF وTIFF بسهولة باستخدام Aspose.CAD لـ Java. قم بتعيين خلفية مخصصة وألوان رسم للحصول على نتائج مذهلة بصريًا.
weight: 15
url: /ar/java/advanced-cad-features/setting-background-and-drawing-color/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ضبط الخلفية ولون الرسم باستخدام Aspose.CAD لـ Java

## مقدمة

في عالم التصميم بمساعدة الكمبيوتر (CAD) الديناميكي، يعد التحويل الفعال للملفات أمرًا ضروريًا للتعاون والتواصل السلس. يظهر Aspose.CAD for Java كأداة قوية توفر إمكانات قوية لتحويل ملفات CAD إلى تنسيقات PDF وTIFF. في هذا البرنامج التعليمي، سنتعمق في عملية تعيين الخلفية ولون الرسم باستخدام Aspose.CAD لـ Java، مما يوفر لك دليلًا خطوة بخطوة للحصول على أفضل النتائج.

## المتطلبات الأساسية

قبل أن نبدأ هذه الرحلة، تأكد من توفر المتطلبات الأساسية التالية:

-  Aspose.CAD لمكتبة Java: تأكد من تثبيت مكتبة Aspose.CAD لـ Java. يمكنك تنزيله[هنا](https://releases.aspose.com/cad/java/).

-  دليل المستندات: احصل على دليل مخصص لملفات CAD الخاصة بك. يستبدل`"Your Document Directory" + "CADConversion/"` مع المسار إلى الدليل الخاص بك.

الآن، دعونا نتعمق في هذه العملية.

## استيراد مساحات الأسماء

تأكد من استيراد مساحات الأسماء اللازمة للاستفادة من وظائف Aspose.CAD لـ Java. في مثالنا نستخدم ما يلي:

```java
import java.awt.Color;
import java.awt.Image;

import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## الخطوة 1: تحميل ملف CAD

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image objImage = Image.load(srcFile);
```

## الخطوة 2: تعيين الخلفية ولون الرسم

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setBackgroundColor(com.aspose.cad.Color.getBeige());
rasterizationOptions.setDrawType(CadDrawTypeMode.UseDrawColor);
rasterizationOptions.setBackgroundColor(com.aspose.cad.Color.getBlue());
```

## الخطوة 3: إنشاء PDF وحفظه

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

## الخطوة 4: إنشاء TIFF وحفظه

```java
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

اتبع هذه الخطوات بعناية لتحقيق أفضل النتائج في تحويل CAD إلى PDF وTIFF باستخدام Aspose.CAD لـ Java.

## خاتمة

يعمل Aspose.CAD for Java على تمكين المطورين من خلال مجموعة أدوات متعددة الاستخدامات لمعالجة ملفات CAD. من خلال إتقان تعقيدات إعداد الخلفية ولون الرسم، يمكنك تعزيز قدرتك على إنتاج تحويلات دقيقة وجذابة بصريًا.

## الأسئلة الشائعة

### س1: هل Aspose.CAD for Java مناسب للتحويلات المجمعة؟

ج1: بالتأكيد! يتفوق Aspose.CAD for Java في التحويلات المجمعة، مما يوفر الكفاءة والدقة.

### س2: هل يمكنني تخصيص لون الخلفية في الملفات التي تم إنشاؤها؟

ج2: نعم، يوضح البرنامج التعليمي كيفية تعيين ألوان خلفية مخصصة لمخرجات PDF وTIFF.

### س3: أين يمكنني العثور على وثائق شاملة لـ Aspose.CAD لـ Java؟

 ج3: راجع[توثيق](https://reference.aspose.com/cad/java/) للحصول على رؤى وأمثلة متعمقة.

### س4: هل هناك نسخة تجريبية مجانية متاحة؟

 ج4: نعم، اكتشف الميزات باستخدام[تجربة مجانية](https://releases.aspose.com/).

### س5: كيف يمكنني الحصول على دعم Aspose.CAD لـ Java؟

ج5: قم بزيارة[منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19) لطلب المساعدة والتفاعل مع المجتمع.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
