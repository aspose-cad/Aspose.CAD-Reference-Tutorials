---
date: 2026-08-17
description: تعلم كيفية إضافة صورة إلى ملفات DWG باستخدام C# و Aspose.CAD لـ .NET.
  يشرح هذا الدليل خطوات استيراد الصور، وتحديد نقاط الإدراج، وتصديرها إلى PDF.
keywords:
- add image to dwg
- convert dwg to pdf
- set insertion point dwg
- embed png in dwg
- save dwg as pdf
lastmod: 2026-08-17
linktitle: استيراد الصور إلى ملفات DWG باستخدام C#
og_description: تعلم كيفية إضافة صورة إلى ملفات DWG باستخدام C#. يغطي هذا البرنامج
  التعليمي استيراد الصور، وتحديد نقاط الإدراج، وتحويل DWG إلى PDF باستخدام Aspose.CAD.
og_image_alt: Guide showing C# code to embed an image into a DWG file using Aspose.CAD
og_title: كيفية إضافة صورة إلى ملفات DWG باستخدام C# و Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-08-17'
  description: Learn how to add image to dwg files using C# and Aspose.CAD for .NET.
    This guide walks you through importing images, setting insertion points, and exporting
    to PDF.
  headline: How to add image to dwg files with C# using Aspose.CAD
  type: TechArticle
- description: Learn how to add image to dwg files using C# and Aspose.CAD for .NET.
    This guide walks you through importing images, setting insertion points, and exporting
    to PDF.
  name: How to add image to dwg files with C# using Aspose.CAD
  steps:
  - name: set up your document directory
    text: Prepare the folder that contains the source DWG and the image you want to
      embed.
  - name: load the dwg file
    text: The `CadImage` class represents a DWG drawing and provides access to its
      entities, layers, and metadata.
  - name: define the image properties
    text: Create an `Image` object that points to the raster file (e.g., PNG) and
      specify its format.
  - name: set insertion point dwg and vectors
    text: Specify where the image should appear inside the drawing and how it should
      be scaled. The insertion point is defined by a 2‑D coordinate, while the vectors
      control width and height.
  - name: create and configure the raster image
    text: Instantiate a `RasterImage` object, assign the image data, and set any additional
      rendering options.
  - name: add image to dwg file
    text: Insert the configured raster image into the DWG’s entities collection so
      it becomes part of the drawing.
  - name: save as pdf (export dwg to pdf)
    text: After embedding the image you can **convert dwg to pdf** or **save dwg as
      pdf** with a single call. This is useful for sharing the drawing with stakeholders
      who don’t have CAD software.
  type: HowTo
