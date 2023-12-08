---
title: تصدير DGN بسهولة إلى AutoCAD PDF باستخدام Aspose.CAD لـ Java
linktitle: تصدير DGN بتنسيق AutoCAD إلى PDF
second_title: Aspose.CAD جافا API
description: استكشف الدليل التفصيلي خطوة بخطوة حول تصدير ملفات DGN إلى تنسيق AutoCAD في PDF باستخدام Aspose.CAD لـ Java. قم برفع قدرات التعامل مع CAD الخاصة بتطبيق Java الخاص بك دون عناء.
type: docs
weight: 12
url: /ar/java/dgn-export-options/exporting-dgn-to-pdf/
---
## مقدمة

مرحبًا بك في هذا البرنامج التعليمي الشامل حول استخدام Aspose.CAD لـ Java لتصدير ملفات DGN بتنسيق AutoCAD إلى PDF. إذا كنت تتطلع إلى تحسين قدرة تطبيق Java الخاص بك على التعامل مع ملفات CAD، فإن Aspose.CAD يعد خيارًا ممتازًا. سنرشدك في هذا البرنامج التعليمي خلال عملية تصدير ملفات DGN خطوة بخطوة.


## المتطلبات الأساسية
قبل أن نتعمق في البرنامج التعليمي، تأكد من أن لديك المتطلبات الأساسية التالية:
-  مكتبة Aspose.CAD: تأكد من تثبيت مكتبة Aspose.CAD الخاصة بـ Java. يمكنك تنزيله[هنا](https://releases.aspose.com/cad/java/).
- دليل المستندات: قم بإعداد دليل المستندات حيث سيتم تخزين ملفات الإدخال والإخراج الخاصة بك.

## حزم الاستيراد

في مشروع Java الخاص بك، قم باستيراد الحزم اللازمة للوصول إلى وظائف Aspose.CAD:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

الآن، دعونا نقسم رمز المثال إلى خطوات متعددة:

## الخطوة 1: تحديد مسارات الملفات

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

تأكد من استبدال "دليل المستندات الخاص بك" بالمسار الفعلي الذي توجد به ملفاتك.

## الخطوة 2: تحميل صورة DGN

```java
DgnImage objImage = (DgnImage) Image.load(fileName);
```

قم بتحميل ملف DGN باستخدام Aspose.CAD.

## الخطوة 3: ضبط خيارات تصدير PDF

```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); // تصدير طرق عرض محددة
options.setVectorRasterizationOptions(vectorOptions);
```

حدد خيارات تصدير PDF، بما في ذلك أبعاد الصفحة وتفضيلات التخطيط.

## الخطوة 4: حفظ ملف PDF

```java
objImage.save(outFile, options);
```

احفظ ملف PDF الذي تم تصديره.

كرر هذه الخطوات لأي ملفات DGN إضافية تريد تحويلها. تهانينا! لقد نجحت في تصدير ملفات DGN إلى تنسيق AutoCAD بتنسيق PDF باستخدام Aspose.CAD لـ Java.

## خاتمة

في هذا البرنامج التعليمي، اكتشفنا كيفية الاستفادة من Aspose.CAD لـ Java لتحسين إمكانات معالجة ملفات CAD الخاصة بتطبيقك. من خلال الخطوات سهلة المتابعة وأمثلة التعليمات البرمجية، يمكنك الآن تصدير ملفات DGN بسلاسة إلى تنسيق AutoCAD في PDF.

## الأسئلة الشائعة

### س1: هل Aspose.CAD متوافق مع جميع تنسيقات ملفات CAD؟

ج1: نعم، يدعم Aspose.CAD نطاقًا واسعًا من تنسيقات CAD، مما يضمن تعدد الاستخدامات في التعامل مع أنواع الملفات المختلفة.

### س2: هل يمكنني تخصيص إعدادات تصدير PDF؟

ج2: بالتأكيد. كما هو موضح في البرنامج التعليمي، يمكنك ضبط خيارات مثل أبعاد الصفحة وتخطيطاتها لتناسب متطلباتك.

### س3: أين يمكنني العثور على دعم أو مساعدة إضافية؟

 ج3: قم بزيارة[منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19) لدعم المجتمع والمناقشات.

### س4: هل هناك نسخة تجريبية مجانية متاحة؟

 ج4: نعم، يمكنك الوصول إلى النسخة التجريبية المجانية[هنا](https://releases.aspose.com/).

### س5: كيف يمكنني الحصول على ترخيص مؤقت؟

 ج5: الحصول على ترخيص مؤقت[هنا](https://purchase.aspose.com/temporary-license/).