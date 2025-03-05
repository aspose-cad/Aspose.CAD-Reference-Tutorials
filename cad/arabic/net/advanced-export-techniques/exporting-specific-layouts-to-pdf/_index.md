---
title: تصدير تخطيطات محددة إلى PDF - دليل Aspose.CAD
linktitle: تصدير تخطيطات محددة إلى PDF
second_title: Aspose.CAD .NET - تنسيق ملف CAD وBIM
description: تعرف على كيفية تصدير تخطيطات محددة إلى PDF باستخدام Aspose.CAD لـ .NET. دليل خطوة بخطوة للتكامل السلس.
type: docs
weight: 13
url: /ar/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/
---
## مقدمة

مرحبًا بك في دليلنا خطوة بخطوة حول تصدير تخطيطات محددة إلى PDF باستخدام Aspose.CAD لـ .NET. Aspose.CAD هي مكتبة قوية تتيح للمطورين العمل مع تنسيقات ملفات CAD بسلاسة. في هذا البرنامج التعليمي، سنركز على تصدير تخطيطات محددة من ملف DWG إلى PDF باستخدام Aspose.CAD في بيئة .NET.

## المتطلبات الأساسية

قبل أن نتعمق في البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:

-  Aspose.CAD لمكتبة .NET: تأكد من تثبيت مكتبة Aspose.CAD. يمكنك تنزيله[هنا](https://releases.aspose.com/cad/net/).

- بيئة التطوير: قم بإعداد بيئة تطوير .NET، مثل Visual Studio.

## استيراد مساحات الأسماء

في مشروع .NET الخاص بك، قم باستيراد مساحات الأسماء الضرورية لـ Aspose.CAD:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## الخطوة 1: تحميل ملف DWG

```csharp
// المسار إلى دليل المستندات.
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";

using (Image image = Image.Load(sourceFilePath))
{
    // الكود الخاص بك لمزيد من الخطوات موجود هنا.
}
```

## الخطوة 2: قم بتعيين خيارات CadRasterization

```csharp
// قم بإنشاء مثيل لـ CadRasterizationOptions وقم بتعيين خصائصه المتنوعة
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
```

## الخطوة 3: تحديد اسم التخطيط

```csharp
// حدد اسم التخطيط المطلوب
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

## الخطوة 4: إنشاء خيارات Pdf

```csharp
// قم بإنشاء مثيل لـ PdfOptions
PdfOptions pdfOptions = new PdfOptions();
// قم بتعيين الخاصية VectorRasterizationOptions
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## الخطوة 5: التصدير إلى PDF

```csharp
MyDir = MyDir + "ExportSpecificLayoutToPDF_out.pdf";
// تصدير DWG إلى PDF
image.Save(MyDir, pdfOptions);
```

## الخطوة 6: عرض رسالة النجاح

```csharp
// عرض رسالة النجاح
Console.WriteLine("\nThe DWG file with a specific layout exported successfully to PDF.\nFile saved at " + MyDir);
```

## خاتمة

تهانينا! لقد تعلمت بنجاح كيفية تصدير تخطيطات محددة إلى PDF باستخدام Aspose.CAD لـ .NET. يوفر هذا الدليل إرشادات مفصلة، مما يضمن أنه يمكنك دمج هذه الوظيفة في مشاريعك دون عناء.

## الأسئلة الشائعة

### س1: هل يمكنني تصدير تخطيطات متعددة في وقت واحد؟

 ج1: نعم، ما عليك سوى تعديل الملف`Layouts` المصفوفة في الخطوة 3 لتضمين أسماء جميع التخطيطات المطلوبة.

### س2: هل Aspose.CAD متوافق مع تنسيقات ملفات CAD الأخرى؟

ج2: نعم، يدعم Aspose.CAD تنسيقات CAD المتنوعة، بما في ذلك DWG وDXF وDWF والمزيد.

### س3: كيف يمكنني ضبط إعدادات إخراج PDF؟

 ج3: استكشاف خصائص`CadRasterizationOptions` في الخطوة 2 للحصول على خيارات التخصيص.

### س4: أين يمكنني العثور على وثائق Aspose.CAD الإضافية؟

 ج4: قم بزيارة[توثيق](https://reference.aspose.com/cad/net/) للحصول على معلومات متعمقة.

### س5: هل هناك نسخة تجريبية مجانية متاحة؟

 ج5: نعم، يمكنك الوصول إلى النسخة التجريبية المجانية[هنا](https://releases.aspose.com/).