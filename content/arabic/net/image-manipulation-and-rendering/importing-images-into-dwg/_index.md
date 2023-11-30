---
title: استيراد الصور إلى ملفات DWG باستخدام C# - دليل Aspose.CAD
linktitle: استيراد الصور إلى ملفات DWG باستخدام C#
second_title: Aspose.CAD .NET - تنسيق ملف CAD وBIM
description: تعلم كيفية استيراد الصور إلى ملفات DWG باستخدام لغة C# مع Aspose.CAD لـ .NET. اتبع دليلنا خطوة بخطوة للتكامل السلس.
type: docs
weight: 11
url: /ar/net/image-manipulation-and-rendering/importing-images-into-dwg/
---
## مقدمة

في عالم التصميم بمساعدة الكمبيوتر (CAD)، يعد دمج الصور في ملفات DWG مهمة شائعة وحاسمة. يوفر Aspose.CAD for .NET مجموعة قوية من الأدوات لتبسيط هذه العملية، مما يجعلها في متناول مطوري C#. في هذا البرنامج التعليمي، سنستكشف كيفية استيراد الصور إلى ملفات DWG خطوة بخطوة.

## المتطلبات الأساسية

قبل الغوص في الدليل، تأكد من أن لديك ما يلي:

- المعرفة الأساسية ببرمجة C#.
-  تم تثبيت Aspose.CAD لـ .NET. يمكنك تنزيله[هنا](https://releases.aspose.com/cad/net/).
- تم إعداد بيئة التطوير.

## استيراد مساحات الأسماء

تأكد من تضمين مساحات الأسماء الضرورية في مشروع C# الخاص بك:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## الخطوة 1: قم بإعداد دليل المستندات الخاص بك

```csharp
string MyDir = "Your Document Directory";
```

## الخطوة 2: قم بتحميل ملف DWG

```csharp
string dwgPathToFile = MyDir + "Drawing11.dwg";
CadImage cadImage1 = (CadImage)Image.Load(dwgPathToFile);
```

## الخطوة 3: تحديد خصائص الصورة

```csharp
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.ObjectHandle = "A3B4";
```

## الخطوة 4: تعيين نقطة الإدراج والمتجهات

```csharp
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

## الخطوة 5: إنشاء وتكوين الصورة النقطية

```csharp
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.ImageDefReference = "A3B4";
cadRasterImage.DisplayFlags = 7;
cadRasterImage.ClippingState = 0;
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(639.5, 561.5));
```

## الخطوة 6: إضافة صورة إلى ملف DWG

```csharp
CadImage cadImage = (CadImage)cadImage1;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadRasterImage);

List<CadBaseObject> list = new List<CadBaseObject>(cadImage.Objects);
list.Add(cadRasterImageDef);
cadImage.Objects = list.ToArray();
```

## الخطوة 7: احفظ بصيغة PDF

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

## خاتمة

يعد دمج الصور في ملفات DWG باستخدام C# وAspose.CAD لـ .NET عملية سلسة، مما يمكّن المطورين من تحسين مشاريع CAD الخاصة بهم باستخدام العناصر المرئية دون عناء.

## الأسئلة الشائعة

### س1: هل يمكنني استخدام Aspose.CAD لـ .NET مع لغات البرمجة الأخرى؟

ج1: تم تصميم Aspose.CAD بشكل أساسي لـ .NET، لكن Aspose يوفر مكتبات لمختلف لغات البرمجة.

### س2: هل تتوفر نسخة تجريبية مجانية من Aspose.CAD لـ .NET؟

 ج2: نعم، يمكنك استكشاف النسخة التجريبية المجانية[هنا](https://releases.aspose.com/).

### س3: أين يمكنني العثور على الوثائق التفصيلية الخاصة بـ Aspose.CAD؟

 ج3: الوثائق متاحة[هنا](https://reference.aspose.com/cad/net/).

### س4: كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.CAD لـ .NET؟

 ج4: زيارة[هذا الرابط](https://purchase.aspose.com/temporary-license/) للحصول على ترخيص مؤقت.

### س5: هل توجد منتديات مجتمعية لدعم Aspose.CAD؟

 ج5: نعم، يمكنك طلب الدعم والتفاعل مع المجتمع[هنا](https://forum.aspose.com/c/cad/19).