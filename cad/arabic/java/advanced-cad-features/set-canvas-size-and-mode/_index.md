---
title: ضبط حجم القماش ووضعه
linktitle: ضبط حجم القماش ووضعه
second_title: Aspose.CAD جافا API
description: اكتشف قوة Aspose.CAD لـ Java من خلال دليلنا المفصّل خطوة بخطوة حول تعيين حجم اللوحة القماشية ووضعها. قم بتحويل ملفات CAD إلى تنسيقات PDF وTIFF بسهولة.
weight: 16
url: /ar/java/advanced-cad-features/set-canvas-size-and-mode/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ضبط حجم القماش ووضعه

## مقدمة

هل تتطلع إلى تسخير قوة Aspose.CAD لـ Java لتحسين عملية تحويل CAD لديك؟ سيرشدك هذا الدليل الشامل عبر خطوات تحديد حجم اللوحة القماشية ووضعها باستخدام Aspose.CAD لـ Java. سواء كنت مطورًا متمرسًا أو بدأت للتو، سيزودك هذا البرنامج التعليمي بالرؤى التي تحتاجها.

## المتطلبات الأساسية

قبل الغوص في البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:

-  Aspose.CAD لـ Java: تأكد من تثبيت مكتبة Aspose.CAD في بيئة Java لديك. يمكنك تنزيله[هنا](https://releases.aspose.com/cad/java/).

- دليل المستندات: قم بإعداد دليل المستندات لتخزين ملفات CAD الخاصة بك. سيتم الرجوع إلى هذا الدليل في خطوات البرنامج التعليمي.

الآن، دعونا نبدأ مع الدليل خطوة بخطوة.

## استيراد مساحات الأسماء

في هذه الخطوة، سنقوم باستيراد مساحات الأسماء اللازمة لبدء مشروع Aspose.CAD الخاص بك.
```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## الخطوة 1: استيراد فئات Aspose.CAD

```java
// المسار إلى دليل الموارد.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

 في هذا المقتطف، قمنا بإعداد المسار إلى دليل الموارد وتحميل ملف DXF باستخدام ملف Aspose.CAD`Image` فصل.

## الخطوة 2: قم بتعيين خصائص CadRasterizationOptions

```java
// قم بإنشاء مثيل لـ CadRasterizationOptions وقم بتعيين خصائصه المتنوعة
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

 هنا، نقوم بإنشاء مثيل`CadRasterizationOptions` وتكوين خصائص مثل عرض الصفحة وارتفاع الصفحة وخيارات القياس.

## الخطوة 3: إنشاء PdfOptions وتعيين VectorRasterizationOptions

```java
// قم بإنشاء مثيل لـ PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// قم بتعيين الخاصية VectorRasterizationOptions
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

 الآن نقوم بإنشاء ملف`PdfOptions` المثال وتعيينه`VectorRasterizationOptions` الخاصية إلى التكوين السابق`CadRasterizationOptions`.

## الخطوة 4: التصدير إلى PDF

```java
// تصدير CAD إلى PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

وأخيرًا، نقوم بحفظ صورة CAD في ملف PDF باستخدام الخيارات المحددة.

## الخطوة 5: إنشاء TiffOptions وتعيين VectorRasterizationOptions

```java
// قم بإنشاء مثيل لـ TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// قم بتعيين الخاصية VectorRasterizationOptions
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

في هذه الخطوة قمنا بإعداد`TiffOptions` المثيل وتكوينه`VectorRasterizationOptions` ملكية.

## الخطوة 6: التصدير إلى TIFF

```java
// تصدير CAD إلى TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

وأخيرًا، نقوم بحفظ صورة CAD في ملف TIFF باستخدام الخيارات المحددة.

## خاتمة

 تهانينا! لقد قمت بنجاح بتعيين حجم اللوحة القماشية ووضعها باستخدام Aspose.CAD لـ Java. يوفر هذا البرنامج التعليمي أساسًا متينًا لمشاريع تحويل CAD الخاصة بك. اكتشف المزيد من الميزات والإمكانيات في[وثائق Aspose.CAD](https://reference.aspose.com/cad/java/).

## الأسئلة الشائعة

### س1: هل يمكنني استخدام Aspose.CAD لـ Java مع أطر عمل Java الأخرى؟

ج1: نعم، تم تصميم Aspose.CAD للتكامل بسلاسة مع أطر عمل Java المتنوعة.

### س2: هل يتوفر ترخيص مؤقت لـ Aspose.CAD؟

 ج2: نعم، يمكنك الحصول على ترخيص مؤقت[هنا](https://purchase.aspose.com/temporary-license/).

### س3: أين يمكنني الحصول على دعم المجتمع لـ Aspose.CAD؟

 ج3: قم بزيارة[منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19) لدعم المجتمع والمناقشات.

### س4: هل يمكنني تجربة Aspose.CAD مجانًا؟

 ج4: بالتأكيد! الحصول على نسخة تجريبية مجانية[هنا](https://releases.aspose.com/).

### س5: كيف يمكنني شراء Aspose.CAD لـ Java؟

 ج5: شراء المنتج[هنا](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
