---
title: عناصر DGN المدعومة في Aspose.CAD لـ .NET
linktitle: عناصر DGN المدعومة
second_title: Aspose.CAD .NET - تنسيق ملف CAD وBIM
description: استكشف ميزات Aspose.CAD لـ .NET القوية للتعامل مع ملفات DGN. اتبع دليلنا خطوة بخطوة للعمل بسلاسة مع العناصر ثنائية وثلاثية الأبعاد.
type: docs
weight: 18
url: /ar/net/cad-features-and-support/supported-dgn-elements/
---
## مقدمة

هل أنت مطور .NET وتتطلع إلى العمل مع ملفات DGN بسلاسة؟ يوفر Aspose.CAD for .NET حلاً قويًا للتعامل مع ملفات DGN بكفاءة. في هذا البرنامج التعليمي، سوف نتعمق في عناصر DGN المدعومة، ونرشدك خلال عملية العمل مع Aspose.CAD لـ .NET.

## المتطلبات الأساسية

قبل أن نبدأ، تأكد من أن لديك ما يلي:

- المعرفة الأساسية ببرمجة .NET.
- تم تثبيت Visual Studio على جهازك.
-  Aspose.CAD لمكتبة .NET، والتي يمكنك تنزيلها[هنا](https://releases.aspose.com/cad/net/).

## استيراد مساحات الأسماء

لبدء مشروعك، قم باستيراد مساحات الأسماء الضرورية إلى تطبيق .NET الخاص بك. تضمن هذه الخطوة أن لديك إمكانية الوصول إلى الوظائف التي يوفرها Aspose.CAD لـ .NET.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.FileFormats.Dgn.DgnElements;
```

## الخطوة 1: قم بتحميل ملف DGN

ابدأ بتحميل ملف DGN موجود على هيئة CadImage في تطبيق .NET الخاص بك.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // الرمز الخاص بك هنا
}
```

## الخطوة 2: التكرار من خلال عناصر DGN

قم بالتكرار عبر عناصر DGN باستخدام حلقة foreach. يوفر Aspose.CAD for .NET مجموعة متنوعة من أنواع عناصر DGN التي يمكنك العمل بها.

```csharp
foreach (DgnDrawingElementBase element in dgnImage.Elements)
{
    // الرمز الخاص بك هنا
}
```

## الخطوة 3: التعامل مع الكيانات المدعومة مسبقًا

تعامل مع الكيانات ثنائية الأبعاد المدعومة مسبقًا، والتي أصبحت الآن مدعومة أيضًا للثلاثية الأبعاد.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.Line:
    case DgnElementType.Ellipse:
    case DgnElementType.Curve:
    // حالات إضافية
        {
            // الرمز الخاص بك هنا
            break;
        }
}
```

## الخطوة 4: التعامل مع الكيانات ثلاثية الأبعاد المدعومة

تعامل مع الكيانات ثلاثية الأبعاد المدعومة التي يوفرها Aspose.CAD لـ .NET.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.SolidHeader3D:
    case DgnElementType.Cone:
    case DgnElementType.CellHeader:
        {
            // الرمز الخاص بك هنا
            break;
        }
}
```

## الخطوة 5: التصدير والحفظ

أخيرًا، قم بتصدير ملف DGN المعدل إلى صورة نقطية واحفظه في الدليل المحدد.

```csharp
Console.WriteLine("\nThe DGN file exported successfully to raster image.\nFile saved at " + MyDir);
```

## خاتمة

في هذا البرنامج التعليمي، اكتشفنا إمكانيات Aspose.CAD لـ .NET في التعامل مع ملفات DGN ومعالجتها. باتباع الدليل الموضح خطوة بخطوة، يمكنك العمل بكفاءة مع عناصر DGN المدعومة، سواء كانت كيانات ثنائية أو ثلاثية الأبعاد. يمكّنك Aspose.CAD for .NET من دمج معالجة ملفات DGN بسلاسة في تطبيقات .NET الخاصة بك.

## الأسئلة الشائعة

### س1: أين يمكنني العثور على الوثائق الخاصة بـ Aspose.CAD لـ .NET؟

 ج1: يمكنك العثور على الوثائق[هنا](https://reference.aspose.com/cad/net/).

### س2: كيف يمكنني تنزيل Aspose.CAD لـ .NET؟

 ج2: يمكنك تنزيل المكتبة[هنا](https://releases.aspose.com/cad/net/).

### س3: هل تتوفر نسخة تجريبية مجانية من Aspose.CAD لـ .NET؟

 ج3: نعم، يمكنك الوصول إلى النسخة التجريبية المجانية[هنا](https://releases.aspose.com/).

### س4: أين يمكنني الحصول على تراخيص مؤقتة لـ Aspose.CAD لـ .NET؟

 ج4: التراخيص المؤقتة متاحة[هنا](https://purchase.aspose.com/temporary-license/).

### س5: هل تحتاج إلى مساعدة أو لديك أسئلة؟

 ج5: قم بزيارة مجتمع Aspose.CAD لـ .NET[منتدى الدعم](https://forum.aspose.com/c/cad/19).