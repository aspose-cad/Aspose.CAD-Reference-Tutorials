---
title: تصدير الصور ثلاثية الأبعاد إلى PDF - البرنامج التعليمي Aspose.CAD
linktitle: تصدير الصور ثلاثية الأبعاد إلى PDF
second_title: Aspose.CAD .NET - تنسيق ملف CAD وBIM
description: قم بتحويل صور CAD ثلاثية الأبعاد بسهولة إلى PDF باستخدام Aspose.CAD لـ .NET. اتبع برنامجنا التعليمي خطوة بخطوة لتصدير ملفات PDF بسلاسة.
weight: 10
url: /ar/net/3d-image-export/exporting-3d-images-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تصدير الصور ثلاثية الأبعاد إلى PDF - البرنامج التعليمي Aspose.CAD

## مقدمة

هل تتطلع إلى تصدير الصور ثلاثية الأبعاد إلى PDF بسلاسة باستخدام Aspose.CAD لـ .NET؟ سيرشدك هذا البرنامج التعليمي خطوة بخطوة خلال العملية، مما يضمن الاستفادة من قوة Aspose.CAD لتحويل صورك ثلاثية الأبعاد إلى تنسيق PDF بسهولة.

## المتطلبات الأساسية

قبل الغوص في البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:

-  Aspose.CAD لـ .NET: تأكد من تثبيت مكتبة Aspose.CAD لـ .NET. إذا لم يكن الأمر كذلك، يمكنك تنزيله من[صفحة تنزيل Aspose.CAD لـ .NET](https://releases.aspose.com/cad/net/).

- دليل المستندات: قم بإعداد دليل حيث يتم تخزين ملفات CAD الخاصة بك، ولاحظ المسار.

## استيراد مساحات الأسماء

في مشروع .NET الخاص بك، قم باستيراد مساحات الأسماء الضرورية للعمل مع Aspose.CAD. أضف الأسطر التالية إلى أعلى ملف التعليمات البرمجية الخاص بك:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

## الخطوة 1: قم بتحميل صورة CAD

 ابدأ بتحميل صورة CAD التي تريد تصديرها إلى PDF. استخدم ال`Load` الطريقة من مكتبة Aspose.CAD. يستبدل`"conic_pyramid.dxf"` مع المسار إلى ملف CAD الخاص بك.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image cadImage = Image.Load(sourceFilePath))
{
    // الكود الخاص بك لتحميل صورة CAD موجود هنا
}
```

## الخطوة 2: تكوين خيارات التنقيط

 قم بتكوين خيارات التنقيط لصورة CAD. قم بتعيين المعلمات مثل عرض الصفحة وارتفاع الصفحة والتخطيطات. قم بإلغاء التعليق على السطر المتعلق بـ`TypeOfEntities` إذا كانت كياناتك ثلاثية الأبعاد.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
// rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;

rasterizationOptions.Layouts = new string[] { "Model" };
```

## الخطوة 3: ضبط خيارات PDF

قم بإنشاء خيارات PDF وربطها بخيارات التنقيط.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## الخطوة 4: احفظ بصيغة PDF

احفظ صورة CAD كملف PDF باستخدام الخيارات التي تم تكوينها. حدد مسار الإخراج لملف PDF.

```csharp
MyDir = MyDir + "Export3DImagestoPDF_out.pdf";
cadImage.Save(MyDir, pdfOptions);
```

## خاتمة

تهانينا! لقد نجحت في تصدير صور ثلاثية الأبعاد إلى PDF باستخدام Aspose.CAD لـ .NET. يضمن هذا البرنامج التعليمي المباشر إمكانية تحويل ملفات CAD الخاصة بك بسهولة إلى تنسيق يسهل الوصول إليه.

## الأسئلة الشائعة

### س1: هل Aspose.CAD متوافق مع جميع تنسيقات ملفات CAD؟

ج1: نعم، يدعم Aspose.CAD نطاقًا واسعًا من تنسيقات CAD، مما يضمن المرونة في التعامل مع أنواع الملفات المختلفة.

### س2: هل يمكنني تخصيص أبعاد الصفحة عند التصدير إلى PDF؟

ج2: بالتأكيد. يوضح البرنامج التعليمي كيفية تكوين عرض الصفحة وارتفاعها وفقًا لمتطلباتك.

### س3: هل التراخيص المؤقتة متاحة لـ Aspose.CAD؟

 ج3: نعم، يمكنك الحصول على تراخيص مؤقتة لـ Aspose.CAD من خلال زيارة الموقع[ترخيص مؤقت](https://purchase.aspose.com/temporary-license/).

### س4: أين يمكنني العثور على دعم إضافي أو مناقشات مجتمعية؟

 ج4: توجه إلى[منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19) من أجل الدعم والتفاعل مع المجتمع.

### س5: هل تتوفر نسخة تجريبية مجانية من Aspose.CAD؟

 ج5: نعم، يمكنك استكشاف ميزات Aspose.CAD عن طريق الوصول إلى ملف[تجربة مجانية](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
