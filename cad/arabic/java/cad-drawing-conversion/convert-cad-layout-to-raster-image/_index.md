---
title: تحويل تخطيط CAD إلى تنسيق الصورة النقطية باستخدام Aspose.CAD لـ Java
linktitle: تحويل تخطيط CAD إلى تنسيق الصورة النقطية
second_title: Aspose.CAD جافا API
description: قم بتحويل تخطيطات CAD بسهولة إلى صور نقطية باستخدام Aspose.CAD لـ Java. تصور عالي الجودة لتعزيز التعاون.
weight: 12
url: /ar/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تحويل تخطيط CAD إلى تنسيق الصورة النقطية باستخدام Aspose.CAD لـ Java

## مقدمة

في العالم الديناميكي للتصميم بمساعدة الكمبيوتر (CAD)، تعد القدرة على تحويل تخطيطات CAD بسلاسة إلى تنسيقات الصور النقطية مهارة قيمة. يظهر Aspose.CAD for Java كحل قوي لتحقيق هذه المهمة بكفاءة. في هذا البرنامج التعليمي، سنرشدك خلال عملية تحويل تخطيط CAD إلى صورة نقطية خطوة بخطوة، باستخدام Aspose.CAD لـ Java.

## المتطلبات الأساسية

قبل الغوص في البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:

1. بيئة تطوير Java: تأكد من أن لديك بيئة تطوير Java عاملة مثبتة على نظامك.

2.  مكتبة Aspose.CAD: قم بتنزيل وتثبيت مكتبة Aspose.CAD. يمكنك الحصول عليه من[Aspose.CAD لوثائق جافا](https://reference.aspose.com/cad/java/).

## استيراد مساحات الأسماء

ابدأ باستيراد مساحات الأسماء الضرورية للاستفادة من وظائف Aspose.CAD لـ Java. في كود Java الخاص بك، قم بتضمين مساحات الأسماء التالية:

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

الآن، دعونا نقسم رمز المثال إلى سلسلة من الخطوات لتحويل تخطيط CAD إلى صورة نقطية.
## الخطوة 1: إعداد دليل الموارد

```java
// المسار إلى دليل الموارد.
String dataDir = "Your Document Directory" + "CADConversion/";
```

تأكد من استبدال "دليل المستندات الخاص بك" بالمسار إلى دليل المستندات الفعلي.

## الخطوة 2: قم بتحميل ملف CAD

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

حدد المسار إلى ملف CAD الخاص بك، وقم بتحميله باستخدام Aspose.CAD.

## الخطوة 3: تكوين خيارات التنقيط

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
rasterizationOptions.setLayouts(new String[] {"Model", "Layout1"});
```

 إنشاء مثيل ل`CadRasterizationOptions` وتعيين أبعاد الصفحة وتخطيطاتها.

## الخطوة 4: ضبط خيارات الصورة

```java
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.setVectorRasterizationOptions(rasterizationOptions);
```

 إنشاء مثيل ل`ImageOptions` وربطها بخيارات التنقيط.

## الخطوة 5: احفظ الصورة الناتجة

```java
image.save(dataDir + "conic_pyramid_layoutstorasterimage_out_.tiff", options);
```

احفظ الصورة النقطية النهائية بالتنسيق والموقع المطلوبين.

كرر هذه الخطوات، واضبط المعلمات حسب الحاجة، لتخصيص التحويل وفقًا لمتطلباتك المحددة.

## خاتمة

يعمل Aspose.CAD for Java على تبسيط عملية تحويل تخطيطات CAD إلى صور نقطية، مما يوفر المرونة والدقة. إن إتقان هذه التقنية يفتح إمكانيات التصور والتعاون الفعال في مشاريع التصميم بمساعدة الكمبيوتر (CAD).

## الأسئلة الشائعة

### س 1: هل Aspose.CAD متوافق مع تنسيقات ملفات CAD المختلفة؟

ج1: نعم، يدعم Aspose.CAD مجموعة متنوعة من تنسيقات CAD، بما في ذلك DWG وDXF وDGN.

### س2: هل يمكنني تخصيص دقة الصورة النقطية الناتجة؟

 ج2: بالتأكيد. أضبط ال`setPageWidth` و`setPageHeight` المعلمات في`CadRasterizationOptions` للقرار المطلوب.

### س 3: كيف يمكنني تحويل تخطيطات CAD متعددة في وقت واحد؟

 A3: ما عليك سوى توسيع الصفيف الذي تم تمريره إليه`setLayouts` بأسماء التخطيطات التي تريد تحويلها.

### س 4: هل هناك تنسيقات إخراج أخرى مدعومة إلى جانب TIFF؟

ج4: نعم، يدعم Aspose.CAD تنسيقات الإخراج المختلفة، مثل PNG وJPG وPDF.

### س5: أين يمكنني طلب المساعدة أو مشاركة تجاربي مع Aspose.CAD؟

ج5: قم بزيارة[منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19) للتفاعل مع المجتمع والحصول على الدعم.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
