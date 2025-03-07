---
title: تحويل DWG إلى PDF مع الإحداثيات في C# - البرنامج التعليمي Aspose.CAD
linktitle: تحويل DWG إلى PDF مع الإحداثيات في C#
second_title: Aspose.CAD .NET - تنسيق ملف CAD وBIM
description: تعرف على كيفية تحويل DWG إلى PDF بإحداثيات محددة في لغة C# باستخدام Aspose.CAD. اتبع دليلنا خطوة بخطوة للحصول على تحويلات ملفات CAD دقيقة وفعالة.
weight: 11
url: /ar/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تحويل DWG إلى PDF مع الإحداثيات في C# - البرنامج التعليمي Aspose.CAD

## مقدمة

مرحبًا بك في هذا البرنامج التعليمي الشامل حول تحويل ملفات DWG إلى PDF بإحداثيات محددة باستخدام Aspose.CAD لـ .NET. Aspose.CAD هي مكتبة قوية تتيح للمطورين العمل مع تنسيقات ملفات CAD في تطبيقات .NET الخاصة بهم بسلاسة. في هذا البرنامج التعليمي، سنرشدك خلال عملية تحويل ملف DWG إلى PDF مع توفير إحداثيات محددة لتحسين الدقة.

## المتطلبات الأساسية

قبل أن نبدأ، تأكد من توفر المتطلبات الأساسية التالية:

- مكتبة Aspose.CAD: قم بتنزيل وتثبيت مكتبة Aspose.CAD لـ .NET. يمكنك العثور على المكتبة[هنا](https://releases.aspose.com/cad/net/).

- بيئة التطوير: تأكد من إعداد بيئة تطوير متوافقة، بما في ذلك Visual Studio أو أي بيئة تطوير متكاملة مفضلة أخرى.

- ملف DWG: احصل على ملف DWG جاهز للتحويل. يمكنك استخدام ملف المثال المقدم أو ملف DWG المخصص الخاص بك.

## استيراد مساحات الأسماء

في مشروع C# الخاص بك، قم باستيراد مساحات الأسماء الضرورية:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadParameters;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.ImageOptions;
```

دعنا نقسم الكود إلى دليل خطوة بخطوة لفهم أفضل:

## الخطوة 1: تحديد دليل المستندات

```csharp
string MyDir = "Your Document Directory";
```

## الخطوة 2: قم بتعيين مسار ملف DWG المصدر

```csharp
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
```

## الخطوة 3: تحميل ملف DWG وتكوين خيارات التنقيط

```csharp
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
    rasterizationOptions.Layouts = new string[] { "Model" };
    rasterizationOptions.NoScaling = true;
```

## الخطوة 4: تحديد الإحداثيات ومنفذ العرض

```csharp
    Point topLeft = new Point(500, 1000);
    double width = 3108;
    double height = 2489;

    CadVportTableObject newView = new CadVportTableObject();
    newView.Name = new CadStringParameter();
    newView.Name.Init("*Active");
    newView.CenterPoint.X = topLeft.X + width / 2f;
    newView.CenterPoint.Y = topLeft.Y - height / 2f;
    newView.ViewHeight.Value = height;
    newView.ViewAspectRatio.Value = width / height;
```

## الخطوة 5: تطبيق إعدادات منفذ العرض

```csharp
    for (int i = 0; i < cadImage.ViewPorts.Count; i++)
    {
        CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
        if (cadImage.ViewPorts.Count == 1 || string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
        {
            cadImage.ViewPorts[i] = newView;
            break;
        }
    }
```

## الخطوة 6: تكوين خيارات PDF والتصدير

```csharp
    Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
    pdfOptions.VectorRasterizationOptions = rasterizationOptions;

    MyDir = MyDir + "ConvertDWGToPDFBySupplyingCoordinates_out.pdf";
    cadImage.Save(MyDir, pdfOptions);
}
```

## الخطوة 7: عرض رسالة النجاح

```csharp
Console.WriteLine("\nThe DWG file exported successfully to PDF.\nFile saved at " + MyDir);
```

## خاتمة

تهانينا! لقد نجحت في تحويل ملف DWG إلى PDF بإحداثيات محددة باستخدام Aspose.CAD لـ .NET. غطى هذا البرنامج التعليمي الخطوات الأساسية وقدم دليلاً واضحًا للمطورين.

## الأسئلة الشائعة

### س1: هل يمكنني استخدام Aspose.CAD مع تنسيقات ملفات CAD الأخرى؟

ج1: نعم، يدعم Aspose.CAD تنسيقات CAD المتنوعة، بما في ذلك DWG وDXF وDWF والمزيد.

### س2: كيف يمكنني معالجة الأخطاء أثناء عملية التحويل؟

ج2: تنفيذ آليات معالجة الأخطاء باستخدام كتل محاولة الالتقاط لالتقاط الاستثناءات وإدارتها.

### س 3: هل Aspose.CAD مناسب لكل من بيئات Windows وLinux؟

ج3: نعم، Aspose.CAD متوافق مع نظامي التشغيل Windows وLinux.

### س4: هل يمكنني تخصيص مخرجات PDF بشكل أكبر؟

ج4: بالتأكيد! استكشف الخيارات الشاملة التي يوفرها Aspose.CAD لتخصيص مخرجات PDF وفقًا لمتطلباتك المحددة.

### س5: أين يمكنني العثور على دعم إضافي أو مناقشات مجتمعية؟

ج5: قم بزيارة[منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19) لدعم المجتمع والمناقشات.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
