---
date: 2026-03-16
description: تعلم كيفية تحويل ملفات DWG إلى PDF أو صور نقطية باستخدام Aspose.CAD لـ
  .NET. يغطي هذا الدرس خطوة بخطوة تحويل CAD إلى PDF تصدير ملفات DWG إلى صيغ صور مثل
  PNG ويظهر كيفية تصدير DWG إلى ملفات صور بكفاءة.
linktitle: Exporting DWG to PDF or Raster Images
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: كيفية تحويل DWG إلى PDF وصور نقطية باستخدام Aspose.CAD لـ .NET
url: /ar/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تصدير DWG إلى PDF أو صور نقطية - دليل Aspose.CAD

## مقدمة

إذا كنت بحاجة إلى **تحويل DWG إلى PDF** (أو إلى صيغ نقطية مثل PNG) مباشرةً من تطبيق .NET، فأنت في المكان الصحيح. في هذا الدرس سنستعرض الخطوات الدقيقة المطلوبة لاستخدام Aspose.CAD for .NET لإجراء التحويل، نشرح لماذا المكتبة خيار قوي، ونظهر لك كيفية التعامل مع كل من مخرجات PDF والصورة ببضع أسطر من الشيفرة.

## إجابات سريعة
- **ما المكتبة التي تتعامل مع تحويل DWG؟** Aspose.CAD for .NET  
- **هل يمكنني تصدير DWG إلى PNG بالإضافة إلى PDF؟** نعم – خيارات الترصيص نفسها تعمل لكلا الصيغتين.  
- **هل أحتاج إلى ترخيص للتطوير؟** النسخة التجريبية المجانية تعمل للاختبار؛ يلزم ترخيص تجاري للإنتاج.  
- **ما إصدارات .NET المدعومة؟** .NET Framework 4.5+، .NET Core 3.1+، .NET 5/6+.  
- **هل يتم التعامل مع تحويل الوحدات تلقائيًا؟** يمكنك تعريف نظام الوحدات يدويًا (متري أو إمبراطوري) كما هو موضح في الشيفرة.

## ما هو “تحويل DWG إلى PDF”؟

تحويل DWG إلى PDF يعني أخذ رسم CAD (DWG) وتحويله إلى مستند محمول للعرض فقط (PDF). هذا مفيد لمشاركة التصاميم مع أصحاب المصلحة الذين لا يمتلكون برنامج CAD، لإنشاء وثائق قابلة للطباعة، أو لأرشفة الرسومات بصيغة يمكن قراءتها عالميًا.

## لماذا نستخدم Aspose.CAD لهذا التحويل؟

- **بدون تبعيات خارجية** – المكتبة تعمل بالكامل في الكود المُدار.  
- **دقة عالية** – تحتفظ بالطبقات، وزن الخطوط، ومعلومات التخطيط.  
- **خيارات نقطية مدمجة** – تتيح لك التصدير إلى PNG، JPEG، BMP، إلخ، باستخدام كائن تكوين واحد.  
- **متعدد المنصات** – يعمل على Windows، Linux، و macOS مع .NET Core.

## المتطلبات المسبقة

قبل أن نبدأ الدرس، تأكد من توفر ما يلي:

- فهم أساسي لبرمجة .NET.  
- مكتبة Aspose.CAD for .NET مثبتة. إذا لم تكن كذلك، قم بتحميلها [هنا](https://releases.aspose.com/cad/net/).  
- بيئة التطوير المتكاملة (IDE) المفضلة لديك مُعدة لتطوير .NET.

## استيراد المساحات الاسمية

لنبدأ باستيراد المساحات الاسمية الضرورية في مشروع .NET الخاص بك. هذا يضمن حصولك على وظائف Aspose.CAD في الشيفرة.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
```

## الخطوة 1: تحميل ملف DWG

ابدأ بتحميل ملف DWG الذي ترغب في تحويله. استبدل `"Your Document Directory"` بالمسار إلى ملف DWG الخاص بك.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for loading DWG goes here
}
```

## الخطوة 2: إعداد تصدير PDF (كيفية تصدير DWG إلى PDF)

الآن، لنقم بتكوين إعدادات تصدير PDF. يوضح هذا المثال كيفية تحديد التخطيط ومعالجة تحويل الوحدات.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };

