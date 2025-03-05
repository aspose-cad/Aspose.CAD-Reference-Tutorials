---
title: تصدير ملفات IFC إلى PNG - البرنامج التعليمي Aspose.CAD
linktitle: تصدير ملفات IFC إلى PNG
second_title: Aspose.CAD .NET - تنسيق ملف CAD وBIM
description: استكشف Aspose.CAD for .NET، وهو حل قوي للتحويل السلس من IFC إلى PNG. قم بالتنزيل الآن لمعالجة ملفات CAD بكفاءة.
type: docs
weight: 10
url: /ar/net/exporting-to-image-formats/exporting-ifc-files-to-png/
---
## مقدمة

في عالم التصميم بمساعدة الكمبيوتر (CAD) الديناميكي، يعد التحويل الفعال للملفات أمرًا بالغ الأهمية. يظهر Aspose.CAD for .NET كأداة قوية توفر إمكانات سلسة لتصدير ملفات IFC (فئات مؤسسة الصناعة) إلى تنسيق PNG. سيرشدك هذا البرنامج التعليمي خطوة بخطوة خلال العملية، مما يضمن تجربة سلسة مع Aspose.CAD.

## المتطلبات الأساسية

قبل الغوص في البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:

### 1. تركيب Aspose.CAD

 تأكد من تثبيت Aspose.CAD for .NET. يمكنك تنزيله من صفحة الإصدار[هنا](https://releases.aspose.com/cad/net/).

### 2. دليل المستندات

 قم بإنشاء دليل مخصص لمستنداتك. في المثال المقدم، المتغير`MyDir` يمثل دليل الوثيقة.

## استيراد مساحات الأسماء

الآن بعد أن قمت بإعداد المتطلبات الأساسية، فلنستورد مساحات الأسماء الضرورية في تطبيق .NET الخاص بك لاستخدام وظائف Aspose.CAD.

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using Aspose.CAD.FileFormats.Ifc;
```

## الخطوة 1: تحميل ملف IFC

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "example.ifc";
using (IfcImage cadImage = (IfcImage)Image.Load(sourceFilePath))
{
```

 في هذه الخطوة، نقوم بتهيئة ملف Aspose.CAD`IfcImage` كائن وتحميل ملف IFC فيه.

## الخطوة 2: تعيين خيارات التنقيط

```csharp
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
   
    rasterizationOptions.PageWidth = 100;
    rasterizationOptions.PageHeight = 100;
```

حدد خيارات التنقيط لتكوين عرض الصفحة وارتفاعها لمخرجات PNG.

## الخطوة 3: تعيين خيارات PNG

```csharp
    PngOptions pngOptions = new PngOptions();
    pngOptions.VectorRasterizationOptions = rasterizationOptions;
```

قم بإنشاء خيارات PNG وربط خيارات التنقيط المحددة مسبقًا.

## الخطوة 4: تحديد مسار الإخراج

```csharp
    // قم بتعيين مسار الإخراج أيضًا
    string outPath = sourceFilePath + ".png";
    cadImage.Save(outPath, pngOptions);
}
```

حدد مسار الإخراج لملف PNG، مع التأكد من أنه يحمل نفس اسم الملف المصدر بامتداد ".png". وأخيرا، احفظ الصورة المحولة.

## خاتمة

من خلال هذه الخطوات المباشرة، تكون قد نجحت في تصدير ملف IFC إلى PNG باستخدام Aspose.CAD لـ .NET. تعمل هذه الأداة متعددة الاستخدامات على تبسيط عملية تحويل CAD، مما يجعلها في متناول المطورين والمهندسين.

## الأسئلة الشائعة

### س1: هل يمكنني استخدام Aspose.CAD لـ .NET على نظام التشغيل macOS أو Linux؟

A1: لا، تم تصميم Aspose.CAD for .NET خصيصًا لبيئات Windows.

### س2: هل الترخيص المؤقت متاح لأغراض الاختبار؟

 ج2: نعم، يمكنك الحصول على ترخيص مؤقت من[هنا](https://purchase.aspose.com/temporary-license/) للتقييم.

### س3: كيف يمكنني الحصول على الدعم لـ Aspose.CAD؟

 ج3: قم بزيارة[منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19) لدعم المجتمع والمناقشات.

### س4: أين يمكنني العثور على وثائق شاملة؟

 ج4: راجع[وثائق Aspose.CAD](https://reference.aspose.com/cad/net/) للحصول على معلومات وأمثلة مفصلة.

### س5: ماذا لو واجهت مشكلات أثناء التثبيت؟

 ج5: تحقق من الوثائق أو اطلب المساعدة بشأن[منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19).