---
title: ضبط الخلفية وألوان الرسم في Aspose.CAD لـ .NET
linktitle: ضبط الخلفية وألوان الرسم
second_title: Aspose.CAD .NET - تنسيق ملف CAD وBIM
description: ماجستير Aspose.CAD لـ .NET. قم بتعيين الخلفية ورسم الألوان دون عناء. اتبع دليلنا خطوة بخطوة.
type: docs
weight: 15
url: /ar/net/cad-features-and-support/setting-background-and-drawing-colors/
---
## مقدمة

في العالم الديناميكي لتطوير .NET، يظهر Aspose.CAD كأداة قوية للتعامل مع ملفات التصميم بمساعدة الكمبيوتر (CAD). إذا كنت حريصًا على تحسين مهاراتك في التعامل مع رسومات CAD، فهذا البرنامج التعليمي هو بوابتك. سنتعمق في تعقيدات إعداد الخلفية وألوان الرسم باستخدام Aspose.CAD لـ .NET، مما يوفر لك دليلًا خطوة بخطوة يضمن الوضوح والفعالية.

## المتطلبات الأساسية

قبل أن نبدأ هذه الرحلة، تأكد من توفر المتطلبات الأساسية التالية:

- الفهم الأساسي لتطوير .NET.
-  تثبيت Aspose.CAD لـ .NET. إذا لم تقم بذلك بعد، يمكنك تنزيله[هنا](https://releases.aspose.com/cad/net/).
- نموذج لملف CAD للتجربة. يمكنك العثور على واحد في دليل المستندات الخاص بك.

## استيراد مساحات الأسماء

في مشروع .NET الخاص بك، ابدأ باستيراد مساحات الأسماء الضرورية:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## الخطوة 1: قم بتحميل ملف CAD

ابدأ بتحميل ملف CAD الذي تريد العمل به باستخدام مقتطف التعليمات البرمجية التالي:

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    // الكود الخاص بك لمزيد من المعالجة موجود هنا
}
```

## الخطوة 2: تكوين خيارات التنقيط

 إنشاء مثيل ل`CadRasterizationOptions` وتعيين خصائصه لإعداد الخلفية ولون الرسم:

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.BackgroundColor = Color.Beige;
rasterizationOptions.DrawType = CadDrawTypeMode.UseDrawColor;
rasterizationOptions.DrawColor = Color.Blue;
```

## الخطوة 3: التصدير إلى PDF

 إنشاء مثيل ل`PdfOptions` وتعيين`VectorRasterizationOptions` ملكية:

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;

// تصدير CAD إلى PDF
image.Save(MyDir + "result_out.pdf", pdfOptions);
```

## الخطوة 4: التصدير إلى TIFF

 إنشاء مثيل ل`TiffOptions` وتعيين`VectorRasterizationOptions` ملكية:

```csharp
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.VectorRasterizationOptions = rasterizationOptions;

// تصدير CAD إلى TIFF
image.Save(MyDir + "result_out.tiff", tiffOptions);
```

## خاتمة

تهانينا! لقد تعلمت بنجاح كيفية تعيين ألوان الخلفية والرسم في Aspose.CAD لـ .NET. يزودك هذا البرنامج التعليمي بالمهارات اللازمة للتعامل مع ملفات CAD دون عناء.

## الأسئلة الشائعة

### س 1: هل يمكنني استخدام Aspose.CAD لـ .NET مع أي نوع من ملفات CAD؟

ج1: نعم، يدعم Aspose.CAD تنسيقات CAD المتنوعة، بما في ذلك DWG وDXF وDGN.

### س2: هل تتوفر نسخة تجريبية مجانية من Aspose.CAD لـ .NET؟

 ج2: نعم، يمكنك استكشاف النسخة التجريبية المجانية[هنا](https://releases.aspose.com/).

### س3: أين يمكنني العثور على الوثائق التفصيلية الخاصة بـ Aspose.CAD لـ .NET؟

 ج3: راجع الوثائق[هنا](https://reference.aspose.com/cad/net/).

### س4: كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.CAD؟

 ج4: يمكن الحصول على تراخيص مؤقتة[هنا](https://purchase.aspose.com/temporary-license/).

### س5: هل تحتاج إلى مساعدة أو تريد التواصل مع المجتمع؟

 ج5: قم بزيارة منتدى الدعم[هنا](https://forum.aspose.com/c/cad/19).