// Check and define the unit system
bool currentUnitIsMetric = false;
double currentUnitCoefficient = 1.0;
DefineUnitSystem(cadImage.UnitType, out currentUnitIsMetric, out currentUnitCoefficient);

// Your code for setting up PDF export goes here
```

## الخطوة 3: تصدير إلى PDF

نفّذ عملية التصدير إلى PDF باستخدام الإعدادات المكوّنة.

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath, pdfOptions);
```

## الخطوة 4: تصدير إلى صور نقطية (export dwg to image)

وسّع الوظيفة لتصدير إلى صور نقطية، مثل PNG.

```csharp
// A4 size at 300 DPI - 2480 x 3508
rasterizationOptions.PageHeight = 3508;
rasterizationOptions.PageWidth = 2480;

PngOptions pngOptions = new PngOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath.Replace("pdf", "png"), pngOptions);
```

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|----------------|------------|
| **صفحات فارغة في PDF** | لم يتم تحديد التخطيط بشكل صحيح | تأكد من أن `rasterizationOptions.Layouts` يتضمن اسم التخطيط الصحيح (مثال، `"Model"`). |
| **أبعاد غير صحيحة** | عدم توافق DPI أو حجم الصفحة | قم بضبط قيم `PageHeight` و `PageWidth` و DPI في `CadRasterizationOptions`. |
| **الوحدات تظهر بشكل غير صحيح** | لم يتم تعريف تحويل الوحدات | استخدم `DefineUnitSystem` لتعيين `currentUnitIsMetric` و `currentUnitCoefficient` بناءً على `cadImage.UnitType`. |
| **استثناء الترخيص** | حدود النسخة التجريبية | طبق ترخيصًا مؤقتًا أو دائمًا قبل استدعاء `Image.Load`. |

## الأسئلة المتكررة

### س1: هل يمكنني استخدام Aspose.CAD for .NET في مشاريعي التجارية؟
A1: نعم، يمكنك ذلك. زر [purchase.aspose.com/buy](https://purchase.aspose.com/buy) للحصول على تفاصيل الترخيص.

### س2: هل تتوفر نسخة تجريبية مجانية؟
A2: بالتأكيد! احصل على النسخة التجريبية المجانية [هنا](https://releases.aspose.com/).

### س3: كيف يمكنني الحصول على دعم Aspose.CAD for .NET؟
A3: توجه إلى [منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19) للحصول على دعم المجتمع.

### س4: هل يمكنني الحصول على ترخيص مؤقت لأغراض الاختبار؟
A4: نعم، يمكنك الحصول على ترخيص مؤقت [هنا](https://purchase.aspose.com/temporary-license/).

### س5: أين يمكنني العثور على الوثائق التفصيلية؟
A5: الوثائق متاحة على [Aspose.CAD](https://reference.aspose.com/cad/net/).

### س6: كيف يمكنني **حفظ CAD كـ PNG** بجودة عالية؟
A6: اضبط `PageHeight` و `PageWidth` إلى أبعاد البكسل المطلوبة واختر DPI بقيمة 300 أو أعلى في `CadRasterizationOptions`.

### س7: ما هي أفضل طريقة لـ **how to convert dwg** عندما يحتوي ملف المصدر على تخطيطات متعددة؟
A7: عَبِّ `rasterizationOptions.Layouts` بجميع أسماء التخطيطات التي تريد تصديرها، ثم كرّر عبر كل تخطيط واستدعِ `Save` لكل صيغة إخراج.

---

**آخر تحديث:** 2026-03-16  
**تم الاختبار مع:** Aspose.CAD 24.11 for .NET  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}