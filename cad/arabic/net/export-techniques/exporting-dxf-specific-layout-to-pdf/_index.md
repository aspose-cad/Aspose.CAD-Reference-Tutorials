---
title: تصدير تخطيط DXF المحدد إلى PDF - دليل Aspose.CAD
linktitle: تصدير تخطيط DXF المحدد إلى PDF
second_title: Aspose.CAD .NET - تنسيق ملف CAD وBIM
description: تعرف على كيفية تصدير تخطيطات DXF محددة إلى PDF باستخدام Aspose.CAD لـ .NET. اتبع دليلنا خطوة بخطوة للحصول على تحويلات فعالة وعالية الجودة.
weight: 11
url: /ar/net/export-techniques/exporting-dxf-specific-layout-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تصدير تخطيط DXF المحدد إلى PDF - دليل Aspose.CAD

## مقدمة

مرحبًا بك في البرنامج التعليمي Aspose.CAD حول تصدير تخطيطات DXF المحددة إلى PDF باستخدام الميزات القوية لـ Aspose.CAD لـ .NET. سيرشدك هذا الدليل خطوة بخطوة خلال عملية تحويل ملفات DXF إلى PDF، مع التركيز على تخطيط محدد يسمى "النموذج". يوفر Aspose.CAD أدوات ووظائف فعالة لتبسيط عملية التحويل، مما يضمن مخرجات عالية الجودة لرسومات CAD الخاصة بك.

## المتطلبات الأساسية

قبل الغوص في البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:

- Aspose.CAD لـ .NET: تأكد من تثبيت مكتبة Aspose.CAD في مشروع .NET الخاص بك. يمكنك تنزيله[هنا](https://releases.aspose.com/cad/net/) واتبع تعليمات التثبيت المتوفرة في الوثائق.

- بيئة التطوير: قم بإعداد بيئة تطوير .NET عاملة، بما في ذلك Visual Studio أو أي بيئة تطوير متكاملة مفضلة أخرى.

- ملف DXF: قم بإعداد ملف DXF الذي تريد تحويله إلى PDF. في هذا الدليل، سنستخدم ملفًا نموذجيًا باسم "conic_pyramid.dxf."

## استيراد مساحات الأسماء

في مشروع .NET الخاص بك، قم بتضمين مساحات الأسماء الضرورية للاستفادة من وظائف Aspose.CAD. أضف الأسطر التالية في بداية الكود الخاص بك:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
namespace Aspose.CAD.Examples.CSharp.DXF_Drawings

```

## الخطوة 1: تحميل ملف DXF

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    //سيتم وضع الرمز الخاص بك لمزيد من الخطوات هنا
}
```

## الخطوة 2: تعيين خيارات التنقيط

```csharp
// قم بإنشاء مثيل لـ CadRasterizationOptions وقم بتعيين خصائصه المتنوعة
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
// حدد اسم التخطيط المطلوب
rasterizationOptions.Layouts = new string[] { "Model" };
```

## الخطوة 3: ضبط خيارات PDF

```csharp
// قم بإنشاء مثيل لـ PdfOptions
PdfOptions pdfOptions = new PdfOptions();
// قم بتعيين الخاصية VectorRasterizationOptions
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## الخطوة 4: تحديد مسار الإخراج

```csharp
MyDir = MyDir + "conic_pyramid_layout_out.pdf";
```

## الخطوة 5: تصدير DXF إلى PDF

```csharp
// تصدير DXF إلى PDF
image.Save(MyDir, pdfOptions);
```

## الخطوة 6: عرض رسالة النجاح

```csharp
// عرض رسالة النجاح
Console.WriteLine("\nThe DXF file with the specific layout exported successfully to PDF.\nFile saved at " + MyDir);
```

## خاتمة

تهانينا! لقد تعلمت بنجاح كيفية تصدير ملف DXF بتخطيط محدد إلى PDF باستخدام Aspose.CAD لـ .NET. يغطي هذا الدليل الخطوات الأساسية، بدءًا من تحميل ملف DXF وحتى ضبط خيارات التنقيط والتصدير إلى PDF.

## الأسئلة الشائعة

### س 1: هل Aspose.CAD متوافق مع كافة إصدارات ملفات DXF؟

 A1: يدعم Aspose.CAD إصدارات مختلفة من ملفات DXF. الرجوع إلى[توثيق](https://reference.aspose.com/cad/net/) للحصول على قائمة الإصدارات المدعومة.

### س2: هل يمكنني تخصيص إعدادات إخراج PDF؟

ج2: نعم، يمكنك تخصيص إعدادات إخراج PDF عن طريق ضبط خصائص`CadRasterizationOptions` و`PdfOptions` وفقا لمتطلباتك.

### س3: هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.CAD؟

 ج3: نعم، يمكنك استكشاف Aspose.CAD من خلال النسخة التجريبية المجانية من خلال زيارة الموقع[هنا](https://releases.aspose.com/).

### س4: كيف يمكنني الحصول على الدعم لـ Aspose.CAD؟

 ج4: للحصول على أي دعم أو استفسارات، قم بزيارة[منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19).

### س5: أين يمكنني شراء ترخيص Aspose.CAD؟

 ج5: يمكنك شراء ترخيص Aspose.CAD[هنا](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
