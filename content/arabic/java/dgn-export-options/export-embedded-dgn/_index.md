---
title: قم بتصدير DGN المضمن إلى PDF باستخدام Aspose.CAD لـ Java
linktitle: تصدير DGN المضمنة
second_title: Aspose.CAD جافا API
description: استكشف الدليل التفصيلي خطوة بخطوة حول تصدير ملفات DGN المضمنة إلى PDF باستخدام Aspose.CAD لـ Java. قم بتحسين تطبيقات Java الخاصة بك من خلال معالجة ملفات CAD بسلاسة.
type: docs
weight: 11
url: /ar/java/dgn-export-options/export-embedded-dgn/
---
## مقدمة

مرحبًا بك في هذا البرنامج التعليمي الشامل حول تصدير ملفات DGN المضمنة باستخدام Aspose.CAD لـ Java. Aspose.CAD هي مكتبة قوية تمكن مطوري Java من العمل مع ملفات CAD بسلاسة. في هذا البرنامج التعليمي، سنرشدك خلال عملية تصدير ملفات DGN المضمنة إلى PDF باستخدام تعليمات خطوة بخطوة. سواء كنت مطورًا متمرسًا أو بدأت للتو، سيساعدك هذا البرنامج التعليمي على الاستفادة من إمكانيات Aspose.CAD لتحسين تطبيقات Java الخاصة بك.

## المتطلبات الأساسية

قبل أن نتعمق في البرنامج التعليمي، تأكد من أن لديك المتطلبات الأساسية التالية:
- بيئة تطوير Java: تأكد من إعداد بيئة تطوير Java على جهازك.
-  Aspose.CAD لـ Java: قم بتنزيل وتثبيت مكتبة Aspose.CAD لـ Java من[هنا](https://releases.aspose.com/cad/java/).

## حزم الاستيراد

للبدء، تحتاج إلى استيراد الحزم الضرورية في مشروع Java الخاص بك. أضف عبارات الاستيراد التالية إلى التعليمات البرمجية الخاصة بك:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

الآن، دعونا نقسم رمز المثال إلى خطوات متعددة:

## الخطوة 1: إعداد مسارات الإدخال والإخراج

حدد مسار الدليل حيث يوجد المستند الخاص بك وحدد اسم ملف DWG للإدخال.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
```

## الخطوة 2: تحميل ملف DWG

 قم بتحميل ملف DWG إلى ملف`Image` كائن باستخدام Aspose.CAD.

```java
Image objImage = Image.load(fileName);
```

## الخطوة 3: تكوين خيارات التنقيط

قم بتكوين خيارات التنقيط، مثل التخطيطات التي سيتم تضمينها في التصدير.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setLayouts(new String[] {"Model"});
```

## الخطوة 4: تكوين خيارات PDF

قم بإعداد خيارات PDF، بما في ذلك خيارات التنقيط المتجه.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## الخطوة 5: حفظ ملف PDF

احفظ ملف PDF بالخيارات التي تم تكوينها.
```java
objImage.save(dataDir + "BlockRefDgn.pdf", pdfOptions);
```

## خاتمة

تهانينا! لقد نجحت في تصدير ملف DGN مضمن إلى PDF باستخدام Aspose.CAD لـ Java. يغطي هذا البرنامج التعليمي الخطوات الأساسية لدمج Aspose.CAD في تطبيق Java لديك لمعالجة ملفات CAD بكفاءة.

## الأسئلة الشائعة

### س1: هل يمكنني استخدام Aspose.CAD لـ Java في مشروع تجاري؟

 A1: نعم، Aspose.CAD for Java هي مكتبة تجارية. يمكنك الحصول على ترخيص من[هنا](https://purchase.aspose.com/buy).

### س2: هل هناك نسخة تجريبية مجانية متاحة؟

 ج2: نعم، يمكنك الوصول إلى النسخة التجريبية المجانية من Aspose.CAD لـ Java[هنا](https://releases.aspose.com/).

### س3: كيف يمكنني الحصول على دعم Aspose.CAD لـ Java؟

ج3: يمكنك طلب الدعم من مجتمع Aspose.CAD على[المنتدى](https://forum.aspose.com/c/cad/19).

### س4: ماذا لو كنت بحاجة إلى ترخيص مؤقت؟

 ج4: يمكنك الحصول على ترخيص مؤقت[هنا](https://purchase.aspose.com/temporary-license/).

### س5: أين يمكنني العثور على الوثائق؟

 ج5: الوثائق متاحة[هنا](https://reference.aspose.com/cad/java/).