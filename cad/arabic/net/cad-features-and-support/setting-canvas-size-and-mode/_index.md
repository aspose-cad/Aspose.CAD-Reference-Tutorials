---
title: ضبط حجم القماش ووضعه في Aspose.CAD لـ .NET
linktitle: ضبط حجم القماش ووضعه
second_title: Aspose.CAD .NET - تنسيق ملف CAD وBIM
description: استكشف الدليل التفصيلي خطوة بخطوة حول تعيين حجم اللوحة القماشية ووضعها في Aspose.CAD لـ .NET. قم بتحسين عرض CAD الخاص بك بسهولة باستخدام هذا البرنامج التعليمي الشامل.
type: docs
weight: 16
url: /ar/net/cad-features-and-support/setting-canvas-size-and-mode/
---
## مقدمة

هل أنت مستعد لإطلاق الإمكانات الكاملة لـ Aspose.CAD لـ .NET وإحداث ثورة في تجربة عرض CAD لديك؟ في هذا البرنامج التعليمي خطوة بخطوة، سنتعمق في تعقيدات تحديد حجم اللوحة ووضعها باستخدام مكتبة Aspose.CAD القوية. سواء كنت مطورًا متمرسًا أو بدأت للتو، سيرشدك هذا الدليل خلال العملية، مما يضمن لك الاستفادة من إمكانات Aspose.CAD بشكل فعال.

## المتطلبات الأساسية

قبل أن نتعمق في البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:

-  مكتبة Aspose.CAD: قم بتنزيل وتثبيت مكتبة Aspose.CAD من ملف[موقع Aspose.CAD](https://releases.aspose.com/cad/net/).

- بيئة التطوير: تأكد من إعداد بيئة تطوير .NET على جهازك.

-  نموذج ملف CAD: في هذا البرنامج التعليمي، سنستخدم نموذج ملف DXF. يمكنك العثور على واحد في[وثائق Aspose.CAD](https://reference.aspose.com/cad/net/).

## استيراد مساحات الأسماء

للبدء، قم باستيراد مساحات الأسماء الضرورية في بداية تطبيق .NET الخاص بك:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## الخطوة 1: تحميل ملف CAD

ابدأ بتحميل ملف CAD باستخدام الكود التالي:

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    //سيتم وضع الرمز الخاص بك لمزيد من الخطوات هنا
}
```

## الخطوة 2: إنشاء CadRasterizationOptions

 إنشاء مثيل ل`CadRasterizationOptions` وتعيين خصائصه:

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
rasterizationOptions.NoScaling = false;
```

## الخطوة 3: إنشاء خيارات Pdf

 إنشاء مثيل ل`PdfOptions` وتعيينها`VectorRasterizationOptions` ملكية:

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## الخطوة 4: التصدير إلى PDF

قم بتصدير ملف CAD إلى PDF باستخدام الخيارات التي تم تكوينها:

```csharp
image.Save(MyDir + "result_out.pdf", pdfOptions);
```

## الخطوة 5: إنشاء TiffOptions

 إنشاء مثيل ل`TiffOptions` وتعيينها`VectorRasterizationOptions` ملكية:

```csharp
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.VectorRasterizationOptions = rasterizationOptions;
```

## الخطوة 6: التصدير إلى TIFF

قم بتصدير ملف CAD إلى TIFF باستخدام الخيارات التي تم تكوينها:

```csharp
image.Save(MyDir + "result_out.tiff", tiffOptions);
```

## خاتمة

تهانينا! لقد قمت بنجاح بتعيين حجم اللوحة القماشية ووضعها في Aspose.CAD لـ .NET. تفتح هذه الميزة القوية عالمًا من الإمكانيات لعرض التصميم بمساعدة الكمبيوتر (CAD). قم بتجربة خيارات مختلفة واكتشف الإمكانات الكاملة لـ Aspose.CAD في تطبيقات .NET الخاصة بك.

## الأسئلة الشائعة

### س1: هل يمكنني استخدام Aspose.CAD مع مكتبات .NET الأخرى؟

ج1: نعم، يتكامل Aspose.CAD بسلاسة مع مكتبات .NET الأخرى، مما يوفر إمكانات محسنة لمعالجة CAD.

### س2: هل تتوفر نسخة تجريبية مجانية لـ Aspose.CAD؟

 ج2: نعم، يمكنك استكشاف ميزات Aspose.CAD من خلال النسخة التجريبية المجانية. يزور[هنا](https://releases.aspose.com/) للبدء.

### س3: كيف يمكنني الحصول على الدعم لـ Aspose.CAD؟

 ج3: للحصول على الدعم والمناقشات، قم بزيارة[منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19).

### س4: أين يمكنني العثور على وثائق شاملة لـ Aspose.CAD؟

 ج4: راجع[وثائق Aspose.CAD](https://reference.aspose.com/cad/net/) للحصول على معلومات وأمثلة مفصلة.

### س5: كيف يمكنني شراء Aspose.CAD لـ .NET؟

 ج5: لشراء Aspose.CAD، قم بزيارة[صفحة الشراء](https://purchase.aspose.com/buy).