---
title: إضافة علامات مائية إلى رسومات CAD - البرنامج التعليمي Aspose.CAD لـ Java
linktitle: أضف علامة مائية
second_title: Aspose.CAD جافا API
description: قم بتحسين رسومات CAD الخاصة بك باستخدام علامات مائية مخصصة باستخدام Aspose.CAD لـ Java. اتبع دليلنا خطوة بخطوة للتكامل السلس.
type: docs
weight: 12
url: /ar/java/other-cad-operations/add-watermark/
---
## مقدمة

مرحبًا بك في هذا الدليل الشامل حول إضافة علامات مائية إلى رسومات CAD باستخدام Aspose.CAD لـ Java. في هذا البرنامج التعليمي، ستتعلم كيفية دمج العلامات المائية بكفاءة، وتعزيز مستندات CAD الخاصة بك برسائل مخصصة أو علامات تجارية. يوفر Aspose.CAD for Java مجموعة قوية من الميزات، مما يجعل عملية إضافة العلامة المائية واضحة ومباشرة.

## المتطلبات الأساسية

قبل أن نتعمق في البرنامج التعليمي، تأكد من أن لديك المتطلبات الأساسية التالية:

-  Aspose.CAD لـ Java: تأكد من تثبيت مكتبة Aspose.CAD في بيئة Java لديك. يمكنك تنزيله[هنا](https://releases.aspose.com/cad/java/).
- Java Development Kit (JDK): تأكد من تثبيت أحدث إصدار من JDK على نظامك.

## حزم الاستيراد

في مشروع Java الخاص بك، قم باستيراد حزم Aspose.CAD اللازمة للبدء:

```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.Cad3DPoint;
import com.aspose.cad.fileformats.cad.cadobjects.CadMText;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## الخطوة 1: إضافة ملف MTEXT جديد

```java
//إضافة MTEXT جديد
CadMText watermark = new CadMText();
watermark.setText("Watermark message");
watermark.setInitialTextHeight(40);
watermark.setInsertionPoint(new Cad3DPoint(300, 40));
watermark.setLayerName("0");
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(watermark);
```

## الخطوة 2: إضافة كيان بسيط مثل النص

يمكنك أيضًا إضافة كيان أكثر وضوحًا مثل النص:

```java
// أو أضف كيانًا أكثر بساطة مثل Text
CadText text = new CadText();
text.setDefaultValue("Watermark text");
text.setTextHeight(40);
text.setFirstAlignment(new Cad3DPoint(300, 40));
text.setLayerName("0") ;
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(text);
```

## الخطوة 3: التصدير إلى PDF

تصدير رسم CAD مع العلامة المائية المضافة إلى ملف PDF:

```java
// تصدير إلى قوات الدفاع الشعبي
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setLayouts(new String[]{"Model"});
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
cadImage.save(dataDir + "AddWatermark_out.pdf", pdfOptions);

```

## خاتمة

تهانينا! لقد نجحت في إضافة علامات مائية إلى رسومات CAD الخاصة بك باستخدام Aspose.CAD لـ Java. تسمح لك هذه العملية البسيطة والقوية بتخصيص تصميماتك أو حمايتها بالعلامة التجارية.

## الأسئلة الشائعة

### س1: هل Aspose.CAD متوافق مع جميع تنسيقات ملفات CAD؟

A1: يدعم Aspose.CAD تنسيقات CAD المتنوعة، بما في ذلك DWG وDXF وDWT وDWF.

### س2: هل يمكنني تخصيص مظهر نص العلامة المائية؟

ج2: نعم، لديك التحكم الكامل في مظهر العلامة المائية، بما في ذلك حجم النص ولونه وموضعه.

### س3: هل هناك إصدار تجريبي متاح لـ Aspose.CAD لـ Java؟

 ج3: نعم، يمكنك تنزيل النسخة التجريبية[هنا](https://releases.aspose.com/).

### س4: كيف يمكنني الحصول على الدعم لـ Aspose.CAD؟

 ج4: قم بزيارة[منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19) لدعم المجتمع.

### س5: أين يمكنني العثور على الوثائق الكاملة لـ Aspose.CAD لـ Java؟

 ج5: راجع[توثيق](https://reference.aspose.com/cad/java/) للحصول على معلومات مفصلة.