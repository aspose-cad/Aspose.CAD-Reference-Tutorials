---
title: تصدير DWG إلى PDF أو صور نقطية - دليل Aspose.CAD
linktitle: تصدير DWG إلى PDF أو الصور النقطية
second_title: Aspose.CAD .NET - تنسيق ملف CAD وBIM
description: استكشف دليلاً شاملاً حول تصدير DWG إلى PDF أو الصور النقطية باستخدام Aspose.CAD لـ .NET. تعرف على الخطوات والمتطلبات الأساسية وتدرب على هذه المكتبة القوية.
type: docs
weight: 11
url: /ar/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/
---
## مقدمة

هل تتطلع إلى تحويل ملفات DWG بسلاسة إلى PDF أو صور نقطية في تطبيق .NET الخاص بك؟ لا مزيد من البحث! سيرشدك هذا الدليل خطوة بخطوة خلال العملية باستخدام مكتبة Aspose.CAD لـ .NET القوية. سواء كنت مطورًا متمرسًا أو بدأت للتو، فإن هذا البرنامج التعليمي يلبي جميع مستويات المهارة.

## المتطلبات الأساسية

قبل أن نتعمق في البرنامج التعليمي، تأكد من أن لديك ما يلي:

- فهم أساسي لبرمجة .NET.
-  تم تثبيت Aspose.CAD لمكتبة .NET. إذا لم يكن الأمر كذلك، قم بتنزيله[هنا](https://releases.aspose.com/cad/net/).
- تم إعداد بيئة التطوير المتكاملة (IDE) المفضلة لديك لتطوير .NET.

## استيراد مساحات الأسماء

لنبدأ الأمور عن طريق استيراد مساحات الأسماء الضرورية في مشروع .NET الخاص بك. وهذا يضمن أن لديك إمكانية الوصول إلى وظيفة Aspose.CAD في التعليمات البرمجية الخاصة بك.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
```

## الخطوة 1: تحميل ملف DWG

ابدأ بتحميل ملف DWG الذي ترغب في تحويله. استبدل "دليل المستندات الخاص بك" بالمسار إلى ملف DWG الخاص بك.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // الكود الخاص بك لتحميل DWG موجود هنا
}
```

## الخطوة 2: إعداد تصدير PDF

الآن، دعونا نقوم بتكوين إعدادات تصدير PDF. يوضح هذا المثال كيفية تعيين التخطيط والتعامل مع تحويلات الوحدات.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };

// فحص وتحديد نظام الوحدة
bool currentUnitIsMetric = false;
double currentUnitCoefficient = 1.0;
DefineUnitSystem(cadImage.UnitType, out currentUnitIsMetric, out currentUnitCoefficient);

// الكود الخاص بك لإعداد تصدير PDF موجود هنا
```

## الخطوة 3: التصدير إلى PDF

قم بتنفيذ التصدير إلى PDF باستخدام الإعدادات التي تم تكوينها.

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath, pdfOptions);
```

## الخطوة 4: التصدير إلى الصور النقطية

قم بتوسيع وظيفة التصدير إلى الصور النقطية، مثل PNG.

```csharp
// حجم A4 بدقة 300 نقطة لكل بوصة - 2480 × 3508
rasterizationOptions.PageHeight = 3508;
rasterizationOptions.PageWidth = 2480;

PngOptions pngOptions = new PngOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath.Replace("pdf", "png"), pngOptions);
```

## خاتمة

تهانينا! لقد تعلمت بنجاح كيفية استخدام Aspose.CAD لـ .NET لتصدير ملفات DWG إلى كل من ملفات PDF والصور النقطية. تعمل هذه المكتبة القوية على تبسيط العملية، مما يجعلها فعالة وصديقة للمطورين.

## الأسئلة الشائعة

### س1: هل يمكنني استخدام Aspose.CAD لـ .NET في مشاريعي التجارية؟

 ج1: نعم يمكنك ذلك. يزور[buy.aspose.com/buy](https://purchase.aspose.com/buy) للحصول على تفاصيل الترخيص.

### س2: هل هناك نسخة تجريبية مجانية متاحة؟

 ج2: بالتأكيد! احصل على النسخة التجريبية المجانية[هنا](https://releases.aspose.com/).

### س3: كيف يمكنني الحصول على دعم Aspose.CAD لـ .NET؟

 ج3: توجه إلى[منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19) لدعم المجتمع.

### س4: هل يمكنني الحصول على ترخيص مؤقت لأغراض الاختبار؟

ج4: نعم، يمكنك الحصول على ترخيص مؤقت[هنا](https://purchase.aspose.com/temporary-license/).

### س5: أين يمكنني العثور على الوثائق التفصيلية؟

 ج5: الوثائق متاحة على[Aspose.CAD](https://reference.aspose.com/cad/net/).