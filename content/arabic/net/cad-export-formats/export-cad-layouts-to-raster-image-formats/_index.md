---
title: تصدير تخطيطات CAD إلى تنسيقات الصور النقطية في Aspose.CAD لـ .NET
linktitle: تصدير تخطيطات CAD إلى تنسيقات الصور النقطية
second_title: Aspose.CAD .NET - تنسيق ملف CAD وBIM
description: تعرف على كيفية تصدير تخطيطات CAD إلى صور نقطية باستخدام Aspose.CAD لـ .NET. اتبع دليلنا خطوة بخطوة للتحويل السلس.
type: docs
weight: 10
url: /ar/net/cad-export-formats/export-cad-layouts-to-raster-image-formats/
---
## مقدمة

هل تتطلع إلى تحويل تخطيطات CAD بكفاءة إلى تنسيقات صور نقطية باستخدام Aspose.CAD لـ .NET؟ سيرشدك هذا الدليل خطوة بخطوة خلال العملية، ويقدم لك تعليمات مفصلة ومقتطفات من التعليمات البرمجية لتسهيل المهمة. سواء كنت مطورًا متمرسًا أو وافدًا جديدًا إلى Aspose.CAD، فإن هذا البرنامج التعليمي يلبي جميع مستويات الخبرة.

## المتطلبات الأساسية

قبل الغوص في البرنامج التعليمي، تأكد من أن لديك ما يلي:

-  Aspose.CAD لمكتبة .NET: تأكد من تثبيت مكتبة Aspose.CAD. إذا لم يكن الأمر كذلك، يمكنك تنزيله من[موقع Aspose.CAD](https://releases.aspose.com/cad/net/).

- ملف رسم CAD: قم بإعداد ملف رسم CAD (على سبيل المثال، conic_pyramid.dxf) الذي تريد تحويله إلى تنسيقات صور نقطية.

## استيراد مساحات الأسماء

في مشروع .NET الخاص بك، قم باستيراد مساحات الأسماء الضرورية للاستفادة من وظائف Aspose.CAD. قم بتضمين مساحات الأسماء التالية في بداية التعليمات البرمجية الخاصة بك:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## الخطوة 1: تحميل رسم CAD

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

// قم بتحميل رسم CAD في مثيل الصورة
using (var image = Image.Load(sourceFilePath))
{
    //الكود الخاص بك لتحميل رسم CAD موجود هنا
}
```

## الخطوة 2: إنشاء CadRasterizationOptions

```csharp
// قم بإنشاء مثيل لـ CadRasterizationOptions
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
```

## الخطوة 3: تحديد الطبقات

```csharp
// أضف اسم الطبقة إلى قائمة طبقات CadRasterizationOptions
rasterizationOptions.Layers = new string[] { "LayerA" };
```

## الخطوة 4: إنشاء JpegOptions

```csharp
// قم بإنشاء مثيل لـ JpegOptions (أو أي ImageOptions للتنسيقات النقطية)
var options = new JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
```

## الخطوة 5: التصدير إلى تنسيق Jpeg

```csharp
// تصدير كل طبقة إلى تنسيق Jpeg
MyDir = MyDir + "CADLayersToRasterImageFormats_out.jpg";
image.Save(MyDir, options);
```

## خطوة إضافية: تحويل جميع الطبقات

إذا كنت تريد تحويل جميع الطبقات، استخدم الطريقة التالية:

```csharp
ConvertAllLayersToRasterImageFormats();
```

تتكرر هذه الطريقة على جميع الطبقات في رسم CAD، وتصدر كل طبقة إلى ملف Jpeg منفصل.

## خاتمة

تهانينا! لقد تعلمت بنجاح كيفية تصدير تخطيطات CAD إلى تنسيقات الصور النقطية باستخدام Aspose.CAD لـ .NET. يوفر هذا البرنامج التعليمي دليلاً شاملاً للمطورين الذين يبحثون عن حلول فعالة وموثوقة لتحويل CAD.

## الأسئلة الشائعة

### س1: هل يمكنني استخدام تنسيقات صور أخرى للتصدير؟

 ج1: نعم يمكنك ذلك. ببساطة استبدل`JpegOptions` مع خيارات التنسيق المطلوب، مثل`PngOptions` أو`BmpOptions`.

### س2: هل هناك نسخة تجريبية متاحة؟

 ج2: نعم، يمكنك استكشاف وظائف Aspose.CAD عن طريق تنزيل الإصدار التجريبي[هنا](https://releases.aspose.com/).

### س3: كيف يمكنني الحصول على الدعم لـ Aspose.CAD؟

 A3: قم بزيارة Aspose.CAD[المنتدى](https://forum.aspose.com/c/cad/19) للحصول على دعم المجتمع أو فكر في شراء ترخيص للحصول على دعم مخصص.

### س4: هل التراخيص المؤقتة متاحة؟

 ج4: نعم، يمكنك الحصول على ترخيص مؤقت[هنا](https://purchase.aspose.com/temporary-license/).

### س5: أين يمكنني العثور على الوثائق؟

 ج5: ارجع إلى الوثائق التفصيلية[هنا](https://reference.aspose.com/cad/net/).