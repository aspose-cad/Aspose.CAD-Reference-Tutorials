---
title: وجهة نظر مجانية في رسومات CAD - دليل Aspose.CAD
linktitle: وجهة نظر مجانية في رسومات CAD
second_title: Aspose.CAD .NET - تنسيق ملف CAD وBIM
description: اكتشف حرية تصور التصميم بمساعدة الكمبيوتر (CAD) باستخدام Aspose.CAD لـ .NET. اتبع دليلنا خطوة بخطوة للحصول على وجهة نظر فريدة من نوعها.
type: docs
weight: 11
url: /ar/net/advanced-cad-techniques/free-point-of-view-in-cad-drawings/
---
في عالم التصميم بمساعدة الكمبيوتر (CAD)، يعد الحصول على وجهة نظر حرة في الرسومات جانبًا مهمًا لتصور وتقديم التصميمات المعقدة. يوفر Aspose.CAD for .NET حلاً قويًا لتحقيق هذه الحرية، مما يسمح للمستخدمين بمعالجة رسومات CAD وتحسينها بسهولة. في هذا الدليل التفصيلي، سنستكشف عملية الحصول على وجهة نظر مجانية في رسومات CAD باستخدام Aspose.CAD لـ .NET.

## المتطلبات الأساسية

قبل الغوص في البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:

1. تركيب Aspose.CAD
 تأكد من تثبيت Aspose.CAD for .NET في بيئة التطوير لديك. إذا لم يكن الأمر كذلك، يمكنك تنزيله من[موقع Aspose.CAD](https://releases.aspose.com/cad/net/).

2. ملف رسم CAD
قم بإعداد ملف رسم CAD الذي تريد معالجته. في هذا الدليل، سنستخدم ملفًا نموذجيًا باسم "conic_pyramid.dxf."

3. بيئة التطوير
تمتع بإعداد بيئة تطوير .NET عاملة باستخدام Visual Studio أو أي بيئة تطوير متكاملة (IDE) مفضلة.

## استيراد مساحات الأسماء

في مشروع .NET الخاص بك، قم باستيراد مساحات الأسماء الضرورية لوظيفة Aspose.CAD. أضف مقتطف الكود التالي إلى أعلى ملفك:

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
```


## الخطوة 1: تحديد دليل المستندات

```csharp
// المسار إلى دليل المستندات.
string MyDir = "Your Document Directory";
```

تأكد من استبدال "دليل المستندات الخاص بك" بالمسار الفعلي لدليل المستندات الخاص بك.

## الخطوة 2: تحديد الملف المصدر

```csharp
string sourceFilePath = MyDir + "conic_pyramid.dxf";
```

قم بتوفير المسار إلى ملف رسم CAD الخاص بك.

## الخطوة 3: تعيين مسار الإخراج

```csharp
var outPath = Path.Combine(MyDir, "FreePointOfView_out.jpg");
```

حدد المسار الذي سيتم فيه حفظ رسم CAD الذي تم التلاعب به.

## الخطوة 4: تحميل صورة CAD

```csharp
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
```

قم بتحميل رسم CAD باستخدام Aspose.CAD.

## الخطوة 5: تكوين خيارات JPEG

```csharp
JpegOptions options = new JpegOptions
{
    VectorRasterizationOptions = new CadRasterizationOptions
    {
        PageWidth = 1500, PageHeight = 1500
    }
};
```

قم بتكوين الخيارات لتصدير رسم CAD إلى تنسيق JPEG.

## الخطوة 6: ضبط زوايا الدوران

```csharp
float xAngle = 10; //زاوية الدوران على طول المحور X
float yAngle = 30; //زاوية الدوران على طول المحور Y
float zAngle = 40; //زاوية الدوران على طول المحور Z
((CadRasterizationOptions)(options.VectorRasterizationOptions)).ObserverPoint = new ObserverPoint(xAngle, yAngle, zAngle);
```

حدد زوايا الدوران على طول المحاور X وY وZ لتحقيق نقطة الرؤية المطلوبة.

## الخطوة 7: احفظ رسم CAD الذي تم التلاعب به

```csharp
cadImage.Save(outPath, options);
}
```

احفظ رسم CAD الذي تم معالجته في مسار الإخراج المحدد.

## الخطوة 8: عرض رسالة النجاح

```csharp
Console.WriteLine("\n3D images exported successfully to JPEG.\nFile saved at " + outPath);
```

أبلغ المستخدم بنجاح تصدير الصورة ثلاثية الأبعاد.

## خاتمة

في هذا البرنامج التعليمي، اكتشفنا عملية الحصول على وجهة نظر مجانية في رسومات CAD باستخدام Aspose.CAD لـ .NET. باتباع هذه التعليمات خطوة بخطوة، يمكنك تحسين قدرات تصور التصميم بمساعدة الكمبيوتر لديك وتقديم تصميماتك بمنظور جديد.


## الأسئلة الشائعة

### س1: هل يمكنني استخدام Aspose.CAD لـ .NET مع تنسيقات ملفات CAD الأخرى؟

ج1: نعم، يدعم Aspose.CAD for .NET تنسيقات ملفات CAD المتنوعة، بما في ذلك DWG وDXF.

### س2: هل تتوفر نسخة تجريبية من Aspose.CAD؟

 ج2: نعم، يمكنك تنزيل نسخة تجريبية مجانية من[هنا](https://releases.aspose.com/).

### س3: كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.CAD؟

 ج3: يمكنك الحصول على ترخيص مؤقت من[هنا](https://purchase.aspose.com/temporary-license/).

### س4: أين يمكنني العثور على دعم إضافي لـ Aspose.CAD؟

 ج4: قم بزيارة[منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19) لدعم المجتمع والمناقشات.

### س5: هل يمكنني تخصيص خيارات التصدير لتنسيقات صور مختلفة؟

ج5: بالتأكيد! يوفر Aspose.CAD مجموعة من خيارات التخصيص، مما يسمح لك بتخصيص عملية التصدير وفقًا لمتطلباتك المحددة.