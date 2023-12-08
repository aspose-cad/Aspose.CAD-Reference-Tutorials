---
title: تصدير DGN إلى صورة نقطية في Aspose.CAD لـ .NET
linktitle: تصدير DGN إلى الصورة النقطية
second_title: Aspose.CAD .NET - تنسيق ملف CAD وBIM
description: قم بتحويل DGN إلى صور نقطية بسهولة باستخدام Aspose.CAD لـ .NET. استكشف الدليل التفصيلي خطوة بخطوة وأطلق العنان لقوة .NET في معالجة ملفات CAD.
type: docs
weight: 13
url: /ar/net/cad-export-formats/export-dgn-to-raster-image/
---
## مقدمة

في المجال الديناميكي لتطوير .NET، يظهر Aspose.CAD كأداة قوية للتعامل مع ملفات التصميم بمساعدة الكمبيوتر (CAD). يتعمق هذا البرنامج التعليمي في عملية تصدير ملفات DGN إلى صور نقطية باستخدام Aspose.CAD لـ .NET. إذا كنت حريصًا على تحويل ملفات DGN الخاصة بك إلى صور نقطية جذابة بصريًا بسلاسة، فأنت في المكان الصحيح.

## المتطلبات الأساسية

قبل أن نبدأ هذه الرحلة، تأكد من توفر المتطلبات الأساسية التالية:

-  Aspose.CAD لـ .NET: تأكد من تثبيت مكتبة Aspose.CAD في مشروع .NET الخاص بك. يمكنك العثور على المكتبة والوثائق ذات الصلة على[موقع إلكتروني](https://reference.aspose.com/cad/net/).

- نموذج ملف DGN: احصل على ملف DGN جاهز للتحويل. في مثالنا، سنستخدم "Nikon_D90_Camera.dgn."

الآن، دعنا نتعمق في الدليل خطوة بخطوة.

## استيراد مساحات الأسماء

في مشروع .NET الخاص بك، ابدأ باستيراد مساحات الأسماء الضرورية لـ Aspose.CAD. تتيح لك هذه الخطوة الوصول إلى الفئات والأساليب المطلوبة لتحويل DGN للصور النقطية.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## الخطوة 1: تحميل ملف DGN

 ابدأ بتحميل ملف DGN في ملف`CadImage` هدف. وهذا يوفر الأساس للعمليات اللاحقة.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // الكود الخاص بك لمزيد من المعالجة موجود هنا
}
```

## الخطوة 2: تحديد خيارات التنقيط

 إنشاء`CadRasterizationOptions` كائن وقم بتعيين خصائص مختلفة لتخصيص عملية التنقيط وفقًا لمتطلباتك.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## الخطوة 3: إنشاء كائن JpegOptions

 نظرًا لأننا نهدف إلى تحويل ملف DGN إلى JPEG، فقم بإنشاء ملف`JpegOptions` الكائن وتعيين المحدد مسبقا`CadRasterizationOptions` إليها.

```csharp
ImageOptionsBase options = new JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
```

## الخطوة 4: احفظ الصورة النقطية

 الاستفادة من`Save` طريقة`CadImage` فئة لتصدير ملف DGN إلى صورة نقطية بالتنسيق المطلوب، في هذه الحالة، JPEG.

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpg", options);
```

## خاتمة

تهانينا! لقد نجحت في التنقل خلال خطوات تصدير ملف DGN إلى صورة نقطية باستخدام Aspose.CAD لـ .NET. لقد زودك هذا البرنامج التعليمي بالمعرفة الأساسية لدمج هذه الوظيفة في مشاريع .NET الخاصة بك دون عناء.

## الأسئلة الشائعة

### س1: هل يمكنني تصدير ملفات DGN إلى تنسيقات أخرى غير JPEG؟

A1: نعم، يدعم Aspose.CAD for .NET تنسيقات الإخراج المختلفة. يمكنك تعديل الخيارات وفقًا لذلك في الخطوة 3.

### س2 كيف يمكنني التعامل مع الاستثناءات أثناء عملية التحويل؟

ج٢: تأكد من حصولك على معالجة الاستثناءات المناسبة، كما هو موضح في التعليمات البرمجية المتوفرة، لمعالجة المشكلات المحتملة.

### س3: هل هناك إصدار تجريبي متاح لـ Aspose.CAD لـ .NET؟

 ج3: نعم، يمكنك استكشاف المنتج من خلال النسخة التجريبية المجانية. يزور[هنا](https://releases.aspose.com/) للمزيد من المعلومات.

### س4: أين يمكنني طلب المساعدة أو مناقشة المشكلات المتعلقة بـ Aspose.CAD لـ .NET؟

 ج4: توجه إلى[منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19) لدعم المجتمع والمناقشات.

### س5: كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.CAD لـ .NET؟

 ج5: زيارة[هذا الرابط](https://purchase.aspose.com/temporary-license/)للحصول على ترخيص مؤقت لاحتياجات التطوير الخاصة بك.