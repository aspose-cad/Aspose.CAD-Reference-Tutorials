---
title: استكشاف العلامات الأساسية لملفات DWG - البرنامج التعليمي Aspose.CAD
linktitle: استكشاف العلامات الأساسية لملفات DWG
second_title: Aspose.CAD .NET - تنسيق ملف CAD وBIM
description: أطلق العنان لقوة Aspose.CAD لـ .NET في استكشاف العلامات الأساسية لملف DWG. اتبع دليلنا خطوة بخطوة.
weight: 13
url: /ar/net/dwg-file-manipulation/exploring-underlay-flags-of-dwg/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# استكشاف العلامات الأساسية لملفات DWG - البرنامج التعليمي Aspose.CAD

## مقدمة

إذا كنت تتعمق في العالم المعقد لملفات CAD، وتحديدًا ملفات DWG، وتريد كشف أسرار العلامات الأساسية، فأنت في المكان الصحيح. سيرشدك هذا البرنامج التعليمي خلال عملية استكشاف العلامات الأساسية في ملفات DWG باستخدام مكتبة Aspose.CAD for .NET القوية.

## المتطلبات الأساسية

قبل أن نتعمق في البرنامج التعليمي، تأكد من أن لديك ما يلي:

- فهم أساسي لبرمجة C# و.NET.
-  تم تثبيت Aspose.CAD لمكتبة .NET. إذا لم يكن الأمر كذلك، يمكنك تنزيله[هنا](https://releases.aspose.com/cad/net/).
- ملف DWG للاختبار. يمكنك استخدام الملف النموذجي "BlockRefDgn.dwg" الموجود في البرنامج التعليمي.

## استيراد مساحات الأسماء

للبدء، تحتاج إلى استيراد مساحات الأسماء الضرورية. إليك مقتطف لمساعدتك:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;

```

## الخطوة 1: تحميل ملف DWG وتحويله إلى CadImage

ابدأ بتحميل ملف DWG الموجود وتحويله إلى CadImage:

```csharp
string fileName = MyDir + "BlockRefDgn.dwg";

// قم بتحميل ملف DWG وقم بتحويله إلى CadImage
using (CadImage image = (CadImage)Image.Load(fileName))
{
    // سيتم وضع الرمز الخاص بك للخطوات اللاحقة هنا
}
```

## الخطوة 2: التكرار من خلال الكيانات

بعد ذلك، قم بالتكرار عبر كل كيان داخل ملف DWG:

```csharp
foreach (CadBaseEntity entity in image.Entities)
{
    // سيتم وضع الرمز الخاص بك للخطوات اللاحقة هنا
}
```

## الخطوة 3: التحقق من نوع CadDgnUnderlay

تحقق مما إذا كان الكيان من النوع CadDgnUnderlay:

```csharp
if (entity is CadDgnUnderlay)
{
    // سيتم وضع الرمز الخاص بك للخطوات اللاحقة هنا
}
```

## الخطوة 4: الوصول إلى العلامات الأساسية

الوصول إلى العلامات الأساسية المختلفة واستخراج المعلومات ذات الصلة:

```csharp
CadUnderlay underlay = entity as CadUnderlay;

Console.WriteLine(underlay.UnderlayPath);
Console.WriteLine(underlay.UnderlayName);
Console.WriteLine(underlay.InsertionPoint.X);
Console.WriteLine(underlay.InsertionPoint.Y);
Console.WriteLine(underlay.RotationAngle);
Console.WriteLine(underlay.ScaleX);
Console.WriteLine(underlay.ScaleY);
Console.WriteLine(underlay.ScaleZ);
Console.WriteLine((underlay.Flags & UnderlayFlags.UnderlayIsOn) == UnderlayFlags.UnderlayIsOn);
Console.WriteLine((underlay.Flags & UnderlayFlags.ClippingIsOn) == UnderlayFlags.ClippingIsOn);
Console.WriteLine((underlay.Flags & UnderlayFlags.Monochrome) != UnderlayFlags.Monochrome);
```

## خاتمة

تهانينا! لقد نجحت في استكشاف العلامات الأساسية لملفات DWG باستخدام Aspose.CAD لـ .NET. يزودك هذا البرنامج التعليمي بالمعرفة اللازمة للتنقل عبر الكيانات واستخراج المعلومات المهمة حول الطبقات السفلية.

## الأسئلة الشائعة

### س1: هل يمكنني استخدام Aspose.CAD لـ .NET مع تنسيقات ملفات CAD الأخرى؟

A1: يدعم Aspose.CAD تنسيقات CAD المتنوعة، بما في ذلك DWG وDXF وDGN والمزيد. تحقق من الوثائق للحصول على القائمة الكاملة.

### س2: هل يتوفر ترخيص مؤقت لـ Aspose.CAD لـ .NET؟

 ج2: نعم، يمكنك الحصول على ترخيص مؤقت[هنا](https://purchase.aspose.com/temporary-license/).

### س3: أين يمكنني العثور على دعم لـ Aspose.CAD لـ .NET؟

 ج3: قم بزيارة منتدى الدعم[هنا](https://forum.aspose.com/c/cad/19) للمساعدة.

### س4: كيف يمكنني شراء Aspose.CAD لـ .NET؟

ج4: شراء المكتبة[هنا](https://purchase.aspose.com/buy).

### س5: هل هناك نسخة تجريبية مجانية متاحة؟

 ج5: نعم، يمكنك الوصول إلى النسخة التجريبية المجانية[هنا](https://releases.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
