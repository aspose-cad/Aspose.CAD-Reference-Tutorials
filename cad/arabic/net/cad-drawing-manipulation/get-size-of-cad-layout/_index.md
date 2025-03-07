---
title: احصل على حجم تخطيط CAD في Aspose.CAD لـ .NET
linktitle: احصل على حجم تخطيط CAD
second_title: Aspose.CAD .NET - تنسيق ملف CAD وBIM
description: تعرف على كيفية استرداد حجم تخطيط CAD في .NET باستخدام Aspose.CAD. اتبع دليلنا خطوة بخطوة لمعالجة ملفات CAD بكفاءة.
weight: 14
url: /ar/net/cad-drawing-manipulation/get-size-of-cad-layout/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# احصل على حجم تخطيط CAD في Aspose.CAD لـ .NET

## مقدمة

مرحبًا بك في هذا الدليل الشامل حول الحصول على حجم تخطيطات CAD باستخدام Aspose.CAD لـ .NET. Aspose.CAD هي مكتبة قوية تمكن المطورين من العمل مع ملفات CAD بسلاسة. في هذا البرنامج التعليمي، سنرشدك خلال عملية استرداد حجم تخطيطات CAD باستخدام أمثلة عملية وتعليمات خطوة بخطوة.

## المتطلبات الأساسية

قبل أن نتعمق في البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:

-  Aspose.CAD لـ .NET: تأكد من تثبيت مكتبة Aspose.CAD. يمكنك تنزيله من[صفحة تنزيل Aspose.CAD لـ .NET](https://releases.aspose.com/cad/net/).

- ملفات المستندات: قم بإعداد ملفات CAD التي تريد العمل بها. يستخدم هذا البرنامج التعليمي "conic_pyramid.dxf" و"Bottom_plate.dwg" كأمثلة.

الآن، دعونا نبدأ!

## استيراد مساحات الأسماء

في مشروع .NET الخاص بك، ابدأ باستيراد مساحات الأسماء الضرورية:

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.ImageOptions;
```

## الخطوة 1: إعداد دليل المستندات

 قم بتعيين المسار إلى دليل المستند الخاص بك. يستبدل`"Your Document Directory"` مع المسار الفعلي

```csharp
string MyDir = "Your Document Directory";
```

## الخطوة 2: تحديد مسارات ملفات CAD

حدد مجموعة من مسارات ملفات CAD التي تريد تحليلها. في هذا المثال، نستخدم "conic_pyramid.dxf" و"Bottom_plate.dwg."

```csharp
string[] sourceFilePaths = new[]
{
    MyDir + "conic_pyramid.dxf",
    MyDir + "Bottom_plate.dwg"
};
```

## الخطوة 3: التكرار من خلال ملفات CAD

قم بالتكرار خلال كل ملف CAD واسترجاع معلومات التخطيط.

```csharp
foreach (var sourceFilePath in sourceFilePaths)
{
    string extension = Path.GetExtension(sourceFilePath);
    using (CadImage cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath))
    {
        // ... (انتقل إلى الخطوة التالية)
    }
}
```

## الخطوة 4: احصل على تخطيطات غير فارغة

حدد طريقة مساعدة للحصول على تخطيطات غير فارغة بناءً على نوع ملف CAD.

```csharp
private static List<string> GetNotEmptyLayouts(Image cadImage, string extension)
{
    // ... (انتقل إلى الخطوة التالية)
}
```

## الخطوة 5: الحصول على تخطيطات لملفات DWG

قم بتنفيذ المنطق لاسترداد التخطيطات غير الفارغة لملفات DWG.

```csharp
private static List<string> GetNotEmptyLayoutsForDwg(CadImage cadImage)
{
    // ... (انتقل إلى الخطوة التالية)
}
```

## الخطوة 6: الحصول على تخطيطات لملفات DXF

قم بتنفيذ المنطق لاسترداد التخطيطات غير الفارغة لملفات DXF.

```csharp
private static List<string> GetNotEmptyLayoutsForDxf(CadImage cadImage)
{
    // ... (انتقل إلى الخطوة التالية)
}
```

## الخطوة 7: استرداد حجم التخطيط وحفظه كصورة

أكمل عملية الحصول على حجم التخطيط وحفظه كصورة.

```csharp
foreach (string layout in layouts)
{
    // ... (انتقل إلى الخطوة التالية)
}
```

## خاتمة

تهانينا! لقد تعلمت بنجاح كيفية الحصول على حجم تخطيطات CAD باستخدام Aspose.CAD لـ .NET. غطى هذا البرنامج التعليمي الخطوات الأساسية، بدءًا من إعداد مشروعك وحتى استرداد معلومات التخطيط وحفظها كصورة. يمكنك الآن دمج هذه المعرفة في تطبيقات .NET الخاصة بك لمعالجة ملفات CAD بكفاءة.

## الأسئلة الشائعة

### س1: هل Aspose.CAD متوافق مع جميع تنسيقات ملفات CAD؟

A1: نعم، يدعم Aspose.CAD تنسيقات ملفات CAD المتنوعة، بما في ذلك DWG وDXF.

### س2: هل يمكنني تخصيص خيارات حفظ الصورة؟

ج2: بالتأكيد! يمكنك ضبط خيارات الصورة، مثل التنسيق والدقة، لتلبية متطلباتك المحددة.

### س3: أين يمكنني العثور على وثائق إضافية؟

 ج3: راجع[وثائق Aspose.CAD](https://reference.aspose.com/cad/net/) للحصول على معلومات وأمثلة مفصلة.

### س4: هل هناك نسخة تجريبية مجانية متاحة؟

 ج4: نعم، يمكنك استكشاف Aspose.CAD باستخدام ملف[تجربة مجانية](https://releases.aspose.com/).

### س5؛ كيف يمكنني الحصول على الدعم الفني؟

 ج5: للحصول على الدعم الفني، قم بزيارة[منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