- questions:
  - answer: The core library is .NET‑specific, but Aspose offers equivalent APIs for
      Java, Python and other platforms.
    question: Can I use Aspose.CAD for .NET with other programming languages?
  - answer: Yes, you can explore a free trial on the [Aspose free trial page](https://releases.aspose.com/).
    question: Is a free trial available for Aspose.CAD?
  - answer: The documentation is available in the [Aspose.CAD .NET API reference](https://reference.aspose.com/cad/net/).
    question: Where can I find detailed documentation for Aspose.CAD?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to get a temporary license.
    question: How do I obtain a temporary license for Aspose.CAD?
  - answer: Yes, you can seek support and engage with the community in the [Aspose.CAD
      community forum](https://forum.aspose.com/c/cad/19).
    question: Are there community forums for Aspose.CAD support?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- CAD
- Aspose.CAD
- C# image processing
- DWG manipulation
title: كيفية إضافة صورة إلى ملفات DWG باستخدام C# و Aspose.CAD
url: /ar/net/image-manipulation-and-rendering/importing-images-into-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية إضافة صورة إلى ملفات DWG باستخدام C# و Aspose.CAD

## مقدمة

إضافة صورة إلى ملف DWG هي متطلب روتيني عندما تحتاج إلى إثراء رسومات CAD بالشعارات أو الصور أو الرسومات النقطية. في هذا البرنامج التعليمي ستتعلم كيفية **إضافة صورة إلى dwg** برمجيًا باستخدام C# و Aspose.CAD لـ .NET، ثم تحويل النتيجة إلى PDF اختياريًا. تم تقسيم الخطوات بحيث يمكنك نسخ‑لصق كل قسم في مشروعك الخاص.

## إجابات سريعة
- **أي مكتبة تتولى المهمة؟** Aspose.CAD for .NET.
- **هل يمكنني تضمين ملفات PNG؟** نعم – PNG، JPEG، BMP وغيرها من صيغ الرسومات النقطية مدعومة.
- **هل أحتاج إلى ترخيص للتطوير؟** نسخة تجريبية مجانية تعمل للاختبار؛ الترخيص التجاري مطلوب للإنتاج.
- **هل يدعم تصدير PDF؟** بالتأكيد – يمكنك تحويل DWG المحدث إلى PDF بسطر واحد.
- **ما إصدارات .NET المتوافقة؟** .NET Framework 4.6+، .NET Core 3.1+، .NET 5/6/7.

## ما هو ملف DWG؟

ملف DWG هو الصيغة الثنائية الأصلية لرسومات Autodesk AutoCAD، يخزن الهندسة المتجهة، الطبقات، وبيانات التعريف. يُستخدم على نطاق واسع في الهندسة المعمارية، الهندسة، والبناء، ويمكن لـ Aspose.CAD قراءة وكتابة هذه الصيغة دون الحاجة إلى تثبيت AutoCAD.

## لماذا إضافة صورة إلى dwg باستخدام Aspose.CAD؟

يدعم Aspose.CAD **أكثر من 50 صيغة إدخال وإخراج**، ويمكنه معالجة ملفات أكبر من 500 ميغابايت دون تحميل المستند بالكامل في الذاكرة، ويوفر API حتمي يعمل في بيئات الخوادم بدون واجهة رسومية. هذا يجعل معالجة دفعات من رسومات DWG سريعة وموثوقة.

## المتطلبات المسبقة
- معرفة أساسية ببرمجة C#.
- تم تثبيت Aspose.CAD لـ .NET. يمكنك تنزيله من [صفحة تنزيل Aspose.CAD لـ .NET](https://releases.aspose.com/cad/net/). يمكنك أيضًا استكشاف منتجات Aspose الأخرى على [صفحة إصدارات Aspose](https://releases.aspose.com/).
- بيئة تطوير مثل Visual Studio 2022 أو أحدث.

## كيفية إضافة صورة إلى dwg باستخدام Aspose.CAD؟

قم بتحميل ملف DWG الهدف، أنشئ كائن صورة نقطية يصف الصورة التي تريد تضمينها، حدد نقطة الإدراج والمتجهات الخاصة بالتحجيم، ثم أرفق الصورة بالرسم. أخيرًا، احفظ ملف DWG المعدل أو صدّره مباشرة إلى PDF. يتطلب سير العمل الكامل بضع نداءات API فقط ويستغرق أقل من ثانية للرسومات النموذجية ذات صفحتين.

### استيراد مساحات الأسماء
قم بتضمين مساحات الأسماء التي تعرض فئات CAD التي ستحتاجها.

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

### الخطوة 1: إعداد دليل المستند الخاص بك
قم بإعداد المجلد الذي يحتوي على ملف DWG المصدر والصورة التي تريد تضمينها.

```csharp
string MyDir = "Your Document Directory";
```

### الخطوة 2: تحميل ملف dwg
تمثل الفئة `CadImage` رسم DWG وتوفر الوصول إلى كياناتها، طبقاتها، وبيانات التعريف الخاصة بها.

```csharp
string dwgPathToFile = MyDir + "Drawing11.dwg";
CadImage cadImage1 = (CadImage)Image.Load(dwgPathToFile);
```

### الخطوة 3: تعريف خصائص الصورة
أنشئ كائن `Image` يشير إلى ملف الرسومات النقطية (مثل PNG) وحدد صيغته.

```csharp
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.ObjectHandle = "A3B4";
```

### الخطوة 4: تعيين نقطة الإدراج في dwg والمتجهات
حدد أين يجب أن تظهر الصورة داخل الرسم وكيفية تحجيمها. تُعرّف نقطة الإدراج بإحداثيات ثنائية الأبعاد، بينما تتحكم المتجهات في العرض والارتفاع.

```csharp
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

### الخطوة 5: إنشاء وتكوين صورة النقطية
أنشئ كائن `RasterImage`، عيّن بيانات الصورة، واضبط أي خيارات تصيير إضافية.

```csharp
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.ImageDefReference = "A3B4";
cadRasterImage.DisplayFlags = 7;
cadRasterImage.ClippingState = 0;
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(639.5, 561.5));
```

### الخطوة 6: إضافة صورة إلى ملف dwg
أدرج صورة النقطية المكوّنة في مجموعة الكيانات الخاصة بـ DWG لتصبح جزءًا من الرسم.

```csharp
CadImage cadImage = (CadImage)cadImage1;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadRasterImage);

List<CadBaseObject> list = new List<CadBaseObject>(cadImage.Objects);
list.Add(cadRasterImageDef);
cadImage.Objects = list.ToArray();
```

### الخطوة 7: حفظ كـ pdf (تصدير dwg إلى pdf)
بعد تضمين الصورة يمكنك **تحويل dwg إلى pdf** أو **حفظ dwg كـ pdf** باستدعاء واحد. هذا مفيد لمشاركة الرسم مع أصحاب المصلحة الذين لا يمتلكون برنامج CAD.

```csharp
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;

cadRasterizationOptions.PageHeight = 1600;
cadRasterizationOptions.PageWidth = 1600;
cadRasterizationOptions.Layouts = new string[] { "Model" };
cadImage1.Save(MyDir + "export2.pdf", pdfOptions);
```

## كيفية تحويل dwg إلى pdf بعد تضمين صورة؟

استدعِ طريقة `Save` على كائن `CadImage`، مع تمرير `SaveFormat.Pdf` واختيارياً كائن `PdfOptions` للتحكم في حجم الصفحة، الرستر، وبيانات التعريف. يحافظ Aspose.CAD على الصورة النقطية المضمّنة، الطبقات، وسمك الخطوط، منتجًا تمثيل PDF دقيق يمكن فتحه في أي عارض. يتم تنفيذ هذا التحويل بسطر واحد من الشيفرة.

## المشكلات الشائعة والحلول
- **الصورة تظهر في الموقع الخطأ** – تحقق مرة أخرى من إحداثيات نقطة الإدراج والمتجهات الاتجاهية؛ فهي نسبية إلى أصل الرسم.
- **الصور الكبيرة تسبب ارتفاعًا في استهلاك الذاكرة** – استخدم خيار `Resize` على صورة النقطية قبل الإدراج، أو اعمل بنسخة ذات دقة أقل.
- **تصدير PDF يفقد جودة المتجهات** – تأكد من حفظك باستخدام `PdfOptions` التي تحتفظ ببيانات المتجهات؛ صور النقطية تُضمّن دائمًا كما هي.

## الأسئلة المتكررة

**س: هل يمكنني استخدام Aspose.CAD لـ .NET مع لغات برمجة أخرى؟**  
ج: المكتبة الأساسية مخصصة لـ .NET، لكن Aspose تقدم واجهات برمجة تطبيقات مكافئة لـ Java و Python وغيرها من المنصات.

**س: هل تتوفر نسخة تجريبية مجانية لـ Aspose.CAD؟**  
ج: نعم، يمكنك تجربة نسخة تجريبية مجانية على [صفحة تجربة Aspose المجانية](https://releases.aspose.com/).

**س: أين يمكنني العثور على وثائق مفصلة لـ Aspose.CAD؟**  
ج: الوثائق متاحة في [مرجع Aspose.CAD .NET API](https://reference.aspose.com/cad/net/).

**س: كيف أحصل على ترخيص مؤقت لـ Aspose.CAD؟**  
ج: زر [صفحة الترخيص المؤقت](https://purchase.aspose.com/temporary-license/) للحصول على ترخيص مؤقت.

**س: هل توجد منتديات مجتمع لدعم Aspose.CAD؟**  
ج: نعم، يمكنك طلب الدعم والتفاعل مع المجتمع في [منتدى مجتمع Aspose.CAD](https://forum.aspose.com/c/cad/19).

---

**Last Updated:** 2026-08-17  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose

## دروس ذات صلة

- [تصدير DWG إلى PDF أو صور نقطية - دليل Aspose.CAD](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [تصدير DWG إلى تنسيق DXF في C# - درس Aspose.CAD](/cad/net/advanced-export-techniques/exporting-dwg-to-dxf/)
- [تصدير تخطيطات محددة إلى PDF - دليل Aspose.CAD](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}