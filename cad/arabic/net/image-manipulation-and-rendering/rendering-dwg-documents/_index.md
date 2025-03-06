---
title: عرض مستندات DWG في C# - دليل Aspose.CAD
linktitle: عرض مستندات DWG بلغة C#
second_title: Aspose.CAD .NET - تنسيق ملف CAD وBIM
description: تعرف على كيفية عرض مستندات DWG في لغة C# باستخدام Aspose.CAD. يغطي هذا الدليل خطوة بخطوة الاستيراد والتكوين والحفظ باستخدام أمثلة التعليمات البرمجية.
weight: 17
url: /ar/net/image-manipulation-and-rendering/rendering-dwg-documents/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# عرض مستندات DWG في C# - دليل Aspose.CAD

## مقدمة

مرحبًا بك في الدليل الشامل حول عرض مستندات DWG بلغة C# باستخدام Aspose.CAD. سواء كنت مطورًا متمرسًا أو بدأت للتو في استخدام .NET، فسيرشدك هذا البرنامج التعليمي خلال عملية الاستفادة من Aspose.CAD لعرض ملفات DWG بكفاءة. Aspose.CAD عبارة عن واجهة برمجة تطبيقات قوية توفر وظائف قوية للعمل مع تنسيقات ملفات CAD، مما يجعلها خيارًا مفضلاً للمطورين الذين يتعاملون مع ملفات DWG.

## المتطلبات الأساسية

قبل الغوص في البرنامج التعليمي، تأكد من أن لديك المتطلبات الأساسية التالية:

- المعرفة الأساسية بلغة البرمجة C#.
- تم تثبيت Visual Studio على جهازك.
-  مكتبة Aspose.CAD مدمجة في مشروعك. يمكنك تنزيله من[هنا](https://releases.aspose.com/cad/net/).
- نموذج لملف DWG، مثل "Bottom_plate.dwg"، للمتابعة مع الأمثلة.

## استيراد مساحات الأسماء

للبدء، تأكد من استيراد مساحات الأسماء الضرورية في بداية كود C# الخاص بك:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.FileFormats.Cad;
```

الآن، دعونا نقسم المثال المقدم إلى خطوات متعددة:

## الخطوة 1: قم بتحميل ملف DWG

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // الكود الخاص بك لتحميل ملف DWG موجود هنا.
}
```

## الخطوة 2: تكوين خيارات التنقيط

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };
rasterizationOptions.NoScaling = true;
//يمكن إضافة تكوينات تنقيط إضافية هنا.
```

## الخطوة 3: تحديد المنطقة المراد رسمها

```csharp
Point topLeft = new Point(6156, 7053);
double width = 3108;
double height = 2489;
```

## الخطوة 4: إنشاء إطار عرض جديد

```csharp
CadVportTableObject newView = new CadVportTableObject();
newView.Name.Value = "*Active";
newView.CenterPoint.X = topLeft.X + width / 2f;
newView.CenterPoint.Y = topLeft.Y - height / 2f;
newView.ViewHeight.Value = height;
newView.ViewAspectRatio.Value = width / height;
```

## الخطوة 5: استبدال إطار العرض النشط

```csharp
for (int i = 0; i < cadImage.ViewPorts.Count; i++)
{
    CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
    if ((currentView.Name.Value == null && cadImage.ViewPorts.Count == 1) ||
    string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
    {
        cadImage.ViewPorts[i] = newView;
        break;
    }
}
```

## الخطوة 6: تكوين خيارات PDF

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## الخطوة 7: احفظ ملف DWG المعروض بصيغة PDF

```csharp
cadImage.Save(MyDir, pdfOptions);
```

## خاتمة

تهانينا! لقد نجحت في تحويل مستند DWG إلى PDF باستخدام Aspose.CAD في C#. لا تتردد في استكشاف المزيد من الميزات وتخصيص الكود بناءً على متطلباتك المحددة.

## الأسئلة الشائعة

### س1: هل يمكنني استخدام Aspose.CAD مع تنسيقات ملفات CAD الأخرى؟

ج1: نعم، يدعم Aspose.CAD تنسيقات CAD المتنوعة، بما في ذلك DWG وDXF وDWF والمزيد.

### س2: هل Aspose.CAD متوافق مع .NET Core؟

ج2: نعم، Aspose.CAD متوافق مع كل من .NET Framework و.NET Core.

### س3: كيف يمكنني التعامل مع التخطيطات المختلفة في ملف DWG؟

 A3: يمكنك تحديد التخطيط المطلوب في`Layouts` ممتلكات`CadRasterizationOptions`.

### س 4: هل هناك أي اعتبارات ترخيص لاستخدام Aspose.CAD؟

 ج4: للحصول على تفاصيل الترخيص، قم بزيارة[هنا](https://purchase.aspose.com/buy).

### س5: أين يمكنني العثور على دعم إضافي؟

ج5: قم بزيارة[منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19) لدعم المجتمع والمناقشات.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
