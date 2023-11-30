---
title: تصدير DGN إلى PDF في Aspose.CAD لـ .NET
linktitle: تصدير DGN إلى PDF
second_title: Aspose.CAD .NET - تنسيق ملف CAD وBIM
description: تعرف على كيفية تصدير ملفات DGN إلى PDF بسهولة باستخدام Aspose.CAD لـ .NET. دليل خطوة بخطوة للتعامل السلس مع ملفات CAD.
type: docs
weight: 12
url: /ar/net/cad-export-formats/export-dgn-to-pdf/
---
## مقدمة

في عالم تطوير .NET، تعد Aspose.CAD مكتبة قوية تسهل معالجة ملفات CAD وتحويلها. إحدى المهام الشائعة التي يواجهها مطورو البرامج غالبًا هي تصدير ملفات DGN إلى تنسيق PDF. في هذا البرنامج التعليمي، سنتعرف على العملية خطوة بخطوة، باستخدام Aspose.CAD لـ .NET.

## المتطلبات الأساسية

قبل الغوص في البرنامج التعليمي، تأكد من أن لديك ما يلي:

- معرفة عملية بـ C# وإطار عمل .NET.
-  تم تثبيت Aspose.CAD لمكتبة .NET. يمكنك تنزيله[هنا](https://releases.aspose.com/cad/net/).
- نموذج لملف DGN، على سبيل المثال، "Nikon_D90_Camera.dgn" لهذا البرنامج التعليمي.

## استيراد مساحات الأسماء

في مشروع C# الخاص بك، ابدأ باستيراد مساحات الأسماء الضرورية:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## الخطوة 1: تحميل ملف DGN

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage cadImage = (DgnImage)Image.Load(sourceFilePath))
{
    // الكود الخاص بك هنا...
}
```

## الخطوة 2: تكوين خيارات التنقيط

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## الخطوة 3: إنشاء خيارات PDF

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## الخطوة 4: احفظ بصيغة PDF

```csharp
cadImage.Save(MyDir + "ExportDGNToPdf_out.pdf", pdfOptions);
```

## خاتمة

تهانينا! لقد نجحت في تصدير ملف DGN إلى PDF باستخدام Aspose.CAD لـ .NET. غطى هذا البرنامج التعليمي الخطوات الأساسية، بدءًا من تحميل ملف DGN وحتى تكوين خيارات التنقيط وحفظ الإخراج كملف PDF.

## الأسئلة الشائعة

### س1: هل يمكنني استخدام Aspose.CAD لـ .NET دون معرفة مسبقة بـ CAD؟

ج1: بالتأكيد! يعمل Aspose.CAD على تبسيط مهام CAD المعقدة، مما يجعله في متناول المطورين ذوي الخلفيات المتنوعة.

### س2: أين يمكنني العثور على المزيد من الأمثلة والوثائق الخاصة بـ Aspose.CAD؟

 ج2: اكتشف[توثيق](https://reference.aspose.com/cad/net/) للحصول على أدلة وأمثلة شاملة.

### س3: هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.CAD؟

 ج3: نعم، يمكنك الحصول على نسخة تجريبية مجانية[هنا](https://releases.aspose.com/).

### س4: كيف يمكنني الحصول على تراخيص مؤقتة لـ Aspose.CAD؟

 ج4: الحصول على تراخيص مؤقتة[هنا](https://purchase.aspose.com/temporary-license/).

### س5: هل تحتاج إلى مساعدة أو لديك أسئلة؟

 ج5: قم بزيارة[منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19) لدعم المجتمع.