---
title: صياغة ملفات PDF الديناميكية باستخدام Aspose.CAD لـ Java
linktitle: ملف PDF واحد بتخطيطات مختلفة
second_title: Aspose.CAD جافا API
description: أنشئ ملفات PDF مذهلة بتخطيطات متنوعة من رسومات CAD باستخدام Aspose.CAD لـ Java. تكامل سهل وميزات قوية لمطوري Java.
type: docs
weight: 16
url: /ar/java/other-cad-operations/single-pdf-different-layouts/
---
## مقدمة

مرحبًا بك في عالم Aspose.CAD لـ Java، وهي مكتبة قوية تمكّن المطورين من التعامل مع رسومات CAD دون عناء. في هذا البرنامج التعليمي، سنتعمق في إنشاء ملفات PDF فردية بتخطيطات مختلفة باستخدام Aspose.CAD لـ Java. سواء كنت مطورًا متمرسًا أو بدأت للتو، سيرشدك هذا الدليل المفصّل خطوة بخطوة خلال العملية.

## المتطلبات الأساسية

قبل أن نبدأ هذه الرحلة، تأكد من توفر المتطلبات الأساسية التالية:
- بيئة Java: تأكد من تثبيت Java على جهازك.
-  مكتبة Aspose.CAD: قم بتنزيل وتثبيت مكتبة Aspose.CAD لـ Java من[رابط التحميل](https://releases.aspose.com/cad/java/).
- دليل المستندات: قم بإعداد دليل لرسومات DWG الخاصة بك.

## حزم الاستيراد

في مشروع Java الخاص بك، قم باستيراد الحزم الضرورية:

```java
import com.aspose.cad.Image;
import com.aspose.cad.SizeF;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.VectorRasterizationOptions;
```

## الخطوة 1: تحميل رسم CAD

 ابدأ بتحميل رسم CAD الخاص بك إلى ملف`CadImage` هدف:

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
CadImage cadImage = (CadImage)Image.load(dataDir + "City skyway map.dwg");
```

## الخطوة 2: تكوين خيارات التنقيط

قم بإعداد خيارات التنقيط لصورة CAD:

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1000);
rasterizationOptions.setPageHeight(1000);
```

## الخطوة 3: تخصيص أحجام صفحة التخطيط

تحديد أحجام مخصصة لعدة تخطيطات داخل رسم CAD:

```java
rasterizationOptions.getLayoutPageSizes().addItem("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.getLayoutPageSizes().addItem("8.5 x 11 Plot", new SizeF(1000, 100));
```

## الخطوة 4: ضبط خيارات PDF

قم بتكوين خيارات PDF، متضمنة إعدادات التنقيط:

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## الخطوة 5: احفظ بصيغة PDF

احفظ صورة CAD التي تمت معالجتها كملف PDF:

```java
cadImage.save(dataDir + "singlePDF_out.pdf", pdfOptions);
```

تهانينا! لقد نجحت في إنشاء ملف PDF واحد بتخطيطات مختلفة باستخدام Aspose.CAD لـ Java.

## خاتمة

في هذا البرنامج التعليمي، اكتشفنا التكامل السلس لـ Aspose.CAD لـ Java لإنشاء ملفات PDF بتخطيطات متنوعة من رسومات CAD. إن مرونة المكتبة وميزاتها القوية تجعلها خيارًا مفضلاً لمهام معالجة CAD.

## الأسئلة الشائعة

### س1: هل يمكنني استخدام Aspose.CAD لـ Java مع مكتبات Java الأخرى؟

ج1: نعم، تم تصميم Aspose.CAD for Java للتكامل بسلاسة مع مكتبات Java الأخرى، مما يوفر وظائف واسعة النطاق.

### س2: هل هناك نسخة تجريبية متاحة؟

 ج2: بالتأكيد! يمكنك الوصول إلى نسخة تجريبية مجانية[هنا](https://releases.aspose.com/).

### س3: أين يمكنني العثور على دعم إضافي؟

 ج3: قم بزيارة[منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19) لدعم المجتمع والمناقشات.

### س4: كيف يمكنني الحصول على ترخيص مؤقت؟

 ج4: يمكنك الحصول على ترخيص مؤقت[هنا](https://purchase.aspose.com/temporary-license/).

### س5: أين يمكنني شراء النسخة الكاملة؟

ج5: قم بشراء الإصدار الكامل من Aspose.CAD لـ Java[هنا](https://purchase.aspose.com/buy).