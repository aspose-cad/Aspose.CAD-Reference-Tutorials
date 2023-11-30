---
title: تحويل رسم CAD إلى صورة نقطية في Aspose.CAD لـ .NET
linktitle: تحويل رسم CAD إلى صورة نقطية
second_title: Aspose.CAD .NET - تنسيق ملف CAD وBIM
description: استكشف العملية السلسة لتحويل رسومات CAD إلى صور نقطية في .NET باستخدام Aspose.CAD. أطلق العنان لسير العمل الفعال وحسّن مشاريع التصميم بمساعدة الكمبيوتر الخاصة بك دون عناء.
type: docs
weight: 11
url: /ar/net/cad-drawing-manipulation/convert-cad-drawing-to-raster-image/
---
## مقدمة

في مشهد التصميم بمساعدة الكمبيوتر (CAD) المتطور باستمرار، تعد الحاجة إلى تحويل رسومات CAD بسلاسة إلى صور نقطية أمرًا بالغ الأهمية. يستكشف هذا الدليل خطوة بخطوة كيفية تحقيق ذلك باستخدام مكتبة Aspose.CAD لـ .NET القوية. يعمل Aspose.CAD على تبسيط العملية، حيث يوفر للمطورين مجموعة قوية من الأدوات لتحسين سير العمل المتعلق بالتصميم بمساعدة الكمبيوتر (CAD).

## المتطلبات الأساسية

قبل الغوص في البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:

1.  Aspose.CAD لمكتبة .NET: قم بتنزيل وتثبيت مكتبة Aspose.CAD من[صفحة التحميل](https://releases.aspose.com/cad/net/).

2. بيئة التطوير: قم بإعداد بيئة تطوير عمل باستخدام IDE متوافق لتطوير .NET.

## استيراد مساحات الأسماء

في مشروع .NET الخاص بك، قم باستيراد مساحات الأسماء الضرورية للوصول إلى وظائف Aspose.CAD. أضف ما يلي في بداية ملف التعليمات البرمجية الخاص بك:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## الخطوة 1: تحديد مسارات الملفات

```csharp
// المسار إلى دليل المستندات.
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
```

تأكد من استبدال "دليل المستندات الخاص بك" بالمسار الفعلي لملف CAD الخاص بك.

## الخطوة 2: تحميل رسم CAD

```csharp
using (Aspose.CAD.Image image = Aspose.CAD.Image.Load(sourceFilePath))
{
```

تعمل هذه الخطوة على تهيئة كائن الصورة Aspose.CAD وتحميل رسم CAD من مسار الملف المحدد.

## الخطوة 3: تكوين خيارات التنقيط

```csharp
// قم بإنشاء مثيل لـ CadRasterizationOptions
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
// ضبط عرض الصفحة وارتفاعها
rasterizationOptions.PageWidth = 1200;
rasterizationOptions.PageHeight = 1200;
```

هنا، قمنا بإعداد خيارات التنقيط، وتحديد عرض وارتفاع صفحة الإخراج.

## الخطوة 4: إنشاء PngOptions للصورة الناتجة

```csharp
// قم بإنشاء مثيل PngOptions للصورة الناتجة
ImageOptionsBase options = new Aspose.CAD.ImageOptions.PngOptions();
// ضبط خيارات التنقيط
options.VectorRasterizationOptions = rasterizationOptions;
```

تتضمن هذه الخطوة تكوين خيارات للصورة الناتجة، وتحديد خيارات التنقيط المحددة مسبقًا.

## الخطوة 5: حفظ الصورة الناتجة

```csharp
MyDir = MyDir + "conic_pyramid_raster_image_out.png";
// حفظ الصورة الناتجة
image.Save(MyDir, options);
```

احفظ الصورة النقطية المحولة في مسار ملف الإخراج المحدد.

## الخطوة 6: عرض رسالة النجاح

```csharp
// ExEnd: تحويل الرسم إلى الصورة النقطية
Console.WriteLine("\nCAD drawing converted successfully to raster image format.\nFile saved at " + MyDir);
```

عرض رسالة نجاح تشير إلى إتمام عملية التحويل.

## خاتمة

في هذا البرنامج التعليمي، استكشفنا العملية خطوة بخطوة لتحويل رسم CAD إلى صورة نقطية باستخدام مكتبة Aspose.CAD for .NET. بفضل ميزاته القوية وسهولة التكامل، يعمل Aspose.CAD على تمكين المطورين من تبسيط سير عمل CAD الخاص بهم دون عناء.

## الأسئلة الشائعة

### س1: هل Aspose.CAD متوافق مع جميع تنسيقات ملفات CAD؟

 ج1: يدعم Aspose.CAD نطاقًا واسعًا من تنسيقات ملفات CAD، بما في ذلك DWG وDXF وDGN والمزيد. الرجوع إلى[توثيق](https://reference.aspose.com/cad/net/) للحصول على قائمة شاملة.

### س2: هل يمكنني تخصيص خيارات التنقيط لمشاريع مختلفة؟

ج2: نعم، يسمح Aspose.CAD بالتخصيص الشامل لخيارات التنقيط، مما يمكّن المطورين من تخصيص المخرجات بناءً على متطلبات المشروع.

### س3: هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.CAD؟

 ج3: نعم، يمكنك استكشاف ميزات Aspose.CAD من خلال النسخة التجريبية المجانية. يزور[هنا](https://releases.aspose.com/) للبدء.

### س4: كيف يمكنني الحصول على الدعم لـ Aspose.CAD؟

 ج4: للحصول على أي مساعدة أو استفسارات، قم بزيارة Aspose.CAD[منتدى الدعم](https://forum.aspose.com/c/cad/19).

### س5: هل التراخيص المؤقتة متاحة لـ Aspose.CAD؟
 
ج5: نعم، يمكن للمطورين الحصول على تراخيص مؤقتة لـ Aspose.CAD من[هذا الرابط](https://purchase.aspose.com/temporary-license/).