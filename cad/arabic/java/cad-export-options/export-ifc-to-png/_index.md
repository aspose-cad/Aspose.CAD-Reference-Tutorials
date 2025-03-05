---
title: قم بتصدير IFC إلى PNG باستخدام Aspose.CAD لـ Java
linktitle: تصدير مؤسسة التمويل الدولية إلى PNG
second_title: Aspose.CAD جافا API
description: قم بتحويل IFC إلى PNG بسهولة باستخدام Aspose.CAD لـ Java. اتبع البرنامج التعليمي خطوة بخطوة.
type: docs
weight: 18
url: /ar/java/cad-export-options/export-ifc-to-png/
---
## مقدمة

مرحبًا بك في هذا البرنامج التعليمي خطوة بخطوة حول تصدير IFC (فئات مؤسسة الصناعة) إلى PNG باستخدام Aspose.CAD لـ Java. Aspose.CAD هي مكتبة Java قوية توفر إمكانات واسعة النطاق للعمل مع ملفات CAD، بما في ذلك تنسيق IFC. سنرشدك في هذا البرنامج التعليمي خلال عملية تحويل ملف IFC إلى صورة PNG مع شرح مفصل في كل خطوة.

## المتطلبات الأساسية

قبل أن نبدأ، تأكد من توفر المتطلبات الأساسية التالية:

-  مكتبة Aspose.CAD: قم بتنزيل وتثبيت مكتبة Aspose.CAD لـ Java من[رابط التحميل](https://releases.aspose.com/cad/java/).

- دليل المستندات: قم بإعداد دليل على نظامك حيث يوجد ملف IFC الخاص بك.

## استيراد مساحات الأسماء

في مشروع Java الخاص بك، قم باستيراد مساحات الأسماء الضرورية كما هو موضح أدناه:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## الخطوة 1: قم بتحميل ملف IFC

```java
String dataDir = "Your Document Directory" + "ExportingIFC/";
String fileName = dataDir + "example.ifc";
IfcImage cadImage = (IfcImage)Image.load(fileName);
```

تتضمن هذه الخطوة تحميل ملف IFC باستخدام Aspose.CAD.

## الخطوة 2: تعيين خيارات المتجهات

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

قم بتكوين خيارات المتجهات للتنقيط، مع تحديد عرض الصفحة وارتفاعها.

## الخطوة 3: تعيين خيارات PNG

```java
PngOptions pngOptions = new PngOptions();
pngOptions.setVectorRasterizationOptions(vectorOptions);
```

قم بتعيين خيارات PNG، بما في ذلك خيارات تنقيط المتجهات.

## الخطوة 4: احفظ بصيغة PNG

```java
String outPath = dataDir + "example.png";
cadImage.save(outPath, pngOptions);
```

احفظ الصورة المعالجة بتنسيق PNG.

## خاتمة

تهانينا! لقد نجحت في تحويل ملف IFC إلى PNG باستخدام Aspose.CAD لـ Java. قدم هذا البرنامج التعليمي دليلاً شاملاً، مما يضمن إمكانية دمج هذه الوظيفة بسلاسة في مشاريعك.

## الأسئلة الشائعة

### س 1: هل Aspose.CAD متوافق مع كافة إصدارات ملفات IFC؟

 A1: يدعم Aspose.CAD إصدارات مختلفة من ملفات IFC. الرجوع إلى[توثيق](https://reference.aspose.com/cad/java/) للحصول على تفاصيل التوافق.

### س2: هل يمكنني تخصيص خيارات التنقيط بشكل أكبر؟

 ج2: بالتأكيد! اكتشف ال[توثيق](https://reference.aspose.com/cad/java/) لخيارات التخصيص المتقدمة.

### س3: هل هناك نسخة تجريبية متاحة؟

ج3: نعم، يمكنك الوصول إلى النسخة التجريبية المجانية[هنا](https://releases.aspose.com/).

### س4: كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.CAD؟

 ج4: الحصول على ترخيص مؤقت من[هذا الرابط](https://purchase.aspose.com/temporary-license/).

### س5: أين يمكنني طلب المساعدة أو مناقشة القضايا؟

ج5: قم بزيارة[منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19) لدعم المجتمع.
