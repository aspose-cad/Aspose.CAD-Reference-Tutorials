---
title: دليل تحويل DGN إلى PDF - Aspose.CAD لـ Java
linktitle: دعم لDGN V7
second_title: Aspose.CAD جافا API
description: قم بتحويل ملفات DGN إلى PDF بسهولة باستخدام Aspose.CAD لـ Java. اتبع دليلنا خطوة بخطوة لتحقيق التكامل السلس وسير العمل الفعال.
weight: 11
url: /ar/java/other-cad-operations/support-for-dgn-v7/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# دليل تحويل DGN إلى PDF - Aspose.CAD لـ Java

## مقدمة

في عالم CAD (التصميم بمساعدة الكمبيوتر) الديناميكي، يعد التحويل الفعال لملفات DGN (التصميم) إلى PDF (تنسيق المستندات المحمولة) متطلبًا بالغ الأهمية. يظهر Aspose.CAD for Java كحل قوي، حيث يوفر تكاملًا سلسًا وقدرات قوية. يهدف هذا الدليل التفصيلي إلى إرشادك خلال عملية تصدير ملفات DGN إلى PDF باستخدام Aspose.CAD لـ Java، مما يضمن سير عمل سلسًا وفعالاً.

## المتطلبات الأساسية

قبل الغوص في البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:
-  Aspose.CAD لمكتبة Java: قم بتنزيل المكتبة وتثبيتها من ملف[صفحة تنزيل Aspose.CAD لـ Java](https://releases.aspose.com/cad/java/).
- بيئة تطوير Java: تأكد من إعداد بيئة تطوير Java على جهازك.

## حزم الاستيراد

ابدأ باستيراد الحزم الضرورية إلى مشروع Java الخاص بك:

## الخطوة 1: استيراد الحزم الضرورية

في مشروع Java الخاص بك، قم باستيراد الحزم المطلوبة لـ Aspose.CAD لـ Java.
```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.cadobjects.DgnImage;
import com.aspose.cad.imageoptions.PdfOptions;
import java.awt.Color;
```

## الخطوة 2: تعيين مسارات الملفات

حدد المسارات لملف DGN للإدخال وملف PDF للإخراج.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

## الخطوة 3: تحميل صورة DGN

قم بتحميل صورة DGN باستخدام مكتبة Aspose.CAD.

```java
DgnImage objImage = (DgnImage)Image.load(fileName);
```

## الخطوة 4: تكوين خيارات تصدير PDF

قم بإعداد خيارات التصدير إلى PDF، بما في ذلك أبعاد الصفحة وقياس التخطيط التلقائي ولون الخلفية والتخطيطات المحددة للتصدير.

```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setBackgroundColor(Color.getBlack());
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); //قم بتصدير 4 مشاهدات فقط (1،2،3 و9).
options.setVectorRasterizationOptions(vectorOptions);
```

## الخطوة 5: حفظ ملف PDF

احفظ صورة DGN كملف PDF بالخيارات المحددة.

```java
objImage.save(outFile, options);
```

كرر هذه الخطوات لملفات DGN المختلفة، واضبط مسارات الملفات وخياراتها حسب الحاجة.

## خاتمة

باستخدام Aspose.CAD لـ Java، يصبح تحويل ملفات DGN إلى PDF عملية مباشرة. يزودك هذا الدليل بالمعرفة اللازمة لدمج المكتبة بسلاسة في مشاريع Java الخاصة بك، مما يسهل تحويلات ملفات CAD الفعالة.

## الأسئلة الشائعة

### س1: هل يمكنني استخدام Aspose.CAD لـ Java مع تنسيقات ملفات CAD الأخرى؟

ج1: نعم، يدعم Aspose.CAD تنسيقات CAD المتنوعة، مما يوفر وظائف متعددة الاستخدامات تتجاوز تحويل DGN إلى PDF.

### س2: هل يتوفر ترخيص مؤقت لـ Aspose.CAD لـ Java؟

 ج2: نعم، يمكنك الحصول على ترخيص مؤقت[هنا](https://purchase.aspose.com/temporary-license/) لأغراض تجريبية.

### س3: كيف يمكنني طلب الدعم أو طرح أسئلة حول Aspose.CAD لـ Java؟

 ج3: قم بزيارة[منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19)للتواصل مع المجتمع وطلب المساعدة.

### س4: ما هي التخطيطات التي يمكنني تصديرها عند تحويل DGN إلى PDF؟

 ج4: يمكنك تحديد التخطيطات المراد تصديرها عن طريق تخصيص ملف`setLayouts` المصفوفة في الكود.

### س5: أين يمكنني العثور على وثائق شاملة لـ Aspose.CAD لـ Java؟

 ج5: راجع[Aspose.CAD لوثائق جافا](https://reference.aspose.com/cad/java/) للحصول على معلومات مفصلة.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
