---
date: 2026-08-23
description: تعلم كيفية إنشاء نافذة عرض dwg c# باستخدام Aspose.CAD. يغطي هذا الدليل
  تحميل ملف DWG، تكوين الرستر، تعريف نافذة العرض، وحفظ النتيجة كملف PDF.
keywords:
- create viewport dwg c#
- render dwg c#
- aspose.cad .net
lastmod: 2026-08-23
linktitle: تصيير مستندات DWG في C#
og_description: تعلم كيفية إنشاء نافذة عرض dwg c# باستخدام Aspose.CAD في .NET. يوضح
  هذا الدليل خطوة بخطوة عملية التحميل، التحويل إلى رستر، تعريف نوافذ العرض، وحفظها
  كملف PDF.
og_image_alt: Guide showing how to create viewport dwg c# with Aspose.CAD in .NET
og_title: كيفية إنشاء نافذة عرض dwg c# باستخدام Aspose.CAD لـ .NET
schemas:
- author: Aspose
  dateModified: '2026-08-23'
  description: Learn how to create viewport dwg c# using Aspose.CAD. This guide covers
    loading a DWG file, configuring rasterization, defining a viewport, and saving
    the result as PDF.
  headline: How to create viewport dwg c# with Aspose.CAD for .NET
  type: TechArticle
- questions:
  - answer: Load the DWG file with `CadImage.Load`.
    question: What is the first step?
  - answer: '`Viewport` inside `CadRasterizationOptions`.'
    question: Which class defines the view area?
  - answer: Yes, using `PdfOptions` after rasterization.
    question: Can I output to PDF?
  - answer: A commercial license is required; a free trial works for evaluation.
    question: Do I need a license for production?
  - answer: Absolutely – Aspose.CAD works with .NET Framework, .NET Core, and .NET 5/6.
    question: Is .NET Core supported?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- create viewport dwg c#
- Aspose.CAD
- C# CAD rendering
- DWG to PDF
- CAD viewports
title: كيفية إنشاء نافذة عرض dwg c# باستخدام Aspose.CAD لـ .NET
url: /ar/net/image-manipulation-and-rendering/rendering-dwg-documents/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# عرض مستندات DWG في C# – دليل إنشاء viewport dwg c#

## مقدمة

في هذا الدليل الشامل ستتعلم كيفية **إنشاء viewport dwg c#** باستخدام Aspose.CAD وعرض ملف DWG إلى PDF. سواء كنت تحتاج إلى استخراج تخطيط محدد، أو إنشاء ورقة قابلة للطباعة، أو تضمين عرض CAD في تقرير، فإن التحكم في الـ viewport يمنحك تحكمًا دقيقًا في عملية العرض. يدعم Aspose.CAD **أكثر من 20 تنسيق CAD** ويمكنه معالجة ملفات تحتوي على آلاف الكيانات دون تحميل المستند بالكامل إلى الذاكرة، مما يجعله مثاليًا لتطبيقات .NET عالية الأداء.

## إجابات سريعة
- **ما هي الخطوة الأولى؟** قم بتحميل ملف DWG باستخدام `CadImage.Load`.
- **أي فئة تحدد مساحة العرض؟** `Viewport` داخل `CadRasterizationOptions`.
- **هل يمكنني الإخراج إلى PDF؟** نعم، باستخدام `PdfOptions` بعد عملية الرستر.
- **هل أحتاج إلى ترخيص للإنتاج؟** يتطلب ترخيص تجاري؛ نسخة تجريبية مجانية تعمل للتقييم.
- **هل .NET Core مدعوم؟** بالتأكيد – Aspose.CAD يعمل مع .NET Framework و .NET Core و .NET 5/6.

## المتطلبات المسبقة

قبل الغوص في الشيفرة، تأكد من أن لديك:

- معرفة أساسية ببرمجة C#.
- Visual Studio (أي إصدار حديث) مثبت.
- مكتبة Aspose.CAD مضافة إلى مشروعك. يمكنك تنزيلها من [صفحة تنزيل Aspose.CAD](https://releases.aspose.com/cad/net/).
- ملف DWG تجريبي مثل **Bottom_plate.dwg** لتتبع الخطوات.

## استيراد المساحات الاسمية

أضف توجيهات `using` المطلوبة في أعلى ملف C# حتى يتمكن المترجم من العثور على أنواع Aspose.CAD.

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

الآن بعد أن تم إعداد البيئة، دعنا نتبع التنفيذ خطوة بخطوة.

## كيف تنشئ viewport dwg c#؟

لإنشاء viewport مخصص، قم أولاً بتحميل ملف DWG إلى كائن `CadImage`، ثم اضبط `CadRasterizationOptions` بالتخطيط والحجم المطلوبين. حدد المنطقة التي تريد عرضها، أنشئ كائن `CadVportTableObject` بالمركز والارتفاع ونسبة العرض إلى الارتفاع المحسوبة، استبدل الـ viewport النشط، اضبط أي خيارات PDF، وأخيرًا احفظ النتيجة.

## الخطوة 1: تحميل ملف dwg

`CadImage.Load` يحمل ملف DWG إلى كائن `CadImage`، الذي يمثل الرسم في الذاكرة.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for loading the DWG file goes here.
}
```

## الخطوة 2: ضبط خيارات الرستر

`CadRasterizationOptions` يحدد كيفية رستر الرسم، بما في ذلك اختيار التخطيط، والتحجيم، وحجم الإخراج.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };
rasterizationOptions.NoScaling = true;
// Additional rasterization configurations can be added here.
```

