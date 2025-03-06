---
title: تحويل DWG إلى تنسيق PDF - البرنامج التعليمي Aspose.CAD
linktitle: تحويل DWG إلى PDF متوافق
second_title: Aspose.CAD .NET - تنسيق ملف CAD وBIM
description: تحويل DWG إلى PDF متوافق باستخدام Aspose.CAD لـ .NET. اتبع البرنامج التعليمي لدينا للحصول على إرشادات خطوة بخطوة.
weight: 13
url: /ar/net/conversion-and-export/converting-dwg-to-compliance-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تحويل DWG إلى تنسيق PDF - البرنامج التعليمي Aspose.CAD

## مقدمة

مرحبًا بك في برنامجنا التعليمي خطوة بخطوة حول تحويل ملفات DWG إلى PDF متوافق باستخدام Aspose.CAD لـ .NET. Aspose.CAD عبارة عن واجهة برمجة تطبيقات .NET قوية تمكن المطورين من العمل مع تنسيقات ملفات CAD دون عناء. في هذا البرنامج التعليمي، سنرشدك خلال عملية تحويل ملف DWG إلى ملف PDF متوافق مع أمثلة وشروحات مفصلة.

## المتطلبات الأساسية

قبل أن نبدأ، تأكد من توفر المتطلبات الأساسية التالية:

-  Aspose.CAD for .NET: تأكد من دمج مكتبة Aspose.CAD في مشروع .NET الخاص بك. يمكنك تنزيله[هنا](https://releases.aspose.com/cad/net/).

- بيئة التطوير: قم بتثبيت بيئة تطوير .NET عاملة، وتأكد من تكوينها بشكل صحيح.

- نموذج ملف DWG: قم بتنزيل نموذج ملف DWG الذي تريد تحويله إلى تنسيق PDF.

## استيراد مساحات الأسماء

في مشروع .NET الخاص بك، قم باستيراد مساحات الأسماء الضرورية للاستفادة من وظائف Aspose.CAD.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

الآن، دعنا نقسم عملية تحويل ملف DWG إلى Compliance PDF إلى خطوات متعددة.

## الخطوة 1: قم بتحميل ملف DWG

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

Aspose.CAD.Image cadImage = Aspose.CAD.Image.Load(sourceFilePath);
```

## الخطوة 2: تعيين خيارات التنقيط

 إنشاء مثيل ل`CadRasterizationOptions` وتكوين خصائصه، مثل لون الخلفية وعرض الصفحة وارتفاع الصفحة.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions
{
    BackgroundColor = Aspose.CAD.Color.White,
    PageWidth = 1600,
    PageHeight = 1600
};
```

## الخطوة 3: إنشاء خيارات PDF

 إنشاء مثيل ل`PdfOptions` وقم بتعيين خيارات تنقيط المتجهات.

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions,
    CorePdfOptions = new PdfDocumentOptions { Compliance = PdfCompliance.PdfA1a }
};
```

## الخطوة 4: حفظ بصيغة PDF (الامتثال لمعايير A1a)

احفظ صورة CAD كملف PDF متوافق مع توافق A1a.

```csharp
cadImage.Save(MyDir + "PDFA1_A.pdf", pdfOptions);
```

## الخطوة 5: حفظ بتنسيق PDF (الامتثال لمعايير A1b)

قم بتغيير نوع التوافق إلى A1b واحفظ صورة CAD بتنسيق PDF الخاص بالتوافق.

```csharp
pdfOptions.CorePdfOptions.Compliance = PdfCompliance.PdfA1b;
cadImage.Save(MyDir + "PDFA1_B.pdf", pdfOptions);
```

## خاتمة

تهانينا! لقد نجحت في تحويل ملف DWG إلى Compliance PDF باستخدام Aspose.CAD لـ .NET. يوفر هذا البرنامج التعليمي دليلاً شاملاً للمطورين الذين يتطلعون إلى دمج إمكانات تحويل CAD في تطبيقاتهم.

## الأسئلة الشائعة

### س1: هل يمكنني تحويل تنسيقات CAD الأخرى إلى تنسيق PDF متوافق باستخدام Aspose.CAD؟

ج1: نعم، يدعم Aspose.CAD العديد من تنسيقات CAD، مما يتيح التحويل إلى Compliance PDF.

### س2: هل Aspose.CAD متوافق مع .NET Core؟

ج2: نعم، Aspose.CAD متوافق مع كل من .NET Framework و.NET Core.

### س3: هل هناك أي خيارات ترخيص لـ Aspose.CAD؟

 ج3: نعم، يمكنك استكشاف خيارات الترخيص[هنا](https://purchase.aspose.com/buy).

### س4: هل هناك نسخة تجريبية مجانية متاحة؟

 ج4: نعم، يمكنك الحصول على نسخة تجريبية مجانية[هنا](https://releases.aspose.com/).

### س5: أين يمكنني الحصول على الدعم لـ Aspose.CAD؟

ج5: قم بزيارة[منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19) لأية استفسارات متعلقة بالدعم.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
