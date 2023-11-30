---
title: تحويل تخطيطات CAD إلى PDF - البرنامج التعليمي Aspose.CAD
linktitle: تحويل تخطيطات CAD إلى PDF
second_title: Aspose.CAD .NET - تنسيق ملف CAD وBIM
description: قم بتحويل تخطيطات CAD إلى PDF بسهولة باستخدام Aspose.CAD لـ .NET. اتبع دليلنا خطوة بخطوة للتكامل السلس.
type: docs
weight: 10
url: /ar/net/cad-layouts-and-decomposition/converting-cad-layouts-to-pdf/
---
## مقدمة

هل تتطلع إلى تحويل تخطيطات CAD الخاصة بك إلى PDF بسلاسة؟ يوفر Aspose.CAD for .NET حلاً قويًا لجعل هذه العملية فعالة ومباشرة. في هذا البرنامج التعليمي، سنرشدك خلال خطوات استخدام Aspose.CAD، وهي واجهة برمجة تطبيقات قوية تمكن المطورين من العمل مع ملفات CAD دون عناء.

## المتطلبات الأساسية

قبل الغوص في البرنامج التعليمي، تأكد من أن لديك المتطلبات الأساسية التالية:

-  Aspose.CAD for .NET: قم بتنزيل المكتبة وتثبيتها. يمكن ان تجدها[هنا](https://releases.aspose.com/cad/net/).

- بيئة .NET: تأكد من أن لديك بيئة تطوير .NET عاملة.

- نموذج ملف CAD: احصل على نموذج ملف CAD جاهز للتحويل. في هذا البرنامج التعليمي، سوف نستخدم "conic_pyramid.dxf".

## استيراد مساحات الأسماء

ابدأ باستيراد مساحات الأسماء الضرورية إلى مشروع .NET الخاص بك. تضمن هذه الخطوة أن يكون لديك حق الوصول إلى وظائف Aspose.CAD.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
using Aspose.CAD.FileFormats.Cad;
```

## الخطوة 1: قم بإعداد مشروعك

ابدأ بإعداد مشروع .NET الخاص بك. أنشئ مشروعًا جديدًا أو افتح مشروعًا موجودًا حيث تريد تنفيذ تحويل CAD إلى PDF.

## الخطوة 2: تحديد مسار ملف CAD المصدر

حدد المسار إلى ملف CAD الخاص بك. في مثالنا، الملف المصدر هو "conic_pyramid.dxf."

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
```

## الخطوة 3: تحميل ملف CAD

قم بإنشاء مثيل لفئة CadImage وقم بتحميل ملف CAD في التطبيق.

```csharp
using (Aspose.CAD.Image cadImage = (Aspose.CAD.Image)Image.Load(sourceFilePath))
```

## الخطوة 4: تكوين خيارات التنقيط

قم بتكوين خيارات التنقيط لتخصيص مخرجات PDF. قم بتعيين أبعاد الصفحة وقياس التخطيط والمعلمات الأخرى ذات الصلة.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
// خيارات التكوين الأخرى...
```

## الخطوة 5: تعيين التخطيطات

حدد التخطيطات التي تريد تضمينها في ملف PDF. في هذا المثال، نستخدم تخطيط "النموذج".

```csharp
rasterizationOptions.Layouts = new string[] { "Model" };
```

## الخطوة 6: تحديد خيارات PDF

قم بإنشاء مثيل لفئة PdfOptions واربطه بخيارات التنقيط.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## الخطوة 7: ضبط خيارات الرسومات

قم بتكوين خيارات الرسومات لملف PDF، بما في ذلك وضع التجانس، وعرض النص، والاستيفاء.

```csharp
rasterizationOptions.GraphicsOptions.SmoothingMode = SmoothingMode.HighQuality;
rasterizationOptions.GraphicsOptions.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
rasterizationOptions.GraphicsOptions.InterpolationMode = InterpolationMode.HighQualityBicubic;
```

## الخطوة 8: حفظ إلى PDF

حدد مسار الإخراج لملف PDF واحفظ تخطيط CAD كملف PDF.

```csharp
MyDir = MyDir + "CADLayoutsToPDF_out.pdf";
cadImage.Save(MyDir, pdfOptions);
```

## خاتمة

تهانينا! لقد نجحت في تحويل تخطيطات CAD إلى PDF باستخدام Aspose.CAD لـ .NET. يوفر هذا البرنامج التعليمي دليلاً شاملاً للمطورين الذين يتطلعون إلى تبسيط هذه العملية في تطبيقاتهم.

## الأسئلة الشائعة

### س1: هل يمكنني تحويل تخطيطات CAD متعددة مرة واحدة؟

 A1: نعم، يمكنك تحديد تخطيطات متعددة في`Layouts` مجموعة لإدراجها في PDF.

### س2: هل هناك أي قيود على تنسيقات ملفات CAD المدعومة؟

ج2: يدعم Aspose.CAD for .NET تنسيقات CAD المتنوعة، بما في ذلك DWG وDXF.

### س3: كيف يمكنني تخصيص مظهر مخرجات PDF؟

A3: استخدم خيارات التنقيط والرسومات المتوفرة لتخصيص إخراج PDF حسب تفضيلاتك.

### س4: هل هناك إصدار تجريبي متاح لـ Aspose.CAD لـ .NET؟

 ج4: نعم، يمكنك استكشاف الميزات باستخدام[نسخة تجريبية مجانية](https://releases.aspose.com/).

### س5: أين يمكنني طلب الدعم أو طرح الأسئلة؟

 ج5: قم بزيارة[منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19) للمساعدة والمناقشات.