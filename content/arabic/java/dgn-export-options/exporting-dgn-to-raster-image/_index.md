---
title: تحويل Java DGN إلى JPEG باستخدام البرنامج التعليمي Aspose.CAD
linktitle: تصدير DGN بتنسيق AutoCAD إلى تنسيق الصورة النقطية
second_title: Aspose.CAD جافا API
description: تعرف على كيفية تصدير ملفات DGN إلى صور JPEG في Java باستخدام Aspose.CAD. يرشدك هذا البرنامج التعليمي خطوة بخطوة خلال العملية دون عناء.
type: docs
weight: 13
url: /ar/java/dgn-export-options/exporting-dgn-to-raster-image/
---
## مقدمة

مرحبًا بك في هذا البرنامج التعليمي الشامل حول تصدير ملفات DGN (التصميم) إلى تنسيق الصور النقطية باستخدام Aspose.CAD لـ Java. Aspose.CAD هي مكتبة قوية تمكن مطوري Java من العمل مع ملفات CAD بسلاسة. في هذا البرنامج التعليمي، سنرشدك خلال عملية تحويل ملفات DGN إلى صور JPEG، ونزودك بتعليمات خطوة بخطوة وأمثلة التعليمات البرمجية.

## المتطلبات الأساسية

قبل الغوص في البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:
1.  مكتبة Aspose.CAD: تأكد من تثبيت مكتبة Aspose.CAD لـ Java. يمكنك تنزيله[هنا](https://releases.aspose.com/cad/java/).
2. Java Development Kit (JDK): تأكد من تثبيت Java على جهازك.
3. بيئة التطوير المتكاملة (IDE): استخدم بيئة تطوير متكاملة متوافقة مع Java مثل IntelliJ أو Eclipse.

## حزم الاستيراد

في مشروع Java الخاص بك، قم باستيراد الحزم اللازمة لـ Aspose.CAD. أضف الأسطر التالية إلى الكود الخاص بك:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
```

## الخطوة 1: تحميل ملف DGN

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
DgnImage dgnImage = (DgnImage) Image.load(dataDir + "Nikon_D90_Camera.dgn");
```

## الخطوة 2: إنشاء كائن JpegOptions

```java
ImageOptionsBase options = new JpegOptions();
```

## الخطوة 3: تعيين خيارات التنقيط

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(600);
vectorOptions.setPageHeight(400);
vectorOptions.setNoScaling(true);
vectorOptions.setAutomaticLayoutsScaling(false);
options.setVectorRasterizationOptions(vectorOptions);
```

## الخطوة 4: احفظ الصورة المحولة

```java
OutputStream outStream = new FileOutputStream(dataDir + "ExportDGNToRasterImage_Out.jpg");
dgnImage.save(outStream, options);
```

كرر هذه الخطوات لملفات DGN المحددة لديك، واضبط مسارات الملفات وفقًا لذلك.

## خاتمة

تهانينا! لقد تعلمت بنجاح كيفية تصدير ملفات DGN إلى تنسيق الصور النقطية باستخدام Aspose.CAD لـ Java. لقد زودك هذا البرنامج التعليمي بالمعرفة اللازمة لدمج هذه الوظيفة في تطبيقات Java الخاصة بك.

## الأسئلة الشائعة

### س1: هل يمكنني استخدام Aspose.CAD لـ Java مع تنسيقات ملفات CAD الأخرى؟

ج1: نعم، يدعم Aspose.CAD تنسيقات CAD المتنوعة، مما يوفر حلاً متعدد الاستخدامات لمطوري Java.

### س2: هل تتوفر نسخة تجريبية مجانية من Aspose.CAD لـ Java؟

 ج2: نعم، يمكنك الوصول إلى النسخة التجريبية المجانية[هنا](https://releases.aspose.com/).

### س3: أين يمكنني العثور على وثائق Aspose.CAD لـ Java؟

 ج3: راجع الوثائق[هنا](https://reference.aspose.com/cad/java/).

### س4: كيف يمكنني الحصول على دعم Aspose.CAD لـ Java؟

 ج4: قم بزيارة منتدى الدعم[هنا](https://forum.aspose.com/c/cad/19).

### س5: أين يمكنني شراء ترخيص Aspose.CAD لـ Java؟

 ج5: يمكنك شراء ترخيص[هنا](https://purchase.aspose.com/buy).