---
title: تصدير DWG إلى PDF أو Raster باستخدام Aspose.CAD لـ Java
linktitle: تصدير DWG إلى PDF أو النقطية
second_title: Aspose.CAD جافا API
description: استكشف العملية السلسة لتصدير ملفات DWG إلى PDF أو الصور النقطية في Java باستخدام Aspose.CAD. يضمن هذا الدليل التفصيلي الدقة والكفاءة.
type: docs
weight: 13
url: /ar/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
---
## مقدمة

في عالم التصميم بمساعدة الكمبيوتر (CAD) الديناميكي، يعد التعامل الفعال مع الرسومات أمرًا بالغ الأهمية. يوفر Aspose.CAD for Java حلاً قويًا لتصدير ملفات DWG إلى PDF أو الصور النقطية. سيرشدك هذا البرنامج التعليمي خلال العملية، مما يضمن لك الاستفادة الكاملة من إمكانات Aspose.CAD لـ Java.

## المتطلبات الأساسية

قبل الغوص في البرنامج التعليمي، تأكد من أن لديك ما يلي:

- الفهم الأساسي لبرمجة جافا.
-  تم تثبيت Aspose.CAD لمكتبة Java. إذا لم يكن الأمر كذلك، قم بتنزيله[هنا](https://releases.aspose.com/cad/java/).
- ملف DWG لأغراض الاختبار. يمكنك استخدام الملف "Bottom_plate.dwg" المتوفر.

## استيراد مساحات الأسماء

في مشروع Java الخاص بك، قم باستيراد مساحات الأسماء اللازمة لبدء العملية:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## الخطوة 1: قم بتحميل ملف DWG

 ابدأ بتحميل ملف DWG الخاص بك باستخدام Aspose.CAD`Image` فصل:

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

## الخطوة الثانية: تحديد نوع الوحدة

بعد ذلك، تحقق من نوع الوحدة لملف DWG الذي تم تحميله:

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

## الخطوة 3: تعيين خيارات التنقيط

بناءً على نوع الوحدة، قم بتكوين خيارات التنقيط:

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();

if (currentUnitIsMetric) {
    // الوحدات المترية
    double metersCoeff = 1 / 1000.0;
    double scaleFactor = metersCoeff / currentUnitCoefficient;
    rasterizationOptions.setPageWidth((float)(210 * scaleFactor));
    rasterizationOptions.setPageHeight((float)(297 * scaleFactor));
    rasterizationOptions.setUnitType(UnitType.Millimeter);
} else {
    // وحدات القياس الملكية
    rasterizationOptions.setPageWidth((float)(8.27f / currentUnitCoefficient));
    rasterizationOptions.setPageHeight((float)(11.69f / currentUnitCoefficient));
    rasterizationOptions.setUnitType(UnitType.Inch);
}
```

## الخطوة 4: تكوين خيارات PDF

إعداد خيارات تصدير PDF:

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

## الخطوة 5: احفظ بصيغة PDF

أخيرًا، احفظ ملف DWG بصيغة PDF:

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

وهناك لديك! لقد نجحت في تصدير ملف DWG إلى PDF باستخدام Aspose.CAD لـ Java.

## خاتمة

قدم هذا البرنامج التعليمي دليلاً خطوة بخطوة حول الاستفادة من Aspose.CAD لـ Java لتصدير ملفات DWG إلى PDF أو الصور النقطية. تعمل هذه المكتبة على تبسيط العملية، مما يسمح لك بالتعامل بكفاءة مع رسومات CAD في تطبيقات Java الخاصة بك.

## الأسئلة الشائعة

### س1: هل يمكنني استخدام Aspose.CAD لـ Java مع أطر عمل Java الأخرى؟

ج1: نعم، يتكامل Aspose.CAD for Java بسلاسة مع أطر عمل Java الشائعة.

### س2: هل يتوفر ترخيص مؤقت لـ Aspose.CAD لـ Java؟

 ج2: نعم، يمكنك الحصول على ترخيص مؤقت[هنا](https://purchase.aspose.com/temporary-license/).

### س3: أين يمكنني العثور على دعم لـ Aspose.CAD لـ Java؟

 ج3: قم بزيارة[منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19) للحصول على المساعدة من المجتمع.

### س4: كيف يمكنني شراء ترخيص Aspose.CAD لـ Java؟

 ج4: يمكنك شراء ترخيص[هنا](https://purchase.aspose.com/buy).

### س5: ما هي الوحدات التي يدعمها Aspose.CAD لـ Java؟

ج5: يدعم Aspose.CAD for Java كلاً من الوحدات المترية والإمبريالية.