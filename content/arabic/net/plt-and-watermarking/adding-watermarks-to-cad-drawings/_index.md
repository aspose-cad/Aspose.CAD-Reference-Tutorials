---
title: إضافة علامات مائية إلى رسومات CAD - دليل Aspose.CAD
linktitle: إضافة علامات مائية إلى رسومات CAD
second_title: Aspose.CAD .NET - تنسيق ملف CAD وBIM
description: قم بتحسين رسومات CAD الخاصة بك باستخدام علامات مائية احترافية باستخدام Aspose.CAD لـ .NET. اتبع دليلنا خطوة بخطوة للحصول على تصميمات مخصصة وجذابة.
type: docs
weight: 11
url: /ar/net/plt-and-watermarking/adding-watermarks-to-cad-drawings/
---
## مقدمة

هل تتطلع إلى تحسين رسومات CAD الخاصة بك عن طريق إضافة علامات مائية احترافية؟ يوفر Aspose.CAD for .NET حلاً قويًا لدمج العلامات المائية بسلاسة في ملفات CAD الخاصة بك. في هذا الدليل التفصيلي، سنرشدك خلال عملية إضافة العلامات المائية باستخدام Aspose.CAD، مما يضمن أن رسوماتك لا تنقل المعلومات المهمة فحسب، بل تحمل أيضًا علامتك الفريدة.

## المتطلبات الأساسية

قبل الغوص في البرنامج التعليمي، تأكد من أن لديك ما يلي:
-  Aspose.CAD لـ .NET: تأكد من تثبيت مكتبة Aspose.CAD. يمكنك تنزيله[هنا](https://releases.aspose.com/cad/net/).
- دليل المستندات الخاص بك: قم بإعداد دليل لتخزين رسومات CAD الخاصة بك.
الآن، لنبدأ بإضافة العلامات المائية إلى رسومات CAD الخاصة بك!

## استيراد مساحات الأسماء

ابدأ باستيراد مساحات الأسماء الضرورية إلى مشروع .NET الخاص بك:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## الخطوة 1: قم بتحميل رسم CAD

```csharp
// المسار إلى دليل المستندات.
string MyDir = "Your Document Directory";
using (CadImage cadImage = (CadImage)Image.Load(MyDir + "Drawing11.dwg")) {
```

## الخطوة 2: أضف علامة مائية كـ MTEXT

```csharp
// إضافة MTEXT جديد
CadMText watermark = new CadMText();
watermark.Text = "Watermark message";
watermark.InitialTextHeight = 40;
watermark.InsertionPoint = new Cad3DPoint(300, 40);
watermark.LayerName = "0";
cadImage.BlockEntities["*Model_Space"].AddEntity(watermark);
```

## الخطوة 3: أو أضف علامة مائية كنص

```csharp
// وبدلاً من ذلك، أضف كيانًا أبسط مثل Text
CadText text = new CadText();
text.DefaultValue = "Watermark text";
text.TextHeight = 40;
text.FirstAlignment = new Cad3DPoint(300, 40);
text.LayerName = "0";
cadImage.BlockEntities["*Model_Space"].AddEntity(text);
```

## الخطوة 4: التصدير إلى PDF

```csharp
// تصدير رسم CAD مع العلامة المائية إلى PDF
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.Layouts = new[] { "Model" };
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
cadImage.Save(MyDir + "AddWatermark_out.pdf", pdfOptions);
```

كرر هذه الخطوات لرسومات مختلفة، وستحصل على ملفات CAD ذات علامات مائية ذات مظهر احترافي في وقت قصير جدًا!

## خاتمة

تهانينا! لقد تعلمت بنجاح كيفية إضافة علامات مائية إلى رسومات CAD الخاصة بك باستخدام Aspose.CAD لـ .NET. تسمح لك هذه العملية البسيطة والقوية بتخصيص تصميماتك مع الحفاظ على سلامة رسوماتك الفنية.

## الأسئلة الشائعة

### س1: هل يمكنني تخصيص مظهر العلامة المائية؟

A1: نعم، يمكنك تخصيص النص والخط والحجم وموضع العلامة المائية وفقًا لتفضيلاتك.

### س2: هل Aspose.CAD متوافق مع تنسيقات ملفات CAD المختلفة؟

ج2: يدعم Aspose.CAD العديد من تنسيقات ملفات CAD، بما في ذلك DWG وDXF، مما يضمن التوافق الواسع.

### س3: هل يمكنني إضافة علامات مائية متعددة إلى رسم CAD واحد؟

ج3: بالتأكيد! يمكنك إضافة العديد من العلامات المائية حسب الحاجة، مما يوفر المرونة لحالات الاستخدام المختلفة.

### س4: هل يقدم Aspose.CAD نسخة تجريبية مجانية؟

ج4: نعم، يمكنك استكشاف ميزات Aspose.CAD من خلال النسخة التجريبية المجانية. احصل عليه[هنا](https://releases.aspose.com/).

### س5: أين يمكنني العثور على الدعم لـ Aspose.CAD؟

 ج5: لأية استفسارات أو مساعدة، قم بزيارة[منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19).