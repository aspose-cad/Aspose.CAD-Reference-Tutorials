---
title: دعم DGN V7 في Aspose.CAD لـ .NET
linktitle: دعم لDGN V7
second_title: Aspose.CAD .NET - تنسيق ملف CAD وBIM
description: استكشف Aspose.CAD للحصول على دعم .NET السلس لـ DGN V7. قم بتحويل ملفات DGN إلى صور نقطية بسهولة من خلال إرشادات خطوة بخطوة.
type: docs
weight: 19
url: /ar/net/cad-features-and-support/support-for-dgn-v7/
---
## مقدمة

في مجال تطوير .NET، يبرز Aspose.CAD كمكتبة قوية للتعامل مع ملفات التصميم بمساعدة الكمبيوتر (CAD). يتطرق هذا البرنامج التعليمي إلى ميزة معينة في Aspose.CAD لـ .NET، وهي دعم ملفات DGN V7. DGN، وهو اختصار لـ Design، هو تنسيق ملف مستخدم على نطاق واسع في مجال CAD. يعمل Aspose.CAD على تبسيط عملية العمل مع ملفات DGN V7، مما يوفر للمطورين تجربة سلسة.

## المتطلبات الأساسية

قبل أن نتعمق في التنفيذ، تأكد من توفر المتطلبات الأساسية التالية:

-  Aspose.CAD لـ .NET: تأكد من تثبيت مكتبة Aspose.CAD. يمكنك تنزيله من[موقع إلكتروني](https://releases.aspose.com/cad/net/).

- بيئة التطوير: قم بإعداد بيئة تطوير .NET عاملة، بما في ذلك Visual Studio أو أي بيئة تطوير متكاملة مفضلة أخرى.

الآن بعد أن قمنا بفرز المتطلبات الأساسية، دعنا نستكشف كيفية الاستفادة من دعم DGN V7 في Aspose.CAD لـ .NET.

## استيراد مساحات الأسماء

ابدأ باستيراد مساحات الأسماء الضرورية للوصول إلى وظائف Aspose.CAD:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## الخطوة 1: تحميل ملف DGN

 ابدأ بتحميل ملف DGN موجود كملف`CadImage` يستبدل`"Your Document Directory"` و`"Nikon_D90_Camera.dgn"` مع مسار الدليل المناسب واسم الملف.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // رمز لمزيد من الخطوات يذهب هنا...
}
```

## الخطوة 2: تكوين خيارات التنقيط

 إنشاء`CadRasterizationOptions` كائن لتحديد وتعيين الخصائص المختلفة المتعلقة بالتنقيط.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions
{
    PageWidth = 600,
    PageHeight = 300,
    NoScaling = true,
    AutomaticLayoutsScaling = false
};
```

## الخطوة 3: قم بتعيين خيارات تنقيط المتجهات

 إنشاء`JpegOptions` كائن كما نعتزم تحويل ملف DGN إلى JPEG. تعيين الذي تم إنشاؤه مسبقا`CadRasterizationOptions` يعترض عليه.

```csharp
ImageOptionsBase options = new JpegOptions
{
    VectorRasterizationOptions = rasterizationOptions
};
```

## الخطوة 4: احفظ الصورة النقطية

 اتصل ب`Save` طريقة`CadImage` كائن فئة لتصدير ملف DGN إلى صورة نقطية، في هذه الحالة، JPEG.

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpeg", options);
```

بعد إكمال هذه الخطوات، يتم تصدير ملف DGN بنجاح إلى صورة نقطية.

## خاتمة

في هذا البرنامج التعليمي، اكتشفنا الدعم السلس لـ DGN V7 في Aspose.CAD لـ .NET. باتباع الدليل الموضح خطوة بخطوة، يمكن للمطورين تحويل ملفات DGN إلى صور نقطية بسهولة، مما يؤدي إلى توسيع قدرات تطبيقات .NET الخاصة بهم.

## الأسئلة الشائعة

### س1: هل Aspose.CAD متوافق مع أحدث مواصفات DGN V7؟

ج1: نعم، تم تصميم Aspose.CAD للتعامل مع ملفات DGN V7 بسلاسة، مما يضمن التوافق مع أحدث المواصفات.

### س2: هل يمكنني تخصيص خيارات التنقيط لتحويل ملف DGN؟

 ج2: بالتأكيد. يوضح البرنامج التعليمي كيفية الإنشاء والتكوين`CadRasterizationOptions` لتخصيص عملية التحويل.

### س3: هل هناك تنسيقات إخراج مدعومة أخرى إلى جانب JPEG؟

A3: نعم، يدعم Aspose.CAD تنسيقات الإخراج المختلفة. يمكنك استكشاف الوثائق للحصول على قائمة شاملة.

### س4: كيف يمكنني الحصول على الدعم للاستعلامات المتعلقة بـ Aspose.CAD؟

 ج4: قم بزيارة[منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19) لدعم المجتمع والمناقشات.

### س5: هل تتوفر نسخة تجريبية مجانية من Aspose.CAD لـ .NET؟

 ج5: نعم، يمكنك الوصول إلى النسخة التجريبية المجانية[هنا](https://releases.aspose.com/).