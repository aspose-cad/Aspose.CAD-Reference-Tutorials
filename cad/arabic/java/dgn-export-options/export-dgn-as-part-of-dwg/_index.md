---
title: تصدير DGN إلى DWG باستخدام Aspose.CAD لـ Java
linktitle: تصدير DGN كجزء من DWG
second_title: Aspose.CAD جافا API
description: اكتشف كيفية تصدير DGN كجزء من DWG باستخدام Aspose.CAD لـ Java. اتبع دليلنا خطوة بخطوة لمعالجة ملفات CAD بكفاءة.
type: docs
weight: 10
url: /ar/java/dgn-export-options/export-dgn-as-part-of-dwg/
---
## مقدمة

في هذا البرنامج التعليمي، سنستكشف كيفية استخدام Aspose.CAD لـ Java لتصدير ملف DGN (MicroStation Design) كجزء من ملف DWG (رسم AutoCAD). Aspose.CAD هي مكتبة قوية توفر وظائف شاملة للعمل مع تنسيقات ملفات CAD. سيساعدك هذا الدليل التفصيلي خطوة بخطوة على فهم عملية تصدير DGN كجزء من DWG باستخدام Java.

## المتطلبات الأساسية

قبل أن نتعمق في البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:
1. مكتبة Aspose.CAD: قم بتنزيل وتثبيت مكتبة Aspose.CAD لـ Java. يمكنك العثور على المكتبة[هنا](https://releases.aspose.com/cad/java/).
2. Java Development Kit (JDK): تأكد من تثبيت Java على نظامك.
3. بيئة التطوير المتكاملة (IDE): اختر Java IDE مثل Eclipse أو IntelliJ للحصول على تجربة تطوير أكثر سلاسة.

## حزم الاستيراد

في مشروع Java الخاص بك، قم باستيراد حزم Aspose.CAD اللازمة لتمكين معالجة ملف CAD. هنا مثال:

```java
import com.aspose.cad;
import com.aspose.cad.imageoptions;
import com.aspose.cad.fileformats.cad.cadconsts;
import com.aspose.cad.fileformats.cad;
import com.aspose.cad.fileformats.cad.cadobjects;
```

## الخطوة 1: تعيين مسارات الملفات

 تحديد مسارات ملف الإدخال والإخراج لملف DWG. تحديث`dataDir`, `fileName` ، و`outPath` المتغيرات تبعا لذلك.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
String outPath = dataDir + "BlockRefDgn.dwg.pdf";
```

## الخطوة 2: إنشاء مثيل PdfOptions

 إنشاء مثيل لـ`PdfOptions` فئة، حيث نقوم بتصدير ملف DWG إلى تنسيق PDF.

```java
PdfOptions exportOptions = new PdfOptions();
```

## الخطوة 3: تحميل ملف DWG

 قم بتحميل ملف DWG الموجود كصورة وقم بتحويله إلى ملف`CadImage` يكتب.

```java
CadImage cadImage = (CadImage) Image.load(fileName);
```

## الخطوة 4: التكرار من خلال الكيانات

انتقل إلى كل كيان داخل ملف DWG وتحقق مما إذا كان تعريفًا للصورة. إذا كان الأمر كذلك، قم باسترداد المرجع الخارجي للكائن.

```java
for (CadBaseEntity baseEntity : cadImage.getEntities()) {
    if (baseEntity.getTypeName() == CadEntityTypeName.DGNUNDERLAY) {
        CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
        System.out.println(dgnFile.getUnderlayPath());
    }
}
```

## الخطوة 5: تحديد خيارات التنقيط

 تحديد الإعدادات ل`CadRasterizationOptions`الكائن، بما في ذلك عرض الصفحة وارتفاعها وتخطيطاتها ولون الخلفية.

```java
CadRasterizationOptions vectorRasterizationOptions = new CadRasterizationOptions();
vectorRasterizationOptions.setPageWidth(1600);
vectorRasterizationOptions.setPageHeight(1600);
vectorRasterizationOptions.setLayouts(new String[] { "Model" });
vectorRasterizationOptions.setAutomaticLayoutsScaling(false);
vectorRasterizationOptions.setNoScaling(true);
vectorRasterizationOptions.setBackgroundColor(Color.getBlack());
vectorRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
```

## الخطوة 6: تعيين خيارات تنقيط المتجهات

قم بتعيين خيارات التنقيط المتجه للتصدير.

```java
exportOptions.setVectorRasterizationOptions(vectorRasterizationOptions);
```

## الخطوة 7: تصدير DWG إلى PDF

 أخيرًا، قم بتصدير ملف DWG إلى PDF عن طريق الاتصال بـ`save` طريقة.

```java
cadImage.save(outPath, exportOptions);
```

## خاتمة

تهانينا! لقد تعلمت بنجاح كيفية تصدير ملف DGN كجزء من ملف DWG باستخدام Aspose.CAD لـ Java. توفر هذه المكتبة القوية إمكانات واسعة النطاق للعمل مع ملفات CAD، مما يجعل مهام معالجة ملفات CAD فعالة ومباشرة.

## الأسئلة الشائعة

### س1: أين يمكنني العثور على الوثائق الخاصة بـ Aspose.CAD لـ Java؟

 ج1: يمكن العثور على الوثائق[هنا](https://reference.aspose.com/cad/java/).

### س2: كيف يمكنني تنزيل مكتبة Aspose.CAD الخاصة بـ Java؟

 ج2: يمكنك تنزيل المكتبة من[هذا الرابط](https://releases.aspose.com/cad/java/).

### س3: هل تتوفر نسخة تجريبية مجانية من Aspose.CAD لـ Java؟

 ج3: نعم، يمكنك العثور على النسخة التجريبية المجانية[هنا](https://releases.aspose.com/).

### س4: أين يمكنني الحصول على ترخيص مؤقت لـ Aspose.CAD لـ Java؟

 ج4: الحصول على ترخيص مؤقت[هنا](https://purchase.aspose.com/temporary-license/).

### س5: هل تحتاج إلى مساعدة أو لديك أسئلة؟

 ج5: قم بزيارة منتدى دعم مجتمع Aspose.CAD[هنا](https://forum.aspose.com/c/cad/19).