## الخطوة 3: تحديد المنطقة المراد رسمها

`Point` يحدد إحداثيات X و Y للزاوية العلوية اليسرى للمنطقة التي سيتم عرضها.

```csharp
Point topLeft = new Point(6156, 7053);
double width = 3108;
double height = 2489;
```

## الخطوة 4: إنشاء viewport جديد

`CadVportTableObject` يمثل كائن viewport يتحكم في المنطقة المرئية ونسبة العرض إلى الارتفاع للرسم المعروض.

```csharp
CadVportTableObject newView = new CadVportTableObject();
newView.Name.Value = "*Active";
newView.CenterPoint.X = topLeft.X + width / 2f;
newView.CenterPoint.Y = topLeft.Y - height / 2f;
newView.ViewHeight.Value = height;
newView.ViewAspectRatio.Value = width / height;
```

## الخطوة 5: استبدال الـ viewport النشط

الحلقة تستبدل الـ viewport النشط بالـ viewport الجديد لتطبيق إعدادات العرض المخصصة.

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

## الخطوة 6: ضبط خيارات PDF

`PdfOptions` يضبط معلمات إخراج PDF مثل الضغط والبيانات الوصفية.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## الخطوة 7: حفظ الـ dwg المعروض كملف PDF

`image.Save` يكتب الصورة المعروضة إلى ملف باستخدام خيارات التنسيق المحددة.

```csharp
cadImage.Save(MyDir, pdfOptions);
```

## لماذا نستخدم viewport مخصص عند عرض DWG؟

يسمح لك viewport مخصص بعزل تخطيط أو منطقة معينة، مما يقلل حجم الملف ويحسن سرعة العرض. يمكن لـ Aspose.CAD عرض ملف DWG مكوّن من 300 صفحة في أقل من ثانيتين عند استخدام viewport مركّز، مقارنةً بالعرض الكامل الذي قد يستغرق عدة ثوانٍ إضافية.

## مشاكل شائعة وحلولها

- **مخرجات فارغة** – تأكد من أن إحداثيات الـ viewport ضمن حدود الرسم؛ استخدم `CadImage.Size` للتحقق من الحدود.
- **طبقات مفقودة** – اضبط `CadRasterizationOptions.Layouts` إلى اسم التخطيط الصحيح؛ وإلا قد يكون التخطيط الافتراضي فارغًا.
- **تباطؤ الأداء** – عطل خاصية مضاد التعرج (anti‑aliasing) في `CadRasterizationOptions` إذا كنت تحتاج فقط إلى معاينة سريعة.

## أسئلة متكررة

### س1: هل يمكنني استخدام Aspose.CAD مع صيغ CAD أخرى؟

ج1: نعم، يدعم Aspose.CAD صيغًا متعددة بما فيها DWG، DXF، DWF، وأكثر من 20 نوع CAD إضافي.

### س2: هل Aspose.CAD متوافق مع .NET Core؟

ج2: نعم، يعمل Aspose.CAD مع .NET Framework و .NET Core وأحدث إصدارات .NET.

### س3: كيف يمكنني التعامل مع تخطيطات مختلفة في ملف DWG؟

ج3: حدد التخطيط المطلوب باستخدام خاصية `Layouts` في `CadRasterizationOptions` قبل عملية العرض.

### س4: هل هناك اعتبارات ترخيص لاستخدام Aspose.CAD؟

ج4: للحصول على تفاصيل الترخيص، زر [صفحة ترخيص Aspose.CAD](https://purchase.aspose.com/buy).

### س5: أين يمكنني العثور على دعم إضافي؟

ج5: زر [منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19) للحصول على مساعدة المجتمع والنقاشات.

### س6: هل يمكنني العرض مباشرة إلى PNG بدلاً من PDF؟

ج6: نعم، استبدل `PdfOptions` بـ `PngOptions` واستدعِ `image.Save("output.png", pngOptions)`.

### س7: كيف أدمج الصورة المعروضة في تطبيق Windows Forms؟

ج7: حمّل الصورة المحفوظة في عنصر تحكم `PictureBox` باستخدام `Image.FromFile("output.png")`.

## الخلاصة

أنت الآن تعرف كيفية **إنشاء viewport dwg c#** وعرض ملف DWG إلى PDF (أو صيغ رستر أخرى) باستخدام Aspose.CAD. من خلال إتقان تعديل الـ viewport ستحصل على تحكم دقيق في المخرجات البصرية، وهو أمر أساسي لإنشاء رسومات هندسية دقيقة، تقارير أو صور مصغرة. استكشف إعدادات الرستر الإضافية، جرب صيغ إخراج مختلفة، ودمج الشيفرة في خدمات .NET أكبر أو أدوات سطح المكتب.

---

**آخر تحديث:** 2026-08-23  
**تم الاختبار مع:** Aspose.CAD 24.11 for .NET  
**المؤلف:** Aspose

## دروس ذات صلة

- [كيفية ضبط Viewport أثناء تحويل DWG إلى PDF مع إحداثيات في C# - دليل Aspose.CAD](/cad/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/)
- [تعلم ضبط خيارات رستر CAD – تصدير تخطيطات محددة إلى PDF باستخدام Aspose.CAD](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)
- [كيفية تحويل DWG إلى PDF وصور رستر باستخدام Aspose.CAD لـ .NET](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}