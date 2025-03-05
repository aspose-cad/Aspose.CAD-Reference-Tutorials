---
title: إنشاء ملف PDF واحد بتخطيطات مختلفة - دليل Aspose.CAD
linktitle: إنشاء ملف PDF واحد بتخطيطات مختلفة
second_title: Aspose.CAD .NET - تنسيق ملف CAD وBIM
description: قم بإنشاء ملف PDF واحد بتخطيطات مختلفة باستخدام Aspose.CAD لـ .NET. اتبع دليلنا خطوة بخطوة للتكامل السلس وإنشاء ملفات PDF بكفاءة.
type: docs
weight: 13
url: /ar/net/advanced-cad-techniques/creating-single-pdf-with-different-layouts/
---
## مقدمة

هل تتطلع إلى إنشاء مستند PDF واحد من رسم CAD بتخطيطات مختلفة باستخدام Aspose.CAD لـ .NET؟ سيرشدك هذا الدليل خطوة بخطوة خلال العملية، مما يساعدك على تحقيق التكامل السلس وإنشاء ملفات PDF بكفاءة. يوفر Aspose.CAD for .NET ميزات قوية لمعالجة رسومات CAD برمجيًا، وفي هذا البرنامج التعليمي، سنركز على إنشاء ملف PDF واحد بتخطيطات مختلفة.

## المتطلبات الأساسية

قبل الغوص في البرنامج التعليمي، تأكد من أن لديك المتطلبات الأساسية التالية:

-  Aspose.CAD لـ .NET: تأكد من تثبيت Aspose.CAD لـ .NET. يمكنك تنزيله من[هنا](https://releases.aspose.com/cad/net/).

- بيئة التطوير: قم بإعداد بيئة تطوير .NET، واحصل على فهم أساسي لبرمجة C#.

## استيراد مساحات الأسماء

في مشروع C# الخاص بك، قم بتضمين مساحات الأسماء اللازمة للاستفادة من وظائف Aspose.CAD لـ .NET:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## الخطوة 1: قم بتحميل صورة CAD

```csharp
// المسار إلى دليل المستندات.
string MyDir = "Your Document Directory";

using (CadImage cadImage = (CadImage)Image.Load(MyDir + "City skyway map.dwg"))
{
    // الكود الخاص بك للخطوة 1 موجود هنا
}
```

## الخطوة 2: تخصيص خيارات التنقيط

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1000;
rasterizationOptions.PageHeight = 1000;

// أحجام مخصصة لعدة تخطيطات
rasterizationOptions.LayoutPageSizes.Add("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.LayoutPageSizes.Add("8.5 x 11 Plot", new SizeF(1000, 100));
```

## الخطوة 3: تحديد خيارات PDF

```csharp
PdfOptions pdfOptions = new PdfOptions() { VectorRasterizationOptions = rasterizationOptions };
```

## الخطوة 4: احفظ بصيغة PDF

```csharp
cadImage.Save(MyDir + "singlePDF_out.pdf", pdfOptions);
```

لقد نجحت الآن في إنشاء مستند PDF واحد بتخطيطات مختلفة باستخدام Aspose.CAD لـ .NET. لا تتردد في استكشاف المزيد من الميزات وتخصيص الكود وفقًا لمتطلباتك المحددة.

## خاتمة

في هذا البرنامج التعليمي، قمنا بتغطية عملية إنشاء ملف PDF واحد من رسم CAD بتخطيطات مختلفة باستخدام Aspose.CAD لـ .NET. تعمل هذه المكتبة القوية على تبسيط مهام معالجة CAD وتوفر المرونة لمختلف السيناريوهات.

## الأسئلة الشائعة

### س1: هل يمكنني استخدام Aspose.CAD لـ .NET مع تنسيقات CAD الأخرى؟

ج1: نعم، يدعم Aspose.CAD for .NET تنسيقات CAD المتنوعة مثل DWG وDXF وDGN والمزيد.

### س2: هل هناك نسخة تجريبية مجانية متاحة؟

 ج2: نعم، يمكنك استكشاف النسخة التجريبية المجانية[هنا](https://releases.aspose.com/).

### س3: كيف يمكنني الحصول على دعم Aspose.CAD لـ .NET؟

 ج3: قم بزيارة[منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19) لدعم المجتمع.

### س4: أين يمكنني العثور على وثائق مفصلة؟

 ج4: راجع الوثائق[هنا](https://reference.aspose.com/cad/net/).

### س5: هل يمكنني شراء ترخيص Aspose.CAD لـ .NET؟

 ج5: نعم، يمكنك شراء ترخيص[هنا](https://purchase.aspose.com/buy).