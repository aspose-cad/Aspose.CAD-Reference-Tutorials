---
title: تحويل التخطيطات إلى صورة نقطية في Aspose.CAD لـ .NET
linktitle: تحويل التخطيطات إلى صورة نقطية
second_title: Aspose.CAD .NET - تنسيق ملف CAD وBIM
description: قم بتحويل تخطيطات CAD بسهولة إلى صور نقطية باستخدام Aspose.CAD لـ .NET. عزز تطويرك من خلال إمكانات معالجة CAD القوية.
type: docs
weight: 12
url: /ar/net/cad-drawing-manipulation/convert-layouts-to-raster-image/
---
## مقدمة

هل تتطلع إلى تحويل التخطيطات بسهولة إلى صور نقطية في تطبيقات .NET الخاصة بك؟ لا مزيد من البحث! سيرشدك هذا الدليل خطوة بخطوة خلال العملية باستخدام Aspose.CAD for .NET، وهي مكتبة قوية تعمل على تبسيط مهام التصميم بمساعدة الكمبيوتر (CAD).

## المتطلبات الأساسية

قبل الغوص في البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:

- Aspose.CAD for .NET Library: قم بتنزيل المكتبة وتثبيتها من ملف[صفحة تنزيل Aspose.CAD لـ .NET](https://releases.aspose.com/cad/net/).

- بيئة التطوير: تأكد من أن لديك بيئة تطوير .NET عاملة تم إعدادها على جهازك.

- المستند المراد تحويله: قم بإعداد مستند CAD يحتوي على التخطيطات التي تريد تحويلها إلى صور نقطية.

- دليل المستندات الخاص بك: استبدل العنصر النائب "دليل المستندات الخاص بك" في التعليمات البرمجية بالمسار إلى دليل المستند الخاص بك.

## استيراد مساحات الأسماء

أولاً، لنستورد مساحات الأسماء الضرورية لتسهيل الوصول إلى وظائف Aspose.CAD في التعليمات البرمجية الخاصة بك.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## الخطوة 1: قم بتحميل مستند CAD

ابدأ بتحميل مستند CAD باستخدام مكتبة Aspose.CAD.

```csharp
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image image = Image.Load(sourceFilePath))
{
    //سيتم وضع الرمز الخاص بك لمزيد من الخطوات هنا
}
```

## الخطوة 2: تكوين خيارات التنقيط

 إنشاء مثيل ل`CadRasterizationOptions` لتعيين عرض الصفحة وارتفاعها وتحديد التخطيطات التي تريد تحويلها.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1200;
rasterizationOptions.PageHeight = 1200;
rasterizationOptions.Layouts = new string[] { "Model", "Layout1" };
```

## الخطوة 3: إعداد TiffOptions للصورة الناتجة

 إنشاء مثيل ل`TiffOptions`لتحديد تنسيق الصورة الناتجة.

```csharp
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.VectorRasterizationOptions = rasterizationOptions;
```

## الخطوة 4: احفظ الصورة الناتجة

حدد مسار الإخراج واحفظ الصورة المحولة.

```csharp
string outputFilePath = MyDir + "conic_pyramid_layoutstorasterimage_out.tiff";
image.Save(outputFilePath, options);
```

## خاتمة

تهانينا! لقد نجحت في تحويل تخطيطات CAD إلى تنسيق صورة نقطية باستخدام Aspose.CAD لـ .NET. الإمكانيات هائلة، وهذا الدليل بمثابة نقطة انطلاق لمساعيك المتعلقة بالتصميم بمساعدة الكمبيوتر (CAD).

## الأسئلة الشائعة

### س1: هل Aspose.CAD متوافق مع جميع تنسيقات CAD؟

 A1: يدعم Aspose.CAD نطاقًا واسعًا من تنسيقات CAD، بما في ذلك DWG وDXF وDWF وSTL والمزيد. افحص ال[توثيق](https://reference.aspose.com/cad/net/) للحصول على قائمة شاملة.

### س2: كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.CAD؟

 ج2: قم بزيارة[صفحة الترخيص المؤقتة](https://purchase.aspose.com/temporary-license/) للحصول على ترخيص مؤقت لأغراض الاختبار والتقييم.

### س3: أين يمكنني العثور على الدعم لـ Aspose.CAD؟

 ج3: تعتبر المنتديات مكانًا رائعًا لطلب المساعدة. قم بزيارة[منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19) للتواصل مع المجتمع والحصول على المساعدة.

### س4: هل يمكنني تجربة Aspose.CAD مجانًا؟

 ج4: بالتأكيد! الاستيلاء على الخاص بك[تجربة مجانية](https://releases.aspose.com/) لاستكشاف ميزات وقدرات Aspose.CAD.

### س5: أين يمكنني شراء ترخيص Aspose.CAD؟

 ج5: انتقل إلى[صفحة الشراء](https://purchase.aspose.com/buy) لشراء ترخيص وفتح الإمكانات الكاملة لـ Aspose.CAD.